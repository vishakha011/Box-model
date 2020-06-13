# Box-Model

## Introduction: 
HTML is all about the content, which resides into elements and every HTML element is a box. Before discussing Box-model we need to understand how these elements are displayed.

We know, that elements are either block-level or inline-level elements. Block-level elements occupy any available width, no matter what their content is, and begins on a new line. On the other hand, Inline-level elements occupy only the width their content requires and line up on the same line, one after the other. 

## Display Properties:

No matter whether an element is block-level or inline-level, it has a default display property value. The common value for display property is *block*, *inline*, *inline-block*, and *none*. 
But these default properties can be overwritten. A block can be displayed as inline or an inline can be displayed as a block-level element.
However, the inline-block level element is little different and interesting. It allows elements to have both block-level and inline-level properties.
Apart from all these values, there is one more, "none" for which will hide the element on the page as if that element does not exist in the HTML document.


## The Box Model

### The Main Pieces of the Box Model
There are 4 important properties that allow you to size and distribute your HTML elements:

- content
- Padding
- Border
- Margin

        ![Images](Write-up\images\box_model.JPG)
            

**Content:**

The content area, contains the “real” content of the element, such as text, an image, etc. Its dimensions are the content width and the content height. Every element has some default width and height based on the display property. If it is a block-level element it will have 100% width covering whole horizontal space. If it is an inline or inline-block element it will have width according to the content it wraps.

**Padding:**

Padding is the inner space between the content and the border of the box. You can use the same value all across the box. 
For example,
```
padding: 20px;
```

or you can give padding to only one side of the box,
for example, 
```
padding-right: 10px;
```

Besides, there are options for shorthand writing, which allow you to give a different value to each side, without writing them separately.
For example, 
```
padding: 10px 20px 5px 15px; 
 
```
equal to
```
padding-top: 10px, 
padding-right: 20px, 
padding-bottom: 5px and 
padding-left: 15px.
```

**Borders:**

The three basic properties for creating borders are:

Border-style :- mostly used with one of the common keywords: solid, dashed or dotted.

Border-width :- tells the browser about the size of the border. Usually, we use pixel value for this property, 
for example,
``` 
border-width: 5px;
```

Border-color :- by default, the value uses the currentColor of the text. However, we prefer to define it even if we don’t have to. For example, 
```
border-color: red;
```

There is a shorthand that gives you the possibility to write all of them together, the border shorthand property.
With this property, we can write only 
```
border: solid 5px red;
```

**Margins:**

Margins are the outer spaces between boxes. The margin property is very similar to padding. But instead of applying inside the element, it sets the space that surrounds outside the element. Margin property is applied to provide a gap between the elements on a page. It provides space around the element. 

## There are 2 types of Box-Sizing Properties.

**Content-Box** — This is the default value as specified by the CSS standard. The width and height properties include the content but does not include the padding, border, or margin. For example,
```
 .box {
     width: 350px; 
     border: 10px solid black;
     } 
```
renders a box that is 370px wide.

**Border-Box** — The width and height properties includes the content, padding, and border, but do not include the margin. The padding and border will be inside of the box. 
For example,
``` 
.box {
    width: 350px; 
    border: 10px solid black;
    } 
```    
renders a box that is 350px wide. 