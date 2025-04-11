# analysis after competition

I attempted the ligand-pose challenge, but unfortunately, my success rate was around 40%.  
Upon reviewing the poses, I found that the average RMSD was 25Å !!   
This was because all the poses were aligned to SARS_ref, which likely caused all the MERS poses to fail.   
So, I caluculated transformation matrix by aligning reference SARS protein to reference MERS protein and just apply it to MERS docking pose.(not re-docking)  

```
[(-0.9992896914482117, -0.03497755900025368, -0.01402241550385952, -0.0644073740693093),
(-0.034628622233867645, 0.9991023540496826, -0.024399228394031525, 0.3994948081138987),
(0.014863253571093082, -0.023896321654319763, -0.9996039271354675, -0.0978587282480966),
(0.0, 0.0, 0.0, 1.0)]
```

## v3(before applying transformation matrix)
### success ratio:40%
<img width="231" alt="Image" src="https://github.com/user-attachments/assets/1facdc62-6c57-480e-8065-1f25ed74e2f0" />   

![Image](https://github.com/user-attachments/assets/3b80f972-e7c9-40d3-bba5-1b0916edfd46)


## v4(after applying transformation matrix)
### success ratio:70%
<img width="231" alt="Image" src="https://github.com/user-attachments/assets/591efa18-de91-45be-b87a-512e473740f9" />  

![Image](https://github.com/user-attachments/assets/f93211a6-6c22-4a81-9e57-43ce2a958c23)  

![Image](https://github.com/user-attachments/assets/45ec8a2e-0dec-4acd-a5bc-c15f947a76ce)  


## v4 but change the therthold of success from 2Å to 2.5Å
### success ratio:84%
<img width="231" alt="Image" src="https://github.com/user-attachments/assets/6c119719-76b4-474d-a3fe-e0b5faf8f8ce" />  



