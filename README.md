# geopackage-owc-spec

This repository represents a *work in progres* extension to the [GeoPackage](http://geopackage.org) standard to facilitate the storage of map styling and context.

# Why?

Migrating projects between environments in the GeoSpatial domain is quite a hassle, since there are many aspects involved, many of them non standardised or disconnected. However the use case is quite strong, many require any project with all of its context to be transfered to an alternative platform, a web appication or mobile app.

The specification defined in this repository aims to provide a mechanism to store a project with all of it's context into a single GeoPackage (SQLite database) using existing standards when available.

# How

Aspects of projects are captured in the GeoPackage using commonly available standards:

- Storage of *Data* according to the GeoPackage standard 
- Storage of *Metadata* is available in the official [metadata extension](http://www.geopackage.org/spec/#extension_metadata) of GeoPackage
- Map styling is stored using the [Styled layer Descriptor](http://www.opengeospatial.org/standards/sld) extension, however other styling encodings can also be provided
- Map Context (how layers are ordered and grouped in the project) is captured using the [OWS Context](http://www.owscontext.org) standard.
- Related resources (thumbnails, icons, fonts, documentation) can be stored as blobs in a resources table (and be referenced from any of the other tables).


# About

The GPKG-OWC spec is currently in an experimental stage. 
It's currently pushed by the groups that have implemented the standard in their products, but we welcome any thoughts in the [issue section](issues). The specification currently mostly wants to proove that there is a need for a standard like this. However it can already be used from the software below.
- [QGPKG](https://github.com/pka/qgpkg) is an extension to QGIS which can load a project from an OWC-GeoPackage
- [GeoCat Bridge](https://geocat.net/bridge) is an extension to ArcMAP, which exports an ArcMAP project to an OWC-GeoPackage

# Specification & Examples

Read the specification [here](owc_geopackage_extension.md) and check some example packages [here](examples).


