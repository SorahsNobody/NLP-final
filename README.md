# NLP-final

This project is for Natural Language Processing (CS 536) with Doctor Casey Kennington, Spring 2023

# Authors

- Benjamin Bettencourt
- Assoumer Redempta Manzi Muneza

## Goal

The goal of this project is to see if there are any language features, from search engine result titles and snippets, that affect whether or not a child searcher will click on a result or not.

## Environment set up

Anaconda3 and Google Collab were both utilized for this project.

You can clone one of the environments used for this project by using:

```
conda create --name <name of your new env> --file nlp_final.txt
```

**OR** you can install the packages listed in "nlp_final.txt" to an existing environment using:

```
conda install --name <name of your env> --file nlp_final.txt
```
**OR** you can install of the needed packages as you progress through the notebooks. If you do this method you'll need the following packages:

- textstat
- langdetect
- spellchecker
- pyspellchecker
- pytorch (with LAPACK if using cpu)
- csv
- pickle
- string
- pandas
- numpy
- tqdm
- json
- nltk
- os
- re
- shlex
- subprocess
- time
- sklearn
- lingfeat

**NOTE**: to get lingfeat to work, you should clone their repo (https://github.com/brucewlee/lingfeat) and move the lingfeat folder up one level.

lingfeat repo structure:
```
-lingfeat <- rename this folder so your environment doesn't confuse the two folders
--img
--lingfeat <- this folder needs to move up one level to work
--.DS_Store
--...
```

Then you can call the lingfeat functions as seen in the included notebooks.

## Implementation

1. With the CAST data dump, run the predict.ipynb notebook to create and output the "full_results_data.csv"
2. Run through the featuresBEN.ipynb notebook to create and output "features.csv", "title_features.csv", and "snippet_features.csv"
3. Run through the DataExtraction.ipynb notebook to create and output the feature files
4. Finally, run through the Classification.ipynb notebook to train, test, and evaluate the models.

**Optional**: You can run through the DataExploration.ipynb if you want to see some preliminary exploration.

## Features Utilized, Subgroup Code, Definition
### Features were extracted using lingfeat: https://github.com/brucewlee/lingfeat
### A huge thank you to Bruce W. Lee and all of the authors of lingfeat for their incredible work

| Linguistic Branch   | Subgroup Code | Subgroup Definition                  | Feature Code | Feature Definition                                                             |
|---------------------|---------------|--------------------------------------|--------------|--------------------------------------------------------------------------------|
| Synta           | PhrF_         | Phrasal Features                     | to_NoPhr_C   | total count of Noun phrases                                                    |
| Synta           | PhrF_         | Phrasal Features                     | as_NoPhr_C   | average count of Noun phrases per sentence                                     |
| Synta           | PhrF_         | Phrasal Features                     | at_NoPhr_C   | average count of Noun phrases per token                                        |
| Synta           | PhrF_         | Phrasal Features                     | ra_NoVeP_C   | ratio of Noun phrases count to Verb phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_NoSuP_C   | ratio of Noun phrases count to Subordinate Clauses count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_NoPrP_C   | ratio of Noun phrases count to Prep phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_NoAjP_C   | ratio of Noun phrases count to Adj phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_NoAvP_C   | ratio of Noun phrases count to Adv phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | to_VePhr_C   | total count of Verb phrases                                                    |
| Synta           | PhrF_         | Phrasal Features                     | as_VePhr_C   | average count of Verb phrases per sentence                                     |
| Synta           | PhrF_         | Phrasal Features                     | at_VePhr_C   | average count of Verb phrases per token                                        |
| Synta           | PhrF_         | Phrasal Features                     | ra_VeNoP_C   | ratio of Verb phrases count to Noun phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_VeSuP_C   | ratio of Verb phrases count to Subordinate Clauses count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_VePrP_C   | ratio of Verb phrases count to Prep phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_VeAjP_C   | ratio of Verb phrases count to Adj phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_VeAvP_C   | ratio of Verb phrases count to Adv phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | to_SuPhr_C   | total count of Subordinate Clauses                                             |
| Synta           | PhrF_         | Phrasal Features                     | as_SuPhr_C   | average count of Subordinate Clauses per sentence                              |
| Synta           | PhrF_         | Phrasal Features                     | at_SuPhr_C   | average count of Subordinate Clauses per token                                 |
| Synta           | PhrF_         | Phrasal Features                     | ra_SuNoP_C   | ratio of Subordinate Clauses count to Noun phrases count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_SuVeP_C   | ratio of Subordinate Clauses count to Verb phrases count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_SuPrP_C   | ratio of Subordinate Clauses count to Prep phrases count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_SuAjP_C   | ratio of Subordinate Clauses count to Adj phrases count                        |
| Synta           | PhrF_         | Phrasal Features                     | ra_SuAvP_C   | ratio of Subordinate Clauses count to Adv phrases count                        |
| Synta           | PhrF_         | Phrasal Features                     | to_PrPhr_C   | total count of prepositional phrases                                           |
| Synta           | PhrF_         | Phrasal Features                     | as_PrPhr_C   | average count of prepositional phrases per sentence                            |
| Synta           | PhrF_         | Phrasal Features                     | at_PrPhr_C   | average count of prepositional phrases per token                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_PrNoP_C   | ratio of Prep phrases count to Noun phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_PrVeP_C   | ratio of Prep phrases count to Verb phrases count                              |
| Synta           | PhrF_         | Phrasal Features                     | ra_PrSuP_C   | ratio of Prep phrases count to Subordinate Clauses count                       |
| Synta           | PhrF_         | Phrasal Features                     | ra_PrAjP_C   | ratio of Prep phrases count to Adj phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_PrAvP_C   | ratio of Prep phrases count to Adv phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | to_AjPhr_C   | total count of Adjective phrases                                               |
| Synta           | PhrF_         | Phrasal Features                     | as_AjPhr_C   | average count of Adjective phrases per sentence                                |
| Synta           | PhrF_         | Phrasal Features                     | at_AjPhr_C   | average count of Adjective phrases per token                                   |
| Synta           | PhrF_         | Phrasal Features                     | ra_AjNoP_C   | ratio of Adj phrases count to Noun phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AjVeP_C   | ratio of Adj phrases count to Verb phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AjSuP_C   | ratio of Adj phrases count to Subordinate Clauses count                        |
| Synta           | PhrF_         | Phrasal Features                     | ra_AjPrP_C   | ratio of Adj phrases count to Prep phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AjAvP_C   | ratio of Adj phrases count to Adv phrases count                                |
| Synta           | PhrF_         | Phrasal Features                     | to_AvPhr_C   | total count of Adverb phrases                                                  |
| Synta           | PhrF_         | Phrasal Features                     | as_AvPhr_C   | average count of Adverb phrases per sentence                                   |
| Synta           | PhrF_         | Phrasal Features                     | at_AvPhr_C   | average count of Adverb phrases per token                                      |
| Synta           | PhrF_         | Phrasal Features                     | ra_AvNoP_C   | ratio of Adv phrases count to Noun phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AvVeP_C   | ratio of Adv phrases count to Verb phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AvSuP_C   | ratio of Adv phrases count to Subordinate Clauses count                        |
| Synta           | PhrF_         | Phrasal Features                     | ra_AvPrP_C   | ratio of Adv phrases count to Prep phrases count                               |
| Synta           | PhrF_         | Phrasal Features                     | ra_AvAjP_C   | ratio of Adv phrases count to Adj phrases count                                |
| Synta           | TrSF_         | Tree Structure Features              | to_TreeH_C   | total Tree height of all sentences                                             |
| Synta           | TrSF_         | Tree Structure Features              | as_TreeH_C   | average Tree height per sentence                                               |
| Synta           | TrSF_         | Tree Structure Features              | at_TreeH_C   | average Tree height per token (word)                                           |
| Synta           | TrSF_         | Tree Structure Features              | to_FTree_C   | total length of flattened Trees                                                |
| Synta           | TrSF_         | Tree Structure Features              | as_FTree_C   | average length of flattened Trees per sentence                                 |
| Synta           | TrSF_         | Tree Structure Features              | at_FTree_C   | average length of flattened Trees per token (word)                             |
| Synta           | POSF_         | Part-of-Speech Features              | to_NoTag_C   | total count of Noun POS tags                                                   |
| Synta           | POSF_         | Part-of-Speech Features              | as_NoTag_C   | average count of Noun POS tags per sentence                                    |
| Synta           | POSF_         | Part-of-Speech Features              | at_NoTag_C   | average count of Noun POS tags per token                                       |
| Synta           | POSF_         | Part-of-Speech Features              | ra_NoAjT_C   | ratio of Noun POS count to Adjective POS count                                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_NoVeT_C   | ratio of Noun POS count to Verb POS count                                      |
| Synta           | POSF_         | Part-of-Speech Features              | ra_NoAvT_C   | ratio of Noun POS count to Adverb POS count                                    |
| Synta           | POSF_         | Part-of-Speech Features              | ra_NoSuT_C   | ratio of Noun POS count to Subordinating Conjunction count                     |
| Synta           | POSF_         | Part-of-Speech Features              | ra_NoCoT_C   | ratio of Noun POS count to Coordinating Conjunction count                      |
| Synta           | POSF_         | Part-of-Speech Features              | to_VeTag_C   | total count of Verb POS tags                                                   |
| Synta           | POSF_         | Part-of-Speech Features              | as_VeTag_C   | average count of Verb POS tags per sentence                                    |
| Synta           | POSF_         | Part-of-Speech Features              | at_VeTag_C   | average count of Verb POS tags per token                                       |
| Synta           | POSF_         | Part-of-Speech Features              | ra_VeAjT_C   | ratio of Verb POS count to Adjective POS count                                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_VeNoT_C   | ratio of Verb POS count to Noun POS count                                      |
| Synta           | POSF_         | Part-of-Speech Features              | ra_VeAvT_C   | ratio of Verb POS count to Adverb POS count                                    |
| Synta           | POSF_         | Part-of-Speech Features              | ra_VeSuT_C   | ratio of Verb POS count to Subordinating Conjunction count                     |
| Synta           | POSF_         | Part-of-Speech Features              | ra_VeCoT_C   | ratio of Verb POS count to Coordinating Conjunction count                      |
| Synta           | POSF_         | Part-of-Speech Features              | to_AjTag_C   | total count of Adjective POS tags                                              |
| Synta           | POSF_         | Part-of-Speech Features              | as_AjTag_C   | average count of Adjective POS tags per sentence                               |
| Synta           | POSF_         | Part-of-Speech Features              | at_AjTag_C   | average count of Adjective POS tags per token                                  |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AjNoT_C   | ratio of Adjective POS count to Noun POS count                                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AjVeT_C   | ratio of Adjective POS count to Verb POS count                                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AjAvT_C   | ratio of Adjective POS count to Adverb POS count                               |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AjSuT_C   | ratio of Adjective POS count to Subordinating Conjunction count                |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AjCoT_C   | ratio of Adjective POS count to Coordinating Conjunction count                 |
| Synta           | POSF_         | Part-of-Speech Features              | to_AvTag_C   | total count of Adverb POS tags                                                 |
| Synta           | POSF_         | Part-of-Speech Features              | as_AvTag_C   | average count of Adverb POS tags per sentence                                  |
| Synta           | POSF_         | Part-of-Speech Features              | at_AvTag_C   | average count of Adverb POS tags per token                                     |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AvAjT_C   | ratio of Adverb POS count to Adjective POS count                               |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AvNoT_C   | ratio of Adverb POS count to Noun POS count                                    |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AvVeT_C   | ratio of Adverb POS count to Verb POS count                                    |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AvSuT_C   | ratio of Adverb POS count to Subordinating Conjunction count                   |
| Synta           | POSF_         | Part-of-Speech Features              | ra_AvCoT_C   | ratio of Adverb POS count to Coordinating Conjunction count                    |
| Synta           | POSF_         | Part-of-Speech Features              | to_SuTag_C   | total count of Subordinating Conjunction POS tags                              |
| Synta           | POSF_         | Part-of-Speech Features              | as_SuTag_C   | average count of Subordinating Conjunction POS tags per sentence               |
| Synta           | POSF_         | Part-of-Speech Features              | at_SuTag_C   | average count of Subordinating Conjunction POS tags per token                  |
| Synta           | POSF_         | Part-of-Speech Features              | ra_SuAjT_C   | ratio of Subordinating Conjunction POS count to Adjective POS count            |
| Synta           | POSF_         | Part-of-Speech Features              | ra_SuNoT_C   | ratio of Subordinating Conjunction POS count to Noun POS count                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_SuVeT_C   | ratio of Subordinating Conjunction POS count to Verb POS count                 |
| Synta           | POSF_         | Part-of-Speech Features              | ra_SuAvT_C   | ratio of Subordinating Conjunction POS count to Adverb POS count               |
| Synta           | POSF_         | Part-of-Speech Features              | ra_SuCoT_C   | ratio of Subordinating Conjunction POS count to Coordinating Conjunction count |
| Synta           | POSF_         | Part-of-Speech Features              | to_CoTag_C   | total count of Coordinating Conjunction POS tags                               |
| Synta           | POSF_         | Part-of-Speech Features              | as_CoTag_C   | average count of Coordinating Conjunction POS tags per sentence                |
| Synta           | POSF_         | Part-of-Speech Features              | at_CoTag_C   | average count of Coordinating Conjunction POS tags per token                   |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoAjT_C   | ratio of Coordinating Conjunction POS count to Adjective POS count             |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoNoT_C   | ratio of Coordinating Conjunction POS count to Noun POS count                  |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoVeT_C   | ratio of Coordinating Conjunction POS count to Verb POS count                  |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoAvT_C   | ratio of Coordinating Conjunction POS count to Adverb POS count                |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoSuT_C   | ratio of Coordinating Conjunction POS count to Subordinating Conjunction count |
| Synta           | POSF_         | Part-of-Speech Features              | to_ContW_C   | total count of Content words                                                   |
| Synta           | POSF_         | Part-of-Speech Features              | as_ContW_C   | average count of Content words per sentence                                    |
| Synta           | POSF_         | Part-of-Speech Features              | at_ContW_C   | average count of Content words per token                                       |
| Synta           | POSF_         | Part-of-Speech Features              | to_FuncW_C   | total count of Function words                                                  |
| Synta           | POSF_         | Part-of-Speech Features              | as_FuncW_C   | average count of Function words per sentence                                   |
| Synta           | POSF_         | Part-of-Speech Features              | at_FuncW_C   | average count of Function words per token                                      |
| Synta           | POSF_         | Part-of-Speech Features              | ra_CoFuW_C   | ratio of Content words to Function words                                       |
| LxSem     | VarF_         | Variation Ratio Features             | SimpNoV_S    | unique Nouns/total Nouns (Noun Variation-1)                                    |
| LxSem     | VarF_         | Variation Ratio Features             | SquaNoV_S    | (unique Nouns**2)/total Nouns (Squared Noun Variation-1)                       |
| LxSem     | VarF_         | Variation Ratio Features             | CorrNoV_S    | unique Nouns/sqrt(2*total Nouns) (Corrected Noun Variation-1)                  |
| LxSem     | VarF_         | Variation Ratio Features             | SimpVeV_S    | unique Verbs/total Verbs (Verb Variation-1)                                    |
| LxSem     | VarF_         | Variation Ratio Features             | SquaVeV_S    | (unique Verbs**2)/total Verbs (Squared Verb Variation-1)                       |
| LxSem     | VarF_         | Variation Ratio Features             | CorrVeV_S    | unique Verbs/sqrt(2*total Verbs) (Corrected Verb Variation-1)                  |
| LxSem     | VarF_         | Variation Ratio Features             | SimpAjV_S    | unique Adjectives/total Adjectives (Adjective Variation-1)                     |
| LxSem     | VarF_         | Variation Ratio Features             | SquaAjV_S    | (unique Adjectives**2)/total Adjectives (Squared Adjective Variation-1)        |
| LxSem     | VarF_         | Variation Ratio Features             | CorrAjV_S    | unique Adjectives/sqrt(2*total Adjectives) (Corrected Adjective Variation-1)   |
| LxSem     | VarF_         | Variation Ratio Features             | SimpAvV_S    | unique Adverbs/total Adverbs (AdVerb Variation-1)                              |
| LxSem     | VarF_         | Variation Ratio Features             | SquaAvV_S    | (unique Adverbs**2)/total Adverbs (Squared AdVerb Variation-1)                 |
| LxSem     | VarF_         | Variation Ratio Features             | CorrAvV_S    | unique Adverbs/sqrt(2*total Adverbs) (Corrected AdVerb Variation-1)            |
| LxSem     | TTRF_         | Type Token Ratio Features            | SimpTTR_S    | unique tokens/total tokens (TTR)                                               |
| LxSem     | TTRF_         | Type Token Ratio Features            | CorrTTR_S    | unique tokens/sqrt(2*total tokens) (Corrected TTR)                             |
| LxSem     | TTRF_         | Type Token Ratio Features            | BiLoTTR_S    | log(unique tokens)/log(total tokens) (Bi-Logarithmic TTR)                      |
| LxSem     | TTRF_         | Type Token Ratio Features            | UberTTR_S    | (log(unique tokens))^2/log(total tokens/unique tokens) (Uber Index)            |
| LxSem     | TTRF_         | Type Token Ratio Features            | MTLDTTR_S    | Measure of Textual Lexical Diversity (default TTR = 0.72)                      |
| LxSem     | PsyF_         | Psycholinguistic Features            | to_AAKuW_C   | total AoA (Age of Acquisition) of words                                        |
| LxSem     | PsyF_         | Psycholinguistic Features            | as_AAKuW_C   | average AoA of words per sentence                                              |
| LxSem     | PsyF_         | Psycholinguistic Features            | at_AAKuW_C   | average AoA of words per token                                                 |
| LxSem     | PsyF_         | Psycholinguistic Features            | to_AAKuL_C   | total lemmas AoA of lemmas                                                     |
| LxSem     | PsyF_         | Psycholinguistic Features            | as_AAKuL_C   | average lemmas AoA of lemmas per sentence                                      |
| LxSem     | PsyF_         | Psycholinguistic Features            | at_AAKuL_C   | average lemmas AoA of lemmas per token                                         |
| LxSem     | PsyF_         | Psycholinguistic Features            | to_AABiL_C   | total lemmas AoA of lemmas, Bird norm                                          |
| LxSem     | PsyF_         | Psycholinguistic Features            | as_AABiL_C   | average lemmas AoA of lemmas, Bird norm per sentence                           |
| LxSem     | PsyF_         | Psycholinguistic Features            | at_AABiL_C   | average lemmas AoA of lemmas, Bird norm per token                              |
| LxSem     | PsyF_         | Psycholinguistic Features            | to_AABrL_C   | total lemmas AoA of lemmas, Bristol norm                                       |
| LxSem     | PsyF_         | Psycholinguistic Features            | as_AABrL_C   | average lemmas AoA of lemmas, Bristol norm per sentence                        |
| LxSem     | PsyF_         | Psycholinguistic Features            | at_AABrL_C   | average lemmas AoA of lemmas, Bristol norm per token                           |
| LxSem     | PsyF_         | Psycholinguistic Features            | to_AACoL_C   | total AoA of lemmas, Cortese and Khanna norm                                   |
| LxSem     | PsyF_         | Psycholinguistic Features            | as_AACoL_C   | average AoA of lemmas, Cortese and Khanna norm per sentence                    |
| LxSem     | PsyF_         | Psycholinguistic Features            | at_AACoL_C   | average AoA of lemmas, Cortese and Khanna norm per token                       |
| ShaTr     | ShaF_         | Shallow Features                     | TokSenM_S   | total count of tokens x total count of sentence                                |
| ShaTr     | ShaF_         | Shallow Features                     | TokSenS_S   | sqrt(total count of tokens x total count of sentence)                                |
| ShaTr     | ShaF_         | Shallow Features                     | TokSenL_S   | log(total count of tokens)/log(total count of sentence)                           |
| ShaTr     | ShaF_         | Shallow Features                     | as_Token_C   | average count of tokens per sentence                                           |
| ShaTr     | ShaF_         | Shallow Features                     | as_Sylla_C   | average count of syllables per sentence                                        |
| ShaTr     | ShaF_         | Shallow Features                     | at_Sylla_C         | average count of syllables per token                                           |
| ShaTr     | ShaF_         | Shallow Features                     | as_Chara_C   | average count of characters per sentence                                       |
| ShaTr     | ShaF_         | Shallow Features                     | at_Chara_C   | average count of characters per token                                          |
| ShaTr     | TraF_         | Traditional Formulas         | SmogInd_S    | Smog Index                                                                     |
| ShaTr     | TraF_         | Traditional Formulas         | ColeLia_S    | Coleman Liau Readability Score                                                 |
| ShaTr     | TraF_         | Traditional Formulas         | Gunning_S    | Gunning Fog Count Score                                                                    |
| ShaTr     | TraF_         | Traditional Formulas         | AutoRea_S    | New Automated Readability Index                                                    |
| ShaTr     | TraF_         | Traditional Formulas         | FleschG_S    | Flesch Kincaid Grade Level                                                           |
| ShaTr     | TraF_         | Traditional Formulas         | LinseaW_S    | Linsear Write Formula Score                                                                  |


## Key References (From the lingfeat readme)

**Variation Features**
> Lu, Xiaofei. "A corpus‐based evaluation of syntactic complexity measures as indices of college‐level ESL writers' language development." TESOL quarterly 45.1 (2011): 36-62.

**Psycholinguistic Features**
> Kuperman, Victor, Hans Stadthagen-Gonzalez, and Marc Brysbaert. "Age-of-acquisition ratings for 30,000 English words." Behavior research methods 44.4 (2012): 978-990.

**Traditional Formulas**
> Kincaid, J. Peter, Robert P. Fishburne Jr, Richard L. Rogers, and Brad S. Chissom. Derivation of new readability formulas (automated readability index, fog count and flesch reading ease formula) for navy enlisted personnel. Naval Technical Training Command Millington TN Research Branch, 1975.

