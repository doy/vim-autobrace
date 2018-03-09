# Overview

This plugin rebinds some characters to make typing matching characters easier.
Specifically, it does these things:

* Opening brace and quote characters (specifically, `(`,
  `[`, `{`, `'`, and `"`) are mapped to make them automatically insert their
  corresponding closing character.
* Typing a closing brace or quote character while the next character past the
  cursor is that character will skip over it instead of inserting it.
* Pressing <CR> when the next character is a closing brace will insert two
  newlines, and leave the cursor in the middle.
* Pressing <BS> when the previous character is an open brace and there is
  nothing but whitespace between the open brace and closing brace will delete
  both the open and closing brace.

# Configuration

None yet, but I'm open to suggestions!

# Bugs

Due to limitations in Vimscript, using this plugin will tend to break using
the `.` operator to repeat insert operations, since the mappings bounce in and
out of normal mode. Suggestions welcome for how to fix this, but as far as I
can tell, it's not actually possible to fix in general currently.
