
**Website are written on HTML**

HTML is the language used for all the web pages you see on the internet. If you right-click on any website (including this one) and press **View Page Source,** you’ll be able to see the HTML that is used to display what you are seeing. 

HTML is built in a **tree-like structure** called the Document Object Model, or **DOM.** The DOM is made up of a bunch of different **tags** that can be nested into each other. Different tags can represent each part of an HTML page, and most elements have an opening and closing one.

An opening tag looks like:  `<element_name>`  and a closing tag usually has the same  `element_name`  just with a  `/`  in the front, e.g.,  `</element_name>` . For example, every web page has the  `html`  opening tag,  `<html>`  , and the closing tag,  `</html>`. All the information you want in that element needs to be between the opening and closing tags.

![[Pasted image 20240921153313.png]]

```html
<!DOCTYPE html>
<html>
	<head>
		<title></title>
	</head>

	<body>
		<h1></h1>
		<h1></h1>
	</body>
</html>
```

There are many different types of tags, each representing different elements that you can put into your web page. Here are some common ones:

- `<p>`  for a paragraph element. 
    
- `<b>`  for a bold element. 
    
- `<a>`  for a hyperlink.
    
- `<div>`  a new section or division.

A couple of important things to know about HTML tags are **`class`** and **`id`** attributes, which are ways to give different HTML elements identifiers. For example, if you want to identify all the items of clothing with a single identifier, you can write the following: 

```html
<p class="clothing">shirt</p>
<p class="clothing">socks</p>
```

https://webformatter.com/html

