# Screen Readers in the Wild

## Panel

- Becky Gibson
    + Host
    + 30+ years at IBM as a developer
    + 20+ years focusing on accessibility
    + W3C contributor - WCAG, ARIA, APA
    + Passionate about making Web usable for all
- Emily Lewis
    + Moderator
- Anthony Vasquez
    + Teaches journalism at Cal State Long Beach
    + MA in East Asian Studies
    + Degrees in Journalism and Chinese Studies
    + Blind and uses screen readers and braille devices on desktop and mobile
- Su Park
    + Pursing a degree in Computer Science
    + Interested in transitioning to Information Security
    + Native screen reader user and experienced accessibility tester


## Agenda

- Overview of Screen Readers
- Demos
- Review of Common Issues
    + Headers
    + Alt Text
    + Labels
    + Control Type
- Mobile Overview
- Mobile Demo
- Q&A


## Overview of Screen Readers

### A11y - Numeronym

- Numeronym
- Accessibility
- Some people argue that numeronyms are not truly accessible


### WCAG

- Web Content Accessibility Guidelines


### Screen Reader Definition

"A screen reader is a form of assistive technology (AT) that renders text and image content as speech or braille output. Screen readers are essential to people who are blind, and are useful to people who are visually impaired, illiterate, or have a learning disability."

\- Wikipedia Definition


## Screen Reader "Requirements"

- Headings
- Labeled buttons and links
- Skip links
- Alternative text for images


### Headings

- Provide structure to the page
- Navigate by headings
    + Generally one heading level 1 (`<h1></h1>`) per page
- Must be coded properly


### Buttons and Links

- Labeled properly 
- Buttons are for action
- Links are for navigating


### Alternative Text

- Alt text
- Describes important images
- Ignores decorative images


### Skip Link

- Quickly navigate to the main region of the page
- First item on the page
- Best if it's a visible link


## Demo - Screen Reader YouTube with JAWS

**Video:** [Navigating YouTube Playlist with JAWS](https://vimeo.com/502344993/f8938fe260)

- Headings
    + Went from `<h1>` to `<h3>`
    + Not necessarily a WCAG failure since it was still heirarchical
- Buttons and Links
    + These were all well-labeled
    + Also had shortcut key which added extra text for the screen reader
- Alt Text
    + Thumbnails were marked as decorative
    + These should have alt text so the screen reader user hears the length of the video
- Skip Link
    + There is one on YouTube before the search bar


## Demo - Google Search with NVDA

**Video:** [Navigating Google Search with NVDA](https://knowbility.org/blog/2019/skip-links/)

- Very good heading heirarchy
- Some headers hidden visually but still present for screen readers' benefit


## Demo - See's Candy with NVDA

**Video:** [Navigating See's Candies with NVDA](https://knowbility.org/blog/2019/skip-links/)

- Increase and Decrease buttons were mislabeled
- Status Messages Not Spoken
    + "Your box is 90% full" - this update did not get read out
    + This would be a WCAG failure

## Takeaways

- If more than one `<nav>` on a page, add ARIA labels


## Demo - iOS Coffee Bean App with Voiceover

**Video:** [iOS Coffee Bean app with VoiceOver](https://vimeo.com/502341456/29176d676e)

- Poor labels & missing feedback
    + No feedback when trying to add whipped cream
    + Some options were headings, others not
    + Did not indicate that they were accordions


## Extra Links

- [Slides (ZIP that contains Powerpoint and PDF)](https://assets.knowbility.org/training/2021/screen-readers/Screen-Readers-in-the-Wild.zip)
- [A Brief History of Screen Readers Blog Post](https://knowbility.org/blog/2021/a-brief-history-of-screen-readers/)
- [Web Developer Toolbar](https://chrispederick.com/work/web-developer/)
- [Skip Links are Important](https://knowbility.org/blog/2019/skip-links/)
- [Knowbility auditing services](https://knowbility.org/services/audits/)
- [Knowbility accessibility training](https://knowbility.org/services/training/) 
- [Access Works usability testing](https://knowbility.org/services/usability-testing/)
- [Challenging Accessibility Assumptions: Screen Readers (February webinar)](https://knowbility.org/services/online-training/2021/february/challenging-accessibility-assumptions-screen-readers/)
- [Implementing Accessible Solutions: Screen Readers (March webinar)](https://knowbility.org/services/online-training/2021/march/implementing-accessible-solutions-screen-readers/)
- [John Slatin Virtual AccessU 2021](https://knowbility.org/programs/accessu/2021/)