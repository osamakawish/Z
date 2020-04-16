# Control Programming

The programming in M is primarily event driven. Functional programming is added for minimizing reusable code.

## Element Access

In M, the elements are defined as follows:

```html
<body/>
    <int i/>5</int> <!-- 1 -->
    <string str/>A string.</string> <!-- 2 -->
    <double,string ,st/>3.1</double,string> <!-- 3 -->
    <string str/>Another string with a previous "variable"</string> <!-- 4 -->
</body>
```

Here's a quick explanation of the code above:

1. An integer element `i` with the number 5.
2. A string element `str` associated to "A string.".
3. An element associated to two tags: one double, one string. The string part has the variable `st`, the double does not.
4. A reuse of the previous variable `str`. 

Accessing element variables is done with `@`. Accessing element tags is done directly by explicit stating the tag. Self-referencing is done through the `@`. Events are accessed with the colon `:`. 

```css
|behaviour {
    string @str { /* all string variables named "str" */
        mouse:press {
            @ += "r"; /* appends 'r' to the end of the string on press */
            int @i++; /* incremenets integer "i" by 1 */
        }
    }
}
```

Note that the type of the variable (`string`) is mentioned alongside the identity/name of the variable (`str`). This is to clearly access the string methods under behaviour, and update the appropriate strings. Thus, the programming in Z is strongly typed. 

> The reason for strong-typing is this: For efficiency, design patterns are often included in the `head` tag. However, as of this point, it’s unclear when the variables will be used and with what types. As such, the variables in the design pattern need to be strongly typed. Even if the design is included at the end of the page, specific methods need to be accessed, encouraging the requirement for string typing. 

## Events

For each type of input for events, there’s 2 tenses: present and past tense. 

Past tense events can be used in other methods, while present tense events can be edited. 



#### Events Structure

Events have two tenses: present and past. When an event occurs:

1. The inputs are stored, if any, into sets with same name as the past tense, if a present tense behaviour is defined.
2. The present tense behaviour is called, if defined.

For example, during a mouse press event, if the left mouse button is clicked, and the

##### Notation

The notation for the event structure is as follows:

`pastTense:presentTense(inputs)`

Replace with nothing if you don’t require a past or present tense.

### Mouse Events

* Press `pressed:press(button)`.
* Double-Press `pressed2:press2(button)`
* Move `moved:move(double[2])`
* Hold `held:hold(button,double[2])`
* Release `released:release(button)`

### Key Events

* Press `pressed:press(key)`
* Release `released:release(key)`
* Hold `held:hold(key)`

### Time Events

* Constructor with Call Operator `@:@(time t=0)`
* Time Zero `:zero`
* Now `:now`
* At `at:is(time t)`
* Since `after:passed(time t)`

Arrays start with 0 or 1 depending on how they’re named. They start with 0 if the name’s first letter is lower case, and 1 if it’s upper case.

### Specific Events

**Specific events** are events that are specific to a given control type. 

```css
behaviour {
    combo {
        /* Selects item at i'th position */
        @.select(int i) {
            
        }
    }
}
```

