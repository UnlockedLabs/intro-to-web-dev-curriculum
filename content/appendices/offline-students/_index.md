---
title: "Offline Students"
date: 2021-10-01T09:28:27-05:00
weight: 10
draft:
originalAuthors: Brandon Milburn, DeAndre Roddy, William Thimiogianis, Joshua Wolf
originalAuthorGitHub: # to be set by page creator
reviewer: # update any time edits are made after review
reviewerGitHub: # update any time edits are made after review
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---

There are sections in this curriculum that require you to have access to the internet which you don't have as an offline student. We didn't want to remove these sections because they illustrate how developers set up their programming environments with the internet. This page seeks to explain how the online curriculum was converted to run offline.

## npm install

If you are working as an offline student, you do not need to run the `npm install` or `npm i` command (it won't work even if you try). Since you do not have access to the internet, an online developer ran the `npm install` command for you and included the downloaded modules for you to use.

<!--
Brandon, Drey, Bill: here is the format for the link to this npm install section

[(Offline Student Read Here)]({{% relref "../../../content/appendices/offline-students/_index.md#npm-install" %}})

-->

## Chapter 25 Studio: HTTP and Forms

As an offline student, you may have never used a search engine before. Whether you have or haven't, its important to know that most search engines work the same way. They have a single text input, and they submit data using a `GET` request. Additionally, many of the most popular search engines also use the same name for the search parameter, `q`.

{{% notice blue "Try It!" "rocket" %}}
Unfortunately, as an offline student you cannot use a real-world search engine. However, you *can* understand how they work.
Open a new tab in your browser and type this into the URL: `http://handlers.education.launchcode.org/request-parrot?q=your+search+term+here`

Use 2-3 different search terms to get an idea of what is happening.

As you have probably gathered, a `GET` request was made containing the name of the parameter `q` and your search term.
{{% /notice %}}

{{% notice blue Note "rocket" %}}
We remarked previously that most forms use `POST` because they cause data to be changed on the server. A web search only *retrieves* data. It does not change data. Therefore it's safe to use a `GET` request for searches.
{{% /notice %}} 

The fact that most search engines use the name `q` for their search boxes
will allow us to easily create a form that is capable of sending a search
request to several search engine URLs, even though we can't access the results.
We can, however, observe the URL in the browser and verify that our search engine selector is working properly.

[(Back to the Studio)]({{% relref "../../../content/user-input-with-forms/studio/_index.md#getting-started" %}})


## Chapter 28 Reading: Create a React Application

Since you are in an offline environment, we took the liberty of using Vite to set up your React applications for you.
To access them, you will need a copy of the LaunchCode React projects repository.

1. Clone the *react-exercises-and-studios repository* from your local server.
1. Switch to the *offline* branch.
1. Navigate into the *react-part-one* root directory:

```console
   $ pwd
      react-exercises-and-studios
   $ ls
      part1 part2 part3
   $ cd part1
   $ cd react-part-one
```

Now that you are in your project's root directory, run the following command:

```bash
npm run dev
```

This will start your local development server and you will see output similar to the below image:

![Image of running application on localhost:5173 after executing the npm run dev command](pictures/npm-run-dev.png?classes=border)

You can view some useful Shortcuts if you press `h`

![Image of Shortcuts after pressing h which is available after executing the npm run dev command](pictures/help-command.png?classes=border)

At this point you can either open a web browser and navigate to `http://localhost:5173` or press `o` if you are within the terminal window running the application.

![Image of running react application scaffolded with Vite](pictures/running-react-application.png?classes=border)

{{% notice blue Note "rocket" %}}
You do not need to press `h` in order for the shortcuts to work. Once the app is running you can press `o` to view the application within the browser (if you are currently within the terminal window running the application).
{{% /notice %}}

[Continue Chapter 29 Reading]({{% relref "../../../content/react-lsn1/reading/more-on-vite/index.md" %}})

## Chapter 29 Exercise: Chores vs. Hobbies

### Complete the `BookList` Component

1. In the `BookList` function, assign a better section heading to the `pageTitle` variable.
   1. The `book` variables should hold URLs for images, but only one is is filled in and it isn't a valid link. 
   Update the three variables to include valid link addresses for three new book releases. Since you're offline,
   we've provided a few book covers for you to choose from. Here's the URL to use: `http://handlers.education.launchcode.org/static/images/books/Title_of_Book.png`

   ![Image of various book covers for use in ch29 exercise](pictures/ch29-exercise-books.png?classes=border)

   2. In the `return` statement for this component, use JSX in the `img`
      tags to display your chosen images and update the `alt` text to reflect what book you are linking.

      ```jsx
         <img src={book1} alt="Appropriate text for the book">
      ```

   1. Refresh the webpage to check the updated content.

   {{% expand "Check Your Solution" %}}
   
   This solution includes three books from the latest releases the week we were working on this book. Your code will have different books!

   ```jsx
   <div>
   <h3>{pageTitle}</h3>
   <img src={book1} alt="Romantic Comedy by Curtis Sittenfield" />
   <img src={book2} alt="Tress of the Emerald Sea by Brandon Sanderson" />
   <img src={book3} alt="The London Seance Society by Sarah Penner" />
   </div>
   ```

   {{% /expand %}}

Before moving on, save and commit your work.


[Back to the Exercise]({{% relref "../../../content/react-lsn1/exercises/_index.md#part-2-add-another-component" %}})


## Chapter 29 Studio: A Few of Your Favorite Recipes

Before you start coding, check out this image of a few popular foods you may enjoy. Go ahead and pick something sweet or savory and jot down the image filename and five of the food's main ingredients. It's time to make a recipe!

![Image of sample food pics](pictures/ch29-studio-foods.png?classes=border)

### Setting Up Your App

To get started coding, you need to first create an application. Don't worry, we've covered that for you.

1. Open the *react-exercises-and-studios* repository in VSCode.
1. Make sure you are working in the *offline* branch.
1. In your terminal, navigate into the *studio* directory and run `npm run dev`.

Great! You're all set up.

### The Components

First create inside `src`, a folder called `components`. Now tackle creating the components one-by-one.

#### The `RecipeDescription` Component

1. Inside the `components` directory, make a new file called `Description.jsx`.
1. Create a new function called `RecipeAuthor()`. For now, this function may not work as expected, but we have more work to do! Since we can't use our own pictures, here's a few personas for you to choose from.

![Image of sample author pics](pictures/ch29-studio-personas.png?classes=border)

Once you know the number of the persona you want to be, make sure your function meets the following requirements:

1.  Have no parameters.
   1. Have three local variables: `authorLink`, `authorPhoto`, and `authorName`.
   1. `authorLink` should contain a link. Since we're offline, why not use `http://education.launchcode.org`?
   1. `authorPhoto` should include a URL pointing to a photo of the author. In our case, we'll use `http://handlers.education.launchcode.org/static/images/authors/02.png`. Be sure to plug in the number of the persona you chose above.
   1. `authorName` should contain the author's full name. Use your creative juices and make one up.
   1. Return something similar to the following:

```jsx
return (
  <div className={styles.recipeAuthorBlock}>
    <img src={authorPhoto} alt="A headshot of the author" className={styles.imageUpdates} />
    <div>
      <h3>{authorName}</h3>
      <a href={authorLink}>Foodie Blog</a>
    </div>
  </div>
);
```

1. Create a new file in the `components` directory called `Description.module.css` and add the following CSS to this file.

    ```css
    .recipeAuthorBlock {
        display: flex;
        justify-content: space-evenly;
    }

    .imageUpdates {
        width: 100px;
        border-radius: 50%;
    }

    .recipePhoto{
         width: 200px;
          border-radius: 20px;
    }
    ```

1. Return to `Description.jsx` and add this `import` statement: `import styles from './Description.module.css;`.
1. Add one more `import` statement: `import React from 'react';`
1. Add a class called `RecipeDescription` which extends `React.Component`. This class should have only a `render()` method which returns something similar to the following JSX:

   ```html
    <div>
      <div>
        <h1>Paradise Brownies</h1>
        <p>Whip up the most magical brownies west of the Mississippi!</p>
      </div>
      <RecipeAuthor />
    </div>
   ```

1. At the bottom of `Description.jsx`, add `export default RecipeDescription;`.
1. Head over to the `App.jsx` file within the root directory and replace what is inside with the following code:

   ```jsx
   import { useState } from "react";
   import "./App.css";

   function App() {
     return (
       <>
         <div className="App"></div>
       </>
     );
   }

   export default App;
   ```

1. Add a second `<div>` and inside that add `<RecipeDescription />` to call your new component. Add any necessary `import` statements. It should now look something like:

   ```jsx
   <div className="App">
     <div>
       <RecipeDescription />
     </div>
   </div>
   ```

1. Run your application! You should have a simple page that just includes your `RecipeDescription` component.

#### The `RecipeIngredients` Component

1. Inside your `components` directory, create a new file called `Ingredients.jsx`.
1. Inside this file, add a new function called `RecipeIngredients()`. This function should include the following:

   1. An array containing the top 5 ingredients of your recipe.
   1. Return something similar to the following JSX:

   ```jsx
   <div>
     <h3>Recipe Ingredients</h3>
     <ul className={styles.ingredientList}>
       <li>{ingredients[0]}</li>
       <li>{ingredients[1]}</li>
       <li>{ingredients[2]}</li>
       <li>{ingredients[3]}</li>
       <li>{ingredients[4]}</li>
     </ul>
   </div>
   ```

1. Now create a new file in the `components` directory called `Ingredients.module.css`.
1. Add the following CSS to this new file:

   ```css
   .ingredientList {
     text-align: left;
   }
   ```

1. Return to `Ingredients.jsx` and add the following `import` statement: `import styles from './Ingredients.module.css';`.
1. If you didn't before, add `export default` in front of your `RecipeIngredients()` function declaration.
1. Head over to `App.jsx`.
1. Right below `<RecipeDescription />`, add `<RecipeIngredients />` and the necessary `import` statement.
1. Run your application! You should now see a list of ingredients below your recipe description.

#### The `RecipePhoto` Component

1. Create a new file in `components` called `Photos.jsx`.
1. Add a new function called `RecipePhoto()`. Remember the image filename you chose at the beginning of this studio? Use it within the correct URL to write something similar to the following JSX.

   ```jsx
   <img src="http://handlers.education.launchcode.org/static/images/food/brownie.png" alt="brownie recipe photo" className={styles.recipePhoto} />
   ```

1. Add the following `import` statement to the top of your file: `import styles from './Description.module.css';`.
1. If you haven't already, add `export default` to your function declaraction.
1. Head over to `App.jsx` and import the `RecipePhoto` component.
1. You will add `<RecipePhoto />` above the inner `<div>`, but inside `<div className="App">`. It should look like the following:

   ```jsx
   <div className="App">
     <RecipePhoto />
     <div>
       <RecipeDescription />
       <RecipeIngredients />
     </div>
   </div>
   ```

1. Now run your application, et bon appétit!

[Continue to Next Steps]({{% relref "../../../content/react-lsn1/next-steps.md" %}})

<!--

Brandon: here is the format for the link to this Create a React Application section. I did not make any changes to the Create a React Application located at http://localhost:1313/react-lsn1/reading/setup/

[(Offline Student Read Here)]({{% relref "../../../content/appendices/offline-students/_index.md#create-a-react-application" %}})
-->
