# sensors-gasParams

Analysis repository for studying **sensor and gas-related parameters** used in detector simulations and performance studies.

The repository contains input parameters, analysis data, output files, and ROOT macros used to compare and visualize the effects of different sensor/gas configurations.

## Repository Structure

```text
sensors-gasParams/
├── analysisData/
│   └── Analysis input/data files
│
├── parameters/
│   └── Sensor and gas parameter configurations
│
├── plot_QE_wavelength_sensors/
│   └── Scripts/data related to sensor QE and wavelength studies
│
├── out/
│   └── Analysis output and generated results
│
├── FitGasCompare.C
├── FitGasCompare2.C
├── FitGasCompare3.C
└── README.md
```

## Analysis Macros

The main analysis is implemented using ROOT/C++ macros:

### `FitGasCompare.C`

Primary comparison macro for studying the dependence of the detector response on different gas/sensor configurations.

```bash
root -l -b -q FitGasCompare.C
```

### `FitGasCompare2.C`

Alternative/extended comparison of gas and sensor configurations.

```bash
root -l -b -q FitGasCompare2.C
```

### `FitGasCompare3.C`

Additional comparison and visualization of the corresponding analysis results.

```bash
root -l -b -q FitGasCompare3.C
```

The macros can be modified according to the required input configuration, parameter set, and output directory.

## Data and Parameters

The repository separates the **input parameters**, **analysis data**, and **generated results**:

* `parameters/` — configuration files and parameter sets used for the studies.
* `analysisData/` — data required by the analysis macros.
* `out/` — generated plots, ROOT output files, and other analysis products.
* `plot_QE_wavelength_sensors/` — material related to sensor quantum-efficiency and wavelength-dependent studies.

This organization is intended to keep input configurations separate from analysis products and generated output.

## Requirements

The analysis is based on **ROOT** and ROOT's C++ interpreter.

A working ROOT installation is required. The macros are intended to be executed from the repository directory.

For example:

```bash
root -l -b -q FitGasCompare.C
```

or interactively:

```bash
root -l
```

and then:

```cpp
.L FitGasCompare.C
```

## Typical Workflow

A typical analysis workflow is:

1. Select or prepare the required sensor/gas parameter configuration.
2. Place or verify the corresponding input data in `analysisData/`.
3. Run the appropriate ROOT analysis macro.
4. Inspect the generated plots and ROOT output.
5. Store the resulting analysis products in `out/`.
6. Keep different parameter/configuration studies organized separately for reproducibility.

## Reproducibility

When adding a new sensor or gas configuration, it is recommended to:

* keep the parameter files in `parameters/`;
* use a clear and descriptive configuration name;
* preserve the corresponding input data in `analysisData/`;
* document any important changes to the analysis macro;
* keep generated plots/results associated with the corresponding configuration.

This allows different sensor and gas configurations to be compared consistently.

## Notes

This repository is primarily intended for **research and detector-performance studies**. The analysis scripts and parameter files may evolve as the simulation and detector configuration develops.

For questions or issues related to the analysis, please use the repository's GitHub Issues.

## Author

**Ramandeep Kumar**

Researcher in Experimental High Energy Physics
INFN Trieste / ePIC Collaboration

## Repository

[sensors-gasParams on GitHub](https://github.com/kumardeepraman/sensors-gasParams?utm_source=chatgpt.com)
