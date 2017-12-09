DBeaver provides a wizard that guides you through the steps to create a connection.
If you run DBeaver for the first time (standalone version), the new connection wizard appears automatically.
In other cases, to create a connection, click:
* Either the **New Connection** button in the application toolbar or in the Database Navigator view toolbar:

  [[images/connect-wizard-item.png]]

* Or **Database -> New Connection** in the menu bar:

  <img src="https://www.dropbox.com/s/g2g9hatjs1c8chx/new%20connection%20on%20menu.png?raw=1"/>

Then, in the Create new connection wizard:
1. Choose a driver for the new connection: click the suitable database type in the list. Then click **Next**.
   
   [[images/connect-wizard-driver.png]]  

   To quickly find the needed driver, you can type a hint in the text field above the list of drivers.  
   If you cannot find a driver for your database then probably there is no suitable driver and you need to create one. Please see [[Create database driver|Create-database-driver]] article.  

   NOTE: The list of database drivers diaplays the number of exising connections next to each driver. No number is displayed if there are no connections.

2. In the Connection Settings screen, on the General tab, set all primary connection settings and then click **Next**:

   [[images/connect-wizard-settings.png]]  

   For most drivers required settings include:   
   - Host  
   - Port  
   - Database name  
   - User name and password  

   However, the number and type of connection properties are very dependent on the driver.  
   For example, embedded drivers (such as SQLite, Derby Embedded, HSQLDB, H2 Embedded), unlike remote ones, require only the path to the database. 

3. If necessary, specify advanced settings, see **Advanced Settings** section below, and click **Next**.
4. In the final screen, you can set the connection name, type and initial settings (such as bootstrap queries, transaction state, global filters, etc.).

   [[images/connect-wizard-general.png]] 

5. To test if the connection works, click **Test Connection**.
6. Click **Finish**. The connection appears in the tree of connections in the Database Navigator and DBeaver actually connects to the database.

 

# Advanced Settings
## Driver Properties
Each driver has its own set of additional properties. Refer to the driver documentation to get information about available properties and their values. 
 
[[images/connect-wizard-settings-driver.png]]  

## Network Settings (SSH, SOCKS, SSL)
If your database cannot be accessed directly, you can use SSH tunnel:

[[images/connect-wizard-ssh.png]]  
