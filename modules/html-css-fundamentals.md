<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Module 4: HTML & CSS — The Dynamic Duo of Web Creation</h1>

**⏱ Estimated Time: 12-16 hours**

---

## Why This Matters

HTML and CSS are the foundation of the web. Every website you've ever visited is built with them.

HTML defines the content and structure. CSS controls how it looks. They're not programming languages—they're markup and styling—but mastering them is essential before you touch JavaScript.

By the end of this module, you'll build web pages from scratch without templates or frameworks.

---

## Setting Up Your Superhero Headquarters

### Environment Setup

To craft HTML and CSS wonders, you need a trusty text editor and a web browser:

- **Text Editor**: VS Code (which you set up in Module 2)
- **Web Browser**: Chrome or Edge for their powerful DevTools
- **Online Editors** (for quick experiments): [CodePen](https://codepen.io/) or [JSFiddle](https://jsfiddle.net/)

---

## HTML: The Structure

HTML stands for HyperText Markup Language. It's how you tell the browser what content is on the page.

### Anatomy of an HTML Element

```html
<tagname attribute="value">Content goes here</tagname>
```

- **Opening tag:** `<tagname>`
- **Attribute:** `attribute="value"` (optional extra info)
- **Content:** What appears on the page
- **Closing tag:** `</tagname>`

Some elements don't have content or closing tags:

```html
<img src="photo.jpg" alt="A photo">
<br>
<input type="text">
```

### The HTML Document

Every HTML page has this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
<body>
  <!-- Your content goes here -->
</body>
</html>
```

**`<!DOCTYPE html>`** — Tells the browser this is HTML5.

**`<html>`** — The root element. Everything goes inside.

**`<head>`** — Metadata, links to stylesheets, page title. Not visible on the page.

**`<body>`** — Everything visible on the page.

In VS Code, type `!` and press Tab to generate this instantly.

---

## Semantic HTML

Semantic elements describe their meaning, not just their appearance.

### Non-Semantic (Old Way)

```html
<div id="header">...</div>
<div id="navigation">...</div>
<div id="main-content">...</div>
<div id="footer">...</div>
```

### Semantic (Right Way)

```html
<header>...</header>
<nav>...</nav>
<main>...</main>
<footer>...</footer>
```

### Why It Matters

- **Accessibility:** Screen readers understand the page structure
- **SEO:** Search engines know what's important
- **Maintainability:** Code is easier to read and understand

### Common Semantic Elements

| Element | Purpose |
|---------|---------|
| `<header>` | Introductory content, usually contains nav and logo |
| `<nav>` | Navigation links |
| `<main>` | Primary content (only one per page) |
| `<article>` | Self-contained content (blog post, product card) |
| `<section>` | Thematic grouping of content |
| `<aside>` | Sidebar, related content |
| `<footer>` | Footer content |
| `<figure>` | Image with caption |
| `<figcaption>` | Caption for figure |

### Content Elements

| Element | Purpose |
|---------|---------|
| `<h1>` to `<h6>` | Headings (h1 is most important) |
| `<p>` | Paragraph |
| `<a>` | Link |
| `<img>` | Image |
| `<ul>`, `<ol>`, `<li>` | Lists |
| `<strong>` | Important text (bold) |
| `<em>` | Emphasized text (italic) |
| `<span>` | Inline container (no meaning) |
| `<div>` | Block container (no meaning) |

### Heading Hierarchy

Use headings in order. Don't skip levels.

```html
<h1>Page Title</h1>
  <h2>Section</h2>
    <h3>Subsection</h3>
  <h2>Another Section</h2>
```

Only one `<h1>` per page.

---

## Links and Images

### Links

```html
<a href="https://www.example.com">Visit Example</a>
<a href="about.html">Internal Link</a>
<a href="#section-id">Jump to Section</a>
<a href="mailto:email@example.com">Email Link</a>
<a href="tel:+1234567890">Phone Link</a>
```

Open in new tab:

```html
<a href="https://example.com" target="_blank" rel="noopener">Opens in New Tab</a>
```

Always include `rel="noopener"` with `target="_blank"` for security.

### Images

```html
<!-- This is an image -->
<img src="image.jpg" alt="An image" />
```

The `alt` attribute is required for accessibility. Describe what's in the image.

```html
<img
  src="images/hero.jpg"
  alt="Team working together in an office"
  width="800"
  height="600"
>
```

Setting width and height prevents layout shift while loading.

---

## Forms

Forms collect user input.

```html
<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4"></textarea>

  <button type="submit">Send</button>
</form>
```

### Input Types

| Type | Purpose |
|------|---------|
| `text` | Single line text |
| `email` | Email address (validates format) |
| `password` | Hidden text |
| `number` | Numeric input |
| `tel` | Phone number |
| `url` | URL |
| `date` | Date picker |
| `checkbox` | Multiple choice |
| `radio` | Single choice |
| `file` | File upload |
| `submit` | Submit button |

### Labels Matter

Always connect labels to inputs using `for` and `id`:

```html
<label for="email">Email</label>
<input type="email" id="email" name="email">
```

This lets users click the label to focus the input. Essential for accessibility.

### Form Attributes

```html
<input
  type="text"
  name="username"
  placeholder="Enter username"
  required
  minlength="3"
  maxlength="20"
>
```

---

## CSS: The Styling

CSS stands for Cascading Style Sheets. It controls how HTML looks.

### Adding CSS

**Inline (avoid):**
```html
<p style="color: red;">Red text</p>
```

**Internal (for single pages):**
```html
<head>
  <style>
    /* This rule sets the color of all h1 elements to red. */
    h1 {
      color: red;
    }
  </style>
</head>
```

**External (recommended):**
```html
<head>
  <link rel="stylesheet" type="text/css" href="styles.css" />
</head>
```

Always use external stylesheets. They're easier to maintain and can be shared across pages.

### CSS Syntax

```css
selector {
  property: value;
  another-property: another-value;
}
```

```css
h1 {
  color: blue;
  font-size: 24px;
}
```

### Selectors

**Element selector:**
```css
p { color: black; }
```

**Class selector:**
```css
.highlight { background: yellow; }
```
```html
<p class="highlight">Highlighted text</p>
```

**ID selector:**
```css
#header { background: navy; }
```
```html
<header id="header">...</header>
```

**Multiple classes:**
```html
<div class="card featured large">...</div>
```

**Descendant selector:**
```css
nav a { color: white; }
```
All links inside nav elements.

**Direct child:**
```css
nav > ul { list-style: none; }
```
Only ul directly inside nav.

**Combining selectors:**
```css
.card.featured { border: 2px solid gold; }
```
Elements with both classes.

### Specificity

When multiple rules apply, the most specific wins:

1. Inline styles (most specific)
2. ID selectors
3. Class selectors
4. Element selectors (least specific)

```css
p { color: black; }           /* 0-0-1 */
.intro { color: blue; }       /* 0-1-0 */
#hero { color: red; }         /* 1-0-0 */
```

When specificity is equal, the last rule wins.

---

## The Box Model

Every HTML element is a box. Understanding the box model is essential.

```
┌─────────────────────────────────────┐
│             MARGIN                  │
│   ┌─────────────────────────────┐   │
│   │         BORDER              │   │
│   │   ┌─────────────────────┐   │   │
│   │   │      PADDING        │   │   │
│   │   │   ┌─────────────┐   │   │   │
│   │   │   │   CONTENT   │   │   │   │
│   │   │   │             │   │   │   │
│   │   │   └─────────────┘   │   │   │
│   │   │                     │   │   │
│   │   └─────────────────────┘   │   │
│   │                             │   │
│   └─────────────────────────────┘   │
│                                     │
└─────────────────────────────────────┘
```

**Content** — The actual content (text, images).

**Padding** — Space between content and border.

**Border** — The edge of the element.

**Margin** — Space outside the border, between elements.

### Box-Sizing

By default, width/height only apply to content. Padding and border add to the total size.

This is confusing. Fix it:

```css
* {
  box-sizing: border-box;
}
```

Now width/height include padding and border. Always add this to your CSS.

### Setting Box Properties

```css
.card {
  /* All sides */
  padding: 20px;
  margin: 10px;

  /* Vertical | Horizontal */
  padding: 20px 40px;

  /* Top | Right | Bottom | Left (clockwise) */
  margin: 10px 20px 10px 20px;

  /* Individual sides */
  padding-top: 20px;
  margin-left: 10px;

  /* Border */
  border: 1px solid black;
  border-radius: 8px;
}
```

---

## Colors and Typography

### Colors

```css
/* Named colors */
color: red;
color: navy;

/* Hex */
color: #ff0000;
color: #f00;  /* Shorthand */

/* RGB */
color: rgb(255, 0, 0);

/* RGBA (with transparency) */
color: rgba(255, 0, 0, 0.5);

/* HSL */
color: hsl(0, 100%, 50%);
```

### Typography

```css
body {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;
  color: #333;
  background-color: #f2f2f2;
}

h1 {
  color: #333;
  font-size: 36px;
  font-weight: 700;
  letter-spacing: -0.02em;
}

p {
  color: #666;
  font-size: 18px;
}

.uppercase {
  text-transform: uppercase;
}

.centered {
  text-align: center;
}
```

### Units

| Unit | Description |
|------|-------------|
| `px` | Pixels, fixed size |
| `%` | Percentage of parent |
| `em` | Relative to parent font size |
| `rem` | Relative to root font size |
| `vw` | Percentage of viewport width |
| `vh` | Percentage of viewport height |

Use `rem` for font sizes (scales with user preferences).

Use `px` or `%` for spacing and layout.

---

## Flexbox

Flexbox is for one-dimensional layouts—either a row or a column.

### The Container

```css
.container {
  display: flex;
}
```

This makes all direct children flex items.

### Direction

```css
.container {
  display: flex;
  flex-direction: row;      /* Default: horizontal */
  flex-direction: column;   /* Vertical */
}
```

### Justify Content (Main Axis)

```css
.container {
  display: flex;
  justify-content: flex-start;    /* Default: items at start */
  justify-content: flex-end;      /* Items at end */
  justify-content: center;        /* Items centered */
  justify-content: space-between; /* Even space between */
  justify-content: space-around;  /* Even space around */
  justify-content: space-evenly;  /* Equal space everywhere */
}
```

### Align Items (Cross Axis)

```css
.container {
  display: flex;
  align-items: stretch;     /* Default: fill height */
  align-items: flex-start;  /* Top */
  align-items: flex-end;    /* Bottom */
  align-items: center;      /* Center vertically */
}
```

### Gap

```css
.container {
  display: flex;
  gap: 20px;                /* Space between items */
  gap: 20px 40px;           /* Row gap, column gap */
}
```

### Flex Items

```css
.item {
  flex-grow: 1;    /* Item can grow */
  flex-shrink: 1;  /* Item can shrink */
  flex-basis: 200px; /* Starting size */

  /* Shorthand */
  flex: 1;         /* grow: 1, shrink: 1, basis: 0 */
}
```

### Centering with Flexbox

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

This centers content both horizontally and vertically.

---

## CSS Grid

Grid is for two-dimensional layouts—rows AND columns.

### The Container

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
  grid-template-rows: 100px 100px;
  gap: 20px;
}
```

### Flexible Columns

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;  /* 3 equal columns */
  grid-template-columns: 1fr 2fr 1fr;  /* Middle is twice as wide */
  grid-template-columns: repeat(3, 1fr); /* Same as first */
}
```

`fr` means "fraction of available space."

### Auto-Fit and Minmax

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```

