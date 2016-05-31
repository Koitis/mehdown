mehdown
=======

The Markdown parser used on the forums at meh.com.

## Adds the following features to Markdown:

- Converts URL-like text to links.
- Converts image URLs to images.
- Optionally detects image sizes.
- External links open in a new browser tab/window.
- Automatic detection of `@usernames`.
- Support for [tables in GitHub Flavored Markdown syntax](https://help.github.com/articles/organizing-information-with-tables/).
- Typographic replacements for `(c) (r) (tm) (p) +- ... !!! ??? --`.
- “Smartypants, double quotes” and ‘single quotes’
- Support for strikethrough using the `~~strikethrough~~` syntax.
- Support for adding anchors to headers.
- Better linebreak/newline support.

## Emoji

- Supports common emoji :shortnames:.
- Supports native unicode emoji: 😄.
- Supports ASCII smileys: :).

## Turns URLs from many popular sites into HTML embeds:

- Image URLs are converted to images.
- imgur GIFV URLs are converted to high quality looping GIF videos.
- Kickstarter URLs are converted to campaign previews.
- Reddit permalink URLs are converted to embeddable comment threads.
- SoundCloud URLs are converted to audio players.
- Twitter status URLs are converted to embeddable tweets.
- Vimeo URLs are converted to video players.
- Vine URLs are converted to video players.
- YouTube URLs are converted to video players.

## Supports /commands:

- `/giphy [text]` - Post a random GIF
- `/shrug` - ¯\\\_(ツ)\_/¯

## Supports a subset of BBCode tags

- `[b], [code], [i], [img], [quote], [s], [url], [youtube]`

## Usage

```
var mehdown = require('mehdown');

mehdown.render('markdown text here', { baseUrl: 'https://meh.com', commands: true, detectImageSizes: false }, function(err, html) {
    console.log(html);
});
```
