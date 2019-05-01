

# What IS The Grid
- In 2018 developing grid with FireFox is more usefull than Chrome.
- Easiest way to centering elements in CSS.
- Grid is convenient for overlapping the elements.
- Flexbox is good but Grid is better in most use case.
- CSS do all the styles layout.

reference:<br/>https://css-tricks.com/snippets/css/complete-guide-grid/<br/>https://www.w3schools.com/css/css_grid.asp

## 1.Introduce
In 2018 developing grid with FireFox is more usefull than Chrome.
firefox develoved mode (F12) grid  support:
- more useful layout tools
- more display detail and informations

## 2.Start to Setup
Download Firefox, node, browser-sync for more productive.

## 3.Grid Fundamentals
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

## 4.CSS Grid Dev Tools
FireFox support toggling the grid layout display.
![](https://github.com/D50000/css-grid-master-D5000/blob/master/04%20-%20CSS%20Grid%20Dev%20Tools/Line%20Meanings.png)

## 5.Grid Implicit vs Explicit Grid Tracks
In FireFox Dev tool layout:<br/>explicit columns and rows: - - - - -<br/>implicit columns and rows: . . . . .

## 6.grid-auto-flow Explained
Auto flow default is **row**.
```
grid-auto-flow: column;
grid-auto-columns: 200px;
```

## 7.Sizing Tracks in CSS Grid
```
.container {
	display: grid;
	grid-template-columns: auto  1fr  auto  1fr;
	/* auto => it will match the biggest size in the column */
	/* fr => fraction unit the left of the space */
}
```

## 8.CSS Grid repeat Function
```
.container {
	display: grid;
	grid-template-columns: 100px  repeat(2, 1fr  auto) 200px  repeat(2, 5fr);
	/* repeat(times, grid-template)
	grid-template-columns: repeat(5, 1fr 2fr); //Make the grid 10 columns wide, every other taking up twice the free space
	*/
}
```

## 9.Sizing Grid Items
```
.item {
	//Merge for the column and row.
	grid-column: span 10;
	grid-row: span 3;
}
```

## 10.Placing Grid Items
```
.item {
	grid-column: span 2;
	/* normal method */
	grid-row: 1 / -1;
	/* shorthand
	grid-column-start: 1;
	grid-column-end: 3;
	ps: end -1 will end in the explicit grid.
	*/
}
```

## 11.Spanning & Placing Cardio
Example for the item property.

 - grid-column: 3 / 5;
 - grid-column: 5 / -1;
 - grid-row: 4 / span 3;


## 12.auto-fit and auto-fill
**Most used properties in css Grid.**
```
.container {
	display: grid;
	grid-gap: 20px;
	border: 10px  solid  var(--yellow);
	grid-template-columns: repeat(auto-fit, 150px);
	/* most used properties in css grid
	auto-fill > RWD auto figure out the space that item need.
	auto-fit > RWD auto figure out the space that item need, and it will stack the explicit grid.
	*/
}
```

## 13.Using minmax( )
**Most used properties in css Grid.**
```
.container {
	display: grid;
	grid-gap: 20px;
	border: 10px  solid  var(--yellow);
	/* grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); */
	/* fit-content(120px) == auto and max size 120px */
	grid-template-columns: fit-content(120px) 150px  150px  150px;
}
```


## 14.Grid Template Areas
Use template columns and rows to set the grid then name them by template areas.If you set a `.` instead of a name, it will be a dead space.
```
.container {
	display: grid;
	grid-gap: 20px;
	grid-template-columns: 1fr  10fr  1fr;
	grid-template-rows: 150px  150px  100px;
	/* use template columns and rows to set the grid
	then name them by template areas.
	*/
	grid-template-areas:
		"sidebar-1 content sidebar-2"
		"sidebar-1 content sidebar-2"
		"footer footer footer"
}

/* Setup the class reference to the "grid-template-areas". */
.footer {
	grid-area: footer;
}

.item1 {
	grid-area: sidebar-1;
}

.item2 {
	grid-area: content;
}

.item3 {
	grid-area: sidebar-2;
}
```

## 15.Naming Lines in CSS Grid
[ ] set the name inside, you can also set multiple names
```
.container {
	display: grid;
	grid-gap: 20px;
	grid-template-columns: [sidebar-start site-left] 1fr [sidebar-end content-start] 500px [content-end] 1fr [site-right];
	grid-template-rows: [content-top] repeat(10, auto) [content-bottom];
}

.item3 {
	background: slateblue;
	grid-column: sidebar-end;
	grid-row: content-top / content-bottom;
	/* same as => grid-column: 2; grid-row: 1 / span 10; */
}
```

## 16.grid-auto-flow dense Block Fitting
grid-auto-flow default is row, and dense will auto fill all the space. But the item order will be wrong.
```
.container {
	display: grid;
	grid-gap: 20px;
	grid-template-columns: repeat(10, 1fr);
	grid-auto-flow: dense;
}
```

## 17.Alignment + Centering
[https://developer.mozilla.org/en-US/docs/Web/CSS/place-content](https://developer.mozilla.org/en-US/docs/Web/CSS/place-content)
 - justify: main axis
 - align: cross axis

## 18.Re-ordering Grid Items
.Item {
	order: 2;
	/* Use order property for ordering, default is 0. */
}

## 19.Nesting Grid Layouts
Simple Nesting Grid layout for albums.

## 20.CSS Grid Image Gallery!
Random size image gallery layout example.
