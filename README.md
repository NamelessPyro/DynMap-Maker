`DynMap Maker` is a desktop utility for merging Dynmap tile exports into a single output image. It provides both a PyQt-based graphical interface and a command-line interface for scripted or manual workflows.

## Basic guide

1. Start the application with the packaged executable.
2. Browse to your Dynmap images folder.
3. Choose an output filename for the merged image.
4. Leave the recommended zoom level selected, or choose a different one.
5. Click `Merge Image` and wait for the output file to be written.

## Overview

The application scans a Dynmap export directory recursively, identifies valid tile files by name, groups them by zoom level, computes the output dimensions, and stitches the tiles into a single raster image. It is intended for local post-processing of exported Dynmap batches.

## Capabilities

- Recursive discovery of Dynmap tile images
- Support for zoom-prefixed tile naming such as `z_0_0.jpg` and `zz_16_8.jpg`
- Graphical drag-and-drop workflow for selecting the input directory
- Automatic recommendation of a suitable zoom level based on estimated memory usage
- Command-line mode for automation and repeatable builds
- Packaging support for Linux and Windows using PyInstaller

## Input format

The application accepts standard Dynmap-style tile names, including:

- `0_0.jpg`
- `-5_12.png`
- `z_0_0.jpg`
- `zz_16_8.jpg`

The input directory is scanned recursively, so nested tile-group folders are supported.
