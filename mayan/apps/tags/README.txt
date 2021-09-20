README

We have implemented a basic pane for reviewer dashboard and management using Mayan EDMS.
On the Mayan website, under tags, you can choose among available tags (reviewers) which 
ones to assign to each document you upload.


The code for our feature can be found in mayan/apps/tags/apps.py 

For now we have hard-coded the list of users in a list - to add new users
simply add their names to the list "user". 
After making the changes, run "make docker-build" and you should be able to see the changes.


We hope to soon extend the feature to pulling user information from a database. 

