# DES Y3 Data for Cobaya Likelihoods

This repository contains data files for the DES Y3 cosmological analysis likelihoods in Cobaya.

## Contents

### For 3x2pt Analysis (`des_y3_csl.three_by_two`)
- `likelihood/des-y3/2pt_NG_final_2ptunblind_02_24_21_wnz_covupdate.v2.fits`
  - DES Y3 TwoPoint FITS for the main sample (used by CSL 2pt_like)
- `likelihood/des-y3/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate.fits`
  - DES Y3 TwoPoint FITS for the maglim sample (optional)
- `examples/des-y3-scale-cuts.ini`
  - Scale cuts used in DES Y3 analyses (parsed by the CSL likelihood)

### For Shear Ratio Analysis (`des_y3_csl.shear_ratio`) 
- `likelihood/des-y3/shear_ratio/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate_sr.pkl`
  - Pickled Python object containing measured shear ratios, covariances, and angular bins
  - Used for the tangential shear ratio likelihood

## Data Provenance

**Original Source**: CosmoSIS Standard Library  
**Original Location**: `cosmosis-standard-library/likelihood/des-y3/` and `cosmosis-standard-library/examples`  
**Extraction Date**: August 2025  
**Purpose**: Testing DES Y3 likelihood implementation in Cobaya

### File Checksums (SHA256)

```
# TwoPoint FITS (main)
a72a8ee02fa72474ad859edab27d946991901e3d9a5bdc95cc9a961b244a32a6  likelihood/des-y3/2pt_NG_final_2ptunblind_02_24_21_wnz_covupdate.v2.fits

# TwoPoint FITS (maglim)
83efa43f6609ff07248b9c4e411b9ab386ec569cba402364fb21edff456e8b76  likelihood/des-y3/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate.fits

# Shear ratio pickles
08e22c501a4f2d12bb2205ed46650d2d772064cd6e5a7d68af1021fd68e628c5  likelihood/des-y3/shear_ratio/2pt_NG_final_2ptunblind_02_24_21_wnz_covupdate_sr.pkl
bc3c9d16a879f4809478b7c3ff59485ea90c34bdb620bdd7594037ead783b4e1  likelihood/des-y3/shear_ratio/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate_sr.pkl
```

## Scientific Reference

These data products correspond to the DES Year 3 cosmological analysis:

> Abbott, T. M. C. et al. (DES Collaboration), "Dark Energy Survey Year 3 results: Cosmological constraints from galaxy clustering and weak lensing", Phys. Rev. D 105, 023520 (2022), arXiv:2105.13549

## Usage in Cobaya

This data package is intended to be downloaded automatically when running:

```bash
cobaya-install des_y3_csl.shear_ratio
# or
cobaya-install des_y3_csl.three_by_two  
```

The likelihoods reference these files using the `{path}` variable in their YAML configurations.

## Migration Path

**Note**: This is a temporary testing repository under `handley-lab`. For production deployment, the data will be moved to the official `CobayaSampler/des_y3_data` repository following the same structure and format.
