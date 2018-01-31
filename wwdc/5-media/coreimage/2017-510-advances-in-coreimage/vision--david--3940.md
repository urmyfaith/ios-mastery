## Vision - David - 3940


### Using Core Image with Vision

A|For example
--|--
Core Image can prepare images before being passed to Vision|Cropping, Orienting, Converting to grayscale
Vision can gather information before processing with Core Image| Feature detection can guide which CIFilters to apply



### Photo from Video with Removal of Unwanted Objects

* AVFoundation: Get the frames out of a short video
* Vision: Determine homography matrices to align frames
* Core Image: Align each video frame
* Core Image: Make a photo from the median of the aligned frames


### // Use Vision to find homographic registration and pass it to CI

### // Core Image Metal kernel to apply a homography matrix

```swift
float2 warpHomography(float3x3 h, destination dest) {
float3 homogeneousDestCoord = float3(dest.coord(), 1.0);
float3 homogeneousSrcCoord = h * homogeneousDestCoord;
float2 srcCoord = homogeneousSrcCoord.xy / max(homogeneousSrcCoord.z, 0.000001); return srcCoord;
}
```



## // Core Image Metal kernel to return the median of 5 images

```swift
inline void swap(thread float4 &a, thread float4 &b) {
float4 tmp = a; a = min(a,b); b = max(tmp, b); // swap sort of two elements
}

float4 medianReduction5(sample_t v0, sample_t v1, sample_t v2, sample_t v3, sample_t v4) {
// using a Bose-Nelson sorting network
swap(v0, v1); swap(v3, v4); swap(v2, v4); swap(v2, v3); swap(v0, v3); swap(v0, v2); swap(v1, v4); swap(v1, v3); swap(v1, v2);
return v2;
}
```

## Demo : Sky Gao - 4430


## Summary - David - 4824
