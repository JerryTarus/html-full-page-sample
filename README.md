# HTML FUNDAMENTALS
What is HTML?

HTML (HyperText Markup Language) defines the structure and meaning of a webpage.

HTML tells the browser:

What is a heading

What is text

What is an image

What is navigation

What is a form

HTML does NOT handle styling — that is CSS’s job.

## Basic HTML Document Structure
Every HTML file must follow this structure:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NextGen Coding Hub</title>
  <link rel="icon" href="images/favicon.ico">
  <link rel="stylesheet" href="styles.css">
</head>
<body>

</body>
</html>

Explanation

<!DOCTYPE html> → Tells the browser this is HTML5

<html> → Root of the document

<head> → Metadata (not visible on page)

<body> → All visible content

# SEMANTIC HTML (MEANINGFUL STRUCTURE)

Semantic elements describe what the content means, not how it looks.

## Core Semantic Elements

| Tag         | Purpose                      |
| ----------- | ---------------------------- |
| `<header>`  | Top section of a page        |
| `<nav>`     | Navigation links             |
| `<main>`    | Main page content (only one) |
| `<section>` | Group of related content     |
| `<article>` | Independent content block    |
| `<aside>`   | Side information             |
| `<footer>`  | Bottom of page               |

### Example:Semantic Page Layout
<header>
  <h1>NextGen Coding Hub</h1>
</header>

<nav>
  <ul>
    <li><a href="home.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</nav>

<main>
  <section id="about">
    <h2>About Us</h2>
    <p>NextGen Coding Hub empowers future developers.</p>
  </section>
</main>

<footer>
  <p>&copy; 2026 NextGen Coding Hub</p>
</footer>


=============================================================================================
# CSS OVERVIEW
=============================================================================================

What is CSS?
CSS (Cascading Style Sheets) controls:

Colors

Layout

Spacing

Fonts

Responsiveness

CSS answers:

“How should this HTML look?”

#### Linking CSS (External Stylesheet)

<link rel="stylesheet" href="styles.css">

This follows the DRY principle (Don’t Repeat Yourself).


## SELECTORS — TARGETING ELEMENTS

#### Element Selector
p {
  color: #333;
}

#### Class Selector
.hero {
  background-color: #0a74da;
}

<section class="hero"></section>


#### ID Selector

#contact {
  padding: 40px;
}

<section id="contact"></section>

##### Rule:

Use classes for styling

Use IDs for unique sections and navigation

## Spacing and Margin
Margin  is the space outside an element.

section {
  margin: 40px;
}

Padding is the space inside an element.

section {
  padding: 20px;
}

#### Visual Understanding
[ Margin ]
  [ Padding ]
    Content

## Positiining and Layout
Parent and CHild Elements

<section class="container">
  <p class="child">Hello</p>
</section>

.container {
  padding: 20px;
}

.child {
  color: blue;
}

.container → parent

.child → child

### Positioning Types

Static (Default)
div {
  position: static;
}


#### Positioning Types
Static (default)
div {
  position: static;
}

#### Relative
Moves element relative to itself

.card {
  position: relative;
  top: 10px;
}


#### Absolute
Moves relative to nearest positioned parent

.badge {
  position: absolute;
  top: 10px;
  right: 10px;
}

## IMAGES & PATHS

Relative paths is the most common for this style of inserting images
<img src="images/logo.png" alt="NextGen Coding Hub Logo">
By relative we mean things based on the current location.

Absolute Paths (We do not recommend this locally)
<img src="https://example.com/logo.png">


### Image Styling
img {
  max-width: 100%;
  border-radius: 10px;
  margin: 20px 0;
}

## Backgrounds

.hero {
  background-image: url("images/hero.jpg");
  background-size: cover;
  background-position: center;
  height: 300px;
}


## Forms (User Input)
Form Structure
<form>
  <label for="name">Full Name</label>
  <input id="name" type="text" required>

  <label for="email">Email</label>
  <input id="email" type="email" required>

  <button type="submit">Submit</button>
</form>

Why This Matters

Labels improve accessibility

required enables validation

Proper structure supports backend integration

### Form Styling

form {
  max-width: 500px;
  margin: auto;
}

input {
  width: 100%;
  padding: 10px;
}

ACCESSIBILITY BEST PRACTICES

✔ Use semantic HTML
✔ Always include alt text
✔ Never skip heading levels
✔ Use labels for inputs
✔ Avoid clickable <div>s

### RESPONSIVE DESIGN
For responsive designs, we use media queries
you insert them at the top of your css file

this is how it looks like:
@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
  }
}

Media Queries make the site work on:

✔ Phones

✔ Tablets

✔ Laptops







