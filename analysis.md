### analysis after competition

I attempted the ligand-pose challenge, but unfortunately, my success rate was around 40%.  
Upon reviewing the poses, I found that the average RMSD was 25Å !!   
This was because all the poses were aligned to SARS_ref, which likely caused all the MERS poses to fail.   
So, I caluculated transformation matrix by pymol and just apply MERS ligand pose not redocking.  

```
[(-0.9992896914482117, -0.03497755900025368, -0.01402241550385952, -0.0644073740693093),
(-0.034628622233867645, 0.9991023540496826, -0.024399228394031525, 0.3994948081138987),
(0.014863253571093082, -0.023896321654319763, -0.9996039271354675, -0.0978587282480966),
(0.0, 0.0, 0.0, 1.0)]
```



