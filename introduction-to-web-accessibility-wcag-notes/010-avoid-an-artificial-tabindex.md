# Avoid an Artificial TabIndex

Every tab key press advances the screen focus one position to the right, onto the next interactive element.


Links and form controls have an implied focus and receive screen focus in the order they're laid out on screen.


The `tabindex` attribute can be used to reorder the sequence in which interactive elements receive focus.


The `tabindex` attribute accepts three possible values:
- `tabindex="-1"`
- `tabindex="0"`
- `tabindex="1"` and above


**A positive `tabindex` value will bring negative outcomes.**


## `tabindex="-1"`

Adding `tabindex="-1"` to any element removes it from the document's tab order and renders it unfocusable from the keyboard.


Elements with `tabindex="-1"` are still displayed to the screen, so nothing visually changes.


However, when navigating via the keyboard, these elements which should be natively focusable from the keyboard are now ignored.


_Example:_

```html

<a href="page2.html" tabindex="-1">Page two</a>

```


### Uses for `tabindex="-1"`

Links in a hamburger menu are hidden in a pop out menu, so they aren't required to be focusable until the menu is shown.


When the menu is shown, the menu items' `tabindex` is set to `0`, so they items become focusable.


## `tabindex="0"`

`tabindex="0"` will allow a component to become focusable as part of the document's natural tab sequence.


Native HTML elements provide this behavior as standard and the attribute isn't required.


Adding this attribute won't change anything to ordinarily focusable elements.


_Example:_

```html

<a href="page2.html" tabindex="0">Page two</a>

```


### Uses for `tabindex="0"`

`tabindex="0"` is used when custom components are developed. Custom components are page components constructed with `<div></div>` and `<span></span>` elements, which don't receive keyboard focus natively.


Adding `tabindex="0"` fixes this, making the component keyboard focusable in the order laid out on screen.


_Example:_

```html

<div tabindex="0">Custom Component Code</div>

```


## `tabindex="1"` and Above

**This is the problem value.**


A `tabindex` value of `1` or above repurposes the element's natural `tabindex` ordering.


Elements with a `tabindex="1"` and above take focus precedence when the tab key is pressed.


The visual layout of elements will not match the tab order.


_Example:_

```html

<a href="page2.html" tabindex="1">Page two</a>

```


## Uses for `tabindex="1"` and Above

It's best to avoid `tabindex="1"` or above. Unless used _very carefully_ it can end up making a page really difficult to understand and navigate around.


## WCAG 2.1 Satisfaction

- **G59:** Placing the interactive elements in an order that follows sequences and relationships within the content
- **H4:** Creating a logical tab order through links, form controls, and objects
- **2.4.3 Focus Order:** If a web page can be navigated sequentially and the navigation sequences affect meaning or operation, focusable components receive focus in an order that preserves meaning and operability (level A)


## Summary

- The `tabindex` attribute and values can have a big impact on the tab ordering sequence of a page
- The only values which should be used are `-1` and `0`
- `tabindex` values of `1` and above can result in a page's focus order being different from its visual order
