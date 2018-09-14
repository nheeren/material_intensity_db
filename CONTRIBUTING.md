# Contributing guidelines

*Thank you for considering to contribute data to the material intensity database project.*

## Data & variables

Please also refer to the [codebook](codebook.md) and the data descriptor article in Nature Scientific Data. The dataset consists of primary and secondary data attributes. In order to make a (data) contribution to this repository please consider the following guidelines:

1. Primary data must be provided. 
2. Provision of secondary data is optional, but encouraged.
3. Adhere to the given CSV [data format](#Data Format)
4. Create a [pull request](https://help.github.com/articles/creating-a-pull-request/)

## Data format

The file must be compliant to RFC 4180. [Microsoft Excel seems to do a decent job of exporting RFC compliant csv data](https://superuser.com/a/302338/215109). Some of the most important implications are:

- The delimiter is a comma.
- One record / data point per line.
- Every record has the same sequence of fields.
- Include a header column.
- Text should always be wrapped by double quotes. Any field may be quoted (with double quotes). Otherwise fields containing a line-break, double-quote, or commas will cause data corruption.
- A (double) quote character in a field must be represented by two (double) quote characters.
- Use MS-DOS-style lines that end with (CR/LF) characters.

Please refer to the [Wikipedia article](https://en.wikipedia.org/wiki/Comma-separated_values) on CSV for more details.





