# PBI_tableLookUp
Python script to find tables being used within your Power BI (.pbix) files.
After a day of scourging the internet to find something that would help me with this, I'd decided to just write this myself. 
I hope this helps you as much as it has helped me for cleaning up unused tables within my data model. 


To use this script, create a folder and put all files from here in it.

There are 3 Python scripts in this repo: main.py, cleanUp.py, and searchForTable.py

When you first use this, you will have to set the paths inside of all the scripts that you are running (there are comments in the code on what paths to change)
Run the main.py program first as this will take all of your .pbix files from your folder (it **WONT** remove them, just make copies it needs) and extract them into
a temporary folder and then convert them to a ZIP file. From there it will extract the ZIP files into another folder (you will set the path in the script). After it
extracts the ZIP files, it will convert the layout file inside of it to a text file. The script will then ask you for a Table Name you want to search for. It will parse the
newly created layout_output.txt file and create a SearchReults.txt file (you will set the path where you want that to be created) that will list all of the reports
that utilize that Table Name. The program is not case sensitive (FactTable and facttable will return same results) but does need to be exact of what the table is
(for example: FactTable and FactTa will not result in the same findings. You must put in the full namme of the table you're looking for)
