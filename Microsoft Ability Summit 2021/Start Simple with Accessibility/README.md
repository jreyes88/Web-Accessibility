# Start Simple with Accessibility

## Speakers

- **Jen Smith**, Senior Program Manager | Microsoft
    + @JenniAynLynn
- **Natalie Patrice Tucker**, Senior Accessibility Lead | Spotify
    + @NataliePatriceT
- **Lori Samuels**, Accessibility Director for NBC Universal
    + @LoriSamuels18


## Agenda

- What to Expect
- Common Points of Confusion
- High Level Process for an Existing Product
- Choose a Small Scope to Test
- Simple Steps to Test for Accessibility
    + Validate Code and Ensure Semantic Markup
        * Under the Hood: Accessibility Object Model
    + Use Keyboard to Navigate and Complete Tasks
    + Turn on High Contrast Mode and Zoom in to 400%
    + Run Accessibility Insights and Fix First Pass Issues
- Prioritize Which Issues to Fix
- Fix Prioritized Issues
- Verify Accessibility Improvements
    + Verify with a Screen Reader
- Common Pitfalls


## What to Expect

There is an emotional aspect to accessibility work. If you don't know if your website is accessible, then it's not.

- You'll find out your product sucks for people with disabilities
- You'll feel badly
- You'll be overwhelmed and confused and not know where to start
- That's why we're doing this presentaiton
- Eventually things will get better
- You might even begin to feel confident about accessibility


## Common Points of Confusion

- How to audit/test?
- How to prioritize?
- How to fix?
- How to verify?


## High Level Process for an Existing Product

More often than not, we are working on an existing product.

1. Choose a small scope to test
2. Test for issues
3. Prioritize which issues to fix
4. Fix prioritized issues
5. Verify with a Screen Reader
6. Verify Accessibility Improvements


## Choose a Small Scope to Test

- "Shrink the change"
- Start with a small representative scope to evaluate for accessibility issues
- Think in terms of user flows or customer journeys
- Pick 1-3 user flows to start user testing on


## Simple Steps to Test for Accessibility

- Validate code and ensure semantic markup
- Use keyboard to navigate and complete tasks
- Turn on high contrast mode and zoom in to 400%
- Run Accessibility Insights and fix First Pass issues


### Validate Code and Ensure Semantic Markup

When validating code, tweak issues found with a:
- Code validator
- Linter
- or other checker associated with codebase
    + W3C Markup Validation Tool
    + Lighthouse
    + Linters specific to your stack


This can also improve performance and cross-browser compatibility.


#### Under the Hood: Accessibility Object Model

Have an understanding how your rendered code impacts the accessibility of your product. Read through the [WICG Accessibility Object Model page](https://wicg.github.io/aom/explainer.html).


### Use Keyboard to Navigate and Complete Tasks

Start from the top and tab through to check that:
- Every link, form field, button, control, and interactive element can be reached with keyboard
- Focus can be seen around each element
- No content or functionality is available *only* with the mouse hover or click actions
- You can move focus onto and away from every interactive element (no keyboard traps!)
- The order of interactive elements makes sense and aligns with how it would be read visually


### Turn on High Contrast Mode and Zoom in to 400%

Use responsive design and ensure that the site style reduces to a single column at 200-400% magnification. Ensure that you haven't removed functionality in this experience. Other common pitfalls are overlapping text or truncated text.


High Contrast can be tested by turning this setting on. Ensure buttons and interactive elements don't disappear and that text colors don't disappear.


Also consider the importance of video and audio in your design. Provide a text alternative -- alt attributes, captions -- so that non-hearing or users who don't use sound can still engage with the content.


### Run Accessibility Insights and Fix First Pass Issues

Use the [Accessibility Insights tool](https://accessibilityinsights.io/docs/en/web/overview/) for automated testing with Fast Pass, which can find issues with:
- Color contrast
- Empty elements
- Language
- Missing alt attributes


## Prioritize Which Issues to Fix

- Color contrast
- Missing labels for form fields
- Link text
- Alt text for image
- Page language
- Keyboard accessibility


Find the meeting of *high user impact* and *low effort to fix*.


Most common WCAG failures:
- Low contrast
- No alt text
- Empty links
- Missing form labels
- Empty buttons


## Fix Prioritized Issues

This is a deep topic, but once you practice and understand the patterns for solutions, you can get things correct the first time going forward. WCAG Guidelines is a great resource.


## Verify Accessibility Improvements

- Repeat
    + Repeating testing steps 1-4 and observe results
- Add
    + Add step 5 to check experience with a screen reader
- Engage
    + Engage users of assistive technology to test your product
    + Good to start building a relationship with folks in the disability community to provide ongoing feedback because you'll always need it


### Verify with a Screen Reader

- Read through with a screen reader to ensure there is accesss to the same meaning, functionality, and content that is presented visually
- Check for consistency, ease of navigation, hidden elements receiving focus
- Learn a few basic commands for your preferred screen reader
- Recommended combinations:
    + Desktop: Chrome + NVDA on Windows or Safari + VoiceOver on Mac
    + Mobile: iOS + VoiceOver or Android + TalkBack
- Break up this task among your team
    + Best would be to find native users
- Beginner mistake: assuming you have to test every single thing and ensure that everything works the same way across all assistive technologies
    + If you embrace best practices, those practices are platform or technology agnostic, and each assistive technology will support


## Common Pitfalls

- Going lone wolf
    + There's a whole community of people online that are blogging about their accessibility techniques and sharing their experiences on social media
- Perfection
    + You don't have to fix absolutely everything for every platform
- Overusing ARIA
    + First rule of ARIA is don't use ARIA
    + If there's a native HTML solution for what you're trying to do, just use that