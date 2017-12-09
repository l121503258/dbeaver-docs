The Data editor appears:
* As the **Data** tab of the [Database Object Editor](https://github.com/serge-rider/dbeaver/wiki/Database-Object-Editor) available only for tables and views.
* As the **Results** tab when you run a custom SQL query in [SQL Editor](https://github.com/serge-rider/dbeaver/wiki/SQL-Editor)

The Data editor allows viewing and editing the data of a database table or view.
The central part of the Data editor is the data table. The editor also provides two toolbars and a filter field:

<img src="https://www.dropbox.com/s/r0ul9jadxbtn046/Data%20tab%20with%20markup.png?raw=1"/>

Every cell in the data table has a context menu – right-click the cell to open the menu. The context menu provides the following items:

Menu Item|Description
---------|-----------
**Cut**|Cuts the content of the current cell or column to the clipboard
**Copy**|Copies the content of the current cell or column to the clipboard
**Advanced Copy**|Opens advanced copy submenu that allows copying data with preset formatting parameters 
**Paste**|Pastes the copied content to the cells in focus
**Advanced Paste**|Pastes several values delimited with a tabulation or line break
**Delete**|Deletes the row that has the cell in focus<br/> NOTE: In fact, when users click **Delete**, the system only highlights the row red while the actual deletion happens when users click **Save**.
**Edit cell**|-	For CLOB/BLOB data format, opens the contents of the cell in a new tab<br/> - For all formats except CLOB/BLOB, opens a properties window for the cell<br/>
**Inline edit**|- Same as double-click on a cell<br/>- Makes the cell editable
**Set to NULL**|Sets the value of selected cells to NULL
**Hide column**|Hides the column currently in focus, see the Managing Display of Columns in Data Table section further in this article
**Save to file…**|- Appears only for columns with BLOB/CLOB data<br/>- Opens the standard Save As window that allows saving data contained in the cell to a file 
**Load from file…**|- Appears only for columns with BLOB/CLOB data<br/>- Opens a standard window for opening files
**Order/Filter**|Displays a submenu that allows selecting filter criteria for the data. The submenu contains the most common filters that can be applied to the cell in focus – see details in …<br/> By default, DBeaver filters data by sending a request to the server (the Server-side results ordering checkbox selected). To filter data on the client side using DBeaver`s internal algorithm, clear the checkbox.
**View/Format**|Opens a submenu that provides tools for formatting and modifying the view of data, see …
**Navigate**|Opens a submenu that helps users navigate throughout the data table, see …
**Layout**|Changes the layout of data, see …
**Export Resultset…**|Opens the Data Transfer wizard that guides you through the steps to select a format and export data<br/>NOTE: The system exports the whole result set including records that are not visible in the screen and preserves all applied data filters and ordering.
**Generate SQL**|Opens a submenu on which you can select the type of SQL query to generate
**Refresh**|Refreshes the whole results set including all items that are not visible in the screen



