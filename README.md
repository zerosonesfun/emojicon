# emojicon

Tiny vanilla JS drop-in that turns emoji in page text into text emoticons / kaomoji.

## Install

```html
<script src="emojicon.js" defer></script>
```

It runs on load and watches for new text incase of ajax/SPA.

## What it does in more detail

- Replaces mapped emoji in text nodes (`(^_^)`, `<3`, `ᕙ(≧▽≦)ᕗ`, etc.)
- Leaves unmapped emoji alone
- Skips `script`, `style`, `noscript`, form fields, `contenteditable`, and code-ish tags (`code`, `pre`, `kbd`, `samp`)

## Where the emoji list comes from

Emoji are taken from Unicode's official emoji test data:

https://unicode.org/Public/emoji/latest/emoji-test.txt

## Manual re-scan

```js
emojicon.run();           // whole body
emojicon.run(someElement) // one subtree
```

## Demo

Open `demo.html` in a browser.