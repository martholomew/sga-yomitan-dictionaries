# SGA (Old Irish) Yomitan Dictionaries

Currently, only corPH, EIGD, and OG are available, as the copyright situation with eDIL is investigated.

## Summary of Dictionaries
| Dictionary | Copyright | Headwords | Focus | Currently? | Download |
| -- | -- | -- | -- | -- | -- |
| [eDIL](#electronic-dictionary-of-the-irish-language-edil) | Copyrighted | 35,466 | Creating a complete dictionary of Old / Middle Irish | Ongoing | *unavailable* |
| [corPH](#corpus-palaeohibernicum-corph-2021) | MIT | 8,073 | Investigating the evolution of Old Irish grammar through extensive tagging of Old / Middle Irish material | Complete, potentially will continue | [latest](https://github.com/martholomew/sga-yomitan-dictionaries/releases/latest/download/corPH.zip) |
| [EIGD](#early-irish-glossaries-database-eigd-2009) | MIT | 2,361 | Transcribing and creating concordances of major Old Irish glossaries | Infrequent updates | [latest](https://github.com/martholomew/sga-yomitan-dictionaries/releases/latest/download/EIGD.zip) |
| [OG](#onomasticon-goedelicum-og-1910) | Unknown | 25,312 | Transcribing the onomastical information in Onomasticon Goedelicum | Complete | [latest](https://github.com/martholomew/sga-yomitan-dictionaries/releases/latest/download/OG.zip) |

## Electronic Dictionary of the Irish Language (eDIL)
*Copyright Status*: Assumed to be under copyright

### Description
The most complete dictionary of Early and Medieval Irish, it is based on the Dictionary of the Irish Language (DIL), which was published in parts between 1913 and 1976.[^1] DIL was digitized and published in electronic format using TEI-formatted XML as eDIL in 2007. There were two further large-scale editions of eDIL containing corrections and new data in 2013 and 2019, with further corrections undertaken in smaller-scale efforts.

[^1]: https://dil.ie/about

This project utilized the 2013 edition as the xml is available to freely download on Github.[^2] No license is contained with the data, so it is assumed to be under copyright.

[^2]: https://github.com/e-dil/dil

### Statistics (eDIL 2013)
Of the 42,700 words in the 2013 edition, around 35,466 are words proper, and around 7233 are references to other words in the form “abaide: x see apuide.”

### Part-of-Speech Breakdown*
| Part-of-Speech | Attestations |
| -- | -- |
| Nouns | 18,238 |
| Adjectives | 6,981 |
| Verbs | 4,052 |
| Undetermined** | 2,464 |
| Proper Nouns | 1,321 |
| Verbal Nouns | 1,153 |
| Participle | 340 |
| Adverbs | 239 |
| Pronouns | 119 |
| Gerunds | 111 |
| Prepositions | 87 |
| Substantives | 72 |
| Conjunctions | 55 |
| Prefixes | 55 |
| Numerals | 48 |
| Interjections | 34 |

*any part-of-speech with less than 30 attestations is not shown
**marked as “ind” in eDIL

### Data Quality

| Data | Quality |
| -- | -- |
| Alternative Forms | ✓✓ |
| Conjugations/Declensions | — |
| Definitions | ✓✓ |
| Examples | ✓✓ |
| Gender | ✓ |
| Part-of-Speech | ✓ |
| Stem | ✓ |
| Verb Class | x |


eDIL is extremely verbose and reliably contains most of the important grammatical information required to enable a reading of Old and Middle Irish texts. Most of this information is easily extractable using any programming language, and it only becomes complicated in the details. Owing to its compilation over a large length of time as mentioned above, there are a great variety of terms used (and spellings of those terms), which required a considerable amount of normalization in order to consistently parse the data. An illustrative case is the part-of-speech tag for “verbal noun”, it is variably written as “vn”, “Vn”, “Vn.”, “vn.”, “VN.”, “vnn.” and “Vnn.”. This is a consequence of accurately copying DIL as it stood, which is a laudable achievement; there is now room, however, to produce a more normalized copy of eDIL, keeping the original as it stood.

It is regretfully difficult to reliably parse the conjugation and declension data in eDIL. The XML which resulted from the digitization is highly descriptive, but it is not easy to perform data harvesting on; about 70% of the total declension and conjugation data can be easily extracted using an extremely fragile process, but even then it will likely make a plethora of mistakes while combing through the XML with a fine-toothed comb. The data that is extracted is of questionably-good quality, and this process needs to be further refined. In summary, the database is great in breadth and depth, but the depth is difficult to access.


## Corpus PalaeoHibernicum (CorPH) (2021)
*Copyright Status*: MIT Licensed[^3]

[^3]: https://github.com/chronhib-MU/Chronhib-Website

### Description
CorPH is a deeply annotated corpus of mostly Old and some Middle Irish texts which was output by ChronHib as a part of an effort to extract meaningful information on the evolution of the Irish language.[^4] The corpus was released as a database containing multiple tables which, taken together, describe the words and grammar contained in “over 70 deeply annotated Old and Middle Irish texts”.[^4] CSV files containing the data can be freely downloaded from their website, and SQL containing the data is available on their Github which indicates that the data is MIT licensed, a permissive license.

[^4]: https://chronhib.maynoothuniversity.ie/chronhibWebsite/home

### Statistics
There are 10,504 lemmata in the dataset, of which the 8,073 we are concerned with have the “Lang” tag “Early Irish or British”, “Irish and Pictish", or “Early Irish”. Of these 8,073 lemmata, there are 108,323 attested morphologies or inflections of the relevant lemmata in the dataset.

### Part-of-Speech Breakdown*
| Part-of-Speech | Attestations |
| -- | -- |
| Nouns | 3125 |
| Adjectives | 1281 |
| Proper Nouns | 1117 |
| Verbs | 1109 |
| Verbal Nouns | 681 |
| Participles | 264 |
| Adverbs | 99 |
| Gerunds | 95 |
| Conjunctions | 38 |
| Prepositions | 38 |

*any part-of-speech with less than 38 attestations is not shown

### Data Quality

| Data | Quality |
| -- | -- |
| Alternative Forms | ✓✓ |
| Conjugations/Declensions | ✓✓ |
| Definitions | ✓ |
| Examples | ✓✓ |
| Gender | ✓✓ |
| Part-of-Speech | ✓✓ |
| Stem | ✓✓ |
| Verb Class | ✓✓ |


As indicated above, the information in CorPH is extremely detailed, and every headword has its requisite grammatical information. Beyond the lemmata alone, the morphed lemmata are brimming with information as well; e.g., whether an initial mutation is present (and whether that mutation is shown), whether it causes an initial mutation (and whether that mutation is shown), an “expected form”, a “stress unit”, the sentence it is from, the grammatical cause of the inflection, et cetera. As every morphed lemma in the CorPH database is associated with a sentence, and a translation thereof, this means that a front-end which takes advantage of this information could present the user with any number of example sentences, even of a specific grammatical inflection, to be perused. The definitions seem to be taken from eDIL, mainly, and are very narrow. As most sources of Old Irish are glosses, the corpus does lean heavily toward certain words over others, but these are the only “pure” sources of Old Irish that exist, therefore their contents are a moot point. 


## Early Irish Glossaries Database (EIGD) (2009)
*Copyright Status*: MIT Licensed[^5]

[^5]: https://github.com/padraicmoran/irishglossaries

### Description
Originally released in 2009 as the result of a three-year project,[^6] EIGD contains concordances and transcriptions of a few of the major glossaries. The more closely related texts contain headwords only of the less-preferred versions, while the preferred versions have full TEI-XML transcriptions of their contents.

[^6]: https://www.asnc.cam.ac.uk/irishglossaries/database.php

### Statistics
There are 9,828 glosses which shrink to 2,361 headwords total.

### Data Quality
The glosses are an extremely quality data source which, beyond assisting with grammar and vocabulary, allow a scholar to find deeper connections between the texts and their worlds. Sadly, about 3,891 of the entries are not transcribed due to the priorities of the project; however, their headwords are all present which at the least allows for full orthographical comparisons of the headwords, if not fully-transcribed entries.


## Onomasticon Goedelicum (OG) (1910)
*Copyright Status*: Unknown

### Description
A monumental project undertaken by Edmund Hogan at the beginning of the 20th century, OG is a compilation of all of the place-name and tribe-name information that Hogan and his assistants could find as he was compiling the book. The book was digitized[^7] starting in 1998 as a first step of the LOCUS project at UCC in their continuing journey towards superseding OG as the best source for onomastical data.

[^7]:  https://research.ucc.ie/doi/locus

### Statistics
There are 25,312 entries, of which most are unique to OG.

### Data Quality
OG contains invaluable placename information which is not contained elsewhere, aside from the far superior information contained in the Historical Dictionary of Gaelic Placenames fascicles. However, this data is exceedingly opaque, and sufferers from an inordinate amount of abbreviations. Aside from the placename and entry data, there are usually references and even example sentences in some entries. There is the possibility of extracting further information from these entries, but it is unclear if there would be a lot of benefit from testing that possibility.
