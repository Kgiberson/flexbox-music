# flexbox-music


## Intro to the Flexbox Model
#### Fundamentals
Flex Container
: the parent element you've set ```display: flex``` on.

Flex Items
: the children elements within a Flex container.

### The Flex Container Properties

##### 1. Flex-direction
the ```flex-direction``` property controls the direction in which the flex items are laid along the main axis. Default value is ```row```.

```
ul {
  flex-direction: row || column || row-reverse || column-reverse;
}
```

##### 2. Flex-wrap
the ```flex-wrap``` defaults to ```no-wrap```, and can take on any of three values:

```
ul {
  flex-wrap: wrap || no-wrap || wrap-reverse;
}
```

##### 3. Flex-flow
the `flex-flow` is a shorthand property which takes `flex-direction` and `flex-wrap` values

```
ul {
  flex-flow: row wrap;
}
```

##### 4. Justify-content
defines how flex items are laid out on the main axis.
```
ul {
  justify-content: flex-start || flex-end || center || space-between || space-around;
}
```

##### 5. Align-items
defines how flex items are laid out on the cross axis.
```
ul {
  align-items: flex-start || flex-end || center || stretch || baseline;
}
```

##### 6. Align-content
defines how flex items are laid out on multi-line flex-containers.
```
ul {
  align-content: flex-start || flex-end || center || stretch;
}
```

### The Flex Item Properties
##### 1. Order
allows for reordering the flex items within a container.
```
  li:nth-child(1) {
    order: 1; /* give a value higher than 0 */
  }
```

##### 2. Flex-grow and flex-shrink
determine how much a flex-item should "grow" if there are spaces, or "shrink" if there are no extra spaces.

They take any values ranging from 0 to any positive number `0 || positive number`. '0' is default, and a "turn-off" switch.

##### 3. Flex-basis
specifies the initial size of a flex-item. Before the 'flex-grow' or 'flex-shrink' properties adjust its size to fit the container or not.

```
li {
  flex-basis: auto || ems || rems || pixels;
}
```

##### 4. The flex shorthand
sets flex-grow, flex-shrink, and flex-basis properties all at once. (GSB)

```
li {
  flex: 0 1 auto; /* default behavior of all flex-items */
}

li {
  flex: 0 0 auto; /* fixed width element whose initial width is based off of the content size */
}

li {
  flex: 1 1 auto;
  /* compute initial width automatically, but grow to fit the entire available space and shrink if necessary */
}

li {
  flex: 2 1 0;
  /* set the initial width of the flex item to zero, grow the item to fill the available space, and shrink item whenever possible */
}
```
