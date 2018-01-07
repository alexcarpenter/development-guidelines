# HTML Guidelines

## Table of Contents

* [General Guidelines](#general-guidelines)
* [Semantics](#semantics)
* [Twig](#twig)
* [Resources](#resources)

## General Guidelines

## Semantics

HTML5 provides us with lots of semantic elements aimed to describe precisely the content. Make sure you benefit from its rich vocabulary.

```html
<!-- bad -->
<div id="main">
  <div class="article">
    <div class="header">
      <h1>Blog post</h1>
      <p>Published: <span>21st Feb, 2015</span></p>
    </div>
    <p>…</p>
  </div>
</div>

<!-- good -->
<main>
  <article>
    <header>
      <h1>Blog post</h1>
      <p>Published: <time datetime="2015-02-21">21st Feb, 2015</time></p>
    </header>
    <p>…</p>
  </article>
</main>
```

## Twig

### Macros vs Includes

* Macros: reusable markup across a lot of templates
* Includes: part of "pages" that are extracted for readability and reusability

## Resources