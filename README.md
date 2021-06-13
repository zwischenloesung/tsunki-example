# Tsunki

This is an example of a knowledge base implemented as a bunch of yaml files.
Its name derives from tsunki (ref. to https://en.wikipedia.org/wiki/Tsunki),
the great spirit of the waters, keeper of health and wisdom.

The example repository is also used as a sandbox. So use it as a first
help to get some guidance, but do not expect it to be complete or
finished.

## Goal

The basic idea behind the surrounding project is to have a very simple but
incredibly powerful, modular and extensible framework to organize ones thoughts,
ideas, concepts, insights, projects, things, relationships, what-evers.

'Tsunki' basically is the total of files that are structered following a
JSON/YAML-schema definition. Such files contain YAML documents called 'tsunki-things'.

A repository containing 'tsunki-things' is called a 'tsunki-context'.
Thus tsunki is the collection of all contexts.
All reachable 'tsunki-things' to a certain phenomenological stream
(stream of perception - e.g. by a human) can be combined and filtered
on demand by software and the selection of fragments is presented as
a 'tsunki-facet'.

To gain access to the 'tsunki-facets' relevant to you,
try [natem](https://gitlab.com/zwischenloesung/natem).


## Features

  * hierarchical and flat relationships, i.e.
    * is
      * multiple inheritance with priority
    * has
      * one/any
      * directed
      * different types
  * simple tags (beside categories defined by relation)
  * data and metadata
  * external references: URI
  * just a bunch of yaml files
  * multiple repositories supported
    * fully connected through `natem`, or
    * loosely referenced by URI

## Structure

  * nodes in tree representing entities resp. pointers to "things"
    * abstract or concrete entities
  * elements of a "thing"
    * entities (subject / object): "nouns"
      * id
        * uuid
        * name
        * urls
    * actions: "verbs"
      * relations
      * (modules)
    * modifiers: "adjectives" / "adverbs" / ...
      * properties

### Directories and Files

  * tree of yaml files as nodes
    * files (<object>.yml) or folders (<object>/init.yml) treated the same
    * free order (hierarchy optional), interpreted as "is"

### noun
#### categories / subject

  * Is-a relationship / inheritance
  * multiple inheritence supported
    * prioritized
      * this folder priority: 0
      * override priorities with values (< 0 >)
  * multiple ways to reference a category
    * containing folder: Throw a file into a folder and it automatically inherits the parameters of the init.yml in the folder with a priority of 0.
    * path, relative to repo
    * uri
    * uuid

#### target / objects

  * reference
    * external resource
    * containing folder: Throw a file into a folder and it automatically inherits the parameters of the init.yml in the folder with a priority of 0.
    * path, relative to repo
    * uri


### verb / action

  * relation between subject and object

### adjective / modifier

## Usage



