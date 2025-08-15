---
title: "Studio: A Few of Your Favorite Recipes"
date: 2023-03-31T09:42:17-05:00
draft: false
weight: 3
originalAuthor: Sally Steuterman # to be set by page creator
originalAuthorGitHub: gildedgardenia # to be set by page creator
reviewer: Rob Thomas 
reviewerGitHub: icre8FreeCode 
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---

One reason we are learning React is because many top tech companies use it, including Pinterest. On Pinterest, we can create boards and save pins of new recipes, wedding decor concepts, and tips and tricks for crafts. When one clicks on the pin, they are taken to a detailed view which includes a photo, a description of the pin, and in the case of recipes, ingredients one needs for that recipe. Today, we are going to try our own take on this page using React and what we have learned about components. 

[(Offline Student Read Here)]({{% relref "../../../content/appendices/offline-students/_index.md#chapter-29-studio-a-few-of-your-favorite-recipes" %}})

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