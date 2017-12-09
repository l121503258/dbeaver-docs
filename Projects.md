# Projects

You might need to classify and group database connections into projects.  Projects store objects related not to a particular database but to all database connections. These are usually files stored on the file system.

The Projects view displays all projects created in the system and provides tools to manage them. To open the Projects view, on the **Window** menu, click **Projects** (or use <kbd>ALT+W+P</kbd> shortcut).

<img src="https://www.dropbox.com/s/v51mrexzl4a561z/Projects%20view.png?raw=1"/>

For information on how to change the view layout, please see the [Application Window Overview](https://github.com/serge-rider/dbeaver/wiki/Application-Window-Overview) article.

The projects are organized into a tree and all have the same high-level structure:
* **Connections** – repeat the content of the Database Navigator view for this project. You can perform the same actions over the objects of the databases as in Database Navigator.
* **Bookmarks** – contains bookmarks – shortcuts to database objects, see … 
* **ER Diagrams** - contains ER diagrams that you can drag-and-drop here from other folders
* **Scripts** – contains scripts that you can drag-and-drop here from other folders

The Projects view provides a toolbar and View menu which contain generic items. Each object in the tree has its own context menu.

To open the view menu of the Projects view, click the View Menu button (<img src="https://www.dropbox.com/s/k4ut6zbp5apbcdo/View%20menu%20icon.png?raw=1"/>) in the upper-right corner of the window. The view menu contains the following items:

Icon|Item|Description
----|----|-----------
<img src="https://www.dropbox.com/s/jlswp7lf1fwijvy/Create%20project%20icon.png?raw=1"/>|Create Project|Opens the Create Project wizard
<img src="https://www.dropbox.com/s/t47ic11b7fxt36d/Refresh%20projects%20icon.png?raw=1"/>|Refresh Projects|Refreshes the projects tree to display changes caused by creating modifying or deleting projects 
<img src="https://www.dropbox.com/s/jg92vpaegfm8alz/Collapse%20All%20icon.png?raw=1"/>|Collapse All|	Collapses the tree to the root level
<img src="https://www.dropbox.com/s/8ctcn4vmkfex5zt/Link%20with%20editor%20icon.png?raw=1"/>|Link with editor|- Enabled when at least one editor is open, otherwise disabled<br/>- Highlights the object in the tree that has its editor open

The toolbar is located in the title bar of the window, its buttons duplicate the view menu items except for the **Refresh Projects** one.

To open the context menu for an object in the tree, right-click the object.
For information about context menu items of all objects under the **Connections** node of the tree, please see [Database Navigator](https://github.com/serge-rider/dbeaver/wiki/Database-Navigator).  The context menus of other nodes in the tree contain some basic items for copy-pasting, renaming, deleting objects, managing their properties, creating folders, etc. 
* The **Set Active Project** menu item (for a project root node) makes the project active, that is visible in the Database Navigator. 
* The **Link File (SQL Script)** and **Link Folder** menu items allow creating links to files and folders in the file system.

# Managing Projects
The Projects view allows creating new projects as well as renaming and deleting projects that are not active.
NOTE: You cannot rename or delete a project that is set as active. 

## Creating Project
To create a project, in the Projects view, in the toolbar, click **Create Project** (<img src="https://www.dropbox.com/s/jlswp7lf1fwijvy/Create%20project%20icon.png?raw=1"/>). The Project Create Wizard opens.

<img src="https://www.dropbox.com/s/ri4t1jsae2ojmpt/Create%20project%20wizard.png?raw=1"/>

TBA 

## Deleting Project
To delete a project, in the Projects view, right-click its name in the tree and click **Delete** on the context menu. Two confirmation dialog boxes appear one after another:
1. Delete object dialog box is to confirm the deletion of the project itself. Click **Yes** if you are sure you want to delete it. Otherwise, click **No**.
2. Delete project dialog box is to confirm the deletion of the project`s contents: these are the data stored in the file system, database connections are not affected. Click **Yes** if you want the contents to be deleted as well. To keep the contents, click **No**.

NOTE: If you have deleted a project and then re-create it with the same name, the new project picks up all the database connections of the deleted project.

# Managing Bookmarks
Bookmarks are quick access links to objects of a database. They appear in the project tree inside the Projects or Project Explorer views.

To create a bookmark:
1. In the Database Navigator or under **Connections** node of the Projects view, click the database object of interest to set focus on it.
2. Press <kbd>CTRL+d</kbd>. The **Bookmark Name** dialog box appears.
3. In the **Bookmark Name** field, enter the bookmark name, then in the **Bookmark folder** field, click the folder, and then click **OK**. The bookmark appears in the selected folder of the related project.

To open an object using its bookmark, double-click the bookmark or right-click it and click **Open Bookmark** on the context menu. You can rename and delete bookmarks using the context menu as well. 
