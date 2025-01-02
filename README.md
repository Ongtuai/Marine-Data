# Marine-Data

# Copernicus Marine Service Toolbox (CLI & Python)

## Features

The Copernicus Marine Toolbox offers capabilities through both **Command Line Interface (CLI)** and **Python API**:

## Documentation

For detailed and up-to-date information, please refer to the [Copernicus Marine Toolbox Documentation](https://toolbox-docs.marine.copernicus.eu/). It includes exhaustive guides, API specifications, and tutorials, automatically versioned.

For additional documentation and smooth transition for users of legacy services such as MOTU, OPeNDAP, or FTP, visit our [Help Center](https://help.marine.copernicus.eu/en/collections/9080063-copernicus-marine-toolbox).

## Installation

The Copernicus Marine Toolbox can be installed and utilized in various ways to suit different user preferences and system configurations. For detailed guidance, refer to the installation page of the [toolbox documentation](https://toolbox-docs.marine.copernicus.eu/).

### Mamba | Conda

```bash
mamba install conda-forge::copernicusmarine --yes
```

or conda:

```bash
conda install -c conda-forge copernicusmarine
```

### Pip

```bash
python -m pip install copernicusmarine
```

### Binaries (no-installation)

These binaries require no installation and run independently on the user system. Simply download ([from release page](https://github.com/mercator-ocean/copernicus-marine-toolbox/releases) or check the installation page of the [toolbox documentation](https://toolbox-docs.marine.copernicus.eu/)) and run the binary for instant access to the toolbox Command Line Interface functionalities.

### Docker

```bash
docker pull copernicusmarine/copernicusmarine:latest
```

### Dependencies

Note that the use of `xarray<2024.7.0` with `numpy>=2.0.0` leads to inconsistent results. See this issue: [xarray issue](https://github.com/pydata/xarray/issues/9179).

## Command Line Interface (CLI)

### The `--help` option

To discover commands and their available options, consider appending `--help` on any command line.

Example:

```bash
copernicusmarine --help
```

Returns:

```bash
Usage: copernicusmarine [OPTIONS] COMMAND [ARGS]...

Options:
  -V, --version  Show the version and exit.
  -h, --help     Show this message and exit.

Commands:
  describe  Print Copernicus Marine catalogue as JSON.
  get       Download originally produced data files.
  login     Create a configuration file with your Copernicus Marine credentials.
  subset    Download subsets of datasets as NetCDF files or Zarr stores.
```

## Python package (API)

The `copernicusmarine` exposes a Python interface to allow you to [call commands as functions](https://toolbox-docs.marine.copernicus.eu/).
