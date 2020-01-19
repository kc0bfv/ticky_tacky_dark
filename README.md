# Ticky Tacky Dark - Theme for Hugo

This is a multi-page theme, where the list page displays a set of image buttons linking to your sub-pages.  It passes the [web accessibility evaluation tool tests](https://wave.webaim.org/).

Preview at <https://kc0bfv.github.io/ticky_tacky_dark>

## Configuration

The exampleSite demonstrates the features unique to this theme.  In your site config params section the following extra parameters are supported:

* `favicon` - the favicon URL, relative to your site (placed in header meta tag)
* `webmasterEmail` - the webmaster email displayed in the footer
* `author` - the author for the header meta tag
* `description` - the description for the header meta tag
* `headerimages` - a list of relative image URLs for the header of each page
* `msvalidate` - MS validation tag
* `googlesiteverification` - Google site verification tag

Pages you add have custom front matter options:

* `buttonimage` - the relative image URL for the page's button on the front page
* `sideimages` - a list of relative image URLs for the left sidebar on the page
* `sideimagealt` - the alternate text for the page's left sidebar image
* `weight` - an integer that specifies page ordering for the front page.  If you want the buttons and navbar items to show pages in a specific order, specify the ordering via weight.  Ordering goes from lowest weight to highest, left to right, top to bottom.

## Page Construction

Navigation from the main page happens via a button image.  These images are, optimally, 300x300 pixels.  Specify these button image URLs in a page's front matter with the `buttonimage` option.

On sub-pages, images can appear on the left side.  Sizing can vary there, but at full size images come out as about 277.5 pixels, and a size of about 300x500 pixels works nicely.  You can specify multiple images for a sub-page, and they'll be randomly selected on load.  Specify them as a list of image URLs on the page front matter, with option `sideimages`.

Header images are, optimally, 950x200 pixels.  Specify these in the site configuration as a list of image URLs with option `headerimages`.  One will be randomly selected on page load.

## Custom Shortcode

### Dropdown Text

To add a link that, when clicked, drops-down a section of text, use shortcode `dropdown/link` and shortcode `dropdown/content`.

**Example**

```
{{< dropdown/link togglename="dropNum1" linktext="Click here to see the text that will drop down." >}}
```

```
{{< dropdown/content togglename="dropNum1" >}}
  This is the text that drops down when you click the link.
{{< /dropdown/content >}}
```

## Usage

Put this theme in your site's themes folder, then modify the site config to specify the theme `ticky_tacky_tark`, or use the `-t ticky_tacky_dark` command line switch.
