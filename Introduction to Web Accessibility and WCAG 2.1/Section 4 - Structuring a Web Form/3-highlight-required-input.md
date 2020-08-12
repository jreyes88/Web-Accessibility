# Highlight Required Input

The accepted convention to indicate that a user must complete a form field is to use a red asterisk character on the label. However, this approach can be difficult to understand for users who may be unfamiliar with online forms.


The asterisk convention requires explanation before a user encounters it. Since a screen reader user navigates a form via interactive elements, this extra text doesn't receive focus and doesn't get announced. When an interactive element with an asterisk _does_ get announced, it is done like so: "first name star" -- this "star" is announced with no context. Additionally, using a color to identify can be problematic for users with a vision impairment. The asterisk is also a small character, typically smaller than the rest of the font size.


The alternative, accessible approach is to use "(required)" in the form label.

```html

<form>
    <label for="firstname">First Name (required)</label>
    <input type="text" id="firstname" required />
</form>

```


Combine this technique with the constraint information:

```html

<form>
    <label for="birthdate">Date of Birth (dd/mm/yyyy required)</label>
    <input type="date" id="birthdate" required />
</form>

```


However, do _not_ mark up optional fields. This just adds to mental overhead.


## WCAG 2.1 Satisfaction

- **H90:** Indicating required form controls using label or legend
- **3.3.2 Labels or Instructions:** Labels or instructions are provided when content requires user input (level A)


## Summary

- The common approach of indicating mandatory fields using a red asterisk is problematic for accessibility
- The asterisk requires explaining before the user enters the form
- Identifying items by color may impact users with a color visual impairment
- The font size of the asterisk will be difficult to see when it's the same size as the other text
- All of these problems can be addressed by using the word "(required)"
