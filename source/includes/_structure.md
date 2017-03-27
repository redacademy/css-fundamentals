# Understanding HTML Structure

HTML documents have a strict __hierarchy__.

To understand with this means, let's explore two ways of modelling the document we defined in the previous example: __trees__ and __nesting boxes__.

## Trees

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

One of the most common ways to model hierarchy is by using a __tree__ (similar to family trees).
In fact, this is how CSS and JavaScript understand HTML!

The tree on the right is just another way of modeling the document defined in the previous example.

Some helpful tree terminology:

- An element directly above another is its __parent__
- An element directly below another is its __child__
- Any elements higher in the tree than an element are its __ancestors__
- Any elements lower in the tree than an element are its __descendants__
- Any elements at the same level of the tree and with the _same parent_ are __siblings__

## Nesting Boxes

```
|-------- html -----------------------------------------|
|                                                       |
|  |---- head ---------------------------------|        |
|  | _______  _________   _______   _________  |        |
|  | |title|  |link x 2|  |script|  |meta x 3| |        |
|  | ⎻⎻⎻⎻⎻⎻⎻  ⎻⎻⎻⎻⎻⎻⎻⎻⎻   ⎻⎻⎻⎻⎻⎻⎻   ⎻⎻⎻⎻⎻⎻⎻⎻⎻  |        |
|  |-------------------------------------------|        |
|                                                       |
|  |---- body ---------------------------------------|  |
|  |                                                 |  |
|  |  |- header -|  |---- div -----|  |-- header -|  |  |
|  |  |  _____   |  |  _____  ___  |  |   ______  |  |  |
|  |  | | h1 |   |  | | h2 | | p | |  |   | h1 |  |  |  |
|  |  |  ⎻⎻⎻⎻⎻   |  |  ⎻⎻⎻⎻⎻  ⎻⎻⎻  |  |   ⎻⎻⎻⎻⎻⎻  |  |  |
|  |  |----------|  |--------------|  |-----------|  |  |
|  |-------------------------------------------------|  |
|                                                       |
|-------------------------------------------------------|
```

Heirarchy can also be modelled as nesting boxes, which is a nice way of understanding which elements are the _owners_ of other elements.

Elements _own_ or _contain_ __all of their descendants__.

Nesting Boxes is how the browser renders HTML. __Rendering__ is the act of transforming code into what is shown on the monitor.
