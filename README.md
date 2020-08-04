# Manipulate Firefox bookmarks

Tool to extract and merge links from HTML bookmarks files exported from
Firefox.  A Firefox bookmarks file doesn't make bookmarks available in a form
that's easy to work with.  This tool solves that problem.

I have found that Firefox's bookmark manager is the least bad method to manage
my bookmarks.  At this point I don't use Firefox Sync, and I wanted an offline
way of importing bookmarks from a second computer.

This tool takes a bookmarks HTML file exported from the primary browser and a
bookmarks HTML file exported from the secondary browser and generates an HTML
file containing links whose addresses only appear in the secondary file.  I can
then import this generated file into my primary browser and move bookmarks
around as I see fit, with the assurance that I'm not bringing in duplicate
links.  This tool also can handle bookmarks exported from Safari.

A pain? Yes.  The best solution? Probably not.  It was fun to make though, and
I'm looking to maximize fun.

## Setup

Install `pyenv` and `pyenv-virtualenv` (e.g. via Homebrew on macOS).

Once that's installed and configured:
```bash
pyenv install 3.8.3
pyenv virtualenv 3.8.3 bookmarks
pyenv activate bookmarks
pip install -r requirements.txt
```

## Tests

LOL.

## Use
```console
$ python bookmarks.py prepare-import bookmarks-primary.html bookmarks-secondary.html > prepped.html
```
