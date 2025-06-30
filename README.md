# Human PVT Atlas: Histologically-Informed MRI Segmentation

This repository provides a publicly available, MRI-compatible atlas of the **paraventricular nucleus of the thalamus (PVT)** derived from histological and neuroanatomical landmarks. The mask is aligned to MNI152 (0.5 mm) space and is designed for use in in vivo human neuroimaging studies.

This atlas is provided in formats compatible with major neuroimaging toolkits (FSL, FreeSurfer, CIVET) to support broad adoption by the research community.

---

## Repository Structure

```
pvt_atlas/
├── data/
│   ├── PVT_mask_MNI152.nii.gz            # Core binary mask in MNI152 0.5mm space
│   ├── PVT_mask_FSL.nii.gz               # FSL-ready version
│   ├── PVT_mask_FreeSurfer.mgz           # FreeSurfer format
│   ├── PVT_mask_CIVET.mnc                # CIVET-compatible mask
├── figures/
│   ├── overview_pipeline.png             # [PLACEHOLDER: Upload pipeline diagram]
│   ├── mask_overlay_views.png            # [PLACEHOLDER: Upload mask overlay image]
├── examples/
│   ├── example_usage_fsl.sh              # Example FSL script
│   ├── example_usage_freesurfer.sh       # Example FreeSurfer script
├── LICENSE
└── README.md
```

---

## About the Atlas

- Derived from a **postmortem human brain** using high-resolution MRI (9.4T and 3T) and **calretinin immunohistochemistry**
- Aligned to **MNI152 (0.5 mm resolution)** using ANTs and FSL tools
- Provides greater posterior coverage than the Morel/Krauth atlas, consistent with cross-species anatomical reports

For full methods and validation, see the associated manuscript:  
**_"A combined neuroanatomy, ex vivo imaging, and immunohistochemistry defined MRI mask for the human paraventricular nucleus of the thalamus"_**  
[*Authors: Tetzlaff, Leonard, Yassa, Baram, Rasmussen*]

---

## How to Use

### FSL
```bash
fslmaths your_image.nii.gz -mas PVT_mask_FSL.nii.gz output_masked.nii.gz
```

### FreeSurfer
```bash
mri_mask your_image.mgz PVT_mask_FreeSurfer.mgz output_masked.mgz
```

### CIVET
Use `PVT_mask_CIVET.mnc` with standard MINC tools:
```bash
minccalc -expression 'A*B' your_image.mnc PVT_mask_CIVET.mnc output_masked.mnc
```

---

## Functional Validation

The mask has been validated using resting-state fMRI from the HCP 7T dataset. Connectivity maps generated using this mask are **highly consistent** with prior MRI-based PVT definitions (DSC > 0.84, R² > 0.85).

---

## Citation

If you use this atlas, please cite the associated publication:  
**[INSERT FULL CITATION HERE]**

---

## Feedback & Issues

If you encounter issues or have requests for additional formats, please open an issue or contact:  
**Jerod M. Rasmussen (rasmussj@hs.uci.edu)**
