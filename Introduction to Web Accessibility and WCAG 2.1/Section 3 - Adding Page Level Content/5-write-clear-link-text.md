# Write Clear Link Text

A screen reader audibly announces the text and labels of links and other interactive elements of a web page when tabbing through with a keyboard.


The following works for a visual user to understand the context of the link:

```html

<p><a href="#fashion-trends">Click here</a> for today's fashion trends</p>

```

While the relationship between the link and surrounding text is established visually, a screen reader will not gather this context between the link and its proximity to other text. The user might just hear "Click here", so it can be difficult to understand the destination of the link.


Unclear link text has a straightforward solution: **Use clear link text.** Screen reader users navigate via page links, so it is vital to provide link text which is understandable when read on its own.


The following would be a better example of clear link text:

```html

<p><a href="#fashion-trends">Click here for today's fashion trends</a></p>

```

You can also remove redundant text. Screen readers will often identify a link and add the word "clickable" to the audible description.


Link which begin "click here" are difficult to navigate using the links or elements list in a screen reader, which is a window which lists all links on a page separately in the screen reading software. All of the page links are listed alphabetically, so a user has to listen to each link in full to determine of the link is what they want to activate by hearing the last unique part of the link text.


Hearing link text spoken is a great way to determine if text is understandable on its own.


## WCAG 2.1 Satisfaction

- **H30:** Providing link text that describes the purpose of a link for anchor elements
- **2.4.8 Link Purpose (Link Only):** A mechanism is available to allow the purpose of each link to be identified from link text alone, except where the purpose of the link would be ambiguous to users in general (level AAA)


## Summary

- Unclear link text can make it difficult for screen reader users to navigate a website in a non-visual way
- Use clear link text
- The best way to determine if the link text chose in is clear by reading aloud