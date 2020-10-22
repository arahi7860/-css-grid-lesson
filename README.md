![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) SOFTWARE ENGINEERING IMMERSIVE

# CSS Grid

## The Concept Of Grid

Although `CSS Grid` wasn't available until 2017 the concept of `grid` isn't new. [Bootstrap](https://getbootstrap.com/docs/4.1/layout/grid/) was built on arranging content in rows and columns, essentially creating a grid.

### What is CSS Grid?

So far we've been using `Flexbox` to arrange content. It's very powerful and something we will continue to work with even with the introduction of CSS Grid. It is however only `one-dimensional`.

<img src="https://i.imgur.com/5NetjtO.png" width=500/>

CSS Grid Layout is a **two-dimensional layout** system (which means it includes both columns and rows).

<img src="https://i.imgur.com/55JCwW4.png" width=500/>

Both `Flexbox` and `CSS Grid` almost always work together with `CSS Grid` being applied to the overall layout and `Flexbox` to the content.

<img src="https://i.imgur.com/zO6XljL.png" width=500/>

### Can I use Grid?

Yes as CSS Grid is supported on almost all modern browsers.

You can always check out [caniuse.com](http://caniuse.com/) to ensure that you are able to use Grid on a specific browser.

<img src="https://i.imgur.com/j1qTzte.png" />

#### Browser Compatibility

Some browsers do require a specific prefix naming convention in order to apply certain properties so we can use [shouldiprefix](http://shouldiprefix.com/) to determine what those are and implement when and where needed, such as IE.

<img src="https://i.imgur.com/V7eggiG.png">

## Working With CSS Grid

Grid is the most robust layout system in CSS. You utilize Grid by applying CSS rules to both the parent `(Grid Container)` and it's children `(Grid Items)`, much like we did with Flexbox.

During the lecture we will reference [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) as our go to guide so let's spend a few minutes taking a look at the docs before moving on.

### Basic Terminology

Here are some of the terms we will need to understand when working with CSS Grid.

-   **Grid container** - An element that defines a grid-formatting context for its contents. (Parent)

-   **Grid item** - An element that participates in grid layout within a grid-formatting context. (Children)

-   **Grid track** - A continuous run between two adjacent grid lines. A grid row or column.

-   **Grid cell** - Any space bounded by four grid lines, with no grid lines running through it.

-   **Grid area** - Any rectangular area bounded by four grid lines and made up of one or more grid cells.

<img src="https://imgur.com/41BYy6R.png" width=600/>
