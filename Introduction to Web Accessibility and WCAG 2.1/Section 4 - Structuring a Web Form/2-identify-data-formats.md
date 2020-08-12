# Identify Data Formats

Input controls normally have contraints for the data being entered. There may be a length requirement or the data may need to be entered in a particular sequence. Feedback for errors of this sort is typically conveyed visually, but these visual cues will be unknown to screen reader users.


To help the user understand the format of data being entered and reduce the occurrence of errors, the extra constraint information must be provided up-front in the label.

```html

<form>
    <label for="firstname">First Name (20 character maximum)</label>
    <input type="text" id="firstname" />
</form>

```


The above allows the constraint to be communicated: "first name twenty character maximum input type and text".


Provide the constraint in parenthesis. For example, for the date of birth format:

```html

<form>
    <label for="birthdate">Date of Birth (dd/mm/yyyy)</label>
    <input type="date" id="birthdate" />
</form>

```


Describe all constraints. All users benefit from knowing how data should be entered. However, keep the constraint description succinct.


## WCAG 2.1 Satisfaction

- **G89:** Providing expected data format and example
- **3.2.2 Labels or Instructions:** Labels or instructions are provided when content requires user input (level A)


## Summary

- Formatting and constraint information can be added to enhance an input control label
- The first example described data length
- The second example described the data format
- Adding constraint information into a control's label can act as a nudge and help reduce avoidable errors
