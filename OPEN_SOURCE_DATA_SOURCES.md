# Open Source Data Sources for Sun-Earth-Moon Alignment

A comprehensive compilation of publicly available datasets and resources for researching sun-earth-moon alignment, lunar phases, tidal effects, and gravitational dynamics.

---

## Primary Data Sources

| Source | URL | Data Type | Format | License | Use Case | Key Features |
|--------|-----|-----------|--------|---------|----------|--------------|
| **NASA JPL Horizons** | https://ssd.jpl.nasa.gov/horizons/ | Ephemerides | ASCII, HTML, XML | Public Domain | Sun-Earth-Moon positions, alignments | Precise coordinates, velocity vectors, custom date ranges |
| **US Naval Observatory (USNO)** | https://aa.usno.navy.mil/data/ | Astronomical Data | JSON, CSV, APIs | Public Domain | Lunar phases, rise/set, eclipses | Historical records, predictions, station-based |
| **NOAA Tide & Currents** | https://tidesandcurrents.noaa.gov/ | Tidal Measurements | CSV, JSON, API | Public Domain | Real-world tidal effects | 1000+ global stations, data since 1850s |
| **NASA SPICE Toolkit (NAIF)** | https://naif.jpl.nasa.gov/naif/index.html | Software/Kernels | C/Fortran source, Binary kernels | Public Domain | Ephemerides computation, dynamics | Programmatic access, trajectory planning |
| **ESA Science Archive** | https://www.cosmos.esa.int/web/esdc | Lunar/Planetary Data | GeoTIFF, NetCDF, ASCII | Open License | Gravitational fields, Moon data | High-resolution models, mass concentrations |
| **Harvard Dataverse** | https://dataverse.harvard.edu/ | Research Datasets | Multiple formats | Varies (mostly CC0/CC-BY) | Peer-reviewed lunar/solar/tidal data | Searchable, citation-enabled |
| **Time and Date AS** | https://www.timeanddate.com/astronomy/ | Astronomical Calendars | CSV, ICS, API | Open | Eclipse catalogs, phase calendars | Historical & future data, timezone support |
| **NASA LRO Data Portal** | https://lunar.gsfc.nasa.gov/data.html | Lunar Surface/Gravity | GeoTIFF, HDF5, NetCDF | Public Domain | Moon topography, gravitational anomalies | Mascon data, elevation models |

---

## Specialized Data Categories

### Lunar Phase Data

| Source | Data Available | Update Frequency | Access Method | Notes |
|--------|-----------------|------------------|----------------|-------|
| USNO Astronomical Applications | Phase dates, illumination % | Daily predictions | Web form, API | Accurate for 500+ years past/future |
| Time and Date | Full/New/Quarter phases | Real-time | Download, API | Includes penumbral eclipse phases |
| NASA Horizons | Moon phase angle | On-demand | Query system | High precision (sub-degree) |
| NOAA Lunar Data | Tidal stage correlation | Historical archives | Database query | Links phases to tidal ranges |

### Ephemeris Data (Positions & Alignments)

| Source | Celestial Bodies | Time Resolution | Accuracy | Format | Notes |
|--------|------------------|------------------|----------|--------|-------|
| NASA Horizons | Sun, Earth, Moon (all major planets) | Minutes to seconds | cm-level | ASCII tables | Customizable output, 10,000-year range |
| ESA Gaia Archive | Stars (reference frame) | Fixed catalog | μas-level | FITS, ASCII | Useful for orientation/alignment references |
| NASA SPICE Kernels | Solar System bodies | Sub-second | mm-level | Binary (.bsp, .tpc) | Needs dedicated software to read |
| USNO ICRF Catalog | Reference frame stars | Static catalog | sub-mas | FITS | For precise coordinate transformations |

### Tidal Data

