---
layout: post
title: Getting Started With Sass - 2
subtitle: A Glimpse of Sass Features
tags: [HTML, CSS, Sass]
author: Ephraim Atta-Duncan
comments: False
---

<div align="center">
  <!-- img: educative.io -->
  <img src="/_posts/images/sass.png" alt="Sass Background">
</div>

# Sass

In the earlier part of this post, I talked about what Sass is and how to get started easily for a beginner programmer. You can find it [here](/dephraiim.github.io/2020/04/18/getting-started-with-sass.html). In this section, I assume you have set up your development environment and you are ready to get started coding with Sass.

<!-- Table of Contents -->

### Table Of Contents

- [Variables](#sass-variables)
- [Nesting](#sass-nesting)
- [Mixins](#sass-mixins)
- [Modules](#sass-modules)
- [Inheritance](#sass-extend)
- [Control Flow](#sass-control-flow)

### Sass Variables

Variables are just placeholders. They hold data for future use. Sass Variables are simple and very elegant. You can just assign a value to a variable name: the value can be a color name, hexadecimal value of a color, size in px or rem, virtually any data useful can be stored.

To assign a variable, prefix `$` infront of the variable name and that's it. It's that simple.

```scss
// Example Variable
// Assigning varible
$primary-color: #333;
$font-stack: Roboto, sans-serif;
$font-size: 1.2em;

// Using the variable

body {
  background: $primary-color;
  font: $font-stack $font-size;
}
```

Sass variables follow the same syntax as assigning a css property to a value `{$}{variable-name}: {value};`.

There are no special rules to Sass variables, they must be meaningful and they follow general variable rules. However, `-` and `_` are considered the same in sass.
For example, `$primary-color` and `$primary_color` are the same.

```scss
$text-color: #f0f0f0;

p {
  color: $text_color:
}

// No errors will be produced
```

> CSS also has variables, seperate from the Sass Variables. The two are not the same.

### Sass Nesting

When writing CSS, take a situation wherehy you are creating a navbar, with the nav tag and in the nav tag are a list each containing a link. To select a link to apply a style to it, you need to select ll the parent tags(for specificity) to get a style work on a specific tag. Sass makes your life easier. You can just write the code for the tag in the parent. That's nesting

```css
nav {
  display: flex;
  flex-direction: column;
  text-align: center;
}

nav li {
  list-style-type: none;
}

nav li a {
  text-decoration: none;
  text-transform: uppercase;
}
```

The above CSS can be written more easier in Sass and Sass will compile it to the same CSS above without any change and errors

```scss
nav {
  display: flex;
  flex-direction: column;
  text-align: center;

  li {
    // The li tag nested in the nav tag
    list-style-type: none;

    a {
      // The anchor tag now nested in the li tag
      // which is nested in the nav tag
      text-decoration: none;
      text-transform: uppercase;
    }
  }
}
```

You can also replace the tags with `id` and `classes`.

> If the property does not apply during nesting, try parent selectors `&`.

> The sytax for the parent selectors in nesting is by replacing the selector with the `&` symbol.

In applying nesting on pseudo-classes and pseudo-elements, you can apply the parent selector for much greater specificity. Also, the parent selector copies the parent name for the nested child.

```scss
section {
  display: grid;
  grid-template-colums: repeat(3, 1fr);

  &.container {
    // Selecting the container class in the section
    max-width: 1000px;
    width: 90%;
    margin: 0 auto;
  }
}
```

The Sass will compile to CSS like the one below,

```css
section {
  display: grid;
  grid-template-colums: repeat(3, 1fr);
}

section section.container {
  max-width: 1000px;
  width: 90%;
  margin: 0 auto;
}
```

To extend a `class` name or `id` name, you can use the parent selector for that too. Assuming we have a `.container` class and we have nested `.container-fluid` in the `.container` class, since both of the class names begin with `.container` and it wont be neceesary to type `.container` for the two class names. You can use the parent selector for it. As I said earlier, Sass makes your life much easier.

```scss
.container {
  max-width: 1000px;
  width: 80%;
  margin: 0 auto;

  &-fluid {
    //Selecting the .container
    width: 100%;
  }
}
```

The compiled CSS will be as below.

```css
.container {
  max-width: 1000px;
  width: 80%;
  margin: 0 auto;
}

.container .container-fluid {
  width: 100%;
}
```

### Sass Mixins

Sass mixins are just like mixins in Ruby and functions in JavaScript. You can type in reusable blocks of code into the mixin and reuse it over and over again. Mixins can take an argument or not, It is not compulsory.

> _Note_: Mixins are not he same as functions. Sass has functions too and the two are not the same.

The syntax to create a mixin is `@mixin <mixin-name> { ... }` or `@mixin <mixin-name>(< arguments...> ) { ... }`. To reuse the mixin after it has been created, you can just type `@include <mixin-name>` or `@include <mixin-name>( < arguments > )` at the place you want to include the mixin then it works. You can include the mixin more than once.

```scss
// Mixin without arguments
@mixin links {
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 3px;
}

// Including mixin
a {
  @include links;
}

// Mixin with arguments
@mixin button($color, $border-width, $padd-top, $padd-left) {
  color: $color;
  text-transform: uppercase;
  margin: 5px 10px;
  border: $border-width solid $color;
  padding: $padd-top $padd-left;
}

button {
  @include mixin(#000000, 5px, 10px, 20px);
}
```

> The order in which you arrange the arguments is not important. But when filling our the arguments with the values, it must be in the same order as you specified them, else you can interchange the value of one property with another.

> Sass Mixins and Functions are not the same.

#### Sass Functions

Sass Functions look similiar to mixins but different.
