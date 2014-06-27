#Sentiment lexicons#

Sentiment lexicons (polarities, aspects) created following several approaches within the OpeNER project.
This is the list of lexicons created and stored in different subfolders:

##lexicons_from_annotations##
Lexicons created from the manual annotated news articles (this data can
 be found also in github, https://github.com/opener-project/opinion_annotations_LANG where
 $LANG can be en/es/fr/nl/de/it) using the supervised 
heuristic implemented in https://github.com/opener-project/opinion-domain-lexicon-acquisition.

##propagation_lexicons##

General lexicons created automatically using the propagation algorithm implemented in https://github.com/opener-project/VU-lexicon-propagation_kernel, and manually
review of the most frequent words for each language. The lexicon comprises the final lexicon after
the manual checking, in CSV and LFM formats, with the manual check items marked explicitly.

These are the parameters used for the automatic propagation of the lexicons:

* Lemma-based output
* Synonymy, antonymy and hyponymy relations of WordNet selected
* Maximum 5 iterations of propagation starting from the seed list (these lists can be found as well in the data)
* Majority voting heuristic for converting synset-based lexicon to lemma-based.

The methodology, evaluation and further details of our approach and implementation of the propagation algorithm can be found in the PDF file
fivepropagations_lrec2014.pdf. Please cite the next paper if you use this work:

```
Generating Polarity Lexicons with WordNet propagation in 5 languages
Isa Maks, Ruben Izquierdo, Francesca Frontini, Montse Cuadros, Rodrigo Agerri and Piek Vossen
9th LREC, Language Resources and Evaluation Conference. May 2014. Reykjavik, Iceland.
```



##cross_cultural_multilingual_lexicon##

This folder the OpeNER cross-lingual lexical resource, which consists of domain-related opinion expressions in the 6 OpeNER languages with mutual inter-lingual and intra-lingual links. The expressions are classified in a sentiment category and labelled for aspect class. A set of opinion expressions within the same aspect class and mutually linked by inter- and intra-lingual links is called a “cross-lingual scale”. The lexicon is built semi-automatically amd starts form the manual opinions of the OpeNER annotated corpus. The annotated opinion expressions are linked to each other with inter-lingual and intra-lingual links. 

More information on the resource can be found in OpeNER deliverable D5.21. The lexicon is published in 2 formats CSV and OPeNER-LMF (XML).

#####CSV (crosslingual.csv)
```shell
de;unfreundlich;negative;BEHAVIOUR;11
en;unfriendly;negative;BEHAVIOUR;11
fr;très peu aimable;strongnegative;BEHAVIOUR;11
nl;niet bepaald vriendelijk;negative;BEHAVIOUR;11
nl;alles behalve vriendelijk;strongnegative;BEHAVIOUR;11
en;not friendly at all;strongnegative;BEHAVIOUR;11
fr;pas aimable;negative;BEHAVIOUR;11
nl;niet vriendelijk;negative;BEHAVIOUR;11
```
each row presents :  languageid, the opinion expression, polarity, aspect group, clsId 
clsId is the id which links together a group of opinion expressions within and across different languages

#####OpeNER LMF XML (crosslingual.lmf)
The LMF version of the lexicon includes the same information as the CSV but represented according to the Lexicon Markup Format guidelines.
cf. D5.21 and the dtd for more information on this version of the resource


#####OpeNER LMF dtd (opener_LMF_ML.dtd)
The dtd  is a second  version of the OpeNER LMF dtd for sentiment lexicons extended with a component for description of multilingual data. 




##Contact##
* Ruben Izquierdo
* Vrije University of Amsterdam
* ruben.izquierdobevia@vu.nl
