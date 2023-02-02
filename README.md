# 2620-Scouting-Data-Compiler

This is the data compiler for FIRST Robotics Competition Team 2620 Scouting Team.
While purposed for the 2023 Season this may be reused as necessary for future seasons.

This tool will simply take in output files from the 2834 Bionic Blackhawks scouting tool and automatically import that data into the main excel document.

NOTE: These instructions will only be applicable for Windows devices.

-------------------------------------
Setup Instructions
-------------------------------------
1. Install Python from https://www.python.org/downloads/
2. Ensure that pip is selected in the installer and that Python is added to your system's environment variables (Admin Priveleges Required)
3. Open the command line and install pandas and openpyxl by running the following two commands
    a. pip3 install pandas
    b. pip3 install openpyxl
4. Open Data_Importer.py and change the value "destinationName" to the name of your scouting excel document.
    NOTE: This does not include .xlsx, only the name of the file. It will default to "Scouting".
5. Also change the desired data sheet name by changing the value "sheetName". It will default to "Sheet1"

Congratulations we are now ready to run the tool.

-------------------------------------
Operating Instructions
-------------------------------------
1. Copy your scouting document to the top level of this project. 
    -Within the folder "2620-Scouting-Data-Compiler"
    -Same level as Data_Importer.py
2. Drop the Blackhawks output data into the Source Files folder. 
    NOTE: These documents will be deleted when the script completes. Please consider having copies of these documents elsewhere.
3. Open cmd and navigate to the project's top level and run the following command:
    python Data_Importer.py
4. The script will run and it will perform the following actions.
    a. Save a copy of the current scouting document and save it in the "Backup Folder"
    b. Copy all .csv files in "Source Files" into the desired sheet in the scouting Excel Document. Deletes all .csv files from this folder.
    c. Saves new version of the scouting document with new data added.

Congratulations! Your data has been saved into your desired Excel document. Lets start collecting some data!