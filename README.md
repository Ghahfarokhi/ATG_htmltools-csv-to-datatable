# CSV/TSV files to HTML DataTable

Render any csv/tsv file into a **responsive**, **sortable**, and **searchable** HTML datatable without any serverside scripting. 
The data file could either be provided via a URL parameter [intended usage] or hard coded into the HTML codes. If the URL parameter is used, then the `table.html` file is a stand-alone file that includes all needed html, javascript and css codes, so it doesn't need to be acompanied by any other helper folder or files. It can be essentially used as a general purpose tool to display tabular data. In principle, it should be possible to run it on any server. 


[<img src="https://raw.githubusercontent.com/Ghahfarokhi/ghahfarokhi.github.io/main/assets/img/htmltools-csv-to-datatable.png">](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo)


## Usage

### URL Parameters

* `table_name` [ **REQUIRED** ] : path to the csv/tsv file. If missing, then a general guideline and a dummy array will be rendered.
* `separator` [optional, default: `\t (tab)`] : specify the delimiter **charachter**; comma `,`, colon `:`, semi-colon `;`.
* `table_title` [optional, default: `table_name`] : will appear as the title.
* `paging` [optional, default: `true`] : determines whether the detatable should be wraped into pages. 
* `style` [optional, default: `display,compact`] other acceptable values include: `none`, `display`, `compact`, `stripe`, 
`hover`, `cell-border`, `row-border`, `order-column`. Multiple value combinations can be used together, separated using a comma.
* `column_filtering` [optional, default: `false`] : will enable per column filtering.
* `scroll_x` [optional, default: `true`] : if disabled, then columns will overflow if their width exceeds the screen width.

### Demo

Note the format of parameters used after the `?` mark in the url examples below:

* **Tab separated**: [default tsv demo](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV%20to%20Datatable%20Demo)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/tab_separated_table.tsv&table_title=CSV to Datatable Demo
```

* **Semicolon separated**: `&separator=;` [semicolon separated demo](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV to Datatable Demo&separator=;
```

* **Styling**: See examples below:
  * `&style=display,compact` : [default](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;)
  * `&style=none` : [none](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=none)
  * `&style=display` : [display](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=display)
  * `&style=compact` : [compact](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=compact)
  * `&style=stripe` : [stripe](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=stripe)
  * `&style=hover` : [hover](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=hover)
  * `&style=cell-border` : [cell-border](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=cell-border)
  * `&style=row-border` : [row-border](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=row-border)
  * `&style=order-column` : [order-column](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=order-column)
  * `&style=hover,cell-border` : [hover,cell-border](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=hover,cell-border)
  * `&style=stripe,compact` : [stripe,compact](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&style=stripe,compact)
  * and so on!


* **Column filtering**: `&column_filtering=true` [Column filtering demo](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&column_filtering=true)
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV to Datatable Demo&separator=;&column_filtering=true
```

* **Large datatables scrollX**: default value is true, to disable use `&scroll_x=false` [disabled scroll_x demo](https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&scroll_x=false) 
```
https://amirtaheri.info/htmltools-csv-to-datatable/table.html?table_name=data/semicolon_separated_table.csv&table_title=CSV%20to%20Datatable%20Demo&separator=;&scroll_x=false
```

* **No parameter provided**: a guideline and a dummy array will be rendered, [No parameter demo](https://amirtaheri.info/htmltools-csv-to-datatable/table.html)
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
Open Google Chrome and navigate to `http://localhost:8080/table.html`.

### Dependencies and References

* Main javascript function `CSVToArray` have been obtained from [Ben Nadal's blog](https://www.bennadel.com/blog/1504-ask-ben-parsing-csv-strings-with-javascript-exec-regular-expression-command.htm).
* DataTable HTML codes have been obtained from [datatables.net](https://datatables.net/).
* JavaScript Library [jQuery](https://jquery.com)

### Errors
Please report errors/bugs to: Amir.Taheri.Ghahfarokhi@gmail.com
