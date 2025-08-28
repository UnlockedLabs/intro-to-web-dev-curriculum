## Any major concerns we need to address



## List of additional http links found within the course that should be downloaded and included



## List of other software modifications like missing npm packages for certain gitweb projects, etc

* Will you __please__ include the solutions for exercises, studios, assignments, etc for intro-to-web-dev-curriculum and Java Web Development? The TAs would like to have access to them. Thank you.



## List of changes to the below Test/Validation list to remove outdated content and test this course properly

* Intro to Web Development >Code Checker (wolf-checker-js) may need to be removed as it was written for the prvious intro-to-web-dev-curriculum. Note: this note is coming from the guy to who wolf-checker-js. :-O



## How to convert intro-to-web-dev-curriculum to a static site.

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

