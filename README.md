Carbon
===

> **Note:** This project was made in an effort to better understand responsive design and CSS layout and is not intended for production use. I recommend using [flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) and/or [grid](https://css-tricks.com/snippets/css/complete-guide-grid/).

### A simple, lightweight and responsive CSS grid system

Carbon makes it easy to create complex layouts without the baggage of an entire framework. Carbon dynamically generates columns based on user specifications and supports both Stylus and Sass.


Getting Started
---

#### 1. Download

Clone the repository.

```
git clone https://github.com/colebemis/carbon.git
```

Or [download the .zip](https://github.com/colebemis/carbon/archive/master.zip). Then copy the desired stylesheet (`carbon.scss` or `carbon.styl`) into your project directory.

#### 2. Configure

Use the Sass and Stylus variables to customize the grid to fit your needs.

| Variable | Description |
| --- | --- |
|`$column-groups`| Controls number of column divisions (e.g. `$column-groups: (2, 3, 4)` will create a 2-, 3- and 4-column grid and allow for the use of small-n-of-2, small-n-of-3 and small-n-of-4 classes) |
|`$max-width`| Sets max-width of `.container`  |
|`$gutter`| Sets column gutter width |
|`$breakpoint-small`| Used in media queries to define seperation between small and medium screen sizes |
|`$breakpoint-medium`| Used in media queries to define seperation between medium and large screen sizes |

#### 3. Preprocess

Using the preprocessor of your choice, compile the stylesheet. Carbon currently supports Sass and Stylus, with Less support coming soon.

#### 4. Link the Stylesheet

Link the stylesheet in the `<head>` of your HTML document.

```html
<link rel="stylesheet" href="path/to/carbon.css">
```

#### 5. Add the Viewport Meta Tag

Place the following meta tag in the `<head>` of your HTML document. This enables use of media queries for cross-device layouts.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Usage
---
Carbon follows the same basic structure as many other grid systems.

```html
<div class="container">
    <div class="row">
        <div class="column small-1-of-3"> ... </div>
        <div class="column small-2-of-3"> ... </div>
    </div>
</div>
```

Carbon is mobile-first grid system, meaning code for small screens will be inhertited by larger screens unless otherwise specified.

Apply these simple classes to your HTML elements to create a beautiful and responsive layout.

| Class | Description |
| --- | --- |
| `.container` | Controls page max-width and centers page in window |
| `.row` | Contains `.column` elements |
| `.centered` | Can be combined with `.row` to center columns within the row |
| `.column` | Applies base styles for every column |



