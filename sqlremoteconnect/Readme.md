SQL Remote Connection
* Allow Remove Connection
** Open SSMS as an administrator
*** Login
*** Right click Server Name
*** Click properties
*** Click Connections under Select a page
**** Make sure the check Allow remote connections to this server is checked
** Open SQL Server Configuration Manager
*** Expand SQL Server Network Configuration in the left pane
**** Select Protocols for Instance Name
***** Enable Named Pipes and TCP/IP is not already enabled
***** Click Okay to the Warning
**** Right click on TCP/IP
**** Click properties
**** Select the IP Addresses tab
***** Make sure port is 1433 for all ports and the IP Address is correct for IP2
****** This can be check by opening the cmd and typing in ipconfig
***** Click Okay
*** Click On SQL Server Services on the left pane
**** Right click SQL Server (Instance Name)
***** Select restart
*** Windows Defender Firewall
**** Click on Advanced Settings
***** Select Inbound Rules in the left pane
***** Click New Rule... in the right pane
***** Select Port in the New Inbound Rule Wizard
***** Click Next
***** Make sure TCP is selected
***** Specific local ports should be 1433
***** Click Next
***** Make sure Allow the connection is selected
***** Click Next
***** Make sure all Domain, Private, and Public are checked
***** Click Next
***** Give the new rule a name
****** e.g. Allow_SQL_Connection
***** Give the new rule a description but is optional
***** Click Finish