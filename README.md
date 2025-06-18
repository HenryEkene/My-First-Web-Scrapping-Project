# My-First-Web-Scrapping-Project
In my first web scraping project, I built a Python script to extract structured data from a Wikipedia page listing the largest companies in the United States by revenue. Using libraries like **requests**, **BeautifulSoup**, and **pandas**, I was able to automate the process of retrieving a data table directly from the web and saving it locally for analysis.

The script performs the following key steps:

*  Sends an HTTP request to the Wikipedia URL and loads the page content.

*  Parses the HTML using BeautifulSoup to locate the target table.

*  Extracts both column headers and row data, cleaning the text as needed.

*  Organizes the data into a pandas DataFrame.

*  Saves the final table as a .csv file without the index column to a specified location on my computer.

This project enhanced my understanding of web technologies, HTML structure, and Python data handling — laying a strong foundation for future work in data collection and automation.
