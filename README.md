# konig-ontodoc
A (web-based) user interface for browsing ontologies

## Usage

1. Clone this repository
2. Point you browser at `/dist/ontodoc.html`

The Ontodoc application will display a subset of the [Schema.org](http://schema.org/)
ontology.

## Customization

If you want to display documentation for your own ontology, you'll need to edit the 
file `/dist/js/konig-ontodoc-services.js`.

In that file, change the method 
```
	StaticOntologyService.prototype.getOntologyGraph
```
so that it returns a JSON-LD representation of your ontology.  The JSON-LD `@graph` may 
contain multiple ontologies.

If your ontologies are in some other format (such as Turtle or RDF/XML), you can
use [EasyRDF](http://www.easyrdf.org/converter) to convert them to JSON format.


