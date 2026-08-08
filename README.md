# HTML and CSS Practice

A set of learning exercises, kept as a record of learning the language rather
than as a project or a library.

> **Cloning this on Windows will fail partway.** One file is named
> `HTML5/<!DOCTYPE html>.html`, which is legal on Linux and macOS but not on
> Windows, where `<` and `>` cannot appear in a filename. `git clone` aborts the
> checkout at that path and leaves the rest of the working tree unwritten. **A
> `git add -A` afterwards then records every unwritten file as deleted** - that
> is exactly how this repository lost all ninety files once, in a commit that
> was only meant to update the README. To clone it here, set
> `git -c core.protectNTFS=false clone ...` and expect that one file still not
> to be written; or clone `--bare`, which never touches a working tree.

Eighty-eight files written while working through HTML and CSS from the
beginning: 24 HTML pages, 54 stylesheets, and the images they load. Two further
files, `HTML5/placeholder.mp4` and `HTML5/placeholder.jpg`, are generated
substitutes rather than original work - see below.

## What is in here

Each file is one idea, tried on its own.

| Area | Files |
|------|-------|
| Layout | `box.html`, `cssboxmodel`, `blockelement`, `display`, `float`, `float1` |
| Colour | `color`, `colorhexa`, `colorchange`, `backgroundgradients`, `background` |
| Type | `fontfamily`, `firstline` |
| Selectors | `descendentChild`, `cssvariables` |
| Structure | `banner`, `twopages`, `twopagesmy`, `form`, `index` |
| Applied | `calcfun` (a small calculator), `django` (template markup) |

`CSS1/` and `HTML5/` hold the earliest exercises, before the files moved to the
top level. There is no build step, no dependency and no framework - nothing is
vendored and nothing is loaded from a CDN. Open any `.html` file in a browser.

## The video was replaced

`HTML5/practice.html` demonstrates the `<video>` element. The clip it originally
loaded, and the poster image beside it, were a commercial Tamil film song -
about three minutes of it, 9.3 MB. That was not mine to republish, so both have
been removed from this repository and from its history.

In their place are `HTML5/placeholder.mp4` and `HTML5/placeholder.jpg`: five
seconds of generated colour-bar test pattern, made with

```sh
ffmpeg -f lavfi -i testsrc=size=640x360:rate=15:duration=5 \
       -c:v libx264 -pix_fmt yuv420p placeholder.mp4
```

The exercise still shows what it was written to show - a `<video>` element with
`poster`, `controls` and a `src`. Only the content behind it changed.

## Rough edges left as they are

Two filenames in `HTML5/` are broken - `<!DOCTYPE html>.html`, and files saved
with no extension at all (`django form`, `form django`). They are what happens
when a save dialog is given the content instead of the name.

They have been left alone deliberately. Renaming files in a record of
what was actually written would make it a less accurate record.

One consequence is worth knowing: the angle brackets in `<!DOCTYPE html>.html`
are not legal in a Windows filename, so this repository cannot be checked out on
Windows unless you set `core.protectNTFS=false`. The file is intact as a blob
either way. Ninety files were once lost to exactly this - a checkout aborted
partway, and a blanket `git add -A` recorded the unwritten files as deleted. They
were restored from history.

## Why it is kept

It is the starting point of the web work that followed. The Django projects and
the vending machine's checkout page all render templates that began as exercises
like these. Nothing here is reusable and none of it is meant to be.

## Licence

MIT, see [LICENSE](LICENSE). That covers the HTML and CSS, which are mine. It
does not cover the sample photographs used to illustrate the exercises
(`dogs.jpg`, `cat.jpeg`, `smoothie.jpeg`, `bigimage.jpg`, `folderimg.jpeg` and
the two `smallimage.jpg`).

Some of their provenance is recoverable and some is not. `CSS1/practice.css` and
`CSS1/practice.html` load images directly from Pexels by URL, and
`HTML5/practice.html` links a Pexels photo page, so those are Pexels stock under
the Pexels licence. The rest were saved locally while learning and their source
was not recorded. Treat the local copies as unlicensed rather than as mine.
