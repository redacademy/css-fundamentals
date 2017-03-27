# Selectors

Selectors are how we define which elements on our site we want to style.

We primarily use three types of selectors: __element__, __class__ and __id__.

## Element Selectors

```css
/* Will select all p elements on a page */
p {
  color: red;
}

/* Will select all header elements on a page */
header {
  position: fixed;
  height: 50px;
  background-color: gray;
}
```

Element selectors are the easiest to understand, as they use the same element names that we use in HTML.

What's important to understand is that when we use element selectors we are choosing to apply a style to __all__ of those elements. This is great for general styles, like text size and color. But what if we want to style just some of a given element? We use __Classes__.


## Classes

```html
<p class="description">This is a description</p>
```

```css
.description {
  font-size: 80%;
  color: lightgray;
}
```

We use classes to group elements. For example, most sites have regular paragraph tags, but also have a __class__ of paragraph called `description`. Descriptions are often a bit smaller, and perhaps a lighter shade of grey than regular text.

To select classes using CSS, prepend the class name with a period.

For example, `<p class="description">` is selected using `.description`.

## IDs

```html
<h1 id="main-description">This is a description</p>
```

```css
#main-description {
  font-size: 110%;
  color: black;
}
```

IDs operate very similarlry to classes.
The difference is that an element of any ID should __only appear once__ on a page.

In the example to the right, we use the id `main-description`. If we need to use the `main-description` id on another element on the page, we should change `main-description` from an ID to a class.
__In general, prefer using classes over IDs__.

To select ids using CSS, prepend the id with a hash.

For example, `<h1 id="main-description">` is selected using `#main-description`.


## Inline Selectors

```html
<p style="color: red">This text will be red</p>
```

Inline selectors are selectors that manually applied to an element.
They exist in the HTML itself.

CSS was essentially invented to avoid inline styles, so they should be avoided whenever possible.
There are a few exceptions (programattically generated background images, some jQuery functionality), but 99% of the time, you should be using CSS instead.
