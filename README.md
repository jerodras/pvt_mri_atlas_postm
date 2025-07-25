# Human PVT Atlas: Histologically-Informed MRI Segmentation

This repository provides a publicly available, MRI-compatible atlas of the **paraventricular nucleus of the thalamus (PVT)** derived from histological and neuroanatomical landmarks. The mask is aligned to MNI152 (0.5 mm) space and is designed for use in in vivo human neuroimaging studies.

This atlas is provided in formats compatible with major neuroimaging toolkits (FSL, FreeSurfer, CIVET) to support broad adoption by the research community.

---

## Repository Structure

```
pvt_mri_atlas_postm/
├── data/
│   ├── PVT_Tetzlaff_Leonard_2025_0p5.nii.gz    # Core binary mask in FSL MNI152 0.5mm space
│   ├── PVT_Tetzlaff_Leonard_2025_fsaverage.mgz    # FreeSurfer format, in fsaverage space, partial-volumed at 0.2
│   ├── PVT_Tetzlaff_Leonard_2025_MNIICBM152NL2009cSym.mnc.gz    # CIVET-compatible mask in MNI-ICBM152 Nonlinear 2009c Sym space, partial-volumed at 0.2
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
