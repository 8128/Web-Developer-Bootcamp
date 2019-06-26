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
<br>
<hr>
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



## Bootstrap 3

### Container class

You can get a dive with padding on the side with class container. And it will also be centered.

### Form Group class

Yon can get several from divided by a little gap if you use form group class

### Form Control class

Set the position inside of a div

### Thumbnail class

It will resize the pic to a thumbnail that fit into your column

### Grid System

Bootstrap has a twelve columns system

eg. col-lg-6 means column large 6

The grid system has four sizes, xs:extra small, sm:small,md:medium and lg:large

### @media

You can add some controls in the @media, eg. @media (max-width : 1200px)

## Bootstrap 4

### Display class

A more significant way for displaying

| Screen Size        | Class                            |
| ------------------ | -------------------------------- |
| Hidden on all      | `.d-none`                        |
| Hidden only on xs  | `.d-none .d-sm-block`            |
| Hidden only on sm  | `.d-sm-none .d-md-block`         |
| Hidden only on md  | `.d-md-none .d-lg-block`         |
| Hidden only on lg  | `.d-lg-none .d-xl-block`         |
| Hidden only on xl  | `.d-xl-none`                     |
| Visible on all     | `.d-block`                       |
| Visible only on xs | `.d-block .d-sm-none`            |
| Visible only on sm | `.d-none .d-sm-block .d-md-none` |
| Visible only on md | `.d-none .d-md-block .d-lg-none` |
| Visible only on lg | `.d-none .d-lg-block .d-xl-none` |
| Visible only on xl | `.d-none .d-xl-block`            |

### Blockquote

for quote

### New rem scale

There is a base rem, you can change the base element.style:font-size to a number, and rem will be the certain scale of that number

### Border Spacing

Spacing utilities that apply to all breakpoints, from `xs` to `xl`, have no breakpoint abbreviation in them. This is because those classes are applied from `min-width: 0` and up, and thus are not bound by a media query. The remaining breakpoints, however, do include a breakpoint abbreviation.

The classes are named using the format `{property}{sides}-{size}` for `xs` and `{property}{sides}-{breakpoint}-{size}` for `sm`, `md`, `lg`, and `xl`.

The default breakpoint of it is xs, and you should add sm,md,lg and xl for others, or they will just use the default one

Where *property* is one of:

- `m` - for classes that set `margin`
- `p` - for classes that set `padding`

Where *sides* is one of:

- `t` - for classes that set `margin-top` or `padding-top`
- `b` - for classes that set `margin-bottom` or `padding-bottom`
- `l` - for classes that set `margin-left` or `padding-left`
- `r` - for classes that set `margin-right` or `padding-right`
- `x` - for classes that set both `*-left` and `*-right`
- `y` - for classes that set both `*-top` and `*-bottom`
- blank - for classes that set a `margin` or `padding` on all 4 sides of the element

Where *size* is one of:

- `0` - for classes that eliminate the `margin` or `padding` by setting it to `0`
- `1` - (by default) for classes that set the `margin` or `padding` to `$spacer * .25`
- `2` - (by default) for classes that set the `margin` or `padding` to `$spacer * .5`
- `3` - (by default) for classes that set the `margin` or `padding` to `$spacer`
- `4` - (by default) for classes that set the `margin` or `padding` to `$spacer * 1.5`
- `5` - (by default) for classes that set the `margin` or `padding` to `$spacer * 3`
- `auto` - for classes that set the `margin` to auto

(You can add more sizes by adding entries to the `$spacers` Sass map variable.)

###  Display

The old 3 version use invisible and hide, but the new version does not, using the display instead

Display utility classes that apply to all [breakpoints](https://getbootstrap.com/docs/4.3/layout/overview/#responsive-breakpoints), from `xs` to `xl`, have no breakpoint abbreviation in them. This is because those classes are applied from `min-width: 0;` and up, and thus are not bound by a media query. The remaining breakpoints, however, do include a breakpoint abbreviation.

As such, the classes are named using the format:

- `.d-{value}` for `xs`
- `.d-{breakpoint}-{value}` for `sm`, `md`, `lg`, and `xl`.

Where *value* is one of:

- `none`
- `inline`
- `inline-block`
- `block`
- `table`
- `table-cell`
- `table-row`
- `flex`
- `inline-flex`

The display values can be altered by changing the `$displays` variable and recompiling the SCSS.

The media queries effect screen widths with the given breakpoint *or larger*. For example, `.d-lg-none` sets `display: none;` on both `lg` and `xl` screens.

## Javascript

### Primitive Types

These six types are considered to be *primitives*. A primitive is not an object and has no methods of its own. All *primitives are immutable*.

- [Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) — true or false
- [Null](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/null) — no value
- [Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) — a declared variable but hasn’t been given a value
- [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) — integers, floats, etc
- [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) — an array of characters i.e words
- [Symbol](https://hacks.mozilla.org/2015/06/es6-in-depth-symbols/) — a unique value that's not equal to any other value

###  Built-in Method

1. clear()
2. alert()
3. Console.log()
4. prompt()可输入的提示框

### Boolean Logic

== means equal, but this equalization doesn't mean that there type should be the same. For example, 1 == "1" is true, but 1==="1" is false. Only if you use the "===" can the type be matched.