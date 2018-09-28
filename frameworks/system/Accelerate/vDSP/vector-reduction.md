- [Vector Reduction](vector-reduction.md)
  - [Vector Extrema Calculation](https://developer.apple.com/documentation/accelerate/vdsp/vector_extrema_calculation)
  - [Vector Average Calculation](https://developer.apple.com/documentation/accelerate/vdsp/vector_average_calculation)
  - [Vector Summation](https://developer.apple.com/documentation/accelerate/vdsp/vector_summation)


### [Vector Extrema Calculation](https://developer.apple.com/documentation/accelerate/vdsp/vector_extrema_calculation)

operation|base|single precision|double precision
---|---|---|---
Vector maximum value|maxv|vDSP_maxv|vDSP_maxvD
Vector maximum value with index|maxvi|vDSP_maxvi|vDSP_maxviD
Vector maximum magnitude|maxmgv|maxmgv|vDSP_maxmgvD
Vector maximum magnitude with index|maxmgvi|vDSP_maxmgvi|vDSP_maxmgviD
Vector minimum value|minv|vDSP_minv|vDSP_minvD
Vector minimum value with index|minvi|vDSP_minvi|vDSP_minviD
Vector minimum magnitude|minmgv|vDSP_minmgv|vDSP_minmgvD
Vector minimum magnitude with index|minmgvi|vDSP_minmgvi|vDSP_minmgviD

### [Vector Average Calculation](https://developer.apple.com/documentation/accelerate/vdsp/vector_average_calculation)

operation|base|single precision|double precision
---|---|---|---
Vector mean value|meanv|vDSP_meanv|vDSP_meanvD
Vector mean magnitude|meamgv|vDSP_meamgv|vDSP_meamgvD
Vector mean square value|measqv|vDSP_measqv|vDSP_measqvD
Vector mean of signed squares|mvessq|vDSP_mvessq|vDSP_mvessqD
Vector root-mean-square|rmsqv|vDSP_rmsqv|vDSP_rmsqvD


### [Vector Summation](https://developer.apple.com/documentation/accelerate/vdsp/vector_summation)

operation|base|single precision|double precision
---|---|---|---
Vector sum|sve|vDSP_sve|vDSP_sveD
Vector sum of magnitudes|svemg|[vDSP_svemg](https://developer.apple.com/documentation/accelerate/1450055-vdsp_svemg)|vDSP_svemgD
Vector sum of squares|svesq|[vDSP_svesq](https://developer.apple.com/documentation/accelerate/1450392-vdsp_svesq)|vDSP_svesqD
Sum of vector elements and sum of vector elements' squares|sve_svesq|[vDSP_sve_svesq](https://developer.apple.com/documentation/accelerate/1449978-vdsp_sve_svesq)|vDSP_sve_svesqD
Vector sum of signed squares|svs|[vDSP_svs](https://developer.apple.com/documentation/accelerate/1450006-vdsp_svs)|vDSP_svsD