# Attributes

```html
<!-- This tag has a 'class' attribute, its value is 'header' -->
<h1 class="header">Header Text</h1>

<!-- This tag has two attributes, 'src' and 'alt' -->
<!-- Their values are 'http://placehold.it/150x150' and 'First image' -->
<img src="http://placehold.it/150x150" alt="First image">
```

All HTML elements can have __attributes__, which essentially provide _additional information_ about the element.

The term __attribute__ is synonymous with the term __property__.

## Usage

```html
<!-- Bad -->
<img CLASS='my-image' src = 'http://placehold.it/150x150'>

<!-- Good -->
<img class="my-image" src="http://placehold.it/150x150">

<!-- Bad -->
<img id="img-12345" class="my-image" width="500" height="300" src="http://placehold.it/150x150" alt="This is a placeholder image">

<!-- Good -->
<img
  id="img-12345"
  class="my-image"
  width="500"
  height="300"
  src="http://placehold.it/150x150"
  alt="This is a placeholder image">
```

When defining attributes, the convention is to write attribute names in lowercase and to wrap their values in double quotes.
Don't leave spaces on either side of the `=`.

If you have more than three attributes, put them on separate lines.


## Key/Value Pairs

```html
<!-- Example 1 -->
<p id="home-description" class="descripion">
  This is the description of my home page.
</p>

<!-- Example 2 -->
<img class="placeholder" src="http://placehold.it/150x150" alt="First image">
```

__Attributes__ are always defined in the opening tag, and are an example of what we call __key/value pairs__.

In Example 1 to the right, the `p` element has __two attributes__, each __paired__ with a value.

| Key (Attribute Name) | Value |
|-----|-------|
| `id` | home-description |
| `class` | description |


In Example 2 to the right, the `img` element has __three attributes__, each __paired__ with a value.

| Key (Attribute Name) | Value |
|-----|-------|
| `class` | placeholder |
| `src` | http://placehold.it/150x150 |
| `alt` | First image |

## IDs and Classes

```html
<!-- Bad -->
<p id="my-description">Description one</p>
<p id="my-description">Description two</p>
<p id="my-description">Description three</p>

<!-- Good -->
<p class="my-description">Description one</p>
<p class="my-description">Description two</p>
<p class="my-description">Description three</p>

<!-- Better -->
<div class="my-descriptions">
  <p>Description one</p>
  <p>Description two</p>
  <p>Description three</p>
</div>
```

The `id` and `class` attributes are very important in HTML, because they're what CSS uses to apply rules to specific elements.

Each document should only have one instance of any given `id`, but it can have as many instances of a given `class` as you'd like.

A helpful tool for understanding IDs and Classes is to consider the analogy of a student. A student can be taking multiple classes at a time, but they only have one ID.

In software, generality is good, so prefer using `class` over `id` whenever possible.

__NOTE__: When naming classes and IDs, use `kebab-case` (lowercase with hyphens)
