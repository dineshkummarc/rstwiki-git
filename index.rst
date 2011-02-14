.. _index:

===========
rstWiki
===========

A simple reStructuredText based Wiki application. 

.. contents ::

Yet another wiki?
----------------------------

This one is simple. It serves a very specific purpose, though can be mangled very easily into something to suit 
your needs. 

rstWiki isn't a `real` wiki, it only pretends to be one. The content for the wiki is, very simply, decoded directly
from reST files on disk. Ideally, these reST files are stored in some form of VCS. rstWiki [will eventually] 
support both git and subversion. VC can be turned off to work directly, locally, or whatever. 

reST is a super powerful yet simple markdown syntax. 

But why not use [...]?
----------------------

Because it was too complicated. 

The Basics
----------

The very most basic of syntax explanations:

Paragraphs are lines of text separated by a blank link. 
This will not become a new paragraph. 

But this will.

Formatting inline text: **bold** ... *less bold* ... ``code`` ... `emphasis` ... 

A handy reference guide is available: http://docutils.sourceforge.net/docs/user/rst/quickref.html


Custom Directives
-----------------

reST is easily extensible. rstWiki ships a custom ``dojo.py`` module defining several custom directives. One 
custom directive included in the ability for reST to understand relative links similar to the way a wiki behaves. 
Sphinx uses these relative references to index content and generate the table of contents. 
eg: :ref:`this links to some internal wiki page "docs/test" <docs/test>`

If interested, checkout the :ref:`custom directives mini docs <docs/directives>`

Setup
-----

Get the code from: http://github.com/phiggins42/rstwiki 

The wiki will run standalone, serving html-rendered-reST data from a configured root path and static files from a 
defined folder.

First clone and init the submodules for the wiki:

.. code :: shell

    git clone git://github.com/phiggins42/rstwiki.git rstwiki
    cd rstwiki && git submodule init && git submodule update

Rename the ``conf.sample.py`` to ``conf.py`` and edit as needed. Then run the server:

.. code :: shell

   mv conf.sample.py conf.py && vi conf.py
   chmod +x wiki.py
   ./wiki.py

If this doesn't work out of the box or you need advanced setup options checkout the :ref:`advanced setup guide <docs/setup>`


Related Items
-------------

* python >= 2.6
* Sphinx
* docutils
* Pygments
* python-ldap
* git, svn
* CodeMirror
* CodeGlass
* Dojo, Dijit, Dojox