| Source | Geographic Coverage | Time Span | Sampling Rate | Data Availability | Use |
|--------|---------------------|-----------|----------------|-------------------|-----|
| NOAA Tide Stations | 1000+ global stations | 1850s–present | 6-min to hourly | CSV, API | Historical tides, lunar phase correlation |
| BODC (UK) | Atlantic, Arctic, Indian | 1970s–present | Varies (hourly–daily) | NetCDF, ASCII | Long-term tidal trends |
| UHSLC (Sea Level Center) | 600+ tide gauges | 1960s–present | Monthly/annual | CSV | Sea level records, gravitational effects |
| GEBCO Bathymetry | Global ocean floor | Static model | 15 arc-second grid | GeoTIFF, NetCDF | Tidal modeling substrate |

### Gravitational Dynamics Data

| Source | Data Type | Coverage | Resolution | Format | Application |
|--------|-----------|----------|-----------|--------|-------------|
| NASA GRAIL Gravity Models | Moon gravity field | Full lunar body | 10–100 km | GeoTIFF, netCDF | Mass anomalies (mascons), interior structure |
| ESA GRACE Data | Earth gravity variations | Global | ~100 km | netCDF | Tidal response of Earth's crust |
| IERS Polar Motion | Earth rotation parameters | Global | Daily | ASCII, XML | Precession, nutation, obliquity changes |
| Jet Propulsion Lab DE440 | Planetary/lunar masses | Solar System | N/A (static) | ASCII, binary | Integration constants for orbital dynamics |

### Eclipse Data

| Source | Coverage | Format | Frequency | Predictions | Historical Data |
|--------|----------|--------|-----------|-------------|-----------------|
| NASA Eclipse Website | Global | CSV, KML, JSON | Updated annually | 500 years ahead | 2000 years back |
| USNO Eclipse Predictions | Global | ASCII, PDF | Real-time | 500 years | 2000 years |
| Timeanddate.com | By location | ICS, CSV | Daily updates | 300 years | 300 years |
| JPL Small-Body Node | Occultations/asteroids | ASCII | As computed | Available | Available |

---

## Software & Computational Tools

| Tool | Purpose | Language | License | Data Input | Output |
|------|---------|----------|---------|------------|--------|
| **SPICE Toolkit** | Ephemeris computation, trajectory planning | C, Fortran, Python | Public Domain | Binary kernels | Positions, orientations, events |
| **Astropy** | Python astronomy library | Python | BSD 3-Clause | URLs, FITS | Coordinates, timeseries, analysis |
| **PyEphem** | Fast ephemeris calculations | Python/C | LGPL | Orbital elements | Positions, phases, rise/set times |
| **SOFA** | IAU-standard astronomical calculations | Fortran, C | LGPL | Orbital elements | Precession, nutation, time scales |
| **Orekit** | Orbital mechanics, propagation | Java | Apache 2.0 | TLE, ephemerides | Trajectories, events, maneuvers |
| **Skyfield** | Precise astronomy calculations | Python | MIT | Ephemerides files | Positions, elongations, separations |

---

## Research & Reference Datasets

| Resource | Topic | Data Format | Size | License | URL |
|----------|-------|-------------|------|---------|-----|
| **JPL Small-Body Database** | Asteroid/comet orbits | ASCII/SQL | ~1 GB | Public Domain | https://ssd.jpl.nasa.gov/sbdb.cgi |
| **Minor Planet Center** | NEO orbits, discoveries | ASCII, CSV | ~500 MB | Public Domain | https://minorplanetcenter.net/iau/mpc.html |
| **SOHO Sunspot Catalog** | Solar activity | FITS, ASCII | ~10 GB | Public Domain | https://cdaw.gsfc.nasa.gov/CME_list/ |
| **IERS EOP Data** | Earth orientation parameters | ASCII, XML | ~50 MB | Public Domain | https://www.iers.org/IERS/EN/DataProducts/EarthOrientationData/eop.html |
| **GFZ GNSS Data** | GPS/GNSS station data | RINEX, ASCII | ~TB (selective) | Open | https://datacenter.iers.org/products/ |
| **Gaia DR3 Catalog** | Star positions (reference frame) | FITS, ASCII | ~1.8 TB | CC-BY 4.0 | https://gea.esac.esa.int/archive/ |

---

## Data Access Patterns

### Real-Time / Automated Access

