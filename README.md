# Svelte SEO

[![Build Status](https://travis-ci.org/artiebits/svelte-seo.svg?branch=master)](https://travis-ci.org/artiebits/svelte-seo)

Svelte SEO is a plugin that makes managing your SEO easier in Svelte projects.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Installing](#installing)
- [Usage](#usage)
  - [Add SEO to Page](#add-seo-to-page)
  - [Open Graph](#open-graph)
    - [Basic Example](#basic-example)
    - [Article Example](#article-example)
- [Acknowledgements](#acknowledgements)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Installing

Install using `yarn`:

`yarn add svelte-seo`

or `npm`:

`npm install --save svelte-seo`

## Usage

### Add SEO to Page

Import Svelte SEO and add the desired properties. This will render out the tags in the `<head>` for SEO. At a bare minimum, you should add a title and description.

```svelte
<script>
  import SvelteSeo from "svelte-seo";
</script>

<SvelteSeo
  title="Simple Usage Example"
  description="A short description goes here."
/>
```

### Open Graph

For the full specification please check out http://ogp.me/

Svelte SEO currently supports:

- [basic](#basic-example)
- [article](#article-example)

#### Basic Example

```svelte
<script>
  import SvelteSeo from "svelte-seo";
</script>

<SvelteSeo
  openGraph={{
    title: 'Open Graph Title',
    description: 'Open Graph Description',
    url: 'https://www.example.com/page',
    type: 'website',
    images: [
      {
        url: 'https://www.example.com/images/og-image.jpg',
        width: 850,
        height: 650,
        alt: 'Og Image Alt'
      }
     ]
  }}
/>
```

#### Article Example

```svelte
<script>
  import SvelteSeo from "svelte-seo";
</script>

<SvelteSeo
  openGraph={{
    title: "Open Graph Article Title",
    description: "Description of open graph article",
    type: "article",
    url: "https://www.example.com/articles/article-title",
    article: {
      publishedTime: "2020-08-03T17:31:37Z",
      modifiedTime: "2020-08-20T09:31:37Z",
      expirationTime: "2025-12-21T17:31:37Z",
      section: "Section II",
      authors: [
        "https://www.example.com/authors/@firstnameA-lastnameA",
        "https://www.example.com/authors/@firstnameB-lastnameB",
      ],
      tags: ["Tag A", "Tag B", "Tag C"],
    },
    images: [
      {
        url: "https://www.example.com/images/cover.jpg",
        width: 850,
        height: 650,
        alt: "Og Image Alt",
      },
    ],
  }}
/>
```

## Acknowledgements

This is inspired by [Next SEO](https://github.com/garmeeh/next-seo) by [@garmeeh](https://github.com/garmeeh).

## License

MIT
