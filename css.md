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

## Organization

## Comments

* Start each file with a [section](https://github.com/alexcarpenter/vscode-idiomatic-css-comments-snippets#section-com-section) comment.
* Outline new sections with a [sub-section](https://github.com/alexcarpenter/vscode-idiomatic-css-comments-snippets#sub-section-com-subsection) comment.

## Whitespace

Whitespace is free, use it to separate items, rules and declarations. Do not hesitate to leave empty lines, it never hurts.

* One (1) empty line between closely related rulesets.
* Two (2) empty lines between loosely related rulesets.
* Four (4) empty lines between entirely new sections.

```css
/* Bad */
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

/* Good */
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

## Resources

* [Sass Guidelines](https://sass-guidelin.es)
* [CSS Guidelines](https://cssguidelin.es/)
* [Managing CSS Projects with ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)