# US Sectorfiles Repository

## Overview

<img src="https://s30121.pcdn.co/wp-content/uploads/2020/01/artcc-map.jpg" alt=""/>

## FAQ

Q: How often are sectorfiles updated?  
A: All sectorfiles are updated at least every AIRAC cycle, typically more frequently.

Q: Can anyone contribute?  
A: Yes! Our data comes from the wonderful OpenStreetMap project. Follow our tutorials to get started.

Q: What do I do if I find a problem?  
A: [File an issue](https://github.com/IVAO-US/SectorFiles/issues/new/choose)!

## Getting Started

All ground-based data comes from OpenStreetMap. You can edit the data [here](https://openstreetmap.org/). For a
more in-depth explnation, watch our [YouTube tutorial](https://youtu.be/-sbA0QU6yv8).  

## Structure

Each ARTCC has a single "sectorfile" which is stored in the repository. These sectorfiles are named after the ARTCC
with the extension `.isc` (e.g. `KZLA.isc` for ZLA). The majority of data is stored in the `US` folder (inside
`Include`) and is split into a number of folders, detailed below.

### GEOs

_GEOs_ are the taxiway and gate centerlines for each airport, as well as the coastline information which is shared
between all sectors. Each airport has a file ending in `.geo` (e.g. `KLAX.geo`) containing the centerlines, and a
shared file named `coast.geo` contains all the coastlines.

### Labels

_Labels_ are the little bits of text that are shown over the taxiways, gates, terminals, and aprons. These are split
into two files for each airport: a `.txi` file containing the taxiway labels, and a `.gts` file containing all other
labels.

### MVAs

_MVAs_ or _MRVAs_ are a set of altitudes which the FAA has determined are safe for IFR aircraft to be vectored at. In
many cases, they represent the lowest altitude you can instruct an aircraft to fly.

### Navaids

_Navaids_ are aids to navigation. In Aurora, we use the term to refer specifically to VORs and NDBs.

### Polygons

_Polygons_ are the shapes that make up the airport layouts. They are the taxiways, runways, aprons, terminals, and
anything else that appears "filled-in" in Aurora.

### Procedures

_Procedures_ are SIDs, STARs, and approaches. SIDs are stored in files ending `.sid` (e.g. `KLAX.sid`), while STARs and
approaches are stored in files ending `.str` (e.g. `KLAX.str`).

### ARTCCs

Each ARTCC has its own folder containing information specific to it.

#### Airports

The `airports.ap` file contains the ICAO code, elevation, location, and name of each airport displayed in the
sectorfile.

#### Airways

The `airways.high` and `airways.low` contain the high and low (respectively) airways which pass through the ARTCC.

#### ARTCC

The `artcc.artcc` file contains the ARTCC boundaries displayed in Aurora. `low.artcc` contains the boundaries of the
class B airports within the sector. Originally class C and D airports were included, but they were removed for
performance reasons.

#### ATC

The `atc.atc` file contains the list of positions which you can connect to in the sector as well as their frequencies.

#### Fixes

The `fixes.fix` file contains the fixes used by the procedures, airways, and airspaces within the sector. `vfr.fix`
contains the visual reporting points (points starting with `VP`, e.g. `VPLQM`) in the sector.

#### Runways

The `runways.rw` file contains the identifiers, elevations, courses, and endpoint positions of all runways in the
sector.

## More information

Learn more about reading sectorfiles: <https://wiki.ivao.aero/en/home/devops/manuals/SectorFile_Definition>
