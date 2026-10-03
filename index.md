---
layout: base
title:  '<Chechen> UD'
udver: '2'
---

# UD for Chechen <span class="flagspan"><img class="flag" src="../../flags/svg/AQ.svg" /></span>

## Tokenization and Word Segmentation

* Words are generally delimited by whitespace.
* Multiword tokens in Chechen are formed with clitics that attach phonologically to the following or preceding host word. The clitics are:

    * The proclitic _ma_, which is used to negate imperatives and desideratives; otherwise it is used with emphatic functions
    * The enclitic _’a_, which has coordinating, additive, and emphatic functions 
    * The emphatic enclitic _q_
* Punctuation marks are attached to neighboring words. They are tokenized as separate tokens.
* There are no multiword tokens written with whitespace.

## Morphology

The morphological layer of the treebank includes Universal Part-of-Speech (UPOS) tags, lemmas, and a rich set of both universal and language-specific features.
Lemmas
Agreeing verbs and auxiliaries are lemmatized using their default `Dclass` citation form (e.g., the verb _j-axa_ "I go" is lemmatized as _d.axa_).
Pronouns are lemmatized to their base absolutive forms
Nouns are lemmatized to their singular forms in the nominative


### Tags

* Chechen-MottDT uses 16 tags, with the exception of [SYM]().
* The tag [PART]() is applied to the proclitic _ma_, the enclitic _q_, and the quotatives _boox_ and _baax_
* The tag [AUX]() is applied to two lexemes: _d.u_, which functions as a copula, and _xülu_, which serves as an auxiliary in complex temporal-aspectual constructions. 
Both items are inflected for grammatical agreement, tense, and have finite, participle, and free relative forms. 
In addition, the tag [AUX]() is applied to the lexical root _wa_ 'stay' when used as an auxiliary in complex temporal-aspectual constructions to contribute imperfective reading.
* The tag [DET]() is applied to pronominal items used attributively. One exception is possessive pronouns, which are all tagged as [PRON](). 
Predicative uses of pronominal items are tagged as [PRON]().
---
**Instruction**: Specify any unused tags. Explain what words are tagged as PART. 
Describe how the AUX-VERB and DET-PRON distinctions are drawn, and 
specify whether there are (de)verbal forms tagged as ADJ, ADV or NOUN. 

---

### Features

#### Nominal features

* Nouns inflect for [Case]() and [Number](). 
* There are two language-specific nominal features: [Log]{} and [NounClass]().

#### Verbal Features

---
**Instruction**: Describe inherent and inflectional features for major word classes (at least NOUN and VERB). 
Describe other noteworthy features. Include links to language-specific feature definitions if any.

---

## Syntax

* Chechen has ergative-absolutive alignment, ergative is marked, while absolutive is unmarked. 
Ergative-marked arguments are syntactic subjects of transitive verbs. Absolutive arguments are syntactic subjects of intransitive verbs and are syntactic objects of transitive verbs. 
Predicates agree with the absoultive argument; the case of the argument, the agreement pattern, and the valence of the predicate are used to distinguish between the subject and the object argument.

* The main copula construction in Chechen uses a form of the copula _d.u_. 
In finite clauses, the copula is inflected for subject agreement, tense, and aspect (as relevant).

~~~ conllu

1	so	so	PRON	_	Case=Abs|Number=Sing|Person=1	5	nsubj
2-3	juq	_	_	_	_	_	_
2	ju	d.u	ADV	_	NounClass=Jclass|Tense=Pres	5	cop
3	q	q	PART	_	_	2	advmod:emph
4	hwa	hwa	PRON	_	Case=Gen|Number=Sing|Person=2	5	nmod
5	jow	jow	NOUN	_	Case=Abs	15	root

so      ju       =q   hwa     jow
1SG.ABS J-be.PRS EMPH 2SG.GEN girl
"I am your daughter."
~~~

* There two language-specific relations: [advmod:emph](), [ccomp:reported](), and [obj:caus]().

* The subtype relations used are as follows:

    * [acl:relcl]()
    * [advmod:emph]()
    * [ccomp:reported]()
    * [compound:redup]()
    * [nmod:poss]()
    * [obj:caus]()


## Treebanks

There is [one](../treebanks/LCODE-comparison.html) Chechen UD treebank:

  * [Chechen-MottDT](../treebanks/UD_Chechen-MottDT/index.html)

---
**Instruction**: Treebank-specific pages are generated automatically from the README file in the treebank repository and
from the data in the latest release. Link to the respective `*-index.html` page in the `treebanks` folder, using the language code
and the treebank code in the file name.

---
