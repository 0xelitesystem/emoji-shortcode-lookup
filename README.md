# Emoji Shortcode Lookup

A searchable table mapping common emoji to their unicode code points and shortcodes (like :smile:). Search by name or shortcode, or paste an emoji to reverse-look-up its code points and shortcode. All data is embedded in the page.

**Live demo:** https://0xelitesystem.github.io/emoji-shortcode-lookup/

## Features

- Several hundred common emoji across categories: smileys, gestures, objects, symbols, and flags.
- Search by name (for example "rocket") or by shortcode (for example ":fire:").
- Reverse lookup: paste an emoji to see its name, shortcode, and code points. If it is not in the dataset, you still get its code points.
- Category filter.
- Each row shows the emoji, name, shortcode, and code point(s), plus a copy button for the emoji.
- Dark mode toggle, keyboard friendly.
- One file, all data inline, no external dependencies, works offline.

## How it works

The emoji dataset is a plain array embedded in the page, one entry per emoji with its name, shortcode, and category. Code points are computed at render time by iterating the string and reading each `codePointAt` value, so multi-code-point emoji (such as regional-indicator flag pairs) display every point. Reverse lookup checks whether your pasted text contains a known emoji, and always falls back to showing raw code points.

## Use

1. Type a name (for example `rocket`) or a shortcode (for example `:fire:`) into the search box.
2. Or paste an emoji to see its name, shortcode and code points.
3. Narrow the table with the category filter.
4. Click Copy on a row to copy that emoji.

## Why this exists

Looking up a shortcode or a code point should not need an account or a page full of ads. This is a single HTML file with the dataset inline, no tracking and no network requests, under the MIT license.

## Privacy

Everything runs in your browser from inline data. Your searches and pasted input never leave your machine. There are no external requests, no analytics, and no tracking.

If you use the theme toggle, your light or dark choice is saved in your browser's localStorage under the key `theme`. Nothing you paste or type is stored.

## Run locally

```
git clone https://github.com/0xelitesystem/emoji-shortcode-lookup
cd emoji-shortcode-lookup
```

Open `index.html` in a browser. Or serve the folder with `python -m http.server` and visit http://localhost:8000.

## Build

No build step. The whole tool is one `index.html` file with inline CSS and JavaScript, and no dependencies.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
