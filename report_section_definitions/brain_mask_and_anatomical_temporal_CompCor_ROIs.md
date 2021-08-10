### Brain mask and (anatomical/temporal) CompCor ROIs

BOLD brain mask with the aCompCor and tCompCor masks. The aCompCor mask (magenta outline) is a conservative CSF and white-matter mask for extracting physiological and movement confounds.  

The anatomical CompCor ROI (magenta contour) is a mask combining CSF and WM (white-matter), where voxels containing a minimal partial volume of GM have been removed.

The tCompCor mask (blue outline) contains the top 5% most variable voxels within a heavily-eroded brain-mask. In general, areas outlined by the blue lines should be areas with high CSF or blood flow, such as between the hemispheres, in ventricles, and between the cortex and the cerebellum. These are the most variable voxels, that will be used later on for functional component correction.