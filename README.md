# Responsive websites with Bootstrap

This is the example developed by Mark Zamoyta in his course _Responsive websites
with Bootstrap 3_ on [PluralSight](https://app.pluralsight.com/library/courses/responsive-websites-bootstrap3).  
It is not directly his course's material but what I created alonside the course,
so it might contain personal interpretations or experimentations.


## Patterns for Responsive Design

### Mostly Fluid pattern

Stacks content-first for XS, same 3-cols layout for SM+.

_Note:_ Remember to construct HTML with mobile in mind (Bootstrap is mobile-first).
It is preferable for mobile users that the content is the first section.  
Then push / pull columns for "sm" media and above with `col-sm-push-*` and
`col-sm-pull-*` _(I made a separate branch to try it with_ `order-` _classes in
Bootstrap 4)_.

### Column Drop pattern

XS stacks all 3 columns. SM displays 2 of them, stacks the 3rd below. MD+ displays
all 3 in a row.

### Layout Shifter pattern

Same as _Column Drop_ but this time, for MD displays alone, we place the links
in a header row. So that now:
- XS: 3 stacks
- SM: 2 cols + 1 (stacked)
- MD: 1 separate row (header) + 2 cols
- LG+: 3 cols

**Drawback:** the links section has to be duplicated in the HTML code as the
layout is not flexible enough to render this without JavaScript code.

### Content Reflow pattern

Use CSS3 media queries to "reflow the content" of the range list when width is
small.  
In other words, when stacked as a single column the links are now displayed
with smaller images with the text aside, instead of (bigger) images and the text
below.
