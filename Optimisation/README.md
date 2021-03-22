__Optimisation Code__

This includes all of the optimisation files created over several generations. Most is legacy code.

Compton Optimisation is a re-write of the Compton Master notebook for the fixed bandwidth optimisation technique.
It is re-wrote to be more conducive to Mathematica's style. It runs quicker and is capable of doing more precise optimisations.

Compton Master is still functional code. It contains an optimisation to show the possible adjustment for small changes in energy spread.

[UPDATE 2020] The Compton_Optimisation round beam code uses the *RMS* Ranjan et al bandwidth and flux by Curatolo et al. The Curatolo et al flux calculation has since been found to be deficient as this is based upon an outdated bandwidth, that was disproved by Ranjan et al. The code has been parallelized and can operate, using multiple Kernels, on the apsv2 server. Finally, it has been modified to also include the hourglass effect and angular crossing effect via Miyahara's luminosity reduction factors.  

[UPDATE 22/03/2021] The RMS_FWHM_Compton_Optimisation notebook is the 'gold standard' round beam Compton optimisation at the moment. This includes full derivations for both the *RMS* case (Ranjan et al bandwidth) and the *FWHM* case (modified Ranjan BW). The *FWHM* case has mostly been used to benchmark the F_0.1% bandwidth flux calculation, as first derived by Geoff Krafft. This code still uses parallel processing on apsv2 in order to speed up the optimisation. The RMS_FWHM_Compton_Optimisation also takes into account the work of Miyahara in including both the angular crossing and the hourglass effects. This also uses my derived collimated flux methodology for the angular, recoil corrected case (excludes energy spreads), which replaces the __systematically incorrect__ calculation by Curatolo et al. 
