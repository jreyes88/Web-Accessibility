# Use Inline Error Messages

Inline validation for form controls can be triggered:
- when the control loses focus, such as navigating away
- when the whole form is submitted and returned with errors


Inline error messages must be programmatically associated with the form control, otherwise the error message that is displayed visually online won't be announced by the screen reader.


An accessible inline error message is contained within the label element and is announced as part of the label text.


The addition of the inline error message is extending the accessibility support the control already has to now include an error message.


The error message could be contained in a `<div>` or `<span>` element, and could be hidden by CSS until needed. When the control is in error, the CSS style is removed, making hte message visible and announced by the screen reader when the control is in focus.


```html

<form>
    <label for="firstname">
        First Name
        <span class="hide">First Name is empty</span>
    </label>
    <input type="text" id="firstname" />
</form>

```

While this technique does announce the error message to a screen reader:
- It's only announced as part of the label, which itself is only announced when a control receives focus
- The message won't be announced dynamically when a user tabs to another control


Because of this, an inline error message shouldn't be the only way to describe a control in error. It's a complementary way to indicate an error, which assists users who use a keyboard and screen reader to navigate. Inline error messages are only ever used when combined with other techniques.


## WCAG 2.1 Satisfaction

- **G83:** Providing text descriptions to identify required fields that were not completed
- **SCR32:** Providing client-side validation and adding error text via the DOM
- **3.3.1 Error Identification:** If an input error is automatically detected, the item that is in error is identified and the error is described to the user in text (level A)


## Summary
