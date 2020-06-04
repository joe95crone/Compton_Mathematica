# Compton_Mathematica
Mathematica notebooks from Compton Work.

All of **my** Mathematica scripts for Compton calculations and Optimizations.

Other Compton Mathematica scripts such as those by Val Kostroun are elsewhere.

__Change Log__

[unknown] The Hartemann Peak Brightness calculate evaluates however there is an unexplained discrepancy from the calculation in PRAB 8, 100702 (2005).

The FixedBandwidthOptExtended.nb works for the CBETA case and produces plots for CBETA that drop off at the expected minimum tunable bandwidth. 

The ComptonMaster.nb now works and is operable for the none head-on case and for energy spread optimisation.

[19/05/2020] Compton_Piss_About.nb added. This calculates none head-on scattered photon energies for CBETA.

Also includes simple spectra plots from (6) C. Sun PRSTAB 12, 062801 (2009).

[04/06/2020] Creation of the Spectrum Code file. This will include the C. Sun code to produce Compton spectra and any attempt at building ICCS in Mathematica.

The C. Sun dependent file is an attempt to make a Compton spectra using (16) of C. Sun PRSTAB 12, 062801 (2009). It is dependent as the scatteded energy is not held at constant theta_f. This results in a poor integral limit.

The C. Sun trial file is an attempt at a Compton spectra using (16) of C. Sun but with theta_f held constant and iterated over. This produces curves for the region inside the collimation angle but when this is increased it seems to fail. Other problems such as highly oscillatory integrands are present. This should be trialed with C. Sun's parameters but these are incomplete with bunch charge, laser pulse energy, beta at the IP, spot size of the laser (or their contemporaries) all undefined.  


