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

- `zero` A zero value is simply given as the number zero. However, it must only be used if the number has been measured and provided in the data source.
- `NULL`: No data was provided. 
- `n/a`: This variable does not apply to or exist in this study or data source.

## References

- https://www.ukdataservice.ac.uk/manage-data/document/data-level/tabular
- https://www.icpsr.umich.edu/icpsrweb/content/shared/ICPSR/faqs/what-is-a-codebook.html

