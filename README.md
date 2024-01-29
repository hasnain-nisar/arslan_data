# LGG Segmentation Dataset

This dataset contains brain MR images together with manual FLAIR abnormality segmentation masks.
The images were obtained from The Cancer Imaging Archive (TCIA). This dataset is the subset of https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation. 
They correspond to 61 patients(16 CS: Case Western Reserve University & 45 DU: Duke University) included in The Cancer Genome Atlas (TCGA) lower-grade glioma collection with at least fluid-attenuated inversion recovery (FLAIR) sequence and genomic cluster data available.
Tumor genomic clusters and patient data is provided in `data.csv` file.


All images are provided in `.tif` format with 3 channels per image.
For 61 cases(16 CS: Case Western Reserve University & 45 DU: Duke University), 3 sequences are available, i.e. pre-contrast, FLAIR, post-contrast (in this order of channels).
Post-contrast sequence and pre-contrast sequence are missing for some cases.
Missing sequences are replaced with FLAIR sequence to make all images 3-channel.
Masks are binary, 1-channel images.
They segment FLAIR abnormality present in the FLAIR sequence (available for all cases).


The dataset is organized into 61 folders named after case ID that contains information about source institution.
Each folder contains MR images with the following naming convention:

`TCGA_<institution-code>_<patient-id>_<slice-number>.tif`

Corresponding masks have a `_mask` suffix.

SOURCES: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=5309188