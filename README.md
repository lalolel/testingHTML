# HTML Basics Guide

## Table of Contents
1. [What is HTML?](#what-is-html)
2. [Getting Started](#getting-started)
3. [Basic HTML Structure](#basic-html-structure)
4. [HTML Elements and Tags](#html-elements-and-tags)
5. [Text Content](#text-content)
6. [Links and Navigation](#links-and-navigation)
7. [Images and Media](#images-and-media)
8. [Lists](#lists)
9. [Tables](#tables)
10. [Forms](#forms)
11. [Semantic HTML](#semantic-html)
12. [HTML Attributes](#html-attributes)
13. [Meta Tags and Document Head](#meta-tags-and-document-head)
14. [HTML5 Features](#html5-features)
15. [Best Practices](#best-practices)

## What is HTML?

**HTML (HyperText Markup Language)** is the standard markup language for creating web pages. It describes the structure and content of web documents using elements and tags.

### Key Features:
- **Markup Language**: Uses tags to define elements
- **Structure**: Provides semantic structure to content
- **Platform Independent**: Works across all browsers and devices
- **Foundation**: Base layer of all web technologies
- **Evolving Standard**: Currently HTML5 with ongoing updates

### How HTML Works:
- HTML files have `.html` or `.htm` extensions
- Browsers parse HTML and render it as web pages
- HTML works with CSS (styling) and JavaScript (interactivity)
- Search engines use HTML structure for indexing

## Getting Started

### Creating Your First HTML File
1. Open a text editor (Notepad, VS Code, Sublime Text, etc.)
2. Save the file with `.html` extension
3. Open the file in a web browser

### Basic Tools Needed:
- **Text Editor**: VS Code, Sublime Text, Atom, or even Notepad
- **Web Browser**: Chrome, Firefox, Safari, Edge
- **Optional**: Live Server extension for real-time preview

### File Structure:
```
project/
├── index.html
├── about.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
└── images/
    └── logo.png
```

## Basic HTML Structure

### Minimal HTML Document
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first web page.</p>
</body>
</html>
```

### Document Structure Explained
- `<!DOCTYPE html>`: Declares HTML5 document type
- `<html>`: Root element of the page
- `<head>`: Contains metadata (not visible on page)
- `<body>`: Contains visible page content
- `<title>`: Sets the browser tab title
- `<meta>`: Provides metadata about the document

## HTML Elements and Tags

### Tag Syntax
```html
<!-- Opening and closing tags -->
<tagname>Content goes here</tagname>

<!-- Self-closing tags -->
<tagname />

<!-- Tags with attributes -->
<tagname attribute="value">Content</tagname>
```

### Common HTML Elements

| Element | Purpose | Example |
|---------|---------|---------|
| `<h1>` to `<h6>` | Headings | `<h1>Main Title</h1>` |
| `<p>` | Paragraph | `<p>This is a paragraph.</p>` |
| `<div>` | Generic container | `<div>Content block</div>` |
| `<span>` | Inline container | `<span>Inline text</span>` |
| `<br>` | Line break | `Line 1<br>Line 2` |
| `<hr>` | Horizontal rule | `<hr>` |

### Block vs Inline Elements
```html
<!-- Block elements (take full width) -->
<div>This is a block element</div>
<p>This is also a block element</p>
<h1>Block element heading</h1>

<!-- Inline elements (only take needed width) -->
<span>This is inline</span> <em>This is also inline</em>
<strong>Inline elements</strong> flow with text.
```

## Text Content

### Headings
```html
<h1>Main Heading (Most Important)</h1>
<h2>Secondary Heading</h2>
<h3>Third Level Heading</h3>
<h4>Fourth Level Heading</h4>
<h5>Fifth Level Heading</h5>
<h6>Sixth Level Heading (Least Important)</h6>
```

### Text Formatting
```html
<!-- Basic text formatting -->
<p>This is a <strong>bold</strong> word.</p>
<p>This is an <em>italic</em> word.</p>
<p>This is <u>underlined</u> text.</p>
<p>This is <s>strikethrough</s> text.</p>

<!-- Semantic text elements -->
<p>The <mark>highlighted</mark> text is important.</p>
<p>This is <small>small</small> text.</p>
<p>The formula is H<sub>2</sub>O.</p>
<p>E = mc<sup>2</sup></p>

<!-- Code and preformatted text -->
<p>Use the <code>console.log()</code> function.</p>
<pre>
    This text preserves
    all    spacing
    and line breaks.
</pre>

<!-- Quotations -->
<blockquote>
    "The best way to predict the future is to invent it."
    <cite>- Alan Kay</cite>
</blockquote>

<p>As Einstein said, <q>Imagination is more important than knowledge.</q></p>
```

### Special Characters
```html
<!-- HTML entities -->
<p>&copy; 2024 My Website</p>
<p>&amp; (ampersand)</p>
<p>&lt; (less than)</p>
<p>&gt; (greater than)</p>
<p>&quot; (quotation mark)</p>
<p>&apos; (apostrophe)</p>
<p>&nbsp; (non-breaking space)</p>

<!-- Unicode characters -->
<p>★ ♥ ♦ ♣ ♠</p>
<p>→ ← ↑ ↓</p>
```

## Links and Navigation

### Basic Links
```html
<!-- External link -->
<a href="https://www.example.com">Visit Example.com</a>

<!-- Internal link (same site) -->
<a href="about.html">About Us</a>

<!-- Link to section on same page -->
<a href="#section1">Go to Section 1</a>
<h2 id="section1">Section 1</h2>

<!-- Email link -->
<a href="mailto:contact@example.com">Send Email</a>

<!-- Phone link -->
<a href="tel:+1234567890">Call Us</a>

<!-- Download link -->
<a href="document.pdf" download>Download PDF</a>
```

### Link Attributes
```html
<!-- Open in new tab/window -->
<a href="https://example.com" target="_blank">External Link</a>

<!-- Link relationships -->
<a href="https://example.com" rel="noopener noreferrer">Secure External Link</a>

<!-- Link with title (tooltip) -->
<a href="about.html" title="Learn more about us">About</a>
```

### Navigation Structure
```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="services.html">Services</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>

<!-- Breadcrumb navigation -->
<nav aria-label="Breadcrumb">
    <ol>
        <li><a href="/">Home</a></li>
        <li><a href="/products/">Products</a></li>
        <li aria-current="page">Laptops</li>
    </ol>
</nav>
```

## Images and Media

### Images
```html
<!-- Basic image -->
<img src="image.jpg" alt="Description of image">

<!-- Image with dimensions -->
<img src="photo.jpg" alt="Photo description" width="300" height="200">

<!-- Responsive image -->
<img src="image.jpg" alt="Description" style="max-width: 100%; height: auto;">

<!-- Image with different sources for different screen sizes -->
<picture>
    <source media="(min-width: 800px)" srcset="large-image.jpg">
    <source media="(min-width: 400px)" srcset="medium-image.jpg">
    <img src="small-image.jpg" alt="Responsive image">
</picture>

<!-- Image as link -->
<a href="full-size-image.jpg">
    <img src="thumbnail.jpg" alt="Click for full size">
</a>
```

### Audio and Video
```html
<!-- Audio -->
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>

<!-- Video -->
<video width="640" height="480" controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

<!-- Video with poster and additional attributes -->
<video width="640" height="480" controls poster="video-thumbnail.jpg" preload="metadata">
    <source src="video.mp4" type="video/mp4">
    <track kind="subtitles" src="subtitles.vtt" srclang="en" label="English">
</video>

<!-- Embedded content -->
<iframe width="560" height="315" 
        src="https://www.youtube.com/embed/VIDEO_ID" 
        title="YouTube video player" 
        frameborder="0" 
        allowfullscreen>
</iframe>
```

## Lists

### Unordered Lists
```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item
        <ul>
            <li>Nested item 1</li>
            <li>Nested item 2</li>
        </ul>
    </li>
</ul>
```

### Ordered Lists
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>

<!-- Ordered list with custom start -->
<ol start="5">
    <li>Fifth item</li>
    <li>Sixth item</li>
</ol>

<!-- Different numbering types -->
<ol type="A">
    <li>Item A</li>
    <li>Item B</li>
</ol>

<ol type="i">
    <li>Item i</li>
    <li>Item ii</li>
</ol>
```

### Description Lists
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language - used for structuring web content</dd>
    
    <dt>CSS</dt>
    <dd>Cascading Style Sheets - used for styling web pages</dd>
    
    <dt>JavaScript</dt>
    <dd>Programming language for web interactivity</dd>
</dl>
```

## Tables

### Basic Table Structure
```html
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>City</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alice</td>
            <td>30</td>
            <td>New York</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>25</td>
            <td>Los Angeles</td>
        </tr>
    </tbody>
</table>
```

### Advanced Table Features
```html
<table>
    <caption>Employee Information</caption>
    <thead>
        <tr>
            <th scope="col">Name</th>
            <th scope="col">Department</th>
            <th scope="col" colspan="2">Contact</th>
        </tr>
        <tr>
            <th scope="col"></th>
            <th scope="col"></th>
            <th scope="col">Email</th>
            <th scope="col">Phone</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Alice Johnson</th>
            <td>Marketing</td>
            <td>alice@company.com</td>
            <td>555-0101</td>
        </tr>
        <tr>
            <th scope="row">Bob Smith</th>
            <td rowspan="2">Engineering</td>
            <td>bob@company.com</td>
            <td>555-0102</td>
        </tr>
        <tr>
            <th scope="row">Carol Davis</th>
            <td>carol@company.com</td>
            <td>555-0103</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="4">Total: 3 employees</td>
        </tr>
    </tfoot>
</table>
```

## Forms

### Basic Form Structure
```html
<form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <button type="submit">Submit</button>
</form>
```

### Input Types
```html
<form>
    <!-- Text inputs -->
    <input type="text" name="username" placeholder="Username">
    <input type="password" name="password" placeholder="Password">
    <input type="email" name="email" placeholder="email@example.com">
    <input type="url" name="website" placeholder="https://example.com">
    <input type="tel" name="phone" placeholder="123-456-7890">
    
    <!-- Number inputs -->
    <input type="number" name="age" min="0" max="120" step="1">
    <input type="range" name="volume" min="0" max="100" value="50">
    
    <!-- Date and time -->
    <input type="date" name="birthdate">
    <input type="time" name="appointment">
    <input type="datetime-local" name="event">
    
    <!-- File upload -->
    <input type="file" name="document" accept=".pdf,.doc,.docx">
    <input type="file" name="images" accept="image/*" multiple>
    
    <!-- Checkboxes and radio buttons -->
    <input type="checkbox" id="newsletter" name="newsletter" value="yes">
    <label for="newsletter">Subscribe to newsletter</label>
    
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
    
    <!-- Hidden input -->
    <input type="hidden" name="form_id" value="contact_form">
</form>
```

### Form Elements
```html
<form>
    <!-- Textarea for multi-line text -->
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50" 
              placeholder="Enter your message here..."></textarea>
    
    <!-- Select dropdown -->
    <label for="country">Country:</label>
    <select id="country" name="country">
        <option value="">Select a country</option>
        <option value="us">United States</option>
        <option value="ca">Canada</option>
        <option value="uk">United Kingdom</option>
    </select>
    
    <!-- Multi-select -->
    <label for="skills">Skills:</label>
    <select id="skills" name="skills" multiple>
        <option value="html">HTML</option>
        <option value="css">CSS</option>
        <option value="js">JavaScript</option>
        <option value="python">Python</option>
    </select>
    
    <!-- Fieldset for grouping -->
    <fieldset>
        <legend>Personal Information</legend>
        <label for="fname">First Name:</label>
        <input type="text" id="fname" name="fname">
        
        <label for="lname">Last Name:</label>
        <input type="text" id="lname" name="lname">
    </fieldset>
    
    <!-- Buttons -->
    <button type="submit">Submit Form</button>
    <button type="reset">Reset Form</button>
    <button type="button" onclick="customFunction()">Custom Action</button>
</form>
```

### Form Validation
```html
<form>
    <!-- Required field -->
    <input type="text" name="username" required>
    
    <!-- Pattern validation -->
    <input type="text" name="zipcode" pattern="[0-9]{5}" 
           title="Please enter a 5-digit zip code">
    
    <!-- Length constraints -->
    <input type="text" name="username" minlength="3" maxlength="20">
    
    <!-- Number constraints -->
    <input type="number" name="age" min="18" max="100">
    
    <!-- Custom validation message -->
    <input type="email" name="email" required 
           oninvalid="this.setCustomValidity('Please enter a valid email address')"
           oninput="this.setCustomValidity('')">
</form>
```

## Semantic HTML

### Semantic Structure Elements
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Semantic HTML Example</title>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section id="home">
            <h1>Welcome to Our Website</h1>
            <article>
                <header>
                    <h2>Latest News</h2>
                    <time datetime="2024-01-15">January 15, 2024</time>
                </header>
                <p>This is the content of our latest news article...</p>
                <footer>
                    <p>By <address>John Doe</address></p>
                </footer>
            </article>
        </section>
        
        <aside>
            <h3>Related Links</h3>
            <ul>
                <li><a href="#link1">Related Article 1</a></li>
                <li><a href="#link2">Related Article 2</a></li>
            </ul>
        </aside>
    </main>
    
    <footer>
        <p>&copy; 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
```

### Semantic Elements Explained

| Element | Purpose |
|---------|---------|
| `<header>` | Page or section header |
| `<nav>` | Navigation links |
| `<main>` | Main content area |
| `<section>` | Thematic grouping of content |
| `<article>` | Independent, standalone content |
| `<aside>` | Side content (sidebar) |
| `<footer>` | Page or section footer |
| `<figure>` | Self-contained content (images, diagrams) |
| `<figcaption>` | Caption for figure |
| `<time>` | Date/time information |
| `<address>` | Contact information |

### Content Sectioning Examples
```html
<!-- Figure with caption -->
<figure>
    <img src="chart.png" alt="Sales data chart">
    <figcaption>Q4 2023 Sales Performance</figcaption>
</figure>

<!-- Details and summary (collapsible content) -->
<details>
    <summary>Click to expand</summary>
    <p>This content is hidden by default and can be toggled.</p>
</details>

<!-- Mark important text -->
<p>The deadline is <mark>December 31st</mark>.</p>

<!-- Progress indicator -->
<label for="progress">Download progress:</label>
<progress id="progress" value="75" max="100">75%</progress>

<!-- Meter (gauge) -->
<label for="disk-usage">Disk usage:</label>
<meter id="disk-usage" value="0.6">60%</meter>
```

## HTML Attributes

### Global Attributes
```html
<!-- id - unique identifier -->
<div id="unique-element">Content</div>

<!-- class - CSS class names -->
<div class="container large-text">Content</div>

<!-- style - inline CSS -->
<p style="color: blue; font-size: 18px;">Styled text</p>

<!-- title - tooltip text -->
<abbr title="HyperText Markup Language">HTML</abbr>

<!-- data attributes - custom data -->
<div data-user-id="123" data-role="admin">User info</div>

<!-- lang - language -->
<p lang="es">Hola mundo</p>

<!-- dir - text direction -->
<p dir="rtl">Right-to-left text</p>

<!-- hidden - hide element -->
<div hidden>This is hidden</div>

<!-- contenteditable - make element editable -->
<div contenteditable="true">You can edit this text</div>

<!-- spellcheck - enable/disable spell checking -->
<textarea spellcheck="false">No spell check here</textarea>
```

### Accessibility Attributes
```html
<!-- ARIA attributes for accessibility -->
<button aria-label="Close dialog">×</button>

<div role="button" tabindex="0" aria-pressed="false">Custom button</div>

<img src="chart.png" alt="Sales increased 25% this quarter" 
     aria-describedby="chart-description">
<p id="chart-description">Detailed description of the sales chart...</p>

<!-- Skip links for keyboard navigation -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Landmark roles -->
<nav role="navigation" aria-label="Main navigation">
<main role="main" id="main-content">
<aside role="complementary" aria-label="Related articles">
```

## Meta Tags and Document Head

### Essential Meta Tags
```html
<head>
    <!-- Document encoding -->
    <meta charset="UTF-8">
    
    <!-- Viewport for responsive design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Page description -->
    <meta name="description" content="Learn HTML basics with this comprehensive guide">
    
    <!-- Keywords (less important for SEO now) -->
    <meta name="keywords" content="HTML, web development, tutorial">
    
    <!-- Author -->
    <meta name="author" content="Your Name">
    
    <!-- Page title -->
    <title>HTML Basics Guide - Learn Web Development</title>
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="/favicon.ico">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    
    <!-- CSS -->
    <link rel="stylesheet" href="styles.css">
    
    <!-- External fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
```

### Social Media Meta Tags
```html
<head>
    <!-- Open Graph (Facebook, LinkedIn) -->
    <meta property="og:title" content="HTML Basics Guide">
    <meta property="og:description" content="Comprehensive guide to learning HTML">
    <meta property="og:image" content="https://example.com/image.jpg">
    <meta property="og:url" content="https://example.com/html-guide">
    <meta property="og:type" content="website">
    
    <!-- Twitter Cards -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="HTML Basics Guide">
    <meta name="twitter:description" content="Learn HTML from basics to advanced">
    <meta name="twitter:image" content="https://example.com/twitter-image.jpg">
    
    <!-- Additional SEO -->
    <meta name="robots" content="index, follow">
    <meta name="googlebot" content="index, follow">
    <link rel="canonical" href="https://example.com/html-guide">
</head>
```

## HTML5 Features

### New Input Types
```html
<!-- HTML5 input types with built-in validation -->
<input type="color" name="theme-color">
<input type="date" name="event-date">
<input type="email" name="user-email" placeholder="you@example.com">
<input type="month" name="birth-month">
<input type="number" name="quantity" min="1" max="100">
<input type="range" name="volume" min="0" max="100" step="10">
<input type="search" name="site-search" placeholder="Search...">
<input type="tel" name="phone" placeholder="(555) 123-4567">
<input type="time" name="appointment">
<input type="url" name="website" placeholder="https://example.com">
<input type="week" name="project-week">
```

### Canvas and SVG
```html
<!-- Canvas for dynamic graphics -->
<canvas id="myCanvas" width="400" height="200">
    Your browser does not support the canvas element.
</canvas>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    ctx.fillStyle = '#FF0000';
    ctx.fillRect(0, 0, 150, 100);
</script>

<!-- SVG for scalable vector graphics -->
<svg width="200" height="200">
    <circle cx="100" cy="100" r="50" fill="blue" />
    <rect x="50" y="50" width="100" height="100" fill="red" opacity="0.5" />
</svg>
```

### Local Storage Example
```html
<script>
    // Store data locally
    localStorage.setItem('username', 'JohnDoe');
    
    // Retrieve data
    const username = localStorage.getItem('username');
    
    // Session storage (cleared when tab closes)
    sessionStorage.setItem('temporary', 'data');
</script>
```

### Geolocation API
```html
<script>
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position) {
            console.log("Latitude: " + position.coords.latitude);
            console.log("Longitude: " + position.coords.longitude);
        });
    }
</script>
```

## Best Practices

### 1. Use Semantic HTML
```html
<!-- Good: Semantic structure -->
<article>
    <header>
        <h1>Article Title</h1>
        <time datetime="2024-01-15">January 15, 2024</time>
    </header>
    <p>Article content...</p>
    <footer>
        <p>By Author Name</p>
    </footer>
</article>

<!-- Poor: Non-semantic structure -->
<div class="article">
    <div class="title">Article Title</div>
    <div class="date">January 15, 2024</div>
    <div class="content">Article content...</div>
</div>
```

### 2. Always Include Alt Text for Images
```html
<!-- Good: Descriptive alt text -->
<img src="chart.png" alt="Sales increased 25% from Q3 to Q4 2023">

<!-- Good: Empty alt for decorative images -->
<img src="decorative-border.png" alt="" role="presentation">

<!-- Poor: Missing or generic alt text -->
<img src="chart.png" alt="image">
<img src="chart.png">
```

### 3. Proper Form Labels
```html
<!-- Good: Explicit labels -->
<label for="email">Email Address:</label>
<input type="email" id="email" name="email">

<!-- Good: Implicit labels -->
<label>
    Email Address:
    <input type="email" name="email">
</label>

<!-- Poor: No labels -->
<input type="email" name="email" placeholder="Email">
```

### 4. Validate Your HTML
```html
<!-- Use W3C Markup Validator: https://validator.w3.org/ -->

<!-- Common validation errors to avoid: -->
<!-- - Unclosed tags -->
<!-- - Missing required attributes -->
<!-- - Invalid nesting -->
<!-- - Duplicate IDs -->
```

### 5. Optimize for Performance
```html
<head>
    <!-- Preload critical resources -->
    <link rel="preload" href="critical.css" as="style">
    <link rel="preload" href="hero-image.jpg" as="image">
    
    <!-- Defer non-critical JavaScript -->
    <script src="analytics.js" defer></script>
    
    <!-- Optimize images -->
    <img src="photo.webp" alt="Description" 
         loading="lazy" width="300" height="200">
</head>
```

### 6. Mobile-First Responsive Design
```html
<head>
    <!-- Essential viewport meta tag -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Responsive images -->
    <picture>
        <source media="(min-width: 800px)" srcset="large.jpg">
        <source media="(min-width: 400px)" srcset="medium.jpg">
        <img src="small.jpg" alt="Responsive image">
    </picture>
</head>
```

### 7. Accessibility Best Practices
```html
<!-- Skip navigation for screen readers -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Proper heading hierarchy -->
<h1>Main Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>

<!-- ARIA labels and roles -->
<nav role="navigation" aria-label="Main navigation">
<button aria-expanded="false" aria-controls="menu">Menu</button>
<div id="menu" role="menu" hidden>
    <!-- Menu items -->
</div>

<!-- Focus management -->
<button type="button" onclick="openModal()" 
        aria-describedby="modal-description">
    Open Modal
</button>
```

### 8. SEO-Friendly Structure
```html
<head>
    <!-- Unique, descriptive titles -->
    <title>HTML Basics Guide - Learn Web Development | YourSite</title>
    
    <!-- Meta description (150-160 characters) -->
    <meta name="description" content="Complete HTML tutorial covering basics to advanced concepts. Learn semantic HTML, forms, accessibility, and best practices.">
    
    <!-- Structured data -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Article",
        "headline": "HTML Basics Guide",
        "author": "Your Name",
        "datePublished": "2024-01-15"
    }
