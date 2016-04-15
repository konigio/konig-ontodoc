# konig-ontodoc
A (web-based) user interface for browsing ontologies

## Usage

1. Clone this repository
2. Point you browser at `/dist/ontodoc.html`

The Ontodoc application will display a subset of the [Schema.org](http://schema.org/)
ontology.

## Customization

There are two ways to display your own ontology in Ontodoc.  You can either
supply the URL to your ontology as the `src` query parameter, or you can edit
the `ontodoc.html` file to embed your ontology as a JSON object.

With the first approach, simply open ontodoc in your browser using a URL of the following form:

```
	{baseURI}/ontodoc.html?src={your-ontology-url}
```

For the second approach, open the `ontodoc.html` file in a text editor. At the bottom of the
file, you will find the following script.

```javascript
var defaultGraph = {...};
			
var ontologyService = new konig.AjaxOntologyService(defaultGraph);
konig.buildOntodoc(ontologyService);

});
```

Replace the value of `defaultGraph`	with a JSON-LD representation of your ontology.

If your ontologies are in some other format (such as Turtle or RDF/XML), you can
use [EasyRDF](http://www.easyrdf.org/converter) to convert them to JSON-LD format.


