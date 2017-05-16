# Software (iOS Apps) Quality


## Concepts

By and large, there are 2 kinds of software quality defects.

* Correctness. (Misbehavior, Bug)
  * Out of expectation. Wrong in logic, what is expected not happening, something unexpected happens.
  * Security and privacy threats.
  * Crash.
* Performance (Slow, inefficient)
  * slow and irresponsive
  * run battery fast.
  * inefficient usage of power, network bandwidth, and other system resources.
  * short lived/Stability. after a period of time, it runs slowly or crashes.

### Activities

Below contents are re-organized from [Process Overview](../process-overview.md), on quality.

* Prevention
  * Requirement Verification and Performance Baseline
  * Architecting/Design (some principle and guideline to follow) - Some performance issue are rooted here.
  * Architecture/Design Review
  * Coding (much more than following coding/naming style)
  * Code Review
  * Testing (Unit, Integration, Field)
* Cure
  * Debugging with Xcode and LLDB
  * (Performance) Profiling with Instruments
  * Process and Practice Improvement

### Side-topic: Complexity and Quality

I do not have to illustrate the point that the higher complexity of software the higher its impacts on quality. If you like to argue it, please see the article [Complexity](complexity).

This complexity of software is not only by the nature of the project, but also introduced through software architecting, e.g. it is a **man-made** problem. Someone may say, "my app is very small in scope, so that I have started coding straightaway. I have no architecture." This cannot be true, just like, not everyone can intellectually describe his own philosophy (that is philosopher's job), that does not mean he *has* no philosophy. As human being, everyone has its way of thinking. Back to software architecture, someone may never think of his software architecture intentionally, that may only mean his architecture is random or inconsistent over time, or not-comprehensive. That introduces unnecessary complexity.

Let me make it clear.
* The *architecting* phase is likely to introduce the *quality problem in complexity*.
  * The means of prevention and cure for such quality problem is *software analyzing/analysis*.
* That is different from the nature of quality problem introduced during *coding* phase, in which we
  * cure them through *debugging* and
  * prevent them through *coding best practice*, which in turn lays on *architecting*/*software design*.

There are boxful of software design tools to help us managing complexity. We will discuss that in [software-arch](../2-architecting) section.

## How to avoid quality defeats.

### Strategically, Prevention is better than cure

There are few means to hopefully prevent bugs, before writing code.
