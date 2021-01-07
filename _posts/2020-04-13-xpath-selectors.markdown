---
title:  "XPath Selectors"
date:   2020-04-13 16:08:32 +0000
excerpt: XPath is a query language that we can use to select elements on a webpage. In QA it's commonly used in automation to select textboxes or buttons on the page that we can interact with.
toc: true
categories:
  - Blog
tags:
  - xpath
  - automation
  - selectors
  - selenium
---


XPath is a query language that we can use to select elements on a webpage. In QA it's commonly used in automation to select textboxes or buttons on the page that we can interact with.

Xpath is arguably the slowest way of finding elements on a page so you should use this as a last resort if your element does not have an id or name, and if CSS selectors aren’t an option. XPath is usually useful when you need more complicated logic than what CSS selectors allow for.

### Testing XPath in your browser

In Chrome you can just open DevTools in the Elements tab, hit Ctrl+F or cmd+F and paste your xpath into the search.

In other browsers you can use the Console tab in DevTools to execute your XPath query eg.

```javascript
$x("//div")
```


### General XPath

| Expression | Description |
|--|--|
| `nodename` | Selects all nodes with the name “_nodename_“ |
| `/` | Selects from the root node |
| `//` | Selects nodes in the document from the current node that match the selection no matter where they are |
| `.` | Selects the current node |
| `..` | Selects the parent of the current node |
| `@` | Selects attributes |


### Wildcards

XPath wildcards can be used to select unknown XML nodes.

⚠️ Use these sparingly, wildcards increase the time it takes to find your element(s)

| Wildcard | Description |
|--|--|
| `*` | Matches any element node |
| `@*` | Matches any attribute node |
| `node()` | Matches any node of any kind |


### Children and Descendants

| Expression | Description |
|--|--|
| `//ul/li/a` | a single “/” finds a child element that is directly below the parent |
| `//ul//li//a` | two “//” finds any descendants of the parent at any level |



### Attributes

| Expression | Description |
|--|--|
| `//input[@id="id"]` | id of element |
| `//input[@class="class"]` | class of an element, matches the class exactly, if your element has multiple classes then see Conditional Logic or contains() below |
| `//input[@type="submit"]` | matches an element of type “input” who has an attribute “type” with the value of “submit” |
| `//a[contains(@href, 'something')]` | matches an element of type a that has an href attribute that contains “something” |
| `//a[starts-with(@href, 'something')]` | matches an element of type a that has an href attribute that starts with “something” |
| `//a[ends-with(@href, 'something')]` | matches an element of type a that has an href attribute that ends with “something” |


### Attribute Operators

| Expression | Description |
|--|--|
| `//a[@id = "xyz"]` | attribute equals a value |
| `//a[@id != "xyz"]` | attribute does not equal a value |
| `//a[@price > 25]` | attribute value is more than |
| `//a[@price = 9.80 or price = 9.70]` | attribute value equals a value OR another value |
| `//a[@price > 9.00 and price < 9.90]` | attribute value matches one condition AND another condition |


### Order Selectors

If you want to select the first, last or nth element in a list you can use [n] in XPath

ℹ️ XPath lists start at 1 not 0

| Expression | Description |
|--|--|
| `//ul/li[1]` | returns the first “li” child of all “ul” elements |
| `//ul/li[2]` | returns the second “li” child of all “ul” elements |
| `//ul/li[last()]` | returns the last “li” child of all “ul” elements |


### Conditional Logic

You can use OR logic to have multiple selectors for one element, this can be useful for example if your DOM changes when the user is on a mobile device. Instead of having to use different elements for desktop vs. mobile you can use one element and have an OR selector that handles both cases


| Expression | Description |
|--|--|
| `//a[contains(@class, 'enabled') and contains(@class, 'visible')]` | AND – if you need to match an element that has this attribute and value,  **and**  another attribute and value |
| `//a[contains(@class, 'enabled')][contains(@class, 'visible')]` | AND – this is another way of writing the previous expression |
| `//a[contains(@class, 'enabled') or contains(@class, 'visible')]`  |  OR – if you need to match an element that has either this attribute value  **or**  a different attribute value  |
| `//a[contains(@class, 'enabled')] | //a[contains(@class, 'visible')]` | OR – this is another way of writing the previous expression |


### Other Useful Expressions


| Expression | Description |
|--|--|
| `//button[text()="Submit"]` | matches the text of an element exactly |
| `//button[contains(text(),"Go")]` | matches an element that contains text “Go” |
| `//product[@price > 2.50]` | you can use maths to match on an attribute that has a value higher or lower than specified |