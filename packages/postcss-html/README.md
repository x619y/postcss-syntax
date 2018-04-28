PostCSS HTML Syntax
====

[![NPM version](https://img.shields.io/npm/v/postcss-html.svg?style=flat-square)](https://www.npmjs.com/package/postcss-html)

<img align="right" width="95" height="95"
	title="Philosopher’s stone, logo of PostCSS"
	src="http://postcss.github.io/postcss/lib/logo.svg">

[PostCSS](https://github.com/postcss/lib/postcss) syntax for parsing HTML (and HTML-like)
- [PHP](http://php.net)
- [Vue component](https://vue-loader.vuejs.org/)
- [Quick App](https://doc.quickapp.cn/framework/source-file.html)

## Getting Started

First thing's first, install the module:

```
npm install postcss-syntax postcss-html --save-dev
```

## Use Cases

```js
const postcss = require('postcss');
const syntax = require('postcss-html')({
	// syntax for parse scss (non-required options)
	scss: require('postcss-scss'),
	// syntax for parse less (non-required options)
	less: require('postcss-less'),
	// syntax for parse css blocks (non-required options)
	css: require('postcss-safe-parser'),
});
postcss(plugins).process(source, { syntax: syntax }).then(function (result) {
	// An alias for the result.css property. Use it with syntaxes that generate non-CSS output.
	result.content
});
```

If you want support SCSS/SASS/LESS/SugarSS syntax, you need to install these module:

- SCSS: [PostCSS-SCSS](https://github.com/postcss/lib/postcss-scss)
- SASS: [PostCSS-SASS](https://github.com/aleshaoleg/postcss-sass)
- LESS: [PostCSS-LESS](https://github.com/shellscape/postcss-less)
- SugarSS: [SugarSS](https://github.com/postcss/lib/sugarss)

## Advanced Use Cases

See: [postcss-syntax](../postcss-syntax)

### Style Transformations

The main use case of this plugin is to apply PostCSS transformations to `<style>` tags and `<div style="*">` property in HTML (and HTML-like).