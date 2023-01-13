# Chiasmi Dataset(s)

This github repository contains an extensive number of annotated data: salient chiasmi and antimetaboles and non-salient antimetaboles. It is also accompanied by a list of random sentences that are not specifically chiastic.

It can be thus be used for any NLP tasks involving chiasmi that needs a large amount of data, like ML and DL models training, for tasks like detection, classification or generation.

## Origin of the data

The salient chiasmi were extracted from various places, including the work of Dr. Marie Dubremetz and Dr. Joakim Nivres on chiasmus detection, the work and direct help of Pr. Randy Harris, the book "Never let a fool kiss you or a kiss fool you" by Dr. Mardy Grothe and various - sometimes serendipitous - findings on the internet. The non-salient antimetaboles were extracted from a subset of the [COCA dataset](https://www.english-corpora.org/coca/). The random sentences were extracted from several datasets from [Data World](https://data.world/): [200k English plaintext jokes](https://data.world/taivop/200-k-english-plaintext-jokes), [un_general_speeches](https://data.world/jmalina/un-general-speeches) and the abstract part of [arXiv STEM scholarly articles](https://data.world/liz-friedman/arxiv-stem-scholarly-articles)

This data was gathered by Yohan Meyer, Diana Nurbakova and Guillaume Berthomet with the help of Jelena Mitrovic and Ramona Kühn.

## Organization and location of the data

The data is organized in json files. Each json file contains a unique list, in which the examples are listed. Each chiasmi has at least two properties: *text* is the raw text containing the antimetabole and *category* is the category of the chiasmi. The category can be one of: `Antimetabole`, `SemanticChiasmus`, `PhoneticChiasmus`, `NonSalientAntimetabole` and `NotAntimetabole`. The difference between the latter two is that a nonsalient antimetabole will still include an inverse repetition of lemmata,  whereas a phrase that is not an antimetabole should not show any inverse repetition.

All the data can be found in the `data` sub-folder, in one of the following files:
- Files with only positive examples of chiasmi:
  - `salient.json`contains all salient chiasmi and antimetaboles. In particular, this file also has extra information about the chiasmi from those dataset, with an indication - when known - of the **source** in which it was found and its **original author**.
- Files with only negative examples of chiasmi:
  - `nonsalient-antimetaboles.json` contains all rhetorically nonsalient antimetaboles. All of those can be considered negative examples of "true" antimetaboles.
  - `not-chiasmi.json` files contains all the extracts without any specific inverse repetition.
- Files with some combinations of both:
  - `all-data.json` contains **all** the data collected, including non-antimetabole text extracts.
  - `all-chiasmi.json` contains all the chiasmi and thus antimetaboles, including nonsalient antimetaboles but not the non-antimetabole extracts.
  - `all-antimetaboles.json` contains all antimetaboles, salient and non salient ones, but no other type of chiasmi.
