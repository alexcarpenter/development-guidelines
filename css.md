# CSS Guidelines

## Table of Contents

* [General Guidelines](#general-guidelines)
* [Organization](#organization)
* [Comments](#comments)
* [Whitespace](#whitespace)
* [Resources](#resources)

## General Guidelines

* two (2) spaces indents, no tabs
* ideally, 80-characters wide lines
* properly written multi-line CSS rules
* meaningful use of whitespace
* prefer single quotes to double quotes
* namespace CSS properties

## Organization

Define a solid CSS organizational foundation. I prefer `ITCSS` Inverted Triangle CSS defined by Harry Roberts.

* **Settings** – used with preprocessors and contain font, colors definitions, etc.
* **Tools** – globally used mixins and functions. It’s important not to output any CSS in the first 2 layers.
* **Generic** – reset and/or normalize styles, box-sizing definition, etc. This is the first layer which generates actual CSS.
* **Elements** – styling for bare HTML elements (like H1, A, etc.). These come with default styling from the browser so we can redefine them here.
* **Objects** – class-based selectors which define undecorated design patterns, for example media object known from OOCSS
* **Components** – specific UI components. This is where majority of our work takes place and our UI components are often composed of Objects and Components
* **Utilities** – utilities and helper classes with ability to override anything which goes before in the triangle, eg. hide helper class

## Comments

Well commented code is extremely important. Take time to describe components, how they work, their limitations, and the way they are constructed. Don't leave others in the team guessing as to the purpose of uncommon or non-obvious code.

Comment style should be simple and consistent within a single code base.

Place comments on a new line above their subject.
Keep line-length to a sensible maximum, e.g., 80 columns.
Make liberal use of comments to break CSS code into discrete sections.
Use "sentence case" comments and consistent text indentation.
Tip: configure your editor to provide you with shortcuts to output agreed-upon comment patterns.

Example:

```css
/* ==========================================================================
   Section comment block
   ========================================================================== */

/* Sub-section comment block
   ========================================================================== */

/**
 * Short description using Doxygen-style comment format
 *
 * The first sentence of the long description starts here and continues on this
 * line for a while finally concluding here at the end of this paragraph.
 *
 * The long description is ideal for more detailed explanations and
 * documentation. It can include example HTML, URLs, or any other information
 * that is deemed necessary or useful.
 *
 * @tag This is a tag named 'tag'
 *
 * TODO: This is a todo statement that describes an atomic task to be completed
 *   at a later date. It wraps after 80 characters and following lines are
 *   indented by 2 spaces.
 */

/* Basic comment */
```

## Whitespace

Whitespace is free, use it to separate items, rules and declarations. Do not hesitate to leave empty lines, it never hurts.

* One (1) empty line between closely related rulesets.
* Two (2) empty lines between loosely related rulesets.
* Four (4) empty lines between entirely new sections.

Below is an example of a poorly written CSS file.

```css
.o-table {
  width: 100%;
}
.o-table--fixed {
  table-layout: fixed;
}
.o-table--tiny {
  th, td {
    padding: $inuit-global-spacing-unit-tiny;
  }
}
.o-table--small {
  th, td {
    padding: $inuit-global-spacing-unit-small;
  }
}
.o-table--large {
  th, td {
    padding: $inuit-global-spacing-unit-large;
  }
}
.o-table--huge {
  th, td {
    padding: $inuit-global-spacing-unit-huge;
  }
}
```

and the same example with proper use of whitespace and comments.

```css
/* ==========================================================================
   #TABLE
   ========================================================================== */

/**
 * A simple object for manipulating the structure of HTML `table`s.
 */

.o-table {
  width: 100%;
}





/* Equal-width table cells
   ========================================================================== */

/**
 * `table-layout: fixed` forces all cells within a table to occupy the same
 * width as each other. This also has performance benefits: because the browser
 * does not need to (re)calculate cell dimensions based on content it discovers,
 * the table can be rendered very quickly. Further reading:
 * https://developer.mozilla.org/en-US/docs/Web/CSS/table-layout#Values
 */

.o-table--fixed {
  table-layout: fixed;
}





/* Size variants
   ========================================================================== */

.o-table--tiny {

  th,
  td {
    padding: $inuit-global-spacing-unit-tiny;
  }

}


.o-table--small {

  th,
  td {
    padding: $inuit-global-spacing-unit-small;
  }

}


.o-table--large {

  th,
  td {
    padding: $inuit-global-spacing-unit-large;
  }

}


.o-table--huge {

  th,
  td {
    padding: $inuit-global-spacing-unit-huge;
  }

}
```

This code example is pulled from the [inuitcss project](https://github.com/inuitcss/inuitcss).

## Resources

* [Sass Guidelines](https://sass-guidelin.es)
* [CSS Guidelines](https://cssguidelin.es/)
* [Managing CSS Projects with ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)
* [ITCSS: Scalable and Maintainable CSS Architecture](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)
* [Manage large-scale web projects with new CSS architecture ITCSS](http://www.creativebloq.com/web-design/manage-large-scale-web-projects-new-css-architecture-itcss-41514731)