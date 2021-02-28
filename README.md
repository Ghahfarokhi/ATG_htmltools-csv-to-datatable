# CSV/TSV files to HTML DataTable

Render any csv/tsv file into a **responsive**, **sortable**, and **searchable** HTML datatable without any serverside scripting. 
The data file could either be provided via a URL parameter [intended usage] or hard coded into the HTML codes. If the URL parameter is used, then the `table.html` file is all-in-one file that includes html, javascript and css codes, so it doesn't need to be acompanied by any other helper folder or files. It can be essentially used as a general purpose tool to visualize data. It can also be renamed to fit the naming schema of a project. In principle, it should be possible to run it on any server. 


[<img src="https://raw.githubusercontent.com/Ghahfarokhi/ghahfarokhi.github.io/main/assets/img/htmltools-csv-to-datatable.png">](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo)


## Usage

### URL Parameters

* `table_name` [REQUIRED, default: `data/tab_separated_table.tsv`] : path to the csv/tsv file.
* `separator` [optional, default: `\t`] : specify the delimiter **charachter**; comma, colon, semi-colon.
* `table_title` [optional, default: `table_name`] : will appear as the title.
* `paging` [optional, default: `true`] : determines whether the detatable should be wraped into pages. 
* `style` [optional, default=display,compact] other acceptable values: none, display, compact, stripe, cell-border, row-border, order-column. Multiple value combinations can be used together, separated using a comma.
* `column_filtering` [optional, default=false] : will enable per column filtering.

### Demo

Note the format of parameters used after the `?` mark in the url examples below:

* **Tab separated**: [Go to the demo web page](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV to Datatable Demo
```

* **Semicolon separated**: [Go to the demo web page](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV to Datatable Demo&separator=;
```

* **Styling**: [Go to the demo web page](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=display,striped)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV to Datatable Demo&separator=;&style=display,striped
```

* **Column filtering**: [Go to the demo web page](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=display,striped)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV to Datatable Demo&separator=;&style=display,striped&column_filtering=true
```

* **No parameter provided**: [Go to the demo web page](https://amirtaheri.info/htmltools-csv-to-datatable/table.html)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html
```

### Run on localhost

#### MacOS

Open a terminal and download a clone of this repository using the commands below.  

```bash
git clone https://github.com/Ghahfarokhi/htmltools-csv-to-datatable.git
cd htmltool_csv_to_datatable
php -S localhost:8080
```
Open Google Chrome and navigate to `http://localhost:8080/`.

### References

* Main javascript function `CSVToArray` have been obtained from [Ben Nadal](https://www.bennadel.com/blog/1504-ask-ben-parsing-csv-strings-with-javascript-exec-regular-expression-command.htm) with slight modifications.
* DataTable HTML codes have been obtained from [datatables.net](https://datatables.net/).

### Errors
Please report errors/bugs to: Amir.Taheri.Ghahfarokhi@gmail.com
