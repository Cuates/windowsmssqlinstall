Windows Firewall

[Windows Firewall Configuration For SQL Server to allow remote connection](https://www.youtube.com/watch?v=3Eyva0OG2tc)<br />
[How to allow SQL Server thorugh Window Firewall](https://www.youtube.com/watch?v=9O2GLm3iNp8)<br />
[Allow SQL Server through Windows Firewall](https://www.youtube.com/watch?v=3jVTUll4PXs)<br />

* Allow SQL through Windows Firewall
  * Run services.msc
    * Find SQL Server (Instance Name)
    * Right click and select properties
    * Find path to executable and select and copy everything including the double quotes
    * Close properties window
  * Run firewall.cpl
    * Click Allow an app or feature through Windows firewall
      * If everything is greyed out click change settings
    * Click Allow another app
      * Click Browse
      * Paste the path to executable into the filename text box and click open
      * Click Add
      * Ensure private is checked and public is unchecked, if you have a domain column check it
    * Click Allow another app
      * Click Browse
      * Navigate back to the services window
      * Find the service for SQL Server Browser
      * Right click and select properties
    * Find path to executable and select and copy everything including the double quotes
    * Close properties window
  * Navigate back to the Allowed apps and browse window we had opened
    * Click Browse
    * Paste the path to executable into the filename text box and click open
    * Click Add
    * Ensure private is checked and public is unchecked, if you have a domain column check it
    * Click Okay
