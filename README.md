TreeTagger part-of-speech tagging models for Sahidic Coptic
===========================================================
Version: 7 (includes POS tagging and lemmatization)

The part-of-speech tagging models are for use with the freely available TreeTagger 
(http://www.cis.uni-muenchen.de/~schmid/tools/TreeTagger/). The models are based
on the guidelines of the Coptic SCRIPTORIUM project, which closely follow Layton's (2004)
grammar. The lexicon used by the tagger is based on a lexicon kindly provided by Prof.
Tito Orlandi and the CMCL project (http://cmcl.let.uniroma1.it/). Please cite the CMCL
project whenever publishing research using the tagging models.

There are two different models: one for the coarse grained tagset, with 22 tags, and one
for the fine grained tagset, which distinguishes 44 tags (including individual tags for
each positive and negative conjugation base). For details on the tagset, see the 
documentation on the Coptic SCRIPTORIUM web page.

To use the models, download and unzip the TreeTagger. In the folder bin/ you will find
the TreeTagger excutable, which requires one of the two parameter files to run. TreeTagger
also expects an input file in a one-token-per-line format. For exaple, the input file input.txt could
include the following tokens (in UTF-8! The ascii characters below are for illustration purposes only): 

p
noute
pe
.

These will be tagged as:

p	ART
noute	N
pe	COP
.	PUNCT

To run the tagger, run the TreeTagger excutable as follows (Windows example): 

tree-tagger.exe coptic_fine.par -token input.txt output.txt

Or to include lemmas in a third column in the output use:

tree-tagger.exe coptic_fine.par -token -lemma input.txt output.txt

The option -token tells the TreeTagger that the input is already tokenized. For a Coptic tokenizer, 
see the Coptic SCRIPTORIUM project web page. Further options, such as allowing for SGML tags in the
input or outputting the word form as a lemma when the lemma is unknown, are documented in the 
TreeTagger documentation. For the coarse grained tags use coptic_coarse.par instead of coptic_fine.par.
