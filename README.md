
# What The Grid
- In 2018 developing grid with FireFox is more usefull than Chrome.
- Easiest way to centering elements in CSS.
- Grid is convenient for overlapping the elements.
- Flexbox is good but Grid is better in most use case.
- CSS do all the styles layout.

reference:
https://css-tricks.com/snippets/css/complete-guide-grid/
https://www.w3schools.com/css/css_grid.asp

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
In FireFox Dev tool layout:
explicit columns and rows: - - - - -
implicit columns and rows: . . . . .

## 6.grid-auto-flow Explained
Auto flow default is **row**.
```
grid-auto-flow: column;
grid-auto-columns: 200px;
```