This creates as many columns as will fit, each at least 250px wide. Perfect for card grids.

### Placing Items

```css
.item {
  grid-column: 1 / 3;  /* Span from line 1 to line 3 */
  grid-row: 1 / 2;

  /* Or use span */
  grid-column: span 2; /* Take up 2 columns */
}
```

### Grid Areas (Named)

```css
.container {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar main main"
    "footer footer footer";
  grid-template-columns: 200px 1fr 1fr;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

---

## Responsive Design

Your site should work on all screen sizes.

### The Viewport Meta Tag

Always include this in your HTML:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Mobile-First Approach

Write CSS for mobile first, then add complexity for larger screens:

```css
/* Mobile styles (default) */
.container {
  padding: 10px;
}

/* Tablet and up */
@media (min-width: 768px) {
  .container {
    padding: 20px;
  }
}

/* Desktop and up */
@media (min-width: 1024px) {
  .container {
    padding: 40px;
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

### Common Breakpoints

| Breakpoint | Target |
|------------|--------|
| 480px | Large phones |
| 768px | Tablets |
| 1024px | Small laptops |
| 1200px | Desktops |

### Responsive Patterns

**Stacking columns on mobile:**
```css
.grid {
  display: grid;
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (min-width: 1024px) {
  .grid {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
```

**Responsive images:**
```css
img {
  max-width: 100%;
  height: auto;
}
```

**Responsive font sizes:**
```css
html {
  font-size: 14px;
}

@media (min-width: 768px) {
  html {
    font-size: 16px;
  }
}
```

---

## CSS Custom Properties (Variables)

Variables make your CSS maintainable and consistent.

```css
:root {
  --color-primary: #091F40;
  --color-secondary: #C5203E;
  --color-text: #333333;
  --color-background: #ffffff;

  --font-main: 'Helvetica Neue', Arial, sans-serif;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 32px;

  --border-radius: 8px;
}

.button {
  background: var(--color-primary);
  padding: var(--spacing-sm) var(--spacing-md);
  border-radius: var(--border-radius);
  font-family: var(--font-main);
}
```

Change the variable once, it updates everywhere.

---

## Practical Exercises

### Exercise 1: Semantic Structure

Create an HTML page with:

- A header with a logo and navigation
- A main section with an article containing headings and paragraphs
- A sidebar with related links
- A footer with copyright

Use only semantic elements. No divs allowed except where truly necessary.

### Exercise 2: Box Model Practice

Create three boxes side by side:

- Each 200px wide
- 20px padding
- 2px solid border
- 10px margin between them
- Different background colors

Use box-sizing: border-box and explain why the total width calculation changes.

### Exercise 3: Flexbox Navigation

Build a navigation bar:

- Logo on the left
- Links on the right
- Vertically centered
- Horizontal gap between links
- Hover effects on links

### Exercise 4: Grid Card Layout

Build a card grid:

- Cards are at least 250px wide
- As many cards fit per row as possible
- Even gaps between cards
- Cards have an image, title, and description
- Responsive (stacks on mobile)

### Exercise 5: Full Page Layout

Build a complete page layout:

- Fixed header that stays at top when scrolling
- Hero section with centered content
- Three-column feature section
- Two-column content + sidebar section
- Footer with multiple columns
- Fully responsive

### Exercise 6: Contact Form

Build and style a contact form:

- Name, email, and message fields
- Labels for all inputs
- Proper input types
- Required validation
- Submit button
- Error states (style :invalid)
- Responsive layout

---

## Common Mistakes and Fixes

### Div Soup

**Wrong:**
```html
<div class="header">
  <div class="nav">
    <div class="nav-item">Link</div>
  </div>
</div>
```

**Right:**
```html
<header>
  <nav>
    <a href="#">Link</a>
  </nav>
</header>
```

### Forgetting Box-Sizing

If your layout math doesn't add up, you probably forgot:

```css
* {
  box-sizing: border-box;
}
```

### Overusing IDs

IDs are for unique elements and JavaScript hooks. Use classes for styling.

### Not Using a Reset

Browsers have default styles. Start with a reset or normalize:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### Fixed Heights on Content

Don't set fixed heights on content containers. Content length varies. Use min-height if needed.

---

## Form Submissions with Formspree

GitHub Pages can't process forms. Use Formspree for free form handling.

### Setup

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form
3. Copy your form endpoint URL

### Implementation

```html
<form action="https://formspree.io/f/yourformid" method="POST">
  <label for="name">Name</label>
  <input type="text" id="name" name="name" required>

  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>

  <label for="message">Message</label>
  <textarea id="message" name="message" required></textarea>

  <button type="submit">Send</button>
</form>
```

Submissions are emailed to you. The free tier allows 50 submissions per month.

---

## How to Know You're Ready

You should be able to do all of the following without looking anything up:

- [ ] Write semantic HTML from scratch
- [ ] Link CSS files to HTML
- [ ] Use class and element selectors
- [ ] Apply the box model (margin, padding, border)
- [ ] Build layouts with Flexbox
- [ ] Build layouts with Grid
- [ ] Make responsive designs with media queries
- [ ] Use CSS custom properties
- [ ] Build and style forms
- [ ] Center things (seriously, this should be easy now)

---

## Your Gate

Build **three practice layouts** that demonstrate:

1. A hero section with navigation
2. A card-based grid layout
3. A styled form

All must be responsive. Keep your code clean and commented.

**These become projects in your portfolio.**

---

## Quick Reference

### HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header></header>
  <main></main>
  <footer></footer>
</body>
</html>
```

### CSS Reset
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### Flexbox
```css
.flex-container {
  display: flex;
  justify-content: center;    /* horizontal */
  align-items: center;        /* vertical */
  gap: 20px;
}
```

### Grid
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```

### Media Query
```css
@media (min-width: 768px) {
  /* Styles for tablets and up */
}
```

### Custom Properties
```css
:root {
  --color-primary: #091F40;
}

.element {
  color: var(--color-primary);
}
```

---

**Now, you're ready to create web wonders with HTML and CSS, turning the ordinary into the extraordinary! ✨**

---

**Next up:** [Module 5: JavaScript Programming](javascript-fundamentals.md)
