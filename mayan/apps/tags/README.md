**Brief Overview of Repository:**  
This repository module adds a method for reviewer assignment and management integrated with the Mayan EDMS software. This new feature makes use of Mayan’s existing tags implementation to allow for an automated and more efficient way to assign multiple reviewers to documents, view the assigned reviewers to a specific document, view the assigned documents to a specific reviewer and search through documents by reviewers. This is done through automating batch tag creation from the backend, where tags are automatically created in one batch for each reviewer in the reviewers list specified by the admin user in the code. This feature is meant for the use of managers and admins for reviewer management, but can also be used by regular users for faster batch tag creation.

**How to Use the Feature:**
1. Fork the Github repository
2. Navigate to the “apps.py” file under the directory “mayan/apps/tags”
3. Locate the list named “reviewers_list” inside the ready function 
4. Edit the list to include the tag labels as strings (i.e. the reviewer names) that you would like to add from the backend
5. Once you start up Mayan again, your new tags should be reflected on the webpage.
  
**Quality Assurance Measures:**
  - Check that all the added reviewers to the tags table in the database are displayed on Mayan website under “Tags” in the home page and on the tags webpage.
  - Check that all Tags functionalities are still operational, that is, the user can add, edit and delete tags, search for tags, assign tags to documents 
  - Check that there are no duplicate tags created . This is to avoid database table unique constraint conflicts.
  - Check that the modified software does not cause a drop in Lighthouse scores, especially the Accessibility and Performance scores. 
  - Check that the modified software passes all of Mayan’s pre-existing test cases in the “test.py” file under the “mayan/apps/tags” directory
