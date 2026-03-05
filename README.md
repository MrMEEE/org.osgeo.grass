# GRASS GIS Flatpak

This repository contains the Flatpak manifest for [GRASS GIS](https://grass.osgeo.org/), the Geographic Resources Analysis Support System.

## Application ID

`org.osgeo.grass`

This follows the standard Flatpak naming convention using reverse domain notation based on the OSGeo domain (osgeo.org).

## Runtime

The Flatpak uses **org.freedesktop.Platform** runtime version 25.08.

## About GRASS GIS

GRASS GIS is a free and open source Geographic Information System (GIS) used for:
- Geospatial data management and analysis
- Image processing
- Graphics and maps production
- Spatial modeling
- Visualization

GRASS GIS is used worldwide in academic and commercial settings, as well as by many governmental agencies and environmental consulting companies.

## Building the Flatpak

### Prerequisites

```bash
# Install flatpak and flatpak-builder
sudo dnf install flatpak flatpak-builder  # Fedora/RHEL
# or
sudo apt install flatpak flatpak-builder  # Ubuntu/Debian

# Add Flathub repository
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# Install required runtime and SDK
flatpak install flathub org.freedesktop.Platform//25.08 org.freedesktop.Sdk//25.08
```

### Build

```bash
flatpak-builder --user --install --force-clean build-dir org.osgeo.grass.yaml
```

### Run

```bash
flatpak run org.osgeo.grass
```

## Features

- Full GRASS GIS 8.4.2 functionality
- Integrated PROJ 9.5, GDAL 3.10, and GEOS 3.13
- Python scripting support with NumPy
- GUI and command-line interfaces
- Access to home directory and documents for project files

## Dependencies Included

- PROJ 9.5.1 - Cartographic projection library
- GDAL 3.10.1 - Geospatial Data Abstraction Library
- GEOS 3.13.0 - Geometry Engine
- NetCDF 4.9.2 - Network Common Data Form
- Python NumPy for scientific computing

## Version

Current version: **8.4.2**

Release date: December 20, 2024

## License

GRASS GIS is released under the GNU GPL v2+ License.

## Links

- [Official Website](https://grass.osgeo.org/)
- [GitHub Repository](https://github.com/OSGeo/grass)
- [Documentation](https://grass.osgeo.org/learn/)
- [Tutorials](https://grass.osgeo.org/learn/tutorials/)
- [Community](https://grass.osgeo.org/support/)

## Contributing

GRASS GIS is a community-driven project. Visit the [GRASS GIS website](https://grass.osgeo.org/contribute/) to learn how to contribute.
