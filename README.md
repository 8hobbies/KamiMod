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

KamiMod makes a few incremental changes to [PaperMod][].

## Features

This theme adds the following features and quality improvements on top of PaperMod. They are
features or improvements that were left unmerged from PaperMod.

- Related posts (Corresponding to adityatelange/hugo-PaperMod#1049, with different implementation)
  - Configurable via `params.RelatedPostsCount`. `0` means no related posts. A positive number indicates the maximum number of related posts appended to the end of each post.
  - See the [Hugo doc](https://gohugo.io/content-management/related/) for further configuration of the behavior of related posts.
- Replace `thumbnailUrl` with `logo` in the schema (adityatelange/hugo-PaperMod#1488)
  - `thumbnailUrl` is not part of the [Organization schema](https://schema.org/Organization)
- Remove the use of `accesskey` to improve accessibility (adityatelange/hugo-PaperMod#1494)
  - [MDN advises not using accesskeys for general purpose websites for various reasons](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey#accessibility_concerns)
  - [WebAIM also recommends against using accesskeys generally](https://webaim.org/techniques/keyboard/accesskey)
- Add an option `params.showDescription` to not display descriptions (adityatelange/hugo-PaperMod#1533)
  - [`.Description` is meant to be used for metadata purpose](https://gohugo.io/methods/page/description/):
    > Conceptually different from a content summary, a page description is typically used in metadata about the page.
- Add last modified date to post header (adityatelange/hugo-PaperMod#1337)

## Demo

There is also a [demo](https://kamimod.8hob.io).

[PaperMod]: https://github.com/adityatelange/hugo-PaperMod