| Data Source | API/Service | Authentication | Rate Limit | Recommended Use |
|------------|-------------|-----------------|-----------|-----------------|
| NOAA Tide API | RESTful JSON | None (key optional) | 1000 req/hour | Automated data collection |
| USNO API | Query-based | None | Reasonable limits | Phase/eclipse predictions |
| Skyfield Ephemerides | Direct download | None | N/A | Local computation |
| ESA CDSE Portal | OAuth 2.0 | Required (free) | Per API | Large-scale scientific queries |

### Bulk Download

| Source | Download Method | File Size | Update Frequency | Notes |
|--------|-----------------|-----------|------------------|-------|
| NASA SPICE Kernels | FTP/HTTPS | 1–50 GB | Monthly updates | Requires ~50 GB for complete set |
| NOAA Historical Data | FTP archives | Varies by station | Fixed (historical) | Organized by station and year |
| GEBCO Bathymetry | HTTPS download | ~430 MB (full) | Annual | Subset downloads available |
| Gaia DR3 | ESA archive mirror | 1.8 TB total | Fixed (DR3) | Regional downloads recommended |

---

## Recommended Data Integration Workflow

### Step 1: Core Dataset Download
- **NASA Horizons**: Query for Sun-Earth-Moon positions (100 year range)
- **USNO**: Extract lunar phase calendar
- **NOAA**: Download tide data from 5-10 representative global stations

### Step 2: Ephemeris Processing
- Parse Horizons ASCII output into structured format (JSON, CSV, SQLite)
- Compute alignment angles (Sun-Earth-Moon configuration)
- Calculate lunar phase correlation with tidal data

### Step 3: Validation & Analysis
- Cross-reference USNO phase predictions with Horizons computed phases
- Correlate tidal extrema with lunar cycles (should match 99.9%)
- Validate gravitational calculations against GRAIL/GRACE anomalies

### Step 4: Storage Organization
```
data/
  ├── ephemerides/
  │   ├── horizons_sun_earth_moon_1900_2100.csv
  │   └── DE440_planetary_masses.txt
  ├── lunar_phases/
  │   ├── usno_phases_1900_2100.csv
  │   └── timeanddate_eclipse_catalog.csv
  ├── tidal_measurements/
  │   ├── noaa_station_[ID]_1900_2024.csv
  │   └── tidal_harmonic_constituents.dat
  └── gravitational_models/
      ├── grail_mascon_moon_model.tiff
      └── grace_earth_gravity_field.nc
```

---

## License Summary

| Category | Typical License | Commercial Use | Redistribution |
|----------|-----------------|-----------------|-----------------|
| NASA Data (JPL, GSFC, SPICE) | Public Domain | ✓ Allowed | ✓ Allowed |
| NOAA Data | Public Domain | ✓ Allowed | ✓ Allowed |
| ESA Data (most) | CC-BY 4.0 or CC0 | ✓ Allowed | ✓ Allowed (with attribution) |
| IERS Data | Public Domain | ✓ Allowed | ✓ Allowed |
| Academic Datasets (Harvard Dataverse) | Varies (usually CC0/CC-BY) | Varies | ✓ Usually allowed |
| Gaia Data | CC-BY 4.0 | ✓ Allowed | ✓ Required attribution |

---

## Contact & Support Resources

| Organization | Support Channel | Response Time | Scope |
|--------------|-----------------|---------------|-------|
| **NASA SPICE** | https://naif.jpl.nasa.gov/naif/webform/ | 1-2 business days | Technical questions, toolkit help |
| **NOAA NOS** | https://www.nos.noaa.gov/contact/ | 1-3 business days | Tide data, station info |
| **USNO** | https://aa.usno.navy.mil/about/contact/ | 1-2 weeks | Astronomical data queries |
| **ESA Helpdesk** | https://www.cosmos.esa.int/web/esdc/data-access | 1-2 business days | Archive access, technical support |

---

## Version Control
- **Last Updated**: 2026-09-14
- **Maintained By**: sun-earth-moon-alignment repository
- **Contributions Welcome**: Please submit PRs for new data sources or corrections

