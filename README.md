# KamiMod: An Incremental [PaperMod][] Fork

KamiMod makes a few incremental changes to [PaperMod][].

## Features

This theme adds the following features and quality improvements on top of PaperMod. They are
features or improvements that were left unmerged from PaperMod.

- Related posts (Corresponding to adityatelange/hugo-PaperMod#1049, with different implementation)
- Replace `thumbnailUrl` with `logo` in the schema (adityatelange/hugo-PaperMod#1488)
  - `thumbnailUrl` is not part of the [Organization schema](Organization: https://schema.org/Organization)
- Remove the use of `accesskey` to improve accessibility (adityatelange/hugo-PaperMod#1494)
  - [MDN advises not using accesskeys for general purpose websites for various reasons](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey#accessibility_concerns)
  - [WebAIM also recommends against using accesskeys generally](https://webaim.org/techniques/keyboard/accesskey)
- Add an option to not display descriptions (adityatelange/hugo-PaperMod#1533)
  - [`.Description` is meant to be used for metadata purpose](https://gohugo.io/methods/page/description/):
    > Conceptually different from a content summary, a page description is typically used in metadata about the page.
- Add last modified date to post header (adityatelange/hugo-PaperMod#1337)


[PaperMod]: https://github.com/adityatelange/hugo-PaperMod
