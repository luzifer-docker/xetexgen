# Luzifer / xetexgen

This container is intended as a replacement for a local TeX installation. The purpose mainly is to have a working TeX environment on a Mac without having to deal with all the implications a local TeX installation brings on OSX.

## Usage

The container contains a simple script with basic commands to generate a PDF from your TeX file. So you can use this command if for example your TeX file is named `letter.tex`:

```bash
# docker run --rm -ti -v $(pwd):/src luzifer/xetexgen letter.tex
This is XeTeX, Version 3.1415926-2.5-0.9999.3 (TeX Live 2013/Debian)
 restricted \write18 enabled.
entering extended mode
This is XeTeX, Version 3.1415926-2.5-0.9999.3 (TeX Live 2013/Debian)
 restricted \write18 enabled.
entering extended mode
Rendering was successful. Cleaning up...
```

Alternatively you can change parameters by overwriting the `ENTRYPOINT`:

```bash
# docker run --rm -ti -v $(pwd):/src --entrypoint=xelatex luzifer/xetexgen --help
Usage: xetex [OPTION]... [TEXNAME[.tex]] [COMMANDS]
   or: xetex [OPTION]... \FIRST-LINE
   or: xetex [OPTION]... &FMT ARGS
[...]
```
