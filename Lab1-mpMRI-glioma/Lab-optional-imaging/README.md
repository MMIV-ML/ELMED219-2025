# Digital imaging and image analysis (optional part)


### Before you start on this optional Lab on imaging (also introducing MRI and IMC):


#### Activate the environment (see local [`setup.md`](../../setup.md)):
```bash
conda activate elmed219
```

-------------------------

# Learning objectives

In the following series of Jupyter notebooks will explore **digital imaging** & **image analysis** and **multichannel imaging data** from two quite different **imaging modalities** (in terms of physical principles, spatial resolution, and invasiveness):
- **Magnetic Resonance Imaging** (MRI: see below)
- **Imaging Mass Cytometry** ([IMC](./IMC.md))

The notebooks will also illustrate the **generic nature of computational imaging** applied to data collection _in vivo_ and _in vitro_ and at different spatial scale.

----------
- [**00-test-installation.ipynb**](https://nbviewer.jupyter.org/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/00-test-installation.ipynb) (requires local installation, cf. `environment.yml` and `setup.md`)

- [**01-imaging-intro.ipynb**](https://nbviewer.jupyter.org/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/01-imaging-intro.ipynb)<a href="https://colab.research.google.com/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/01-imaging-intro.ipynb">
<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

The notebook will download illustrative **assets** from Google Drive cloud:
```
Lab-optional-imaging% tree assets
assets
├── 0.0-test_nifti.nii.gz
├── 3DT1_spgr_out_of_phase_2_2_mov.gif.png
├── abdominal_ct_fov.png
├── binary_mathematical_morphology.png
├── BMED_360_Damond_etal_2019_Tab1_IMC_panel.png
├── BMED_360_Lec1_introduction_mri_ip_CNR.png
├── BMED_360_Lec1_introduction_mri_ip_image_space_feature_space.png
├── BMED_360_Lec1_introduction_mri_ip_measuring_noise.png
├── carbohydrate_diet_dobson_tab_6_3.csv
├── chaddad_etal_2018_fig1.png
├── colocalization.png
├── convolution_filtering.png
├── Coordinate_systems.png
├── coordinate_transformation.png
├── Damond_etal_2019_donor_6126_E08_6x6.png
├── Damond_etal_2019_donor_6126_E08.png
├── Damond_etal_2019_donor_6126_E08_pycaret_kmeans_2.png
├── Damond_etal_2019_Fig1.jpg
├── Damond_etal_2019_Fig_S2A.png
├── Damond_etal_2019_Graphical_abstract.png
├── Damond_etal_2019_Tab1_IMC_panel.png
├── Damond_etal_2019_TabS1_Clin_data.png
├── dess_060.dcm
├── digital_imaging.png
├── fisp_060.dcm
├── flash_060_brain_mask.png
├── flash_060.dcm
├── flash_060_training_mask_6cla.png
├── image_classification_and_segmentation.png
├── image_restoration.png
├── images_as_matrices.png
├── image_tensors.jpg
├── intensity_transformations.png
├── kidney_slice10_frame10_roi_avi_ezgif.com-video-to-gif.gif.png
├── knn_illustration.png
├── mpMRI_figure_pptx.png
├── multispectral_mri_cnr_table.png
├── multispectral_tissue_classification_pptx.png
├── noise_in_mr_images.png
├── noise-in-MRI.png
├── pixel_density_ppi.png
├── pixel_grid.png
├── psif_060.dcm
├── test_view_img_on_surf.png
├── tmsk_and_roi_on_flash_freeview.png
├── tmsk_on_channels_freeview_pptx.png
├── view_img_on_surf.png
├── volume_rendering.png
└── Zebra_running_Ngorongoro.jpg
```
- [**02-mri-intro.ipynb**](https://nbviewer.jupyter.org/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/02-mri-intro.ipynb)<a href="https://colab.research.google.com/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/02-mri-intro.ipynb">
<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

<!--
- [**00-get-mri-imc-data.ipynb**](https://nbviewer.jupyter.org/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/00-get-mri-imc-data.ipynb) <a href="https://colab.research.google.com/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/00-get-mri-imc-data.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
-->

The notebook will download illustrative IMC and MRI data from Goggle Drive cloud:

```
Lab-optional-imaging% tree data
data
├── 00-test-data.csv
├── 00-test-nifti.nii.gz
├── imc
│   ├── E08_a0_full.csv
│   ├── E08_a0_full.tiff
│   └── table1_IMC_panel_37x4.csv
└── mri
    ├── 0.0-test_nifti.nii.gz
    ├── brain_roi_mask.nii.gz
    ├── BraTS20
    │   ├── BraTS20_Training_002_flair.nii.gz
    │   ├── BraTS20_Training_002_HDGlioSeg.nii.gz
    │   ├── BraTS20_Training_002_seg.nii.gz
    │   ├── BraTS20_Training_002_t1ce.nii.gz
    │   ├── BraTS20_Training_002_t1.nii.gz
    │   └── BraTS20_Training_002_t2.nii.gz
    ├── dess_060.dcm
    ├── dess_060.nii.gz
    ├── fisp_060.dcm
    ├── fisp_060.nii.gz
    ├── flash_060_brain_mask.png
    ├── flash_060.dcm
    ├── flash_060.nii.gz
    ├── flash_060_training_mask_6cla.png
    ├── mni_icbm152_t1_tal_nlin_sym_09c.nii.gz
    ├── multispectral_mri_training_data.csv
    ├── psif_060.dcm
    ├── psif_060.nii.gz
    └── training_mask_1_6.nii.gz
```

- [**03-imc-intro.ipynb**](https://nbviewer.jupyter.org/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/03-imc-intro.ipynb)<a href="https://colab.research.google.com/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioma/Lab-optional-imaging/03-imc-intro.ipynb">
<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>  (see also `IMC.md`)

<!--
```
% tree data
data
├── imc
│   ├── E08_a0_full.csv
│   ├── E08_a0_full.tiff
│   ├── E08_a0_panel_data_and_channel_numbering.csv
│   └── table1_IMC_panel_37x4.csv
└── mri
    ├── 0.0-test_nifti.nii.gz
    ├── brain_roi_mask.nii.gz
    ├── dess_060.dcm
    ├── dess_060.nii.gz
    ├── fisp_060.dcm
    ├── fisp_060.nii.gz
    ├── flash_060.dcm
    ├── flash_060.nii.gz
    ├── flash_060_brain_mask.png
    ├── flash_060_training_mask_6cla.png
    ├── mni_icbm152_t1_tal_nlin_sym_09c.nii.gz
    ├── multispectral_mri.nii.gz
    ├── multispectral_mri_training_data.csv
    ├── multispectral_mri_training_data_from_nifti_mask.csv
    ├── psif_060.dcm
    ├── psif_060.nii.gz
    └── training_mask_1_6.nii.gz
```

- [**01-mri-intro.ipynb**](https://nbviewer.jupyter.org/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/01-mri-intro.ipynb) <a href="https://colab.research.google.com/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/01-mri-intro.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>


- [**02-mri-multispectral.ipynb**](https://nbviewer.jupyter.org/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/02-mri-multispectral.ipynb) <a href="https://colab.research.google.com/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/02-mri-multispectral.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>


- [**03-mri-snr-cnr.ipynb**](https://nbviewer.jupyter.org/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/03-mri-snr-cnr.ipynb) <a href="https://colab.research.google.com/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/03-mri-snr-cnr.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- [**04-imc-Introductory.ipynb**](https://nbviewer.jupyter.org/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/04-imc-intro.ipynb) <a href="https://colab.research.google.com/github/computational-medicine/BMED360-2021/blob/main/Lab1-MRI/04-imc-intro.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

-->

----------------

## Sources of information related to MRI principles and applications

### Introductory videos
- **How Does an MRI Scan Work?** 1:20 (https://youtu.be/1CGzk-nV06g)
- **MRI vs. CT** 2:31 (https://youtu.be/aQZ8tTZnQ8A)
- **Brain MRI scan protocols, positioning and planning** 9:34 (https://youtu.be/R5LQzoFynqI)
- **MRI: Basic Physics & a Brief History**  25:51 (https://youtu.be/djAxjtN_7VE)
- **Bergen fMRI group - the birth of a research group** 19:45 (https://youtu.be/6UhfAX3RusE)

### Awesome Magnetic Resonance Imaging (MRI)
 - **A curated list of delightful Magnetic Resonance courses, books, lectures, papers, blogs and free resources** by Daniel Gomez, Donders Institute for Brain, Cognition and Behaviour (https://github.com/dangom/awesome-mri)
 - **MRIMASTER.COM** (https://mrimaster.com)

### Simulators and more

- **The (web) compass simulator** from the Danish Research Centre for Magnetic Resonance and TDU  (http://www.drcmr.dk/CompassMR)
- **The (web) [Bloch simulator](http://drcmr.dk/new-bloch-simulator)** from the Danish Research Centre for Magnetic Resonance and TDU (http://drcmr.dk/BlochSimulator)
- **MRiLab** A Numerical Magnetic Resonance Imaging Simulation Platform in MATLAB by Fang Liu (https://github.com/leoliuf/MRiLab)

- **MRI-education-resources** UCSF Peder Larson Research Group (https://github.com/LarsonLab/MRI-education-resources) _Highly recommended_

- **Pulse sequence graphics** by Daniel Gomez (https://github.com/dangom/mr-sequence-diagrams/blob/master/README.org)


----------------------

### To relax and enjoy digital and biological vision (in spare time) - see

**Enhanced Pixel Examination** [try it [here](https://pixspy.com)] and 
[this webpage](https://michaelbach.de/ot) containing demos of many beautiful and fascinating optical illusions and visual phenomena. Professor Michael Bach gives detailed descriptions of these phenomena also from a theoretical perspective.
Even more interested? see https://foundationsofvision.stanford.edu by Prof. Brian A. Wandell at Stanford.
