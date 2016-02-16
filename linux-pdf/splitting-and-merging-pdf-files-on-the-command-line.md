# Splitting and merging PDF files on the command line

You can use poppler-utils to do a lot of pdf stuff.


1. First, install it. On Debian-based systems: `sudo apt-get install poppler-utils`
1. To split, `pdfseparate -f <start page> -l <end page> <source pdf> <destination pdf>`
1. To merge, `pdfunite <source pdf 1> <source pdf 2> <source pdf ...> <destination pdf>`


There are many other utils provided, such as:

1. `pdfdetach` - lists or extracts embedded files (attachments)
1. `pdffonts` - font analyzer
1. `pdfimages` - image extractor
1. `pdfinfo` - document information
1. `pdfseparate` - page extraction tool
1. `pdftocairo` - pdf to png/jpeg/pdf/ps/eps/svg converter using cairo
1. `pdftohtml` - pdf to html converter
1. `pdftoppm` - pdf to ppm/png/jpeg image converter
1. `pdftops` - pdf to postscript (ps) converter
1. `pdftotext` - text extraction
1. `pdfunite` - document merging tool

Sourced from [this excellent blog post](http://jorge.fbarr.net/2015/02/20/split-and-merge-pdfs-part-2/).

