# Reset Annotations

## Document

How minimal can we go with this? We should defer to browser as much as possible!

Things like `img { max-width: 100% }` we know for sure.

### Exclusions

The following tag selectors were intentionally omitted from the reset:

- mark - do we want a consistent yellow?
- time

Every browser supports all of the HTML5 tags.

address, article, aside, figcaption, figure, footer, header, hgroup, layer, main, nav, section

## Application

## Hybrid

We need to explicitly re-apply .doc styles which is much different from the implicit nature of our original document reset.

### Exclusions

The following tag selectors were intentionally omitted from the reset:

Shouldn’t be using h4, h5, or h6

## Random thoughts

What types of tags are expected for documents vs. applications?

[Custom document underlines](https://medium.com/designing-medium/crafting-link-underlines-on-medium-7c03a9274f9) should be a part of core styles