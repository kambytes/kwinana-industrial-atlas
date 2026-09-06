# Data Source Register

## Purpose

## 1. National Pollutant Inventory

### Dataset

**National Pollutant Inventory (NPI)** - national facility-level information on reported emissions of NPI substances to air, land and water, together with waste-transfer information. The project will use the NPI facility, emissions, substances and ANZSIC resources, focusing on reported annual **air emissions** from facilities in and around the Kwinana study area.

The current NPI release available at the time of this register review is **2024–25**. NPI data are published annually and historical reporting years are available through the NPI data resources.

### Publisher

Australian Government **Department of Climate Change, Energy, the Environment and Water (DCCEEW)**.

### Official URLs

* NPI data and documentation: https://www.dcceew.gov.au/environment/protection/npi/data
* NPI dataset and downloadable resources: https://data.gov.au/data/dataset/npi
* NPI data dictionary: https://www.data.gov.au/data/dataset/npi/resource/e73a9a72-0eca-4937-a5e6-7fe9c9341e3d
* NPI reporting information: https://www.dcceew.gov.au/environment/protection/npi/reporting
* NPI substances: https://www.dcceew.gov.au/environment/protection/npi/substances

### Intended use

The NPI will provide the project's primary facility and annual source-emissions layer. It will be used to:

* identify reporting facilities and their locations;
* identify facility ANZSIC classifications;
* obtain annual reported emissions by substance;
* restrict analysis to emissions to air;
* assess facility and pollutant reporting coverage over time; and
* calculate pollutant-specific source, concentration-of-reporting, trend and population-proximity summaries.

NPI emissions will be described as **reported annual air emissions**. They will not be treated as ambient concentrations, human exposure estimates, or evidence of facility-level causation.

### Access

The NPI provides downloadable facility and emissions resources through Data.gov.au, including CSV/XLSX resources and facility GeoJSON. The NPI also provides an online database for searching facility and emissions information.

The project will use the official downloadable resources where practicable so that ingestion can be automated or reproduced from a documented source snapshot.

NPI reporting covers a **1 July–30 June reporting period** for facilities reporting on a financial-year basis. Most facility reports are submitted by 30 September and facility data are published by the NPI on or before 31 March for the preceding financial year. DCCEEW may subsequently publish corrections or interim updates.

### Update frequency

**Annual**, with the main NPI release published on or before **31 March** for the preceding financial year. Smaller corrections or updates may occur between annual releases.

### Licence

**Creative Commons Attribution 4.0 International (CC BY 4.0)**, as specified in the current Data.gov.au NPI dataset metadata and resources.

Use of the data must comply with the CC BY 4.0 attribution requirements and any exclusions or notices applying to particular material, such as the Commonwealth Coat of Arms or third-party material where applicable.

### Raw-data handling

Raw NPI downloads will be stored locally under:

`data/raw/npi/`

The raw files will remain **Gitignored** and will not be committed to the repository.

For each retrieved source file, the project will record the source URL, retrieval date, file name, file size and SHA-256 checksum in the retrieval metadata/manifest.

### Publication permissions

The NPI dataset is licensed under CC BY 4.0, so reuse and adaptation are permitted subject to the licence and required attribution.

The project will nevertheless distinguish between:

* original NPI source files;
* project-derived analytical tables;
* charts, maps and summaries derived from NPI data.

Raw source files will not be distributed through the project repository unless there is a specific reason to do so and the applicable licence/attribution requirements have been reviewed. The published project will primarily provide derived, reproducible results and links back to the official NPI source.

### Attribution

Use an attribution based on the official source and licence:

> Contains data sourced from the National Pollutant Inventory, © Commonwealth of Australia, licensed under CC BY 4.0.

The published report and README will also link to the official NPI/Data.gov.au source.

### Retrieval metadata

**Access date:** 5 September 2026

**Current release reviewed:** NPI 2024–25

