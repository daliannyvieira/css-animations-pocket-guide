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

A practical example:
We want to change the color of an element when you position the cursor over it.

```css
/* Adding a modification */
.element:hover {
      background-color: tomato;
}
```
But we want this change to happen smoothly. Then add a transition, with the modified property and the duration you want 1 second, for example:

```css
/* Adding transition */
.element {
     transition: background-color 1s;
}
```

![transitions example](../images/01.gif)

###More transitions

It's also possible to add more properties in a same transition separating them, and giving the same duration or not, for example:

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

We can add transformations to elements, scaling, rotating or moving them, in 2D and 3D. Existing transformations are: scale, rotate, translate and skew.

####Transform scale

Scale makes an element grow or shrink in dimension. Example: to make an element grow up in a proportion equivalent to half its size, we use scale(1.5); Were we wanting to make it double its size instead, we would use scale(2); and so it goes.

If we are dealing with hover scaling, for example, it may be interesting to continue combining transformations and transitions, making it way more enjoyable to see. We may use all to maintain the same duration per second in a transition. Example:

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

Rotate, as its name may suggest, is able to make an element spin. We can make it rotate using deg or turn as value, 1turn being equivalent to 360 degrees.

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

Translate moves the element in the X or Y axes from its original position. The offset value may be given in any of the CSS length units.

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

Skew is able to tilt and twist an element along the X and Y axes.

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
