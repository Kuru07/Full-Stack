[[CSS]]

CSS- CASCADIAN STYLE SHEETS

## Syntax
1) Create ==style.css== file
2) Use link tag and rel="Stylesheet" and href = "style.css" in html file
3) Like for example body tag changes ![[Pasted image 20241207180119.png]]
## Comments
* /* Comments * /
## Selectors
* body -> selector
* To select the element which is to be styled
* can select the particular element with its ==id== like ==#welcome== where #welcome is id
* can select by the class also ==.className== to style the class specifically to define across various elements of same class
* to have the particular tag and its class ==h1.class== like this
*  " * * "  to style the whole elements in a page
* to mingle the elements for a same style ==h1,p== 
## Background
1) Bg color 
2) To make opacity use ==opacity== attribute
3) background-image == to change the background as image![[Pasted image 20241207182223.png]]
4) background-position
## Margins
Space from all sides around elements
* top , bottom , left , right
* margin - top : value -> px or %
* margin : top_px , right_px , bottom_px , left_px
* inherit - to iinherit from its parent elements
## Border
* border-style 
	1) solid -> solid line
	2) dotted -> dotted border
	3) groove -> lighter solid line
	4) dashed -> dashed border
	5) double -> similar to groove but more thicker
	6) outset -> 3d effect like text above a shape
	7) inset -> 3d effect like text inside shape
	8) none -> no border
	9) hidden -> none shown
	10) top_brd , right_brd , bottom_brd , left_brd -> to mix the borders
* border-width -> to give the thickness of border == number_px or width rate("medium" , "thick", etcc)
* border - color -> to give color to the border
* border-top-style : dashed
* border-left: 10px dashed purple
* border-radius -> to give corners of border to be curved
## Padding
To give space around a element which is inside a border
* padding-top : px 

## Height & width
* height -> To define how much height bottom after text
* width ->To define how much width right after text
* It can be numbers in px or %
* max-width -> Set  a max width of the element
## Outlines
Same as border but in top or bottom -> wraps around the element
* outline-style -> To define the style of the outline
* outline-offset -> To leave the space for border and outline
## Text
* color -> Color the text
* text-align ->To align the text
	1) left
	2) right
	3) center 
	4) justify-> stretches around to give equal space wraps around the text
* text-align-last -> align the last line of the text
* vertical-align -> align the text vertically 
* text-decoration-line -> To decorate the text
	1) underline
	2) line-through -> strikes a line across the text
	3) overline -> line over the top
* text-decoration-color -> color the text decoration
* text-decoration-style -> style the decoration
* text-decoration-thickness -> define thickness of decoration
* text-decoration : overline purple solid 6px 
* text-decoration : none
* text-transform
	1) lowercase
	2) uppercase
	3) capitalize -> word in sentence with starts with capital letter
* text-indent -> To give indent a text
* letter-spacing -> give sapcing between the letter
## Fonts
* font-family 
	1) Arial , Helvetica , sans-serif
* font-style
	1) italic
	2) oblique - similar to italic
	3) normal
* font-weight
	1) bold
	2) normal
* font-size -> to give the size of the text px or em(16px=1em)
## Icons
*  to define google api font link in link tag in the head in href
```
<i class="material-icons">cloud</i>
<i class="material-icons">computer</i>
```
## Tables
![[Pasted image 20241207195421.png]]
to hover over the particular row
```
tr:hover
{
	background-color:blue;
}
```
## Display and Visibility
```
{
	display:none -> it will not be there in the page itself nothing displayed
	viibility:hidden -> its there but hidden
}
```
## Combinators
```
h1 b
{
	/* It will select the b elements inside h1*/
}

h1>b{
	/* It will select only the b elements which is direct child from h1 */
}

h1+b{
/* Adjacent selector select the b after h1 tag only the first adjacent of h1*/
}

h1~b{
/* General sibling selector select the every b after h1 tag*/
}

```
## Dropdown Menu
```
<body>
    <div class="dropdown">
      <button class="dropdownbutton">Dropdown Button</button>
      <div class="dropdown-menu">
        <a href="#">List</a>
         <a href="#">List</a>
         <a href="#">List</a>
         <a href="#">List</a>
      </div>
    </div>
  </body>
```
Above is html
Below is CSS
```
.dropdownbutton
{
  background-color: blue;
  color: white;
  padding: 13px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}
.dropdown{
  position: relative;
  display: inline;
}
.dropdown-menu{
 display: none;
  position: absolute;
  background-color: lightblue;
  min-width: 150px;
}
.dropdown-menu a {
  color: black;
  passing: 11px 15px;
  text-decoration: none;
  display: block;
}
.dropdown-menu a:hover {
  background-color: white;
}
.dropdown:hover .dropdown-menu{
  display: block;
}
.dropdown:hover .dropdownbutton{
  background-color: grey;
}
```
## Attribute selector 
```
div[class]
{
  color: red;
}
div[class="test"]
{
  color: red;
}
```
To select the attribute inside a tag with the class name or any class