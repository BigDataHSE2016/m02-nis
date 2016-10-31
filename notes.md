vfomichev@hse.ru
room 809 


# The impact of artificial intelligence theory and discrete math on Big Data Systems.
It's the main topic in this module.

## Semantic Web project and Big Data Systems
SW == Semantic Web

The SW prj was announced in 2001 by W3C.
The principal objective was as follows: to make the content of web pages readable not only by people but also by computer intelligent agents (aka CIA). 
So CIA'll be able to use the content of web pages and other web-based resources for solving the tasks formulated by the users.
The second objective was to considerably improve the preconditions of semantic (aka conceptual) information retrieval on the Web.
The central idea was to reach these objectives mainly with the help of 
- new semantically structured informational languages
- a rich family (to be developed!) of antologies (distributed knowledge bases) storing knoledge from numerous application domains

This task statements based on th results obtained during the preliminary stage of SW process (second half of the 1990s).
These results are:
- resource description framework (RDF) - it is interpreted as the simpliest information language for developing distributed databases and knowledge banks. The main data structure of RDF is triples of the form (A, B, C) where 
  - A is subject
  - B is predicate
  - C is object
- the language system RDF Schema (aka RDFS) in 1997-1999.
  - the ways of defining subclasses of objects 
  - it is possible to define a vocabulary of an application domain
  - it is possible to introduce semantic restrictions for the attributes of relationships and for the arguments and values of functions
  
### The first stage of SW project (2001- 2004)
RDF + RDFS => OWL (Onthology Web Language, 2004).
During last 12 years this language has been used as the principle tool for developing onthologies. A big family of web-based onthologies in many domains has been created.

### A possible look at the current state of Big Data Systems
[pic1 here]
LOD is a big data system , it can be imagined as a huge marked graph formed by elementary graphs representing RDF-triples (see pic1).
One of the main components of LOD is DBpedia, it has been auto. constructed by means of extracting semantic relations from wikipedia.

### The central Ideas of first order logic (FOL) approach to representic information
FOL is the central theory of mathematical logic.
FOL was the starting point for the Semantic Web project.
In partticular, the RDF triples ase equivalent to atomic formula of FOL.
Example:
RDF - (Leo Tolstoy, Authorship, War and Peace)
FOL - Authorship(Leo Tolstoy, War and Peace)

More detailes about the influence of FOL on SW project 
FOL => Terminological knowledge representation language (developed in AI theory)=> Description Logics => The languages RDF, RDFS, OWL, the algorithms of process. knowl. presented by this 
