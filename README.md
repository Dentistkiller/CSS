# 🎨 CSS Crash Course

This crash course provides a detailed overview of **CSS (Cascading Style Sheets)**—the language used to style HTML elements.

## 📚 Table of Contents
1. [What is CSS?](#what-is-css)
2. [CSS Syntax](#css-syntax)
3. [CSS Selectors](#css-selectors)
4. [CSS Box Model](#css-box-model)
5. [CSS Units](#css-units)
6. [CSS Positioning](#css-positioning)
7. [CSS Flexbox](#css-flexbox)
8. [CSS Grid](#css-grid)
9. [CSS Transitions & Animations](#css-transitions--animations)
10. [Responsive Design](#responsive-design)

---

## 📖 What is CSS?
CSS (Cascading Style Sheets) is used to control the presentation of HTML documents. It allows you to style elements, including layout, colors, and fonts.

### 🔥 Why CSS?
- **Separation of Concerns**: HTML structures content, CSS styles it.
- **Consistency**: Apply consistent styles across multiple pages.
- **Accessibility**: Improve user experience across devices.

---

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

