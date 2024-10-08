# dconvert

`dconvert` is a command-line tool that allows you to easily convert data files between various formats, including JSON, CSV, XML, HTML, and XLSX. The tool supports advanced options such as newline-delimited JSON, inclusion/exclusion of row indices, and automatic format inference based on file extensions.

## Features

- Convert between **JSON, CSV, XML, HTML, and XLSX** formats.
- Support for newline-delimited JSON (`jsonlines`).
- Option to include or exclude row indices in the output.
- Automatic detection of input and output file formats based on file extensions.
- Simple and intuitive command-line interface.

## Installation

```bash
pip install dconvert
```
or...

Clone this repository and navigate to the project directory:

```bash
git clone https://github.com/aaronlmathis/dconvert.git
cd dconvert
```

### Install the required dependencies.
```bash
pip install -r requirements.txt
```

## Usage
The dconvert tool provides a flexible way to convert data files. Below is a comprehensive guide on how to use it.

###Basic Command Structure
The basic command structure includes specifying the input file, output file, and desired output format. Optional arguments allow you to specify the input file type, whether to use newline-delimited JSON, and whether to include the row index in the output.

#### Required Arguments
- **--input or -i:** Path to the input file to be converted.
- **--outfile or -o:** Path to the converted output file.
- **--format or -f:** The desired output format. Accepted values are csv, json, html, xml, xlsx.

#### Optional Arguments
- **--inputfiletype or -t**: The type of the input file. Accepted values are csv, json, html, xml, xlsx.
If not provided, dconvert will try to infer the input file type from the file extension.
- **--jsonlines or -l:** Whether to output JSON as newline-delimited (true for newline-delimited, false for a single JSON array).
Defaults to false if not specified.
- **--index:** Whether to include the row index in the output (true to include, false to exclude).
Defaults to false if not specified.

#### Examples
Convert a CSV file to JSON as a single JSON array.
```bash
dconvert -i my_file.csv -o my_file.json
```
Convert an XLSX file to JSON with each row as a separate JSON object on a new line.
```bash
dconvert -i my_file.xlsx -o my_file.json -l 
```
Convert a JSON file to CSV and include the row indices in the output.
```bash
dconvert -i my_file.json -o my_file.csv -index
```
Convert an HTML file to XML and exclude the row indices.
```bash
dconvert -i my_file.html -o my_file.xml
```
## Error Handling
If the output format is not specified and cannot be inferred from the output file extension, dconvert will raise an error. If the input file type is not specified and cannot be inferred from the input file extension, dconvert will raise an error.

## File Formats Supported
- JSON: JavaScript Object Notation, supports both single array and newline-delimited formats.
- CSV: Comma-Separated Values, a simple text format for tabular data.
- XML: Extensible Markup Language, used for structured data interchange.
- HTML: HyperText Markup Language, typically used for web pages but also useful for tabular data.
- XLSX: Microsoft Excel Open XML Spreadsheet format.

## Contributing
If you'd like to contribute to dconvert, please fork the repository and submit a pull request. You can also open issues for feature requests or bugs.

## License
This project is licensed under the GPL 3.0 License - see the LICENSE file for details.

## Contact
For any questions, feel free to contact the project maintainer.
