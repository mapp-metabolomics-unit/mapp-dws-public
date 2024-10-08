---
id: g3k3fvda7q4b1efq0j84eyg
title: Mzmine
desc: ''
updated: 1726643192191
created: 1726643166909
---


### Data processing 

The MS data were converted from .RAW (Thermo) standard data format to .mzML format using the MSConvert software, part of the ProteoWizard package (Chambers et al., 2012). The converted files were treated using the MZmine software suite v. 2.53 (Pluskal et al., 2010). The parameters were adjusted as follows: the centroid mass detector was used for mass detection with the noise level set to 2.0E4 for the MS level set to 1, and to 0 for the MS level set to 2. The ADAP chromatogram builder was used and set to a minimum group size of scans of 5, minimum group intensity threshold of 2.0E4, minimum highest intensity of 2.0E4, and m/z tolerance of 12 ppm (Myers et al., 2017). For chromatogram deconvolution, the algorithm used was the wavelets (ADAP). The intensity window signal‐to‐noise (S/N) was used as an S/N estimator with a S/N ratio set at 15, a minimum feature height at 2.0E4, a coefficient area threshold at 80, a peak duration range from 0.02 to 1.00 min and the retention time (RT) wavelet range from 0.02 to 0.05 min. Corresponding MS2 was paired with the following parameters (0.025 Da and 0.15 min). Isotopes were detected using the isotope peaks grouper with a m/z tolerance of 8 ppm, an RT tolerance of 0.08 min (absolute), the maximum charge set at 4, and the lowest m/z was used as the representative isotope. Peak alignment was performed using the join aligner method (m/z tolerance at 12 ppm), absolute RT tolerance 0.08 min, weight for m/z at 30, and weight for RT at 30. The aligned feature list (XXXX features) was exported using the export to Global Natural Product Social Molecular Networking (GNPS) Feature‐Based Molecular Network (FBMN) module. The MZmine parameters used for the data treatment are available at XXXXX