# Contributing guidelines

*Thank you for considering to contribute data to the material intensity database project.*

## Data & variables

Please also refer to the [codebook](codebook.md) and the data descriptor article in Nature Scientific Data. The dataset consists of primary and secondary data attributes. In order to make a (data) contribution to this repository please consider the following guidelines:

1. Primary data must be provided. 
2. Provision of secondary data is optional, but encouraged.
3. Adhere to the given CSV [data format](#Data Format)
4. Create a [pull request](https://help.github.com/articles/creating-a-pull-request/). It is also possible to [edit files online on github](https://help.github.com/articles/editing-files-in-another-user-s-repository/), which may be inconvenient for larger changes.

We encourage the use of the [liberated_data project](https://github.com/nheeren/liberated_data) if you are extracting data from non-portable, such as figures or tables in PDF files.

## Data format

The file must be compliant to [RFC 4180](https://www.rfc-editor.org/info/rfc4180). [Microsoft Excel seems to do a decent job of exporting RFC compliant csv data](https://superuser.com/a/302338/215109). 

We require that pull requests adhere to the following guidelines (most based on RFC 4180):

- The delimiter is a comma.
- One record / data point per line.
- Every record has the same sequence of fields.
- Include a header column.
- Text should always be wrapped by double quotes. Any field may be quoted (with double quotes). Otherwise fields containing a line-break, double-quote, or commas will cause data corruption.
- A (double) quote character in a field must be represented by two (double) quote characters.
- Use MS-DOS-style lines that end with (CR/LF) characters.
- Use UTF-8 encoded files.

Please refer to the [Wikipedia article](https://en.wikipedia.org/wiki/Comma-separated_values) on CSV for more details.





