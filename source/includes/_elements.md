# Elements

```html
<!-- Format: -->
<element>
  ...content
</element>

<!-- Examples: -->
<h1>This is a large header</h1>

<p>
  This is a paragraph. It can contain as many words as you need.
</p>

<div>
  This is a div, a generic element that contains other elements.
  <h4>Like this smaller header,</h4>
  <p>And this paragraph</p>
</div>
```

__HTML Elements__ (AKA HTML Tags) are the objects we place within an HTML __document__.

They are specific words wrapped in angle brackets (`<` and `>`).
We say that they are _opened_ when you write a tag, (ie. `<header>`),
and _closed_ when you  right the tag again, this time with a forward slash (ie. `</header>`.

## Block Elements

```html
<h1>The header of my documents</h1>
<h4>The subheader; a bit of context</h4>

<p>
  This is where I describe what my page is about.
  Paragraphs are generally much longer than headers.
</p>
```

By default, __Block Elements__ take up the entire width of the document.

In the example to the right, each element will be on its own horizontal section.

<a target="_blank" href="http://codepen.io/bwt604RED/pen/evMgoK">View in Codepen</a>

## Inline Elements

```html
<p>
  <strong>This strong text</strong>
  is beside this normal text
  <em>and beside this emphasized text</em>
</p>

<div>
  <!-- These images will be beside each other -->
  <img src="http://placehold.it/150x150" alt="First image">
  <img src="http://placehold.it/150x150" alt="Second image">
  <img src="http://placehold.it/150x150" alt="Third image">  
</div>
```

Unlike Block Elements, __Inline Elements__ are displayed _in a line_.

<a target="_blank" href="http://codepen.io/bwt604RED/pen/evMgwK">View in Codepen</a>


## Void Elements

```html
<!-- Void Element Usage -->
<img src="http://placehold.it/150x150" alt="First image">
<br>
<input type="text" name="myInput">
```

__Void__ (AKA Empty) elements are not designed to have any content.
Because of this, they don't require a closing tag.

<a target="_blank" href="http://codepen.io/bwt604RED/pen/NpYdQj">View in Codepen</a>







