[SSMS Backup](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-ver15)<br />
[Best Easiest Way To Make A SQL Server Dump And Import That Dump In Another SQL](https://stackoverflow.com/questions/5026990/best-easiest-way-to-make-a-sql-server-dump-and-import-that-dump-in-another-sql)

* Open SSMS
* Log into database with credentials of database ownership
* Expand Databases
* Right click database_instance
  * Hover over Tasks
  * Click Back Up...
* General
  * Source
    * Database: database_instance
    * Backup type: Full
  * Destination
    * Back up to: Disk
    * /path/to/backup/
* Backup Options
  * Backup set
    * Name: database_instance_backup_date_time
    * Description: Optional
* Click OK
* NOTE: If you get a sector error, then remove the old bak file and start again
