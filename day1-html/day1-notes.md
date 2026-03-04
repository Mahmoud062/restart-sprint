# Day 1 Notes

Completed tasks and self-test answers for Day 1.

## Self-test Answers

1. I created a semantic `index.html` with `<!doctype html>`, `html lang="en"`, `head` meta charset and viewport, `header`, `nav`, `main` with four sections, and a `footer`.
2. The About section includes a 5–7 line paragraph and an image with meaningful `alt` text.
3. Skills are provided as an unordered list with at least 8 items (technical + soft skills).
4. Projects are in a table with columns Project, Description, Status and three rows.
5. The Contact form includes labeled inputs: name, email, topic (`select`), message (`textarea`), and a submit button — each `label` is linked via `for`/`id`.

## Notes

- Added `tasks.html` static prototype with Today and This Week sections.
- Each task is an `<article>` with `<h3>`, `<p>`, `<time datetime="YYYY-MM-DD">`, and `<details><summary>` for extra info.

---

What is semantic HTML?
Semantic HTML is the use of HTML elements that convey meaning about the content they contain. It helps to structure the content in a way that is meaningful to both humans and machines, improving accessibility and SEO. Examples of semantic HTML elements include `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, and `<footer>`.

Think of semantic HTML as the difference between labeling your moving boxes "Stuff" versus "Kitchen – Plates" and "Bedroom – Books." Both get the job done, but one makes life significantly easier for everyone involved when it comes time to unpack.

In web development, non-semantic tags (like `<div>` and `<span>`) tell the browser nothing about what is inside them. Semantic tags, however, convey the meaning of the content to both the browser and the developer.

Why It Matters
Using semantic tags isn't just about "good practice"—it directly impacts the user experience and your site's performance:

- **Accessibility:** Screen readers rely on semantic structure to navigate a page for visually impaired users. If your entire site is made of `<div>` tags, a screen reader cannot easily distinguish between a navigation bar, the main content, or a sidebar.

- **SEO (Search Engine Optimization):** Search engine crawlers analyze your HTML to understand the hierarchy of your content. Semantic tags help them index your page more accurately, prioritizing content that is clearly marked as `<article>` or `<section>`.

- **Maintainability:** When you (or a teammate) return to your codebase months later, semantic tags act as instant documentation. `<footer>` is self-explanatory; `<div class="footer-wrapper">` requires you to verify the CSS to be sure.

Common Semantic Tags

`<header>`: Introduces introductory content or navigational links.

`<nav>`: Used for major navigation blocks.

`<main>`: Wraps the dominant content of the document.

`<article>`: Represents independent, self-contained content (like a blog post).

`<section>`: Defines a thematic grouping of content.

`<aside>`: Contains content tangentially related to the main content (like a sidebar).

`<footer>`: Marks the bottom of a section or page, usually containing copyrights or contact info.

---

The "Div Soup" Approach (Avoid this):

```html
<div class="header">...</div>
<div class="nav">...</div>
<div class="content">
  <div class="article">...</div>
</div>
<div class="footer">...</div>
```

The Semantic Approach (Preferred):

```html
<header>...</header>
<nav>...</nav>
<main>
  <article>...</article>
</main>
<footer>...</footer>
```

---

Difference between `<section>` and `<div>`

The difference is largely one of intent and meaning:

- **Type:** `<div>` — non-semantic (generic). `<section>` — semantic (thematic group).
- **Purpose:** `<div>` is for styling and layout grouping; `<section>` is used when the content forms a distinct chapter or topic and usually has a heading.
- **When to use `<div>`:** Use a `<div>` when you need a container purely for styling or scripting (e.g., a grid wrapper or layout helper).
- **When to use `<section>`:** Use `<section>` when the content inside is thematically related and would normally have a heading (e.g., "Features", "Contact").

Best Practices

- Don't over-section: if a grouping exists only for layout, prefer a `<div>`.
- Use headings: a `<section>` typically benefits from a heading (e.g., `<h2>`).
- Consider alternatives: an independent piece of content might be an `<article>`, and supplementary content might be an `<aside>`.

---

What does `<meta name="viewport"...>` do?

If you’ve ever opened a website on your phone and had to "pinch-to-zoom" just to read a single sentence, you’ve experienced a site that forgot its viewport meta tag.

At its core, this tag tells the browser how to adjust the page's dimensions and scaling to fit the screen it's being viewed on. Without it, mobile browsers assume you're looking at a desktop-sized page and try to cram all 1,000+ pixels of width into your tiny phone screen.

The Anatomy of the Tag
The most common implementation looks like this:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Here is what those specific instructions are actually doing:

- `width=device-width`: This tells the page to match the screen's width in "device-independent pixels." This allows the page to reflow content based on whether you're using an iPhone, a tablet, or a giant monitor.

- `initial-scale=1.0`: This sets the zoom level when the page first loads. `1.0` means "no zoom" (a 1:1 relationship between CSS pixels and device-independent pixels).

---