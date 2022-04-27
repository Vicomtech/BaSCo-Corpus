# BaSCo-Corpus
Released April, 2022

* * *


1. [Introduction](#introduction)
2. [Data curation and Annotation](#data-curation-and-annotation)
    3.1. [NLU](#nlu)
    3.2. [Code-Switching](#code-switching)
    3.3. [Domain](#domain)
3. [Data structure](#data-structure)
4. [License](#license)
5. [Reference](#reference)
6. [Download](#download)
7. [Contact](#contact)

* * *



## INTRODUCTION

BaSCo  -Basque Spanish Code-Switching- is the first corpus with annotated linguistic resources encompassing Basque-Spanish code-switching. The mixture of Basque and Spanish languages within the same utterance is popularly referred to as Euskañol, a widespread phenomenon among bilingual speakers in the Basque Country. Thus, this corpus has been created to meet the demand of annotated linguistic resources in Euskañol in research areas such as multilingual dialogue systems. The presented resource is the result of translating to Euskañol a compilation of texts in Basque and Spanish that were used for training the Natural
Language Understanding (NLU) models of several task-oriented bilingual chatbots. Those chatbots were meant to answer specific questions associated with the administration, fiscal, and transport domains. In addition, they had the transverse potential to answer to greetings, requests for help, and chit-chat questions asked to chatbots. BaSCo is a compendium of 1377 tagged utterances with every sample annotated at three levels: (i) NLU semantic labels, considering intents and entities, (ii) code-switching proportion, and (iii) domain of origin.


***


## DATA CURATION AND ANNOTATION

The curation phase involved removing duplicates and filtering out which utterances were or were not valid for the target Euskañol corpus. To do so, a set of guidelines to determine the validity of an utterance was established. An utterance would be considered valid if:

• It is compliant with the task objective: the utterance is, to whatsoever extent, in a mixture of Spanish and Basque.

• From a semantic point of view, its content remains the same as its reference text’s: the same NLU labels are valid for both the reference utterance and the new one
in Euskañol. 

• It sounds natural: it could be an utterance that a person would use in a real conversation in Euskañol, it does not sound artificial.

Following these guidelines, only those utterances that were considered valid by at least 2/3 of the annotators would be included and annotated in the final corpus.

After invalid samples were filtered out, the next phase involved the annotation of the valid utterances.

### NLU

Semantically annotated with intents, entities, and their normative values when needed.

### CODE-SWITCHING

An additional annotation level includes annotator’s perspectives on the proportion of Basque and Spanish constituting the new Euska ̃nol utterance. Three main classes were defined for this level:

• more-es label: if it is considered that the utterance includes a larger proportion of Spanish than Basque.

• more-eu label: if it is considered that the utterance includes a larger proportion of Basque than Spanish.

• balanced label: if it is considered that the proportion of Basque and Spanish is more or less balanced.

Annotators’ considerations on the language proportion were not necessarily based on number of words or even morphemes in each utterance, but it was rather a more
general perspective on the whole sample based on native speaker intuition. In cases where annotators reached a tie between the three possible labels, the final label for the sample would be balanced.

### DOMAIN

Given that the source data was obtained from task-oriented chatbots, a label referring to the source domain was automatically included. The possible domain labels are: administration, transport, fiscal, generic, or social


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

