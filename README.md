# Grasslands in Latvia

This repository contains code and documentation for analyzing grassland areas in Latvia.

-----------------

## Project Structure

```
01_LUC/              - Land Use Classification analysis
02_age/              - Grassland Age Analysis
data/                - Raw and processed data
environment.yml      - Conda environment definition
config_local.py      - Local configuration file
```

-----------------

## Cloning the Repository

To clone this repository, use the following command:

```bash
git clone https://github.com/bredijs/grassLVnd
cd grassLVnd
```

-----------------

## Environment Setup

1. Install Miniforge: <https://github.com/conda-forge/miniforge> (or any other Conda distribution)

2. Create the environment:

   ```bash
   conda env create -f environment.yml
   ```

3. Activate the environment:

   ```bash
   conda activate zalaju_petijums
   ```

4. Verify the environment is set up correctly:

   ```bash
   python --version
   ```

Tested on Windows 11.

-----------------

### Configuration File

The `config_local.py` file contains the local configuration variables for [Copernicus Data Space Ecosystem (CDSE)](https://documentation.dataspace.copernicus.eu/APIs/S3.html). You need to update the file contents with your key ID and secret access key:

```python
KEY_ID = "YOUR_KEY_ID"
SA_KEY = "YOUR_SECRET_ACCESS_KEY"
```

-----------------

## Analysis Workflow

Run the scripts in sequence:

1. 01_LUC/ - Performs land use classification using satellite imagery.
2. 02_age/ - Determines the continuity of grasslands across analysis years.

-----------------

## Data Sources

- [Lauksaimnieku deklarētās platības 2024.gadā](https://data.gov.lv/dati/dataset/lauksaimnieku-deklaretas-platibas-2024-gada) (LAD_lauki_url)
- [Meža valsts reģistra meža dati](https://data.gov.lv/dati/dataset/meza-valsts-registra-meza-dati) (MVR_url)
- [Aizsargājamās dzīvotnes - biotopi](https://data.gov.lv/dati/dataset/aizsargajamas-dzivotnes-biotopi) (biotopi_url)
- [Valsts adrešu reģistra atvērtie dati](https://data.gov.lv/dati/dataset/varis-atvertie-dati) (adreses_url)
- [Administratīvās teritorijas – 2021](https://data.gov.lv/dati/dataset/atr) (admin_url)
- [Latvijas Republikas administratīvo teritoriju karte uz 2021. gada 1. jūliju](https://data.gov.lv/dati/lv/dataset/administrativo-teritoriju-karte) (admin_url_detailed)
- [Pieturvietas](https://data.gov.lv/dati/dataset/pieturvietas) (pieturas_url)
- [Lauku atbalsta dienesta 2005. gada LIZ poligoni](https://www.lad.gov.lv/lv) (LAD_2005_izejas.gdb, jāiegūst pieprasot)