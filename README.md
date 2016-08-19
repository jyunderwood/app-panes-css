# App Panes

To demonstrate using [flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout) to quickly mock up application interfaces that have the same UI structure of an iCloud web app.

![App Panes Demo](https://raw.githubusercontent.com/jyunderwood/app-panes-css/master/screenshot.png)

[View Live Demo](http://jyunderwood.github.io/app-panes-css)

## CSS class overview

```css
.pane
.pane.pane--application /* To take up 100% of the viewport */
.pane.pane--details     /* Doubles the width of the pane */

/* Pane Child Elements */

.pane__bar             /* Toolbar for a pane's header or footer */
.pane__outlet          /* A container for nesting panes */
.pane__content         /* A container for content */
```

Some neat pseudo selector usages:

- Borders for `.pane__bar` change because of `.pane > .pane__bar:first-child` or `.pane > .pane__bar:last-child` so you don't need to express anything else like "header" or "footer." Note, just `.pane__bar:first-child` won't work, you need a parent selector, too.

- Sibling panes get a left border when needed thanks to `.pane:nth-child(n+2)`.
