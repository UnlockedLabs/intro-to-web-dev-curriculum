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



<!--

Brandon: here is the format for the link to this Create a React Application section. I did not make any changes to the Create a React Application located at http://localhost:1313/react-lsn1/reading/setup/

[(Offline Student Read Here)]({{% relref "../../../content/appendices/offline-students/_index.md#create-a-react-application" %}})
-->
