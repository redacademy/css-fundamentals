# Element Reference

## Typography

```html
<h1>Main Heading</h1>
<h2>Secondary Heading</h2>
<h3>Smaller than h2</h3>
<h4>Smaller than h3</h4>
<h5>Smaller than h4</h5>
<h6>Smaller than h5</h6>
<p>This is where we place regular text</p>
<p>One word will be <strong>bold</strong></p>
<p>One word can be <span>styled</span></p>
<p>This will be on <br> 2 lines</p>
```

| Element | Example | Type | Void |
|---------|---------|------|------|
|Heading 1|`<h1>Main Heading</h1>`|Block|False|
|Heading 2|`<h2>Secondary Heading</h2>`|Block|False|
|Heading 3|`<h3>Smaller than h2</h3>`|Block|False|
|Heading 4|`<h4>Smaller than h3</h4>`|Block|False|
|Heading 5|`<h5>Smaller than h4</h5>`|Block|False|
|Heading 6|`<h6>Smaller than h5</h6>`|Block|False|
|Paragraph|`<p>This is where we place regular text</p>`|Block|False|
|Strong|`<p>One word will be <strong>bold</strong></p>`|Inline|False|
|Emphasis|`<p>One word will be <em>emphasized</em></p>`|Inline|False|
|Span|`<p>One word can be <span>styled</span></p>`|Inline|False|
|Line Break|`<p>This will be on <br> 2 lines</p>`|Inline|True|

<a target="_blank" href="http://codepen.io/bwt604RED/pen/QprbJX">View in Codepen</a>

## Grouping

```html
<div>
  DIV elements are used for arbitrarily grouping elements. You can add plain text...
  <p>
    But it is usually better to add text within
    <em>typography elements</em>
    like paragraphs.
  </p>
</div>

<header>
  <p>
    HTML5 gave us more semantic elements like <strong>header</strong>.
    It acts the same as div, but its name gives us an idea of what it <em>does</em>.
  </p>
  
  <p>
    For example, <strong>headers</strong> often contain site navigation, which we can define using the <strong>nav</strong> element:
  </p>
  
  <nav>
    <a href="/html/">HTML</a> |
    <a href="/css/">CSS</a> |
    <a href="/js/">JavaScript</a> |
    <a href="/jquery/">jQuery</a>
  </nav>
</header>

<article>
  <section>
    <h2>When do we use section?</h2>
    <p>It's really up to you. The name section implies that it is a <em>section</em> of something, so you shouldn't use a single section on a page.</p>
  </section>
  
  <section>
    <h2>Do sections have to be part of an article?</h2>
    <p>Nope! Though they <em>can</em> be. <strong>Articles</strong> can also be part of sections - it depends on how you structure your page.</p>
  </section>
</article>

<aside>
  <h4>Many sites also have content that is related to the main content.</h4>
  <p>That's where we can use the aside element.</p>
</aside>

<footer>
  <p>Most sites also contain a footer. Footers sometimes contain their own navigation, and maybe some contact info:</p>
  <p>Contact information: <a href="mailto:someone@example.com">
  someone@example.com</a>.</p>
</footer>
```

| Element | Example | Type | Void |
|---------|---------|------|------|
|Header|`<header></header>`|Block|False|
|Footer|`<footer></footer>`|Block|False|
|Division|`<div></div>`|Block|False|
|Section|`<section></section>`|Block|False|
|Article|`<article></article>`|Block|False|
|Navigation|`<nav></nav>`|Block|False|
|Aside|`<aside></aside>`|Block|False|

<a target="_blank" href="http://codepen.io/bwt604RED/pen/gmzpZB">View in Codepen</a>

## Lists

```html
<ol>
  <li>This will be an ordered (numbered) list</li>
  <li>You can have as many items as you need</li>
</ol>

<ul>
  <li>This will be an unordered (bullet) list</li>
  <li>You can have as many items as you need</li>
</ul>
```

| Element | Example | Type | Void |
|---------|---------|------|------|
|Ordered List|`<ol></ol>`|Block|False|
|Unordered List|`<ul></ul>`|Block|False|
|List Item|`<li></li>`|Block|False|

<a target="_blank" href="http://codepen.io/bwt604RED/pen/OpZNqr">View in Codepen</a>

## Forms

```html
<form>
  <label for="username">Username</label>
  <input type="text" id="username"> <br>

  <label for="password">Password</label>
  <input type="password" id="password"> <br>

  <select>
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </select> <br>

  <label for="description">Description</label> <br>
  <textarea id="description"></textarea>
</form>
```

| Element | Example | Type | Void |
|---------|---------|------|------|
|Form|`<form></form>`|Block|False|
|Input|`<input>`|Inline|True|
|Dropdown Menu (Select)|`<select></select>`|Inline|False|
|Dropdown Menu Option|`<option></option>`|Inline|False|
|Large Text Box|`<textarea></textarea>`|Inline|False|
|Input Label|`<label></label>`|Inline|False|
|Button|`<button></button>`|Inline|False|

<a target="_blank" href="http://codepen.io/bwt604RED/pen/wJjWGV">View in Codepen</a>

## Media

```html
<img src="http://placehold.it/150x150" alt="Second image">

<audio controls>
  <source src="https://www.w3schools.com/tags/horse.ogg" type="audio/ogg">
  <source src="https://www.w3schools.com/tags/horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>

<video width="320" height="240" controls>
  <source src="https://www.w3schools.com/tags/movie.mp4" type="video/mp4">
  <source src="https://www.w3schools.com/tags/movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

| Element | Example | Type | Void |
|---------|---------|------|------|
|Image|`<img>`|Inline|True|
|Audio|`<audio></audio>`|Block|False|
|Video|`<video></video>`|Block|False|

Here are some of the more common elements and their usage.
There are many more, but this should get you started!

<a target="_blank" href="http://codepen.io/bwt604RED/pen/VpxmeP">View Examples in Codepen</a>













