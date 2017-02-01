# standardfmt.el

Emacs minor-mode to format JavaScript with [standard][] / [semistandard][] on
save.

Core parts of `standardfmt.el` are borrowed from [`go-mode`][go-mode] and it's
invocation of `gofmt`.

## Installing

Drop `standardfmt.el` somewhere into you `load-path`. I favour the folder
`~/.emacs.d/vendor`:

```lisp
(add-to-list 'load-path "~/.emacs.d/vendor")
(require 'standardfmt)
```

## Usage

To enable formatting JavaScript buffers on save, simply enable
`standardfmt-mode`. If you use `js-mode` to edit JavaScript buffers, something
like this will do the trick:

```lisp
(add-hook 'js-mode-hook #'standardfmt-mode)
```

## Commands

- `standardfmt` - Format current buffer with standard/semistandard.
- `standardfmt-mode` - Toggle formatting on save.

## Customization

### Use Semistandard

By default standard will be used, but you can change it to use semistandard by
customizing `standardfmt-command` with `M-x customize-variable` or:

```lisp
(setq standardfmt-command "semistandard")
```

## License

Copyright (C) 2017 Jim Myhrberg

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


[standard]: https://github.com/feross/standard
[semistandard]: https://github.com/Flet/semistandard
[go-mode]: https://github.com/dominikh/go-mode.el
