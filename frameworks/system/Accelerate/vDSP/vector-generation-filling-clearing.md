
## Vector Generation, Filling, and Clearing

operation|base | single precision | double precision |fixed-point 1.15| fixed-point 8.24 format
---|---|---|---|---|---
vrampmul|vrampmul|func vDSP_vrampmul|func vDSP_vrampmul_s1_15|
Stereo version of vDSP_vrampmul|vDSP_vrampmul2|func vDSP_vrampmul2
vrampmuladd|vrampmuladd|vDSP_vrampmuladd
func vDSP_vrampmuladd2
Vector tapered ramp|vgen|func vDSP_vgen|func vDSP_vgenD
Vector generate by extrapolation and interpolation|vgenp|vDSP_vgenp|vDSP_vgenpD
Vector Generation with Lookup Tables|vtabi|vDSP_vtabi|vDSP_vtabiD


operation|base | single precision | double precision 
---|---|---|---
vramp | vDSP_vramp |func vDSP_vrampD
Vector tapered ramp|vgen|func vDSP_vgen|func vDSP_vgenD
Vector generate by extrapolation and interpolation|vgenp|vDSP_vgenp|vDSP_vgenpD
Vector Generation with Lookup Tables|vtabi|vDSP_vtabi|vDSP_vtabiD
vDSP_blkman_window|blkman_window|vDSP_blkman_window|vDSP_blkman_windowD
func vDSP_hamm_window|hamm_window|vDSP_hamm_window|vDSP_hamm_windowD
Vector clear|vclr| vDSP_vclr|vDSP_vclrD
Vector fill|fill|vDSP_vfill|vDSP_vfillD
Complex vector fill|zvfill|vDSP_zvfill|vDSP_zvfillD

Integer vector fill.  func vDSP_vfilli

