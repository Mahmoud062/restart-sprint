# Day 1 Notes

Completed tasks and self-test answers for Day 1.

## Self-test Answers

1. I created a semantic `index.html` with `<!doctype html>`, `html lang="en"`, `head` meta charset and viewport, `header`, `nav`, `main` with four sections, and a `footer`.
2. The About section includes a 5–7 line paragraph and an image with meaningful `alt` text.
3. Skills are provided as an unordered list with at least 8 items (technical + soft skills).
4. Projects are in a table with columns Project, Description, Status and three rows.
5. The Contact form includes labeled inputs: name, email, topic (`select`), message (`textarea`), and a submit button — each `label` is linked via `for`/`id`.

# Semantic HTML: Quick Reference

Stop using `<div>` for everything. Semantic elements describe the meaning of the content they wrap, which makes things clearer for browsers, screen readers, search engines, and other developers.

---

## Why It Matters

### Accessibility

Screen readers can properly understand and navigate your page structure.

### SEO

Search engines recognize content hierarchy (for example, they can tell what’s main content and what’s footer content).

### Maintainability

No more digging through “div soup.” A `<header>` tag explains itself.

---

## Core Semantic Elements

### `<main>`

Represents the primary content of the page. Use it only once per page.

### `<nav>`

Contains main navigation links.

### `<section>`

Represents a thematic grouping of content. Usually includes a heading (like `<h2>`).

### `<article>`

For self-contained content that makes sense on its own (e.g., a blog post).

### `<aside>`

Secondary content like sidebars or related information.

### `<footer>`

Footer content for a page or a specific section.

---

## `<section>` vs `<div>`

Use `<div>` when you only need a container for styling or layout (Flexbox/Grid). It has no semantic meaning.

Use `<section>` when the content represents a specific topic or logical block.

**Rule of thumb:**  
If the container needs a heading, it’s probably a `<section>`.

---

## Mobile Viewport Meta Tag

This prevents your website from rendering like a zoomed-out desktop version on mobile devices.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### What It Does

- `width=device-width` → Sets the page width to match the device’s screen width.
- `initial-scale=1.0` → Sets the initial zoom level to 100% when the page loads.
