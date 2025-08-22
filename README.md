# DES Y3 Data for Cobaya Likelihoods

This repository contains data files for the DES Y3 cosmological analysis likelihoods in Cobaya.

## Contents

### For 3x2pt Analysis (`des_y3.three_by_two`)
- `likelihood/des-y3/y3_5x2_maglim_UNBLIND_07202021_120721_bestfit3x2.fits`
  - SACC-format FITS file containing 3x2pt data vectors, covariances, and tracers (n(z))
  - Used for the combined galaxy clustering + galaxy-galaxy lensing + cosmic shear analysis

### For Shear Ratio Analysis (`des_y3.shear_ratio`) 
- `likelihood/des-y3/shear_ratio/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate_sr.pkl`
  - Pickled Python object containing measured shear ratios, covariances, and angular bins
  - Used for the tangential shear ratio likelihood

## Data Provenance

**Original Source**: CosmoSIS Standard Library  
**Original Location**: `cosmosis-standard-library/likelihood/des-y3/`  
**Extraction Date**: August 22, 2025  
**Purpose**: Testing DES Y3 likelihood implementation in Cobaya

### File Checksums (SHA256)

```
d861b20a4edc59df55248be992dc0bda100363f194ea0abe0c4a5837683c2ff7  likelihood/des-y3/y3_5x2_maglim_UNBLIND_07202021_120721_bestfit3x2.fits
bc3c9d16a879f4809478b7c3ff59485ea90c34bdb620bdd7594037ead783b4e1  likelihood/des-y3/shear_ratio/2pt_NG_final_2ptunblind_02_26_21_wnz_maglim_covupdate_sr.pkl
```

## Scientific Reference

These data products correspond to the DES Year 3 cosmological analysis:

> Abbott, T. M. C. et al. (DES Collaboration), "Dark Energy Survey Year 3 results: Cosmological constraints from galaxy clustering and weak lensing", Phys. Rev. D 105, 023520 (2022), arXiv:2105.13549

## Usage in Cobaya

This data package is automatically downloaded when running:

```bash
cobaya-install des_y3.shear_ratio
# or
cobaya-install des_y3.three_by_two  
```

The likelihoods reference these files using the `{path}` variable in their YAML configurations.

## Migration Path

**Note**: This is a temporary testing repository under `handley-lab`. For production deployment, the data will be moved to the official `CobayaSampler/des_y3_data` repository following the same structure and format.