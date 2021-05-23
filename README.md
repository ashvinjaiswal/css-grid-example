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

### Example 2 Fr Unit, Short Hand for grid

Fr Unit: Fr is a fractional unit and 1fr is for 1 part of the available space. 

```
.container{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 100px 100px;
    gap: 5px;
}
```

We are using fr unit to make three equl width column layout.

reapet function: specifies, as a space-separated track list, the line names and track sizing functions of the grid.

```
.container{
    display: grid;
    grid-template-columns:repeat(3, 1fr);
    grid-template-rows: repeat(2, 200px)
}
```

Shorthand: Shorthand for setting grid-template-columns, grid-template-rows, and grid-template-areas in a single declaration.

Syntax: none |  <'grid-template-rows'> / <'grid-template-columns'>  |  <line-names>? <string> <track-size>? <line-names>? / <explicit-track-list> 

```
.container{
    display: grid;
    grid-template:repeat(2, 100px) /repeat(3, 1fr);
    gap: 5px;
}
```

### Example 3: Placement of item
Items that are not explicitly placed on the grid will be placed according to an algorithm. We use grid-column-start, grid-column-end, grid-row-start and grid-row-end to define where an item starts and ends on the grid.

```
.header{
  grid-column-start: 1;
  grid-column-end: 3;
}

//Short Hand start/end

.header{
  grid-column:1/3;
}
```
In above example, we used class selector to select element and select postion based on grid column lines.

```
.footer{
  grid-column:1/3;
}

//alternate way
.footer{
  grid-column:1/span 2;
}

```
In above example, select first grid column line and span element to two columns


```
.footer{
  grid-column:1/-1;
}
```
In above example, select first column grid line and span element to last column grid line 

#### Resource 
[Grid Vocabulary](https://www.digitalocean.com/community/tutorials/css-css-grid-layout-intro)