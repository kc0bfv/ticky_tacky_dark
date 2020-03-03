# Ticky Tacky Dark - Theme for Hugo

This is a multi-page theme, where the list page displays a set of image buttons linking to your sub-pages.  It passes the [web accessibility evaluation tool tests](https://wave.webaim.org/).

Preview at <https://kc0bfv.github.io/ticky_tacky_dark>

## Configuration

The exampleSite demonstrates the features unique to this theme.  In your site config params section the following extra parameters are supported:

* `favicon` - the favicon URL, relative to your site (placed in header meta tag)
* `description` - the description for the header meta tag
* `images` - a list of relative image URLs for the header of each page
* `headername` - text to place over the header images
* `msvalidate` - MS validation tag
* `googlesiteverification` - Google site verification tag

Additionally, `Author.name` and `Author.email` in the site config will display as the author and webmaster email.

Pages you add have custom front matter options:

* `buttonimage` - the relative image URL for the page's button on the front page
* `images` - a list of relative image URLs for the left sidebar on the page
* `imagealt` - the alternate text for the page's left sidebar image
* `weight` - an integer that specifies page ordering for the front page.  If you want the buttons and navbar items to show pages in a specific order, specify the ordering via weight.  Ordering goes from lowest weight to highest, left to right, top to bottom.
* `author.name`, `author.email` - overrides the site author name and email

## Page Construction

Navigation from the main page happens via a button image.  These images are, optimally, 300x300 pixels.  Specify these button image URLs in a page's front matter with the `buttonimage` option.

On sub-pages, images can appear on the left side.  Sizing can vary there, but at full size images come out as about 277.5 pixels, and a size of about 300x500 pixels works nicely.  You can specify multiple images for a sub-page, and they'll be randomly selected on load.  Specify them as a list of image URLs on the page front matter, with option `images`.

Header images are, optimally, 950x200 pixels.  Specify these in the site configuration as a list of image URLs with option `images`.  One will be randomly selected on page load.

## Custom Shortcode

### Dropdown Text

To add an HTML details element that, when clicked, drops-down a section of text, use shortcode `dropdown`.

**Example**

```
{{< dropdown summary="Click here to see the text that will drop down." >}}
  This is the text that drops down when you click the link.
{{< /dropdown >}}
```

## Usage

Put this theme in your site's themes folder, then modify the site config to specify the theme `ticky_tacky_tark`, or use the `-t ticky_tacky_dark` command line switch.

## Licenses

The [Ubuntu Titling font](https://en.wikipedia.org/wiki/Ubuntu_Titling) is used, licensed by the GNU Lesser GPL, license included.
