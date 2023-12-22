# BOOTSTRAP NOTES

## 1. Bootstrap Containers

# **Creating Containers with Bootstrap**

Containers are the most basic layout element in Bootstrap and are required when using the grid system. Containers are basically used to wrap content with some padding. They are also used to align the content horizontally center on the page in case of fixed width layout.

Bootstrap provides three different types containers:

- `.container`, which has a max-width at each responsive breakpoint.
- `.container-fluid`, which has 100% width at all breakpoints.
- `.container-{breakpoint}`, which has 100% width until the specified breakpoint.

The table below illustrates how each container's max-width changes across each breakpoint.

| Bootstrap  Grid System | X-Small<576px | Small≥576px | Medium≥768px | Large≥992px | X-Large≥1200px | XX-Large≥1400px |
| --- | --- | --- | --- | --- | --- | --- |
| .container | 100% | 540px | 720px | 960px | 1140px | 1320px |
| .container-sm | 100% | 540px | 720px | 960px | 1140px | 1320px |
| .container-md | 100% | 100% | 720px | 960px | 1140px | 1320px |
| .container-lg | 100% | 100% | 100% | 960px | 1140px | 1320px |
| .container-xl | 100% | 100% | 100% | 100% | 1140px | 1320px |
| .container-xxl | 100% | 100% | 100% | 100% | 100% | 1320px |
| .container-fluid | 100% | 100% | 100% | 100% | 100% | 100% |

# **Fluid Containers**

You can use the `.container-fluid` class to create a full width container. The width of the fluid container will always be 100% irrespective of the devices or screen sizes.

```html
<div class="container-fluid">
    <h1>This is a heading</h1>
    <p>This is a paragraph of text.</p>
</div>
```

# **Specify Responsive Breakpoints for Containers**

Since Bootstrap v4.4, you can also create containers that is 100% wide until the specified breakpoint is reached, after which max-width for each of the higher breakpoints will be applied.

For example, `.container-xl` will be 100% wide until the xl breakpoint is reached (i.e., viewport width ≥ 1200px), after which max-width for xl breakpoint is applied, which is 1140px.

```html
<div class="container-sm">100% wide until screen size less than 576px</div>
<div class="container-md">100% wide until screen size less than 768px</div>
<div class="container-lg">100% wide until screen size less than 992px</div>
<div class="container-xl">100% wide until screen size less than 1200px</div>
```

## Card

A **card** is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options. If you’re familiar with Bootstrap 3, cards replace our old panels, wells, and thumbnails. Similar functionality to those components is available as modifier classes for cards.

```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

## ****Bootstrap Grid System****

Bootstrap grid system provides an easy and powerful way to create responsive layouts of all shapes and sizes. It is built with [flexbox](https://www.tutorialrepublic.com/css-tutorial/css3-flexible-box-layouts.php) with mobile-first approach. Also, it is fully responsive and uses twelve column system (12 columns available per row) and six default responsive tiers.

# **Creating Column Layouts**

The following example will show you how to create two column layouts for medium, large and extra large devices like tables, laptops and desktops etc. However, on mobile phones (screen width less than 768px), the columns will automatically become horizontal (2 rows, 1 column).

```html
<div class="container">
    <!--Row with two equal columns-->
    <div class="row">
        <div class="col-md-6">Column left</div>
        <div class="col-md-6">Column right</div>
    </div>
    
    <!--Row with two columns divided in 1:2 ratio-->
    <div class="row">
        <div class="col-md-4">Column left</div>
        <div class="col-md-8">Column right</div>
    </div>
    
    <!--Row with two columns divided in 1:3 ratio-->
    <div class="row">
        <div class="col-md-3">Column left</div>
        <div class="col-md-9">Column right</div>
    </div>
</div>
```

# **Column Wrapping Behavior**

Now we are going to create more flexible layouts that changes the column orientation based on the viewport size. The following example will create a three column layout on large devices like laptops and desktops, as well as on tablets (e.g. Apple iPad) in landscape mode, but on medium devices like tablets in portrait mode (768px ≤ screen width < 992px), it will change into a two column layout where the third column moves at the bottom of the first two columns.

```html
<div class="container">
    <div class="row">
        <div class="col-md-4 col-lg-3">Column one</div>
        <div class="col-md-8 col-lg-6">Column two</div>
        <div class="col-md-12 col-lg-3">Column three</div>
    </div>
</div>
```

## ****Alignment of Grid Columns****

You can use the flexbox alignment utilities to vertically and horizontally align grid columns inside a container. Try out the following examples to understand how it works:

### **Vertical Alignment of Grid Columns**

You can use the classes `.align-items-start`, `.align-items-center`, and `.align-items-end` to align the grid columns vertically at the top, middle and bottom of a container, respectively.

```html
<div class="container">
    <div class="row">
        <div class="col align-self-start">Column one</div>
        <div class="col align-self-center">Column two</div>
        <div class="col align-self-end">Column three</div>
    </div>
</div>
```

### **Horizontal Alignment of Grid Columns**

You can use the classes `.justify-content-start`, `.justify-content-center`, and `.justify-content-end` to align the grid columns horizontally at the left, center and right of a container, respectively. Let's check out the following example to see how it works:

```html
<div class="container">
    <div class="row justify-content-start">
        <div class="col-4">Column one</div>
        <div class="col-4">Column two</div>
    </div>
    <div class="row justify-content-center">
        <div class="col-4">Column one</div>
        <div class="col-4">Column two</div>
    </div>
    <div class="row justify-content-end">
        <div class="col-4">Column one</div>
        <div class="col-4">Column two</div>
    </div>
</div>
```