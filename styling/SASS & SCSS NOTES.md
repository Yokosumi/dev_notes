
## how to install SASS

initialize a package.json. the (-y) parameter stands for yes for every option (quick setup)

```JavaScript
npm init -y
```

install sass with following line. the -D parameter stands for devDependencies

```JavaScript
npm install -D
```

## how to use SASS

one way is to write a script in `package.json` 

```JavaScript
"scripts": {
 "sass": "sass --watch file.scss:file.css"
}
```

to start sass use the following line

```JavaScript
npm run sass
```

## how to use variables

you can define color values of ex. hsl with variables to do mathematic operations.

use case: you have the same color with different shades or other values that slightly differ.

```SCSS
$hue: 50;
$comp-hue: $hue + 180;

$primary-color-dark: hsl($hue, 75%, 20%);
$primary-color: hsl($hue, 75%, 47%);
$complementary-color: hsl($comp-hue, 75%, 47%);
$primary-color-light: hsl($hue, 75%, 80%);
```



## how to use mixins

you can define mixins with the  `@mixins` rule, give it a name open curly-brackets and define properties that can be used multiple times.

```SCSS

@mixin font-style {
 color: red;
 font-weight: 600;
 font-family: monospace, sans-serif;
}

```

## mixin example

`@content`  at-rule enable code block for mixins

```SCSS
@mixin alert-text($color: #555, $border: 2px solid #333) {

  background-color: $color;

  color: black;

  font-variant: small-caps;

  padding: 0.5rem;

  width: fit-content;

  border: $border;

  background-color: $color;

  @content;

}

.error-text {
  @include alert-text(tomato);

}
.info-text {

  @include alert-text(lightblue, 2px dashed navy);

}
.normal-text {
  @include alert-text(white, null);
}

.faded-text {
  @include alert-text {
    opacity: 0.5;
    border: 0px;
  }
}
```


### selectors in mixin

additionally you can also put pseudo-elements like `:hover` , `:focus` , `:active` in a mixin to use it multiple times

```SCSS
@mixin states {
  &:hover {
    color: $main-color;
  }

  &:focus {
    background-color: black;
  }

  &:active {
    outline: 5px solid $main-color;
  }
}
```

## @include 

with the `@include` expression you can then use the previously defined mixin

```SCSS
p {
@include font-style;
}
a {
@include font-stlye;
}
```

## ampersand (&)

the `&` character references to the parent-selector, it is used when nesting selectors, it is used when a more specific selector is needed

```SCSS
.container {
  & .box {
    background-color: blue;
  }
}

```

## 7-1 folder structure
 
![[ohtheseven.png]]

## using variables

you need this star so you just can use the variables without delcare variables every time

```scss
	@use '/sass/base/variables' as *
	
```


