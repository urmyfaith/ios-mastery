


- [Vector-Scalar Arithmetic](vector-scale-arithmetic.md)
  - [Basic Arithmetic Functions](https://developer.apple.com/documentation/accelerate/vdsp/basic_arithmetic_functions)
  - [Multiply-Add Functions](https://developer.apple.com/documentation/accelerate/vdsp/multiply-add_functions)
  - [Multiply-Subtract Functions](https://developer.apple.com/documentation/accelerate/vdsp/multiply-subtract_functions)

x

operation|base|single precision|double precision|integer
---|---|---|---|---
Vector-scalar add|vsadd|vDSP_vsadd|vDSP_vsaddD|vDSP_vsaddi
real vector-scalar multiply|vsmul|vDSP_vsmul|vDSP_vsmulD
complex vector-scalar multiply|zvzsml|vDSP_zvzsml|vDSP_zvzsmlD
Vector scalar divide|vsdiv|vDSP_vsdiv|vDSP_vsdivD|vDSP_vsdivi
Divide scalar by vector|svdiv|vDSP_svdiv|vDSP_svdivD

## [Multiply-Add Functions](https://developer.apple.com/documentation/accelerate/vdsp/multiply-add_functions) and [Multiply-Subtract Functions](https://developer.apple.com/documentation/accelerate/vdsp/multiply-subtract_functions)

operation|base|single precision|double precision
---|---|---|---
real vector-scalar multiply and vector add.|vsma|vDSP_vsma|vDSP_vsmaD
complex vector-scalar multiply and vector add|zvsma|vDSP_zvsma|vDSP_zvsmaD
real vector-scalar multiply and scalar add|vsmsa|vDSP_vsmsa|vDSP_vsmsaD
real vector-scalar multiply, vector-scalar multiply, and vector add.|vsmsma|vDSP_vsmsma|vDSP_vsmsmaD
Vector-scalar multiply and vector subtract|vsmsb|vDSP_vsmsb|vDSP_vsmsbD


