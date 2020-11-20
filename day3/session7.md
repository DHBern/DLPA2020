---
layout: single
title: Session 7
---

In the first part of this session, we will experiment how to publish remote images within our workspace. In the second part, we will manipulate a vector graphic image illustrating dance notation movements as one might want to do it in order to create an interactive application around it.

## Locate a IIIF manifest

* Find a resource in [Gallica](https://gallica.bnf.fr)
* Identify the manifest looking at the BNF [API](http://api.bnf.fr/api-iiif-de-recuperation-des-images-de-gallica)

### Publication

For the publication, we use [TIFY](https://github.com/tify-iiif-viewer/tify) that is already loaded in the website structure. To run it, we need a to use another front matter than for the other pages. It needs to be
```md
---
layout: iiif
title: Title-of-your-page
manifest: "url-of-the-manifest"
---
```

## SVG shapes and CSS

From the [following](https://commons.wikimedia.org/wiki/File:Labanotation2.svg) SVG image, we extracted a set of basic shapes. It is available for editing in [JSFiddle](https://jsfiddle.net/lpugin/ypskga23/)

By going through some [CSS](https://www.w3schools.com/css/default.asp) and some [SVG](https://www.w3schools.com/graphics/svg_intro.asp) tutorial, you should be able make some modification to the image.

Try to:
* Add a color to some of the shape
* Group them semantically
* Add some properties responding to some mouse events

### Publication

Because SVG is natively supported by web browser, you can simply copy is in a page!