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

Generated on 2026-03-04.
What is semantic HTML?
Semantic HTML is the use of HTML elements that convey meaning about the content they contain. It helps to structure the content in a way that is meaningful to both humans and machines, improving accessibility and SEO. Examples of semantic HTML elements include <header>, <nav>, <main>, <article>, <section>, and <footer>.

Think of semantic HTML as the difference between labeling your moving boxes "Stuff" versus "Kitchen – Plates" and "Bedroom – Books." Both get the job done, but one makes life significantly easier for everyone involved when it comes time to unpack.

In web development, non-semantic tags (like <div> and <span>) tell the browser nothing about what is inside them. Semantic tags, however, convey the meaning of the content to both the browser and the developer.

Why It Matters
Using semantic tags isn't just about "good practice"—it directly impacts the user experience and your site's performance:

Accessibility: Screen readers rely on semantic structure to navigate a page for visually impaired users. If your entire site is made of <div> tags, a screen reader cannot easily distinguish between a navigation bar, the main content, or a sidebar.

SEO (Search Engine Optimization): Search engine crawlers analyze your HTML to understand the hierarchy of your content. Semantic tags help them index your page more accurately, prioritizing content that is clearly marked as <article> or <section>.

Maintainability: When you (or a teammate) return to your codebase months later, semantic tags act as instant documentation. <footer> is self-explanatory; <div class="footer-wrapper"> requires you to verify the CSS to be sure.

Semantic vs. Non-Semantic
Here is a quick look at how shifting to semantic markup cleans up your structure:

The "Div Soup" Approach (Avoid this):

HTML

<div class="header">...</div>
<div class="nav">...</div>
<div class="content">
  <div class="article">...</div>
</div>
<div class="footer">...</div>
The Semantic Approach (Preferred):

HTML

<header>...</header>
<nav>...</nav>
<main>
  <article>...</article>
</main>
<footer>...</footer>
Common Semantic Tags
<header>: Introduces introductory content or navigational links.

<nav>: Used for major navigation blocks.

<main>: Wraps the dominant content of the document.

<article>: Represents independent, self-contained content (like a blog post).

<section>: Defines a thematic grouping of content.

<aside>: Contains content tangentially related to the main content (like a sidebar).

<footer>: Marks the bottom of a section or page, usually containing copyrights or contact info.

---

Difference between <section> and <div>?

The difference between <section> and <div> is all about intent. While they might look identical in a browser, they tell very different stories to search engines and assistive technologies.The Quick BreakdownFeature<div><section>TypeNon-semantic (Generic)Semantic (Meaningful)PurposeStyling and layout grouping.Thematic grouping of content.SEO ImpactNone; ignored by crawlers.Helps search engines understand page structure.AccessibilityInvisible to screen readers.Can act as a landmark for navigation.When to use <div>Use a <div> when you need a container solely for CSS styling or JavaScript hooks, and the content inside doesn't necessarily form a "chapter" or a distinct part of the page's story.Example: Wrapping a group of elements to apply a Flexbox grid, adding a background color, or creating a "wrapper" to center your content on the screen.Think of it as: A plain cardboard box used just to move things around.When to use <section>Use a <section> when the content inside is thematically related and would typically appear in a document's outline. A good rule of thumb: if the group of elements deserves a heading (<h2> through <h6>), it probably belongs in a <section>.Example: A "Features" area, a "Contact Us" block, or a "Testimonials" part of a landing page.Think of it as: A chapter in a book. It has a specific topic that contributes to the whole.Best PracticesDon't over-section: If you are only using a tag to fix a layout issue (like a margin or padding problem), stick with a <div>.Use headings: A <section> almost always feels "naked" without a heading. If you can't think of a title for that block of content, you might actually need a <div>.Consider alternatives: Before reaching for <section>, ask if the content is self-contained enough to be an <article> (like a blog post) or if it’s just supplementary information for an <aside> (like a sidebar).

---

What does <meta name="viewport"...> do?

If you’ve ever opened a website on your phone and had to "pinch-to-zoom" just to read a single sentence, you’ve experienced a site that forgot its viewport meta tag.

At its core, this tag tells the browser how to adjust the page's dimensions and scaling to fit the screen it's being viewed on. Without it, mobile browsers assume you're looking at a desktop-sized page and try to cram all 1,000+ pixels of width into your tiny phone screen.

The Anatomy of the Tag
The most common implementation looks like this:

<meta name="viewport" content="width=device-width, initial-scale=1.0">

Here is what those specific instructions are actually doing:

width=device-width: This tells the page to match the screen's width in "device-independent pixels." This allows the page to reflow content based on whether you're using an iPhone, a tablet, or a giant monitor.

initial-scale=1.0: This sets the zoom level when the page first loads. 1.0 means "no zoom" (a 1:1 relationship between CSS pixels and device-independent pixels).
