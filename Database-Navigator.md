Database Navigator is the main view to work with the structure and content of databases. To open Database Navigator, on the Windows menu, click **Database Navigator**. For information on how to change the view layout, please see the [Application Window Overview](https://github.com/serge-rider/dbeaver/wiki/Application-Window-Overview) article.

[[images/database-navigator.png]]

Database Navigator contains a tree of objects, a toolbar and View menu which contain generic items. Each object in the tree has its own context menu.
The tree contains the following objects:
* Folders - <img src="https://www.dropbox.com/s/kxehrqzy14u88d4/Connection%20folder%20icon.png?raw=1">
* Database connections - <img src="https://www.dropbox.com/s/vcoyyh5ygds38qe/Connections%20icons.png?raw=1"> and other (icons differ depending on the database type)
* Database objects - various depending on the database type, such as Tables <img src="https://www.dropbox.com/s/f4dsi8knfu62v7k/Table%20icon.png?raw=1">, Views <img src="https://www.dropbox.com/s/2plf0fwwaorw82l/View%20icon.png?raw=1">, Columns <img src="https://www.dropbox.com/s/wxffh1j7sd8m2sp/Column%20icons.png?raw=1">, Indexes <img src="https://www.dropbox.com/s/bkegxqbvrohucqq/Index%20icon.png?raw=1">, etc.

To open the view menu of Database Navigator, click the View Menu button (<img src="https://www.dropbox.com/s/k4ut6zbp5apbcdo/View%20menu%20icon.png?raw=1"/>) in the upper-right corner of the window. 
For more information on where to find the view toolbar and menu, please see the [Views](https://github.com/serge-rider/dbeaver/wiki/Views) article.

The menu contains the following items:

Icon|Menu item|Description
----|---------|-----------
<img src="https://www.dropbox.com/s/iwa48qjl029pkzh/Driver%20Manager%20icon.png?raw=1"> |**Driver Manager**|Opens the Driver Manager window that allows creating, editing and deleting drivers for databases. See … for information about managing database drivers
<img src="https://www.dropbox.com/s/dkysg3skiwl2n9e/New%20connection%20icon.png?raw=1"> |**New Connection**|Opens the Create new connection wizard. See … for information about creating connections
(empty) | **Active Project** |Displays a submenu which allows you to choose a project. See ... for information about projects.
<img src="https://www.dropbox.com/s/pg9eoar3zkyymem/New%20Folder%20icon.png?raw=1"> |**New Folder** |Opens a dialog box for creating a new folder
<img src="https://www.dropbox.com/s/jg92vpaegfm8alz/Collapse%20All%20icon.png?raw=1"> | **Collapse All** |Collapses the tree to the root level
<img src="https://www.dropbox.com/s/8ctcn4vmkfex5zt/Link%20with%20editor%20icon.png?raw=1"> | **Link with editor** | Enabled when at least one editor is open, otherwise disabled - highlights the object in the tree that has its editor open

The toolbar is located in the title bar of the window, its buttons duplicate the menu items except for the **Active Project** one. 

To open the context menu for an object, right-click the object in the tree. The following table summarizes context menu items for all types of objects that may appear in the tree. Note that the presence or absence of context menu items for an object depends on the database and object types.

Menu item|Description
---------|-----------
**Open folder**|Opens a folder in a separate view
**Create new connections / Create New Connection**|Opens the Create new connection wizard
**New Folder**|Opens a dialog box for creating a new folder
**Copy**|Copies an object to the clipboard 
**Paste**|Inserts the copied object into a selected folder - most convenient for copy-pasting connections
**Delete**|Deletes an object<br/> **WARNING!** The Delete menu item removes the object not only from the tree but from the database itself or the file system, and this action is irreversible. 
**Rename**|Opens the Rename [object] dialog box
**Properties**|Opens the Properties for [object] window which allows viewing and modifying the object`s properties
**Refresh**|Depending on the object, refreshes the object itself, or its parent, or its subnodes – mostly used for refreshing tables and schemes
**Connect**|Attempts to connect to the database
**Invalidate/Reconnect**|Checks the status of connection, if it is broken, attempts to reconnect
**Disconnect**|Disconnects from the database
**SQL Editor**|Opens a new SQL editor for the connection
**Recent SQL Editor**|Opens the most recently opened SQL editor
**Edit Connection**|Opens the Connection Configuration window that allows configuring connection settings
**View [objects]**|-	For objects that DBeaver can create and delete, opens the object in a separate editor<br/>-	For objects that DBeaver cannot create and delete, opens the object in a separate viewer
**Edit [object]**|-	For objects that DBeaver can create and delete, opens the object in a separate editor<br/>-	For objects that DBeaver cannot create and delete, opens the object in a separate viewer
**Create new [object]**|Opens an editor in which you can specify properties and save the new object
**Filter**|Opens a submenu of one or more filtering options (depending on the object):<br/>-	Hide [object]<br/>-	Show only [object]<br/>-	Configure [objects] filter<br/>-	Toggle filter<br/>-	Clear filter<br/> See ... for information.
**Copy Advanced Info**|Copies the full name of an object
**Read Data in SQL Console**|Opens an SQL console displaying the object`s data
**Copy Advanced Info**|Copies the full name of an object
**Read Data in SQL Console**|Opens an SQL console displaying the object`s data
**Compare**|- Appears only if you select several objects of the same level<br/> - Opens the Compare objects wizard which guides you through the steps to generate a comparison report for the selected objects
**Generate SQL**|Opens a submenu on which you can select the type of SQL query to generate:<br/>- SELECT<br/>- INSERT<br/>- UPDATE<br/>- DELETE<br/>- MERGE<br/>- DDL<br/> Clicking one of the items (for example INSERT) generates a relevant query in a separate window.
**Export Table Data**|Opens the Data Transfer wizard that helps you select a format and export table data 
**Import Table Data**|Opens a window with existing database connections in which you can select a table to import data from 
**Tools**|Opens a submenu that provides tools for database backup and restore, vacuum, etc.

You can filter database objects in Database Navigator, see [Filter Database Objects](https://github.com/serge-rider/dbeaver/wiki/Filter-Database-Objects).
