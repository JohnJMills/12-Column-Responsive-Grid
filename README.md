TWELVE COLUMN RESPONSIVE GRID
=============================

OVERVIEW
There are a lot of grid systems already out there, but this is one that I have been using on my own for several projects now. Rather than dusting it off and updating for each new project, I decided to document it and post it here so I can keep track of changes and updates. 

The grid is a 12 column responsive grid that can be either fluid or fixed width. The supported breakpoints are (arbitrarily named):
- iPhone: 320px wide
- Android Phone: 420px wide
- Kindle Fire: 600px wide
- iPad: 768px wide
- Desktop: 960px wide

USAGE
Add the "_responsive-grid.scss" to your project and compile with your other SASS files. Additionally you can add the "_responsive-content.scss" which allows you to show/hide content for various breakpoints. 

To create the grid, first create a containing element with the class "center-content". Within that element, add a <div> for each column with the classname "column".

<section class="center-content">
    <div class="column"></div>
</section>

COLUMN WIDTHS
Columns by default span the width of the page (100%). The column grid is base 12, so sizes can be set in the number of 12ths that the column will span. A 1/12th column would be assigned a class of "col-1x". A 1/3 column would be assigned a class of "col-4x".

MODIFIER CLASSES
- no-margin: removes the right margin from a column
- fat: adds the width of both the right and left margins to a column
- center: removes float and centers the column within the center-content container
- no-float: removes float from a column
- wide-mobile: forces a column to be 100% wide at mobile resolutions

NESTING
Nesting columns is supported. In order for percentage values to be calculated correctly, an inner container element must be used withe the class "container" applied to it as in the following example:

<div class="column col-8x center">
    <div class="container">
        <div class="column col-2x"></div>
        <div class="column col-4x"></div>
        <div class="column col-2x"></div>
    </div>
</div>

ROWS
To properly manage floats and possibly force a row break, add a <div> element with the "row-break" class applied. 

<div class="row-break"></div>

FIXED WIDTHS
By default the grid is fluid. You can fix the "center-content" element to match the width of the breakpoint by adding a "fixed" class to the <body> tag. This will force the "center-content" element to be either 320, 480, 600, 768, or 960px wide,


