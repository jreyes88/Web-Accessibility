# Suggest Corrections

Inline error messages and labels with data formats all help the user to enter correct data. However, when the data provided is incorrect, further assistance can be provided by error message suggestions.


Error message suggestions can be thought of as further nudges or prompts to the user:
- Users with learning difficulties can be provided with extra guidance in the error message, describing what they need to do
- Vision impaired users have further clarity as to the nature of the error
- Users with short term memory impairment will experience less repetition with entering data


## Scenario 1: Missing Required Data

If a mandatory control is left blank, the inline message technique described in [Section 4.5 - Inline Error Messages](https://github.com/jreyes88/Web-Accessibility/blob/main/Introduction%20to%20Web%20Accessibility%20and%20WCAG%202.1/Section%204%20-%20Structuring%20a%20Web%20Form/5-use-inline-error-messages.md) can be extended to provide information that the control cannot be left blank, and requires data.


Try to use natural sounding wording for this, such as "This cannot be blank."


## Scenario 2: Incorrect Data Format

Any specific formatting requirement must be conveyed in the error message. Describe the data format requirement in the control's label, and make sure it is repeated in the error message. Also explain why the value was rejected as well as the correct format.

```html

<form>
    <label for="dob">
        Date of birth (dd/mm/yyyy)
        <span class="hidden">Incorrect format, the required format is dd/mm/yyyy</span>
    </label>
    <input type="text" id="dob" />
</form>

```


## Scenario 3: Limited Responses

When the information provided by a user is one of a limited set of values, ensure that the error message conveys this, explaining why the value was rejected, and the limited number of allowable responses.


```html

<form>
    <label for="quantity">
        Number of Items to Buy (max 4 items per customer)
        <span class="hidden">Incorrect value. Values 1 to 4 only are allowed.</span>
    </label>
    <input type="number" id="quantity" />
</form>

```


## WCAG 2.1 Satisfaction

- **G83:** Providing text descriptions to identify required fields that were not completed
- **G85:** Providing a text description when user input falls outside the required format or values
- **G177:** Providing suggested correction text
- **G84:** Providing a text description when the user provides information that is not in the list of allowed values
- **3.3.3 Error Suggestion:** If an input error is automatically detected and suggestions for correction are known, then the suggestions are provided to the user, unless it would jeopardize the security or purpose of the content (level AA)


## Summary

- Suggested corrective error messages are another way to reduce the user encountering repeated errors
- Error messages should indicate there has been a problem
- Explain why the problem has a occurred
- If the situation allows, suggest a correction
