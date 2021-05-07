# Developing with Accessibility in Mind

Building a product is like planning and throwing a party.


## Presenters

- Sana Ajani
    + Program Manager 2 | Microsoft
- John Alkire
    + Software Engineer 2 | Microsoft
- Fernanda Bonnin
    + Program Manager 2 | Microsoft
- Sep DiMeglio
    + Customer Engineer | Microsoft
- Dante Gagne
    + Senior Program Manager | Microsoft
- Isidor Nikolic
    + Senior Software Engineer | Microsoft


## Phases of Product Development

- Define vision with good user research
- Design
- Development
- Post Development


## Define Vision with Good User Research

- Talk to diverse user groups
    + Ensure we are aware of all of our users' needs
- Learn about Assistive Technologies
    + Ensure that our product has a good experience for those using assistive technologies
- One extends to many
    + Designing specifically to a group with one set of needs, we can extend the benefits of that assistive technology to all
    + Example: Everyone, walking or not, will enjoy wide walkways


## Design

- High color contrast
- Multiple visible indicators for all components
    + Shopping website with add to card button, which has a shopping cart icon, strong color, and the words "add to cart"
- Keyboard/touch interactions
    + Touch target size
    + Padding around buttons
- Set Up Easy Recovery
    + Users will likely make mistakes when using our products. That's okay
    + Make it easy to recover or escape when they do something that they didn't mean to do


## Development

- Use standardized components wherever possible
    + Variety of components are already designed with assistive technology in mind
        * Good headings
        * Good page structure
        * Available acccessible web components from libraries
- Create scalable pages
    + Ensure that our components and pages that adjust to different screen sizes
- Perform automated testing (accessibility insights)
    + Microsoft's Accessibility Insights for Web or Desktop


## Post Development

- Check for Common Issues
    + Accessibility Insights
- Include Help Content
    + and onboarding guides
- Get Feedback
    + For future iterations
    + If it's difficult to provide feedback, then it's likely we'll only get negative feedback
        * That can be helpful, but it means we won't get a full picture


## Accessibility Insights

Cost of fixing an Accessibility Bug is very high, there's a back and forth between the developer and testers/customers. Meanwhile there are customers who cannot use the products.


How much better would it be to think about accessibility from the beginning and ensuring it is a part of the product?


Accessibility Insights is an open source suite of tools that helps developers catch accessibility issues early in the development cycle. You can code and run automated tests before creating a pull request. This allows us to integrate accessibility into the development loop.