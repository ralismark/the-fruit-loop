---
permalink: /about
---

# The Fruit Loop

The Fruit Loop is based on the [Wreath Webring Template](https://github.com/ralismark/wreath-webring-template), a template for building a [webrings](https://en.wikipedia.org/wiki/Webring) with Jekyll on GitHub Pages.

## Joining

To add a person to the webring, create a file in the `_ring` folder named `YOUR_NAME.html` -- this name won't be used anywhere except for in the URL of the navbar widget.
Its content should be like this:

```md
---
href: "<url>"
name: "<name>"
blurb: |
  <description>
---

<extra html>
```

where:

- `<url>` is the URL of their website, that links in the webring for your website will point to.
- `<name>` is the name shown in the navbar widget, and on the index page.
- `<description>` is a brief description, used in the listing on the index page.

You can also have a look at existing entries to see examples

## How to embed the navbar

Once you're part of this webring, it's highly recommended that you add the navbar widget to your website.
To do so, include the following html snippet, replacing `YOUR_NAME` with the username you registered with.

```html
<iframe
  style="
    width: 100%;
    max-width: 25rem;
    display: block;
    margin: 0 auto;
    height: 6rem;
    border: none;
  "
  src="{{ "/embed/YOUR_NAME" | absolute_url }}"
></iframe>
```

<!-- {{ "--" }}{{ ">" }}

Here's an example of what it looks like (with an added border so you can see the size):

<iframe
  style="
    width: 100%;
    max-width: 25rem;
    display: block;
    margin: 0 auto;
    height: 6rem;
    border: 1px solid grey;
  "
  src="{{ site.ring[0].url | absolute_url }}"
></iframe>

{{ "<!" }}{{ "--" }} -->

Feel free to tweak the style attribute -- these are just defaults that work for most people.

You can specify `<extra html>` to inject extra CSS to your widget to make it fit in better with your website.
