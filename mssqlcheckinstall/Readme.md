Microsoft SQL Server Check and Install

Check the system
* After opening the SQL Server Installation Center
** Click System Configuration Checker
*** Show details and see if everything has passed
** Click Okay


Install
* Click the Installation on the left pane
** Click New SQL Server stand-alone installation or add features to an existing installation
*** Enter product key if you have one else choose free edition
*** Click Next
*** Check I accept the license terms and Privacy Statement box
*** Click Next
**** Wait for this process to finish
*** Click Next
**** Wait for this process to finish
*** Click Next
*** Check the features you want
**** At the minimum you will need to check Database Engine Services
**** Leave all the directories as is
*** Click Next
**** Wait for this process to finish
*** Leave instance id to Default instance
**** Unless you need it to be called something else
*** Click Next
**** Wait for this process to finish
*** Note if PolyBase was chosen then leave default option as is
**** Click Next
*** Note if Java was chosen then leave default option as is
**** Click Next
*** Click Next
*** Leave all server configuration options as is except for
**** SQL Server Browser should be set to Automatic
**** Click Next
*** Add Current User to the Database Engine Configuration
*** Select Mixed Mode for authentication Mode (user can either be from a domain or added manually in the SQL instance)
**** Enter sa password
**** Click Next
*** If Analysis was chosen
**** Add Current User as administrator then leave option as is
**** Select Multidimensional and Data Mining Mode
**** Click Next
*** Integration Services Scale Out Configuration - Master Node
**** Leave as is
**** Click Next
*** Integration Services Scale Out Configuration - Worker Node
**** Leave as is
**** Click Next
*** Distributed Replay Controller
**** Add Current User
**** Click Next
*** Distributed Replay Client
**** Leave as is
**** Click Next
*** Consent to install Microsoft R Open
**** Accept
***** Wait for this process to finish
**** Click Next
*** Consent to install Python
**** Accept
***** Wait for this process to finish
**** Click Next
*** Ready to Install
**** Check that everything is correct
**** Click Next
*** Click Install
**** Wait for this process to finish (this will take a while)
*** Check to make sure all Succeeded and Green Check Marks
**** Click Close