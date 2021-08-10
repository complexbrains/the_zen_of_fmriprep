### Spatial noralization of the Anatomical T1w Reference

The MNI normalization report shows how successfully your T1w image(s) were resampled into standard space, for each of the template spaces used. (due to the use of the averaged template, the sulci is less pronounced and gyri to be wider on the template compared to T1w). If you used '--fs-no-reconall' flag to skip the surface based preprocessing then this section report will not be produced. 

Normalizing the scans to be used as map reference for surface reconstruction (this is essentially the “computerized” representation of the brain we are working with for analysis) which concludes the anatomical preprocessing step. Spatial normalization makes all different brain scans map onto one another: since human brains are different, we need to normalize so that the locations are consistent.

The red line encompasses the entire brain, the blue line encompasses white matter, and magenta encompasses the cerebral spinal fluid (CSF). This will give you an idea of the quality of the skull extraction

Note that cerebellum and brainstem are excluded from the surface reconstruction in fMRIPrep; the outlines will not therefore not include these areas.
