__Optimisation Code__

This includes all of the optimisation files created over several generations. Most is legacy code.

Compton Optimisation is a re-write of the Compton Master notebook for the fixed bandwidth optimisation technique.
It is re-wrote to be more conducive to Mathematica's style. It runs quicker and is capable of doing more precise optimisations.

Compton Master is still functional code. It contains an optimisation to show the possible adjustment for small changes in energy spread.

[UPDATE 22/03/2021] The RMS_FWHM_Compton_Optimisation notebook is the 'gold standard' round beam Compton optimisation at the moment. This includes full derivations for both the RMS case (Ranjan et al) and the FWHM case (modified Ranjan). The FWHM case has mostly been used to benchmark the F_0.1% bandwidth flux calculation, as first derived by Geoff Krafft. The RMS_FWHM_Compton_Optimisation also takes into account the work of Miyahara in including both the angular crossing and the hourglass effects. This also uses my derived collimated flux methodology for the angular, recoil corrected case (excludes energy spreads), which replaces the __systematically incorrect__ calculation by Curatolo et al. 
