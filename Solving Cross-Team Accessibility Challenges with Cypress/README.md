# Solving Cross-Team Accessibility Challenges with Cypress

## Presenter

- [Mark Noonan](https://www.linkedin.com/in/markthomasnoonan/)

[This presentation](https://youtu.be/jEbd7EBXqvI?si=yzJ0NpcXo25RxMGj) was mostly an ad for Cypress, but it had some tidbits that I liked a lot and wanted to capture:

- Accessibility is user independence
  - Users must always be able to answer these questions:
    - Where am I in the app?
    - What's on the page right now?
    - What's the current state?
    - What can I do?
- What's hard about accessibility automation?
  - Technical challenges:
    - Training all test authors about when to run checks
    - Clear and efficient communication of issues to other teams like product and design
    - Investigating the introduction of a new issue
    - Detecting trends and patterns
    - Alerting and blocking
    - Isolating results according to owners
    - Debugging violations from inadequate text snippets
    - CI execution time and stability - slower tests, more failed pipelines
    - Handling results with agents
    - Ensuring all teams actually do the same standard of testing
  - Emotional challengeces/resistance at the team level:
    - It requires specialized knowledge
- How is Cypress Accesibility different?
  - It piggy-backs on Cypress tests (open & close menus, go into forms), processes that information, derives accesibility checks from other tests
  - It offers solutions for many of the technical challenges listed earlier
- How do you evolve a team from 'detect and report' to 'prevent regressions by default' without causing CI fatigue or resistance from devs?
  - Core idea is to do it like a linter rollout: don't introduce all strict at once because you'll  suddenly make your team responsible for a lot of rules they don't know or understand
  - First, defend your current standard as much as possible. If you're WCAG 2.1 compliant but aiming for WCAG 2.2, but notice 2.1 success criteria slipping, focus there
  - Second, find the low-hanging fruit for the state you want to achieve