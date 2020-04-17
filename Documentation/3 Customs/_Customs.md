# Z Customs

## Comments



## Name

To initiate a control with some desired name `custom`, create a new file named `custom.zc`. 

Type names can only start with letters and can end with numbers or symbols. This enforces a camel case notation. The only general exception to the type naming rule will be colours, which generally begin with `#`. 

## Hull

The **hull** is a reference to the main component of the Z Customs file. 

### Inheritance

Chances are, you don’t want to start from scratch. Unless you do, it’s recommended you inherit all the traits from `control` class.

```python
|anatomy head
|class control
```

The initiating `|` is simply to access **vitals**. Symbols in Z are for accessing some key or crucial concept. Symbols are syntactically represented by what programming languages refer to as **keywords**. 

To inherit custom controls, use `|inherits "filePath"`. It’s generally preferable to use a file path relative to the folder the file is being made in. Also, the file path can only accept underscores, letters, numbers, and spaces. Use `.` (current directory), `..` (one level up in the directory), and `/` (subdirectory) for accessing directories.

The external `.` is mainly to access general methods for making a custom control.

## Layout

To make your layout, define your `<@/>` and `</@>` tags. If desired, you may strictly your `<@>` tag differently.

```html
<@/> {
	
}

</@> {
	
}

<@> {
    
}

|child <li/></li>
```

Child controls can be private or public. 

> The protected option is removed to resolve the fragile base class problem cleanly.

During **control fusion**, the 

### Arguments

Your control can take custom arguments - either types or non-types. Not that Z remains strongly typed. Furthermore, in Z, templated controls must also have their template types which are generally interfaces. This allows for efficient method accessing. 

Interfaces:

* `numerical`: for numerical types such as `int`, `int+`, `float`, `float2`, etc.
* `text`: for text-based controls, such as `h1`, … , `h6`, `p`, `clause`, etc.
* `anatomy`: for `head` or `body`

### Fusion

You can create custom behaviour during fusions.

## Design

Works similarly to the styling layout, except now you don’t need to specify the id, except for sub contents, if desired.

```css
|placement {
	.size.x: 22px;
}

|appearance {
    
}

|behaviour {
    
}
```

Besides the usual implementation of the inherited traits as you would with a 

### Traits

You can define custom traits for your control. 

```Css
|appearance {
    +midcolor: color;
}
```

The new traits may then later be used in the actual designing.

```css
|appearance {
    +button_color: color;
    @.button fore: button_color;
}
```

For all child buttons of the custom control being defined, the foreground color is set to whatever `button_color` is set to.

### Events

Events allow you to define custom events for your control. 

For example, for a custom timer, you may want a tick event.

```css
|import timer

time: time; /* private trait */
.text: time; /* public trait */

|events {
    :(time t=0); /* constructor */
    ticked:tick();
}
```

Although an actual timer will be part of the Z standard library, this is the gist of what’s going on here.

We have a past tense getter `ticked` and a setter function `tick` with strongly typed argument(s) `double time` for the associated event. 

The events can later be used in behaviour as desired.

```css
|behaviour {
    
}
```

