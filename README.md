PS 239T Final Project
Sarah Lee

## Short Description

My project compares sermons from a Chinese official church to those from an American church. Using Python, I webscrape from a Chinese webpage and two American church webpages, and also all of the links to documents(.doc and .pdf). After downloading them into separate folders, I use the terminal to batch convert the files into plain text files. Then using python, I call these files back in to make a list of dictionaries consisting of at least the 'filename' and 'text'. Then I export them as .csv files. Finally, using R, I merge datasets together and perform text-analysis. The final visual results are graphs and word clouds of frequently used words. 

## Dependencies

1. R, version 3.1
2. Python 2.7, Anaconda distribution.

### Data

1. allsermons.csv: Merged product of sermonsfull.csv and sermontexts.csv
2. edmondsermons.csv: Data consisting of 'filename' and 'text' for each sermon from Edmonds church.
3. Pasadenasermontexts.csv: Data consisting of 'filename' and 'text' for each sermon from Pasadena church.
4. sermonsfull.csv: Data web scraped from Chinese church, consisting of "date","preacher","scripture","title" and "filename".
5. sermontexts.csv: Data consisting of 'filename' and 'text' for each sermon from Chinese church. 
6. Edmond (folder): all raw pdf files and converted plain text files of each sermon from Edmonds church.
7. rawdata (folder): all raw .doc files and converted plain text files of each sermon from Chinese church.
8. rawdataEng (folder): all raw .pdf files and converted plain text files of each sermon from Pasadena church. 


### Code

1. 01_Webscraping_Table_ChineseChurch.ipynb: Collects data from the Chinese sermon page and exports data to the file sermonsfull.csv
2. 02_Downloading_Docs_from_Webpage.ipynb: Collects all links to document files and downloads each document to a local folder.
3. 03_Creating_CSV_of_Texts.ipynb: Creates a csv file consisting of 'filename' and 'text' from the documents in a local folder that are converted to plain text files. The resulting file is 'sermontexts.csv'
4. 04_Merging_Datasets.Rmd: Merges the two .csv files from 01 and 03 above. 
5. 05_Downloading PDFs_from_Webpage_(Pasadena).ipynb: Same as 02 above, but downloading .pdf files from an American church webpage. 
6. 06_Downloading PDFs_from_Webpage_(Pasadena)-2.ipynb: Same as 05, but repeated to get more sermons. Then 03 is used to create Pasadenasermontexts.csv.
7. 07_Downloading PDFs_from_Webpage_(Edmonds).ipynb: Same as 05 and 06, but repeated to get .pdf sermons from Edmonds church. Produces "edmondsermons.csv".
8. 08_Text_Analysis.Rmd: Performs text analysis on allsermons.csv (Chinese sermons) and edmondsermons.csv (Edmonds sermons).

### Results

1. mostfreqwords.jpeg: creates a bar graph of frequency of words.
2. WC-Chinafreq.jpeg: creates a word cloud with most frequently used words from Chinese sermons.
3. WC-EdmondFreq.jpeg: creates a word cloud with most frequently used words from Edmonds sermons.

## More Information

I have webscraped and cleaned the Pasadena files, but have not included the text analysis done on this set of sermons. Instead, I only included the text analysis comparing Chinese sermons with Edmonds sermons. I also have created, but not included a dataset of translated Chinese sermons, and I also performed text analysis to compare with Edmonds sermons. Contact me for more information. 

Sarah Lee
Ph.D Student, UC Berkeley
lee.sarah@berkeley.edu
