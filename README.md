This plugin interfaces [bibtex2html](http://www.lri.fr/~filliatr/bibtex2html/) with Jekyll
to generate an html bibliography list from bibtex entries.
For this to work, the bibtex entries must be enclosed in a special liquid block:

    {% bibtex _plugins/style.bst %}
      ....
    {% endbibtex %}

where `_plugins/style.bst` is a bibtex style file (which you can, of course, 
rename or move to another directory).

Setup
-----

* Install [bibtex2html](http://www.lri.fr/~filliatr/bibtex2html/). 
* Copy `bibtex.rb` to your `_plugins/` directory. 
* Edit `bibtex.rb` to tweak the options that are passed to `bibtex2html`.
* A default `style.bst` is provided. You can edit it to suit your needs or replace 
  it with any `.bst` file.

Example
-------
You can find a short usage example inside the `example/` directory
(the actual pdf files are missing, so the links will be broken).
This code is what I use (with some css minor differences) to generate
my own [publication list](http://www.sifflez.org/publications).

Limitations
-----------

The options that are passed to `bibtex2html` can only be changed 
in the plugin source. We should be able to change them per bibtex
block.

License
-------

This plugin is realeased under the MIT License.

Contact
-------

You can reach me at Pablo de Oliveira <pablo@sifflez.org>.
