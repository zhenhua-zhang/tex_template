# A Tex biorxiv template

The template was forked from [biorxiv-inspired-latex-style](https://github.com/alexsbaldwin/biorxiv-inspired-latex-style)


## Files and directories
```
├── config/
│   ├── latexmkrc
│   └── tikz.lua
├── figures/
│   └── LaTeX_project_logo_bird.png
├── pdfs
│   └── main.pdf
├── src/
│   ├── main.bib
│   └── main.tex
├── template/
│   └── biorxiv.sty
├── LICENSE
├── Makefile
└── README.md
```

### Contents directories and files

| Dir or file |  Description                                                  |
| :---------: | :------------------------------------------------------------ |
| `config/`   | Configuration, `lua` filters, etc.                            |
| `figures/`  | Directories where the `latexmk` to search figures.            |
| `pdfs/`     | Directories where the compiled `.pdf` files located.          |
| `src/`      | Source files e.g., `.tex` and `.bib` files.                   |
| `template/` | Style files, e.g., `.cls`                                     |
| `LICENSE`   | License of the `.tex` files, should be adapted accordingly.   |
| `Makefile`  | The `Makefile` to compile `.tex` files by a one-line command. |
| `README.md` | This README file.                                             |


## Build

For the convinience of compiling `.pdf`/`.docx` from the source `.tex` files,
a `Makefile` was included to create target PDF/DOC files by one-line command.

To compile all `.tex` files into `.pdf` files:

```{bash}
cd tex_template
make
```

Also, the `.tex` files can be converted into `.doc`/`.docx` files via `Pandoc`:
```{bash}
cd tex_template
make main.docx
```
Then, check `./tex_template/pdfs` for the compiled file.
Further format could be needed for better outlook.

To clean up:
```{bash}
make clean       # Clean all
make clean-build # Clean the intermediate files in ./build
```

**Note**:  
1. The content in `\tikzpicture` meta will be converted into pictures via a
`lua` filter in `./config` directory, when converting `.tex` files into
`.docx` files.

## Contact

For more information, please contact zhenhua.zhang217@gmail.com

## License

Attribution 4.0 International (CC BY 4.0). For more information, check LICENSE.

## To-do

- [ ] More style files

<!-- vim: set ai ft=pandoc ts=4 tw=120: -->
