# WRFupdates
Research-level WRF module versions
module_bl_mynn_thaxton_xxx.F are modified versions of the WRF MYNN code to improve performance over complex terrain.

v01: - Lines 700: 706: Add conditional for bl_mynn_mixlength.GE.10 to enhance turbulent length scale, elt, across all domains (No flow conditional). alp1 = ( bl_mynn_mixlength-100.0 )/100.0

In MYNN code: zi = PBL height - how is this computed? ; transition layer = h1

See: line 884 el(k) = el(k)*(1.-wt) + elf * wt

See: line 859        wt=.5*TANH((zwk - (zi2+h1))/h2) + .5
