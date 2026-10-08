# Micro-XRF App

A MATLAB App Designer application for automated calibration of micro-XRF measurements at the PolyX synchrotron beamline. The application combines calibration-standard measurements, spectrum visualization, and energy, detector-resolution, and elemental-sensitivity calibration in a graphical interface.

**[Read the User Manual and Technical Documentation (PDF)](docs/Micro-XRF-App-Manual.pdf)**

## Interface

![Micro-XRF App: Set Calibration interface](docs/images/Set_Calibration_Panel.svg)


## Main functionality

- Select calibration standards and characteristic emission lines according to the beam energy.
- Coordinate automated measurements using a dedicated holder with 30 standards arranged in a 5 × 6 grid.
- Display individual and overlaid spectra, with channel/energy axes and linear/logarithmic scales.
- Determine energy-calibration parameters and inspect fit quality and residuals.
- Determine FWHM calibration and the NOISE and FANO detector parameters.
- Calculate elemental sensitivity for selected spectral lines and two detectors.
- Load previously acquired measurement data for offline analysis.
- Export acquisition statistics and calibration results to Excel and text files.

## Operating modes

| Mode | Purpose | Required context |
| --- | --- | --- |
| Beamline measurements | Standard positioning, data acquisition, and calibration | The configured PolyX control environment and its hardware-control functions |
| Offline analysis | Load existing measurement folders, inspect spectra, and update calibration | Previously acquired datasets in the application's expected format |

Live measurement operation depends on the PolyX beamline software infrastructure. The application calls its existing MATLAB-accessible functions for hardware communication and configuration. These functions must be available on the MATLAB path in the beamline environment.

Offline analysis uses stored measurement folders, including header, snapshot, and sequence `.mat` files. See the manual for the required data structures and workflow.

## Documentation

The **[User Manual and Technical Documentation](docs/Micro-XRF-App-Manual.pdf)** is a 43-page English document covering the interface, measurement workflow, software architecture, calibration methods, data export, and experimental examples.

| Topic | Manual section | Pages |
| --- | --- | --- |
| Application purpose, standards, and experimental setup | 1 | 3–6 |
| Interface, data structures, beamline integration, and positioning | 2 | 7–13 |
| Spectrum visualization and offline analysis | 3 | 14–16 |
| Peak detection and energy calibration | 4 | 17–25 |
| FWHM calibration and NOISE/FANO parameters | 5 | 26–27 |
| Elemental sensitivity calibration | 6 | 28–30 |
| Export of calibration results | 7 | 31 |
| Experimental validation and example results | 8 and Appendix | 31–34, 36–43 |

For a first overview, read Section 1.5 (experimental setup and application workflow). For analysis of existing measurements, continue with Section 3.2 and Section 4.2.1.

## MATLAB environment

The application was developed using MATLAB App Designer. Live acquisition additionally requires the configured PolyX control environment; the offline workflow operates on recorded measurement data. Consult the application source and the manual for environment-specific setup.

## Academic background

Developed by **Marcin Drąg** as part of an engineering degree project in Technical Physics at AGH University of Krakow, 2026.

**Project title:** Automated calibration of synchrotron beamline for micro-XRF experiments.


## License

See [LICENSE](LICENSE) for the repository license.
