# Additional HTML Controls

## Introduction

The next step of the implementation is to add controls to our existing
application. We will be using the following controls:

1. Buttons
2. Dropdown menu
3. Badge (to represent the user's avatar)
4. Checkbox
5. Label
6. Input box

For this section, we will go through adding controls to the first panel, and
then we will go over each other type of control and ask you to add them yourself
based on what you will have learned up to that point.

## Buttons

To take full advantage of Bootstrap styling, we should not use colors directly.
Instead, we use `primary` and `secondary` to designate colors within a theme,
and could later control which colors are in our entire application by simply
changing the theme. And while managing themes is beyond the scope of this
course, the use of Bootstrap's color scheme is still a good habit to get into.

We can add a button to our "header" component with the following simple HTML:

```html
<button>Logout</button>
```

To add Bootstrap styling, we add 2 classes:

```html
<button class="btn btn-primary">Logout</button>
```

We also need to add the welcome message for "Claire", who is the mock user we
are assuming is logged at the moment. We can do with a simple header tag:

```html
<h2>Welcome, Claire</h2>
```

Now let's use Bootstrap's layout capabilities to put these 2 components in the
right place on the UI:

```html
<div class="container">
  <div class="row">
    <div class="col-9 p-3">
      <h2>Welcome, Claire</h2>
    </div>
    <div class="col-3 p-3 float-end">
      <div class="float-end">
        <button class="btn btn-primary">Logout</button>
      </div>
    </div>
  </div>
</div>
```

Let's break this code down:

1. We remove the "component works" default text
2. We create an overall `container` `div` for the content in our component
3. We have a single `row` of content, so we create a `div` for that
4. We have 2 `col`umns of content, so we create a `div` each for that
5. We give the first `col` most of the width (9 cells) of the container for the
   welcome message
6. We give the second `col` the rest of the width (3 cells) of the container for
   the "logout" button
7. We put the button in a `div` with the `float-end` class so that it's "right
   aligned" in that 3-column space
8. We remove all `border` classes, since we no longer need to detail out the
   layout (for this section)

> Note: continue to remove the `border` classes, as you add the actual elements
> to your views
