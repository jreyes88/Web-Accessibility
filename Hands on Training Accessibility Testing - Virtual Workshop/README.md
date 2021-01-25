# Hands on Training Accessibility Testing - Virtual Workshop

Hosted by Nicholas Steenhout


**Nicholas Steenhout**

- Blog: [https://incl.ca](https://incl.ca)
- Twitter: [@vavroom](https://twitter.com/vavroom)
- Email: [nic@incl.ca](mailto:nic@incl.ca)
- Podcast: [https://a11yrules.com](https://a11yrules.com)


## Structure

- **1st Hour:** the background and why
- **2nd & 3rd Hours:** Testing methods overview


## Disclaimer

- No time for everything
- Getting you started
- Workflow to find majority of issues


## Accessibility Overview

- You don’t know what you don’t know, and that’s okay.
- However, once you start hearing about things, you can begin to integrate accessibility

### \#a11y
- Numeronym
- Accessibility
- Some people argue that numeronyms are not truly accessible


**Accessibility:** The inclusive practice of making websites usable by everyone, regardless of ability or disability.


## Statistics

- 1 in 4 people in the United States have some form of disability
- Perhaps the largest minority out there
- That doesn’t mean that 1 in 4 people have a condition that impacts their use of the web
- However the number game is a losing battle, once you start breaking down those numbers
    + “1 in 8 men are colorblind” but how what type of colorblindness?
- What browsers you support is probably a more important questions


## Disability Types

- Vision
- Blind, low vision, color blind
- Hearing
- Deaf, hard of hearing
- Look into “Deaf” and “deaf” with capital/non-capital letters
- Physical or Motor
    + Fine control, slow motion, no mouse
- Cognitive or Neurological
    + Learning impairment, distracted, decision making


### All Devices

This workshop will focus on desktop, but much of it will be cross-device friendly. **Our users are not disabled until we present them with a non-accessible website.** The onus of accessibility is where it belongs -- on the owners, designers, and stakeholders, rather than on the end user.


### Temporary Impairments

- Nicholas once broke both of his wrists, both wrists were in a cast
- Became a sighted keyboard-only users
- Then went to voice-input user


### Situational Impairment

- Holding a baby
- Cerebral Palsey hard to do fine movements
- On the bus, it’s shaky, big hands and small check boxes
- Non-native language speakers
- People who are born deaf are truly ESL users
    + Structure of ASL is different than common written English
    + Complex written sentences can be challenging
- Looking at phone in bright sunlight


Above all, accessibility is making sure that our digital resources are available to everyone.


## WCAG 2.1 - Web Content Accessibility Guidelines

Broken down into 3 levels:
- **A:** the minimum requirements that provide accessibility to a large number of users
- **AA:** things we should do to make things more accessible
- **AAA:** More things that can be implemented to make it even better


There are very few websites that can meet AAA levels of accessibility, but you should try.


**Accessibility is a continuum, and it’s always a search of improvement.**


Meeting AA level is totally possible.


Heirarchy of WCAG:
- 3 Levels
- 4 Principles
- 13 Guidelines
- 78 Success Criteria
- Lots of Techniques


## 4 Principles: POUR

- **Perceivable:** Able to perceive info through their senses either via browser or assistive technology
- **Operable:** Able to interact with controls or dynamic elements with mouse, keyboard, etc.
- **Understandable:** Able to understand information and how to use the interface
- **Robust:** Content can be accessed by old and new user agents and assistive technology


Compliance != Accessibility. Meeting requirements doesn’t always ensure accessibility.


## Testing Method Overview

### Automated testing

#### Pros:
- Quick
- Not all errors need a human eye
- Can review hundreds of pages
- Good for getting “pulse”, starting point for the health of the assets you’re testing


#### Cons:
- Incomplete coverage
- Can determine if alternate text is available on an image, but can’t (yet) determine the quality of that alternate text
- Not good with all aspects of forms
- Picks things up that aren’t there
- Strong at testing CSS colors but maybe not an image with white text on a light gray background
- Scripting, dynamic content, etc.


UK Government Digital Service a few years ago built the worst accessible page ever (intentionally):
- 130 something errors
- Best tool only picked up 38% of barriers
- **CHECK OUT: This study**


### Manual testing

- Relies on Human Judgment
- Slower
- Depends on tester’s experience


### User testing

- Real users
- Discovering things testers can miss
- [https://access-works.com](https://access-works.com)
- Extremely worthwhile to do user testing at every stage of development (prototype, MVP, finished product) if you have the resources
- Best if the disabled users use their own devices, do it through Zoom. Not like a typical focus group where you bring the group into a lab or facility


## Automated Testing Tools

### Tenon.io

- Ranked highest in UK Digital Services Test
- Paid service
- Can easily set up a large suite of pages to audit
- Can run audit on certain intervals
- Can push results to ticketing systems like Jira or Github
- Can check staging server


### Axe Accessibility Engine

- Plugin in Firefox, Chrome, Safari
- Free


### Wave toolbar

- Plugin for Firefox and Chrome
- Will put flags throughout the page to identify
- **CHECK OUT: one million website WebAIM study**


### Accessibility Insights

- Built on Axe Engine
- Cool presentation and gives you tips on manually testing/fixing individual elements


## Manual Testing Tools

### Keyboard
- Direct descendant of something that was designed for people with disabilities in the 1850s
    + Hansen keyboard that allowed his pupils to communicate faster with hearing people who didn’t speak sign language
    + [https://en.wikipedia.org/wiki/Hansen_Writing_Ball](https://en.wikipedia.org/wiki/Hansen_Writing_Ball)
- Since then there have been about 55 major iterations and variations of keyboards


### Color Contrast Analyser

- Many tools out there
- WebAIM contrast analyser
- [https://bit.ly/Webaim-contrast](https://bit.ly/Webaim-contrast)


### Browser Zoom

- Firefox has Zoom text only
- Issue with larger text in browser is that generally if people zoom text, it typically is set at the system level


### Code inspection

- Web developer toolbar
- Browser developer tools, etc.


### Screen Readers

- Typically we think of screen readers as having no vision, interacting with keyboard
- However, not all screen readers have vision issues. Screen readers are being recommended for users with dyslexia
- _Exercise:_ Try it, get stuck, figure out what’s not working, turn screen off
- Using Screen Readers
    + Complex software
    + It’s a way of interacting with the computer in a non-visual way, not just reading websites
    + Experience is mission critical
    + Good indication but can lead to false positives
        * Tab Index=0 makes elements that are not natively focusable focusable, it makes these elements part of the tab order
        * If you’re not an expert screen reader it can give these false positives
- JAWS (Windows)
- NVDA (Windows)
- VoiceOver (OS X)
- Orca (Linux)
- Narrator (Windows)
- Screen readers / browser combo:
    + JAWS (Windows) - IE / Edge
    + NVDA (Windows) - Firefox/Chrome
    + VoiceOver (OS X) - Safari
    + Using a bad combo can make you think you have a lot of accessibility issues when you really don’t
- _Question:_ Is there a flag or something to set in Google Analytics to know if users are using a screen reader, and determine what browser they’re working with?
- NVDA Key Combinations:
    + Modifier Key: INSERT or CAPS LOCK
    + [http://bit.ly/Webaim-NVDA](http://bit.ly/Webaim-NVDA)
- JAWS Key Combinations:
    + [http://bit.ly/Webaim-JAWS](http://bit.ly/Webaim-JAWS)
- VoiceOver Key Combinations
    + Modifier keys: CTRL+OPTIONS = VO
    + [http://bitl.ly/Webaim-VO](http://bitl.ly/Webaim-VO)
    + Also good to have a dedicated Windows machine or virtual machine
- Screen reader demo
    + Can bring up a list of different elements on a web page.
        * Screen reader analog for a sighted user’s ability to quickly glance at headings/landmarks/form items
        * Can also use this to navigator
    + 67% of screen reader users use headings to navigateTables are intrinsically difficult from a screen reader perspective because it’s meant to display information in a visual, two-dimensional manner.
        * How to watch Table


## Manual Testing


### Keyboard
- Navigate forward: TAB
- Navigate backward: SHIFT + TAB
- Activate with SPACEBAR or ENTER
- _Keyboard Challenge:_ Spend a day or an hour without using your mouse or trackpad. Challenge your friends and colleagues: [http://nomouse.org](http://nomouse.org).

#### Keyboard Testing
- Is there a skip link? An easy way to jump past the header and main navigation
    + Should be the main element on the page
    + Can also be useful in a Twitter feed where the name, date, handle, etc. are all links
    + Skip link doesn’t always have to be visual, can hide it until it receives focus
- Focus visible?
    + Big problem: Sighted keyboard users can’t see what is in focus
    + Early bootstrap used Eric Meyer reset which sets focus to zero. He has since fixed the focus issue
- Keyboard traps?
    + Is there something that makes you unable to go forward or backward or get out of when you’re using a keyboard?
    + This is common in custom filtering or search functionality
- Interactive elements:
    + Buttons, links, forms, can you actually get to these elements with a keyboard?

### Images/Alt attribute
- `alt=””`
    + If the image is not informative and is purely decorative, leave the alt as empty
- `alt=”Some description.”`
    + Use a description if the image is informative
    + Always finish your alt text with a period
- http://bit.ly/alt-decision-tree
- If an image is the only content of a link, it must have alt text, and the alt text must describe the destination of the link.


### Form
- Don’t rely on placeholder attribute to inform the user of the field purpose
Also look at error messages
- Programmatically associate error messaging with bad input


### Aria
- W3C set of guidelines to make web elements more accessible for screen readers before HTML 5 came in with better semantic markup
- First rule: don’t use ARIA unless there is no native HTML markup for what you’re trying to accomplish
