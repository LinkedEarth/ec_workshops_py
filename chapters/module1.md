---
title: 'Module 1: Intro to Python'
description:
  'In this module, you will learn how to write basic Python code.'
prev: null
next: /module2
type: chapter
id: 1
---
<exercise id="1" title="Why Python?">

You might be wondering why you should be learning Python.

Python is widely used in the scientific community and it is a great tool to help you further advance your geosciences research.

We will present you with the most important reasons to start using Python in the following [link](https://foundations.projectpythia.org/foundations/why-python.html).


</exercise>

<exercise id="2" title = "Getting Started with Python">

Now that you know why you should be learning Python, let's get started!

Read the [Quickstart zero to Python](https://foundations.projectpythia.org/foundations/quickstart.html) article and try to run the code using Binder (tip: make sure you open the Binder link under the "Rocket Ship" in another window).

Once you are done with the tutorials, complete the exercises below to test your understanding!

Be patient - it might take a few minutes the first time you run the code. But it usually speeds up.

**Question:**

1. Print "I love doing paleoclimate research with Python" on the console.

<codeblock id="01_01">

Remember the print command!

</codeblock>

</exercise>
<exercise id="3" title = "Playing with lists">

**Question:**

1. Create a list with the following archives: `Marine Sediment`, `Coral`, `Ice`, `Wood`
2. Loop over the list to print: "I study paleoclimate using " [archive]

<codeblock id="01_02">
You can create a string by attaching two strings together by using `+`.

For instance,

```
str1 = "I love Python"
str2 = " and I can't wait to use it in paleoclimate research"

str = str1 + str2
```

str is now "I love Python and I can't wait to use it in paleoclimate research"

</codeblock>
</exercise>

</exercise>
<exercise id="4" title = "Playing with dictionaries">

**Question:**

1. Create a dictionary called `dataset1`, that have the following keys: `archiveType`, `geo`, `data`.
2. Set the value for archiveType to `marinesediment`
3. Set the value for `geo` to another dictionary with keys `lat` and `lon`. The `lat` value is `-5` and the `lon` value is `140`
4. Set the value for `data` to a dictionary with keys `values` (set to a list of `[1,2,3]`) and `units` (set to `N/A`)
5. Return the value of the latitude information into a new variable called `latitude`

<codeblock id="01_03">

When using nested dictionaries, you can access the value in the nested dictionary by chaining the keys.

</codeblock>
</exercise>
