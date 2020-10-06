[Create Linked Servers SQL Server Database Engine](https://docs.microsoft.com/en-us/sql/relational-databases/linked-servers/create-linked-servers-sql-server-database-engine?view=sql-server-ver15)

### SQL Server Linked Server
* Open SQL Server Management Studio desktop application
* Log in as System Administrator
  * Expand: Server Objects
    * Right Click: Linked Servers
      * Click: New Linked Server
        * New Linked Server
          * General Page
            * Input: Linked Server
              * Remote SQL Server you are connecting to
            * Server type
              * Select: SQL Server
          * Security Page
            * Select: Be made using this security context
              * Input: Remote login username
              * Input: Remote login password
          * Click: OK
          * Right Click: Linked Server
            * Click: Test Connection
* Example Select Statement
  * `select`<br />
    `*`<br />
    `from [Linked_Server_Name_IP_Address].[Databasename].[Objectname].[Tablename]`
* Example Open Query Statement
  * `select`<br />
    `sqlserver.*`<br />
    `from openquery`<br />
    `(`<br />
    `"Linked_Server_Name_IP_Address",`<br />
    `'select`<br />
    `*`<br />
    `from [Objectname].[Tablename]'`<br />
    `) as sqlserver`

[Creating A Linked Server With A Postgres Database](https://peter-whyte.com/creating-a-linked-server-with-a-postgres-database/)<br />
[How To Create A Linked Server To Connect To PostgreSQL From SQL Server](https://dbtut.com/index.php/2019/10/22/how-to-create-a-linked-server-to-connect-to-postgresql-from-sql-server/)<br />
[PostgreSQL Drivers](https://www.postgresql.org/ftp/odbc/versions/msi/)<br />
[SQL Server And PostgreSQL Linked Server Configuration Part 2](https://www.mssqltips.com/sqlservertip/3662/sql-server-and-postgresql-linked-server-configuration--part-2/)<br />
[MSSQL MySQL Linked Server](https://gunnarpeipman.com/mssql-mysql-linked-server/)

### PostgreSQL Linked Server
* Download and Install PSQL ODBC Drivers
  * [PostgreSQL Drivers](https://www.postgresql.org/ftp/odbc/versions/msi/)
* Install PSQL ODBC Driver
  * Double Click: psqlodbc_x64.msi
  * Click: Next
  * Check: I accept the terms in the License Agreement
    * Click: Next
  * Install ODBC Driver and Documentation
    * Click: Next
  * Click: Install
    * WAIT FOR THIS TO FINISH
  * Click: Finish
* Create ODBC Data Source
  * Windows Server
    * Open Server Manager
      * Click: Tools
        * Select: ODBC Data Source (64-bit)
  * ODBC Data Source
    * Select: System DSN Tab
    * Click: Add button
    * Create New Data Source
      * Select: PostgreSQL Unicode(x64)
    * Click: Finish
    * PostgreSQL Unicode ODBC Driver Setup
      * Input all information for proper connection
      * Click: Test
      * Click: Save
    * Click: OK
* Open SQL Server Management Studio desktop application
* Log in as System Administrator
  * Expand: Server Objects
    * Right Click: Linked Servers
      * Click: New Linked Server
        * Linked Server
          * New Linked Server
            * General
              * Provider: Microsoft OLE DB Provider for ODBC Drivers
            * Server Options
              * RPC: True
              * RPC Out: True
              * Click: OK
          * Providers
            * Right Click: MSDASQL
              * Select: Properties
              * Check: Level zero only
              * Click: OK
* Example Select Statement
  * `select`<br />
    `*`<br />
    `from [Linked_Server_Name_IP_Address]...[tablename]`<br />
* Example Open Query Statement
  * `select`<br />
    `postgresql.*`<br />
    `from openquery`<br />
    `(`<br />
    `"Linked_Server_Name_IP_Address",`<br />
    `'select`<br />
    `*`<br />
    `from [tablename]'`<br />
    `) as postgresql`

[Create A Linked Server To MySQL From SQL Server](https://www.mssqltips.com/sqlservertip/4577/create-a-linked-server-to-mysql-from-sql-server/)<br />
[MSSQL MySQL Linked Server](https://gunnarpeipman.com/mssql-mysql-linked-server/)<br />
[Configure ODBC Drivers For MySQL](https://www.sqlshack.com/configure-odbc-drivers-for-mysql/)<br />
[MSSQL MySQL Linked Server](https://gunnarpeipman.com/mssql-mysql-linked-server/)

### MariaDB/MySQL Linked Server
* Download and Install MySQL ODBC Drivers
  * [MySQL Connector And Driver](https://dev.mysql.com/downloads/connector/odbc/)
* Install MySQL ODBC Driver
  * Double Click: mysql-connector-odbc-8.0.21-winx64.msi
  * Click: Next
  * Select: I accept the terms in the License Agreement
    * Click: Next
  * Select: Complete
    * Click: Next
  * Click: Install
    * WAIT FOR THIS TO FINISH
  * Click: Finish
* Create ODBC Data Source
  * Windows Server
    * Open Server Manager
      * Click: Tools
        * Select: ODBC Data Source (64-bit)
    * ODBC Data Source
      * Select: System DSN Tab
      * Click: Add button
      * Create New Data Source
        * Select: MySQL ODBC 8.0 Unicode Driver
      * Click: Finish
      * MySQL Connector/ODBC Data Source Configuration
        * Input all information for proper connection
        * Click: Test
        * Click: OK
* Open SQL Server Management Studio desktop application
* Log in as System Administrator
  * Expand: Server Objects
    * Right Click: Linked Servers
      * Click: New Linked Server
        * New Linked Server
          * Linked Server
            * General
              * Provider: Microsoft OLE DB Provider for ODBC Drivers
            * Server Options
              * RPC: True
              * RPC Out: True
              * Click: OK
          * Providers
            * Right Click: MSDASQL
              * Select: Properties
              * Check: Level zero only
              * Click: OK
* Example Select Statement
  * `select`<br />
    `*`<br />
    `from [Linked_Server_Name_IP_Address]...[Tablename]`<br />
* Example Open Query Statement
  * `select`<br />
    `mariadb.*`<br />
    `from openquery`<br />
    `(`<br />
    `"Linked_Server_Name_IP_Address",`<br />
    `'select`<br />
    `*`<br />
    `from [Tablename]'`<br />
    `) as mariadb`<br />
