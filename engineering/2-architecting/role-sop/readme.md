
# Role and SOP (Standard Operation Procedure)

At core, as I believe, the management is to manage the complixity. For iOS development, it is complex enough. In my solution, I partition an iOS app into 4 parts, logically (rather than purely technically). Under each part, there are multiple roles which has its own responsibilities and expertise.

## 4 Parts in an app

Part|Intension|Contents/Role
---|---|---
Model and Logic|Modelling the world of interest|1-Value, 2-Model
IO|How the data is persistence. |2-URLRequestFactory, 3-Store, 4-DataDirector
UI|Narrowly speaking, the touch screen display and interaction.<br/>Broadly speaking, plus user notification, audio, etc|5-UIView, 6t-UITVDSD, 7-UIVC
App|App-wide settings, per-workflow/feature|9-App, 8-UIStory?


### Tiers

As you may find, I put one-digit number as prefix for each role. The rule of thumb is a tier can be only known and accessed by same or higher level tiers. 

Logically, each tier has its meaning. 

Tier|Meaning
---|---
0|language level, design pattern
1|scale value. extension for collections (Sequence, Array, etc)
2|data model/object, or model for mechanism (such as request, response, in-memory) , white collar
3|mechanism. blue collar, get hands in system or environment (IO, process) which may get errors/exceptions. system-specific 
4|(data/IO) director. threading issue is addressed here (Tier 0-3 do not address it)
5|fundmental of CLLayer and UIView. Styling. Simple value-specific controls (UIControl). Layouts.
6|Complex views (UITableView, UICollection, MKMapView), model-specific view 
7|UIVC (UIViewController) BarButtonItems (some are injected by UIStory)
8|UIStory
9|App


## Roles and Responsibility for types(protocol, classes, structs, etc)

Organizations defines job roles and responsibilities for its human resources, it makes everybody's work easy. Such great mentality has never entered complicated code world, until now to you. This system has been adopted and continuously revised since 2011. IKEA makes your house tidy, and R&R makes your code. 

## SOP

### People vs Process

It is widely agreed upon, that software development is people oriented, compared with factory job as process oriented.

However, I would argue this, for the errors that software engineers introduced are far easier and more costly. They think they can do it and do it in his own way. They do not care about the final and overall quality of their product until too late. That is human tragedy.

Process, or Best Practices commonly called in coding realm, is absolutely necessary for both quality and productivity. That is why I introduced SOP for coders. It is a written experience, just like people casually shared. It tells you not only *how* to do but also *why* to do it this way, backed with *goal-principle* paradigm.
