# find_missing_sds
<br/>
This program is designed specifically for Open Enventory to fix issue with
molecule missing sds (could not be extracted through "Read data from supplier")
This programs does:
    1. Connect into mysql database and find molecule in 'molecule' table
of specific database and find those molecule with missing sds
    2. Try to download sds files into a folder in /var/lib/mysql/missing_sds
    3. Update those sql entries with new downloaded sds files
   

Version 5:
    - Incorporated result from Fluorochem
    - Fixing bug with existing default_safety_sheet_url and default_safety_sheet_mime
    by setting them to NULL


Version 4:
    - Testing using cheminfo.org/webservices by extracting catalog number from fluorochem


Version 3:
    - Refractored extracting url download into its own method
    - Added extracting url download from chemicalsafety.com


Version 2:
    - Added asking if user is root and password
    - Added asking what database to be modified
    - Switch to extracting data from https://www.fishersci.com because Chemexper
    has limited requests
