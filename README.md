# Multisite test dataset with FreeSurfer volumes

This is simulated data created for test and demonstration purposes for decentralized algorithms for [COINSTAC](https://github.com/trendscenter/coinstac).

Each folder has a CSV file with the two columns of demographic data and a column of filenames containing the volumes of the regions of interest (ROIs) of the subjects' brains. These volumes are typically produced by segmentation using `recon-all` in the [FreeSurfer](https://surfer.nmr.mgh.harvard.edu) program.

Data dictionary
  - freesurferfile: filename associated with subject containing volumes of ROIs, as typically produced by FreeSurfer segmentation
  - age (float): subject's age
  - isControl (Boolean): whether subject was a control (True) or had a medical condition (False)

There are a total of 418 subjects, distributed over 5 sites. Below are the numbers of subjects at each site.
  - Site 1: 72
  - Site 2: 49
  - Site 3: 99
  - Site 4: 79
  - Site 5: 119

This data was created on Feb 2, 2017 by Jing Ming at the Mind Research Network.
