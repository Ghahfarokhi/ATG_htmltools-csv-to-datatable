# CSV/TSV files to HTML DataTable

Render any csv/tsv file into a **responsive**, **sortable**, and **searchable** HTML datatable without any serverside scripting. 
The data file could either be provided via a URL parameter [intended usage] or hard coded into the HTML codes. If the URL parameter is used, then the `index.html` file is all-in-one file that includes html, javascript and css codes, so it doesn't need to be acompanied by any other helper folder or files. It can be essentially used as a general purpose tool to visualize data. It can also be renamed to fit the naming schema of a project. In principle, it should be possible to run it on any server. 

## Usage

### URL Parameters

* `table_name` [optional, default: `data/tab_separated_table.tsv`] : path to the csv/tsv file.
* `separator` [optional, default: `\t`] : specify the delimiter **charachter**; comma, colon, semi-colon, etc.
* `table_title` [optional, default: `table_name`] : will appear as the title.
* `paging` [optional, default: `true`] : determines whether the detatable should be wraped into pages. 

### Demo

URL below is a [demo](https://amirtaheri.info/htmltools-csv-to-datatable/index.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo) on how it can be used. Note the format of parameters used after the `?` mark in the url.

```
https://amirtaheri.info/htmltools-csv-to-datatable/index.html?table_name=data/tab_separated_table.tsv&table_title=CSV to Datatable Demo
```

### Run on localhost

#### MacOS

Open a terminal and download a clone of this repository using the commands below.  

```bash
git clone https://github.com/Ghahfarokhi/htmltools-csv-to-datatable.git
cd htmltool_csv_to_datatable
php -s localhost:8080
```
Open Google Chrome and navigate to `http://localhost:8080/`.

### References

* Main javascript function `CSVToArray` have been obtained from [Ben Nadal](https://www.bennadel.com/blog/1504-ask-ben-parsing-csv-strings-with-javascript-exec-regular-expression-command.htm) with slight modifications.
* DataTable HTML codes have been obtained from [datatables.net](https://datatables.net/).

### Errors
Please report errors/bugs to: Amir.Taheri.Ghahfarokhi@gmail.com
