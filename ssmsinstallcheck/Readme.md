Microsoft SQL Server Management Studio (SSMS)

(Download SQL Server Management Studio SSMS)[https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15]<br />

* Download and install SQL Server Management Studio (SSMS)
  * Install and restart machine
  * Launch SSMS
    * Make sure you are able to connect to the SQL Server via SSMS
    * Create database
      * Right click database
      * Select New database...
      * Type database name
      * Leave Owner as is
      * Use logical name for file name
      * Click Okay
    * Create new users
      * Login as administrator
      * Expand security
      * Right click logins
      * Select New Login...
      * Type Login name of user
      * Select SQL Server Authentication
      * Type in password
      * Un-check
        * Enforce password expiration
        * User must change password at next login
      * Select a default database
      * Select a default language
      * Select server roles on the left pane
        * Default server role to public
      * User mapping
        * Check map for the database of choice
        * User default to user name of choice
        * Default schema is dbo
        * Check db_reader
        * Check db_writer
        * Check db_owner
        * Leave public checked
        * Click Okay
