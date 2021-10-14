# Remark Slug Anchor

Automatically append anchor tags to your header elements.

<br>

Your code:
```md
# Hello World
```

Your page:

![](https://i.imgur.com/f04B9Bl.png)

<br>

## Install

This package is [ESM only](https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c):
Node 12+ is needed to use it and it must be `import`ed instead of `require`d.

```bash
npm install remark-slug-anchor remark-slug
```

You can now use this along with `remark-slug` (must use), you can find an example [here](https://www.npmjs.com/package/remark-slug) of how to use `remark-slug` - include this package in the same way

You also need to import that css file, if you are using a preprocessor/bundler you can import from the package `remark-slug-anchor/dist/anchor.css`, if not use the cdn:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/remark-slug-anchor@0/dist/anchor.css" />
```

# Options / Styling

We had to switch from embedding a svg to inline and due to that limitation styling isn't really possible on the svg itself

To pass in options do this:
```js
import remarkSlugAnchor from 'remark-slug-anchor';
import remarkSlug from 'remark-slug';

const plugins = [
    remarkSlug,
    [remarkSlugAnchor, { /* options */ }]
]
```

Options:

- `color`:<br />
    You can set the color of the anchor (if using built in anchor) with this option

    > NOTE: You must use an absolute colour, you are unable to use something like `var(--color)`, anything like rgb, rgba, hex, built ins, etc are supported

- `icon`: <br />
    You can pass in your own **svg** icon, with this option

    > Must be a string as it's encoded to be used as an anchor