# Setting Up a Project

```
project-folder
  - index.html
```

An HTML project starts very simply.
All you need is a directory (AKA folder) that contains a file called `index.html`.

To view it in your browser, simply open `index.html`. HTML files will open in your default browser.

__Some Best Practices:__

- Use lowercase names for directories and files
- Don't use spaces in your file names, instead use hyphens or underscores to separate words
- Don't use special characters in your file names
- Choose logical and descriptive names for files and folders

## Adding CSS files

```
project-folder
  - css
    - main.css
    - reset.css
  - index.html
```

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
    <!-- Linking CSS -->
    <link rel="stylesheet" type="text/css" href="css/reset.css">
    <link rel="stylesheet" type="text/css" href="css/main.css">
  <head>
  <body></body>
</html>
```

We generally group css files in their own directory. Let's call it `css`.

## Adding JavaScript files

Like CSS files, we group JavaScript files in their own directory. Let's call it `js`.

```
project-folder
  - css
    - main.css
    - reset.css
  - js
    - app.js
    - slideshow.js
  - index.html
```

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/reset.css">
    <link rel="stylesheet" type="text/css" href="css/main.css">

    <!-- Linking Javascript -->
    <script src="js/slideshow.js"></script>
    <script src="js/app.js"></script>
  <head>
  <body></body>
</html>
```

## Adding Assets (Images, etc)

It's good practice to store assets in their own folder as well.
Let's call it `assets`.

Within `assets`, we'll make a folder called images.

```
project-folder
  - css
    - main.css
    - reset.css
  - js
    - app.js
    - slideshow.js
  - assets
    - images
      - car.jpg
      - truck.png
  - index.html
```

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/reset.css">
    <link rel="stylesheet" type="text/css" href="css/main.css">

    <script src="js/slideshow.js"></script>
    <script src="js/app.js"></script>
  <head>

  <body>
    <!-- Using Assets -->
    <img src="assets/images/car.jpg" alt="This is a car">
    <img src="assets/images/truck.png" alt="This is a truck">
  </body>
</html>
```
