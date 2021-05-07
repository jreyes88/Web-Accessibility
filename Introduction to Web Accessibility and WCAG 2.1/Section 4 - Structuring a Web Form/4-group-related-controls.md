# Group Related Controls

The way that form controls are grouped together on screen can help enhance understanding of the relationship between those controls. A collection of dropdowns for a date of birth may be be visually understandable when they are adjacent to one another. However, if a user cannot perceive this grouping visually, that user will only hear the labels and it may not be clear how they relate to each other.


Grouping controls together semantically can help a screen reader user understand how components relate to each other. To identify related controls, use the `<fieldset>` and `<legend>` elements, which provide a description for the whole group. This grouping mechanism triggers a screen reader to announce the `<legend>` text before the label text of each control.


```html

<form>
    <fieldset>
        <legend>Date of Birth</legend>

        <label for="day">Day</label>
        <input type="text" id="day" />

        <label for="month">Month</label>
        <input type="text" id="month" />

        <label for="year">Year</label>
        <input type="text" id="year" />
    </fieldset>
</form>

```


The `<legend>` element is the first element within the `<fieldset>` element, and is announced by the screen reader.


Grouping controls is most important for radio buttons and checkboxes. The individual control label may be insufficient to describe the whole group's description.


```html

<form>
    <fieldset>
        <legend>Shipping</legend>

        <label for="standard">Standard</label>
        <input type="radio" name="shipping" id="standard" />

        <label for="priority">Priority</label>
        <input type="radio" name="shipping" id="priority" />

        <label for="threeworkingdays">3 Working Days</label>
        <input type="radio" name="shipping" id="threeworkingdays" />
    </fieldset>
</form>

```


## WCAG 2.1 Satisfaction

- **H71:** Providing a description for groups of form controls using fieldset and legend elements
- **1.3.1 Info and Relationships:** Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text (level A)


## Summary

- `<fieldset>` and `<legend>` elements are a great way to group related controls together
- Grouped controls trigger the screen reader to announce the legend text followed by the control label
- It's best suited to use for checkboxes and radio buttons, where the individual label for each control may be insufficient
