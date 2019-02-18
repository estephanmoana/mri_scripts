# mri_scripts
### BASH scripts to process and analyze neuroimaging data using FSL and Freesurfer  
By Estephan Moana-Filho
February 18, 2019

These are BASH scripts I developed during my PhD to process and analyze MRI data using mainly FSL and Freesurfer (DTI-TK is also used by some scripts). These scripts were developed in a macOS environment, but they should be also compatible with BASH in Linux.  While these scripts were tested to the best of my knowledge, they should be seen as "in development" with no guarantee of working in other systems.

Required software:
- FSL: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki
- Freesurfer: https://surfer.nmr.mgh.harvard.edu/fswiki
- DTI-TK: http://dti-tk.sourceforge.net/pmwiki/pmwiki.php  

Edits to BASH profile are needed to include these scripts in your computer's PATH variable. See an example of a ".bash_profile" file for a macOS-based computer

------------------
\# FSL Setup
FSLDIR=/usr/local/fsl
PATH=${FSLDIR}/bin:${PATH}
export FSLDIR PATH
. ${FSLDIR}/etc/fslconf/fsl.sh

\# Freesurfer Setup
export FREESURFER_HOME=/Applications/freesurfer
source $FREESURFER_HOME/SetUpFreeSurfer.sh

\# DTI-TK Setup
export DTITK_ROOT=/Users/userX/mri_software/thirdparty_scripts/dtitk/dtitk-2.3.3-Darwin-x86_64
export PATH=${PATH}:${DTITK_ROOT}/bin:${DTITK_ROOT}/utilities:${DTITK_ROOT}/scripts

\# Adding path to custom-scripts written by Moana-Filho to PATH variable
PATH=$PATH:/Users/userX/mri_software/mri_scripts  

------------------

# Scripts Use
Once such BASH profile is available in the home directory of your computer, you initiate the main script by typing "mrianalysis_mainscript". It will offer a menu with (hopefully) self-explanatory options. You may want to explore a bit to understand the possibilities, and I highly recommend looking into the code of each script itself.