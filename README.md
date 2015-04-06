# Reset

Minimal CSS resets for documents + applications in modern browsers.

## Purpose

While I don’t believe there is a one-size fits all solution for resetting user agent stylesheets, these resets are the product of iterating through custom resets for dozens of projects over the past several years. I decided to turn it into an npm module to keep my workflow as <abbr title="Don’t repeat yourself.">DRY</abbr> as possible. If it saves me time, hopefully it will do the same for you.

## Supported Browsers

These resets are intended to revert styles defined in **user agent stylesheets** for popular modern browsers including Chrome, Safari, Firefox, and Internet Explorer. As a general rule, everything should be pretty reliable for the last several stable versions of each browser. For now, these resets will support IE 9+, but expect that to change in the near future. There is also an underlying assumption that the mobile counterparts for each of these browsers are also supported.

- Chrome + Safari both use the **[Webkit user agent stylesheet](http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css)**
- Firefox uses the **[Mozilla user agent stylesheet](http://mxr.mozilla.org/mozilla/source/layout/style/html.css)**
- IE uses some ungodly, bastardized semblance of a user agent stylesheet + these resets will try to keep rendering as consistent as possible, but no promises

I have had zero experience supporting other browsers, but I am assuming that a solid reset combined with logical, well-organized production styles should render everything accurately on these browsers. *Untargeted browsers* may be a more accurate descriptor for these than unsupported browsers.

## Flavors

### Document

Intended for information-heavy, public-facing sites like blogs, personal sites, online periodicals, marketing sites, landing pages, and other commercial sites.

### Application

Intended for public and private interaction-driven sites like single-page web apps, social networks, enterprise software, or most online experiences requiring a login.

### Hybrid

Uses the application reset + supplies a `.doc` class to restore typical document styles for documents rendered within an application.

> Note: The `.doc` class introduces one level of specificity which may override selectors defined later in the stylesheet and require an undesireable increase in specificity on each of these selectors. It may be better to use Sass mixins for document styles within the context of an application.

## Usage

Be sure include the reset before any of your other styles.

### Proper Method

Add to your project with `npm install --save-dev mb-reset`, then copy one of the .css files from `node_modules/mb-reset` into your assets folder or import into an existing stylesheet as part of your build process.

If this is confusing or you just want to test the thing, use the quick + dirty method below.

### Quick + Dirty Method

> Heads up! This is **not recommended for production.**

Include one of the following in your `<head>`:

#### Document reset

```
<link href="https://raw.githubusercontent.com/mattborn/reset/master/reset-doc.css" rel="stylesheet" />
```

#### Application reset

```
<link href="https://raw.githubusercontent.com/mattborn/reset/master/reset-app.css" rel="stylesheet" />
```

#### Hybrid reset

```
<link href="https://raw.githubusercontent.com/mattborn/reset/master/reset.css" rel="stylesheet" />
```

## Annotations

### [Read the annotated reset](annotations.md)

## Examples

No examples, yet. Put this here so it bothers me.

## Resources

### Other CSS Resets

[CSSReset.com](http://cssreset.com) does a good job rounding these up + explaining the differences.

### Light Reading

[Which CSS Reset Should I Use?](http://www.cssreset.com/which-css-reset-should-i-use) **TL;DR:** Design your own CSS reset.

[Why “Reset” Style Sheets Are Bad](http://meiert.com/en/blog/20080419/reset-style-sheets-are-bad)

## Contribute

So far, all of this was built in a vacuum, so I would encourage anyone to analyze, criticize + challenge what I’ve done here. If you have questions or suggestions, please submit an issue or pull request.

Thank you!

—Matt