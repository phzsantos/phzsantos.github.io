---
author:
  name: Paulo Henrique Zanoteli Santos
title: Markdown notebook
date: 2022-03-09 16:00:00 UTC-3
categories: [Notebooks, Markdown]
tags: [markdown]
---

## Markdown

Markdown is a markup language similar to HTML but more simple. You can write everything in markdown. Especially documentation. My entire blog posts is written in markdown, every single documentation on github is written using markdown. What are you waiting to learn it? Here's my notes of a course that I did to learn markdown.

## Titles

```markdown
# title 1
## title 2
### title 3
#### title 4
##### title 5
###### title 6

or 

# title 1 #
## title 2 ##
### title 3 ###
#### title 4 ####
##### title 5 #####
###### title 6 ######

or

title
=====

or

title
-----
```

## Paragraph

```markdown
text text text__ <- 2 spaces at end "break line"

text text text
                 <- this, really break line
text text text
```

Example with 2 spaces at end:

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.  
It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

## Highlights

```markdown
**bold** or __bold__

*italic* or _italic_

***bold italic*** or **_bold italic_** or __*bold italic*__

~~scratched~~

> quote
```

## Horizontal rule

```markdown
*** or * * * or ***...

or 

--- or - - - or ---...

or 

___ or _ _ _ or ___...
```

## Unordered list

```markdown
* item 1
* item 2
* item 3

or 

- item 1
- item 2
- item 3

or 

+ item 1
+ item 2
+ item 3

or 

. item 1
. item 2
. item 3
```

## Ordered list

```markdown
1.        1.             1.
2.   or   1.   result -> 2.   markdown follow the sequence of the first number 
3.        1.             3.
```

## Link

```markdown
[text](link)

[text](link "text if the user stop the mouse on the link")
```

## image

```markdown
![text](path)

[![text](path)](link)
```

## Table

```markdown
|title|title|
|-----|-----|
|data |data |

can be like this (but it's not recommended):

|title|title|
|-|-|
|data|data|

Alignment:

left: |:-|
right: |-:|
center: |:-:|

Example:

table with data aligned on center:

|title|title|
|:---:|:---:|
|data |data |
```

## Code

~~~markdown
code in line `code`  
  
code block (can be a pair of 3 "~"):

```language
code
```  
~~~

## Checkbox

```markdown
* [ ] item 1
* [x] item 2 marked
* [ ] item 3
``` 

## Emoji

```markdown
:smile
```

## Documentation and Utilities

[Markdown offical documentation](https://www.markdownguide.org/basic-syntax/)  

[Markdown Emojis](https://gist.github.com/rxaviers/7360908)

[Markdown web preview](https://markdownlivepreview.com/)

[Free course on Udemy(in Portuguese)](https://www.udemy.com/course/aprenda-markdown/)