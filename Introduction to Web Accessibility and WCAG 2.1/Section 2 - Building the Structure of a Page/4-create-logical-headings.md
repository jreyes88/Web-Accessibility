# Create Logical Headings

Headings are the webpage outline. Users who can see the headings can decide instantly if they wish to continue reading the page due to being able to quickly scan the heading levels.


When a page structure is coded correctly, screen readers and assistive technology users can navigate the webpage by the heading level. Users can list all page headings, jump between heading levels, and even navigate to specific headings.


If headings are used correctly, this ultimately means users understand the structure of the page in a non-visual way.


There are six levels of headings to structure the sections of a webpage. **They don't all need to be used.** Use as many heading levels as is appropriate. Pages should apply headings in a logical order.


- `<h1>heading 1</h1>` - **Master heading**, title of the page, only one per page
- `<h2>heading 2</h2>`
- `<h3>heading 3</h3>`
- `<h4>heading 4</h4>`
- `<h5>heading 5</h5>`
- `<h6>heading 6</h6>`

Each level denotes a subsection of content from the previous parent heading level.


_Example:_ Heading 3 content is the subsection of Heading 2 content, which is a subsection of Heading 1.


Before adding a new heading level, decide if a new level is in fact appropriate. Is new content being introduced or is it a continuation of previous content?


**Heading levels must always be used in sequence, and skipping heading levels must be avoided.**


The _only_ time it is acceptable to skip a heading level is when closing a section.


_Example:_

```html

<!-- H3 Heading Level -->
<h3>Making great products</h3>
<p>We make products in several sizes and to various dimensions. We can also provide different material.</p>

<!-- H4 Heading Level, part of the previous section -->
<h4>Some of the products we make</h4>
<p>Our top selling product is the patented ACME widget, made in durable PVS and available in a range of colours and sizes.</p>
<p>We also produce products on behalf of other companies.</p>

<!-- H2 Heading Level, a new unrelated section is introduced -->
<h2>Who we work with</h2>
<p>We work with many companies large and small. From big multinationals to small suppliers.</p>

```


## WCAG 2.1 Satisfaction

- **H42:** Using h1-h6 to identify headings
- **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text (level A)


## Summary

- Heading elements provide a navigable hierarchy for screen reader and other assistive technology users
- The heading elements must be in sequence otherwise the hierarchy will be difficult to understand
- Use as many heading levels as appropriate for your content
