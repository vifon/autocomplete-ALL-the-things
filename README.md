Name
====

autocomplete-ALL-the-things - an urxvt plugin allowing user to easily complete arbitrary text

Installation
------------

Copy the `autocomplete-ALL-the-things` file to the urxvt perl-lib directory
(default: `~/.urxvt/ext/`).

Add the following lines to your `~/.Xresources` (or `~/.Xdefaults`):

```
URxvt.perl-ext-common:    ...,autocomplete-ALL-the-things
URxvt.keysym.M-C-slash:   perl:aAtt:word-complete
URxvt.keysym.M-question:  perl:aAtt:fuzzy-complete
URxvt.keysym.M-quotedbl:  perl:aAtt:undo
```

Description
-----------

Completes the currently typed word using the other words visible in the urxvt window.

For example the terminal looks like this:

![Preview](https://cloud.githubusercontent.com/assets/674812/3480320/3bd2e726-035f-11e4-9e64-db599724c931.gif)

It was strongly inspired by `dabbrev` feature in GNU Emacs and later by
[skeleton-complete](https://github.com/baohaojun/skeleton-complete) by Bao
Haojun.

Basic usage
-----------

Just press the key bound to `aAtt:complete` (in the example above:
Alt-Ctrl-slash) to complete the word at point. Subsequent uses cycle through
other possible completions.

Key bound to `aAtt:undo` (Alt-Shift-quote) undoes the completion.
Additionally, pressing `Escape` undoes the completion too regardless
of this setting.

Advanced usage
--------------

For more advanced completions use `aAtt:fuzzy-word-complete`
(Alt-Shift-slash) and `aAtt:skeleton-complete`. It's behavior is inspired by
[skeleton-complete](https://github.com/baohaojun/skeleton-complete), please see
[its readme](http://baohaojun.github.io/skeleton-complete.html) for a more
detailed explanation.

Available functions
-------------------

* `aAtt:word-complete` -- classical prefix-based completion for words
* `aAtt:WORD-complete` -- completion for WORDS (in the Vim meaning)
* `aAtt:fuzzy-word-complete` -- fuzzy completion for words
* `aAtt:fuzzy-WORD-complete` -- fuzzy completion for WORDS
* `aAtt:fuzzy-complete` -- fuzzy completion for arbitrary strings
* `aAtt:undo` -- undo the completion (must be used right after a completion)

Acknowledgments
---------------

Thanks to Stanislav Seletskiy for various contributions.

Thanks to Bao Haojun for the great idea of [skeleton-complete](https://github.com/baohaojun/skeleton-complete).

Copyright
---------

Copyright (C) 2012-2014  Wojciech Siewierski

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
