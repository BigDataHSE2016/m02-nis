# The impact of artificial intelligence theory and discrete math on Big Data Systems.
It's the main topic in this module.

## Semantic Web (SW) project and Big Data Systems

The SW prj was announced in 2001 by W3C.
The principal objective was as follows: to make the content of web pages readable not only by people but also by computer intelligent agents (aka CIA). 

So CIA'll be able to use the content of web pages and other web-based resources for solving the tasks formulated by the users.

The second objective was to considerably improve the preconditions of semantic (aka conceptual) information retrieval on the Web.

The central idea was to reach these objectives mainly with the help of 

- new semantically structured informational languages
- a rich family (to be developed!) of antologies (distributed knowledge bases) storing knoledge from numerous application domains

This task statements based on the results obtained during the preliminary stage of SW process (second half of the 1990s).
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

<img src='http://g.gravizo.com/g?
@startuml;
package "Big Data Systems" {;
    package "Semantic Web" {;
    [Linked Open Data \n%28LOD%29];
    [A family of OWL-based \nontologies];
    [==TODO ==Something];
    };
};
@enduml
'>

LOD is a big data system , it can be imagined as a huge marked graph formed by elementary graphs representing RDF-triples (see pic1).

One of the main components of LOD is DBpedia, it has been automatically constructed by means of extracting semantic relations from wikipedia.

### The central Ideas of first order logic (FOL) approach to representic information
FOL is the central theory of mathematical logic.
FOL was the starting point for the Semantic Web project.
In partticular, the RDF triples ase equivalent to atomic formula of FOL.

Example:

- RDF - (Leo Tolstoy, Authorship, War and Peace)
- FOL - Authorship(Leo Tolstoy, War and Peace)

### More detailes about the influence of FOL on SW project 
FOL => Terminological knowledge representation language (developed in AI theory)=> Description Logics => The languages RDF, RDFS, OWL, the algorithms of process. knowl. presented by this 

### 2 classes of well formed expressions in FOL
**Class 1** consists of terms. The terms are interpreted as simple and compound designations (or names) of the objects (aka entities) from considered application domains. 

Examples of simple terms:

- Russia, India, China, Austria, 
- Moscow, Vieanns
- x1, y3, z12
- green, yellow
- 22, 421212
- 650/km, 320/eur

For the construction of the compound terms it is nessesary to use the names of functions. 
Examples of compound terms:

- Capital(Austria), Area(Capital(Austria)),
- Distance(Moscow, Vienna), 
- Distance(Capital(Austria), Capital(Russia)), 
- +(12, 8), +(x3, 81),
- *(+(12,8), -(21, 16)
- Height(x5), Price(z7)

**Class 2** consists of formulas . They represent the meanings of the statements (aka propositions aka assertions).

The statements are phrases with the linked element from the set {true, false}.

Example 1: Charles Price has a BMW car. 

The examples of simpliest (atomic) formulas: 

- Part(Moscow, Russia), 
- Less(+(12, x2), *(12, r5)), 
- Qualification(PNosov, Programmer)

Arbitrary complex formulas are constructed from atomic formulas with the help pf logical connectives NOT, OR, AND, ~ (aka equivalence), -> (aka mplication) and with the help of logical quantifiers  (aka universal quantifier and (aka existence quantifier).

Example of complex formula: 
$$\forall x1(Natural(x1) \rightarrow \exists x2 (Natural(x2) \wedge Greater(x2, *(x1, 200)))$$

### The groups of basic symbols for building expressions in FOL
**Group1** = Const constants

Examples: Russia, Moscow, HSE, Nosov, Enterprise, person, firm

**Group2** = Var consists of variables.

Examples: Var = ${x1, x2, ...} \cup {y1, y2, ...} \cup {z1, z2, ...}$

**Group 3** = F consists of functional symbols (aka the names of functions).

Example: ${Height, Weight, Capital, +, -, *, Distance}$

**Group 4** = Pred consists of the elements called predicate symbols (aka the names of predicates).

Example: ${Odd, Even, Less, Part, Greater, Colour}$

Definition 1 (a denotation): Let $Z$ be anarbitrary non-empty set, and $n >= 1$. Then

- $Z^n = Z$,  $n = 1$, 
- $Z*Z*Z (n times)$, $n > 1$

Example: If Z is $\mathbb{R}$ (all real numbers) , the $Z^3 = \mathbb{R} ^3$ is a 3-dimentional space. 

The set $Z^n$ is called the *Carthesian n-degree* of the set Z.

Definition 2 (a goal denotation): Let Z be anarbitrary non-empty set, and $n >= 1.$ Then [latex here]
an n-any predicate on Z is arbitrary function p:
$p: Z^n -> {true, false}$

- in case $n = 1$ p is called an unary predicate on Z
- in case $n = 2$ p is called a binary predicate on Z 

Example 1: Let Z the set of all people and the function Boss is defined as follows: for every a, b in Z (where a != b) Boss(a,b) = true <=> there is an organisation C such that b is a chief of a in organisation C => Boss is a binary predicate on the set of all people