**Raw files:** Not yet downloaded — to be recorded during Phase 0.3.

**SHA-256 checksums:** Not yet available — to be calculated when the Phase 0.3 source snapshots are downloaded.

**Selected NPI resources for the MVP:**

* Facilities
* Emissions
* Substances
* Data Dictionary
* ANZSIC 2006

The project will retain the source identifiers and original substance labels/units during ingestion. Air point emissions, air fugitive emissions and total air emissions will be handled according to the NPI data definitions rather than inferred or recombined by the project.


## 2. DWER Air Quality
## 2. DWER Air Quality

### Dataset

**Western Australian air-quality monitoring data** published by the Department of Water and Environmental Regulation (DWER).

The dataset provides ambient-air-quality observations and monitoring-site information from DWER's air-quality monitoring network. The project will use the data to assess:

* which relevant pollutants are measured at monitors near the Kwinana study area;
* monitor locations and operating periods;
* available observation periods and averaging periods;
* data completeness and missingness; and
* descriptive ambient-air-quality context for pollutants selected for the MVP.

DWER presents current and historical air-quality information as ambient concentrations and Air Quality Index (AQI) values. The published historical plots follow the averaging requirements of the National Environment Protection (Ambient Air Quality) Measure (AAQ NEPM).

### Publisher

**Western Australian Department of Water and Environmental Regulation (DWER).**

### Official URLs

* DWER air-quality data: https://der.wa.gov.au/your-environment/air/air-quality-data
* WA Government air-quality information: https://www.wa.gov.au/service/environment/environment-information-services/air-quality
* DWER air-quality publications: https://der.wa.gov.au/your-environment/air/air-quality-publications
* DWER Active Acceptance Licence Agreement: https://catalogue.data.wa.gov.au/dataset/dwer-active-acceptance-licence-agreement

### Intended use

DWER data will provide the project's ambient-monitoring layer. It will be used to:

* identify relevant monitoring sites and their geographic locations;
* identify pollutants measured at each site;
* determine available observation periods and averaging periods;
* calculate monitor × pollutant × year data completeness;
* describe missing and invalid observations;
* calculate monitor proximity to facilities and population areas; and
* provide descriptive ambient-observation context for selected pollutants.

Ambient observations will remain analytically separate from NPI reported annual emissions. The project will not use DWER observations to attribute measured concentrations to individual facilities or to estimate individual human exposure or health risk.

### Access

DWER provides public access to current and historical air-quality information through its official air-quality data service. The service states that monitoring data are updated hourly and that historical plots are available for selected sites and dates.

The published historical data use pollutant-specific averaging periods consistent with the AAQ NEPM, including:

* CO — 8-hour rolling average;
* NO₂ — 1-hour average;
* SO₂ — 1-hour average;
* O₃ — 1-hour average;
* PM10 — 24-hour rolling average; and
* PM2.5 — 24-hour rolling average.

For the MVP, the exact machine-readable retrieval method and historical coverage will be established during the Phase 0 feasibility audit. The project will not assume that the public website itself constitutes a stable API.

### Update frequency

**Current monitoring data:** updated hourly through DWER's public air-quality service.

**Historical data:** published through the DWER historical-data service; the availability and retrieval mechanism for the required historical period will be documented during the Phase 0 audit.

Monitoring-site availability is not assumed to be constant over the full study period. Changes in sites, pollutants and monitoring campaigns will be recorded where identifiable.

### Licence

**Reuse terms require verification for the specific DWER data resource used.**

The DWER/Data WA catalogue uses DWER-specific **Active Acceptance Licence** arrangements for relevant datasets. The catalogue's DWER Active Acceptance Licence Agreement states that accessing or using data/resources is subject to DWER's licence conditions.

The public availability of the air-quality observations therefore must not be interpreted as unrestricted permission to redistribute the raw observations. The project will review the applicable terms for the exact data retrieval/resource before publishing raw observations or redistributing source extracts.

