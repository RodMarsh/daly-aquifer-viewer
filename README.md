# Daly Basin Aquifer 3D Viewer

Interactive 3D web viewer of the Cambrian Limestone Aquifer system underlying the Katherine Water Allocation Plan area in the Northern Territory, Australia.

Live: <https://daly-aquifer-viewer.marsh.eco>

## What it shows

- **Four hydrostratigraphic units** of the Cambrian Limestone Aquifer system: Tindall Limestone, Jinduckin Formation, Oolloo Dolostone, Florina Formation.
- **Tindall as a real 3D top surface** when no basemap is selected — interpolated from 4,553 structure contours, depth-ramped from −600 m to +150 m.
- **Tindall as a flat slab** when a basemap (OpenStreetMap or OpenTopoMap) is selected, sitting in correct stratigraphic order beneath Jinduckin, Oolloo and Florina.
- **Two Katherine Water Allocation Plan boundaries**: 2024–2026 (existing) and 2026–2036 (proposed, 13 May 2026 package).

Layers can be toggled, vertical exaggeration adjusted (default 50×; required because the aquifer is ~300 km north–south but only ~500 m thick), and the view rotated, panned and zoomed.

## Tech stack

Static HTML + three.js (r171, loaded via importmap from unpkg). No build step. Single JSON payload (~1.3 MB) of pre-triangulated geometry.

## Data sources and attribution

- **Aquifer geometry** — Bureau of Meteorology, *Geofabric Groundwater Cartography v3.3* (November 2022). © Commonwealth of Australia (Bureau of Meteorology) 2022. Licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **Plan boundaries** — Northern Territory Government, NTLIS cadastral and water-allocation-plan datasets.
- **Basemap (OpenStreetMap)** — © OpenStreetMap contributors, [ODbL](https://www.openstreetmap.org/copyright).
- **Basemap (OpenTopoMap)** — map data © OpenStreetMap contributors, SRTM; style © OpenTopoMap ([CC-BY-SA](https://creativecommons.org/licenses/by-sa/3.0/)).
- **three.js** — MIT.

## Notes on accuracy

The Tindall surface is a real top-of-formation interpolation from BoM Geofabric structure contours. The Jinduckin, Oolloo and Florina formations are shown as **flat slabs at illustrative stratigraphic positions** — the BoM Geofabric does not publish depth contours for these three units, so their actual top depths are not represented. The slabs preserve the correct stratigraphic stacking order but not real elevations.

For the formal aquifer descriptions and water-allocation context, refer to the [Katherine Water Allocation Plan](https://nt.gov.au/environment/water/management-security/water-control-districts) published by the Northern Territory Department of Lands, Planning and Environment.

## Licence

Source code (HTML/JS): [MIT](./LICENSE). Data: as per the data-source attributions above (BoM Geofabric is CC-BY 4.0; basemap tiles per their respective providers).
