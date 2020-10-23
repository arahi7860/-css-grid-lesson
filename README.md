![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) **SOFTWARE ENGINEERING IMMERSIVE**

# CSS Grid

## Objectives

By the end of this lesson students will be able to:

- [ ] Explain when to use Flexbox vs. Grid
- [ ] Use proper terminology to refer to the different grid pieces

- [ ] Create layouts using CSS Grid

## The Concept Of Grid

Although `CSS Grid` wasn't available until 2017 the concept of `grid` isn't new. [Bootstrap](https://getbootstrap.com/docs/4.1/layout/grid/) was built on arranging content in rows and columns, essentially creating a grid.

### What is CSS Grid?

So far we've been using `Flexbox` to arrange content. It's very powerful and something we will continue to work with even with the introduction of CSS Grid. It is however only `one-dimensional`.

<img src="https://i.imgur.com/5NetjtO.png" width=500/>

CSS Grid Layout is a **two-dimensional layout** system (which means it includes both columns and rows).

<img src="https://i.imgur.com/55JCwW4.png" width=500/>

Both `Flexbox` and `CSS Grid` almost always work together with `CSS Grid` being applied to the overall layout and `Flexbox` to the content.

<img src="https://i.imgur.com/zO6XljL.png" width=500/>

<!-- ### Can I use Grid?

Yes as CSS Grid is supported on almost all modern browsers.

You can always check out [caniuse.com](http://caniuse.com/) to ensure that you are able to use Grid on a specific browser.

<img src="https://i.imgur.com/j1qTzte.png" /> -->

<!-- #### Browser Compatibility

Some browsers do require a specific prefix naming convention in order to apply certain properties so we can use [shouldiprefix](http://shouldiprefix.com/) to determine what those are and implement when and where needed, such as IE.

<img src="https://i.imgur.com/V7eggiG.png"> -->



### Basic Terminology

Here are some of the terms we will need to understand when working with CSS Grid.

-   **Grid container** - An container element that defines a grid-formatting context for its contents.

-   **Grid item** - Each child element of a grid container is a grid item

-   **Grid track** - A continuous run between two adjacent grid lines. A grid row or column.

-   **Grid cell** - Any space bounded by four grid lines, with no grid lines running through it.

-   **Grid area** - Any rectangular area bounded by four grid lines and made up of one or more grid cells.

<!-- <img src="https://imgur.com/41BYy6R.png" width=600/> -->

## Working With CSS Grid

Grid is the most robust layout system in CSS. You utilize Grid by applying CSS rules to both the parent `(Grid Container)` and it's children `(Grid Items)`, much like we did with Flexbox.

During the lecture we will reference [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) as our go to guide so let's spend a few minutes taking a look at the docs before moving on.

## Implementation: Holy Grail Layout

Let's take a few minutes to explore this [web app](https://www.inprnt.com/discover/) built with Grid layout.

> This site was built by a former GA student using CSS-Grid layout, Flexbox, and React.

There are a few ways to implement css grid. We will focus on the following:

1. To start, you must have a **container** (or **parent**) element, with at least one **nested** (or **child**) elements inside.

```html
<div class="parent">
    <div class="child" id="one">1</div>
    <div class="child" id="two">2</div>
    <div class="child" id="three">3</div>
    <div class="child" id="four">4</div>
    <div class="child" id="five">5</div>
</div>
```

2. On the container, specify that you are using `display: grid` and what your **_template_** will look like - more specifically, your **_rows_** and **_columns_**. Here's an example.

```css
.parent {
    display: grid;
    grid-template-rows: 100px 600px 100px;
    grid-template-columns: 1fr 3fr 1fr;
}
```

`fr` represents `fraction`, it's a unit that will evenly span the remainder of the space.

Here we have specified **_3 rows_**, taking up 100, 600, and 100 pixels respectively. We also specified **_3 columns_**, giving us a total of **_9 cells_**. `grid-template` also takes other units like `%`, `rem`, and `auto`. For now we will focus on `px` and `fr` units. You can also use `repeat` to specify multiple rows or columns of one size like this `repeat(5, 1fr)`

3. the _child_ elements, you can specify _where_ the _cells_ are located and the _size_ you want them to be. I like to follow this pattern...

```css
selector {
    grid-row: where-to-start / span size;
}
```

> same would work for `grid-column`

So something like this on a _child_ element for example the header...

```css
#one {
    grid-row: 1 / span 1;
    grid-column: 1 / span 3;
}
```

This element takes up 1 row, starting at row 1, and takes up 3 columns, starting at column 1.

We could also write `grid-row: 1;` for short, if your element only spans 1 row.

### Great Resources:

-   [CSS Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

-   [Grid Garden](https://cssgridgarden.com/)

-   [Css Grid - Scrimba](https://scrimba.com/learn/R8PTE)
