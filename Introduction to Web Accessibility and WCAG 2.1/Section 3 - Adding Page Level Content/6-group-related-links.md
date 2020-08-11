# Group Related Links

Screen reader users navigate websites in a non-visual way. Links arranged visually need to be marked up to induce the screen reader to provide extra helpful information. The meaning of what these links mean can become confusing without this screen reader hint.


`<ul>` and `<ol>` elements can be used to trigger the screen reader to announce:
- Type of list (ordered or unordered)
- The number of items in the list
- Whether the list is bulleted or numbered


The behavior is dependent on the assistive technology.


Use the technique carefully and apply it only when necessary. Announcing the list type and element position adds to the audible overhead a screen reader has to understand. It can be fatiquing to hear.


You need to make a judgment call:
- Does the collection of links require grouping into list elements?
- Does providing list metadata provide helpful information to the user, helping them understand the relationship of the contained links?
- Or is it providing unnecessary noise?


## WCAG 2.1 Satisfaction

- **H48:** Using ol, ul, and dl for lists or groups of links
- **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text (level A)


## Summary

- List elements provide extra metadata for screen reader users
- This metadata helps a user understand the list
- Grouping related links together should not be overused due to the extra noise produced
