# Material intensity database project

***Work in progress – this repository will be part of a scientific publication.***

:floppy_disk:  Welcome to the Material Intensity Research Database MIR-DB!  :floppy_disk:  

This database contains data on material intensity of buildings, but can be extended for further infrastructure in the future. The initial database version was assembled (seeded) by Heeren and Fishman (submitted). The publication provides some analysis of the data and discusses a number of applications for the database.

## Content

- [CONTRIBUTING](CONTRIBUTING.md): Guidelines on contributing data
- [Codebook](codebook.md): Document describing the database, meaning of parameter values, and the [codebook table](codebook.csv).
- [codebook table](codebook.csv): Tabular document describing the database variables.
- [data/buildings.csv](data/buildings.csv): The building material intensity database
- [references/buildings.csv](references/buildings.bib): References to the data sources used in the material intensity data file.

## Contributing

*Data contributions, and further extensions to the database are very much encouraged.* The more data is contained in the MIR-DB, the more meaningful analysis and can be made with it.

### New data

In case you know of a potential data source, but do not want to provide the data yourself, please consider [creating an issue](https://github.com/nheeren/material_intensity_db/issues/) and leaving a link to the dataset, or [send me an email](https://github.com/nheeren).

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for more info on how to contribute data. We encourage the use of the [liberated_data project](https://github.com/nheeren/liberated_data) if you are extracting data from non-portable, such as figures or tables in PDF files.

### Database structure

For proposing new database attributes or changes to existing ones, please create an issue and propose a new [codebook](codebook.md). Please keep in mind that the goal of this project is to provide a comprehensive and complete database. The database contains primary and secondary attributes and the former are required. See the [codebook](codebook.md) for more details.

### Errors

In case you find errors in the data, please correct them (as described in [CONTRIBUTING.md](CONTRIBUTING.md)), [create an issue](https://github.com/nheeren/material_intensity_db/issues/), or [contact me](https://github.com/nheeren).

## Citation

This database has been documented in the following research article: ...

## Acknowledgements

:+1: The following people supported the compilation of the original database (Heeren and Fishman (submitted)):

- Marshall Borrus
- [Edgar Hertwich](https://github.com/Hertwich)
- Fritz Kleemann 
- [Farnaz Nojavan Asghari](https://github.com/farnazn)
- [Thibaud Pereira](https://github.com/ThibPereira)
- Emanuel Riegelbauer

## TODO

- [ ] Determine if a line ending encoding could become an issue for this repo and discuss in [CONTRIBUTING.md](CONTRIBUTING.md) (see [here](https://stackoverflow.com/a/10855862/2075003) and [here](https://help.github.com/articles/dealing-with-line-endings/) for more details on encoding and github)
- [ ] Create a script that makes consistency check:
  - All primary columns have a value?
  - int, float variables do not contain text

- [ ] Database review
  - [ ] Verify if a data conversion applied and update NULLs in column `conversion`
  - [ ] Verify if a data conversion applied and update NULLs in column `aggregation`
  - [ ] Fix no_floors
  - [x] Replace 0 values with NA in construction_period_start
  - [x] review `urban_rural` column. Fill empty fields.	
  - [x] Fill empty `climate_classification` columns
  - [x] Merge comment columns for HDD, CDD, land area, etc into comment column
  - [x] Split `comment`column into conversion, aggregation, comment

- [x] Discuss with Farnaz:
  - N/A vs NULL vs "". What to use when.