### Raw-data handling

Raw DWER retrievals will be stored locally under:

`data/raw/dwer/`

Raw files will remain **Gitignored** and will not be committed to the repository.

For each retrieval, the project will record:

* source URL or endpoint;
* retrieval date;
* retrieval method;
* source file name or request parameters;
* file size where applicable;
* SHA-256 checksum where applicable; and
* relevant source/version metadata.

### Publication permissions

**Raw DWER observations: publication status — not yet confirmed.**

Until the applicable DWER licence/reuse conditions have been reviewed for the exact resource used, raw observations will not be redistributed through the GitHub repository or published on the project website.

The MVP will initially favour publication of derived summaries, completeness statistics, charts and other outputs where permitted. Any publication of derived DWER data will remain subject to the applicable source terms and attribution requirements.

If the historical observations cannot be retrieved in a sufficiently repeatable and permitted manner, the project will document that limitation and may restrict the MVP to publicly documented monitor locations, pollutant availability and other reproducible DWER information.

### Attribution

Attribution will follow the applicable DWER/Data WA licence conditions for the exact resource used.

For the MVP, the project will identify the source as:

> Air-quality observations are sourced from the Western Australian Department of Water and Environmental Regulation.

The final attribution wording will be updated if the applicable DWER licence specifies additional wording or acknowledgement requirements.

### Retrieval metadata

**Access date:** 5 September 2026

**Current access method:** DWER public air-quality data service.

**Historical machine-readable retrieval method:** To be determined during Phase 0.3–0.4.

**Raw files:** Not yet downloaded — to be recorded during the Phase 0 source-sample audit.

**SHA-256 checksums:** Not yet available — to be calculated for any downloaded source files.

**Monitoring context:** DWER's 2024–25 annual report states that a new air-quality monitoring campaign in the Kwinana Industrial Area began in 2025. Monitoring-site availability and pollutant coverage will therefore be treated as time-dependent rather than assumed to be constant across the full study period.


## 3. ABS Population

### Dataset

**Australian Bureau of Statistics (ABS) population data**, with two candidate products being assessed for the MVP:

1. **Australian Population Grid 2025** — 1 km² grid-cell population estimates provided in GeoTIFF format as part of the ABS Regional Population 2024–25 release.
2. **2021 Census Mesh Block Counts** — 2021 Census counts of usual resident population and dwellings at Mesh Block level, which can be combined with the corresponding ABS digital boundary files.

The Australian Population Grid is the preferred initial candidate because its 1 km² grid structure is directly suited to population-within-distance-band analysis. Mesh Blocks will also be assessed because they provide substantially finer spatial units and broadly identify land use, including residential and industrial areas.

The final MVP population product will be selected during the Phase 0 feasibility audit based on spatial resolution, suitability for buffer aggregation, population reference period, processing requirements and applicable licence conditions.

### Publisher

**Australian Bureau of Statistics (ABS), Commonwealth of Australia.**

### Official URLs

* Regional Population 2024–25, including Australian Population Grid 2025: https://www.abs.gov.au/statistics/people/population/regional-population/2024-25
* Regional Population 2024–25 methodology: https://www.abs.gov.au/methodologies/regional-population-methodology/2024-25
* 2021 Census Mesh Block Counts: https://www.abs.gov.au/census/guide-census-data/mesh-block-counts/2021
* ABS Mesh Blocks — ASGS Edition 3: https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs/edition-3-july-2021-june-2026/main-structure-and-greater-capital-city-statistical-areas/mesh-blocks
* ABS Digital Boundary Files: https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs/edition-3-july-2021-june-2026/access-and-downloads/digital-boundary-files
* ABS Conditions of Sale and licensing: https://www.abs.gov.au/about/legislation-and-policy/purchasing-data/abs-conditions-sale

### Intended use

ABS population data will provide the project's community-context layer. It will be used to:

