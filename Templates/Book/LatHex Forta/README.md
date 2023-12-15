# LatHeX Template

> A sober, hassle-free, LaTeX template for reports and books.

You can preview the template on a [real world report][forta-evasion-report].

## Preview

| Dark Theme                                       | Light Theme                                         | Forta Theme                                         |
| :----------------------------------------------: | :-------------------------------------------------: | :-------------------------------------------------: |
| [![Dark title page][demo-dark-title]][demo-dark] | [![Light title page][demo-light-title]][demo-light] | [![Forta title page][demo-forta-title]][demo-forta] |
| [![Dark page][demo-dark-page]][demo-dark]        | [![Light page][demo-light-page]][demo-light]        | [![Forta page][demo-forta-page]][demo-forta]        |

## Usage

The template is demonstrated with the example document in the repository:

```bash
# Get the code
git clone https://github.com/apehex/lathex-template.git && cd lathex-template/

# Build
lualatex --output-dir build/ main/book.tex
makeindex build/book.idx -s indexstyle.ist
biber main/book.tex
lualatex --output-dir build/ main/book.tex
```

The recommended compilers are `lualatex` and `xetex`, though `pdflatex` will mostly work too.
The only difference will be in the fonts for the `Forta` theme: it imports `ttf` files, which cannot be handled by `pdflatex`.

## Template structure

The project has the following tree:

```bash
< PROJECT ROOT >
   |
   |-- bibliography/          # The references
   |
   |-- build/                 # Where the compiled pdf will pop, as well as temp files
   |
   |-- images/                # Assets used in the document
   |
   |-- sections/              # All the individual sections
      |
      |-- part1/              # The sections of the first part
      |
      |-- appendices/         # The appendices at the end of the document
   |
   |-- template/              # The actual template definition, independent from the document it presents
   |
   |-- context.tex            # Optional script with the metadata (author, revision, date, etc)
   |
   |-- main.tex               # The script that assembles all the parts into one document
```

## Credits

The syntax highlighting for Solidity has been made by [Sergei Tikhomirov][solidity-syntax-highlighting]

The rest of the template is original work entirely.
Still it has roots in the popular LaTeX scripts mentioned below.

### Legrand Orange Book

The template started from the [Legrand Orange template][legrand-orange-book].

### Latexdraw.com

The cover page started from the templates in [Latexdraw][latexdraw-cover-pages].

## License

This work is licensed under the GNU [aGPL v3](LICENSE) by [apehex][github-apehex].

---

[demo-dark]: https://github.com/apehex/lathex-template/blob/main/build/dark.pdf
[demo-forta]: https://github.com/apehex/lathex-template/blob/main/build/forta.pdf
[demo-light]: https://github.com/apehex/lathex-template/blob/main/build/light.pdf
[demo-dark-page]: images/dark-page.png
[demo-forta-page]: images/forta-page.png
[demo-light-page]: images/light-page.png
[demo-dark-title]: images/dark-title.png
[demo-forta-title]: images/forta-title.png
[demo-light-title]: images/light-title.png
[forta-evasion-report]: https://github.com/apehex/web3-evasion-techniques/blob/main/report/forta.pdf
[github-apehex]: https://github.com/apehex/
[latexdraw-cover-pages]: https://latexdraw.com/tikz-cover-pages-gallery/
[legrand-orange-book]: https://www.latextemplates.com/template/legrand-orange-book
[solidity-syntax-highlighting]: https://github.com/s-tikhomirov/solidity-latex-highlighting
