# Dosimetry Data for Nevada Nuclear Bomb Tests

This directory contains a cleaned distribution copy of dosimetry data for atmospheric Nevada Test Site (NTS) nuclear tests. The data are organized into two libraries:

- Ground deposition of I-131 and Cs-137
- Thyroid dose estimates for the U.S. population

The distribution keeps one analysis-ready copy of each duplicated dataset. Thyroid dose files are provided in CSV format, and ground-deposition summary data are provided as Excel workbooks. Duplicate original `.RES` text files were omitted from this cleaned copy.

## Download

### [DOWNLOAD LINK](https://drive.google.com/drive/folders/1B2cI9eewJzRn5DJMaOGJ1RloNv0blxSF?usp=share_link)

Access to the download link is restricted to users with:
- an approved **Software Transfer Agreement (STA)** for non-commercial research use, or
- a completed **commercial licensing agreement**.

Unlicensed access or redistribution is not permitted.

## Directory Structure

```text
NTS/
├── README.md
├── ground_deposition/
│   ├── NTS-DEP-PER-TEST-DAY-CS137-20221202.xlsx
│   ├── NTS-DEP-PER-TEST-DAY-I131-20221202.xlsx
│   ├── NTS-DEP-PER-TEST-I131-20230911.xlsx
│   └── NTS-TOTALDEP-I131-CS137-20221202.xlsx
└── thyroid_dose/
    ├── age_dependent/
    │   └── SSNNDAA.csv
    └── per_capita/
        └── SSNNPCD.csv
```

## Inventory

| Dataset | Directory | Format | Files |
| --- | --- | --- | ---: |
| Ground deposition | `ground_deposition/` | `.xlsx` | 4 |
| Age-dependent thyroid dose | `thyroid_dose/age_dependent/` | `.csv` | 1,079 |
| Per-capita thyroid dose | `thyroid_dose/per_capita/` | `.csv` | 83 |

## Ground Deposition

The ground-deposition dataset contains nationwide county-specific deposition estimates for I-131 and Cs-137.

| File | Description |
| --- | --- |
| `NTS-DEP-PER-TEST-DAY-CS137-20221202.xlsx` | Cs-137 deposition estimates by county, test, and day |
| `NTS-DEP-PER-TEST-DAY-I131-20221202.xlsx` | I-131 deposition estimates by county, test, and day |
| `NTS-DEP-PER-TEST-I131-20230911.xlsx` | I-131 deposition estimates by county and test, with dates combined |
| `NTS-TOTALDEP-I131-CS137-20221202.xlsx` | Total I-131 and Cs-137 deposition estimates by county |

The per-test-day workbooks include FIPS, geographic coordinates, 1960 population, and area for 3,094 counties and split-counties of the continental United States.

The Cs-137 data correspond to the data used in Simon et al. (2004), summed over daily deposition densities for each test. The I-131 data are more recent and include improvements for counties within roughly 300 km of the NTS to account for fractionation of radioactive debris.

## Thyroid Dose

The thyroid-dose dataset contains county-specific thyroid dose estimates in CSV format.

### Age-Dependent Dose

Directory: `thyroid_dose/age_dependent/`

The age-dependent dose dataset contains 1,079 CSV files, corresponding to 83 tests and 13 age groups.

Filename pattern: `SSNNDAA.csv`

- `SS`: test series
- `NN`: test number
- `D`: dose
- `AA`: age group

Example: `BJ02D12.csv` is the thyroid dose for age group 12, 15-19 years, from Buster-Jungle test series number 2.

Columns:

- `STATE`
- `COUNTY`
- `AM-GM`, `AM-GSD`: average-diet milk drinker
- `HM-GM`, `HM-GSD`: high milk consumption
- `CM-GM`, `CM-GSD`: milk from backyard cow
- `NM-GM`, `NM-GSD`: no milk consumption
- `MM-GM`, `MM-GSD`: mother's milk

### Per-Capita Dose

Directory: `thyroid_dose/per_capita/`

