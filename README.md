# website

Argo website in Jekyll

## General guidelines for adding new content

### Images in the Home and Overview pages

For consistent look, keep them at 3:2 aspect ratio if possible.  The
resolution of the images should be at least 900x600 pixels.  There's no
need to draw a border in the images; the shadow drawn by the browser will
provide a natural border (consequently, a white or transparent background
works best).

### Images in the Overview subpages

Aspect ratios, rendering sizes, and image placement are at your discretion;
use the existing pages as examples.  Note that `responsive-width-XX` (`XX`
equal to `20`, `30`, `40`, `50`, or `60`) classes are available to specify
the relative width of the image on screen as a percentage of the browser
window width.  For narrow windows, they all revert to `100%`.  More widths
can trivially be added in `assets/css/main.css`.  To ensure high rendering
quality, image width of around 1,200 pixels is recommended for
`responsive-width-50`; scale accordingly up/down for other sizes.

The purpose of the `<br clear="both" />` near the bottom of existing
subpages is to provide a barrier that no included image extends beyond;
that way, the names of the people responsible always start near the left
edge of the browser window.

### Links

When providing a series of links, e.g., in the _Resources for Developers_
page, use icons to brake the monotony.  We use Font Awesome, which provides
a large collection of icons; see
[https://fontawesome.com/icons?d=gallery&m=free](https://fontawesome.com/icons?d=gallery&m=free).

### Mugshots

For member images in the Team page, use `.jpg` images of 600x600 pixels for
best results.  For a consistent look, crop the images so that the heads
occupy a similar amount of space as in existing images.

### Publications

The easiest way to deal with those is to email Kamil the PDF and the link
to the publisher page if available and he'll take care of the rest.  In
general though:

_Papers_ should only contain items that were actually published in the
proceedings/journals/etc., e.g., are available through a 3rd party
publisher website, have a DOI number, and so on.  So in general, keep,
e.g., extended abstracts accompanying poster submissions out of here (they
could go with the posters if you wish).

If at all possible, do include a PDF with the final preprint version of the
paper, e.g., after all the review corrections have been applied.  Do
**not** use PDFs downloaded from the publisher's website though, as those
are copyrighted.  It should be a PDF that _you_ generated.

_Talks_ is reserved for events that didn't include regular, published
proceedings (e.g., some workshops).  If you would like to provide slides
that were presented during a paper presentation, include them under
_Papers_.

If there is enough interest in posting unpublished work, we will create a
separate _Technical Reports_ section or some such.

The thumbnails on the left of the page are generated manually.  Take a
screenshot, crop window borders, resize, save as `.png` (not `.jpg`).  Use
200px high for portrait orientation, 200px wide for landscape.  Gimp can
import PDF files directly, saving the initial steps.  For best results,
start with a reasonably high resolution image and scale it down; avoid
viewers that use subpixel rendering as it can result in moire when
rescaling.

### News

Whenever there is anything newsworthy to report about the project,
especially if it involves changes to the website, try to also provide a
short news blurb in the `_posts` directory.  The name of the files there
being with a date in the YYYY-MM-DD format; this date should by preference
be the date that the reported event took place, not the date we reported
about it (which could be weeks or even months later).  Any posts added will
automatically be included in the news reel on the front page and in the
news archive.
