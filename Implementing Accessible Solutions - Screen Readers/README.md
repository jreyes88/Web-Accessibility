# Implementing Accessible Solutions: Screen Readers

## Presenter

- Alicia Evans (she/her/hers)
    - [alicia@knowbility.org](mailto:alicia@knowbility.org)
    - [linkedin.com/in/aliciaadamsevans/](https://linkedin.com/in/aliciaadamsevans/)


## This Presentation *Is*

- A deeper dive into a few techniques you can use for website accessibility when you leave this webinar
- Focused on screen reader accessibility


## This Presentation *Is Not*

- A complete education on how to make websites accessible
- Focused on other access needs or assistive technologies beyond screen readers


## Agenda

- Screen Readers
    + What Are Screen Readers?
    + Who Uses Screen Readers?
- Accessible Names
    + What's An Accessible Name?
- Accessibility Pane in Developer Tools
- All Examples on CodePen
- HTML
    + Image with Alt Attribute
    + Links
    + Inputs
- ARIA
    + `aria-label`
    + `aria-labelledby`
    + Accessible Description & `aria-describedby`
- Hiding and Revealing Content
    + CSS and Screen Reader Accessibility
    + Visually-Hidden Text Examples
    + `aria-hidden`
- The First Rule of ARIA
    + You *Can* Make an ARIA Button (But Shouldn't)


## Screen Readers

### What Are Screen Readers?

"A **Screen Reader** is a form of assistive technology (AT) that renders text and image content as speech or braille output."
- Wikipedia Definition


### Who Uses Screen Readers?

People who:
- Are blind
- Are deafblind
- Have low vision
- Have cognitive or learning disabilities
    + Dyslexia
- Have temporary disabilities
- Would rather listen than read


## Accessible Names

### What's An Accessible Name?

The **Accessible Name** is the name that assistive technologies communicate to users to identify an element. How does this work on the web?

1. Code
2. Browser renders/interprets the code
3. Operating System (OS) uses Accessibility API to communicate that interpretation
4. Screen Reader announces to users


[W3 Article on Accessible Name Computation](https://w3.org/TR/accname-1.1)


## Accessibility Pane in Developer Tools

- Right Click > Inspect an Element
    + Highlight HTML Element
- Accessibility Tab on the right pane (may need to arrow over `>>`)
- Accessibility Tree
    + Example: `img "[alt value]"`
    + Computed Properties
        * alt: provided by `alt` attribute
        * the naming options presented are a hierarchy.
            - Higher up takes precedence over lower options
- `alt=""`
    + Accessibility Tree will say "ignored"
    + Tells Assistive Technology to ignore the element
- No `alt` attribute
    + Accessibility Tree will show and announce that an image is present, but no label, name, or title
    + This is inaccessible


**ARIA Naming Options are a Hierarchy**. ARIA will overwrite the `alt` attribute text.


## All Examples on CodePen

[https://codepen.io/collection/XkKOaW](https://codepen.io/collection/XkKOaW)


## HTML

### Image with Alt Attribute

- [https://codepen.io/team/Knowbility/pen/BaLXxWa](https://codepen.io/team/Knowbility/pen/BaLXxWa)


### Links

- Basic Link Example
    + [https://codepen.io/team/Knowbility/pen/JjbweEE](https://codepen.io/team/Knowbility/pen/JjbweEE)
    + With no title or anything, Accessibility Tree will take the link text as the title
- Image Link Example
    + [https://codepen.io/team/Knowbility/pen/poEQgeJ](https://codepen.io/team/Knowbility/pen/poEQgeJ)
    + It's important to make a linked image's `alt` attribute the destination of the link
    + Accessibility Tree accepts the `alt` attribute for the name contents
    + "Knowbility" vs. "Knowbility Homepage" in `alt` attribute -- either can go. Within a navigation area, the user most likely understands the context that the link will go to the homepage.


### Inputs

- Input Missing Programmatic Label
    + [https://codepen.io/team/Knowbility/pen/MWjdvpV](https://codepen.io/team/Knowbility/pen/MWjdvpV)
- Input Label Programmatically Associated
    + [https://codepen.io/team/Knowbility/pen/vYXwJmO](https://codepen.io/team/Knowbility/pen/vYXwJmO)
- Placeholders
    + The `placeholder` attribute is not adequate to use alone. It *may* be announced, but it can disappear when the input receives focus. Might work for screen reader users, but not for people with short term memory issues. Similarly `title` attribute doesn't work the same as a `label` element


## ARIA

ARIA stands for **Accessible Rich Internet Applications**.


WAI-ARIA, the Accessible Rich Internet Applications, defines a way to make Web content and Web apps more accessible to people with disabilities. It especially helps with dynamic content and advanced user interface controls developed with HTML, JavaScript, and related technologies.


This is for things that don't have native HTML solutions.


### `aria-label`

- One way to provide an accessible name
- Use it when there is not visible text available for an element
- Does not work consistently on all elements (like `<div>` or `<span>`)
- Will overwrite content - use with extreme caution!
    + Higher in Accessibility Tree hierarchy
- Spell things correctly, not phonetically
- Format: `aria-label="value"`


#### `aria-label` Examples

- Button that uses SVG as visual Label
    + [https://codepen.io/team/Knowbility/pen/xxENrBJ](https://codepen.io/team/Knowbility/pen/xxENrBJ)
- Close buttons, hamburger/menu buttons, options, buttons, etc.
- Differentiate landmarks
    + What do you do if you have multiple `<nav>` elements?
    + Can distinguish by having one labeled "main" and another labeled "breadcrumb"
    + [https://codepen.io/team/Knowbility/pen/vYyvMGv](https://codepen.io/team/Knowbility/pen/vYyvMGv)


### `aria-labelledby`

- Use to associate visible text with the element
- Does not work consistently on all elements (like `<div>` or `<span>`)
- Will overwrite content - use with extreme caution!
    + Higher in Accessibility Tree hierarchy
- format: `aria-labelledby="id1 id2 id3"` - space separated id values


#### `aria-labelledby` Examples

- Add Delivery Address
    + [https://www.w3.org/TR/wai-aria-practices/examples/dialog-modal/dialog.html](https://www.w3.org/TR/wai-aria-practices/examples/dialog-modal/dialog.html)
- Read More Link
    + [https://codepen.io/team/Knowbility/pen/oNYJOMm](https://codepen.io/team/Knowbility/pen/oNYJOMm)


### Accessible Description & `aria-describedby`

- An **Accessible Description** provides additional information, related to an interface element, that complements the accessible name. The accessible description might or might not be visually perceivable
- `aria-describedby` is one way to provide an accessible description
- Does not work consistently on all elements (like `<div>` or `<span>`)
- Format: `aria-describedby="id1 id2 id3"`
- [https://www.w3.org/TR/accname-1.1/#dfn-accessible-description](https://www.w3.org/TR/accname-1.1/#dfn-accessible-description)


#### `aria-describedby` Examples

- Form field instructions
    + [https://codepen.io/team/Knowbility/pen/RwoEmXg](https://codepen.io/team/Knowbility/pen/RwoEmXg)
    + "Password must be at least 8 characters"
- Other important information to know when interacting with an element
- Applications (`role="application"`)
    + You should not use this frequently
- Individual error messages


## Hiding and Revealing Content

### CSS and Screen Reader Accessibility

- Use `display: none` or `visibility: hidden` to hide content that should be hidden from everyone. Don't rely on opacity, hiding off-screen, or clipped text if the content should be hidden for all users
- Use a `"visually-hidden"` or similar class to hide content visually that adds context for screen reader users
- [How to Hide Content](https://www.a11yproject.com/posts/2013-01-11-how-to-hide-content)


### Visually-Hidden Text Examples

- Strikethrough
    + [https://codepen.io/team/Knowbility/pen/jOVXoEG](https://codepen.io/team/Knowbility/pen/jOVXoEG)
- Context to links
    + [https://codepen.io/team/Knowbility/pen/XWNowVQ](https://codepen.io/team/Knowbility/pen/XWNowVQ)
- Context for buttons
- Skip links (until they receive focus)
- Headings


### `aria-hidden`

- Use `aria-hidden` when content should be visible on the page but hidden from assistive technologies
- Use `aria-hidden` with `opacity: 0` (for animations, for example)
- There are some ways to hide content with native HTML, example `alt=""`
- Never use it on focusable content
- Always remember to remove it if content should be perceived again
- Format: `aria-hidden="true"`


#### `aria-hidden` Example

- `aria-hidden` Unicode characters
    + https://codepen.io/team/Knowbility/pen/YzpBxVR


## First Rule of ARIA

Don't use ARIA if there's a native HTML solution.


### You *Can* Make an ARIA Button (But Shouldn't)

- ARIA Button
    + [https://codepen.io/team/Knowbility/pen/MWbLEqz](https://codepen.io/team/Knowbility/pen/MWbLEqz)
- `role="button"`
- `tabindex="0"`
- Enter and Spacebar key event listeners
- Prevent default when Spacebar is pressed
- Include CSS custom focus styles
