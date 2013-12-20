# jQuery Tabel to CSV plugin

A simple, lightweight jQuery plugin for reading a table and outputting its data as a csv file. 

## Instalation

Include script *after* the jQuery library (unless you are packaging scripts somehow else):

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