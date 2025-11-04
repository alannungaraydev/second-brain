# Modern CSS

## Introduction to CSS

CSS or Cascading Style Sheets is a language for applying styling and layout to HTML documents.

Anatomy of a CSS Rule

```css
selector {
  property: value;
}
/* THIS IS A COMMENT */

selector:pseudo-class::pseudo-element {
}

@at-rule {
  @import "path/to/file";
  @media {
  }
}
```

_selector_
: refer to a target on DOM can be a single or multiple elements.
_property_
: parameter of the element that will be targeted.
_pseudo-class_
: refers to a specific state of the targeted element.
pseudo-element: refers to a specific part of the targeted element
at-rule
: is a special CSS rule to control a behavior.

## Conflict resolution

When multiple CSS rules apply to the same element, the browser must determine which rule takes precedence. This is known as conflict resolution. The following factors influence the resolution process:

1. **Specificity**: More specific selectors take precedence over less specific ones. Specificity is calculated based on the types of selectors used (e.g., IDs are more specific than classes).

2. **Source Order**: If two rules have the same specificity, the one that appears later in the CSS file will take precedence.

3. **Importance**: The `!important` declaration can be used to give a rule higher priority, but it should be used sparingly as it can make debugging more difficult.

Understanding these principles is crucial for effectively managing CSS styles and avoiding unintended overrides.

## Basic Usage

### Inline Styles

```HTML
<div style="background-color:red;">This is a text in a div</div>

```

The inline styles refers the use of the HTML attribute style to change the property values of its self and doesn't affect to others elements

### Internal StyleSheets

```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      div {
        color:red;
      }

    </style>
  </head>
<body>
<div>This text should be in red</div>
  </body>
</html>
```

### External StyleSheets

The styles can be written in a text file with a extension .css that can be referenced in a HTML file using a link element which j

```HTML
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>
  <body>
    <div>This text should be in red</div>
  </body>
</html>
```

```CSS
/* styles.css */
div {
  color: red;
}
```
