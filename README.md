# MSC_Thesis
Programs and Scripts created for my Master Thesis

Download c3d convert tool of ITK-Snap to preprocess images http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.C3D 


Download deeds-BCV from Heinrich, it is easily found using Google.

In deedsBCV-master folder:

landmarks_split_txt.py: splits the landmark coordinates provided in the original dataset into MRI and Ultrasound
landmarks_split_txt.py: calculates the center of mass of each sphere landmark, and calculates the euclidean distances between these centers.

example: src/deedsBCV -F img2_res.nii.gz -M img4_res.nii.gz -O nonlinear_2_4 -A affine_2_4_matrix.txt -S seg4_res.nii.gz

-F: fixed image
-M: moving image
-O: output file name
-A: affine matrix (output from applyBCV, which applies rigid + affine)
-S: mask file

In MIND-SSC folder:

MIND_descriptor.m and SSC_descriptor.m: generate the structural representations of the images.

In NiftyReg/reg-apps folder:

reg_aladin 

-ref (fixed image) 
-flo (moving image) 
-aff (name for the output affine matrix that the program will give (.txt)) 
-rmask (fixed mask) 
-res (output image name) 
-nac (choose whether to use the header of the image as initial alignment or not) 
-%v (percentage of blocks used form matching) 
-%i (inlier for LTS) 
-ln (number of pyramid levels) 
-maxit (max number of iterations, can be chosen for each pyramid level by repeating the command)


In Python folder:

Resample_Multichannel_Preprocessed.ipynb: used to reset the origin and orientation of the images after applying MIND/SSC.

Thresholding.ipynb: Used to generate the fixed masks

mutual_information_full.ipynb: calculate the MI between the images before and after preprocessing using MIND/SSC.


