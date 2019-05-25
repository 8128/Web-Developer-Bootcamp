[TOC]

# Web-Developer-Bootcamp

Udemy Course: the-web-developer-bootcamp

Finished Parts:  

- Bootstrap 3 2018.12.24
- CSS 2018.12.23
- HTML 2018.12.15

In Progress:

- Bootstrap 4

# Note

## HTML

### The General Rule

<tagName> Some Content </tagname>

https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML

### Doctype

HTML always start with 

```html
<!DOCTYPE HTML>
```

### Comments

```html
<!-- this is a comment-->
```

### Elements

https://developer.mozilla.org/en-US/docs/Web/HTML/Element

```html
<strong></strong>
<em>emphasize</em>
<i>italic</i>
<p>paragraph</p>
<ol>
  <li>ordered bullet point</li>
</ol>
<ul>
  <li>unordered bullet point</li>
</ul>
<img src="aaa.png">
<a href="url">Link Text</a>
```

### Divs and Spans

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div

div is a block level element, span in a in line container

### Tables

```html
<table>
  <thead>
    <tr>
      <th>h1</th>
      <th>h2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>a</td>
      <td>b</td>
    </tr>
  </tbody>
</table>
```

Tr for each row

td for each element

### Inputs

```html
<form action="some url" method="POST">
  <input type="text">
  <input type="color">
  <input type="radio">
  <input type="email">
  <input type="checkbox">
  
  <!-- if you want only one radio box be checked you can use the same name attribute, to disginush the value, set value-->
	<form>
    <input name="a" type="radio" value="dog">
    <input name="a" type="radio" value="cat">
    
    <!-- only if a name is set can info be conveyed-->
    <!-- the default value sent will be option, unless you set values-->
    <select name="color">
      <options>a</options>
      <options>a</options>
      <options>a</options>
    </select>
    
    <textarea name="paragraph" rows="10" cols="10"></textarea>
  </form>
  
	<!-- placeholder is the information shown inside the input box-->
  <label>
    Username:<input name="username" type="text" placeholder="username">
  </label>
  <label>
    Password:<input name="password" type="password" placeholder="password">
  </label>
  
  <label for="username">Username:</label>
  <input id="username" name="username" type="text" placeholder="username" required>
  <!-- restriction on password -->
  <label for"password">Password:</label>
  <input id="password" name="password" type="password" pattern=".{5,10}" requiredtitle="password must be bewteen 5 an 10" placeholder="password">
  
  <button>Submit</button>
  <input type="submit">
</form>
```

## CSS

### How to use CSS:

1. The first way is to add the script below

   ```html
   <style type="text/css">
     <!-- write your css code here -->
     h1 {
       color:purple;
     }
   </style>
   ```

2. write the css file seperatly and use a link tag

   ```html
   <link rel="stylesheet" type="text/css" href="app.css">
   ```

### Color

You can find colors here[colors](http://colours.neilorangepeel.com), or you can use the Hexadecimal

### Background

You can set the background to any color

```css
body{
	background: red;
	/* or you can use a image, and the image will be tightened to the whole screen */
	background: url(...);
	background-repeat: no-repeat;
	/* strech */
  background-size: cover;
}
```

### Border

You have to set all color, width and style to see the result

```css
h1 {
  color: rgba(0,200,100,0.8);
  border-color: purple;
  border-width: 5px;
  border-style: solid;
  /* or using */
  border: 5px dashed purple;
}
```

### Selector

1. set the id in the html, and then you can use #id to change the certain style of it.

2. But id is limited to one, so if you want to change severl, you can use the class, and use .classname in the css file

3. star select will select everything on the page

   ```css
   * {
     color: green;
   }
   ```
   
4. [desxendant selector]consecutive selector will find the sub one, eg. the below one will find the lind inside of a bullet point

   ```css
   ul li a {
     
   }
   ```

5. [adjacent selector]this one will select the adjancent h4 and ul together

   ```css
   h4 + ul{
     
   }
   ```

6. [attribute selector] 

   ```css
   a[href="http://www.google.com"]{
   }
   ```

7. nth of type

   ```css
   ul: nth-of-type(3){
   } 
   ```

### Font

```css
h1{
  font-size:200px;
  font-size: 2.0em;/*double the size of enclosing emelemt of the parent element*/
  font-weight: normal/bold;
  line-height: 1.5;
  text-align: right;
  text-decoration: underline;
  text-transform: uppercase;
}
```

Becaues the initial size of the em is not certain, you can set the body font size firstly

To use a google font, add it to the head of the file, and then use the font-family=""

### Box Model

- Content

  width and height

- Padding

- Border

- Margin

  Margin: 20px 40px 500px 100px//top right bottom left

Float:left then the next box will adjacent to the left of the box



## Bootstrap4

### Container class

You can get a dive with padding on the side with class container. And it will also be centered.

### Form Group class

Yon can get several from divided by a little gap if you use form group class

### Form Control class

Set the position insied of a div