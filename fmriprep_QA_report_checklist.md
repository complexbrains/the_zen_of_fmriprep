# fMRIPrep Quality Analysis Report Checklist


| fMRIPrep Checklist/Subject ID   | Sub-001 | Sub-002  |
|:------ |:------- | --- |
| ID:|         |     |
| Structural:|         |     |
| Functional:|         |     |
| Standard output spaces:|         |     |
| Non-standard output spaces:|         |     |
| Freesurfer reconstruction:|         |     |
| **Error Tab**|         |     |
| Is there is any reported error?|         |     |
| **Structural Images**|         |     |
| Any missing data?|         |     |
| Data labelling matches?|     |     |                                       |Data dimension matches?          |     |
|Voxel Size matches?|         |     |
| Any discarded images?|         |     |
| [**Brain mask and brain tissue segmentation of the T1w**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/brain_mask_and_anatomical_temporal_CompCor_ROIs.md)|         |     |
| Grey matter outlines, magenta lines, are  correctly drawn?|         |     |
| White matter outlines, blue lines, are  correctly drawn?|         |     |
| Blue line follows the white/grey matter tissue boundary?|         |     |
| Red line follows the brain mask that covers the whole brain, not dura or any other outside of the brain?|         |     |
| Any intensity/non-uniformity artifacts? |         |     |
| [**Spatial normalization of the Anatomical T1w Reference**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/spatial_normalization_of_the_anatomical_T1w_reference.md) |         |     |
| The flipping before/after images are lined up? |         |     |
| The grey/white matter and anatomical landmarks (eg. ventricles) are lined up?  |         |     |
| White matter and pial surface boundary outlines do not cross or overlap each other?|         |     |
| Does any of the brain in the participant view look stretched or distorted?|         |     |
| **Surface Reconstruction:**|         |     |
| Grey matter outlines, magenta lines, are  correctly drawn?|         |     |
| White matter outlines, blue lines, are  correctly drawn?|         |     |
| Does red line outline the outer boundary of the grey matter and exclude the cerebellum?|         |     |
| **Functional Images**|         |     |
| Any note on on orientation: qform matrix overwritten?|         |     |
| Any non-steady state volumes?|         |     |
| Is there any mismatching parameters (TR, phase encoding direction, sequence details, slice timing, susceptibility correction,registration)? |         |     |
| TR? |         |     |
| PE direction?|         |     |
| Sequence?|         |     |
| Slice timing applied?|         |     |
| Susceptibility distortion correction? |         |     |
| Registration ?|         |     |
| Any Non-steady-state volumes? |         |     |
| [**Estimated fieldmap and alignment to the corresponding EPI reference**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/estimated_fieldmap_and_alignment_to_the_corresponding_EPI_reference.md)|         |     |
| Anything suspicious?|         |     |
| [**Susceptibility distortion correction** ](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/susceptibility_distortion_correction.md)|         |     |
| The distortion-corrected (or ???after???) image shows improved alignment between the brain and the GM/WM boundary, compared to the ???before??? image?|         |     |
| [**Alignment of functional and anatomical MRI data (surface driven)**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/alignment_of_functional_and_anatomic.md)|         |     |
| The BOLD and T1w images are aligned by following the image boundaries and anatomical landmarks (ventricles and corpus collosum)? |         |     |
| White and pial surface outlines (red and blue lines) appear to correspond well to the tissue boundaries in the functional images?|         |     |
| Some drop out in inferior brain regions (such as the OFC or medial temporal lobe) in functional images is somewhat inevitable. Depending on the type of analysis you???re doing and what you???re interested in, this may be more/less of an issue for you. If you see a lot of signal drop out, you will probably want to check the mask generated by fMRIPrep to see how that drop-out impacts the location and quantity of missing voxels in your mask. |         |     |
| [**Brain mask and (anatomical/temporal) CompCor ROIs** ](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/brain_mask_and_anatomical_temporal_CompCor_ROIs.md)|         |     |
| Does the brain mask outlined by the red contour remain outside the brain image?|         |     |
| Does the magenta lines remain inside the white matter/CSF?|         |     |
| [**Variance explained by t/aCompCor components**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/variance_explained_by_t_a_CompCor_components.md)|         |     |
| Anything suspicious? |         |     |
| [**BOLD Summary**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/BOLD_summary.md)|         |     |
| Investigate the big spikes in any of the line plots.|         |     |
| Review the carpet plot (the thing that looks like static that). This plot shows you the time series of each major tissue types. The blue column represents the voxels from cortical areas, orange column represents subcortical, green is for grey matter and cerebellum, and red for white matter and CSF. For any columns that all seem to have a jump in values, this will look like vertical bands or lines down the plot covers across the entire column for that time point. |         |     |
| [**Correlations among nuisance regressors**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/correlations_among_nuisance_regressors.md)|         |     |
| Investigate the highly correlated components.|         |     |
| [**ICA Components classified by AROMA**](https://github.com/complexbrains/the_zen_of_fmriprep/blob/main/report_section_definitions/ICA_components_classified_by_AROMA.md)|         |     |
| Anything suspicious?|   

### **References**

Please not that, these are entirely my own personal notes to myself to make sure I understand all these terminologies and concepts well enough before I claim any expertise on them, which I am in the making but not there yet. 

Therefore the definitions of the subsections in the report were taken as they are from the references below to make sure the definitions are reflected as they should be (to avoid any rephrasing related misdirection). However I will make sure in the close future that I will make them summarised. 

[fMRIPrep Guideline](https://fmriprep.org/en/stable/outputs.html)

[fMRIPrep Report Guideline](https://docs.google.com/document/d/1TE6ZWzNg8cDpvL4Vu0VGOZQLXkQ88Fa59AORzN01Avk/edit#)

[Identifying and removing widespread signal deflections from fMRI data: Rethinking the global signal regression problem](https://www.sciencedirect.com/science/article/pii/S1053811920301014)

[Using fmriprep for fMRI data preprocessing](https://medium.com/@gelana/using-fmriprep-for-fmri-data-preprocessing-90ce4a9b85bd)

[Andy's Brain Book](https://andysbrainbook.readthedocs.io/en/latest/OpenScience/OS/fMRIPrep.html)

[Neurostars fMRIPrep Questions](https://neurostars.org/search?q=fmriprep)

[Nipy - Nibabel](https://nipy.org/nibabel/coordinate_systems.html#naming-reference-spaces)

[fMRIPrep QA Guideline](https://github.com/complexbrains/fmriprep_qa_guide)
