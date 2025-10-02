## Any major concerns we need to address:

* React repo "react-exercises-and-studios" needed some work for offline use. Many of the React apps would not start because they were missing certain node modules. I (Brandon) cut an "offline" branch and added multiple Vite React apps, node modules, and changed JSON data throughout to work offline:
  * Part 1 Reading First React App, added Vite React app "/part1/react-part-one"
  * Part 1 Studio "/part1/studio"
  * Part 2 Exercise oceans.json image urls (I added these images to the handlers.education.launchcode.org flask server)
  * Part 2 Studio recipe.json image urls (I added these images to the handlers.education.launchcode.org flask server)
  * Part 3 Reading, added Vite React app
  * Part 3 Exercise, added Vite React app and updated data.json for offline
  * Part 3 Studio, added Vite React app and startcode files

* I (Brandon) added images to the handlers.education.launchcode.org flask server, in the static/images directory. These are required for all three React chapters.

* Chapter 30 > Studio > Part 3: Add the Recipe > Ingredients Lists - I (Brandon) did not have the solutions branch for refrence so I wasn't sure how to proceed here. The chapter reading did not explicitly cover accessing an array within a JSON object and the studio instructions were not very clear on the steps to complete what is being asked. I came up with a simple solution and changed the instructions to better explain. If there is a better solution we can change again. Here's my code:

<!-- 
function IngredientList() {
  return (
    <div>
      <h3>Ingredients</h3>
      <ul>
        {recipedata.map((data) => {
          return data.ingredients.map((item, index) => <li key={index}>{item}</li>);
        })}
      </ul>
    </div>
  );
}
 -->
 
__handlers.education.launchcode.org__ We might be able to use the current apache server to accomplish what the Flask app is doing.  Please see http://education.launchcode.org/request-parrot.php in the current image as an example.

* Chapter 1: Introduction > Reading > Class Platforms:
  * The way in which Canvas is referenced for use is not the way we use our little module. Our module is only used for a rough calendar, submitting Assignments, and the Gradebook for rubrics and grading. We would love to import the Canvas module being referenced in the curriculum and begin to use it.


## List of additional http links found within the course that should be downloaded and included:
* Refer to broken_links.ods
* For multiple page web site scrapes, how should we package the site for reference (hlink)? As an http site, or a raw file path? And where in the file structure should it/they put located?



## List of other software modifications like missing npm packages for certain gitweb projects, etc:

* Will you __please__ include the solutions for exercises, studios, assignments, etc for intro-to-web-dev-curriculum and Java Web Development? The TAs would like to have access to them. Thank you.

* Please include Rect Dev Tools and React VSCode extensions in the finished image



## List of changes to the below Test/Validation list to remove outdated content and test this course properly:

* __Test Wolf Checker__ Wolf Checker may need to be removed as it was written for the previous intro-to-web-dev-curriculum. Note: this note is coming from the guy to who wrote wolf-checker-js. :-O

* __Jasmine Tests__ update to Jest.

* __Angular__ remove.

* __Test Scratch__ remove for Intro to Professional Web Dev NOT for Think Python.

* __Launchcode http://education.launchcode.org there should be 5 blue and white tiles users can select from__ the number 5 might change based upon updates.