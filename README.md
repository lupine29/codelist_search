User Instruction Guide for Medical Condition Code Search
This Python script allows users to search for medical condition codes from two sources: HDRUK API and OpenCodelists website.

Features

Choice of Source: Search from HDRUK, OpenCodelists, or both.
Flexible Search: Choose between simple or advanced search methods for HDRUK.
Custom Save Location: Opt for a custom directory where search results will be saved.
Excel Preparation: A unique feature for HDRUK that lets you prepare SNOMED codes for Excel.

Prerequisites
Python 3.x installed.
Required Python packages: requests, pandas, BeautifulSoup4, os, csv, json, re, datetime.
You can install these via pip:

bash
Copy code
pip install requests pandas beautifulsoup4

How to Run the Script
Navigate to the Script: Open a terminal and navigate to the folder where the script is located.
Run the Script: Type python script_name.py to run the script. Replace script_name with the actual name of the script.

User Inputs
Choosing a Source
When prompted:

sql
Copy code
Which source would you like to search? (Enter 'opencodelists', 'hrduk', or 'both'):
Type opencodelists to search only OpenCodelists.
Type hrduk to search only HDRUK.
Type both to search both sources.

Providing Search Terms
When prompted:


csharp
Copy code
Please enter the conditions you are interested in, separated by commas:
Enter the medical conditions you'd like to search for, separated by commas (e.g., Diabetes, Asthma).

Advanced Search (HDRUK Only)
When prompted:

sql
Copy code
Would you like to use advanced search techniques? (y/n):
Type y for Yes and n for No.

Custom Save Location (HDRUK Only)
When prompted:

vbnet
Copy code

Do you want to choose the save location for the outputted results? (y/n):
Type y for Yes and n for No.
If you chose 'Yes', you will be asked to enter the directory where you'd like to save the files.


Excel Preparation (HDRUK Only)
After the search is complete, you'll be prompted:

sql
Copy code
Would you like to alter any SNOMED codes to prepare them for Excel? (y/n):
Type y for Yes and n for No.

Output
The script will generate text files containing the codes for each medical condition. These files will be saved in the chosen or default directory.

For HDRUK, the files are tab-separated text files.
For OpenCodelists, files include CSVs and a metadata JSON file.

Troubleshooting
API Error: If you see Failed to fetch data for condition, it means the HDRUK API couldn't be reached for that particular search.
Invalid Source Selection: If you enter an invalid source, the script will terminate with a message "Invalid source selection".
