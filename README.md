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

## Configuration

The rich text editor is opt-in per field. After enabling the module, visit the
field settings for any text with summary field and check **Enable rich text
editor for the summary field** to activate it for that field:

`Administration > Structure > Content types > [type] > Manage fields > [field] > Edit`

Without this setting enabled, the field behaves exactly as it does without the
module installed — the summary remains hidden until an editor opens it manually.

## HTML in meta descriptions

Because the summary field can now contain HTML, take care when using it as a
source for meta descriptions or search engine previews. HTML tags will appear as
raw text in those contexts.

This module provides a `[node:summary-plain]` token that returns the summary
with all HTML stripped. Use this token when configuring SEO or metatag settings
instead of the raw summary token.

If no summary is set, the token falls back to a plain-text excerpt of the body
field (up to 300 characters).

## Requirements

- Text module (Backdrop core)
- A WYSIWYG editor enabled for the text format used by the body field
  (e.g. CKEditor enabled for "Full HTML" at `admin/config/content/formats`)

## Installation

Install and enable as you would any Backdrop contrib module. Then enable the
rich text editor per field as described under Configuration above.

## Issues

Bugs and feature requests should be reported in the
[Issue Queue](https://github.com/backdrop-contrib/summary_editor/issues).

## Current Maintainers

- [Tim Erickson](https://github.com/stpaultim).

## License

This project is GPL v2 software. See the [LICENSE.txt](LICENSE.txt) file in
this directory for complete text.
