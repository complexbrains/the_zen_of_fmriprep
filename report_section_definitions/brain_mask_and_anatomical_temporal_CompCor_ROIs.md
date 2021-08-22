### Brain mask and (anatomical/temporal) CompCor ROIs

BOLD brain mask with the aCompCor and tCompCor masks. The aCompCor mask (magenta outline) is a conservative CSF and white-matter mask for extracting physiological and movement confounds.  

The anatomical CompCor ROI (magenta contour) is a mask combining CSF and WM (white-matter), where voxels containing a minimal partial volume of GM have been removed.

The tCompCor mask (blue outline) contains the top 5% most variable voxels within a heavily-eroded brain-mask. In general, areas outlined by the blue lines should be areas with high CSF or blood flow, such as between the hemispheres, in ventricles, and between the cortex and the cerebellum. These are the most variable voxels, that will be used later on for functional component correction.

What we are interested in is the grey matter in general and what we do not analyse is the white matter and CSF. So these outlines here try to estimate the voxels that are not belong to the grey matter that takes, signal, time course to regress their influences out of the model. 

The blue lines, the temporal components, are the voxels that reflect very high fluctuation. Because what you would expect in mri, like a linear trend, like how the things changes related to your paradigm, because of the magnetisation, and people attend to what is happening in your paradigm , like fatigue and all these things. But if these are voxels they fluctuate a lot, and then basically, if you would run a model on it, you would see that those voxels are not fluctuating based on your paradigm, but due to other noise interfere with your data, so these voxels let you to know about these high variation for you to exclude them from your model. 

Usually these blue voxel sets are seen close to the border of the brain or border between the tissues, that might be correlated with the movements, or fluctuate that is not much based on the task but more like a some different reasons than the task related modification, hence the noise.  