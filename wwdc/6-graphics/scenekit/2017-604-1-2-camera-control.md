
## Camera Control - Thomas Goossens [12:40]

### Object inspection and scene browsing

Previously
* Directly manipulate the camera position, rotation or transform
* For debugging use allowsCameraControl API


* Introducing SCNCameraController
* Built-in support for common controls modes
* Default camera controller provided by SCNView



```swift
// turn on camera control
scnView.allowsCameraControl = true
// configure the camera control behaviour
scnView.defaultCameraController.interactionMode = .orbitTurntable scnView.defaultCameraController.inertiaEnabled = true scnView.defaultCameraController.maximumVerticalAngle = 45 //degrees
```

name| description
--|--
Orbit Turntable
Orbit Arcball|doesn't prevent roll
Orbit Angle Mapping
Fly| lap scene
Pan
Roll
Frame nodes
Dolly
Inertia
Truck




orbitTurntable

orbit Arcball







[`SCNCameraController`](SCNCameraController)

[`SCNCameraControllerDelegate`](https://developer.apple.com/documentation/scenekit/scncameracontrollerdelegate)


[`SCNCameraControlConfiguration`](https://developer.apple.com/documentation/scenekit/scncameracontrolconfiguration)

### Camera with a behavior

Chain SCNConstraint objects to define a camera behavior

#### 4 old

SCNLookAtConstraint / SCNTransformConstraint / SCNBillboardConstraint / SCNIKConstraint

#### 5 new

constraint | description
--|--
SCNDistanceConstraint
SCNReplicatorConstraint
SCNAccelerationConstraint
SCNSliderConstraint
SCNAvoidOccluderConstraint



## Constraints

[API](https://developer.apple.com/documentation/scenekit/constraints)


### Node manipulation helpers

Math helpers on SCNNode for common transformations Vector conversion from node to node
SCNNode transforms properties available as SIMD types

```swift
// Working with SIMD
aNode.simdPosition += aNode.simdTransform * anotherNode.simdPosition
```

simd limitation:

* not KVC, KVO compliant
* not be included as an NSValue.
