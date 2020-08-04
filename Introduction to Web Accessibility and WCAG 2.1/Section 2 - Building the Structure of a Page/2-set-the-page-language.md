# Set the Page Language

Pages with a missing language code are usually not a problem if the screen reader and web content language are the same.


However, if the screen reader is set to a language different from the web content, problems arise.


_Example:_ If a screen reader's default language is French and a page is written in UK English and no language is specified, then French language and pronunciation will be used to read English language content, resulting in it being difficult to understand.


A language set on the `lang` attribute on the `<html>` element will affect the whole page content as it's applied globally.


It needs to be set correctly for every page.


The `lang` attribute uses an ISO two-character language code as its value: `<html lang="en">`.


Can include extended character codes for regional and country variants of languages: `<html lang="en-au">`.


The `lang` attribute can be applied to chunks of text where the language is different from the webpage's primary language. Because the `lang` attribute is a global attribute, it can be used on any HTML element.

```html

<html lang="en">

    <div lang="fr">
        <p>Bonjour.</p>
    </div>

</html>


```


## WCAG 2.1 Satisfaction

- **H57:** Using language attributes on the HTML element
- **3.1.1 Language of Page:** The default human language of each web page can be programmatically determined (level A)


## Summary

- Setting the `lang` attribute on the `<html>` element will trigger screen readers and assistive technology to load the correct language profile
- The `lang` attribute value is a two character ISO country code which sets the page language
- Sections within a webpage can have a different language set


## Set the Page Language Links

- [What is the difference between <html lang=“en”> and <html lang=“en-US”>?](https://stackoverflow.com/questions/11318961/what-is-the-difference-between-html-lang-en-and-html-lang-en-us)
- [Language tags in HTML and XML](https://www.w3.org/International/articles/language-tags/)