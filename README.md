# Bipolar disorder - Brain map fMRI data
## Home assignment - Programming for Psychologists - 2024/2025

**Name:** Siri Onshuus Kågen

**Date:** 04/12/2024

**Student number:** 2860899

------------------------------------------------------------------------------------------

### Software:
The project was developed using the following tools:

- **Programming Language:** Python
- **Interactive Environment:** Jupyter Notebook
- **IDE:** Visual Studio Code
  
**Data source:** [https://neurosynth.org/analyses/terms/bipolar/]
<br/>

-------------------------------------------------------------------------------------------

## Table of contents
- **Description** (*of project*)
- **Files and folders in repository** (*explaination of files and folders found in this repository*)
- **Python packages**
- **Tips before you start**

--------------------------------------------------------------------------------------------

### Description
The goal of this programming assignment was to ......?

The data is from a term-based meta-analysis on 157 studies where the key term is bipolar disorder. Originally I hoped to do a comparison of one meta-analysis baseed on 130 studies, and the following meta-analysis on 157 studies. However, I did not have time for everything in the end, but the traces of my fanatasy are left behind. AKA the unneccessary add-on of "157" here and there. The numbers carry no significance past a reek of grappling passion for fancy 0s & 1s, and time-blind enthusiasm. I chose to both visualize the association data and the uniformity data, for my own curiosity, but also to showcase the difference in these types of data. Below I have included an explaination of the association test map and uniformity test map from the same source I acquired these data sets. 
<br/>
<br/>

_**Explaination of files:**_

The following explainations for the uniformity and association test maps are derived from NeuroSynth itself: 
[https://neurosynth.org/analyses/terms/bipolar/]

"*In brief, the _**uniformity test map**_ displays brain regions that are consistently active in studies that load highly on the term bipolar. Voxels with large z-scores are reported more often in studies whose abstracts use the term bipolar than one would expect them to be if activation everywhere in the brain was equally likely. Note that this is typically not so interesting, because it turns out that some brain regions are consistently reported in a lot of different kinds of studies (again, see our paper). So as a general rule of thumb, we don't recommend paying much attention to uniformity test maps.*

_**association test maps**_ *are, roughly, maps displaying brain regions that are preferentially related to the term bipolar. The association test map for bipolar displays voxels that are reported more often in articles that include the term bipolar in their abstracts than articles that do not. Most of the time this a more useful way of thinking about things, since association test maps tell you whether or not there's a non-zero association between activation of the voxel in question and the use of a particular term in a study.*"
<br/>

--------------------------------------------------------------------------------------------
<br/>

### Files and folders in repository:

_**NB!**_
If you take notice of the various DS_Store files added to practically every repository folder, this is due to me using a macOS system, and the files store metadata about the folder they are in (locally on my computer). I uploaded my project directly from Visual Studio Code to GitHub, and since I did not add a .gitignore file, these local project files tagged along. They are not important for this project, so please ignore them. I uploaded my project a little last minute since I waws mainly working locally, and I do not have time to remove them.
<br/>
<br/>

**fMRI files (folder):**
- *anatomical_157_nii*
    - Structural MRI scan of the human brain
- *association_157.nii*
    - Statistical map of brain regions (X, Y, Z) associated with bipolar disorder 
- *uniformity_157.nii*
    - Statistical map of activity in brain regions (X, Y, Z) associated with bipolar disorder 
<br/>
<br/>

**fMRI visualization images (folder):**
- *MAIN_Visualization (alternative 3).png*
    - A detailed visualization of the axial, saggital and coronal planes for both the association and uniformity values, presented in a 6 subplots figure. The voxel coordinates are different for each plane, to showcase and correspond to the highest Z-value of each data set. Some aesthetic changes were also done to the figure. Everything is further explained in the notebook, either in markdowns or along the code changes themselves. 
- *Overlay_Visualization(altnerative 1).png*
     - The most basic visualization plot, and the first I did.
- *SimpleSubplot_Visualization (alternative 2).png*
     - A subplot to visualize the data next to each other, at the same coordinates, rather than an overlay. 
  
<br/>
<br/>

**Histograms (folder):**
- *Histogram_MAIN (alternative 3).png*
    - The main histogram I want to be graded on, which has a cmap coloration which corresponds respectively to each brain fMRI image plot, and has a fitted curve and mean data point to easier read and understand the data when it is presented in a histogram plot. The x-axis values were also altered so they are centered underneath each respective bin, rather than just as a gliding value scale, since the x-axis represents (for the most part) quite specific uniformity/ association values
- *histogram (alternative 1).png*
  - The bare minimum histogram plot, which was my original histogram plot 
- *histogram (alternative 2).png*
  - The middle ground between the simple alternative 1, and the more complex alternative 3, which has an improved readability due to a fitted curve and mean data point. However, it takes more effort to see the correlation with the histogram plot due to simplistic, uniform coloring 
  
<br/>
<br/>

**Voxels data (folder):**
- *voxel_association_histogram.csv*
    - A CSV file containing the corresponding voxel coordinates (X, Y, Z) for each association value above 0 (and convieniently the ones used in the histogram)
- *voxel_full_data.csv*
    - A CSV file containing the corresponding voxel coordinates (X, Y, Z) for all uniformity and association values in the imported data files. Not visualized in a histogram or brain fMRI plot, but useful if wishing to compare uniformity and association data values at the same voxel coordinates. 
- *voxel_uniformity_histogram.csv*
    - A CSV file containing the corresponding voxel coordinates (X, Y, Z) for each uniformity value above 0 (and convieniently the ones used in the histogram)

<br/>
<br/>

**Additional files (without folder):**
- *Bipolar-fMRI notebook.ipynb*
  - Main coding branch for all code done to visualize the brain fMRI data and histograms 
- *Voxels - notebook.ipynb*
   - Notebook for code used to visualize and extract the voxel coordinates for the Z-values from the uniformity and association value data, by tying the voxel indices to MNI coordinates, and exporting them to a readable csv file. Further explained in the notebook markdowns. 
- *Pull request - Edurardo.png*
   - Screenshot of the pull request I did on Eduardo, where I applied cmap coloration to his histogram, and centered the xticks underneath each respective bin. I also simplified his folder path, as it seemed overly complicated for this type of project. 
- *Explaination_Association values.png*
    - A screenshot to visualize what the voxel coordinates from the CSV files found in the "Voxels data" folder actually correspond to by comparing them to the NeuroSynth webpage (where we extracted the data files). A randomly selected association value was chosen from the voxel_association_histogram.csv file. 
- *README.md*
    - This one ought to be rather self-explanatory. 

<br/>

--------------------------------------------------------------------------------------------
<br/>

### Python Packages used:
  - **os:** Operating system tasks (file paths, directories)
  - **nibabel:** Reading/writing neuroimaging data (e.g., NIfTI)
  - **nilearn:** Neuroimaging machine learning, statistical analysis, and visualization
      - from nilearn.plotting import _**plot_stat_map**_: Plot statistical maps on brain templates
  - **matplotlib:** Creating visualizations (plots, graphs)
      - _**matplotlib.pyplot**_: Simple interface for plotting
      - _**matplotlib.cm**_: Access color maps
      - _**matplotlib.colors**_: Advanced color handling for visualizations
  - **numpy:** Numerical computations and array manipulation
  - **panda:** Data manipulation and analysis
  - **scipy:** Advanced scientific computing
      - from scipy.optimize import _**curve_fit**_: Model fitting for experimental data
	
<br/>

--------------------------------------------------------------------------------------------
<br/>

### Tips before you start:

**Create customary kernel:**

It may be benefical to create a kernel which all the neccessary packages installed, so you won't have to worry about installation everytime you open VS Code. One way of doing this, is typing the following into a new terminal (run one line of code at a time):


     conda create -n fmri_env python=3.12.4 -y
*Tells conda to create a new python kernel with the given name, which is in this case fmri_env*

     conda activate fmri_env
*Tells conda to activate your new kernel, so the following installation can be done*

     pip install nilearn nibabel matplotlib numpy os panda scipy 
*Installs the Python packages directly into your new kernel*
