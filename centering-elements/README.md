# 💡 How to center elements in CSS - Complete Guide

<hr>
<br>

## 🃏 Horizontally

<br>

### - Is it inline or inline-* elements (like text or links) ? <br> <br>

This elements can be centered within a block-level parent element, just with:

```
.center {
    text-align: center;
}
```

<br>
<br>

### - Is it a block level element (like div's) ? <br> <br>

You can center this kind of elements giving it an auto side margin (left | right), see:

```
.center {
    margin: 0 auto;
}
```

<br>
<br>

### - Position absolute <br> <br>

You can use position absolute to center any type of element, this way:

```
.center {
	position: absolute;
	left: 50%;
	transform: translateX(-50%);
}
```

or

```
.center {
	position: absolute;
	right: 50%;
	transform: translateX(50%);
}
```

<br>

If you know the item width, you can just use left or right as 50% and subtract half of item width of margin, like:

```
.element {
    width: 100px;
}

.center {
	position: absolute;
	right: 50%;
	margin-right: -50px;
}
```

or

```
.element {
    width: 100px;
}

.center {
	position: absolute;
	left: 50%;
	margin-left: -50px;
}
```

<br>

Obs: To use absolute position, the parent element need to have the property position: relative setted! 

<br>
<br>

### - Can you use flexbox ? <br> <br>

If the flex property flex-direction is equal to row, you can just set this property to align the childs of it:

```
.parent-element {
    justify-content: center
}
```

<br>

If the flex property flex-direction is equal to column, you can just set it:

```
.parent-element {
    align-items: center
}
```

<br>
<hr>
<br>

## 🀄 Vertically

<br>

### - Is it inline or inline-* elements (like text or links) ? <br> <br>

If is a single line element just set the padding top and bottom as equal, see:

```
.center {
  padding-top: 30px;
  padding-bottom: 30px;
}
```

If padding isn’t an option for some reason, and you’re trying to center some text that you know will not wrap, there is a trick were making the line-height equal to the height will center the text:

```
.center-text-trick {
  height: 100px;
  line-height: 100px;
  white-space: nowrap;
}
```

<br>

If is a multiple line element it can be a bit difficulty, see it to learn more detail:

https://css-tricks.com/what-is-vertical-align/

<br>
<br>

### - Is it a block level element (like div's) ? <br> <br>

If you do not care if the element stretches the height of the container, you can use it in the parent element:

```
.center {
    display: table-cell;
    vertical-align: middle;
}
```

<br>
<br>

### - Position absolute <br> <br>

You can use position absolute to center any type of element, this way:

```
.center {
	position: absolute;
    top: 50%;
    transform: translateY(-50%);
}
```

or

```
.center {
	position: absolute;
    bottom: 50%;
    transform: translateY(50%);
}
```

<br>

If you know the item height, you can just use top or bottom as 50% and subtract half of item height of margin, like:

```
.element {
    height: 100px;
}

.center {
	position: absolute;
    bottom: 50%;
    margin-bottom: -50px;
}
```

or

```
.element {
    width: 100px;
}

.center {
	position: absolute;
    top: 50%;
    height: 100px;
    margin-top: -50px;
}
```

<br>

Obs: To use absolute position, the parent element need to have the property position: relative setted! 

<br>
<br>

### - Can you use flexbox ? <br> <br>

If the flex property flex-direction is equal to row, you can just set this property to align the childs of it:

```
.parent-element {
    display: flex
    align-items: center
}
```

<br>

If the flex property flex-direction is equal to column, you can just set it:

```
.parent-element {
    display: flex
    justify-content: center
}
```

<br>
<hr>
<br>

## 🗿 Horizontally & Vertically

<br>

### - Position absolute <br> <br>

You can use position absolute to center any type of element, this way:

```
.center {
	position: absolute;
	top: 50%;
	right: 50%;
	transform: translate(50%, -50%);
}
```

or

```
.center {
	position: absolute;
	bottom: 50%;
	left: 50%;
	transform: translate(-50%, 50%);
}
```

<br>

If you know the item width and height, you can just use top or bottom as 50% and subtract half of item height and width of margin, like:

```
.element {
    height: 100px;
}

.center {
	position: absolute;
	top: 50%;
	right: 50%;
	margin: -50px -50px 0 0;
}
```

or

```
.element {
    width: 100px;
    height: 100px;
}

.center {
	position: absolute;
	bottom: 50%;
	left: 50%;
    margin: 0 0 -50px -50px;
}
```

<br>

Obs: To use absolute position, the parent element need to have the property position: relative setted! 

<br>
<br>

### - Can you use flexbox ? <br> <br>

You can just set this properties to align the childs of it:

```
.parent-element {
    display: flex
    align-items: center
    justify-content: center;
}
```

<br>
<br>

### - Can you use grid ? <br> <br>

This is just a little trick (sent in by Lance Janssen) that will pretty much work for one element:

```
.parent-element {
    display: flex
    align-items: center
    justify-content: center;
}
```

<br>
<hr>
<br>

### ㊙️ Inspiration: https://css-tricks.com/centering-css-complete-guide/