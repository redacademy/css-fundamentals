# How CSS Works

```
                    HTML Document Tree

                           html
                            |
             -----------------------------------
             |                                  |
           head                                body
             |                                  |
  ---------------------------           ---------------------
  |       |         |       |           |        |           |
title  link(x2)  script  meta(x3)     header    div       footer
                                        |        |           |
                                       h1    ---------       p
                                             |        |
                                             h2       p

```

In our <a target="_blank" href="https://redacademy.github.io/html-fundamentals/#understanding-html-structure">HTML Wiki</a> we talk about how CSS understands an HTML Document as a __tree__.

This is a really important concept, as it helps us visualize how CSS applies rules to HTML elements.


## Forget the Head

```
HTML Document Tree (without head)

             html
              |
             body
              |
     ---------------------
     |        |           |
   header    div       footer
     |        |           |
    h1    ---------       p
          |        |
          h2       p

```

The `head` tag doesn't actually render any HTML Elements, so we can ignore it when thinking about the Document Tree in the context of CSS.

## Apply a Selector

```css
div {
  color: blue;
}
```

```
The div elements and its descendants
will have the 'color: blue' rule applied

               html
                |
               body
                |
       ---------------------
       |        |           |
     header  → div ←      footer
       |        |           |
      h1    ---------       p
            |        |
          → h2 ←   → p ←
```

Let's say we want to select all `div` elements in our page and apply a font color to them.

CSS finds any `div` elements in the tree, and applies the style to them __and all of their descendants__.

In the example on the right, all text within the `div` will be red, but so will the text in the `h2` and `p` elements that descend from the `div`.

<a target="_blank" href="http://codepen.io/bwt604RED/pen/VpdNqZ">View in Codepen</a>

## Cascading

```css
html {
  font-size: 16px;
}
```

```
The html element and its descendants
will the 'font-size: 16px' rule applied

            html
             ↓
            body
             ↓
    ← ← ← ← ← → → → → → →
    ↓        ↓           ↓
  header    div       footer
    ↓        ↓           ↓
   h1   ← ← ← → → →      p
        ↓         ↓
        h2        p
```

As we saw in the previous example, if we apply a CSS rule to an element, it will be applied to all of its descendants. So, if we apply a rule to `html`, the rule will be applied to the __entire document__.

If we think of the tree as a waterfall with water flowing from the root (the `html` element) down every branch until it finds the bottom, we can say that the CSS rules for `html` __cascade__ down the waterfall to every descendant of `html`.


## Sub-Trees

```css
div {
  color: blue;
}
```

```
Div Sub-Tree

    div
     ↓
 ← ← ← → → →
 ↓         ↓
 h2        p
```

When we use a selector, we effectively break the document tree into __sub trees__.
So, as in the previous example, when we select a `div`, we apply rules to it and its descendants.

CSS works exactly as it did with the `html` element, except now the waterfall starts at the root of the sub tree (`div`) and cascades down from there.

## Combining Selectors

```html
<body>
  <div class="intro uppercase">
    <p>Intro Text</p>
  </div>

  <p>This is the main paragraphy in the document</p>
</body>
```

```css
/*
  Multiple selectors on a single element
*/

/* Select an element and a class */
div.intro {}

/* Select an element with both classes */
.intro.uppercase {}

/*
  Selectors that use hierarchy
*/

/* Select paragraphs descending from elements with a class of intro */
.intro p {
  color: red;
}
```

Sometimes you need to select an element in a certain context. To do this, we can __combine__ selectors.
In the example on the right, if we wanted to select the `p` tags within the `intro` div, we simply combine the two selectors: `.intro p`.

When we combine selectors, we can do it in a couple ways.

First, we can apply several selectors on a simple element. For example, for a `div` with a class of `intro` we can select `div.intro`. If we have a `div` with two classes, `intro` and `uppercase`, we can use both in a selector: `.intro.uppercase`. Notice that there is no space between the selectors.

We can also take advantage of hierarchy when we use selectors. To do so, use a space between selectors. For example, `.intro p` means any paragraphs _that are descendants_ of any elements with the `intro` class. This is extremely powerful. The space is what we use to __signify descendance__. Note that descendants don't need to be _direct_ descendants (children), they can be grand-children, great-grand-children, etc. If we picture our HTML as a tree this is easy to understand. We apply the first selector to part of the tree, and any subsequent selectors are found within that element's sub-tree.


## Specificity

Because CSS rules apply to their selected element and all descendants, it is inevitable that elements will have multiple CSS rules assigned to them. So what happens if those rules conflict? How does the browser know which rule to apply?

The answer is __specificity__.

Specificity calculation is actually very simple math based on the selectors you write. Here's how it works:

- [Inline selectors](#inline-selectors) are worth 1000 points
- [ID](#ids) selectors are worth 100 points
- [Class](#classes) selectors are worth 10 points
- [Element](#element-selectors) selectors are worth 1 point

This is easier to digest when viewed in a table:

Selector | Inline | ID | Class | Element | Score |
|--------|--------|----|-------|---------|-------|
| `p` | 0 | 0 | 0 | 1 | 1 |
| `.intro` | 0 | 0 | 1 | 0 | 10 |
| `#wrapper` | 0 | 1 | 0 | 0 | 100 |
| `#wrapper article.featured p` | 0 | 1 | 1 | 2 | 112|
| `#wrapper nav li.active i` | 0 | 1 | 1 | 3 | 113|
| `#wrapper nav ul li.active i` | 0 | 1 | 1 | 4 | 114|

As you may have guessed, the selector with the higher score will be applied, and any less specific rules will be ignored.

This is called __clobbering__. The strongest survive!

## How specific should you be?

```css
/*
  Keep it simple!
*/

/* This is crazy */
#wrapper nav ul li.active i {}

/* This is probably a better version */
nav .active i {}

/*
  Avoid using html or body selectors, they're probably not needed
*/

/* Bad */
body p {}

/* Good */
p {}

/*
  It helps to define general classes and apply them
  in multiple places in the html
*/
.uppercase { text-transform: uppercase; }
```

Less is more.

The purpose of CSS is to be able to write generalized rules that apply to an entire site.
If you're writing a selector to only apply to one element, ask yourself _why_ that element is different than every other element, and whether it needs to be.

As we mentioned before, Inline and ID selectors should be avoided.
If you only use class and element selectors, your specificity score should never be above 15.

There will be exceptions to this, particularly if you're using outside libraries and need to clobber their CSS, but it's a good generalized rule.
