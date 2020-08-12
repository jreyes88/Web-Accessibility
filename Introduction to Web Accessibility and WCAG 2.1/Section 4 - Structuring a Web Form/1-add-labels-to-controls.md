# Add Labels to Controls

Form controls often have a text label adjacent to the control, which gives the user a hint as to what type of information is required. However, relying only on the physical placement means that screen reader users won't understand what data is required.


When a label receives focus, a screen reader only announces the type of input control, not the adjacent label. The screen reader may announce "input type and text", not that it is for a first name. If a label is not programmatically associated to the control, the label remains unannounced.


Creating a relationship between a `<label>` element and an input control overcomes this issue. The `for` attribute value of the label element uses the `ID` of the form control:

```html

<form>
    <label for="firstname">First Name</label>
    <input type="text" id="firstname" />
</form>

```


The screen reader will now announce the text label for the input requiring control: "first name input type and text".


Not all form controls require an explicitly set label.

The following form controls require a `<label>` element:

- `<input type="text">`
- `<input type="checkbox">`
- `<input type="radio">`
- `<input type="file">`
- `<input type="password">`
- `<textarea>`
- `<select>`


The following form controls **do not** require a `<label>` as the text description is provided by the `value` attribute, `alt` attribute, or content within the element.

- `<submit>` button - text description is provided by the `value` attribute of the control
    + `<input type="submit" value="Submit" />`
- `<reset>` button - text description is provided by the `value` attribute of the control
    + `<input type="reset" value="Reset" />`
- `<img>` button - text description is provided by the `alt` attribute of the control if the image cannot be displayed
    + `<input type="image" alt="search">`
- `<hidden>` input - No label is required as the hidden control does not display
    + `<input type="hidden">`
- `<button>` element - No label is required as the text description is provided by the enclosed text
    + `<button type="button">Add to Basket</button>`


An addition benefit of progammatically associating a label to a form control is that it provides a larger clickable area for the control. Activation can now happen either from the label or the control. This is helpful for users with dexterity issues.


## WCAG 2.1 Satisfaction

- **H44:** Using label elements to associate text labels with form controls
- **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation can be progammatically determined or are available in text (level A)


## Summary

- Progammatically associated labels is a nice quick win to improve the accessibility of online forms
- Associate a label to a form control using the `FOR` and `ID` attributes
- Some form controls require a label and some don't
