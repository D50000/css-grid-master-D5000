# What The Grid
- In 2018 developing grid with FireFox is more usefull than Chrome.
- Easiest way to centering elements in CSS.
- Grid is convenient for overlapping the elements.
- Flexbox is good but Grid is better in most use case.
- CSS do all the styles layout.

reference:
https://css-tricks.com/snippets/css/complete-guide-grid/
https://www.w3schools.com/css/css_grid.asp

## Introduce
In 2018 developing grid with FireFox is more usefull than Chrome.
firefox develoved mode (F12) grid  support:
- more useful layout tools
- more display detail and informations

## Start to Setup
Download Firefox, node, browser-sync for more productive.

## Grid Fundamentals
Basic Grid syntax.
```
.container {
	display: grid;
	/* You can use repeat for loop the grid => repeat(5, 100px) */
	grid-template-columns: 200px  500px;
	/* columns width */
	grid-template-rows: 200px  100px  400px;
	/* rows height */
	grid-gap: 20px;
}
```
