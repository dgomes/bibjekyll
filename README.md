Fork Info
----

This Plugin is a fork from [Pablo Oliveira](https://github.com/pablooliveira/bibjekyll) and intends to change from a Liquid Block into a Tag

The plugin interfaces [bibtex2html](http://www.lri.fr/~filliatr/bibtex2html/) with Jekyll
to generate an html bibliography list from bibtex entries.
For this to work, the bibtex entries must be enclosed in a special liquid Tag:

    {% bibtex _plugins/style.bst /complete/path/to/your/bibtex_file.bib %}

where `_plugins/style.bst` is a bibtex style file (which you can, of course, 
rename or move to another directory).

and where `/complete/path/to/your/bibtex_file.bib` is a bibtex file containing your references (and which requires the full path to it, since it assumes that you dont keep it in your jekyll path)

Setup
-----

* Install [bibtex2html](http://www.lri.fr/~filliatr/bibtex2html/). 
* Copy `bibjekyll.rb` to your `_plugins/` directory. 
* Edit `bibjekyll.rb` to tweak the options that are passed to `bibtex2html`.
* A default `style.bst` is provided. You can edit it to suit your needs or replace 
  it with any other `.bst` file.

Example
-------
You can find a short usage example inside the `example/` directory
(the actual pdf files are missing, so the links will be broken).
This code is what I use (with some css minor differences) to generate
my own [publication list](http://www.diogogomes.com/cv/).

Limitations
-----------

The options that are passed to `bibtex2html` can only be changed 
in the plugin source. We should be able to change them per bibtex
block.

License
-------

This plugin is released under the MIT License.

Contact
-------

You can reach me at Pablo de Oliveira <pablo@sifflez.org>.
