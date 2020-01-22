[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Intro to HTML

Our first official forray in to the world of web development will be to learn
HTML. There are three components to every website: HTML, CSS, and JavaScript.
Each "ingredient" has a specific function, for HTML it's the content and
structure of the webpage.

## Prerequisites

* The WDI prework

## Objectives

By the end of this, developers should be able to:

* Write html tags, including writing tags with attributes
* Build out the skeleton for a webpage using the HTML5 boilerplate
* Use a variety of semantic HTML tags
* Convert a design/mock up into a wireframe, then into an HTML document

## Introduction

There are three "ingredients" to every website: HTML, CSS, and JavaScript:

| "Ingredient" | Purpose |
| --- | --- |
| HTML | Content & Structure |
| CSS | Styling and Layout |
| JavaScript | Interactivity |

We're learning HTML in this lesson, which we use for the content and structure
of a Webpage.

HTML is actually the only *required* ingredient and it used to be the case (back
in the very early days of the web) that web pages were only made of HTML. That's
because the original purpose of the world wide web was for sharing scientific
research and reports amongst academics. They had the content of their reports
and needed a way to annotate it so that it would have some styling.

The purpose of HTML is very functional, we want to annotate text to give that
text meaning. You can see what we mean by comparing a document written in plain
text with the same document written in HTML:

![Comparing plain text with HTML](assets/text-v-html.png)

In the plain text example (on the left), it's hard to determine the hierarchy of
the information. With just a touch of HTML, we can fix that problem and give our
content some structure.

So when someone says HTML is the "content and structure" of a webpage, that's
what they mean!

## Review: HTML tags and attributes

The following should all be review from the prework. That's okay though, because
learning is iterative (meaning each time you review something, you learn
a little more and you learn it a little deeper).

### Anatomy of a Tag

From the prework, we know that an HTML tag looks like this:

```html
<p>Content</p>
```

**Review Questions:**

* Which part of this code snippet is the tag?
* Which part of this code snippet is the content?
* What does this tag mean? (i.e. what type of element is this?)

#### Self-closing Tags

The tag in the snippet above has both an opening and a closing tag - a tag that
marks the beginning of some content and a *separate tag* that marks the end of
that content. In this case, the tags mark the begging and ending of a paragraph.
As we learned in the prework, not all elements are made with an opening and
a closing tag; some elements are made with *self-closing* tags:

```html
<img src="cat.gif" alt="A funny cat gif" />
```

**Review Questions:**

* Is this tag self-closing? When looking at the snippet, how do we know?
* What is `src="cat.gif"` in relation to the tag? Is this unique to self-closing
    tags?

#### Attributes

The code snippet above includes two HTML attributes: the `src` and `alt`.
Attributes are for data that describes the tag. So for an `img` tag, the `src`
attributes tells the browser the source of the image we want to display.
Attributes are not unique to self closing tags! That is, both self-closing and
non-self-closing tags can have attributes:

```html
<a href="http://www.google.com">Google</a>
```

**Review Questions:**

* What type of element is this?
* What is the purpose of `href="http://www.google.com"`?
* Can you see a pattern in how tags and attributes work?

#### Common Tags

There are 113 HTML tags in the HTML specification - that's a lot! Luckily,
you'll only use a handful of them in your day-to-day. Here are a few of those:

##### Text Wrappers:

* `<p>`
* `<h1>` to `<h6>`
* `<blockquote>`
* `<li>`

##### Semantic Inline Text-Wrappers:

* `<a>`
* `<span>`
* `<em>`
* `<strong>`


##### Semantic Block Containers:

* `<header>`
* `<footer>`
* `<main>`
* `<section>`
* `<article>`
* `<nav>`
* `<aside>`
* `<div>`

##### List Containers:

* `<ul>`
* `<ol>`
* `<dl>`

**Review Questions:**

> Use these questions for each section above

* What would you suppose this element does?
* Why is it called what it is?
* What meaning does this tag have? Similarly, how might you use it?
* What is the difference between a block and an inline element?

While there are over 100 HTML tags, you only need a handful to build a semantic
HTML page. Don't worry about memorizing any of these (unless you want to).
Instead, learn them as you go!

This [HTML Reference](https://htmlreference.io/) is a really handy page
describing all 113 HTML tags, with examples! We highly recommend bookmarking it
and referring back to it from time to time.

## HTML Pages

Let's move away from talking about single HTML tags and elements and turn to
discussing the HTML page as a whole.

A web page is defined in an HTML document, ending with the extension `.html`.
But we need more than just the extension in an HTML document! We need a tag to
let the browser know that our document is an HTML document, we need some meta
information to describe our document, and we need to let the browser know where
the body of our document is.

All together, that looks like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>This is the title</title>
  </head>
  <body>

  </body>
</html>
```

**Review Questions:**

<details>
  <summary>Does this look familiar, from the prework?</summary>

  It should! But if it doesn't, that's alright. Know that this is the
  boilerplate for just about every HTML document. Read more about it <a
  href="http://htmlshell.com/">here</a>

</details>

<details>
  <summary>What does <code>!DOCTYPE html</code> do?</summary>

<code>!DOCTYPE html</code> declares that the document is an HTML document. This
is largely vestigial but necessary and not worth worrying about at the moment
beyond knowing it is necessary.

</details>

<details>
  <summary>What is the <code>html</code> tag for?</summary>

The next line opens the top level element, <code>html</code>, which represents
the entire document. This is the only top level element and spans the whole
document. The closing <code>html</code> tag should be the last line of the page.

</details>

<details>

  <summary>What information goes inside of the <code>head</code> tag? What about
  the <code>body</code> tag?</summary>

The <code>head</code> element holds metadata about the document; metadata
meaning extra information about the document beyond the content of the document.

One required piece of metadata is the <code>title</code> element. Every page is
required to have a title; without one the HTML document is invalid. The title
element defines what shows up in the browser window, what the page is called
when added to favorites/bookmarks, and what the page is titled in search-engine
results.

The <code>meta</code> element declares that the charset or set of characters
used in this document is <code>utf-8</code> which includes most characters from
all known human languages.  This is not required but can avoid some problems you
might run into if you use special characters.

The <code>body</code> element is for the contents of our document. We're going
to write our own HTML between the opening and closing <code>body</code> tag.

</details>

## Nesting Tags to Build Webpages

So we've discussed tags in isolation and we've discussed the overall webpage as
a whole. How do the two come together to make a webpage?

We can nest tags inside of each other to create a full webpage:

```html
<section>
  <p>
    Something about news:
    <a href="http://www.cnn.com">CNN</a>
  </p>
</section>
```

* What elements are in the snippet above?
* What are we describing with HTML?

## I Do: Working with a Mock

To see the HTML elements we've learned in action, we're going to build out the
HTML for a common piece of a webpage: a header navigation.

The exercise we're going to work through together is [in this
repository](https://git.generalassemb.ly/dc-wdi-fundamentals/nav-bar)

## You Do: Mock -> Wireframe -> HTML

The designer who made the navigation bar was so impressed with your work that they want you to build something else for them.

Work through [this exercise](https://git.generalassemb.ly/dc-wdi-fundamentals/html-css-card-element) on your own to practice the skills we worked on in the previous exercise.

## Closing

We covered the common HTML tags you'll use as a web developer, but we were
really focusing on a separate skill: using HTML to build a webpage, translating
a mock for a webpage to an HTML document. This is an essential skill for web
developers! Now that we've practiced, we can start styling it.

## Additional Resources

* [Internetting is Hard](https://internetingishard.com/)
* [About HTML semantics and front-end architecture](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/)
* [W3 School HTML Tutorial](https://www.w3schools.com/html/)
* [MDN Web Docs: Learning
    HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
alternative licensing, please contact legal@ga.co.
