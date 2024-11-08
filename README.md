<!-- insert
---
title: "KamiMod: An Incremental PaperMod Fork"
date: 2024-11-04
author: "8 Hobbies JavaScript Blog"
tags: ["kamimod", "themes"]
description: "KamiMod is an incremental fork of PaperMod."
---
end_insert -->
<!-- Powered by https://cj.rs/riss -->
<!-- remove -->

# KamiMod: An Incremental [PaperMod][] Fork
<!-- end_remove -->

KamiMod makes a few incremental changes to [PaperMod][]. This fork regularly syncs up with PaperMod.

## Features

This theme adds the following features and quality improvements on top of PaperMod. They are
features or improvements that have been left unmerged from PaperMod.

### Show Related Posts

- Corresponding to [adityatelange/hugo-PaperMod#1049](https://github.com/adityatelange/hugo-PaperMod/pull/1049), with different implementation.
- Configurable via `params.RelatedPostsCount`. `0` means no related posts. A positive number indicates the maximum number of related posts appended to the end of each post. Default: `0`.
- See the [Hugo doc](https://gohugo.io/content-management/related/) for further configuration of the behavior of related posts.

### Add last modified date to post header

- [adityatelange/hugo-PaperMod#1337](https://github.com/adityatelange/hugo-PaperMod/pull/1337)
- Use the `time` tag instead of `span` to express post dates.

### Add an option `params.showDescription` to not display descriptions

- [adityatelange/hugo-PaperMod#1533](https://github.com/adityatelange/hugo-PaperMod/pull/1533)
- [`.Description` is meant to be used for metadata purpose](https://gohugo.io/methods/page/description/):
  > Conceptually different from a content summary, a page description is typically used in metadata about the page.
- Set `params.showDescription` to `true` to display descriptions, or `false` to hide descriptions. Default: `false`.

### Allow setting `ShowFullTextinRSS` in individual pages

- [adityatelange/hugo-PaperMod#1542](https://github.com/adityatelange/hugo-PaperMod/pull/1542)

### Add an option to exclude pages from the RSS feed

- Setting `params.excludeFromRSS` to true in the frontmatter of a page to exclude it from the RSS feed.

### Allow extending `robots.txt`

- Content from `layouts/partials/extend_robots.txt` is appended to the builtin `robots.txt` file.

### Set preferred name for serach engines

[Google relies the `WebSite` structured data](https://developers.google.com/search/docs/appearance/site-names#website) to find out the site name and homepage URL.

## Fixes and Changes

### `<image><link>` in RSS should link to the permalink

- [adityatelange/hugo-PaperMod#1545](https://github.com/adityatelange/hugo-PaperMod/pull/1545)

### Remove the use of `accesskey` to improve accessibility

- [adityatelange/hugo-PaperMod#1494](https://github.com/adityatelange/hugo-PaperMod/pull/1494)
- [MDN advises not using accesskeys for general purpose websites for various reasons](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey#accessibility_concerns).
- [WebAIM also recommends against using accesskeys generally](https://webaim.org/techniques/keyboard/accesskey).

### Use `.Summary` as RSS description instead of `.Description`

- [Hugo description](https://gohugo.io/methods/page/description/) is conceptually for [metadata about a page](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#adding_an_author_and_description). Using `.Description` in RSS leads to very little information for readers.

### Use `site.Title` instead of `site.Params.Title`

- `site.Params.Title` seems redundant and only used once in PaperMod.

### Add `utm_*` params to various places

- The `utm_medium=sharing` param is added to the URLs shared by the share buttons.
- The `utm_medium=rss` param is added to the RSS links.

### Allow specifying `alternateName` in the `WebSite` structured data

[`alternateName`](https://developers.google.com/search/docs/appearance/site-names#alternative) is
used by Google to select a name of the site. In addition to `title`, you can specify alternate
site names in `params.alternateSiteNames`:

```yaml
params:
  alternateSiteNames: ["Name1", "Name2"]
```

### Don't show an output format as `<link rel=...>` if `rel` is empty

- Many custom output formats don't need such a link element.

## Installation

You may follow the [installation instructions from PaperMod](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-installation/), with the following changes:

- Replace `https://github.com/adityatelange/hugo-PaperMod` with `https://github.com/8hobbies/KamiMod`.
- Replace all other occurrences of `PaperMod` with `KamiMod`.

## Configurations

Except for the features listed above, please follow the [PaperMod doc](https://github.com/adityatelange/hugo-PaperMod/wiki/Features) for configurations.

## Demo

There is also a [live demo](https://kamimod.8hob.io), along with [its source code](https://github.com/8hobbies/KamiMod-example-site).

## Contribution

If you would like to report a bug, please use the [GitHub issue tracker](https://github.com/8hobbies/KamiMod/issues). Since KamiMod is an incremental fork of PaperMod, it is highly recommended to report to PaperMod if applicable.

If you would like to make code contribution, please make a pull request to PaperMod first if applicable. If the pull request does not get merged in a reasonable amount of time, feel free to port the pull request here. To maintain the incremental nature of this project, we will not consider pull requests that are applicable to PaperMod if they haven't been submitted to PaperMod first.

[PaperMod]: https://github.com/adityatelange/hugo-PaperMod
