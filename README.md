# pandoc-from-markdown-to-pdf

Use the pandoc command to convert from a markdown file to a PDF file.

This tool uses our favorite settings for layouts, styles, fonts, etc.

You can edit this tool as you wish.

Syntax:

```sh
pandoc-from-markdown-to-pdf <args>
```

Syntax for typical use:

```sh
pandoc-from-markdown-to-pdf <input.md> -o <output.pdf>
```

Example:

```sh
$ pandoc-from-markdown-to-pdf example.md -o example.pdf
```


# Install

Clone this repo to anywhere you want, and add it to your path, such as:

```sh
cd $HOME
git clone https://github.com/SixArm/pandoc-from-markdown-to-pdf.git
export PATH="$PATH:$HOME/pandoc-from-markdown-to-pdf"
```


# Availability

This tool is currently tested on macOS Ventura.

If you want to use this tool on other systems,
then please contact us, or open an issue, to let us know.


# Prerequisites

This script requires these prerequisites to be installed:

* pandoc document converter

* xelatex implementation of LaTex converters

* pygments syntax highlighting

* Bitstream Vera fonts
  
If you want a different choices for any of the above,
then please contact us or open an issue, to let us know.


## macOS install

Example using brew:

```sh
brew install pandoc
```

If you prefer a heavyweight install:

```sh
brew install mactex
```

If you prefer a lightweight install:

```sh
brew install basictex
eval "$(/usr/libexec/path_helper)"
# Update $PATH to include `/usr/local/texlive/2022basic/bin/universal-darwin`
sudo tlmgr update --self
sudo tlmgr install texliveonfly
sudo tlmgr install adjustbox
sudo tlmgr install tcolorbox
sudo tlmgr install collectbox
sudo tlmgr install ucs
sudo tlmgr install environ
sudo tlmgr install trimspaces
sudo tlmgr install titling
sudo tlmgr install enumitem
sudo tlmgr install rsfs
```

Verify the programs are runnable:

```sh
$ which pandoc
/usr/local/bin/pandoc

$ pandoc --version
pandoc 2.17.1.1

$ which xelatex
/Library/TeX/texbin/xelatex

$ xelatex --version
XeTeX 3.141592653-2.6-0.999993 (TeX Live 2021)
```

## Troubleshooting xelatex

If the `xelatex` command is not found, then look for it:

```sh
find / -name xelatex
```

Example result on macOS after brew install:

```sh
/Library/TeX/texbin/xelatex
```

Then add xelatex to your path:

```sh
export PATH="$PATH:/Library/TeX/texbin/xelatex"
```

If that works, then adjust your path as you wish, such as in your `.env` file, or `~/.zshenv` file, etc.


## Fonts

For help with fonts, see the `fonts` directory.


## Thanks

Thanks to https://learnbyexample.github.io/customizing-pandoc/

Thanks to https://github.com/sixarm/sixarm-unix-shell-functions/


## Tracking

  * Package: pandoc-from-markdown-to-pdf
  * Version: 1.1.0
  * Created: 2022-03-12T22:05:34Z
  * Updated: 2023-03-15T18:08:35Z
  * License: GPL-2.0 or GPL-3.0 or contact us for more
  * Website: https://github.com/sixarm/pandoc-from-markdown-to-pdf
  * Contact: Joel Parker Henderson (joel@sixarm.com)
  