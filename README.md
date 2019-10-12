# LaTeX IEEE template

Latex IEEE conference paper template. Based on the official `IEEEtran` template. The IEEEtran how to documentations is located in the `IEEE` folder.

## Citations

Package `bibTex` is used to create Citations. References is inserted into `bibliography.bib`.

## References

The package `cleveref` is enabled in the template for easier reference to chapters with it's name. Also the custom commands `Fullref` and `fullref` is created for the ability to create full references where the chapter number and it's name is printed out in the document.

## Tables

The template has support for .csv files out of the box. Which means that .csv-files is transformed into tables in the compiled document. The package `csvsimple` is providing the template with this support.

## Custom command

The template has a few different custom command, so called "oneliners" for easy writing and cleaner documents.

| Command    | inputs                                       | description                                                     |
| ---------- | -------------------------------------------- | --------------------------------------------------------------- |
| \fig       | position, caption, label, size, imagename    | Inputs image file into the document                             |
| \framedFig | position, caption, label, size, imagename    | Inputs image with black frame into the document                 |
| \tikzFig   | position, caption, label, filename           | Inputs tikZ image into the document. Filename is a `.tex` file  |
| \texTable  | position, caption, label, filename           | Inputs LaTeX-table into the document. Filename is a `.tex` file |
| \csvTable  | position, caption, label, filename           | Takes a `.csv` file and turn it into a LaTeX-table              |
| \code      | position, caption, label, language, filename | Inputs code from extrernal files                                |
| \fullref   | label                                        | Full reference mentioned in `reference` section above           |
| \numItems  | countList label                              | Get the size of a custom enumerate (countList)                  |

### Inputs

| Input    | Description                    |
| -------- | ------------------------------ |
| position | LaTeX position of the element  |
| size     | Float value between 0.0 - 1.0. |

### Examples

```latex
\fig{H}{figure caption}{figureOneLabel}{1.0}{imageOne.jpg}

\framedFig{H}{figure caption}{figureOneLabel}{0.5}{imageOne.jpg}

\tikzFig{H}{Tikz caption}{tikzLabel}{dataPlot.tex}

\texTable{H}{table caption}{tableLabel}{tableOne.tex}

\csvTable{H}{csv table catpion}{csvTableLabel}{table.csv}

\code{H}{code caption}{codeLabel}{cpp}{main.cpp}

\fullref{labelInText}

\numItems{countListLabel}
```

## Attachments

Attachments should be placed in the `attachments` folder. Depending on what kind of element that is inserted different path's should be used.
The `main.tex` hold's variables for the different paths (example below with the predefined paths). Change these paths to suit you're needs.

```latex
\graphicspath{{./attachments/figures/images/}}
\newcommand{\tikzPath}{./attachments/figures/tikz/}
\newcommand{\codePath}{./attachments/code/}
\newcommand{\tablePath}{./attachments/tables/}
```

These variables is used in the onelines mentioned above.
