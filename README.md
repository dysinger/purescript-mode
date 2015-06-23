PureScript Mode for Emacs
----------------------

This is the PureScript mode package for Emacs.

To report problems or suggestions, please
[open an issue](https://github.com/dysinger/purescript-mode/issues?state=open)
in the issue tracker.

Below is a brief setup guide.

Quick Emacs rundown
--------------------

When Emacs is started up, it normally loads the
[Emacs initialization file](http://www.gnu.org/software/emacs/manual/html_node/emacs/Init-File.html)
usually called `~/.emacs`, `~/.emacs.el`, or `~/.emacs.d/init.el`;
with `~` standing for for your home directory.  This file should
contain all of your personal customisations written as a series of
Emacs Lisp commands.  In the following sections, this file will simply
be referred to as the `.emacs` file.

Installation
------------

GNU Emacs version 23 or later is officially supported.  It may work
with other Emacsen, but we don't have the resources to support other
versions.

### Installation from Git

-   `git clone https://github.com/purescript/purescript-mode.git` into a
    suitable directory, e.g. `~/lib/emacs/purescript-mode/` where `~`
    stands for your home directory.

-   Assuming you have unpacked the various purescript-mode modules
    (`purescript-mode.el` and the rest) in the directory
    `~/lib/emacs/purescript-mode/`, you need generate the autoloads file
    (`purescript-mode-autoloads.el`) by either

    - Invoking `make purescript-mode-autoloads.el`, or `make all` (use
      this to perform byte-compilation and Info manual generation)

    - From inside Emacs, `M-x update-directory-autoloads` and answering the question for
      the folder with `~/lib/emacs/purescript-mode/` and the question for the output-file with
      `~/lib/emacs/purescript-mode/purescript-mode-autoloads.el`

    and then adding the following command to your `.emacs`:

    ```el
    (add-to-list 'load-path "~/lib/emacs/purescript-mode/")
    (require 'purescript-mode-autoloads)
    (add-to-list 'Info-additional-directory-list "path-to-purescript-mode/")
    ```

-   After updating your purescript-mode working directory, you need to
    re-run `make all` or `M-x update-directory-autoloads`.

Basic Configuration
-------------------

For setup instructions, please consult the new integrated purescript-mode
[Info](https://www.gnu.org/software/texinfo/manual/info/info.html)
manual which can be accessed after installation via
`M-x info-display-manual [RET] purescript-mode`.

Support
-------

- [Github homepage](https://github.com/purescript/purescript-mode)

Contributing
------------

Please make sure your pull requests are at least properly rebased and up to date.
