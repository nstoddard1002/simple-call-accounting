# simple-call-accounting

Designed to capture SMDR records from any PBX/KSU that can send CSV values to a TCP/IP address & port, this python application delivers "simple" call accounting. 

## Components so far:
* configs.py - sets up the system for the configuration files located in configs/
* ippbx.py - manages connections to the IP PBXs (or KSUs) identified by configs.py
* filemanager.py - creates the needed directories for both call accounting records and error logs, and manages log roll over
* parser.py - uses SMDR information to parse individual call records and validate before saving to call accounting records (or passing the information to the error log for troubleshooting)
* recording.py - currently saves each call record into the CSV files, will eventually connect to a database instead
* database.py - will be used in the future to manage connection to the database and the tables for different PBXs/KSUs
