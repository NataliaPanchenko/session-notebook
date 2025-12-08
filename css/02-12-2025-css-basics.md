## What is CSS?

With CSS (_Cascading Stylesheets_) you can add styling to your HTML elements.

The term _cascading_ in CSS refers to an algorithm that resolves conflicts when multiple styles are defined for a particular element. When deciding which style to apply, CSS takes into account three key factors: specificity, source order, and inheritance.

- Specificity refers to how precisely a selector targets an element. Styles with higher specificity take precedence over those with lower specificity.

- The source order of styles also plays a role in determining which style should be applied. When multiple styles with the same specificity are defined, the style that appears last in the stylesheet will override any previous styles for that element.

- Additionally, CSS allows styles to be inherited from parent elements to their child elements. This means that certain styles can be passed down through the document tree, affecting multiple elements simultaneously.

The term _stylesheet_ refers to a collection of rulesets declared using CSS, usally within a `.css` file.

## Linking Stylesheets

To separate your HTML and CSS code, you can create a new file, like `css/styles.css` and link it to
your HTML file by placing a `<link>` tag in the `<head>` of your HTML document.

```html
<head>
  …
  <link rel="stylesheet" href="css/styles.css" />
</head>
```

A ruleset can have multiple declarations:

```css
h1 {
  color: blue;
  font-size: 3rem;
  text-align: center;
}
```

### Pseudo-classes

The pseudo-class selector selects all elements that are in a specific state. It is used in combination with other selectors.

**Syntax**: `:hover`, `:focus`, … (the pseudo-class name starting with a colon `:`)

#### `:hover`

Selects an element when you hover over it with the mouse.

**Example**:

Select all hovered links.

```css
a:hover {
  color: hotpink;
}
```

```html
<a href="https://www.neuefische.de">neuefische</a>
```

#### `:focus`

Selects an element when it is focused. This is usually the case when you click into an input field or select an element with the tab key.

**Example**:

Select all focused input fields.

```css
input:focus {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

#### Other pseudo-classes

There are many more pseudo-classes like `:active`, `:first-child`, `:last-child`, `:first-of-type`, `:last-of-type`, `:nth-child()`, `:nth-of-type()`, `:not()`, …

### Attribute selectors

The attribute selector selects all elements based on the presence or value of a given attribute.

#### Basic attribute selector

Selects all elements with the specified attribute.

**Syntax**: `[attribute]` (attribute name in square brakets `[]`)

**Example**:

Select all elements that have a `type` attribute.

```css
[type] {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

#### Attribute value selector

Selects all elements with the specified attribute and value.

**Syntax**: `[attribute="value"]` (attribute name followed by `=` and the attribute value in quotation marks `""` — all in square brakets `[]`)

**Example**:

Select all elements that have a `type` attribute with the value `text`.

```css
[type="text"] {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

## Inline and block elements

There are basically two types of elements: inline-level and block-level elements.

### Inline elements

Inline elements **are as wide as their maximum content width** and **flow with the text lines**. They start and end within a line of text. Their box can be cut into multiple parts by line breaks.

Common inline elements include:

- `a`
- `span`
- `strong`
- `em`
- `img`
- `input`
- `button`
- …

### Block elements

Block elements **take up the full width of their parent element** and **always start on a new line**.

Common block elements are:

- `p`
- `h1` - `h6`
- `div`
- `section`
- `article`
- `header`
- `footer`
- `nav`
- …
