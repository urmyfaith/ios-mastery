

2017-606-whats-new-with-screen-recording-and-live-broadcast.md

# [2017 606 What's New with Screen Recording and Live Broadcast](https://developer.apple.com/videos/play/wwdc2017/606/)


ReplayKit 2


* In-App Screen
* iOS Screen Record Broadcast  
* Fast Camera Capture and Broadcast
* Pairing Switching


## [In-App Screen Capture](2017-606-1-in-app-screen-capture.md) - Johnny Trenh [4:45]

## [Live Broadcast](2017-606-2-broadcast.md) - Alexander Subbotin [16:36]


## Broadcast Pairing - Johnny Trenh - [30:55]

### Broadcast Pairing Flow

 Application - RPBroadcastActivity  ViewController - User Enters Broadcast  Information -  Broadcast Starts

```swift
 // Broadcast Pairing API
 class func load(withPreferredExtension preferredExtension: String?, handler: @escaping (RPBroadcastActivityViewController?, Error?) -> Void)
```  


```swift
func didPressBroadcastPairButton () {
RPBroadcastActivityViewController.load(withPreferredExtension:"com.conferenceApp.broadcastExten stion") { (broadcastAVC, error) in
  broadcastAVC?.delegate = self
  self.present(broadcastAVC, animated: true, completion: nil)
}
```

Broadcast Pairing

* Application provides extension bundleID
* User approves extension


## Fast Camera Switching [34:45]

* Front Camera and Back Camera switching
* Camera preview view available in RPScreenRecorder
* Subclass of UIView
* Developer is responsible for UI elements for fast switching

```swift
RPScreenRecorder.cameraPosition

public enum RPCameraPosition: Int {
  case front
  case back
}
```

```swift
func didPressCameraSwitch() {
  let sharedRecorder = RPScreenRecorder.shared()
  if (sharedRecorder.cameraPosition == RPCameraPosition.back) {
    sharedRecorder.cameraPosition = RPCameraPosition.front }
  else {
    sharedRecorder.cameraPosition = RPCameraPosition.back
  }
}
```

## Summary [37:45]

* In-App Screen Capture
* iOS Screen Record and Broadcast
* Broadcast Pairing
* Fast Camera Switching
