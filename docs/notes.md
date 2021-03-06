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

[the second lecture is missed]

### 2.7 The class of firs-order languages

### 2.8 A method of representing a meaning of a natural language text as a formula of FOL
Definition from theoretial linguistics and AI theory: a semantic role is a relation between a meaning of a verbal form (verb, infinitive, gerund, etc.) and a meaning of a word combination (or a word) _depending in a sentence_ on this verbal form.
Example: Let T1 = "Anton has switched off the computer."
- (has switched off, Anton) is a relation called Agent
- (has switched off, computer) is a relation called Object
One says that the semantic roles Agent and object a explicitly realised in T1.

The notion 'semantic role' has several synonyms:
- deep case (1968) ("глубинный падеж")
- conceptual case
- semantic case
- thematic role

Computational linguistics includes a special branch called Semantic Role Labelling. The objective is to develop the methods of discovering possible semantic roles realised in the pairs of the form (verb form, dependent word combination or a word).


Definition from theoretical and computational linguistics: let Expr be an expression in natural language (NL). Then a formal structure Semrepr is called a possible semantic representation (SR) of Expr in case the formal structure Semrepr is composed by semantic units informational units) but not by the words and reflects semantic relations between the elements of Expr.

This formal structure Semrepr may be a string or an array of stings, a textual file, a marked graph (a semantic net), etc.

=> Consider the steps of building a possible semantic representation of a natural language text as a formula of FOL.  

Let Disc1 (discourse) be "Robert Price developed alpha technology in the year 2012. As a consequence he became next year a vice president of a company Rainbow."

Step 1: We introduce the marks of different entities mentioned in the considered text. Formally, theses marks are variables.
e1 - the mark of the event 'developing alpha technology'
e2 - the mark of the event 'recieving a working position'
x1 - the person Robert Price
x2 - the technology called 'alpha technology'
x3 - the company Rainbow
t2 - the time of the event e2

Step 2: We define the set of constants Const: "robert", "Price", "Rainbow", 2012/year, person, development1, recieving-working-position, technology, company1, "aplha-technology"

