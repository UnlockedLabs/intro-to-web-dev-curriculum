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

<!--

Brandon: here is the format for the link to this Create a React Application section. I did not make any changes to the Create a React Application located at http://localhost:1313/react-lsn1/reading/setup/

[(Offline Student Read Here)]({{% relref "../../../content/appendices/offline-students/_index.md#create-a-react-application" %}})
-->
