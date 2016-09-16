---
layout: post
title: Universal Web Design：响应式设计要点
category: [coding, booknote, blog]
---

There's no mobile design. It's all about universal web design.

## Fixed Design V.S. Fluid Design

### Units
e.g., px v.s. em

### Fluid Layout

<b>target/context = result</b>
关键是确定context.

- for <b>elements</b>, the context is its container'width;
- for <b>margins(or anything outside a box model)</b>, the context is its container'width;
- for <b>paddings(or anything inside a box model)</b>, the context is the element itself's width; 


## Adaptive Design

target on different devices, or resolutions, and so on.


## Responsive Design

more universal and flexible

## Media Queries

example
```css
@media screen and (max-width: 960px) 
{
/**/
}
```

## Responsive Media

### Using max-width

```css
img, object, enbed, video {
  max-width: 100%;
}
```

this can keep the media object scale into the right size

### Retina Images

#### background-image

```css
@media
only screen and (-webkit-min-device-pixel-ratio: 1.5),
only screen and (min-device-pixel-ratio: 1.5),
{
  background-image: url("image@2x.png");
  -webkit-background-size: 40px 20px;
  background-size: 40px 20px;  /*just as the same as the original image size*/
}
```

#### file size


[<b>pictureFill Method</b>](http://scottjehl.github.io/picturefill/)

this method must include picturefill.js in <head>

```html
<picture alt="Our Alternate Text">
  <!-- Smallest size first - no @media qualifier -->
  <source src="content-image.jpeg" />
  <!-- Large size - send to viewports 800px wide and up -->
  <source src="content-image-lrg.jpeg" media="(min-width:
 800px)" />
<!-- Fallback content for non-JS or non-media-query-
supporting-browsers -->
<noscript>
  <img src="content-image.jpeg" alt="Our Alternate
 Text" />
  </noscript>
</picture>
```

