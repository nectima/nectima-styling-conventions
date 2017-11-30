# Nectima Styling Conventions

This repository is a reference for styling conventions and best practices used at Nectima AB. 

## Table of Contents

- [Introduction](#introduction)
- []

## Introduction

Styling complex projects is team effort that requires collaboration between multiple designers and developers. Furthermore, many of Nectima's projects are later turned over to other development teams, which must continue or improve upon our own work. This only serves to emphasize the importance of a clean, systematic and structured approach to front-end development.

This document serves as a guide to new developers (as well as a reference to all Nectima team members) of how we choose to implement styling in front-end projects. As in life, there are always exceptions to the rule, but by following these guidelines we can make reading and writing code easier, faster and more maintainable for everyone. We want to create applications that are both beautiful to look at and painless to scale. :heart:

---
## Tools
### SCSS

At Nectima most projects use [SCSS](http://sass-lang.com/) in lieu of simple CSS. SCSS is a superset of CSS which means that everything you know about CSS can still be applied in SCSS code, but this extension has powerful features which make the development process faster and easier.

If you are new to SASS or need a review, checkout these resources:

- [Sass Basics](http://sass-lang.com/guide)

- [Learn Sass In 15 Minutes (Tutorial)](https://tutorialzine.com/2016/01/learn-sass-in-15-minutes)

- [Learn the Best and Most Useful SCSS (Tutorial)](https://egghead.io/courses/learn-the-best-and-most-useful-scss)

In any given project nearly all SCSS features are used, so it's important that you have a good understanding of the language.

### Compilers 
(todo)

### Linters
(todo)

### IDE Extensions
(todo)

---

## Implementation Guidelines

### Using Libraries

Most projects have initial styling dependencies. In the best case, these third-party libraries also use Sass so that importing and extending them is easy and painless.

The most common library used is Twitter's [Bootstrap](https://getbootstrap.com/).

### Reusability v. Speed

All projects should start with an period of styling smaller reusable components rather than immediately focusing on developing screens. For example, add a simple design page and dedicate one or more days to writing and styling simple elements such as headers, buttons, form fields, containers, etc. This will allow you to implement styling in isolation from context and have a reference for elements and class names later in the development process.

See an example of a design page with components [here](design-page.png).

This workflow requires a little more time at the beginning of a project, but speeds up the process significantly later on. Plus having a dedicated page as a component reference enforces consistency and prevents developers from unecessarily restyling components.

### Naming

All class names should be in English and written in all (lowercase) kebab-case across the entire project. The only exception to this rule is when it is necessary to override existing styling by third-party libraries.

```css
// GOOD
.class-name {
    ...
}

// BAD
.className,
.ClassName,
.class_name,
.Class-Name,
.klass-namn {
    ...
}
```

Try to extend upon existing class name conventions. If a class name uses an abbreviation it should be uniform across the project. For example **Bootstrap** uses `btn` as an abbreviation for "button." If you write a custom class name for a button element it should follow this convention as well. 

For example, because the button identifier is prefixed by `btn` (as in `btn-primary` or `btn-sm`) you should do this:

```css
// GOOD
.btn-cool {
    ...
}

// BAD
.cool-btn,
.button-cool {
    ...
}
```

### Selectors

Our styling is written using primarily element and class names. In rare cases we use ids, but this makes overriding code difficult. If more specificity is required consider using one of the following lesser known selectors:

| Selector              | Example               | Description
| --                    | --                    | --
| \>                    | div \> p              | Selects all `<p>` elements where the parent is a `<div>` element
| element+element       | div + p               | Selects all `<p>` elements that are placed immediately after `<div>` elements
| element1~element2     | div ~ p               | Selects every `<ul>` element that are preceded by a `<p>` element
| \[attribute\] | \[target\] | Selects all elements with a target attribute
| \[attribute=value\] | \[target=_blank\] | Selects all elements with target="_blank"
| \[attribute~=value\] | \[title~=flower\] | Selects all elements with a title attribute containing the word "flower"
| \[attribute\|=value\] | \[lang\|=en\] | Selects all elements with a lang attribute value starting with "en"
| \[attribute^=value\] |  a\[href^="https"\] | Selects every `<a>` element whose href attribute value begins with "https"
| \[attribute$=value\] |  a\[href$=".pdf"\] | Selects every `<a>` element whose href attribute value ends with ".pdf"
| \[attribute*=value\] |  a\[href*="w3schools"\] | Selects every `<a>` element whose href attribute value contains the substring "w3schools"
| :first-child          | p:first-child         | Selects every `<p>` element that is the first child of its parent
| :nth-child(n)         | p:nth-child(3)        | Selects every `<p>` element that is the third child of its parent
| :nth-last-child(n)    | p:nth-last-child(2)   | Selects every `<p>` element that is the second to last child of its parent
| :last-child           | p:last-child          | Selects every `<p>` element that is the last child of its parent
| :first-of-type        | p:first-of-type       | Selects every `<p>` element that is the first `<p>` element of its parent
| :nth-of-type(n)       | p:nth-of-type(2)      | Selects every `<p>` element that is the second `<p>` element of its parent
| :nth-last-of-type(n)  | p:nth-last-of-type(3) | Selects every `<p>` element that is the third to last `<p>` element of its parent
| :last-of-type         | p:last-of-type        | Selects every `<p>` element that is the last `<p>` element of its parent

For a complete reference look to [W3 Schools](https://www.w3schools.com/cssref/css_selectors.asp).
## Units
stick to rem
## Tips and Tricks
- using +
- mixins
## Comments and Labeling
## Browser Compatability
- no flex
- no css grid
## Other
- no !important

## Directory Structure
asdfasdasdf












### Contributors

Axel Yung (Developer)