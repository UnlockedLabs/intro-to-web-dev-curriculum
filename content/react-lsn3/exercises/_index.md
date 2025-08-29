---
title: "Exercises"
date: 2023-04-12T16:25:46-05:00
draft: false
weight: 2
originalAuthor: Sally Steuterman # to be set by page creator
originalAuthorGitHub: gildedgardenia # to be set by page creator
reviewer: Rob Thomas 
reviewerGitHub: icre8FreeCode 
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---

Time to make a React app to share a hobby you love (or pretend like you love) with your friends and family!

1. We've created a new application called `exercises` in the `part3` directory of the *react-exercises-and-studios* repo. cd into it and run `npm run dev`
1. In `App.jsx`, remove the boilerplate content as you have done in previous lessons. Replace it with an `<h1>` heading that says "My Hobby: " with your temporary favorite hobby (needlepoint!) coming after the colon.

   {{% expand "Check Your Solution" %}}
   ```jsx
   <div className="App">
      <h1>My Hobby: Needlepoint</h1>
   </div>
   ```
   {{% /expand %}}

1. Create a new `components` directory in `src`.
1. Create a new file called `Introduction.jsx` in `components` and inside create a new functional component called `HobbyIntroduction`.

   {{% expand "Check Your Solution" %}}
   ```jsx
   export default function HobbyIntroduction () {
      return();
   }
   ```
   {{% /expand %}}

1. This functional component return a `<div>` that contains the following:

   1. An `<h2>` heading that says something to the effect of "3 Fun Facts About Needlepoint".
   1. An ordered list that contains three facts that you want others to know about needlepoint. Here's a few:
      * Needlepoint uses a specialized canvas as it's base.
      * The most basic stitch is called a tent stitch.
      * Needlepoint uses a lot of different kinds of fibers.

1. Import and Call the new `HobbyIntroduction` component under your `<h1>` heading in `App.jsx`.

   {{% expand "Check Your Solution" %}}
   ```jsx
   <div className="App">
      <h1>My Hobby: Needlepoint</h1>
      <HobbyIntroduction />
   </div>
   ```
   {{% /expand %}}

1. Run the application to see your new fun facts! Once you are satisfied, turn off the server so we can practice with state.
1. Inside `src`, we've added a file called `data.json`. We are going to use this file to make a small gallery of images of projects or plans you have needlpoint. Inside this file, you will see a list of JSON objects called `projects`. Your list should contain 4 JSON objects and each one should have 4 properties.

   {{% expand "Check Your Solution" %}}
   Here is a shortened example of what an object looks like for our app about needlepoint.

   ```json
   {
      "canvas": "Fox",
      "designer": "Pip and Roo",
      "photoUrl": "long URL",
      "alt": "Stitched fox with fluffy tail"
   }
   ```
   {{% /expand %}}

1. Create a new file called `Projects.jsx` in `components`. This file will hold a functional component called `MyProjects`.
1. Import the data from `data.json` and `useState` from `'react'` at the top of `Projects.jsx`.

   {{% expand "Check Your Solution" %}}
   ```jsx
   import data from './../data.json';
   import { useState } from 'react';
   ```
   {{% /expand %}}

1. Inside the `MyProjects` component, start by setting up a state variable for the index so we can loop through our list of projects. You can do this with the following code: `const [index, setIndex] = useState(0);`.
1. Now we need to set up some local variables and a return statement. 

   1. First, set up a JavaScript variable that contains your list from `data.json`. Then set up a variable that contains the item in that list at the position determined by `index`.
   1. Inside `return`, set up a button that contains the text, "Next". Set the `onClick` attribute to `{handleClick}`. 
   1. Below your button, add HTML that will nicely display all four properties of your JSON objects.
   {{% expand "Check Your Solution" %}}
   ```jsx
  let projects = data.projects;
  let project = projects[index];

  return (
    <div>
      <button onClick={handleClick}>
        Next
      </button>
      <h2>{project.canvas} by {project.designer}
      </h2>
      <img src={project.photoUrl} alt={project.alt} />
    </div>
  );
   ```
   {{% /expand %}}
1. Finally, above the return statement, we need to set up `handleClick()` like so:

   ```jsx 
   function handleClick() {
      if (index < data.projects.length-1)
      {
         setIndex(index + 1);
      }
      else 
      {
         setIndex(0);
      }
   }
   ```

1. Return to `App.jsx` and call the completed `MyProjects` component below `HobbyIntroduction`. Run the application to see your new gallery! Hit the *Next* button to see state in action!
