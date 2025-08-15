---
title: "Create a React Application"
date: 2023-03-31T09:42:17-05:00
draft: false
weight: 3
originalAuthor: Sally Steuterman # to be set by page creator
originalAuthorGitHub: gildedgardenia # to be set by page creator
reviewer: Rob Thomas
reviewerGitHub: icre8FreeCode
lastEditor: John Woolbright # update any time edits are made after review
lastEditorGitHub: jwoolbright23 # update any time edits are made after review
lastMod: 10-17-2023 # UPDATE ANY TIME CHANGES ARE MADE
---

Now that we understand more about React and components, we are ready to build a React app. To make a new React application, we will be using a front-end tool called [Vite](https://vitejs.dev/). This will allow us to scaffold a new `React` project with the required dependencies and launch a local dev server.

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