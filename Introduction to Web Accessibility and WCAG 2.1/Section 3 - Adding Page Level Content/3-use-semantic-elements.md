# Use Semantic Elements

Semantic elements provide structure to content and makes it easier for assistive technology users to understand.


Semantic elements may trigger the screen reader to use a different intonation when reading italicized text, or announce the heading level when reading a heading.


Semantic heading elements structure web page content, and allow a screen reader to navigate between heading levels and understand the structure and hierarchy of a page in a non-visual way.


Semantic elements provide meaning to content. They can be used for wayfinding and navigating a page hierarchy, or provide context for web content.


The most comment semantic elements to use are:

- `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>`
- `<ol>, <ul>`
- `<blockquote>, <em>`
- `<header>, <footer>, <main>, <article>, <nav>`
- `<time>`


## Heading Elements

Heading elements structure a page and allow a user to navigate the page hierarchy via the keyboard. Because they help users navigate a hierarchy, they must be used correctly:

- Only one `<h1>` heading per page
- Use only as many heading as is required
- Don't skip heading levels


For more information on this, please see [Section 2.4 - Create Logical Headings](https://github.com/jreyes88/Web-Accessibility/blob/main/Introduction%20to%20Web%20Accessibility%20and%20WCAG%202.1/Section%202%20-%20Building%20the%20Structure%20of%20a%20Page/4-create-logical-headings.md).


## Lists

Lists provide a way to group related information together. The screen reader announces the total number of items followed by each item.


If the list is **unordered** `<ul>` the screen reader will announce bullet item followed by the item.


_Example:_ 


```html

<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
</ul>

// Screen reader: "bullet item one"

```


If the list is **ordered** `<ol>` the screen reader will announce the position of the item within the list followed by the item.


```html

<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
</ol>

// Screen reader: "one item one"

```


## Blockquote

The `<blockquote>` is used to indicate a long quotation. The opening and closing tags surround the quotable content.


An optional `cite` attribute is used to identify the source of the quote.


The element `<cite>` can be used within the blockquote.


_Example:_

```html

<blockquote cite="www.ACME.com/message.">
    We've perfected makin great outfits for everyone.
    <cite>ACME fashion house directors message</cite>
</blockquote>

```


## Emphasis

The `<em>` element is used on content where it is required to stress emphasis on a word or phrase. The placement of this emphasis can change the meaning of the sentence.


_Examples:_

Compare the following:

```html

<p>Cars are fast.</p> // No emphasis

<p>Cars <em>are</em> fast.</p> // Could be in response to someone saying cars aren't fast.

<p><em>Cars</em> are fast.</p> // Could be in response to saying something other than cars are fast.

```


## Time

The `<time>` element allows content which displays a date, time, or duration to marked up via the ISO 8601 standard.


While people can understand dates and times in any number of ways, machines can't. The `<time>` element is a consistent and unambiguous way to provide dates and times, which means assistive technologies will reliably read it as it's presented in a machine-readable format.


The element has a mandatory attribute of `datetime`. The format chosen must match the text description, i.e. no attribute of March 3 paired with text of June 3.


_Example:_

```html

<time datetime="2020-03-03">March 3</time>

```


## Code Legibility

Aside from accessibility, using semantic elements means your code is much clearer to read. With semantic elements, we have clearly defined structures which describe the content in a readable way.


## WCAG 2.1 Satisfaction

- **G115:** Using semantic elements to mark-up structure
- **H49:** Using semantic markup to mark emphasized or special text
- **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text (level A)


## Summary

- Semantic elements provide meaning to content
- Content which is structured can be used for wayfinding and hierarchy navigation
- Using semantic elements improves the readability of code