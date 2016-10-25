![cover](../images/cover01.png)

All the [examples](http://codepen.io/collection/XmZvqo/) included in this guide are available on Codepen.

## Map

* [Introduction](#introduction)
    * [Recommendations](#recommendations)
* [Transitions](#transitions)
    * [More transitions](#more-transitions)
* [Transforms](#transforms)
    * [Transforms 2D](#transforms-2d)
        * [Transform scale](#transform-scale)
        * [Transform rotate](#transform-rotate)
        * [Transform translate](#transform-translate)
        * [Transform skew](#transform-skew)
    * [Transforms 3D](#transforms-3d)
        * [Transform rotateX](#transform-rotatex)
        * [Transform rotateY](#transform-rotatey)
        * [Transform rotateZ](#transform-rotatez)
* [Animations](#animations)
    * [Building](#building)
        * [Keyframe](#keyframe)
        * [Animation](#animation)
* [UI Examples](#ui-examples)
        
## Introduction

### Recommendations

## Transitions

```css
.element {
    transition: <property> <duration>;
}
```
    

```css
/* Adding a modification */
.element:hover {
      background-color: tomato;
}
```


```css
/* Adding transition */
.element {
     transition: background-color 1s;
}
```

![transitions example](../images/01.gif)

###More transitions

```css
/* Adding transitions */
.element {
    transition:
        background-color 1s,
        height 1s,
        width 1s,
        opacity 1s;
}

/* Adding a modification */
.element:hover {
    background-color: green;
    height: 70px;
    width: 70px;
    opacity: 0;
}
```

![More transitions](../images/02.gif)

##Transforms

###Transforms 2D

####Transform scale

```css
/* Adding transition */
.element {
    transition: all 1s;
}

/* Adding modification */
.element:hover {
    background-color: green;
    transform: scale(1.5);
}
```
    
![Transform scale](../images/03.gif)

####Transform rotate

```css
/* Adding transition */
.element {
    transition: all 1s;
}

/* Adding modification */
.element:hover {
    background-color: green;
    height: 70px;
    width: 70px;
    transform: rotate(360deg);
}
```

![Transform rotate](../images/04.gif)

####Transform translate

```css
/* Adding transition */
.element {
    transition: all 1s;
}

/* Adding modification */
.element:hover {
    background-color: green;
    transform: translateY(30px);
}
```

![Transform translate](../images/05.gif)

####Transform skew


```css
/* Adding more transition */
.element {
    transition: all 1s;
}

/* Adding more modifications */
.element:hover {
    background-color: green;
    transform: skew(0deg, 20deg);
}
```

![Transform skew](../images/07.gif)

###Transforms 3D

####Transform rotateX

```css
/* Adding more transition */
.element {
    transition: all 1s;
}

/* Adding more modifications */
.element:hover {
    background-color: green;
    transform: rotateX(90deg);
}
```

![Transform rotateX](../images/09.gif)
####Transform rotateY

```css
/* Adding more transition */
.element {
    transition: all 1s;
}

/* Adding more modifications */
.element:hover {
    background-color: green;
    transform: rotateY(180deg);
}
```

![Transform rotateY](../images/10.gif)
####Transform rotateZ

```css
/* Adding more transition */
.element {
    transition: all 1s;
}

/* Adding more modifications */
.element:hover {
    background-color: green;
    transform: rotateZ(90deg);
}
```

![Transform rotateZ](../images/11.gif)
##Animations

###Building

```css
/* Creating a keyframe */
@keyframes animacao {
    0% {
        transform: scale(0.9);
        opacity: 0;
    }
    50% {
        transform: scale(1.1);
        opacity: 1;
    }
    100% {
        transform: scale(1);
    }
}
```
    

```css
/* Adding an animation */
.element {
    animation: animacao 1s infinite;
}
```

![keyframes-animations](../images/06.gif)

###Keyframe

###Animation

###UI Examples
