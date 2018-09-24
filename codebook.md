# Codebook for MI database

This file and [`codebook.csv`](codebook.csv) document the structure of the data file and documents its variables. Codebooks are a common way to document data files and their contents. 

## Codebook columns

The codebook has the following columns:

1. `variable_name`: The name of the variable
2. `notes`: Description of the variable, including notes, remarks, or comments that contextualise the conveyed information.
3. `unit`: The unit that applies to the variable. 'n/a' if it has no unit, e.g. for a comment variable.
4. `values`: An explanation of the allowable values for this variable, e.g. integer, float number, text, etc. This can have multiple items, but only the first will be considered by the verification algorithm. 
5. `classification_scheme`: Provides a scheme which the variable follows, e.g. an ISO standard.
6. `missing_data`: Describes how missing values are treated for the variable.
7. `required`: [TRUE, FALSE] Indicates if the variable is required for submission of new data. A 'True' value means that the field cannot be empty. If the data source does not provide data it must be 'NULL' or 'n/a'. See section [special values](#special-values) for more details.

The database contains *primary* and *secondary* attributes (see the `required` keyword in the list above). Primary attributes are mandatory throughout database and for any data new data contributions, while secondary ones are optional.

Please also consider the technical file formatting guidelines described in the [contributing document](CONTRIBUTING.md).

## Special values

- `NULL`: This is the default value of cells in a new column or row. It should be treated to mean _awaiting data input_. 
If a data contributor has not completed entering data, is unsure, or does not provide secondary data attributes, the corresponding cells should remain NULL. A secondary objective of this project is to minimize 'NULL' valued cells.

### If a material is mentioned in the data source, but without a positive value:
- `0`: A zero value is only the number zero (0). It must only be used if the number zero was explicitly provided in the data source. For example, a building that was studied and found to have no wood content shall have the value '0' in the corresponding column.
- `unspecified`: The data source contains an explicit unspecified value, such as "unspecified", "not available", "-", "unknown", "unclear", "trace amounts", "some", etc. This means that the data creators considered this attribute but have not provided a numerical value (zero or non-zero number). For example, a building that was studied and the data creators state that copper content is known to be part of the building in an unknown amount shall have 'unspecified' in the corresponding column.
### If a material is not mentioned in the data source:
- `NA`: No data identified in the data source, i.e. no data was provided, is not applicable, or could not be attributed. This means that no (suitable) value was found in the source. For example, if a study focused only on steel in reinforced concrete buildings, then the 'concrete' column shall have a 'NA' value: clearly this building has a concrete content but the study doesn't mention its value. 

The version 1.0 release database contains a number of NULL values across some columns because the authors added these attributes at a later stage of the project.

## References

- https://www.ukdataservice.ac.uk/manage-data/document/data-level/tabular
- https://www.icpsr.umich.edu/icpsrweb/content/shared/ICPSR/faqs/what-is-a-codebook.html

