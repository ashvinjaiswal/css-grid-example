# css-grid-example
Create the layout using CSS grid

### Example 1 - Create Grid

```
.container{
    display: grid;
    grid-template-columns: 100px auto 100px;
    grid-template-rows: 100px 100px;
    gap: 5px;
}
```
1. Create three coloum 

grid-template-columns: Define the width of column

Ex- First column: 100px, Second Column:Grow and Shrink based on available space, Third column:100px

2.  Create Two Row
 
grid-template-rows: Define height of rows
Ex- First row height: 100px, Second Row:100px

3. Grid Space
gap: The gap CSS property is a shorthand property for row-gap and column-gap specifying the gutters between grid rows and columns.