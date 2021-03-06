---
title: Data preperation
drawer: true
category: Documentation
subCategory: User guides
---

# Data preperation

<p class="comment-warning">NB: This page has not been revised</p>
 
## Things to consider
  * create a local identifier if not existing
  * create full dwc:scientificName including authorship
  * create decimal coordinates & precision

## Database Source
  * setup a SQL view to use functions (can also be done in IPT sql source definition)
    * concatenation, splitting of strings: e.g. build full scientific name (watchout autonyms)
    * format dates ala ISO
    * create year/month/day by parsing native sql date types
  * use a UNION to merge 2 or more tables, e.g. accepted taxa and synonyms or specimen and observations
  * select fixed values (prefer to do this in IPT mapping)

## Text Files Source
  * convert to UTF8
  * use standard CSV (i.e. delimiter = , quotation = ") or TAB files
  * make sure you have replaced line breaks, i.e. \r \n or \r\n with either simple spaces or use 2 characters "\r" to escape the line break if the intention is to preserve them
  * encode NULLs as empty fields, i.e. no characters between 2 delimiters, not \N or \NULL

### Utility: Character encoding converter - iconv
Simple tool for unix and windows to convert character encodings of files.
  * http://en.wikipedia.org/wiki/Iconv
  * http://www.gnu.org/software/libiconv/
  * http://gnuwin32.sourceforge.net/packages/libiconv.htm

Examples:
  * convert character encodings from Windows-1252 to UTF-8 using [iconv](http://unixhelp.ed.ac.uk/CGI/man-cgi?iconv):
> > `iconv -f CP1252 -t utf-8 example.txt > exampleUTF8.txt`

### Utility: Unix Stream Editor,  SED
A unix commandline tool to manipulate files as streams, thereby allowing to modify very large files without the need to load them into memory first (this is what pretty much all editors apart from few, e.g. vi, do)

  * http://www.unixguide.net/unix/sedoneliner.shtml
  * http://www.brunolinux.com/02-The_Terminal/Find_and%20Replace_with_Sed.html
  * replace in place and create backup copy
> > `sed -i.old "s/\\\\N//g" allNames.txt`
  * convert DOS newlines (CR/LF) to Unix format:
> > `sed 's/.$//'`