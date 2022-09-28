Here we have notebooks to de-noise matter fields as described in "De-noising non-Gaussian fields in cosmology with normalizing flows."

The notebooks load pre-trained flows for either periodic or non-periodic data in pretrained_flows directory.

Wiener filtering requires the power spectrum coefficients of the maps, which are provided in sample_test_data directory.

To reconstruct noisy 128 px periodic maps: run nbody_128px_mask_1p0_flow_and_wf.ipynb to to find the flow maximum-a-posterior (MAP) and do Wiener filtering on 100 test maps provided in sample_test_data directory. Then run quality_measures_128px_mask.ipynb to make power spectrum and cross-correlation plots with the results.

To reconstruct a noisy 384 px patched from 128 px maps: run nbody_384px_mapx_1p0_flow.ipynb to find the flow MAP, and nbody_384px_mapx_1p0_wf.ipynb to do Wiener filtering. Then run quality_measures_384px_mask.ipynb to patch together the 384 px map, and make power spectrum and cross-correlation plots with the results.

Requirements: numpy, scipy, matplotlib, PyTorch (we use version 1.11.0), imageio, Pk_library
