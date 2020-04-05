# Modular Layouts

 

### Comments



## Basic Modules

A **module** is a component of a page, like a button, or text, or the navigation bar. Each module has an associated **tag**. Tags are just “words” to represent the modules, which are used in various contexts. The tag for buttons is `button` the tag for navigation bars is `nav`. 

#### Tags

A tag containing text will look like this:

```
<tag:>Some text.<:tag>
<tag:>
    Some more text.
<:tag>
```

The module associated with the tag will determine how the tag appears. Overall, there is no difference between the above two formats in terms of the final result produced. One format might be preferred over the other in difference situations.

Alternatively, tags may be isolated, without containing any text:

```html
[tag]
```

Note the difference in the placement of the colons `:`.

Tags can also have inputs when required.

```
[tag(input)]
[tag(input):]Text.[:tag]
```

 Finally, tags can be associated to a variable.

```
{tag(input)}
```



### Anatomy

Anatomy modules isolate the main parts of the webpage from one another. They’re at the fundamental level of the web page.

#### Head

This contains the page title and an excerpt. The excerpt is used for searches. 

In addition, it’s used to link the associated design files to the page and import any custom designed modules, which we’ll get to later. 

```html
<head>
    <title>The Title is here.</title>
    <excerpt>This is an excerpt for this page. The excerpt shows a quick summary for search engines. This page is just a sample.</excerpt>
    <design ("home.z1")>
    <import ("ComboBox.zc")>
</head>
```

#### Body



### Numbers

#### Int



#### Floats



#### Fractions



#### Span

Span are for measurements. 

### Text

#### String



#### Headings



#### Paragraphs



#### Clause

A clause represents a section of a sentence in Z.

#### Text Formatting

Text formatting involves changing the colour or text or making it bold, italicized, underlined, or strikethrough. 

```html
<p>
    <#red>This text is red</#red>.
</p>
```

![](text_colouring.png)

The following example covers **bold**, *italics*, <u>underline</u>, and ~~strikethrough~~.

```html
<p>
   <b>Bold.</b> <i>Italics.</i> <u>Underline.</u> <s>Strikethrough.</s>
</p>
```

![](text_formatting.png)

### Breaks

Breaks are to add breaks in between lines. There are two types of breaks in Z: the soft break and the hard break. The **soft break** is for line breaks and adding spacing between paragraphs if desired. The **hard break** is for adding a break between two paragraphs, and generally adds a line between them. Use `<br/>` for a soft break and `<Br/>` for a hard break.

```html
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras et blandit justo. Donec ac sapien ornare, sagittis tellus quis, condimentum justo. Aenean porta felis tincidunt ultrices sodales. Nullam ut lacinia mi. Vestibulum egestas euismod elit quis consectetur. Curabitur luctus ex et ipsum dictum, ornare malesuada purus dictum. In hac habitasse platea dictumst. Nulla bibendum, orci laoreet cursus accumsan, nunc diam commodo lorem, nec pulvinar felis dui eu ante. Sed sed metus nec mi lacinia luctus ut eget risus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Praesent quis mauris mauris. Nulla tempus et mauris non eleifend. Donec tempor quam nec orci elementum, quis placerat massa gravida. Fusce sagittis felis in dolor fringilla, ut tincidunt urna feugiat. Nam et magna dui. Aenean sed iaculis dui.
</p>

<br/>

<p>
Vestibulum cursus urna in justo tempus tempus. Suspendisse ullamcorper fringilla est non sagittis. Nam ut molestie purus, sit amet semper dolor. Aenean malesuada ligula ut velit convallis, sit amet porttitor ante viverra. Ut quis bibendum dolor. Duis pulvinar ex nec consectetur malesuada. Vivamus fermentum tellus eu molestie faucibus. Nam luctus aliquet lacus, non gravida dui accumsan sed. Integer eget tempus nulla. Integer quis pretium purus. Donec at tincidunt turpis. Aliquam et enim mollis diam dapibus iaculis ut at nibh. Vestibulum libero quam, convallis eget semper pulvinar, aliquet et turpis.
</p>

<Br/>

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed lectus tortor, vestibulum elementum varius vel, hendrerit sed ante. Aenean nisl sem, pretium eu tincidunt eu, condimentum ac sapien. Etiam at erat sapien. Nulla pharetra auctor risus, at molestie nisi sagittis nec. Donec tempus libero suscipit ligula interdum molestie. Fusce id auctor risus. Vestibulum sed dolor augue. Sed posuere tincidunt nisi. Quisque luctus justo id tellus consectetur vestibulum. Curabitur eget rutrum purus. In eros mauris, aliquam nec condimentum in, malesuada sit amet odio. Nullam venenatis vel tortor ut placerat. Nullam condimentum, massa at rutrum imperdiet, nisi ante vestibulum est, tempor dictum turpis est nec mi. Donec ullamcorper dictum mauris, vel auctor neque rhoncus et.
</p>
```

![](breaks.png)



### References

Reference

#### Links



#### Images



#### Files



## Variables

For those of HTML/CSS background, variables substitute ids and classes. Variables can later have their appearance edited. A single variable may be used with multiple elements.

For example:

```html
<int num>12</int>
<int num>15</int>
<double num>3.14</double>
<string num>43</string>
<int i>-6</int>
```



