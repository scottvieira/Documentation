CORAL Documentation Style Guide
-------------------------------

### About the Style Guide ###

The purpose of the style guide is to help keep the documentation consistent in style while at the same time providing tips for contributing to the CORAL Documentation Project (CDP) and other relevant information.

### Setting Up ###

The CDP is managed in a repo on GitHub found at [https://github.com/Coral-erm 
](https://github.com/Coral-erm  "https://github.com/Coral-erm ").  The project uses the [Sphinx Python Documentation Generator](http://www.sphinx-doc.org/en/stable/) and [ReCommonMark](http://recommonmark.readthedocs.io/en/latest/).  The documentation files are edited in a combination of [reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText) and [Markdown](https://en.wikipedia.org/wiki/Markdown), both markup languages supported by GitHub.  In addition, [Read the Docs](https://readthedocs.org/) is used for hosting the documentation and providing additional documentation conversion and indexing tools.   


### File Structure and File Naming Conventions ###

#### Images ####

1) Create a subfolder under /img using the same name as the markdown file in which the images will be used.  

For example, the following folder name for organizations.md

	/img/organizations/


2) Add images to the subfolder created in step 1.  Name the images with a prefix identifying the markdown file they are associated with, separated Uppercase letters with a brief description of the image. Note: The underscore character causes GitHub to incorrectly process the image filenames in Markdown, which leads to problems in building files in the ReadtheDocs.

For example: **organizationsAccountsView.png** for a a screenshot of the Organization's module accounts form.


