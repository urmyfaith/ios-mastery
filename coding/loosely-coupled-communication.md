# Loosely Coupled Communication (Passive)

## First question to ask: if the intended listeners is one or many

* One
  * Speaker is a private component, managed by its creator or owner
* Many
  * Speaker is a public service, or a data model.

## Second question: Mechanism Choice

### To-One

* Protocol
  * Examples: [`UITableViewDataSource`](https://developer.apple.com/reference/uikit/uitableviewdatasource), [`UITableViewDelegate`](https://developer.apple.com/reference/uikit/uitableviewdelegate)
  * Cons: Boilerplate code on application side.
  * Cons: Wholesales mode. Even you are interested in a single event, you still have to adapt a protocol (leaving others no chance to adapt the same.)
* Block/Closure
  * Pros: Block can be created anywhere with its context.
  * Can be used as events of an object.
* Single Target-Action
  * Example: [`UIControl`](https://developer.apple.com/reference/uikit/uicontrol)
  * Guide: [Cocoa Application Competencies for iOS: Target-Action](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/TargetAction.html#//apple_ref/doc/uid/TP40009071-CH3)

### To-Many

* KVO
  * for model objects
  * Guide: [Key-Value Observing Programming Guide](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/KeyValueObserving/KeyValueObserving.html#//apple_ref/doc/uid/10000177i)
* NSNotification
  * for public services, such as [`UIApplication`](https://developer.apple.com/reference/uikit/uiapplication)
  * DO NOT FORGET to unregister observers when observer is `deinit`'ed or no longer interested in listening.
* Multiple Target-Action
  * Example: [`UIGestureRecognizer`](https://developer.apple.com/reference/uikit/uigesturerecognizer)


## Implementation Details.

### Target-Action

```swift
@objc private func action_play(_ sender: Any) {

}
```

### Notification


### KVO

```swift
'NSInternalInconsistencyException', reason: 'An instance 0x17000e730 of class CLHeading was deallocated while key value observers were still registered with it. Current observation info: <NSKeyValueObservationInfo 0x17003e1e0> (
<NSKeyValueObservance 0x17005aa30: Observer: 0x127e0a740, Key path: trueHeading, Options: <New: YES, Old: NO, Prior: NO> Context: 0x0, Property: 0x17005d040>
```
