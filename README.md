# Zaid Raza - Personal Resume Website

A responsive personal resume website built with plain HTML5 and CSS3 for an academic web development project (BBA in Digital Business and Entrepreneurship, IIM Bangalore).

## How to open it

1. Keep `index.html` and `style.css` in the same folder.
2. Double-click `index.html`. It opens in any modern browser.

No build step or extra files are needed. Headings and body text use Google Fonts (Young Serif and Hanken Grotesk), loaded by a `<link>` in `index.html`. If you are offline, the site falls back to Georgia and your system fonts and still works.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page structure and content |
| `style.css` | All styling (external stylesheet) |
| `README.md` | This file |

## Design idea

The look is based on indigo-dyed denim and tailoring.

- **Palette:** deep indigo, denim blue, washed-denim light blue and a chalk-white background, with marigold used only for small decorative details (like contrast stitching on a pair of jeans).
- **Ruler marks:** the bottom edge of the header is marked like a tailor's tape, drawn with CSS gradients.
- **Stitching:** dashed lines are used for dividers, the garment-style "quick facts" label, the education timeline and the seam on the dark achievement band.
- **Icons:** the Clothing and textiles and Skateboarding interests have small line icons (inline SVG).

## Page structure

1. Header with wordmark and navigation (About, Experience, Education, Interests, Contact)
2. Introduction: name, short summary, quick-facts label, "How I think about business", and three short columns
3. Experience (three entries, dates and labels on the left, details on the right)
4. Selected achievement
5. Education (ordered list timeline)
6. Interests (two-column grid)
7. Skills and languages (grouped tags)
8. Contact (table with clickable email and phone links)
9. Minimal footer

## Where each concept is used

**HTML**

- Document structure: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
- Semantic elements: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
- Headings and paragraphs: `<h1>` to `<h3>`, `<p>`
- Unordered lists: experience bullets, navigation, skill tags
- Ordered list: education timeline
- Definition list: quick facts
- Table: contact details
- Anchor tags: in-page navigation (`href="#experience"`), `mailto:` and `tel:` links
- Classes and IDs: for example `class="entry"` and `id="experience"`

**CSS**

- Element, class and ID selectors: `p`, `.entry`, `#site-header`
- Combined selectors: `.nav-list a`, `.timeline .entry-body`, `#experience h2, #education h2`
- Pseudo-classes and pseudo-elements: `a:hover`, `.facts div:first-child`, `::before`, `::after`, `::marker`
- Adjacent sibling selector: `.trio-item + .trio-item`
- Typography, colours and fonts: CSS variables on `:root`, serif headings, sans-serif body
- Box model: `padding`, `margin`, `border`, `border-radius`, `outline`, plus `box-sizing: border-box`
- Cascade and specificity: `.section-white` overrides the base `.section` rules because it comes later with equal specificity; ID selectors such as `#site-header` are more specific than class selectors
- Display properties: `display: grid`, `display: flex`, `display: inline-block`
- Positioning: `position: sticky` on the header, `position: absolute` for the ruler marks, timeline dots and skip link, `position: relative` on cards and the dark band
- Flexbox: header layout, navigation, skill tags, footer
- CSS Grid: two-column layouts, hero, three columns, interests grid, experience entries
- Responsive design: media queries at 900px (tablet) and 640px (mobile)

## Customising

- **Colours:** edit the variables at the top of `style.css`.
- **Content:** edit the text in `index.html`. Each section is marked with a comment.
