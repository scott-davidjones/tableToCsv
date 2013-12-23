# jQuery Table to CSV plugin

A simple, lightweight jQuery plugin for reading a table and outputting its data as a csv file. This plugin was created to allow more flexability with downloading straight from JavaScript and allows the user to specify a name, file extension and if table headers should be outputted.

## Instalation

Include script *after* the jQuery library (unless you are packaging scripts some other way):

```html
<script src="/path/to/jquery.cookie.js"></script>
```

## Usage

Ensure your table has the following layout:

```html
<table id="myTable">
	<thead>
		<tr>
			<th>Column 1</th>
			<th>Column 2</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>cell 1</td>
			<td>cell 2</td>
		</tr>
	</tbody>
</table>
```

Simply and easy to use:

```javascript
$('#table_element').tableToCsv();
//OR
$('.table_element').tableToCsv();
```

##Options

tableToCsv allows you to specify a range of options by passing in an object like so:

```javascript
var options = {
	seperator: '|',
	fileName: 'my_file',
	extension: 'txt',
	outputheaders: false
}
$('#table_element').tableToCsv(options);
```
### seperator

Specify this to change the charactor used for seperating your values, e.g. '|', ',', '\t'

### fileName

Name of the file, do not include the extension.

### extension 

File extension to use, for example: 'csv', 'txt', 'tsv'

### outputheaders

Specify true to generate a header row based on the tables `thead`

### Default Options

Default options are as follows:
- seperator: ',',
- fileName: table ID,
- outputheaders: true,
- extension: 'csv'

## Compatability

tableToCSV uses the new HTML5 ```download``` attribute for ```<a>``` elements. As such this plugin will only work for browsers that support this functionality. tableToCSV has been tested in latest Chrome, firefox and Opera.

## Issues

Internet Explorer and Safari are know to have issues and I am working on them.

### Bugs

Please use the issue tracker for submitting bugs

## Contributing

If you wish to contribute please fork and submit merge requests.