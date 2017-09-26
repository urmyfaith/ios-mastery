

# [602 Adopting Metal, Part 1](https://developer.apple.com/videos/play/wwdc2016/602/)

2016/602-adopting-metal-part-1.md



Conceptual Overview
Creating a Metal Device Loading Data
Metal Shading Language
Building Pipeline States
Issuing GPU Commands

Animation and Texturing


```swift
// Creating a Sampler Object
let samplerDescriptor = MTLSamplerDescriptor()
samplerDescriptor.sAddressMode = .repeat
samplerDescriptor.tAddressMode = .repeat
samplerDescriptor.minFilter = .nearest
samplerDescriptor.magFilter = .linear
let sampler = device.newSamplerState(with: samplerDescriptor)

// Bind our texture so we can sample from it in the fragment shader
renderEncoder.setFragmentTexture(texture, at: 0)
// Bind our sampler state so we can use it to sample the texture in the fragment shader
renderEncoder.setFragmentSamplerState(sampler, at: 0)
```

```swift
fragment half4 fragment_lit_textured(
  VertexOut fragmentIn [[stage_in]],

  texture2d<float, access::sample> tex2d [[texture(0)]],
  sampler sampler2d [[sampler(0)]])
{
  
}
```
