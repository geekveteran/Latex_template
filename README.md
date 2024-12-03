# Latex_template

## Table of Contents

- [Latex\_template](#latex_template)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Features](#features)
  - [Installation](#installation)
  - [License](#license)
  - [Contact](#contact)

## Introduction

A simple guide about how to use latex in vscode. The best word editor for me is LaTex + Emacs(Vscode)+ Git(SVN).

## Features

- **Interactive Charting**:
  - Create bar, line, pie, scatter, and custom charts.
  - Support for multiple datasets and dynamic updates.
  - Customizable styles and themes.

- **Spreadsheet Management**:
  - Import/export data in various formats (CSV, XLSX, JSON).
  - Formulas and cell formatting.
  - Sorting, filtering, and conditional formatting.

- **Integration Ready**:
  - Works seamlessly with React, Angular, and Vanilla JS projects.
  - REST API support for server-side processing.

- **Accessibility and Responsiveness**:
  - Mobile-friendly and supports screen readers.

## Installation

To get started, follow these steps:

1. **Install the LaTeX**:

2. **Install the Git**:

3. **Install the Vscode**:

4. **Install the Vscode extension such as LaTex and LaTeX Workshop**:

5. **Set the Vscode setting Json**:

```json

{
  //------------------------------ LaTeX Configuration ----------------------------------
  // Set whether to auto-build
  "latex-workshop.latex.autoBuild.run": "never",
  
  // Right-click menu
  "latex-workshop.showContextMenu": true,
  
  // Auto-complete commands and environments based on used packages
  "latex-workshop.intellisense.package.enabled": true,
  
  // Set whether to show popup notifications on build errors
  "latex-workshop.message.error.show": false,
  
  // Set whether to show popup notifications on warnings
  "latex-workshop.message.warning.show": false,

  // Build tools and commands
  "latex-workshop.latex.tools": [
    {
      "name": "xelatex",
      "command": "xelatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOCFILE%"
      ]
    },
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOCFILE%"
      ]
    },
    {
      "name": "latexmk",
      "command": "latexmk",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "-pdf",
        "-outdir=%OUTDIR%",
        "%DOCFILE%"
      ]
    },
    {
      "name": "bibtex",
      "command": "bibtex",
      "args": [
        "%DOCFILE%"
      ]
    }
  ],
  
  // Configuration for the build chain
  "latex-workshop.latex.recipes": [
    {
      "name": "XeLaTeX",
      "tools": [
        "xelatex"
      ]
    },
    {
      "name": "PDFLaTeX",
      "tools": [
        "pdflatex"
      ]
    },
    {
      "name": "BibTeX",
      "tools": [
        "bibtex"
      ]
    },
    {
      "name": "LaTeXmk",
      "tools": [
        "latexmk"
      ]
    },
    {
      "name": "xelatex -> bibtex -> xelatex*2",
      "tools": [
        "xelatex",
        "bibtex",
        "xelatex",
        "xelatex"
      ]
    },
    {
      "name": "pdflatex -> bibtex -> pdflatex*2",
      "tools": [
        "pdflatex",
        "bibtex",
        "pdflatex",
        "pdflatex"
      ]
    }
  ],

  // File cleanup. This property must be an array of strings.
  "latex-workshop.latex.clean.fileTypes": [
    "*.aux",
    "*.bbl",
    "*.blg",
    "*.idx",
    "*.ind",
    "*.lof",
    "*.lot",
    "*.out",
    "*.toc",
    "*.acn",
    "*.acr",
    "*.alg",
    "*.glg",
    "*.glo",
    "*.gls",
    "*.ist",
    "*.fls",
    "*.log",
    "*.fdb_latexmk"
  ],

  // Set to "onFailed" to clean auxiliary files after a failed build
  "latex-workshop.latex.autoClean.run": "onFailed",
  
  // Use the last used recipe for compilation
  "latex-workshop.latex.recipe.default": "lastUsed",
  
  // Keybinding for internal viewer to sync with PDF (Ctrl/Cmd + click by default or double-click)
  "latex-workshop.view.pdf.internal.synctex.keybinding": "double-click",

  // Use SumatraPDF to preview the compiled PDF file
  // Set the internal PDF viewer for VSCode to the external viewer
  "latex-workshop.view.pdf.viewer": "external",
  
  // The viewer for the [View on PDF] links on \ref
  "latex-workshop.view.pdf.ref.viewer": "auto",
  
  // Command to open the external viewer when using SumatraPDF. Make sure to update the path.
  "latex-workshop.view.pdf.external.viewer.command": "F:/SumatraPDF/SumatraPDF.exe",
  
  // Arguments for the external viewer when used. The %PDF% placeholder is replaced with the absolute path to the generated PDF file.
  "latex-workshop.view.pdf.external.viewer.args": [
    "%PDF%"
  ],
  
  // Command to forward SyncTeX to the external viewer when syncing
  "latex-workshop.view.pdf.external.synctex.command": "F:/SumatraPDF/SumatraPDF.exe",
  
  // Arguments for SyncTeX when syncing with the external viewer. The %LINE% placeholder is replaced with the line number, %PDF% with the PDF file path, and %TEX% with the LaTeX source file path.
  "latex-workshop.view.pdf.external.synctex.args": [
    "-forward-search",
    "%TEX%",
    "%LINE%",
    "-reuse-instance",
    "-inverse-search",
    "\"F:/Microsoft VS Code/Code.exe\" \"F:/Microsoft VS Code/resources/app/out/cli.js\" -r -g \"%f:%l\"",
    "%PDF%"
  ]
}
   ```
## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For questions, feedback, or support:
