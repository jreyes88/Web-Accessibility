# How to Assess Web Accessibility

Every guideline in POUR principles has:
- Several success criteria
- Sufficient techniques
- (Sometimes) Failure criteria - ways in which content can be tested to determine if it passes WCAG 2.1 conformance


Each failure criterion includes:
- Details about the failure
- An example of a failure
- Single statement tests with an expected result


Running the test against your own content can determine if it meets the criteria of passing.


## Example of Failure Criterion

**2.4.7 Focus Visible Level AA** - Any keyboard operable user interface has a mode of operation where the keyboard focus indicator is visible.
- F55: Failure of Success Criteria 2.1.1, 2.4.7, and 3.2.1 due to using script to remove focus when focus is received
- F78: Failure of Success Criterion 2.4.7 due to styling of element outlines and borders in a way that removes or renders non-visible the visible focus indicator


This failure boils down to:
- Hiding the focus with CSS
- Having a default styling around elements which is visually similar to in focus elements
- Applying a focus effect which obscures the screen focus


Tests:
1. Set the focus to all focusable elements on a page using the keyboard
2. Check that the focus indicator is visible


Expected Results:
- The focus indicator is visible
- If the result is confirmed in your own tests, the criterion has been passed


## When Failure Criterion Is Not Provided

Some tests do no provide failure criteria. Instead, use the tests from any of the sufficient techniques applied.

_Example_: **2.4.6 Headings and Labels Level AA** does not provide failure criteria.
- G130: Providing Descriptive Headings
    1. Determine of the webpage contains headings
    2. Check that each heading identifies its section of the content


Unfortunately, this leaves room for ambiguity:
- _What are sections of content?_
- _Is the heading text clear and understandable?_


Tests must not be carried out in isolation either. Think of each test as one of series of tests that components must undergo.


## Summary

- Failure criteria are clearly defined ways to test content against failures
- When failure criteria don't exist, check the test within each sufficient technique
- Failure criteria check the outcome of applying success criteria
- Tests within sufficient techniques test whether the sufficient technique has been applied correctly


## How to Assess Web Accessibility Links

- [F78 Failure Criterion](https://www.w3.org/WAI/WCAG21/Techniques/failures/F78.html)