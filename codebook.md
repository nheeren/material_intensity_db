# Codebook for MI database

This file and [`codebook.csv`](codebook.csv) document the structure of the data file and documents its variables. Codebooks are a common way to document data files and their contents. 

## Codebook columns

The codebook has the following columns:

1. `variable_name`: The name of the variable
2. `unit`: The unit that applies to the variable. 'n/a' if it has no unit, e.g. for a comment variable.
3. `values`: An explanation of the allowable values for this variable, e.g. integer, float number, text, etc.
4. `classification_scheme`: Provides a scheme which the variable follows, e.g. an ISO standard.
5. `missing_data`: Describes how missing values are treated for the variable.
6. `required`: Indicates if the variable is required for submission of new data.
7. `notes`: Additional notes, remarks, or comments that contextualize the information conveyed in the variable.

## Variables

See also the [tabular variable descriptor file](cookbook.csv).

TODO

- 

## Special values

- `zero` A zero value is simply given as the number zero. However, it must only be used if the number has been measured and provided in the data source.
- `NULL`: No data was provided. Same as an empty field.
- `n/a`: This variable does not apply to this study or data source.

## References

- https://www.ukdataservice.ac.uk/manage-data/document/data-level/tabular
- https://www.icpsr.umich.edu/icpsrweb/content/shared/ICPSR/faqs/what-is-a-codebook.html

