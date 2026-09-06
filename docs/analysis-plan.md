Geography
Study-area boundary: to be established through the Phase 0 feasibility audit using a reproducible, documented geographic definition.
- Basically, we need to define the Kwinana geographical area boundary we are studying.
- We will establish this during data audit stage

Analysis period for datasets NPI, DWER and ABS.
- We need to dtermine the actual overlapping periods after inspecting the three datasets.

Importantly, we should distinguish:
- NPI reporting year
- DWER observation period
- ABS population reference year
We cannot imply that a 2021 population estimate, for example, represents every year from 2010 onward.

Distance bands:
Pre-register:
- 1 km
- 3 km
- 5 km
These are the initial bands specified by the project.
We'll later perform sensitivity analysis across them rather than choosing whichever distance produces the most interesting result.

Pollutants
Below are some I have noted down, yet to confirm. Will be confirmed during data audit.

Record the candidates:
- SO₂
- PM10
- NOx / NO₂
- potentially ammonia
- potentially named VOCs
But establish the selection criteria:
1. sufficient NPI facility-year coverage;
2. air-emission data;
3. stable names/units/interpretation;
4. ideally corresponding DWER monitoring;
5. clear industrial-context rationale.

- Maximum: Three pollutants for the MVP. (decide after data audit)

Missing data rules:
After performing data audit, record and plan out any appropriate rules for this.

We need to decide before looking at results how we'll treat:
- missing NPI years;
- facilities entering/leaving the reporting dataset;
- missing coordinates;
- DWER invalid observations;
- missing DWER periods;
- incomplete monitor-year coverage;
- population reference years that don't match an emissions year.
The project outline says missing years and invalid observations must be documented rather than silently discarded.

For now, I'd establish the principle: Missingness will be retained and reported where it affects interpretation. Missing records will not automatically be interpreted as zero emissions or zero population.

We'll refine the exact operational rules after seeing the source schemas.
- After MVP stage when we use AI, can we do some data science? bring in other sources?

Main outputs:
Document after data audit.
For each selected pollutant:
NPI
- annual reported emissions by facility;
- annual study-area total;
- reporting-facility count;
- facility share;
- multi-year trend.
DWER
- monitor availability;
- pollutant availability;
- completeness by monitor × pollutant × year;
- descriptive concentration summaries;
- missingness.
Population
- population within 1/3/5 km of reporting facilities;
- distance to nearest reporting facility;
- distance to nearest relevant monitor.

At the end, make a table outlining our gaps.

Evidence gap matrix
Ultimately:
Pollutant	NPI source coverage	Ambient-monitor coverage	Population proximity context	Main evidence limitation

This matrix is specifically identified in the build guide as a key output.