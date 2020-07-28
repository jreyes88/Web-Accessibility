# Bypass Repeating Content

Links, navigation components, and search bars are all typically found at the top of a webpage. Each one of these components may have several tab positions.


Where sighted users who can use a mouse can navigate in a non-linear way and skip these components, screen reader and keyboard users aren't able to, and are at a huge disadvantage where they must navigate the page linearly by pressing the tab key to advance to the next link or form control.


## Skip Links/Bypass Blocks

Skip links or bypass blocks are a mechanism which allow a user to avoid, or bypass, repeating page content easily.


The bypass block can be used to avoid repeating page content and move the user's keyboard focus onto a named region further down in the page.


A bypass block at a minimum must include a skip to content link. This link skips to the main content on the page using an in-page anchor.


_Example:_

```html

<html lang="en-us">
    <head>
        <title>Homepage</title>
    </head>
    <body>
        <!-- Here is the skip to content link -->
        <div id="skiplink">
            <a href="#main-content">Skip to Main Content</a>
        </div>
        <nav>
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/about">About Us</a></li>
            </ul>
        </nav>

        <!-- Here is the in-page anchor -->
        <div id="main-content">
            <h1>Main Content</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima et, sapiente assumenda alias deleniti at veritatis consequatur aut. Qui quasi culpa omnis vero, rerum! Atque similique magni quasi, temporibus nisi.</p>
        </div>

        <footer>
            &copy; 2020
        </footer>
    </body>
</html>

```

Skip links can also be added for navigating anywhere on the page, such as to a newsletter signup section or a footer section. **However, try and limit skip links to three links or fewer.** Anything more than that and the feature decreases in utility.


## Removing from Page Flow Unless Keyboard Navigation is Used

For situations where a skip link may look out of place, a visually hidden CSS style can be applied which renders the link visible only when in focus.


This works well for all users because:
- Keyboard users will see the link only when it receives keyboard focus
- Screen reader users will hear the link
- Mouse users won't see any change in how they navigate the page


The skip links are contained in a `<div></div>` element with an ID of "skiplink":


```html

<div id="skiplink">
    <a href="#main-content">Skip to Main Content</a>
</div>

```


The link within this `<div></div>` element are given off screen positioning with height and width properties set to 1px.

The CSS pseudo-class `:focus` allows styling to be applied when the element receives focus:


```css

#skiplink a {
    position: absolute;
    left: -10000px;
    top: auto;
    width: 1px;
    height: 1px;
    overflow: hidden;
}

#skiplink a:focus {
    position: static;
    width: auto;
    height: auto;
}

```


## WCAG 2.1 Satisfaction

- **G1:** Adding a link at the top of each page that goes directly to the main content area
- **G124:** Adding links at the top of the page to each area of content
- **2.4.1 Bypass Blocks:** A mechanism is available to bypass blocks of content that are repeated on multiple web pages (level A)


## Summary

- Bypass blocks can be used to reduce a user's keystrokes by bypassing repeating page content
- Skip links must have at a minimum a link named "Skip to main content"
- CSS can be used to make skip links visible only when in focus


## Bypass Repeating Content

- [CANAXESS Homepage (tab through the page to see the skiplinks revealed)](https://www.canaxess.com.au/)