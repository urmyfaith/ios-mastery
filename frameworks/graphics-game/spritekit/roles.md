
## 6-SKViewManager

* is created by, usually UIVC
* connects with its view, via `setupSKView(_:)`
  * set up view, such as `view.showsFPS = true`
* disconnects with its view, via `teardownSKView(_:)`
* accommodates model object and observes it
* creates it view model, SKScene in SpriteKit
* assigns view model to view (skView.present(scene))
* loads or creates demo data, then passes to scene. (don't let scene to create demo data)


## 5?-SKScene

### Issues

* defining scene's size
* add children from different scale, etc.
  * call `setScale`, and set `zPosition`
* scene is created and presented before data is ready/assigned.


### Approaches

* creates a base ViewModel as it, then configure/decorate it. - who will be its delegate?
* subclasses the base ViewModel -
  * self delegate? / no need to be self-delegate, since scene has `did`-prefixed methods for same events as delegate methods.
* hires a ViewModel Creator/Factory. such as 5?-SKSceneCreator
  * ? or SKNodeCreator, or
  * SKSceneDecorator, or SKNodeDecorator ?

## 5?-SKSceneCreator


## 5?-SKSceneDecorator

scene decorator comes with a set of settings, to decorate a given scene. Such settings are mutable. so be prepared to accommodate the update after decorateScene has been called.

you can regard this as a way to organize layers of nodes. for example, user can toggle the visibility of group of nodes easily.

* setup and teardown pairs



## 4?-SKNode - model-based
