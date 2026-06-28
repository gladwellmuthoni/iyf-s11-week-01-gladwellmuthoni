# Accessibility Audit Report: index.html

## 1. Issues Found
Using Chrome DevTools Lighthouse and the WAVE evaluation tool, I identified the following accessibility gaps in my initial `index.html`:

- **Missing Language Attribute:** The `<html>` tag lacked a `lang` attribute, making it difficult for screen readers to identify the language of the page.
- **Inaccessible Image Path/Alt Text:** The profile image used a local file path (`C:\...`) that would not render on other machines, and while it had an `alt` tag, it needed to be more descriptive.
- **Generic Link Text:** Links like "Visit W3Schools" were functional but could be more descriptive to assist users relying on screen reader "list of links" features.
- **Flat Heading Structure:** The hierarchy needed to be strictly enforced to ensure users can navigate the content sections logically.
- **Form/Input Labels:** (For future pages) Need to ensure that every `<input>` has a matching `<label>` element.

## 2. How I Fixed Them

* **Language Attribute:** Added `lang="en"` to the `<html>` tag to ensure proper screen reader support.
* **Image Accessibility:** * Moved the image into the project folder (`images/ciara.jpg`).
    * Updated the `alt` tag to be descriptive: `alt="Portrait of Gladwell Muthoni, web development student"`.
* **Descriptive Links:** Updated the link text to be more context-aware. Instead of "Visit W3Schools," I used "Learn more about web development at W3Schools."
* **Heading Hierarchy:** Refactored the document to ensure a logical flow:
    * `<h1>` for the main site title.
    * `<h2>` for page sections (Welcome, Interests, etc.).
* **Semantic Structure:** Wrapped content in `<header>`, `<main>`, `<nav>`, and `<footer>` to provide clear landmarks for assistive technology.

## 3. Final Lighthouse Accessibility Score
**Score: 100/100**
*All manual and automated checks passed, ensuring the page is navigable via keyboard and readable by screen readers.*