The per-capita dose dataset contains 83 CSV files, one for each test.

Filename pattern: `SSNNPCD.csv`

- `SS`: test series
- `NN`: test number
- `PCD`: per-capita dose

Example: `BJ02PCD.csv` is the per-capita thyroid dose from Buster-Jungle test series number 2.

Columns:

- `STATE`
- `COUNTY`
- `AD-MC-GM`, `AD-AMC-GSD`: average doses from milk consumption
- `AD-AE-GM`, `AD-AE-GSD`: average doses from all exposure routes
- `CD-MC-GM`: collective doses from milk consumption
- `CD-AE-GM`: collective doses from all exposure routes

## Test Series

| ID | Test Series | Test Name | Test Date |
| --- | --- | --- | --- |
| BJ01 | Buster-Jungle | Baker | 10/28/1951 |
| BJ02 | Buster-Jungle | Charlie | 10/30/1951 |
| BJ03 | Buster-Jungle | Dog | 11/1/1951 |
| BJ04 | Buster-Jungle | Easy | 11/5/1951 |
| BJ05 | Buster-Jungle | Sugar | 11/19/1951 |
| BJ06 | Buster-Jungle | Uncle | 11/29/1951 |
| HT01 | Hardtack-Phase II | Eddy | 9/19/1958 |
| HT02 | Hardtack-Phase II | Hidalgo | 10/5/1958 |
| HT03 | Hardtack-Phase II | Quay | 10/10/1958 |
| HT04 | Hardtack-Phase II | Lea | 10/13/1958 |
| HT05 | Hardtack-Phase II | Vesta | 10/17/1958 |
| HT06 | Hardtack-Phase II | Rio Arriba | 10/18/1958 |
| HT07 | Hardtack-Phase II | Socorro | 10/22/1958 |
| HT08 | Hardtack-Phase II | Wrangell | 10/22/1958 |
| HT09 | Hardtack-Phase II | Sanford | 10/26/1958 |
| PB01 | Plumbbob | Boltzmann | 5/28/1957 |
| PB02 | Plumbbob | Wilson | 6/18/1957 |
| PB03 | Plumbbob | Priscilla | 6/24/1957 |
| PB04 | Plumbbob | Hood | 7/5/1957 |
| PB05 | Plumbbob | Diablo | 7/15/1957 |
| PB06 | Plumbbob | Kepler | 7/24/1957 |
| PB07 | Plumbbob | Stokes | 8/7/1957 |
| PB08 | Plumbbob | Shasta | 8/8/1957 |
| PB09 | Plumbbob | Doppler | 8/23/1957 |
| PB10 | Plumbbob | Franklin Prime | 8/30/1957 |
| PB11 | Plumbbob | Smoky | 8/31/1957 |
| PB12 | Plumbbob | Galileo | 9/2/1957 |
| PB13 | Plumbbob | Laplace | 9/8/1957 |
| PB14 | Plumbbob | Fizeau | 9/14/1957 |
| PB15 | Plumbbob | Newton | 9/16/1957 |
| PB16 | Plumbbob | Whitney | 9/23/1957 |
| PB17 | Plumbbob | Charleston | 9/28/1957 |
| PB18 | Plumbbob | Morgan | 10/7/1957 |
| RA01 | Ranger | Baker | 1/28/1951 |
| RA02 | Ranger | Baker-2 | 2/2/1951 |
| RA03 | Ranger | Fox | 2/6/1951 |
| TP01 | Teapot | Wasp | 2/18/1955 |
| TP02 | Teapot | Moth | 2/22/1955 |
| TP03 | Teapot | Tesla | 3/1/1955 |
| TP04 | Teapot | Turk | 3/7/1955 |
| TP05 | Teapot | Hornet | 3/12/1955 |
| TP06 | Teapot | Bee+Ess | 3/22/1955 |
| TP07 | Teapot | Wasp Prime | 3/29/1955 |
| TP08 | Teapot | Post | 4/9/1955 |
| TP09 | Teapot | Met | 9/15/1955 |
| TP10 | Teapot | Apple2 | 5/5/1955 |
| TP11 | Teapot | Zucchini | 5/15/1955 |
| TS01 | Tumbler-Snapper | Able | 4/1/1952 |
| TS02 | Tumbler-Snapper | Baker | 4/15/1952 |
| TS03 | Tumbler-Snapper | Charlie | 4/22/1952 |
| TS04 | Tumbler-Snapper | Dog | 5/1/1952 |
| TS05 | Tumbler-Snapper | Easy | 5/7/1952 |
| TS06 | Tumbler-Snapper | Fox | 5/25/1952 |
| TS07 | Tumbler-Snapper | George | 6/1/1952 |
| TS08 | Tumbler-Snapper | How | 6/5/1952 |
| UE01 | Underground Era | Antler | 9/15/1961 |
| UE02 | Underground Era | Danny Boy | 3/5/1962 |
| UE03 | Underground Era | Platte | 4/14/1962 |
| UE04 | Underground Era | Eel | 5/19/1962 |
| UE05 | Underground Era | Des Moines | 6/13/1962 |
| UE06 | Underground Era | Sedan | 7/6/1962 |
| UE07 | Underground Era | Johnie Boy | 7/11/1962 |
| UE08 | Underground Era | Small Boy | 7/14/1962 |
| UE09 | Underground Era | Bandicoot | 10/9/1962 |
| UE10 | Underground Era | Pike | 3/13/1964 |
| UE11 | Underground Era | Sulky | 12/18/1964 |
| UE12 | Underground Era | Palanquin | 4/14/1965 |
| UE13 | Underground Era | Pin Stripe | 4/25/1966 |
| UE14 | Underground Era | Cabriolet | 1/26/1968 |
| UE15 | Underground Era | Buggy | 3/12/1968 |
| UE16 | Underground Era | Schooner | 12/8/1968 |
| UE17 | Underground Era | Baneberry | 12/18/1970 |
| UK01 | Upshot-Knothole | Annie | 3/15/1953 |
| UK02 | Upshot-Knothole | Nancy | 3/24/1953 |
| UK03 | Upshot-Knothole | Ruth | 3/31/1953 |
| UK04 | Upshot-Knothole | Dixie | 4/6/1953 |
| UK05 | Upshot-Knothole | Ray | 4/11/1953 |
| UK06 | Upshot-Knothole | Badger | 4/18/1953 |
| UK07 | Upshot-Knothole | Simon | 4/25/1953 |
| UK08 | Upshot-Knothole | Encore | 5/8/1953 |
| UK09 | Upshot-Knothole | Harry | 5/19/1953 |
| UK10 | Upshot-Knothole | Grable | 5/25/1953 |
| UK11 | Upshot-Knothole | Climax | 6/4/1953 |

## Age Groups

| Age Group ID | Age Group |
| ---: | --- |
| 2 | 11-20 week |
| 3 | 21-30 week |
| 4 | 31-40 week |
| 5 | 0-2 month |
| 6 | 3-5 month |
| 7 | 6-8 month |
| 8 | 9-11 month |
| 9 | 1-4 year |
| 10 | 5-9 year |
| 11 | 10-14 year |
| 12 | 15-19 year |
| 13 | Adult male |
| 14 | Adult female |

## References

- Simon SL, Bouville A, Beck HL. The geographic distribution of radionuclide deposition across the continental US from atmospheric nuclear testing. Journal of Environmental Radioactivity. 2004;74:91-105.
- National Cancer Institute. Estimated exposures and thyroid doses received by the American people from iodine-131 in fallout following Nevada atmospheric nuclear bomb tests. Bethesda, MD: NCI; NIH Publication No. 97-4264; October 1997. Available at: https://radiationcalculators.cancer.gov/fallout.
- Department of Health and Human Services. A report on the feasibility of a study on the health consequences to the American population from nuclear weapons tests conducted by the United States and other nations. Prepared for the U.S. Congress; 2005. Available at: https://www.cdc.gov/nceh/radiation/fallout/default.htm.
