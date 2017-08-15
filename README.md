# py2md - Documentation auto-generator 

## py2md.py - Simple documentation generator for Python source code.
py2md is a simple Python 3 program to automatically generate a function reference guide for a Python project, in markdown format (.md).

To use py2md your project needs to meet the following requirements:

1. The Python files that you want to document reside in one folder. For a multi-folder project you could create a markdown file for each folder.
2. Your Python source files are commented using the [Google docstring style](https://google.github.io/styleguide/pyguide.html#Comments).

## Usage 
```
python py2md.py [-h] --sourcedir SOURCEDIR --docfile DOCFILE [--projectname PROJECTNAME]

Shortcuts: --sourcedir/-s, --docfile/-o, --projectname/-n
```

## Example
```
mkdir docs
cd docs
python .\py2md.py -s ..\azurerm -o README.md -n "azurerm - Azure REST wrappers"
```

You can see this example in action in the _azurerm_ Github repository: [azurerm technical reference](https://github.com/gbowerman/azurerm/tree/master/docs)

## Why py2md, and not Sphinx, Napoleon, etc.?
I was originally planning to use Sphinx to auto-generate documentation for my Python project, and host it on readthedocs.org. After spending some time installing and setting it up, editing conf.py etc., I realized that in order to generate a well-formatted function reference based on Google-style docstrings, it would also need the Napoleon extension. Once some HTML documentation was created, and after getting various errors with readthedocs.org, I finally asked:

- Why not just create markdown docs to display in github?
- Why is it so complex to auto-create simple documentation from well structured docstrings?

The result is _py2md_, which has the following goals:
- Require only two mandatory parameters: source folder and output file. Additional optional parameters with good defaults are ok.
- Be a simple Python 3 script with no fancy installation or configuration requirements.

## Possible future enhancements
- Improve the core file processing loops (the code is a bit messy).
- Support static header and footer markdown files.
- Table of contents with hyperlinks to each section.
- Options links to source files.
- Provide an HTML output option.