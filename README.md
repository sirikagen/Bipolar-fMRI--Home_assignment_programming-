Association vs uniformity
https://neurostuff.github.io/compose-docs/tutorial/advanced/mkda_association

The association test maps tell you whether activation in a region XXX occurs more consistently for studies in your meta-analytic sample m than for other studies in the reference dataset. In other words, a large positive z-score implies that studies in a meta-analysis are more likely to report XXX activation than studies whose abstracts don't include the word 'emotion'.

Note that association maps do not tell you what the probability of a given psychological concept or task is. High Z-scores do not imply that a certain region or voxel is selective for a given concept or task. Instead, it just means there is evidence that there is at least a non-zero difference between reference studies, and studies in the meta-analysis.

-------------------------------------------------------------------------------------------------------

HOW TO WRITE A GOOD README
https://codingnomads.com/python-101-documentation-readme#:~:text=Contents,-Introduction&text=You%20can%20think%20of%20a,to%20take%20to%20run%20it.


It may be benefical to create a kernel which all the neccessary packages installed, so you won't have to worry about installation everytime you open VS Code. 

conda create -n fmri_env python=3.12.4 -y
conda activate fmri_env
pip install ......
!pip install nilearn 
!pip install nibabel
!pip install matplotlib 
!pip install jupyter 
!pip install numpy
!pip install seaborn
!pip install scipy

The data is from a term-based meta-analysis on 157 studies where the key term is bipolar disorder. Originally I hoped to do a comparison of one meta-analysis baseed on 130 studies, and the following meta-analysis on 157 studies. However, I did not have time for everything in the end, but the traces of my fanatasy are left behind. AKA the unneccessary add-on of "157" here and there. The numbers carry no significance past a reek of grappling passion for fancy 0s & 1s, and time-blind enthusiasm. 