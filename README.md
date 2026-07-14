# Emoji Shortcode Lookup

A searchable table mapping common emoji to their unicode code points and shortcodes (like :smile:). Search by name or shortcode, or paste an emoji to reverse-look-up its code points and shortcode. All data is embedded in the page.

## Live demo

https://0xelitesystem.github.io/emoji-shortcode-lookup/

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

## Privacy

Everything runs in your browser from inline data. Your searches and pasted input never leave your machine. There are no external requests, no analytics, and no tracking.

## License

MIT. Copyright 0xelitesystem 2026.
