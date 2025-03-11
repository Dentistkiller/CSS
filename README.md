# HTML, CSS, and C# in Web Development

This guide explains how **HTML**, **CSS**, and **C#** work together in web development using **ASP.NET Core MVC**.

## 📚 Table of Contents
1. [What is HTML?](#-what-is-html)
   - [Common HTML Tags and Their Purpose](#-common-html-tags-and-their-purpose)
2. [CSS Crash Course](#-css-crash-course)
   - [What is CSS?](#-what-is-css)
   - [CSS Syntax](#-css-syntax)
   - [CSS Selectors](#-css-selectors)
   - [CSS Box Model](#-css-box-model)
   - [CSS Units](#-css-units)
   - [CSS Positioning](#-css-positioning)
   - [CSS Flexbox](#-css-flexbox)
   - [CSS Grid](#-css-grid)
   - [CSS Transitions & Animations](#-css-transitions--animations)
   - [Responsive Design](#-responsive-design)
3. [What is C#?](#-what-is-c)
   - [Example C# Controller](#-example-c-controller)
   - [Example C# View (Index.cshtml)](#-example-c-view-indexcshtml)
   - [Common C# Concepts and Their Purpose](#-common-c-concepts-and-their-purpose)
4. [How Do HTML, CSS, and C# Work Together?](#-how-do-html-css-and-c-work-together)

---

## 🌐 What is HTML?

**HTML (HyperText Markup Language)** provides the basic structure of a webpage by defining elements like headings, paragraphs, links, and images.

### Example HTML Structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Web Page</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a simple webpage using HTML.</p>
    <a href="https://example.com">Visit Example</a>
</body>
</html>
```

### 📄 Common HTML Tags and Their Purpose:

| Tag            | Description                              |
|----------------|------------------------------------------|
| `<!DOCTYPE>`   | Declares the HTML version being used     |
| `<html>`       | Root element of an HTML document         |
| `<head>`       | Contains metadata (title, styles, links) |
| `<title>`      | Defines the page title in the browser tab|
| `<body>`       | Main content of the webpage              |
| `<h1>` - `<h6>`| Headings (from largest to smallest)      |
| `<p>`          | Paragraph                               |
| `<a>`          | Hyperlink to another webpage             |
| `<img>`        | Embeds an image                         |
| `<ul>`         | Unordered (bulleted) list               |
| `<ol>`         | Ordered (numbered) list                 |
| `<li>`         | List item                               |
| `<div>`        | Division (block-level container)        |
| `<span>`       | Inline container for styling            |
| `<input>`      | Input field for forms                   |
| `<button>`     | Clickable button                        |
| `<form>`       | Form for user input                     |
| `<table>`      | Table structure                         |
| `<th>`, `<td>` | Table headers and data cells            |

---

# 🎨 CSS Crash Course

This crash course provides a detailed overview of **CSS (Cascading Style Sheets)**—the language used to style HTML elements.

## 📖 What is CSS?

**CSS (Cascading Style Sheets)** is used to control the presentation of HTML documents. It allows you to style elements, including layout, colors, and fonts.

### 🔥 Why CSS?

- **Separation of Concerns**: HTML structures content, CSS styles it.
- **Consistency**: Apply consistent styles across multiple pages.
- **Accessibility**: Improve user experience across devices.

## 🧱 CSS Syntax
```css
selector {
  property: value;
}
```
Example:
```css
h1 {
  color: blue;
  font-size: 24px;
}
```

### 💡 Ways to Apply CSS
1. **Inline**: Directly within HTML elements.
   ```html
   <h1 style="color: blue;">Hello</h1>
   ```
2. **Internal**: Within a `<style>` tag in the HTML `<head>`.
   ```html
   <style>
     h1 { color: blue; }
   </style>
   ```
3. **External**: Link to a separate `.css` file.
   ```html
   <link rel="stylesheet" href="styles.css">
   ```

---

## 🎯 CSS Selectors
CSS selectors target HTML elements to style them.

### 🔎 Basic Selectors
```css
/* Element selector */
p { color: red; }

/* Class selector */
.button { background-color: blue; }

/* ID selector */
#header { font-weight: bold; }

/* Universal selector */
* { margin: 0; padding: 0; }
```

### 🎨 Advanced Selectors
```css
/* Grouping selector */
h1, h2, h3 { color: green; }

/* Descendant selector */
article p { line-height: 1.5; }

/* Pseudo-class */
a:hover { color: purple; }

/* Pseudo-element */
p::first-line { font-weight: bold; }
```

---

## 📦 CSS Box Model
Every HTML element is a box with these properties:

```
| Margin    | (Space outside the border)
| Border    | (Surrounds padding and content)
| Padding   | (Space between content and border)
| Content   | (Text, images, etc.)
```

Example:
```css
div {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}
```

---

## 📏 CSS Units

### 📊 Absolute Units
- `px` (Pixels)
- `in`, `cm`, `mm` (Inches, centimeters, millimeters)

### 📐 Relative Units
- `%` (Percentage of parent element)
- `em` (Relative to the font size of the element)
- `rem` (Relative to the root element's font size)
- `vw` (Viewport width)
- `vh` (Viewport height)

Example:
```css
p { font-size: 2rem; }
```

---

## 📌 CSS Positioning

### 🗺️ Position Values
- `static` (Default)
- `relative` (Relative to itself)
- `absolute` (Relative to nearest positioned ancestor)
- `fixed` (Relative to viewport)
- `sticky` (Switches between relative and fixed)

Example:
```css
div {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

---

## 📊 CSS Flexbox
Flexbox is a layout model for building flexible and responsive designs.

### 🎛️ Basic Flexbox Example
```css
.container {
  display: flex;
  justify-content: space-between; /* Aligns items horizontally */
  align-items: center; /* Aligns items vertically */
}
```

### 📚 Key Properties
- `justify-content`: Controls horizontal alignment
- `align-items`: Controls vertical alignment
- `flex-direction`: Defines main axis (`row`, `column`)

---

## 📐 CSS Grid
CSS Grid provides a powerful 2D layout system.

### 📦 Basic Grid Example
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

### 📊 Key Properties
- `grid-template-columns` & `grid-template-rows`
- `gap`: Space between grid items
- `grid-area`: Define item positions

---

## 🎬 CSS Transitions & Animations

### 🎥 Transitions
```css
button {
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: blue;
}
```

### 📽️ Key Transition Properties
- `property`: What to animate
- `duration`: Length of animation
- `timing-function`: Easing method

### 🎞️ Animations
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.box {
  animation: fadeIn 2s ease-in;
}
```

---

## 📱 Responsive Design

### 📏 Media Queries
```css
@media (max-width: 600px) {
  body { background: lightgray; }
}
```

### 📐 Flexible Units for Responsiveness
- Use `%`, `vw`, and `vh`
- Avoid fixed `px` for better scaling

---

## 📌 Resources to Learn More
- [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS Tricks](https://css-tricks.com/)

Happy Styling! 🎨

### 🎨 Common CSS Properties and Their Purpose:

| Property         | Description                                   |
|------------------|-----------------------------------------------|
| `color`          | Sets the text color                           |
| `background`     | Background color/image                        |
| `font-size`      | Text size                                    |
| `font-family`    | Font type                                    |
| `margin`         | Space outside an element                     |
| `padding`        | Space inside an element                      |
| `border`         | Border style, width, and color               |
| `width`, `height`| Sets dimensions of an element                |
| `display`        | Determines display type (block, inline, etc.)|
| `position`       | Positioning method (relative, absolute, fixed)|
| `flex`           | Flexbox for flexible layouts                  |
| `grid`           | Grid layout system                           |
| `animation`      | Animates element properties                  |
| `transform`      | Rotate, scale, skew, or translate elements   |

---

## ⚙️ What is C#?

**C#** is a modern, object-oriented programming language commonly used for building web applications with **ASP.NET Core MVC**.

In an ASP.NET Core MVC project:
- **HTML** defines the structure (Views)
- **CSS** applies styles
- **C#** manages logic and data (Controllers and Models)

### Example C# Controller:

```csharp
using Microsoft.AspNetCore.Mvc;

namespace MyWebApp.Controllers
{
    public class HomeController : Controller
    {
        public IActionResult Index()
        {
            ViewBag.Message = "Welcome to My Website";
            return View();
        }
    }
}
```

### Example C# View (Index.cshtml):

```html
@{
    ViewData["Title"] = "Home Page";
}

<h1>@ViewBag.Message</h1>
<p>This is a webpage using HTML, CSS, and C#.</p>
```

### 🧰 Common C# Concepts and Their Purpose:

| Concept          | Description                                   |
|------------------|-----------------------------------------------|
| `namespace`      | Defines a collection of related classes       |
| `class`          | Blueprint for creating objects                |
| `public`, `private` | Access modifiers for visibility control    |
| `string`, `int`, `bool` | Data types                            |
| `var`            | Implicitly typed local variable               |
| `if`, `else`     | Conditional statements                        |
| `for`, `foreach` | Loops for iteration                          |
| `try`, `catch`   | Error handling                               |
| `async`, `await` | Asynchronous programming                      |
| `ViewBag`, `ViewData` | Pass data from Controller to View        |
| `IActionResult`  | Represents the result of an action method     |

---

## 📊 How Do HTML, CSS, and C# Work Together?

1. **HTML** defines the content structure (e.g., headings, paragraphs, forms).
2. **CSS** styles the content (e.g., colors, fonts, layout).
3. **C#** handles the backend logic, processes user input, and renders dynamic content.

