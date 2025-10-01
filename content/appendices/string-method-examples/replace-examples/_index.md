---
title: "replace Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 5
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
stringName.replace(searchChar, replacementChar);
```

Given a search string `searchChar` and a replacement value `replacementChar`, this method returns a copy of `stringName` with the *first* occurrence of `searchChar` replaced by `replacementChar`.

{{% notice blue Note "rocket" %}}
The `replace` method can be used in more powerful ways utilizing regular expressions. We will not cover those here, but you [can read more at MDN.](http://localhost:8080/devdocs_en_javascript_2025-01/global_objects/string/replace)
{{% /notice %}}


{{% notice blue "Example" "rocket" %}}
 ```js {linenos=table}
console.log("carrot".replace("r", "t"));

console.log("Launch Code".replace(" ", ""));
```
**Console Output**

```console
catrot
LaunchCode
```
{{% /notice %}}

{{% notice blue "Example" "rocket" %}}
Some email providers, including Gmail, allow users to put a `.` anywhere before the `@` symbol. This means that `fake.email@launchcode.org` is the same as `fakeemail@launchcode.org`.

Remove the `.` before the `@` symbol in an email address.

```js {linenos=table}
let input = "fake.email@launchcode.org";
let email = input.replace(".", "");
console.log(email);
```
**Console Output**

```console
fakeemail@launchcode.org
```

This example illustrates a common use case of `replace`, which is to remove a character by replacing it with an empty string.

{{% /notice %}}

{{% notice orange "Warning" "rocket" %}} 

Notice in the last example that if there is not a `.` before the `@` symbol, the `.` that is part of the domain, `launchcode.org` would be inadvertently removed. In a real application, we would want to isolate the portion in front of `@` using `slice`.

{{% /notice %}}