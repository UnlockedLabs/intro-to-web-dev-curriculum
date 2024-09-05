---
title: "trim Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 4
originalAuthor: Christian Frauenhoffer # to be set by page creator
originalAuthorGitHub: johncfrauen-lc101 # to be set by page creator
reviewer: # update any time edits are made after review
reviewerGitHub: # update any time edits are made after review
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---


The general syntax for this method is:

```console
   stringName.trim();
```

This method returns a copy of the string with any leading or trailing whitespace removed. Whitespace characters are those that do not display anything on the screen, such as spaces and tabs.

{{% notice blue "Example" "rocket" %}}

 ```js {linenos=table}
	console.log("Saint Louis ".trim());
	console.log(" Saint Louis".trim());
	console.log(" Saint Louis ".trim());
```

**Console Output**

```console
	Saint Louis
	Saint Louis
	Saint Louis
```
{{% /notice %}}

{{% notice blue "Example" "rocket" %}}
When typing an email address into a web site, a user may inadvertently type a space before and/or after the email address. We can clean up such input using the `trim` method.

This example cleans up user input with `trim`.

 ```js {linenos=table}
	let input = " fake.email@launchcode.org ";
	let email = input.trim();
	console.log(email);
```

**Console Output**

```console
	fake.email@launchcode.org
```
{{% /notice %}}