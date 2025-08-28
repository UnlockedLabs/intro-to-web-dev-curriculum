## Any major concerns we need to address:



## List of additional http links found within the course that should be downloaded and included:



## List of other software modifications like missing npm packages for certain gitweb projects, etc:

* Will you __please__ include the solutions for exercises, studios, assignments, etc for intro-to-web-dev-curriculum and Java Web Development? The TAs would like to have access to them. Thank you.



## List of changes to the below Test/Validation list to remove outdated content and test this course properly:

* __Test Wolf Checker__ Wolf Checker may need to be removed as it was written for the previous intro-to-web-dev-curriculum. Note: this note is coming from the guy to who wolf-checker-js. :-O

* __Jasmine Tests__ update to Jest.

* __Angular__ remove.

* __Test Scratch__ remove for Intro to Professional Web Dev NOT for Think Python.

* __Launchcode http://education.launchcode.org there should be 5 blue and white tiles users can select from__ the number 5 might change based upon updates.



## How to convert intro-to-web-dev-curriculum to a static site:

We found a way to convert a running hugo server into a static html site using wget.  Please note that there may be a way to do this with a hugo command (maybe?).

Steps:

* Start hugo server.
* Open terminal.
* Enter:
* wget --restrict-file-names=windows -p -m  -k -P ./mirror http://localhost:1313/
* Change port 1313 if hugo is running on a different port.
* Wait for wget to finish.
* Open the mirror directory.
* Rename localhost:1313 to a directory name of your choosing. 
* Drop the new directory onto apache server.
* Open browser and enter url path to site.

