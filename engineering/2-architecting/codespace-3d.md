
# 3 Dimensions of (Software) Code Space.

## Objectives

* Make code space well organized.
  * for ease and productivity of human Engineers
  * for quality of code and software, managing complexity.
    * reusability / robustness (ease of debugging) /
* Specific on iOS apps development. General

## 3 Axes


Axis | Dimension | Type of Requirement | Description | Who is concerned
--|----|----|----|---
X| Width of Business | Functional | Product's functionality/feature and procedure | product designers, clients, and users
Y| Height of Arch | Non-Functional <br/> Global | Follow the tech trends. In iOS, follow and learn new features of each iOS versions. <br/> Technical issues such as Performance and Security, that non-technical may not address on, is our hardcore area to demostrate technical maturity.| technologist/engineer
Z | Depth of Engineering | Global | Code Reusability <br/> Proven Quality <br/> Configuration Over Programming | software architect

### Width of Business

### Height of Architecture

For UIKit, as you know, there are logical layers of CALayer (lower) - UIView - UIViewController - UIApplication (higher). On each layer, there is rich and different set of API, usage and concerns. By the nature of these layers, you should split your code into the right class, rather than writing everything in UIViewController subclass. Since it is hierarchical, you must hold the rule that lower level is ignorant of the higher level, its creator, owner and user. In arguable cases of the lower knows the higher, the lower should hold a __weak__ reference to higher.


### Depth of Engineering

One of simple case of it is to apply [Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle) in your software. That will break code into due classes, and decouple from bidirectional relationship.


## Per-axis professional growth strategy/guideline

This is about people, not only on his knowledge and skill sets which can be learnt and trained, but also his personality to fit the job.



## Business

Pay attention on details of domains, such as branch cases of workflow, exception of rules.


### Technologist



One problem I saw in China iOS developer community, is people are more interested in framework-wrapper or syntax sugar open source projects, rather than any that provide functional feature contributing to value-added products.

If you are a developer for car navigation app, do you know CoreMotion's [`CMMotionAcivityManager`](https://developer.apple.com/reference/coremotion/cmmotionactivitymanager), or make it useful in your app?



### Engineering

Excellence of structural (rather than functional).

Elegance of design. (Using Rest'ful API, with HTTP original intents)

[Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)

[SOLID Principles](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design))

[UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language), visualized design tool.

[Software Analysis], home-brew
