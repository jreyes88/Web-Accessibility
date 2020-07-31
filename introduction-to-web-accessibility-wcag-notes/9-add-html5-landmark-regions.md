# Add HTML5 Landmark Regions

HTML traditionally lacked a way to provide structure to different regions of a page. `<div></div>` and `<span></span>` elements could be marked up with names such as nav, header, or footer to apply styles onto.


HTNL5 landmarks mean areas can be marked up consistently, and structural information is exposed to screan readers. These landmarks only provide a benefit for screen reader users. There is no visible change to the way the page renders.


The most importan HTML5 landmark regions are:
- `<header></header>`
- `<footer></footer>`
- `<main></main>`
- `<article></article>`
- `<nav></nav>`


They act as containers for content.


## `<header></header>` and `<footer></footer>`

### `<header></header>`

- The location for page or content header
- May also contain company-specific branding or a logo


### `<footer></footer>`

- Contains non-primary navigation links


`<header></header>` and `<footer></footer>` can be added to anywhere it's appropriate to have a header or footer, including modal dialogues and within sections.


## `<main></main>`

- Describes the part of the webpage which has prominent content
- Cannot be nested inside `<article>` region
- There can only be one `<main></main>` region per page


## `<article></article>`

- Represents a complete piece of content that could stand alone without the rest of the website
- Most appropriate for content which could be syndicated
- Each `<article></article>` can include `<header></header>` and `<footer></footer>` elements
- Can nest many sub `<article></article>` elements
- Can be nested in other landmark regions


## `<nav></nav>`

- Groups "major navigation links" together
- This could be:
    + Several related links which navigate to different pages
    + A table of contents
    + Previous and next links


## WCAG 2.1 Satisfaction

-  **G115:** Using semanting elements to mark up structure
-  **H97:** Grouping related links using the nav element
-  **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation and can be programmatically determined or are available in text (level A)
