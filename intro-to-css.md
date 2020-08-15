## CSS (Cascading Style Sheets)

We use CSS to tell browsers how we would like for them to **display** the
elements of our document.

### So Many Ways To Style A Site

So far the website we've created together has no CSS and is a little plain.

Let's look at some websites and take away their CSS and see how dull and plain
they become.  Note that the content will still be the same, just the *styling*
will be different.  

Now lets checkout [CSS Zen Garden](http://www.csszengarden.com) to see some
  examples of the great power and diversity that CSS can have on a website.  

#### What Not To Build

Although its possible to implement just about any design possible that doesn't mean you should.  That being said let's examine [https://www.lingscars.com/](https://www.lingscars.com/) and see why that might be the case. 

### CSS File: We do (5 minutes / 1:55)

To get started writing styles.

```css
body {
  background: lemonchiffon;
}
```

When we refresh the page, we should see the background color change.

Note: There are three ways to write CSS into your HTML file.

- **Inline** (Good) ==> `<p style="background: blue;">Inline Example</p> `
- **Internal** (Better) ==> `<style>` element in `<head>` of html file
- **External** (Best!) ==> linking an external CSS file

### CSS Rules (5 minutes / 2:00)

CSS styles are a series of **rules** or **rulesets**. A rule is a combination of
a **selector** and a set of **declarations**.

<img src="https://i.imgur.com/k9bCRpG.png" width=400/>

## Selector (10 minutes / 2:10)

A selector is a pattern used to match HTML elements to the rule that should
apply. As shown, a selector can be an element. Or, very commonly, we add `class`
or `id` attributes to mark elements for targeting by a specific rule.

- Periods '.' are used to select a class like this

```css
.class-name {
  color: red;
}
```

- Hashes '#' are used to select an id like this

```css
#id-name {
  color: blue;
}
```

Note: CSS rules that are **More Specific** will override rules that are less
specific.

- Targeting parent element ==> *Least specific*
- Targeting element directly ==> *Less specific*
- Targeting class ==> *More specific*
- Targeting id ==> *Most specific*

CSS can also overwrite itself. For example, if you have two rules that have the same precedence (like two classes), the one that appears further down in the file will overwrite the previous one.

## Box Model: I do (10 minutes / 3:10)

The browser represents HTML elements on the page as blocks. Every block on the page has `width`, `height`, `padding`, `margin`, and `border` properties. This diagram shows how these values relate to one another.

![Box
Model](https://upload.wikimedia.org/wikipedia/commons/5/53/Css_box_model.svg)

## Taking Up Space: Inline vs Block Elements, and How to Center Content (10 minutes / 3:20)

Typically, elements are either **inline** or **block** elements.  We can change this with the `display` property, and the four values we can assign it.  

![block](./images/block.png)

- A **block** element has some whitespace above and below it and does not tolerate any HTML elements next to it. This makes the element a block box. It won't let anything sit next to it on the page and takes up the full width. This is what most of the elements on a webpage are.

----

![inline](./images/inline.png)

- An **inline** element has no line break before or after it. This makes the element sit on the same line as another element, but without formatting it like a block. It only takes up as much width as it needs. Inline places all your elements on a single line. Padding / margins only work left + right, not top and bottom. Top and bottom spacing is controlled by line-height property because the content is inline.

----

![inline-block](./images/inline-block.png)

- An **inline-block** element is placed as an inline element (on the same line
  as adjacent content), but it behaves as a block element. This makes the
  element a block box but will allow other elements to sit next to it on the
  same line. You can move these with the text-align property, which is weird but useful.

----

- If you assign **none** as the value of the display, this will make the element and its content disappear from the page entirely!

## Importing Fonts: 

Google hosts a massive repository of fonts that can be imported for use on your
page.

To add a font:

1. Go to [Google Fonts](https://fonts.google.com/)
2. Click the **+** button next to any font you want to import to your page (as a rule, any more than 3 fonts in a project quickly begins to look disjointed).
3. After selecting 1 or more fonts, click the bar on the bottom that says **1 Family Selected**.
4. Add the provided link element (something like `<link
   href="https://fonts.googleapis.com/css?family=Fresca" rel="stylesheet">`) to the head of your HTML.
5. Add the provided declaration (something like `font-family: 'Fresca',sans-serif;`) to a CSS rule targeting the elements to which you would like toapply the font.

To see this inline behavior we can create a few `div` tags to our **HTML**

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
