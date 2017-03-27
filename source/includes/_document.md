# The Document

```html
<!DOCTYPE html>
<html>
  <head><head>
  <body></body>
</html>
```

When your browser loads an HTML file - anything with the `.html` extension - it renders a __document__.
Like word processing documents, HTML documents specify the shape and style of their content.

HTML Documents have a DOCTYPE and two sections: the __head__ and the __body__.

## DOCTYPE

```html
<!DOCTYPE html>
```

The DOCTYPE tells the browser what version of HTML to expect. We use HTML5, which is defined using `<!DOCTYPE html>`.

## Head

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Document</title>

    <!-- Document Icon -->
    <link rel="shortcut icon" href="http://example.com/favicon.ico" />

    <!-- CSS Dependency -->
    <link rel="stylesheet" href="style.css">

    <!-- JS Dependency -->
    <script src="main.js"></script>

    <!-- Meta Tags - These provide non-essential information about the document -->
    <!-- This one tells the browser what text encoding we're using -->
    <meta charset="UTF-8">

    <!-- These two are used for Search Engine Optimization -->
    <meta name="keywords" content="wood, furniture, garden, garden-table, etc.">
    <meta name="description" content="Official dealer of wooden garden furniture.">

  <head>

  <body></body>
</html>
```

The document head contains information about the document, including the document title, any meta tags, any CSS and JavaScript dependencies, and the document icon (displayed in the browser tab).

## Body

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Document</title>

    <link rel="shortcut icon" href="http://example.com/favicon.ico" />
    <link rel="stylesheet" href="style.css">
    <script src="main.js"></script>

    <meta charset="UTF-8">
    <meta name="keywords" content="wood, furniture, garden, garden-table, etc.">
    <meta name="description" content="Official dealer of wooden garden furniture.">
  <head>

  <!-- The Body: -->
  <body>
    <header>
      <h1>This is my header text</h1>
    </header>

    <div class="content">
      <h2>This is the content header</h2>
      <p>This is the content</p>
    </div>

    <footer>
      <p>This is my footer text</p>
    </footer>
  </body>
</html>
```

The body contains the content of the page, built using [HTML Elements](#elements).


