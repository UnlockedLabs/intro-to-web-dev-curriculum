---
title: "indexOf Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 1
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
   stringName.indexOf(substr);
```

Given a candidate substring, this method returns the integer index of the first occurrence of the substring in the string. If the substring does not occur in the string, -1 is returned.

{{% notice blue "Example" "rocket" %}}

   ```js {linenos=table}
      console.log("LaunchCode".indexOf("C"));

	  console.log("LaunchCode".indexOf("A"));

      console.log("dogs and dogs and dogs!".indexOf("dog"));
   ```

   **Console Output**

   ```console
      6
	 -1
      0
   ```

{{% /notice %}}

{{% notice blue "Example" "rocket" %}}
An email address must contain an @ symbol. Checking for the presence of this symbol is a part of email address verification in most programs.

   ```js {linenos=table}
      let input = "fake.email@launchcode.org";
	  let atIndex = input.indexOf("@");

	  if (atIndex >-1) {
   	    console.log("Email contains @");
      } else {
        console.log("Invalid email");
      }
   ```

   **Console Output**

   ```console
      Email contains @
   ```

{{% /notice %}}