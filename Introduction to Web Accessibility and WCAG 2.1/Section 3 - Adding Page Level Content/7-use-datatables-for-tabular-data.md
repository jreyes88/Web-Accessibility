# Use Datatables for Tabular Data

Tables can help users make visual connections between tables in rows and column headers. To make this same information navigable for screen reader users, correct markup must be used to make the same table navigable.


Table headers are created using the `<th>` and `<td>` elements contained with every `<tr>` element.


The `<th>` element triggers the screen reader to interpret the element as a table header.


Additionally, these elements use `scope="col"` to designate they are column headers. Try to avoid merging cells and building complex data tables with the `scope` attribute. The cognitive effort of attempting to understand a complex table in a non-visual way can begin to become increasingly difficult.


The `<caption>` element is used to provide a brief description of the table and its data. It must be the first element after the opening `<table>` tag.


_Example:_

```html

<table>
    <caption>Suggested clothing choices</caption>
    <tr>
        <th scope="col">Morning</th>
        <th scope="col">Afternoon</th>
        <th scope="col">Evening</th>
    </tr>
    <tr>
        <td>Summer Blouse</td>
        <td>V Neck Jumper</td>
        <td>Jacket</td>
    </tr>
    <tr>
        <td>Chino Shorts</td>
        <td>Denim Jeans</td>
        <td>Dress Pants</td>
    </tr>
    <tr>
        <td>Sandals</td>
        <td>Running Shoes</td>
        <td>LAce Up Shoes</td>
    </tr>
</table>

```


## WCAG 2.1 Satisfaction

- **H51:** Using table markup to present tabular information
- **H63:** Using the scope attribute to associated header cells and data cells in data tables
- **1.3.1 Info and Relationships**: Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text (level A)


## Summary

- Tables must be marked up for a programmatic association to be made
- Column headers are created using the `<th>` element and `scope="col"`
- A table description is provided using the `<caption>` element
