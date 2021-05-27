__Optimisation Code__

This includes all of the optimisation files created over several generations. Most is legacy code.

Compton Optimisation is a re-write of the Compton Master notebook for the fixed bandwidth optimisation technique.
It is re-wrote to be more conducive to Mathematica's style. It runs quicker and is capable of doing more precise optimisations.

Compton Master is still functional code. It contains an optimisation to show the possible adjustment for small changes in energy spread.

[UPDATE 2020] The Compton_Optimisation round beam code uses the *RMS* Ranjan et al bandwidth and flux by Curatolo et al. The Curatolo et al flux calculation has since been found to be deficient as this is based upon an outdated bandwidth, that was disproved by Ranjan et al. The code has been parallelized and can operate, using multiple Kernels, on the apsv2 server. Finally, it has been modified to also include the hourglass effect and angular crossing effect via Miyahara's luminosity reduction factors.  

[UPDATE 22/03/2021] Derived_ColFlux_Compton_Optimisation_Hourglass.nb uses the new derived collimated flux method and the *RMS* Ranjan bandwidth for the round beam oiptimisation. 

[UPDATE 22/03/2021] The RMS_FWHM_Compton_Optimisation notebook is the 'gold standard' round beam Compton optimisation at the moment. This includes full derivations for both the *RMS* case (Ranjan et al bandwidth) and the *FWHM* case (modified Ranjan BW). The *FWHM* case has mostly been used to benchmark the F_0.1% bandwidth flux calculation, as first derived by Geoff Krafft. This code still uses parallel processing on apsv2 in order to speed up the optimisation. The RMS_FWHM_Compton_Optimisation also takes into account the work of Miyahara in including both the angular crossing and the hourglass effects. This also uses my derived collimated flux methodology for the angular, recoil corrected case (excludes energy spreads), which replaces the __systematically incorrect__ calculation by Curatolo et al. 

[UPDATE 27/05/2021] A GA non-round beam (varying emittance, varying beta* functions) optimisation has been created with Balsa Terzic using the SPEA2 algorithm and PISA platform. See other repository for this code. The GA_Compton_Optimisation_Results.nb is a script to analyse the results of these simulations. There is also an accompanying simplex/nelder-mead script Simplex_2D_Optimisation.nb, which produces 2D Fcol-BW IP variable optimisations using many local optimisations. As a results, sometimes this method does not produce a valid result. It only gives a single value too, insead of the full pareto space like the GA does. This is capable of producing single BW point optimisations and tuning curves. These fit well inside the pareto space of the GA. The ICS_2D_OPT_MATHEMATICA_COMP.nb script compares the simulated annealing and differential evolution approaches with the simplex method.   
