
For this assignment, you will need to download two CSV files from the following links: 

Page Loads: https://storage.googleapis.com/aller-structure-task/page_loads.csv 
Clicks: https://storage.googleapis.com/aller-structure-task/clicks.csv 

The **page loads file** contains one row for each page visit we received on the 29th of January. The following fields are included: 

**UserID:** An ID to uniquely identify a visitor. 

**PageView:** An ID to uniquely identify the page visit. A new PageView is created every time a user refreshes a page. 

**Site:** The name of the site the page visit occurred on. 

**Device:** The device the visitor was using (desktop, mobile, tablet, etc). 

**HarvesterID:** An ID to uniquely identify the page visited. For example, the Dagbladet front page has the HarvesterID “www.dagbladet.no”. 

**Date:** The date and time when the user visited the page. 

The **clicks file** contains one row for each click that occurred on one of our pages on the 29th of January. The following fields are included: 

**PageView:** An ID to uniquely identify the page visit that the click occurred on. This can be used to join the clicks data with the page loads data, e.g. to find which page a click occurred on. 

**Date:** The date and time when the user clicked the link. 

**HarvesterID:** An ID to uniquely identify the page the user clicked on. 
To provide an example, say you find the following data: 

1. The page loads file contains a row with the PageView of “12345”, UserID of “ABCDE”, HarvesterID of “dagbladet.no/7654321”, and Date of “2020-01-29 10:00:00”. 2. The clicks file contains a row with the PageView of “12345”, HarvesterID of “dagbladet.no/8756593”, and Date of “2020-01-29 10:10:00”. 
This would mean that user “ABCDE” visited the page “dagbladet.no/7654321” at “2020-01-29 10:00:00”, and then from that page clicked on a link to “dagbladet.no/8756593” ten minutes later. 

**Questions** 

Using either Python or SQL (or a combination of the two), please provide code that answers the following questions: 
1If you provide SQL, it is fine to pretend the CSV files are tables in a relational database. That is, there is no need to actually provide code for loading the CSV into tables.
1. How many page loads did the Dagbladet front page receive on January 29th on desktop? (Note: The Dagbladet front page has the HarvesterID “www.dagbladet.no”) 
2. How many unique users (distinct UserIDs) visited the Dagbladet front page on January 29th between 10am and 11am (UTC time)? 
3. What page received the most clicks from the KK front page on January 29th on mobile? (Note: The KK front page has the HarvesterID “www.kk.no”) 
4. What percentage of pageviews on the Dagbladet front page on January 29th resulted in at least one click? 
5. A “session” begins when a user visits a page more than one hour after his or her last page load in a given day. How many unique users had more than one session on Dagbladet on January 29th?
