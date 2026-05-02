# Identifying fatal-flaws in proposed hydropower dam sites

## Protected Areas Analysis

**Authors:** Aakriti Poudel, Leela Dixit, Megan Hessel, and Lucian Scher

### Purpose

This repository checks whether proposed dam sites around the world overlap with protected areas such as places like national parks, conservation areas, nature reserves where construction is not allowed. If a planned dam sits inside a protected area, it is flagged as a "fatal-flaw," meaning it is very unlikely to be approved and should be ruled out early.

We first test this approach in Nepal to make sure it works, then apply it to every proposed dam in the world.

This is part of a larger project, NetZeroHydro, that aims to identify which future hydropower dams would have the least environmental harm. The results here feed directly into our scoring model in the companion [`MCDA-model`](https://github.com/NetZeroHydro/MCDA-model) repository.

### File Structure

| File/Folder | Description |
| --- | --- |
| `protected-areas-aakriti.qmd` | Main analysis file. Checks whether dams (existing and proposed) overlap with protected areas, first for Nepal, then globally. |

**File Path**

```
fatal-flaws/
├── protected-areas-aakriti.qmd
├── population_counts.qmd
├── README.md
└── LICENSE
```
### Data

The raw data files are too large to store here. Download them from the links below and place them in the file paths referenced inside each `.qmd` file.

| Dataset | Description | Source |
| --- | --- | --- |
| [Global Dam Watch (GDW)](https://www.globaldamwatch.org/) | Locations and details for existing large dams around the world | Global Dam Watch |
| [Future Hydropower and Reservoir Data (FHReD)](https://www.globaldamwatch.org/directory) | Proposed future dams that could generate at least 1 MW of power | Global Dam Watch |
| [HydroRIVERS](https://www.hydrosheds.org/products/hydrorivers) | A global map of river networks with flow and drainage information | HydroSHEDS |
| [Free-Flowing Rivers (FFR)](https://www.hydrosheds.org/applications/free-flowing-rivers) | Identifies which rivers still flow freely and which are at risk | HydroSHEDS |
| [Protected Planet (WDPA)](https://www.protectedplanet.net/en) | A global map of protected areas on land and at sea | Protected Planet |

### Packages and Software

All analysis is written in R using Quarto (`.qmd`) notebooks. The following R packages are needed to run the code:

| Package | What it does |
| --- | --- |
| `sf` | Reads and works with map and geographic data |
| `tmap` | Makes interactive and printable maps |
| `leaflet` | Powers the interactive maps in the browser |
| `tidyverse` | Cleans and organizes data |
| `janitor` | Tidies up messy column names |
| `here` | Manages file paths so the code works on any computer |

See `session_info.txt` *(to be added)* for the full list of R package versions used.

### Technical Documentation

To read more about the project, visit our [Bren project page](https://bren.ucsb.edu/projects/hydropowers-low-hanging-fruits-leveraging-least-impact-dams-power-net-zero-future).

### License

**MIT License**

Copyright (c) 2026 NetZeroHydro

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
