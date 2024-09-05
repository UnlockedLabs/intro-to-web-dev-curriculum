---
title: "toLowerCase Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 2
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
   stringName.toLowerCase();
```

This method returns a copy of `stringName` with all uppercase letters replaced by their lowercase counterparts. It leaves non-alphabetic characters unchanged.

```console
   "LaunchCode".toLowerCase();
```

**Console Output**

```console
	launchcode
```

{{% notice blue "Example" "rocket" %}}
The domain portion of an email address (the portion after the `@` symbol) is case-insensitive. Emails with domain `launchcode.org are the same as those with domain `LAUNCHCODE.ORG`. By convention, the all-lowercase version is typically used by an application.

This program standardizes an email address by converting it to all lowercase characters.

 ```js {linenos=table}
	let input = "fake.email@LAUNCHCODE.ORG";
	
	let email = input.toLowerCase();
	
	console.log(email);
```

**Console Output**

```console
	fake.email@launchcode.org
```

{{% /notice %}}

{{% notice orange "Warning" "rocket" %}} 
This example is a bit crude, since the portion of an email address before the `@` symbol is allowed to be case-sensitive. When standardizing the case of an email in a real application, we would want to be more precise and only convert the domain portion to lowercase characters.

{{% /notice %}}