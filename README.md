# Summary Editor

Attaches a WYSIWYG editor to the summary textarea on text with summary fields,
allowing site editors to apply formatting (bold, italic, links, etc.) to summary
text without needing to type HTML manually.

## How it works

Backdrop's text with summary field widget provides a summary textarea, but does
not attach an editor to it — only the main body field gets one. This module
swaps the plain summary textarea for a full editor-enabled field, inheriting the
same text format as the body field. The format selector is hidden since the
summary always uses the body's format.

No changes are made to how summary content is stored.

## Requirements

- Text module (Backdrop core)
- A WYSIWYG editor enabled for the text format used by the body field
  (e.g. CKEditor enabled for "Full HTML" at `admin/config/content/formats`)

## Installation

Install and enable as you would any Backdrop contrib module. No configuration is
required.

## Issues

Bugs and feature requests should be reported in the
[Issue Queue](https://github.com/backdrop-contrib/summary_editor/issues).

## Current Maintainers

- [Tim Erickson](https://github.com/stpaultim).

## License

This project is GPL v2 software. See the [LICENSE.txt](LICENSE.txt) file in
this directory for complete text.
