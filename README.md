# Jamulus Website

This is the home of the Jamulus Website and Wiki.



## Tech

Built with Jekyll

## Contribute

Want to contribute to the Jamulus Wiki/Website?
This project uses the fox css framework. See the [FOX-CSS documentation](http://www.fox-css.com/documents/).
CSS files can be found in the assets/css folder. More information about the files can be found at the README.md file in this folder. 

Translations are handled by the [Polyglot Yekyll Plug-in](https://github.com/untra/polyglot).
If you want to translate a file, you must first know where it is located on this repo. 

The homepage is located in the repo root and named [langcode]-index.html

To translate this file, please duplicate index.html and change the lang: attribute at the top of the file from lang: en to lang: YOURLANGUAGECODE

The wiki can be translated in the wiki/ folder. Just open the folder of the language you want to translate and find the file (or create it)

The Navigation of the wiki can be found in the _data folder.

The general translations for the whole site can e.g. be found in the _includes/general/YOURLANGUAGECODE folder. 

If you want to add a new language, you must follow the instructions on the polyglot site and add the folders/files. At least the footer, the Wiki Navigation and the Homepage should be translated. 
Please open a PR!
