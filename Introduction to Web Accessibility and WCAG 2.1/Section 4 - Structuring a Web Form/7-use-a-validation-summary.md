# Use a Validation Summary

A validation summary is a summary of all errors on the form. Along with inline errors, it is a complementary way to provide error identification. It is a region above the form indicating errors have occurred, and identifying which controls are in error.


Use list elements to group errors. This means the number of items will be announced by the screen reader:


```html

<h2 id="validationsummary">Errors have occurred</h2>
<ul>
    <li>First name is blank</li>
    <li>Last name is blank</li>
    <li>Address is blank</li>
</ul>

```


The validation summary uses additional styling to draw focus to the in-error region:
- Prominent color
- Heading element
- Bold text
- Full or partial border


In traditional websites, the page is sent to the server to be validated. If errors have been identified, the page is returned with the validation summary and inline error messages visible. However, when the page is reset, the user's focus is lost and is moved back to the top of the screen.


The lost user focus can be fixed by appending the hash (#) character in the returned URL. The hash triggers the screen focus to navigate to in-page named regions. This can automatically redirect the user to the validation summary region when the page is returned.


## WCAG 2.1 Satisfaction

- **Advisory:** Re-displaying a form with a summary of errors
- **3.3.1 Error Identification:** If an input error is automatically detected and suggestions for correction are known, then the suggestions are provided to the user, unless it would jeopardize the security or purpose of the content (level A)


## Summary

- Without a validation summary, a user has to navigate through form controls to determine if any are in error
- Validation summary regions are an additional cue which can help users understand form errors
- They are a complementary technique to using inline errors and provide a convenient central location for grouping all errors together
