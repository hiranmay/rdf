# rdf
This project contains a simple rdf file (in .n3 notation) and a few sparql queries that can be run on them. The project has been designed to demonstrate encoding of simple scene graphs (spatial relations) in rdf, and querying on them. 
The scene graph used in this project is based on a snapshot of my desk as depicted the image **scene.jpg** (https://github.com/hiranmay/rdf/blob/main/scene.jpg). 
The scene graph is pictorially depicted in the image **scene-graph.png** (https://github.com/hiranmay/rdf/blob/main/scene-graph.png).
The rdf (n3) file encoding the scene-graph is in **scene-graph.n3** (https://raw.githubusercontent.com/hiranmay/rdf/main/scene-graph.n3). 
  **IMPORTANT:** You have to use http://... instead of https://... to specify the scene-graph with SPARQL endpoint.

We have included the following sparql queries:
* **sparql0**(https://raw.githubusercontent.com/hiranmay/rdf/main/sparql0): Retrieve all objects in the scene with their types.
* **sparql1**(https://raw.githubusercontent.com/hiranmay/rdf/main/sparql1): Retrieve all objects above the Desk (a specific object). Note that the items that are directly on the desk (i.e. Laptop, Mouspad and Book2) are retrieved. The items that are above these items (recursively), e.g. Mouse, Book1, Spectacles are not retrieved. See queries sparql3, sparql4
*  **sparql2**(https://raw.githubusercontent.com/hiranmay/rdf/main/sparql2): Retrieve all objects that are above an object of type Book (a class of objects). Book1 and Spectacles are retrieve.
*  **sparql3**(https://raw.githubusercontent.com/hiranmay/rdf/main/sparql3): Retrieves all objects above Desk recursively (as a union of sets). Also report the height they are at. Limitation: One need to know how many levels to go and explicitly code for every level.
*  **sparql4**(https://raw.githubusercontent.com/hiranmay/rdf/main/sparql4): Retrieves all objects above Desk recursively (in one statement). One need not know how many lavels to go. Limitation: Cannot find the height where the objects are.


The queries have been tested on the generic sparql endpoint SPARQLer (http://sparql.org/sparql.html) and Rasqual (https://librdf.org/query/)

**Following queries are recommended for the students.**

* Find all objects of type Gadget on the desk (recursively). Should retrieve Laptop, Mouse, Mousepad. ... also Spectacles which is a Wearable, a subclass of Gadget.
* Find all objects at the right of Laptop (recursively). Also implement the rule if y *right* x and z *above* y, then z *right* x, i.e. the query should retrieve the objects Mousepad, Mouse, Book1, Book2 and Spectacles.
* Find all objects to the left of Book1. Follow the logic: 
