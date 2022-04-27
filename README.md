# BaSCo-Corpus
Released April, 2022

* * *


1. [Introduction](#introduction)
2. [Data curation and Annotation](#data-curation-and-annotation)
    3.1. [NLU](#nlu)
    3.2. [Code-Switching](#code-switching)
    3.3. [Domain](#domain)
3. [Data structure](#data-structure)
4. [Corpus Statistics](#corpus-statistics)
5. [License](#license)
6. [Reference](#reference)
7. [Download](#download)
8. [Contact](#contact)

* * *



## INTRODUCTION

BaSCo  -Basque Spanish Code-Switching- is the first corpus with annotated linguistic resources encompassing Basque-Spanish code-switching. The mixture of Basque and Spanish languages within the same utterance is popularly referred to as Euskañol, a widespread phenomenon among bilingual speakers in the Basque Country. Thus, this corpus has been created to meet the demand of annotated linguistic resources in Euskañol in research areas such as multilingual dialogue systems. The presented resource is the result of translating to Euskañol a compilation of texts in Basque and Spanish that were used for training the Natural
Language Understanding (NLU) models of several task-oriented bilingual chatbots. Those chatbots were meant to answer specific questions associated with the administration, fiscal, and transport domains. In addition, they had the transverse potential to answer to greetings, requests for help, and chit-chat questions asked to chatbots. BaSCo is a compendium of 1377 tagged utterances with every sample annotated at three levels: (i) NLU semantic labels, considering intents and entities, (ii) code-switching proportion, and (iii) domain of origin.


***


## DATA CURATION AND ANNOTATION

### NLU

### CODE-SWITCHING

### DOMAIN


***


## DATA STRUCTURE

Here is a real example of an annotated utterance:

    {
         "referent": "dónde está la casa del deporte?",
          "source_lang": "es",
          "domain": "administration",
          "intents": [
            "preguntar|ubicacion",
            "informar|tipo-oficina"
          ],
          "entities": [
            {
              "entity": "tipo-oficina",
              "value": "casa del deporte",
              "normative_value": "deportes",
              "start": 14,
              "end": 29,
              "type": "bounded"
            }
          ],
          "code_switching": [
            {
              "text": "Casa de deporte non dago?",
              "entities": [
                {
                  "entity": "tipo-oficina",
                  "value": "Casa de deporte",
                  "normative_value": "deportes",
                  "start": 0,
                  "end": 14,
                  "type": "bounded"
                }
              ],
              "lang_proportion": "balanced"
            }
          ]
    }


***


## CORPUS STATISTICS


***


## LICENSE


The resources in this repository are licensed under the Creative Commons Attribution-ShareAlike 3.0 Spain
License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/3.0/es/ or send
a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.


***

## REFERENCE

To be published:

```
Aguirre, M., García-Sardiña, L., Serras, M., Méndez, A., and López, J. (2022).
BaSCo: An Annotated Basque-Spanish Code-Switching Corpus for Natural
Language Understanding. In *LREC*.
```

For any further information about the corpus, please refer to the mentioned paper.


***


## DOWNLOAD

The utterances tagged as valid can be found in: https://github.com/Vicomtech/BaSCo-Corpus/blob/main/valid_utterances.json

The utterances tagged as invalid can be found in: https://github.com/Vicomtech/BaSCo-Corpus/blob/main/invalid_utterances.json


## CONTACT

magirre@vicomtech.org

