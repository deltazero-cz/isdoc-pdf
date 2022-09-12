# isdoc-pdf

Attach ISDOC to a PDF and convert it to PDF/A-3B standard.

ISDOC is a XML based Invoicing Standard of the Czech Republic (EU), simillar to Factur-X and ZUGFeRD.

### Requirements

- A Bash-compatible shell
- A recent version of Ghostscript (at least 9.14, further details here)

### Installation

Clone this repo or [download a zip](https://github.com/deltazero-cz/isdoc-pdf/archive/master.zip),
make sure `isdoc-pdf` is executable by `chmod +x isdoc-pdf`.
 
Don't forget to install Ghostscript (9.27 or later).

### Usage

```shell
./isdoc-pdf input.pdf input.isdoc [output.isdoc.pdf]
```

This script will attach your input ISDOC file to the input PDF as an alternative attachment,
compress and flatten the PDF and convert it into PDF/A-3B, as stated by the 
[official docs](https://isdoc.github.io/doc/isdoc.html#reprezentace). 

You can validate your result's PDF/A-3 compliance using 
[veraPDF demo](https://demo.verapdf.org/). 

If you want to run this script silently, direct stdout to /dev/null
```shell
./isdoc-pdf input.pdf input.isdoc [output.isdoc.pdf] > /dev/nul
```

### Thank yous

This package is based upon code fragments & inspiration from:
 - [pdf2archive](https://github.com/matteosecli/pdf2archive) by [Matteo Seclì](https://github.com/matteosecli)
 - [PDF/A PostScript](https://stackoverflow.com/a/58814712/3290062) by [KenS](https://stackoverflow.com/users/701996/kens)
 - [GhostScript blogpost on ZUGFeRD](https://www.ghostscript.com/blog/zugferd.html)
