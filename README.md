This project contains a simple rdf file (in .n3 notation) and a few sparql queries that can be run on them. The project has been designed to demonstrate encoding of simple scene graphs (spatial relations) in rdf, and querying on them. 

The scene graph used in this project is based on a snapshot of my desk as depicted this image (https://github.com/hiranmay/rdf/blob/main/scene.jpg). 
The scene graph is pictorially depicted in this image (https://github.com/hiranmay/rdf/blob/main/scene-graph.png).
The rdf (n3) file encoding the scene-graph is here (https://raw.githubusercontent.com/hiranmay/rdf/main/scene-graph.n3). 
  **IMPORTANT:** You have to use http://... instead of https://... to specify the scene-graph with SPARQL endpoint.

We have included the following sparql queries:
* **sparql1**: Find all items above the Desk (a specific object). Note that the items that are directly on the desk (i.e. Laptop, Mouspad and Book2) are retrieved. The items that are above these items (recursively), e.g. Mouse, Book1, Spectacles are not retrieved. See queries sparql3, sparql4
*  **sparql2**: Find all items that are above an object of type Book (a class of objects). Book1 and Spectacles are retrieve.


The queries have been tested on the generic sparql endpoint SPARQLer (http://sparql.org/sparql.html)
