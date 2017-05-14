# Software(iOS Apps) Quality


## Concepts

By and large, there are 2 kinds of software quality defects.

* Misbehavior (Bug)
  * Out of expectation. Wrong in logic, what is expected not happening, something unexpected happens.
  * Security and privacy threats.
  * Crash.
* Poor performance.
  * slow and irresponsive
  * run battery fast.
  * inefficient usage of power, network bandwidth, and other system resources.
  * short lived/Stability. after a period of time, it runs slowly or crashes.

### Activities

* Prevention
  * Requirement Verification and Performance Baseline
  * Architecting/Design (some principle and guideline to follow)
  * Architecture/Design Review
  * Coding (much more than following coding/naming style)
  * Code Review
  * Testing (Unit, Integration, Field)
* Cure
  * Debugging with Xcode and LLDB
  * (Performance) Profiling with Instruments
  * Process and Practice Improvement

### Side-topic: Complexity and Quality

As a common sense, when a thing is simple (in term of scope of feature/requirement and the number of developers getting involved.), quality-wise, it is hard to make it wrong, even it happens to get wrong, it is easy to fix it. For example, if you are writing a numeric calculator app, you are unlikely to run into multi-threading problem, compared with apps connecting to remote servers.

Comparatively consider this case below:
* a newly formed team of people work in a product;
* the existing code base is heterogeneity in programming languages and tool chains;
* the product has a dynamic and rich set of features,
* the product have to use many technologies, legacy and novel, home brewed and 3rd party;
* the product runs on variety of market, culture and geography, office and wilderness.

It is complicated and inherently hard for quality assurance. Complexity must worthy of being managed well, especially for the sake of product quality. Since this series of topic is on Quality, I will also address the topic of managing software complexity in architecture and coding practices to help.

## How to avoid quality defeats.

### Strategically, Prevention is better than cure

There are few means to hopefully prevent bugs, before writing code.
