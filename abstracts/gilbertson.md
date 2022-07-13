# Jointly Modeling Telluric Features and Stellar Variability with [StellarSpectraObservationFitting.jl](https://github.com/christiangil/StellarSpectraObservationFitting.jl)
## Christian Gilbertson (Penn State)

Recently, several extreme precision radial velocity (EPRV) spectrographs have been providing high-resolution and high signal-to-noise spectra with the express purpose of exoplanet discovery and characterization. A significant barrier to this endeavor is the existence of time-variable features in the spectra from both telluric absorption and stellar variability. Traditional methods discard significant portions of data to minimize the effects of telluric contamination, but new data-driven methods may enable the use of a larger fraction of the available data. Here we present [StellarSpectraObservationFitting.jl](https://github.com/christiangil/StellarSpectraObservationFitting.jl) (SSOF), a Julia package for creating data-driven linear models (with fast, physically-motivated Gaussian Process priors) for the time-variable spectral features in both the observer and observed frames. SSOF utilizes Julia's strong native support for fast linear algebra with sparse arrays to enable several novel analysis techniques to be applied to EPRV spectra for the first time. We have demonstrated SSOF's state-of-the-art RV precision performance on EXPRES and NEID data and discuss how the resulting model can be used to aid in mitigating remaining sources of correlated noise in the radial velocity time series.