* identify population located within 1 km, 3 km and 5 km distance bands of facilities reporting selected pollutants;
* calculate population-area distance to the nearest reporting facility;
* support spatial maps of facilities, monitors and population;
* provide population context for pollutant-specific source patterns; and
* identify limitations in the spatial and temporal representation of population.

Population proximity results will be described as **population context or population within a defined geographic distance**, not as exposure estimates or health-risk estimates.

### Access

The ABS Regional Population 2024–25 release provides an **Australian Population Grid 2025** as a downloadable GeoTIFF. The grid represents population density using 1 km² grid cells.

The ABS also provides downloadable **2021 Census Mesh Block Counts**, containing total usual resident population and dwelling counts for Mesh Blocks. Corresponding Mesh Block spatial boundaries are available through the ABS digital boundary files.

For the MVP, one of these products will be selected after testing its spatial format, resolution and suitability for aggregation around facility buffers.

### Update frequency

The **Australian Population Grid** is associated with the annual Regional Population release. The current release has a **2024–25 financial-year reference period** and provides the 2025 population grid.

The **Census Mesh Block Counts** are Census-based and therefore are not annual population estimates. The currently available Census Mesh Block Counts use the **2021 Census reference period**.

The project will record the exact population reference year separately from the analysis year. Population data will not be presented as if the 2021 Census counts or 2025 grid necessarily represent population for every year in the NPI/DWER study period.

### Licence

ABS material is generally provided under **Creative Commons Attribution 4.0 International (CC BY 4.0)** where the relevant product is explicitly licensed under CC BY 4.0. ABS states that licensing details are displayed within individual products and that where no licensing indication is provided, full copyright terms apply.

The exact licence statement for the selected population product and any associated boundary files will therefore be verified before publication.

### Raw-data handling

Raw ABS downloads will be stored locally under:

`data/raw/abs/`

Raw source files will remain **Gitignored** and will not be committed to the repository.

For each downloaded source file, the project will record:

* source URL;
* retrieval date;
* exact product/release;
* reference year;
* file name;
* file size where applicable; and
* SHA-256 checksum.

### Publication permissions

If the selected ABS product is licensed under CC BY 4.0, the project may reuse, transform and publish derived material subject to the licence conditions and required attribution.

The project will nevertheless keep original ABS source files outside Git and will publish only the source material or derived outputs necessary for the analysis.

Any derived population grids, spatial aggregates, charts or proximity summaries published by the project will be clearly identified as project-derived work and will not be attributed to the ABS as an ABS analysis or conclusion.

If a particular ABS product or boundary file carries different licensing conditions, those product-specific conditions will take precedence and will be recorded before publication.

### Attribution

For transformed or derived material, use the ABS-recommended attribution form:

> Based on Australian Bureau of Statistics data.

Where appropriate, the published report will identify the specific ABS product and reference period, for example:

> Based on Australian Bureau of Statistics data, Australian Population Grid 2025.

The final attribution will be checked against the licence statement accompanying the exact resources used.

### Retrieval metadata

**Access date:** 5 September 2026

**Candidate population product 1:** Australian Population Grid 2025, from Regional Population 2024–25.

**Candidate population product 2:** 2021 Census Mesh Block Counts with corresponding ASGS Mesh Block boundaries.

**Selected product:** To be determined during Phase 0.3–0.4 feasibility audit.

**Raw files:** Not yet downloaded — to be recorded during the Phase 0 source-sample audit.

**SHA-256 checksums:** Not yet available — to be calculated for downloaded source files.

**Spatial reference:** To be recorded from the exact downloaded product and standardised during the spatial-processing phase. Project distance calculations will use GDA2020 / MGA Zone 50 or another documented appropriate projected CRS.

**Population reference period:** Must be retained explicitly in the analysis tables and must not be confused with the NPI reporting year or DWER observation year.

## Source-selection notes