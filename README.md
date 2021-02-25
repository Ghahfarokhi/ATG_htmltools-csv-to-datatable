# CSV/TSV files to HTML DataTable

Render any csv/tsv files into responsive, sortable, and searchable HTML datatables without any serverside scripting. 
Data files could either be provided via URL parameters [intended usage] or hard coded into the HTML codes. If the URL parameters are used, then the `index.html` file is all-in-one html, javascript and css codes, so it doesn't need to be acompanied by any other helper folder or file. It can be essentially used as a general purpose tool to visualize dats. It can also be renamed to fit be naming schema of a project. In principle, it should be possible to run it on any server. 

## Usage

### URL Parameters

* `table_name` [OPTINAL, default: `data/tab_separated_table.tsv`] : path to the csv/tsv file.
* `separator` [OPTIONA, default: `\t`] : specify the delimiter **charachter**; comma, colon, semi-colon, etc.
* `table_title` [OPTINAL, default: `table_name`] : will appear as the title.
* `paging` [OPTINAL, default: `true`] : determines whether the detatable should be wraped into pages. 

### Demo

URL below is a [demo](https://amirtaheri.info/htmltools-csv-to-datatable/index.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo) of how it can be used. Note the format of parameters used after the `?` mark in the url.

```
https://amirtaheri.info/htmltools-csv-to-datatable/index.html?table_name=data/tab_separated_table.tsv&table_title=CSV to Datatable Demo
```

### Run on localhost

#### MacOS

Open a terminal and download a clone of this repository using the commands below. Open Google Chrome and navigate to `http://localhost:8080/`. 

```bash
git clone https://github.com/Ghahfarokhi/htmltools-csv-to-datatable.git
cd htmltool_csv_to_datatable
php -s localhost:8080
```

### References

* Main javascript function `CSVToArray` have been obtained from [Ben Nadal](https://www.bennadel.com/blog/1504-ask-ben-parsing-csv-strings-with-javascript-exec-regular-expression-command.htm) with slight modifications.
* DataTable HTML codes have been obtained from [datatables.net](https://datatables.net/).

### Errors
Please report errors/bugs to: Amir.Taheri.Ghahfarokhi@gmail.com
