# py2md - Doc Converter 

## py2md.py - Simple docs generator for Python code documented to Google docstring standard.

py2md is a simple Python 3 program to automatically generate a function reference guide for a Python project, in markdown format (.md).

To use py2md your project needs to meet the following requirements:

1. The Python files for your markdown output file reside in one folder. For a multi-folder project you could create a markdown file for each folder.
2. The Python files are commented using the [Google docstring style](https://google.github.io/styleguide/pyguide.html#Comments).

## Usage 
```
python py2md.py [-h] --sourcedir SOURCEDIR --docfile DOCFILE [--projectname PROJECTNAME]

Shortcuts: --sourcedir/-s, --docfile/-o, --projectname/-n
```

# Example
```
mkdir docs
cd docs
python .\py2md.py -s ..\azurerm -o README.md -n "azurerm - Azure REST wrappers"
```

You can see this example in action in the _azurerm_ Github repository: [azurerm technical reference](https://github.com/gbowerman/azurerm/tree/master/docs)

