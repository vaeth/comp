# comp

Compare files or directories, including metadata

Author: Martin Väth (martin at mvath.de)

This project is under a BSD type license, meaning that you can do practically
everything with it except removing my name.

The command `comp` is similar to `diff -r -q`, but it compares also metadata
like symlinks, timestamps, permissions, partial content, etc.

You can specify in great detail which data actually will be compared
or ignored, whether symlinks will be followed, etc.

Use `comp --man` to get an extended help as a manpage.

This is a ground-up rewrite and redesign of the `comp-old` script
(originally called `comp`) from https://github.com/vaeth/mv_perl/

The script requires __perl-5.12__ or newer and some modules shipped with that
perl version. In addition, it is recommended to have the `String::ShellQuote`
module installed to get an improved output, though this is not mandatory.

To install this script, simply copy the content of `bin/` to your `$PATH`.
To obtain __zsh completion__ support, also put the content of `zsh/` into
your `$fpath`.
(If you do not have root access, you can add the corresponding directory with
`fpath+=("...")` before you call `compdef` from your zsh initialization files).

For installation under Gentoo, you can use the ebuild from the mv overlay
(which is available over layman).
