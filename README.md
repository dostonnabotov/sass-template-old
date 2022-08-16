# Sass Template

## Table of Contents

- [About](#about)
- [Prerequisites](#prerequisites)
- [Process](#process)
  - [Install](#install)
  - [Run](#run)
- [Structure](#structure)
  - [Folders & Files](#folders--files)
  - [Comments](#comments)
- [Resources](#resources)
- [References](#references)

## About

First of all, I didn't invent new rules, methods or anything. It is just the combination of 7-1 folder structure from [Sass Guidelines](https://sass-guidelin.es/) and [@forward and @use](https://www.youtube.com/watch?v=CR-a8upNjJ0) method by Kevin Powell with some modifications on them. So, if you know these two, it's great! You can easily use this template in your Sass projects. However, if you are unaware of them, I highly recommend you to check out these two and come back to this template.

## Prerequisites:

A basic understanding of:

- 7-1 folder structure
- `@forward` and `@use`
- `@each`, `@if` and `@else` rules
- `maps`, `@mixin` and `variables`

## Process

### Install

If you don't have Sass installed on your computer, you can install it by running `npm install -g sass` in the command line. It will install it globally on your computer. If you want to use Sass only for this project and don't want to use globally, you can run `npm install sass --save-dev`. It will install node_modules in order for Sass to compile your code into CSS.

### Run

After installation, run

`npm run dev`

Congrats! Sass is watching for changes.

## Structure

### Folders & Files

```
sass/
|
|- abstracts/
|    |- _variables.scss
|    |- _colors.scss
|    |- _type.scss
|    |- _media-query.scss
|    ...
|    |- _index.scss
|
|- base/
|    |- _root.scss
|    |- _reset.scss
|    |- _base_.scss
|    ...
|    |- _index.scss
|
|- vendors/
|    |- _modern-reset.scss
|    ...
|    |- _index.scss
|
|- utilities/
|    |- _composition.scss
|    |- _typography_.scss
|    |- _colors__.scss
|    |- _exceptions.scss
|    ...
|    |- _index.scss
|
|- components/
|    |- _buttons.scss
|    ...
|    |- _index.scss
|
|- layout/
|    |- _header.scss
|    |- _forms.scss
|    |- _sidebar.scss
|    |- _footer.scss
|    ...
|    |- _index.scss
|
|- pages/
|    |- _about.scss
|    |- _contact.scss
|    ...
|    |- _index.scss
|
|- themes/
|    |- _theme.scss
|    |- _admin.scss
|    ...
|    |- _index.scss
|
|- _shame.scss
|
|- style.scss
```

If you have created a file in one of these folders (except `abstracts/`) and run into a problem that says "Undefined variable" or "Undefined mixin", make sure that at the top of your file. you have this line of code: `@use "../abstracts" as *;`.

Aslo, when it doesn't compile your code in CSS, make sure that you have forwarded them in `_index.scss` file in the same folder.

### Comments

Block comments:

```
/* ==============================
 * Components | Buttons
 * ------------------------------ */
```

Inline comments:

```
/* primary
============== */
```

> ATTENTION! Do not include block or inline comments in files located in the `abstracts/` folder. Becuase nothing from `abstracts/` folder is compiled in CSS, while comments will.

## Resources

### Must-know

- [Sass Guidelines](https://sass-guidelin.es/)
- [@forward and @use](https://www.youtube.com/watch?v=CR-a8upNjJ0) explained by Kevin Powell

### Useful

- [CUBE CSS](https://cube.fyi/)
- [Custom Props & Utility Classes with Sass](https://www.youtube.com/watch?v=gP8yFWCTr7Q) by Kevin Powell

## References

- [.sr-only](https://gist.github.com/ffoodd/000b59f431e3e64e4ce1a24d5bb36034)
- [Logo](https://github.com/sass/sass-site/blob/main/source/assets/img/logos/logo.svg) from [Sass official site](https://sass-lang.com/)
