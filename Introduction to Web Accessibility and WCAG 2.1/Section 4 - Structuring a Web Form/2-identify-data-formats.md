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
