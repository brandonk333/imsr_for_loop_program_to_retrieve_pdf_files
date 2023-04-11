# ismr_for_loop_program_to_retrieve_pdf_files
This program is a Python script designed to retrieve daily IMSR (Interagency Mobilization Status Report) PDF files from the NIFC (National Interagency Fire Center) website for a specified year and save them to a local directory. 

The script imports the necessary modules to run the program - requests, os, and datetime.

A variable year is initialized with the year for which we want to download IMSR files.

A folder is created to store IMSR files for the specified year. The folder's name is created using an f-string format with the current year.

A for loop is used to loop through all the months of the year.

An if-else statement is used to get the number of days in each month of the year. The number of days in December is calculated differently since it is the last month of the year.

Another for loop is used to loop through all the days in each month of the year.

The day and month numbers are converted to zero-padded strings.

A URL is constructed based on the year, month, and day of the IMSR file we want to download.

The filename is constructed based on the year, month, and day of the IMSR file we want to download.

A filepath is constructed using the folder name and filename.

The script sends a GET request to the URL and saves the response content to the file path.

If the GET request is successful, the script prints a message saying that the file was successfully downloaded. Otherwise, it prints a message saying that the file download failed.

The script completes after all the IMSR files for the specified year have been downloaded and saved to the local directory.

Overall, this program uses Python's requests module to download IMSR files for a given year from the NIFC website and saves them to a local directory using the os module. It does this by iterating through all the days of each month and constructing the appropriate URL for each file.
