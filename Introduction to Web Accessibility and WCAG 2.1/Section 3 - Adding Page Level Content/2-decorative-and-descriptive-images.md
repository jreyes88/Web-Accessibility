# Decorative & Descriptive Images


**Rule 1: Ensure every image has an `ALT` attribute.**


When an image has no `ALT` attribute it means a text description (if required) can't be provided. A screen reader uses the value of the `ALT` attribute of the image element to provide a text description for the user.


If an image has no `ALT` attribute, the screen reader will announce "image". The user is aware that an image is there, it maybe relevant, it may not be, but they are left uncertain


_Example:_ `<img src="someimg.png" alt="" />`


For an image of a boat, appropriate `ALT` text could be "boat". While this is technically correct, adding such succinct `ALT` text isn't really in the spirit of web accessibility. What is the image describing, why is it relevant, what does it show?


Apply a richness to the description when adding `ALT` text.


_Example:_ `<img src="boat.png" alt="boat sailing under Sydney Harbour bridge on a sunny morning." />`


Avoid overly verbose descriptions as well. `ALT` text of the length of a sentence is probably the upper limit. Just use enough text to describe what the image is showing.


**Rule 2: Descriptive images require `ALT` text, decorative images don't.**


Unless an image is crucial for a user to understand, set the `ALT` attribute to null:

- When an image is decorative and doesn't require an explanation, use blank `ALT` text
- The image still has the `ALT` attribute, but it has no value
- Using null `ALT` text means the screen reader will ignore the image


_Example:_ `<img src="decorative-image.png" alt="" />`


## WCAG 2.1 Satisfaction

- **H37:** Using `ALT` attributes on img elements
- **G82:** Providing a text alternative that identifies the purpose of the non-text content
- **1.1.1 Non-text Content:** All non-text content that is presented to the user has a text alternative that serves the equivalent purpose (level A)


## Summary

- The screen reader uses the `ALT` text to provide a text description of an image
- To hide a decorative image set the `ALT` attribute value to null
- All images require `ALT` attributes
- Some images require `ALT` text