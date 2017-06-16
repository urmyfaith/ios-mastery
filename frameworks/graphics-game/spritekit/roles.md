
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

### Approaches

* creates a base ViewModel as it, then configure/decorate it. - who will be its delegate?
* subclasses the base ViewModel - self delegate?
* hires a ViewModel Creator/Factory. such as 5?-SKSceneCreator
  * ? or SKNodeCreator, or
  * SKSceneDecorator, or SKNodeDecorator ?


## 4?-SKNode - model-based
