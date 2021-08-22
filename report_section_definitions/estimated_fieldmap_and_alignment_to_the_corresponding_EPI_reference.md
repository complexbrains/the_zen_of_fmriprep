### Estimated fieldmap and alignment to the corresponding EPI reference

 Note that for the seconds runs of the bart and rest tasks, there is another image called Estimated fieldmap and alignment to the corresponding EPI reference. This is because those runs had the magnitude/phasediff field maps applied to them, as opposed to spin echo field maps.

The estimated fieldmap was aligned to the corresponding EPI reference with a rigid-registration process of the magnitude part of the fieldmap, using antsRegistration. Overlaid on top of the co-registration results, the displacements along the phase-encoding direction are represented in arbitrary units. Please note that the color scale is centered around zero (i.e. full transparency), but the extremes might be different (i.e., the maximum of red colors could be orders of magnitude above or below the minimum of blue colors.)

If you see some laser beam kind of spreading activations especially through where the eyeballs are, these are the significant indication of the eye movements or due to the artefacts might have been caused due to the air pads between the tissues in forehead.            