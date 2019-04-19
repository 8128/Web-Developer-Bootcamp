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