

## Types of Software Defeats and Their Root Causes


* Value/Calculation
* complexity of your software architecture.
* OS interaction (misunderstanding on OS framework usage)
* User,  environment


## 3 Aspects of Quality Assurance

* (Pre-code) Design
* Coding
* (Post-code) Tools (Testing, Debugging with Xcode/LLDB, Profiling with Instruments)



## Swift Coding

* use enum and switch, if appropriate, for exhaustive value choice/range, rather than Int or String.
* Restricting [Access Control](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID3). For access modifiers, starting with private or fileprivate. Open up (to internal, public, or open) only when necessary
* As a caller, if at your scope,
  * handle Optional's nil-ness of callee's return or inout parameters. Do not use force unwrapping or force casting (as!)
  * handle error thrown by callee, with all related error types. Do not use force try (try!)
* As a callee method, you should declare throws, for any uncertainties of inputs or environment. Do not over-promise that something you may not accomplish due to context constraints. such as Internet reachability, or error thrown by underneath functions, that your caller is at better position to handle.
* Write Generic to reduce unnecessary code duplications.

## Cocoa Coding

* pair registration-unregistration as an observers of NotificationCenter, KVO, Target-Action.
