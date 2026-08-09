# Docsify Table of Contents

<p align="center">
  <img src="https://docsify.js.org/_media/icon.svg" />
  <br />
  <code>docsify-toc</code>
</p>


**Note**: I won't be adding features but feel free to add pull requests and if they work/pass tests I'll add them in.

## Changes in this fork

This fork includes fixes and a mobile UX improvement on top of the original plugin:

- **Fixed:** heading selectors with multiple comma-separated levels (e.g. the default `h1, h2`) weren't properly scoped to `scope`, so heading levels after the first could match elsewhere on the page.
- **Fixed:** the mobile layout forced the ToC (and page) to a fixed pixel width, which could force horizontal scrolling / a zoomed-out layout on narrow phone viewports.
- **Fixed:** a couple of edge cases in the list-building code that could throw when jumping between heading levels.
- **Added:** on mobile, the ToC is now a collapsible "On this page" accordion instead of an always-open list, so it no longer pushes page content down by a full screen's height before a reader reaches the article.

## To use
Add stylesheet
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/paulhibbitts/docsify-toc@master/dist/toc.css">
```

Add JS
```html
<script src="https://cdn.jsdelivr.net/gh/paulhibbitts/docsify-toc@master/dist/toc.js"></script>
```

Add settings
```js
window.$docsify = {
  toc: {
    scope: '.markdown-section',
    headings: 'h1, h2, h3, h4, h5, h6',
    title: 'On this page',
  },
}
```

# TODO
- [ ] Tests
- [ ] Example
- [x] ~Documentation~
