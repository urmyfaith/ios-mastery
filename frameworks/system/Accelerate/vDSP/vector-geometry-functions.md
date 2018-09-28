- [Vector Geometry Functions](vector-geometry-functions.md)
  - [Vector-to-Vector Distance and Pythagorean Computation](https://developer.apple.com/documentation/accelerate/vdsp/vector-to-vector_distance_and_pythagorean_computation)
  - [Dot Product Calculation](https://developer.apple.com/documentation/accelerate/vdsp/dot_product_calculation)



### [Vector-to-Vector Distance and Pythagorean Computation](https://developer.apple.com/documentation/accelerate/vdsp/vector-to-vector_distance_and_pythagorean_computation)




operation|base|single precision|double precision
---|---|---|---
Vector distance|vdist|[vDSP_vdist](https://developer.apple.com/documentation/accelerate/1450257-vdsp_vdist)|vDSP_vdistD
Square of the Euclidean distance between two points in N-dimensional space, each defined by a real vector|distancesq|[vDSP_distancesq](https://developer.apple.com/documentation/accelerate/1450619-vdsp_distancesq)|vDSP_distancesqD
Vector Pythagoras|vpythg|[vDSP_vpythg](https://developer.apple.com/documentation/accelerate/1450824-vdsp_vpythg)|vDSP_vpythgD


### [Dot Product Calculation](https://developer.apple.com/documentation/accelerate/vdsp/dot_product_calculation)

operation|base|single precision|double precision
---|---|---|---
Computes the dot or scalar product of vectors A and B and leaves the result in scalar \*C|dotpr|vDSP_dotpr|vDSP_dotprD
Stereo variant of vDSP_dotpr|dotpr2|[vDSP_dotpr2](https://developer.apple.com/documentation/accelerate/1450752-vdsp_dotpr2)|vDSP_dotpr2D
Calculates the complex dot product of complex vectors A and B and leaves the result in complex scalar \*C|zdotpr|[vDSP_zdotpr](https://developer.apple.com/documentation/accelerate/1450701-vdsp_zdotpr)|vDSP_zdotprD
Calculates the conjugate dot product (or inner dot product) of complex vectors A and B and leave the result in complex vector C|zidotpr|[vDSP_zidotpr](https://developer.apple.com/documentation/accelerate/1450063-vdsp_zidotpr)|vDSP_zidotprD
Calculates the complex dot product of complex vector A and real vector B and leaves the result in complex vector C|zrdotpr|[vDSP_zrdotpr](https://developer.apple.com/documentation/accelerate/1450544-vdsp_zrdotpr)|vDSP_zrdotprD

