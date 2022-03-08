# ChangeManagementAutomation

This is private project developed at my time at BLK.
While details cannot be disclosed, a very high level decription would suffice.

###Motiviation###
Every weekend, our team is involved with multiple other Operation teams at BLK, to conduct housekeeping changes such as netowrk and switch upgrades, Windows and Unix servers patches,
DR tests, site powerdowns, etc.
The job of curating all changes that our team is involved in, assigning resources to assist with completion of these changes, troubleshoot when necessary and monitor changes by external groups that might involve our systems is part our BAU responsibilities.
Every Tuesday and Wednesday, our team needs to obtain a list of such changes (both, internal and external) after fitlering out changes that could potentially affect our systems and servers, and assign resources. 
Keyword based filtering frequently need be ammended as well, as infrastructure changes happen frequently.

###Process###
This project automates this report generation process by presenting an intuitive UI driven GUI, spun up using HTML and Boostrap CSS.
The backend is written in Python-Flask, that scrapes our internal website to download the report of all changes within the firm, and then filter out changes on the basis of a stored list of keywords.
All changes are split into historical and future changes to allow for easy lookup of previous changes (for a period of two weeks) and keywords are highlighted on each change row.
Selenium webdriver is used to scrape our intranet for real time updated Javascript tables while the Openpyxl library is used to interface between Excel and Python. 
A separate tab on the GUI also allows for easy addition/deletion of filter-keywords.

###Results###
This effort has already saved the team up 8-9 hours of weekly manual labor involved in downloading, curating and having the report made avaialbe to the team.
Owing to the success of this project, this is now being utilized by other Operations teams at BLK. 

###Future###
Looking ahead, more features of this project will be made available online - viewing and editing the report being the most important one.
Complex combination of keywords And/Or other keywords will be allowed to be compiled and stored for filtering.
Using APIs, a copy of the report will also be made available to the concerned Microsoft Teams channel and as an Outlook email item.
