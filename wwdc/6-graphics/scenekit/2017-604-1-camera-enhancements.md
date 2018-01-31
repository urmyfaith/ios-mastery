
## [Camera (~18:45)](2017-604-1-camera-enhancements.md)

### Demo - [Fox 2](https://developer.apple.com/sample-code/wwdc/2017/Fox2.zip)

follow character smoothly.

```swift

//Physically Based Camera

 // configure field of view...
  camera.fieldOfView = 60.0 //degrees

// ...or focal
camera.focalLength = 50.0  //mm
camera.sensorHeight = 24.0 //mm


```

configure the depth of field


```swift
camera.wantsDepthOfField = true camera.focusDistance = 0.8 //meters
camera.fStop = 5.6
```
// configure the camera for HDR
camera.wantsHDR = true

// configure the depth of field
camera.apertureBladeCount = 5

// Activate Motion Blur
camera.motionBlurIntensity = 1.0


###  Ambient Occlusion

```swift
// Activate SSAO
 camera.screenSpaceAmbientOcclusionIntensity = 1.0

// Configure SSAO
camera.screenSpaceAmbientOcclusionRadius = 5 //scene units
camera.screenSpaceAmbientOcclusionBias = 0.03 //scene units
camera.screenSpaceAmbientOcclusionDepthThreshold = 0.2 //scene units
camera.screenSpaceAmbientOcclusionNormalThreshold = 0.3
```

### Demo x3


## Camera Control

```swift
// turn on camera control
scnView.allowsCameraControl = true
// configure the camera control behaviour
scnView.defaultCameraController.interactionMode = .orbitTurntable scnView.defaultCameraController.inertiaEnabled = true scnView.defaultCameraController.maximumVerticalAngle = 45 //degrees
```


[`SCNCameraController`](SCNCameraController)

[`SCNCameraControllerDelegate`](https://developer.apple.com/documentation/scenekit/scncameracontrollerdelegate)


[`SCNCameraControlConfiguration`](https://developer.apple.com/documentation/scenekit/scncameracontrolconfiguration)


## Constraints

[API](https://developer.apple.com/documentation/scenekit/constraints)
