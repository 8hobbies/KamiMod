<!-- insert
---
title: "KamiMod: An Incremental PaperMod Fork"
date: 2024-06-02
author: "8 Hobbies"
tags: ["themes"]
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

### Related Posts

- Corresponding to [adityatelange/hugo-PaperMod#1049](https://github.com/adityatelange/hugo-PaperMod/pull/1049), with different implementation.
- Configurable via `params.RelatedPostsCount`. `0` means no related posts. A positive number indicates the maximum number of related posts appended to the end of each post. Default: `0`.
- See the [Hugo doc](https://gohugo.io/content-management/related/) for further configuration of the behavior of related posts.

### Add last modified date to post header

- [adityatelange/hugo-PaperMod#1337](https://github.com/adityatelange/hugo-PaperMod/pull/1337)

### Add an option `params.showDescription` to not display descriptions

- [adityatelange/hugo-PaperMod#1533](https://github.com/adityatelange/hugo-PaperMod/pull/1533)
- [`.Description` is meant to be used for metadata purpose](https://gohugo.io/methods/page/description/):
  > Conceptually different from a content summary, a page description is typically used in metadata about the page.
- Set `params.showDescription` to `true` to display descriptions, or `false` to hide descriptions. Default: `false`.

### Remove the use of `accesskey` to improve accessibility

- [adityatelange/hugo-PaperMod#1494](https://github.com/adityatelange/hugo-PaperMod/pull/1494)
- [MDN advises not using accesskeys for general purpose websites for various reasons](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey#accessibility_concerns).
- [WebAIM also recommends against using accesskeys generally](https://webaim.org/techniques/keyboard/accesskey).

### Replace `thumbnailUrl` with `logo` in the schema

- [adityatelange/hugo-PaperMod#1488](https://github.com/adityatelange/hugo-PaperMod/pull/1488)
- `thumbnailUrl` is not part of the [Organization schema](https://schema.org/Organization).

## Installation

You may follow the [installation instructions from PaperMod](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-installation/), with the following changes:

- Replace `https://github.com/adityatelange/hugo-PaperMod` with `https://github.com/8hobbies/KamiMod`.
- Replace all other occurrences of `PaperMod` with `KamiMod`.

## Demo

There is also a [live demo](https://kamimod.8hob.io), along with [its source code](https://github.com/8hobbies/KamiMod-example-site).

## Contribution

If you would like to report a bug, please use the [GitHub issue tracker](https://github.com/8hobbies/KamiMod/issues). Since KamiMod is an incremental fork of PaperMod, it is highly recommended to report to PaperMod if applicable.

If you would like to make code contribution, please make a pull request to PaperMod first if applicable. If the pull request does not get merged in a reasonable amount of time, feel free to port the pull request here. To maintain the incremental nature of this project, we will not consider pull requests that are applicable to PaperMod if they haven't been submitted to PaperMod first.

[PaperMod]: https://github.com/adityatelange/hugo-PaperMod
