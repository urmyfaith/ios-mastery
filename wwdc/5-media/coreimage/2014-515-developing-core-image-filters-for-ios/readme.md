2014-515-developing-core-image-filters-for-ios/readme.md

# [2014 515 Developing Core Image Filters for iOS](https://developer.apple.com/videos/play/wwdc2014/515)

Alex, Tony


Key Concepts

Examples of writing Kernels

Platform Differences


## [1 Key Concepts](1-key-concepts.md) | |


## [2.1 Color Kernels - CIColorKernel](2.1-color-kernels-cicolorkernel.md) | |


## [2.2 Warp Kernels - CIWarpKernel](2.2-warp-kernels-ciwrapkernel.md) | 1630 | p103

### [More Complex Warp Kernel - Anamorphic stretch](2.2.1-more-complex-warp-kernel-anamorphic-stretch.md) | | p140


## [2.3 General Kernels - CIKernel](2.3-general-kernels-cikernel.md) | Tony Chu | 3119 | p200



Portability of General Kernels | 4323| p280

OS X and iOS

* Desktop-class kernel type with the same language syntax and semantics as OS X
* New built-in filters on iOS ported from OS X using general kernels


### Performance Considerations

Multiple render passes


### Intermediate Buffers

kCIContextWorkingFormat


### [Square Kaleidoscope](2.3.1-square-kaleidoscope.md)


Recommendations

* Write a general kernel only when needed
* Write a general kernel initially for rapid prototyping, then try replacing   with some combination of warp and color kernels

## 3 Platform Differences | 4840 | p315
