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

[21/07/2020] C. Sun spectra code is now working, re-creates C. Sun Fig 3a well. The problem was incorrect characterisation of aperture and a selection of linac parameters not storage ring parameters it is based upon. Can produce plots with square and circular apertures, see the x0 and y0 definitions for further details . Emittance plot Fig. 4a of C. Sun not perfectly reproduced, think this is because of incorrect beta*. Energy spread plot Fig. 4b of C. Sun is reproduced well although there is noise in some of the plots which is due to a lack of points (reduce npts) and from Fourier effects when converting between a square distribution to a Gaussian. Further work to be done includes investigation of integration methods and order of integration, plotting an identical case for square vs circular aperture, comparison of linac and storage ring re-plot, investigation into beta*  

[24/08/2020] Hywel and I noticed an error in the formulation of Sun's spectra. There is an L^2 term in the prefactor. This is incorrect as it would mean the number of photons through the coillimator would increases the further the collimator is from the source i.e. the opposite of the inverse square law. This has been corrected with the L^2 now placed in the denominator of the prefactor. For the CBETA source there is then a 10^4 reduction in the spectral yield in comparison to the previous value. There is now rought agreement between this and ICCS.

[22/09/2020] Geoff and I noticed an error where Sun uses w0=2sigma_L which changed the Rayleigh range equation and subsequently caused a ~3.255 decrease in yield which brought the spectrum code closer into line with ICCS and ICCS3D. The shape differences are due to Sun only using emittance in 1 plane as derived for a storage ring i.e emit_x >> emit_y.

[29/09/2020] The Compton caluculations notebooks have been encompassed into one single corrected + consistent notebook. The Hartemann peak brightness has been included within this too. All analytical spectral calculations - excluding optimisation - can be produced from a single notebook.  

[06/10/2020] The Sun code is currently undergoing extension to 2D. The code has been constructed identically to the 1D Sun code. The polarisation component has been taken care of by the fact its contribution disappears in the forward direction - the region of interest or that we can take the case where polarisation is in the direction of the x axis. Integrals over theta_y, theta_x and k are not evaluating. The reason for this is unknown and some significant testing + checking has been used. 

[09/10/2020] The Compton Optimisation code takes the previously wrote Compton Master code and re-writes this in a more Mathematica friendly way. This code runs faster and allows greater, more precise optimisations. Both the single case and tuning curve codes return the results of Compton Master i.e. code is benchmarked.

[16/10/2020] The SUN2D code has been modified to include the k dependence within the integral, the Rayliegh range is excluded. Mostly this inc=volves using a k dependence within the incident photon energy. Code is still not functional.

[21/10/2020] Further completion of benchmarking against the 1D case (emit_y = 1/100 emit_y_CBETAICS). Spectral shapes match pretty much exactly. Reduction overall in ICCS3D yield in comparison to the SUN1D yield. Why? 

[17/11/2020] Hourglass effect calculation notebook added. This follows the work of M. Furman (Furman, Miguel A. "Hourglass effects for asymmetric colliders." (1991)) and Y. Miyahara (Y. Miyahara, Luminosity of angled collision of strongly focused beams with different Gaussian distributions, NIM A 588, 3 (2008)). Use of numerical integration and understanding of laser divergence was required to achieve this code. It is noted that Fig. 7 of Miyahara's paper isn't identical to that which I produced for PEPII, the beam-beam values in the table are reproduced though. Fig. 6 of Miyahara has been reproduced and is consistent with Furman. A comparison of DIANA and MAXII NEQ R_ACHG against crossing angle shows dependence on transverse effects. A comparison of DIANA and MAXIII NEQ shows that R_ACxR_HG vs bunch length is the same for DIANA + MAXIII NEQ, but when using the full Miyahara calculation these are different. This means the small change in transverse parameters or the bunch length causes R_ACxR_HG to be deficient in relation to Miyahara's R_ACHG calculation. 

[20/11/2020] SUN2D code is working. The problem is that the x0 limit was incorrectly entered. It used an incorrect fuction which defined the radius. The caveat is that the cross section term is not k dependent. Benchmarking of the number of points in the MonteCarlo integration and the effect of delta k, the bandwidth of the incident photons, are underway. 
