# dotcss

dotcss is two(2) things:

  1. A [tiny web server][server] that runs on your machine, serving CSS files
     out of `~/.css`
  2. A [Chrome extension][extension] that fetches these CSS files and injects
     them based on their filename.

The files are requested on a per-page basics, based on the hostname. For
example, if you go to [https://github.com](https://github.com),
`~/.css/github.com.css` would be injected into the page.

This makes it super simple and easy to change and improve the look of your favorite sites.

## How it works

Chrome extensions can't access the filesystem, so dotcss runs a [tiny web
server][server] on port 1243 that serves files out of the `~/.css` folder.

## Requirements

- OS X or Linux
- Ruby 1.8 or newer
- rake (`gem install rake`)
- Chrome or Chromium
- `/usr/local/bin` in your `$PATH`
- on Linux: `exo-open` (Can be found in [exo-utils][] on Ubuntu. Required until
  [Bug #378783 in xdg-utils][exo-bug] is fixed.)

## Installation

1. Ensure you have stewart's dotcss installed and running
2. [Install the extension](https://github.com/maman/dotcss.safariextension/blob/master/dotcss.safariextz?raw=true)

## Thanks

- [Chris Wanstrath][defunkt] for [dotjs][], which 90% of this is based on.
- [Will Farrington](https://github.com/wfarr) for [dotjs.safariextension](https://github.com/wfarr/dotjs.safariextension), which another 90% of this is based on.

[server]: https://github.com/stewart/dotcss/blob/master/bin/dcssd
[extension]: http://j.mp/dotcss_chrome_ext
[exo-utils]: http://packages.ubuntu.com/search?keywords=exo-utils
[exo-bug]: https://bugs.launchpad.net/ubuntu/+source/xdg-utils/+bug/378783
[defunkt]: https://github.com/defunkt
[dotjs]: https://github.com/defunkt/dotjs