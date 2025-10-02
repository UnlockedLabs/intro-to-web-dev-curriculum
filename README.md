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

## Resources

We added two new resources to the resource directory: www.nytimes.com and HTML5NotesForProfessionals_entities.pdf.

We reused www.nytimes.com/index.html. The page that contains the link to it is http://localhost:1313/html/studio/.

HTML5NotesForProfessionals_entities.pdf is linked to on page http://localhost:1313/assignments/html-me-something/part-1/.  We could not find any entities in the zims.  There may be a better resource to use for this page. 

We linked the 7_LPdttKXPc.webm and OvF_pnJ6zrY.webm videos. However, they seem to be the same video.

## links, servers, and ports

The following links require running servers.  Please note the port numbers.

* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/7_LPdttKXPc.webm
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/ASCII%20table.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/HTML5NotesForProfessionals_entities.pdf
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/OvF_pnJ6zrY.webm
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/Scope%20and%20Closures%20in%20JavaScript.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/StackOverflow%20Survey%202025.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/Substack%20-%20First%20Computer%20Bug.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/Wikipedia%20-%20HTTPS.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/Wikipedia%20-%20Voyager%20program.html
* http://education.launchcode.org/resources/intro-to-web-dev-curriculum/www.nytimes.com/index.html
* http://handlers.education.launchcode.org/static/planets.json
* http://handlers.education.launchcode.org/static/weather.json
* http://localhost:8081/devdocs_en_css_2025-01/class_selectors
* http://localhost:8081/devdocs_en_css_2025-01/css_logical_properties_and_values/margins_borders_padding#margin_examples
* http://localhost:8081/devdocs_en_css_2025-01/css_logical_properties_and_values/margins_borders_padding#padding_examples
* http://localhost:8081/devdocs_en_css_2025-01/id_selectors
* http://localhost:8081/devdocs_en_css_2025-01/index
* http://localhost:8081/devdocs_en_css_2025-01/specificity
* http://localhost:8081/devdocs_en_css_2025-01/type_selectors
* http://localhost:8081/devdocs_en_dom_2025-01/document_object_model
* http://localhost:8081/devdocs_en_dom_2025-01/html_dom_api
* http://localhost:8081/devdocs_en_dom_2025-01/response
* http://localhost:8081/devdocs_en_dom_2025-01/window/alert
* http://localhost:8081/devdocs_en_dom_2025-01/window/load_event
* http://localhost:8081/devdocs_en_git_2025-07/index
* http://localhost:8081/devdocs_en_html_2025-01/element/form
* http://localhost:8081/devdocs_en_html_2025-01/index
* http://localhost:8081/devdocs_en_javascript_2025-01/classes
* http://localhost:8081/devdocs_en_javascript_2025-01/functions/arguments
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/array#array_methods_and_empty_slots
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/error
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/json
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/math
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/object
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/referenceerror
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/set
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/string/length#description
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/string/replace
* http://localhost:8081/devdocs_en_javascript_2025-01/global_objects/string#instance_methods
* http://localhost:8081/devdocs_en_javascript_2025-01/index
* http://localhost:8081/devdocs_en_javascript_2025-01/lexical_grammar#keywords
* http://localhost:8081/devdocs_en_javascript_2025-01/operators/bitwise_and
* http://localhost:8081/devdocs_en_javascript_2025-01/operators/bitwise_or
* http://localhost:8081/devdocs_en_javascript_2025-01/operators/equality
* http://localhost:8081/devdocs_en_javascript_2025-01/operators/operator_precedence#table
* http://localhost:8081/devdocs_en_javascript_2025-01/operators/spread_syntax
* http://localhost:8081/devdocs_en_javascript_2025-01/statements/for#see_also
* http://localhost:8081/devdocs_en_javascript_2025-01/statements/try...catch
* http://localhost:8081/devdocs_en_jest_2025-01/index
* http://localhost:8081/devdocs_en_jest_2025-01/using-matchers
* http://localhost:8081/devdocs_en_mariadb_2025-01/index
* http://localhost:8081/devdocs_en_react_2025-01/index
* http://localhost:8081/devdocs_en_react_2025-01/learn/javascript-in-jsx-with-curly-braces
* http://localhost:8081/devdocs_en_react_2025-01/learn/passing-props-to-a-component
* http://localhost:8081/devdocs_en_react_2025-01/learn/responding-to-events
* http://localhost:8081/devdocs_en_react_2025-01/reference/react/fragment#usage
* http://localhost:8081/devdocs_en_vite_2025-01/index
* http://localhost:8081/devdocs_en_vitest_2025-01/index

## gitweb

assumes gitweb lives at http://localhost/git/

## lively_links

This is a python script that walks through the curriculum while being served by hugo.  As it walks, it checks each url for a status code of 200. If the code is not 200, then the failed url is written to the missing_links.csv file. We are running hugo at http://localhost:1313/. Please note line 27 in run.py.  This script takes about 5 minutes to complete on the securebooks.