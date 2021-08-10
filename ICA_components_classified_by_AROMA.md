### ICA Components classified by AROMA: 

fMRIprep only uses non-agressive ICA denosing (fits all regressors, and then re-adds the components attributed to the “signal” regressors) as a last step, which removes a lot less signal related varianve than aggressive denoising (detrending based on the regressors marked as “noise”). It generates non-aggresively denoised images. 


non-aggressive AROMA denoising is a fundamentally different procedure from its “aggressive” counterpart and cannot be performed only by using a set of noise regressors (a separate GLM with both noise and signal regressors needs to be used). Therefore instead of regressors, fMRIPrep produces non-aggressive denoised 4D NIFTI files in the MNI space:

*space-MNI152NLin6Asym_desc-smoothAROMAnonaggr_bold.nii.gz

!!! ICA-AROMA algorithm is trained to pick up motion artifacts specifically, so won’t take care of any physio-related denoising that needs to occur. For this, you may want to use the “aCompCor” regressors. Some people suggest that you also use the cosine regressors in the confounds.csv file if using “aCompCor” (or even if not - they perform high-pass filtering)

The number of ICA-AROMA components depends on a dimensionality estimate made by FSL MELODIC. For datasets with a very short TR and a large number of timepoints, this may result in an unusually high number of components. By default, dimensionality is limited to a maximum of 200 components. 

Aroma denoised files are called *_bold_space-MNI152NLin2009cAsym_variant-smoothAROMAnonaggr_preproc.nii

More reading on non-aggressive ICA https://github.com/oesteban/aroma-chris-notebook/blob/master/Denoising%2Bthe%2Bdenoising.ipynb

