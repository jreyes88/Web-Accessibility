# Add Keyboard and Mouse Focus

Some users may prefer to use a keyboard to navigate a website. We need to ensure we cater for users navigating via the keyboard and apply a screen focus effect.


Without a clear focus indicator, it becomes a guessing game of what element is in focus, and a trial-and-error effort of tabbing around to try to discern what interactive element is currently selected.


The default browser caret focus helps, but is often difficult to identify (it may be a faint dotted line), and varies from browser to browser.


Relying on a change of color alone means it can be dfificult to identify with a color vision impairment. Additional style must be applied to mouse hover and keyboard tab events. This could be underlined text or a prominent border.


A good principle to apply that achieves consistency is that if a promiment focus effect is applied by mouse focus, this same effect should be applied by keyboard focus.


The following is an example that achieves this consistency as well as provides multiple visual emphases across mouse and keyboard focus.


```css

a:focus, a:hover {
    text-decoration: underline;
    border: 4px solid #08495F;

}

```


## Form Controls

Form controls are different from links with how focus is applied. There isn't just one element to target in the CSS, there are several.


```css

input:focus, select:focus, textarea:focus, button:focus, input:hover, select:hover; textarea:hover, button:hover {

}

```


The focus effect is different as well. The underline property doesn't work as you need to underline the text within the input, not the input itself, and even so this can be visually confusing. Instead, the following is an accepted convention for an input:

```css

input:focus, select:focus, textarea:focus, button:focus, input:hover, select:hover; textarea:hover, button:hover {
    border: 4px solid #08495F;
}

```


## WCAG 2.1 Satisfaction

- **C15:** Using CSS to change the presentation of a user interface component when it receives focus
- **2.4.7 Focus Visible:** Any keyboard operable user interface has a mode of operation where the keyboard focus indicator is visible (level AA)


## Summary

- Navigating a website via the keyboard becomes difficult without a clear focus style
- All keyboard accessible elements on a page must have a distinct focus effect when they receive keyboard focus
- This must be applied consistently with the mouse hover focus state