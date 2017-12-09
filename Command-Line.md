# Command line parameters

Command line parameters might be passed directly to dbeaver[.exe] executable.  
On Windows you also can use `dbeaver-cli.exe` executable (it doesn't spawn new window so you can see output messages).  

## DBeaver control
Name|Value|Example
----|-----|-------
`-help`|Prints help message|
`-stop`|Quits DBeaver|
`-dump`|Prints DBeaver thread dump|
`-f`|Opens file in DBeaver UI|`-f c:\some-path\some-file.sql`
`-con`|Opens database connection in DBeaver UI|See [connection parameters table](#connection-parameters)
`-closeTabs`|Closes all open editor tabs|
<nobr>`-disconnectAll`</nobr>|Closes all open connections|
`-reuseWorkspace`|Force reuse of single workspace by multiple DBeaver instances|
`-newInstance`|Force new DBeaver instance creation (do not try to reuse already running one)|

## System parameters

Name|Value|Example
----|-----|-------
-nl|Locale|en_US
-data|Workspace path|c:\ProgramData\MyWorkspace
-nosplash|Omits splash screen|true
-clean|Clears all Eclipse caches. Use it if DBeaver fails to start after version upgrade.
-vmargs|VM parameters|See [VM arguments table](#vm-arguments)

### VM arguments

You can pass any advanced Java parameters supported by your local JVM (Oracle, OpenJDK, IBM, etc).  
Parameters supported by Oracle JVM (1.8): https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html

Parameters supported by all JVMs:

Name|Value|Example
----|-----|-------
-Xms|Sets initial memory available for DBeaver|`-Xmx1000m`
-Xmx|Sets maximum memory available for DBeaver|`-Xmx4000m`

### Connection parameters
All connection parameters must be supplied as a single command line argument, parameters are divided by pipe (`|`). Parameter name and value are divided by `=`.  
Example: `-con driver=sqlite|database=C:\db\SQLite\Chinook.db|name=SQLiteChin|openConsole=true|folder=SQLite`

Name|Value|Example
----|-----|-------
name|Connection name|`Test connection`
driver|Driver name or ID|`driver=sqlite`, `driver=mysql`, etc
url|Connection URL. Optional (JDBC URL may be constructed by driver from other parameters)|`url=jdbc:sqlite:C:\db\SQLite\Chinook.db`
host|Database host name (optional)|`host=localhost`
port|Database port number (optional)|`port=1534`
server|Database server name (optional)|`server=myserver`
database|Database name or path (optional)|`database=db-name`
user|User name (optional)|`user=root`
password|User password (optional)|`password=mysecret`
savePassword|Do not ask use password on connect|`savePassword=true`
connect|Connect to this database|`connect=false`
openConsole|Open SQL console for this database (sets `connect` to true)|`openConsole=true`
folder|Put new connection in a folder|`folder=FolderName`
autocommit|Sets connection autocommit flag (default value depends on driver)|`autocommit=true`
prop.propName|Advanced connection parameters (depend on driver)|`prop.connectTimeout=30`