Step 3: We introduce the set of functional symbols F and the set of predicate symbols.
Let F = {NextYear}
Pred = {Sem-descr, Agent, New-product, Time, Name, Surname, Name1, Working-position, Part-time
Let's believe that Pred contains binary predicates.

Step 4: We construct atomic formula reflecting sertain pieces of the text's meaning.
Cause(e1, e2),
Sem-descr(e1, development1),
Agent(e1, x1),
Sem-descr(x1, person),
Name(x1, "Robert"),
Surname(x1, "Price"),
New-product(e1, x2),
Sem-descr(x2, technology),
Time(x1, t1),
Part-time(t1, 2012/year),
Name1(x2, "aplha-technology")

=> now we do have the components for reflecting the meaning of the first sentence.
=> Let's act in a similar way for the second sentence.
Sem-descr(e2, recieving position),
Agent(e2,x1)
Working-position(e2, vice-president)
Organisation(e2, x3)
( => include Organisation into the set Predicates)
Sem-descr(x3, company1)
Name1(x3, "Rainbow")
Time(e2, t2)
Part-time(t2, NextYear(2012/year))

=> Very likely we do have all components for constructing a formula being a possible semantic representation of Disc1.
The prepared atomic formulas are used for constructing a possible SR of the given text.

=> see an electronuc guide illustrating step 5 for the text Disc1.

=> Home task1 preliminary: construct a SR of the considered discourse Disc1.
Remark 1: please pay attention to small differences in atomic formulas considered during the lecture and in the electronic guide.
Remark 2: please finf a typing error in SR of Disc1 in the electronic guide (the bottom of last page).

In particular the formula Cause(e1, e2) is default (?)

HW: print on paper!!! page 1 is a title page
Deadline: 28.11
Consulting: 21.11

HW: Invent a discourse containing 2 or 3 sentences (like Disc1). It should pertain to a real fiels of professioanl activity. The invented discourse is to describe 2 or more events. There are casual and time relations between these events.
Objective 1: define a logical basis LogBS fro buildin a semantic representation of the considered text.
Objective 2: construct a formula  Sem-repr from (Formulas(LogBS)) being a possible SR of your discourse.

[lection #3  should be here]

### 3.4 The topicality of using NLP in Big Data Systems
Let's consider the principal objectives of an international company "Expert System Semantic Intelligence" (founders are from Italy).

//links here

Rationale for using NLP in BDS:
- Big date is largely unstructured in a state of permanent growth. It is also mostly text.
NLP of Big data is the next great oppotunity. For example (stored textual information):
  - customer and sales information
  - transactional data
  - external open-source information (in particular from social media)
- NLP helps computers to understand not only simple words and word combinations but also sentences and discourses as they are spoken or written by a human. Regardless of the sector every business today relies on large volumes of textual information. For example, a law firm works with large volumes of past and ongoing legal transaction documents, notes, email correspondence as well as large volumes of governmental and specialied reference information. Example 2: A pharmacentical company has to deal with large volumes of clinical trial information and data, doctors' notes, patient information and data, patent and regulatory information as well as the latest research on competitors.

Current applications of NLP:
- smartphones assistances like Apple's Siri
- intelligence interfaces in online banking
- retail self-service tools

The users ask questions in everyday language and recieve an immediate accurate answers.

####  Nearest applications of NLP in BDS:
##### Business intelligence
NLP for Big data can be leveraged to automatically find relevant information and/or summarige of the content of the documents in large volumes of information for collective insights (see first web reference).

##### Sentiment Analysis
Sentiment Analysis (extraction of users' opinions).
Social channels are a rich (though noisy) source of valuable information. Using NLP for sentiment analysis the companies can understand what is being said about their brands and products as well as how it is being talked about - how users feel about the service, product or concept idea.
This is a powerful way to discover information about the market and current and potentional customers, opinions and information about customer habits, preferences, needs and wants as well as demographic information.
This information can be than applied to product development, BI and market researches.

##### Semantic technology Cogito.
The company "Expert System Semantic Intelligence" has developed a semantic technology (it takes into account the meanings of words and sentences) called Cogito.

Cogito leverages deep learning and AI algorythms for simulating how people understand language and in this way the system recognizes the meanings of words in context.

(see the second web reference)

Cogito understands that the text is about politics and econmics even if it doesn't contain the exact words but contains the related concepts.

##### A distinguishing feature of semantic technology.
Unlike keywords and statistics technologies all machine-learning and probabilistic algorithms approaches Cogito does not process a text as a string of characters without considering the concepts (the meanings) they express.
Relying on a deep semantic analysis and the  constructed knowledge graph Cogito tries to understand a text as a person would.
The same can be said about the algorithms of semantic parsing by Fomichov (see yellow book).

### Homework 2
Make a try to discover some intelligent abilities of the semantic technology [Cogito](http://www.intelligenceapi.com/demo/).
Print your dialogs with Cogito (several pages, >= 2) and submit the printed texts on next Monday.  

Remember that the theory of K-representations considers (introduces) 2 classes of formulas: l-formulas, t-formulas and y-formula.

Only l-formulas and t-formulas are used as semantic representations of expressions in NL.
Y-formulas are used for mathematical investigation of the properties of l-formulas and t-formulas.

[missed part]
Examples:
- (space.ob, dyn.phys.ob) belong to Gen
- (space.ob, space.ob) belong to Gen
- (sit, event) belong to Gen
- (real, natural) belong to Gen
- (real, real) belong to Gen

There is a simpler form for expressing  the same information:
- space.ob -> dyn.phys.ob
- space.ob -> space.ob
- sit -> event
- sit -> sit
- real -> natural
- real -> real

Z^5 = X - a  - a countable set of symbols , this set is called a primary informational univers X\supset St.

The elements of X are interpleted as primary informational units.
Examples:

(this function associates the set of all suppluers with the concrete entrprise )

Theoretical home task:
Grasp the interpretations of distinguished elements from the list Z1...Z15. These elements will be indicated in the email.
Ch. 3 of the book.
The first element is Z4 - Tol.

2016-12-12
### Shortly about a system of partial operations for constructing semantic representations of arbitrarily complex natural language sentences and discourses.

This theme relates to text mining.

A fundamental question is how the expr. of NL are organised on the level of structured meanngs (semantic level) and on semantic level.
Practical significance of an answer to this question : we'll be able to represent the meaning of a search request  as an expression of a certain semantic language (intermediate level). Than we do the same with the meaning of an analysed fragment of a text stored on web (possibly in a different NL) => it would be possible to compare meaning1 (request) and meaning2 (fragment) and to take a desision about the usefullness of the analysed text.

As far back as 50 years ago, the scientists had no reasonable answer to this fundamental question.

The first mathematically complete answer was formulated in the paper "The mathematical model for describing structured items of conceptual level" by ????. This paper described a system consisting of 10 partial operations on concepual structures , in particular a new class of formal languages was defined: the class of restricted standard knowledge languages (RSK-languages). A modified version of this system of 10 partial operations is described in the monograph by Fomichov (2010).
=> let's consider very short characteristics of 10 partial operations on conceptual structures.
These operations enable us to build SRs of arbitrary complex NL-texts.

For k = 1,...,10 the partial operations Op[k] is defined by a statement (called a rule) P[k].

Op[1] allows to build l-formulas of the form
```
qtr conc,
```
where qtr is an intersional quantifier ( a semantic untit corresponding to the words and word combinations
```
arbitrary, any, a certain, all, several, etc.
```
), conc is a simple or compound designation of a notion.

Examples:
- certain person
- certain textbook
- all person
- all textbook
- certain person * (Coubtry, Russia)
- certain textbook * (Level, high-school),(filed of knowledge, biology)

Op[2] constructs l-formula of the form f(a1,..an), where n>=1, f is the designation of a function with n arguments and a1-an are the designations of the arguments.

Examples:
- Capital(Russia)
- Number_of_inhab(Capital(Russia))
- Suppliers(IBS)
- Friends(P.Somov)
- Price(certain car * (Manufacturer, BMW))


Op[3] enables us to construct l-formulas (a1==a2) where a1, a2 are l-formulas.

Examples:
- (Capital(Russia) == Moscow)
- (Price (Cretain Car) == x7)

p.82 of the book

### The ways of constructing compound designations of objects and sets from compound designations of notions
