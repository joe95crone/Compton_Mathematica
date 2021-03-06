__ICS Calculation + Investigation Mathematica Scripts__

AngularCrossingCollimatedFlux.nb calculates the collimated flux by the new derived method + compares this to existing sources but is legacy code.
It is kept as it is a comprehensive example and shows where the *RMS* to *FWHM* problem wasn't accounted for and how this caused disagreement in benchmarking.

ComptonCalcs is the most simple set of calculations to do everything analytical that we like to calculate (Scattered Photon Energy, Flux, Bandwidth, Brilliance, Source Size etc).
Code that might need updating slightly + reuploading.

FWHM_RMS_CollimatedFluxInvestigation uses the derived method of collimated flux calculation to calculate collimated flux in both the DIANA and CBETA cases for both *RMS* and *FWHM* optimised cases as well as a baseline case. This is then compared to a range of other calculation methods and codes such as the calculation by Curatolo et al, Geoff Krafft's F_0.1% bandwidth calculation (only applies to FWHM), an angular spread (small angle approximation) method and the results of semi-analytical codes: ICARUS and ICCS3D. Agreement to within ~10% (as expected) is found between all methods except the Curatolo et al method which is found to be deficient by a factor ~1.5 (potentially a square root of an *RMS* to *FWHM* conversion?). This verifies the new collimated flux method as well as tests the optimisation extension to *FWHM*. 

Hourglass Effect is an investigation into the Furman method of hourglass effect compensation, the Suzuki + Akagi methods of angular crossing compensation (which are equivalent)
and the Miyahara method of combined hourglass effect and angular crossing compensation. These are all benchmarked using several cases (both beam - beam and beam - photon beam),
which has shown that these methods are valid and reproducible. This work is then used elsewhere.

ICS Energy Loss and Beam Loss is a bit deficient in it's naming. This code just shows the required energy acceptance to retain all of the electron beam in the head-on case.
It is clearly unfinished code, which has been discontinued. The beam loss element is supplanted by the NEQ-SR ICS Emittance Degradation code. 

NEQ SR ICS Emittance Degradation code uses the methodology of R. Ruth and Z. Huang (Laser - Electron Storage Ring) as shown in Rod Loewen's thesis to show the emittance degradation
caused by repeated ICS interaction in a storage ring, in this case applied to a non-equilibrium ring. This method appears to be the worst case scenario and did not include effects
such as CSR and intrabeam scattering (IBS). The findings can be summarised as this is a small problem @ ~500MeV , negigible @ ~100MeV and potentially problematic @ ~GeV scale.
Hywel + Geoff Krafft did have some quarrel's with this methodology though.

Peak_Brightness_Hartemann is an investigation of the calculation of peak brilliance/brightness by Hartemann + Brown, which is a very comprehensive calculation. However, this is only
valid in the head-on case with no recoil (Thomson Scattering). It has been incorporated into ComptonCalcs.

YieldCalculations is a first attempt at calculating the flux yields of the ICS semi-analytical codes SUN_1D, ICCS, ICCS3D and ICARUS. This was used to understand how to import and operate
on the data produced, this code has since been used, improved + updated elsewhere. For example see the FWHM_RMS_CollimatedFluxInvestigation code.

__Change Log__
