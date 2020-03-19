# RuggedCSV

A simple C# library to read .csv files to DataTables, and write DataTables to .csv files.

## Installation

1. Download the RuggedCSV.dll
2. In Visual Studio, Click Project->Add Reference...
3. Browse for the RuggedCSV.dll in the downloaded location, click Add, and then click OK.


## Usage

### Importing

First add the using state as shown below.

```c#
using static RuggedCSV.RuggedCSV;
```
You now have access to the following methods:
* ReadCSV_ToDataTable(string filePath)
* WriteCSV_FromDataTable(DataTable myDataTable, string filePath)
### Read .csv file to DataTable
The **ReadCSV_ToDataTable** method returns a DataTable from the given filePath. E.g. C:\output.csv

Example:
```c#
DataTable myDataTable = ReadCSV_ToDataTable("output.csv");
```

### Write .csv file from DataTable
The **WriteCSV_FromDataTable** method returns a boolean value, true if successful and false is an error occurred.

Example:
```c#
if (WriteCSV_FromDataTable(myDataTable, "output.csv"))
{
    // Write successful
}
else
{
    // Write unsuccessful
}
```
## License
[MIT](https://choosealicense.com/licenses/mit/)
