Motif Sublime Text Snippets
====

This is a collection of Sublime Text shortcut snippets to enable quicker code commenting and Less variable conversion in Motif projects. Place these inside the Sublime Text `Packages/User` folder.

- [Cheat Sheet](#cheat-sheet)
- [Less/CSS Comments](#less-comments)
- [Less/CSS/JavaScript Comments](#less-js) (DocBlock-style)
- [Less Variable Conversions](#less-conversions)
- [HTML Comments](#html-comments)

Other useful downloads:

- [DocBlockr plugin](https://github.com/spadgos/sublime-jsdocs) (helps keep DocBlock-style comments going)


<a name="cheat-sheet"></a>
## Cheat Sheet

Snippet                          | Tab Trigger
---------------------------------|------------
CSS Comment Section              | `*===`
CSS Comment Subsection           | `*___`
CSS/JS Comment                   | `**`
CSS Comment: Variables           | `//var`
CSS Comment: Extends             | `//ext`
CSS Comment: Mixins              | `//mix`
CSS Comment: Positioning         | `//pos`
CSS Comment: Display & Box Model | `//dis`
CSS Comment: Other               | `//oth`
Less Em Conversion               | `@#`
Less Em Conversion (Alt)         | `@@`
Less New Base Text Size          | `@-`
Less New Base Text Size (Alt)    | `@_`
HTML Comment Section             | `!===`
HTML Comment Subsection          | `!___`
HTML Comment Block               | `!--`


<a name="less-comments"></a>
## Less/CSS Comments

### CSS Comment Section

**Trigger:** `*===`

As noted in [Motif's CSS coding style guide](https://github.com/MotifFramework/idiomatic-css#comments):

```css
/* ==========================================================================
   [Section]
   ========================================================================== */
```



### CSS Comment Subsection

**Trigger:** `*___`

As noted in [Motif's CSS coding style guide](https://github.com/MotifFramework/idiomatic-css#comments):

```css
/* [Subsection]
   ========================================================================== */
```


### Less/CSS Inline Comments

Inline comments are used to group and organize the style properties in your stylesheets. (See the [Motif coding style guide for declaration order](https://github.com/MotifFramework/idiomatic-css#declaration-order).)


#### Variables

**Trigger:** `//var`

```css
/* Vars */
@width: 20px;
```

#### Extends

**Trigger:** `//var`

```css
/* Extends */
&:extend(.class);
```

#### Mixins

**Trigger:** `//mix`

```css
/* Mixins */
.m-clearfix();
```

#### Positioning

**Trigger:** `//pos`

```css
/* Positioning */
position: absolute;
top: 0;
left: 50%;
```

#### Display & Box Model

**Trigger:** `//dis`

```css
/* Display & Box Model */
display: block;
margin: 0 auto;
padding: 20px;
width: @width;
```

#### Other

**Trigger:** `//oth`

```css
/* Other */
font-size: 20px;
color: #000;
background: #fff;
```

Put it all together:

```css
.selector {
    /* Vars */
    @width: 20px;

    /* Extends */
    &:extend(.class);

    /* Mixins */
    .m-clearfix();

    /* Display & Box Model */
    display: block;
    margin: 0 auto;
    padding: 20px;
    width: @width;

    /* Positioning */
    position: absolute;
    top: 0;
    left: 50%;

    /* Other */
    font-size: 20px;
    color: #000;
    background: #fff;
}
```



<a name="less-js"></a>
## Less/CSS/JavaScript Comments

**Trigger:** `**`

A DocBlock-style comment, as noted in [Motif's CSS coding style guide](https://github.com/MotifFramework/idiomatic-css#comments):

```css
/**
 * [Sentence-case text]
 */
```

<a name="less-conversions"></a>
Less Variable Conversion

### Em Conversion

**Trigger:** `@#`

A shortcut to bring up a formula to easily convert pixels to ems:

```less
@[1]px: (1em * ([1] / [@base-text-size]));
```

### Em Conversion (Alt)

**Trigger:** `@@`

Same as above, only it doesn't assume the variable name will be a number:

```less
@[name]: (1em * ([1] / [@base-text-size]));
```

### New Base Text Size

**Trigger:** `@-`

A shortcut to quickly set a new `@base-text-size` for the scope:

```less
@base-text-size: [@normal]-text-size;
```

### New Base Text Size (Alt)

**Trigger:** `@_`

Same as above, only it doesn't assume the variable will follow the `@[name]-text-size` pattern:

```less
@base-text-size: [@normal-text-size];
```




<a name="html-comments"></a>
## HTML Comments

### HTML Comment Section

**Trigger:** `!===`

As noted in [Motif's HTML coding style guide](https://github.com/MotifFramework/idiomatic-html#6-comments):

```html
<!--
 - ==========================================================================
 - [Section]
 - ==========================================================================
 -->
 ```

### HTML Comment Subsection

**Trigger:** `!___`

As noted in [Motif's HTML coding style guide](https://github.com/MotifFramework/idiomatic-html#6-comments):

```html
<!--
 - [Subsection]
 - ==========================================================================
 -->
 ```


### HTML Comment Block

**Trigger:** `!--`

As noted in [Motif's HTML coding style guide](https://github.com/MotifFramework/idiomatic-html#6-comments):

```html
<!--
 - [Comment block]
 -->
 ```

