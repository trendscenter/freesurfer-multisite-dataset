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

The volumes were simulated with equations of the following form:

<img src="https://render.githubusercontent.com/render/math?math=y = \beta_0"> + 
<img src="https://render.githubusercontent.com/render/math?math=\beta_1 \cdot age"> + 
<img src="https://render.githubusercontent.com/render/math?math=\beta_2 \cdot isControl"> +
<img src="https://render.githubusercontent.com/render/math?math=\beta_3 \cdot \epsilon">

where <img src="https://render.githubusercontent.com/render/math?math=\epsilon ~ N(0, 1)">

Each volume was given a fixed intercept (<img src="https://render.githubusercontent.com/render/math?math=\beta_0">) (e.g., 48466.3 for Right-Cerebellum-Cortex). The effect of age (<img src="https://render.githubusercontent.com/render/math?math=\beta_1">) was selected randomly from the range [-300, -100], and the effect of diagnosis (isControl, <img src="https://render.githubusercontent.com/render/math?math=\beta_2">) was selected randomly from the range [500, 1000] for each pseudo subject. A standard unit Gaussian noise multiplied by a random index from the range [1800, 2200] was added subsequently.

This data was created on Feb 2, 2017 by Jing Ming at the Mind Research Network and presented in this paper:

Ming J, Verner E, Sarwate A et al. COINSTAC: Decentralizing the future of brain imaging analysis [version 1; peer review: 2 approved]. F1000Research 2017, 6:1512 (https://doi.org/10.12688/f1000research.12353.1)
