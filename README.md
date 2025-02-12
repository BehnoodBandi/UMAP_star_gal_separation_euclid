This repository is forked from https://github.com/toddlcook/UMAP-star-gal-separation

# UMAP star/gal separation
 
### Introduction
I've created this repo as a brief overview of the star/galaxy separation for the WAVES catalogue, described in [Cook et al. (2024)](https://arxiv.org/abs/2406.11611). 

The method uses UMAP (Uniform Manifold Approximation and Projection for Dimension Reduction), a method for non-linear dimensionality reduction, which has been deemed particulary effective in star/galaxy separation in the WAVES target catalogue, and is now being used as part of the pipeline.

For this tutorial, I utilise a subset of the G09 catalogue, which uses the same photometry and is processed in exactly the same way as the WAVES fields. 

The G09 data as well as the GAMA data used in these notebooks can be found in a Google Drive folder [here](https://drive.google.com/drive/folders/1HaKHaa_uZQPCnYF70e-btLDitqiIsXbe?usp=sharing).

It should be trivial to replace the G09 data with any other WAVES fields, should the code need to be re-run.

### Tutorial
You should run the notebooks in order of their numbers.

The first notebook (**1.G09_u.ipynb**) applies UMAP and uses HDBSCAN to conduct the star/galaxy separation with all available bands ($u-K_s$).

The second notebook (**2.G09_no_u.ipynb**) is exactly the same as the first, but without using the $u$-band (the most shallow and thus with the most missing data). 

The third notebook (**3.G09_combination.ipynb**) combines the labels generated by the previous two notebooks to create a new dataframe with the cluster labels.

Finally, the fourth notebook (**4.G09_analysis.ipynb**) conducts some cursory analysis of the sources according to our star/galaxy separation, and compares them to GAMA.


### Happy UMAPing! 
![UMAP corner](https://github.com/toddlcook/UMAP-star-gal-separation/blob/main/plots/UMAP_corner.jpg)
