# NLP-final

This project was done for Natural Language Processing (CS 536) with Professor Casey Kennington, Spring 2023.

## Goal

The goal of this project is to explore what language features, if any, affect whether a typical 7-11 year-old searcher will click on a search engine result or not.

## Language Features Utilized in Project
| idx | Linguistic Branch   | Subgroup Code | Subgroup Definition                  | Feature Code | Feature Definition                                                             |
|-------|---------------------|---------------|--------------------------------------|--------------|--------------------------------------------------------------------------------|                                        |
| 77    | Synta           | PhrF_         | Phrasal Features                     | to_NoPhr_C   | total count of Noun phrases                                                    |
| 78    | Synta           | PhrF_         | Phrasal Features                     | as_NoPhr_C   | average count of Noun phrases per sentence                                     |
| 79    | Synta           | PhrF_         | Phrasal Features                     | at_NoPhr_C   | average count of Noun phrases per token                                        |
| 80    | Synta           | PhrF_         | Phrasal Features                     | ra_NoVeP_C   | ratio of Noun phrases count to Verb phrases count                              |
| 81    | Synta           | PhrF_         | Phrasal Features                     | ra_NoSuP_C   | ratio of Noun phrases count to Subordinate Clauses count                       |
| 82    | Synta           | PhrF_         | Phrasal Features                     | ra_NoPrP_C   | ratio of Noun phrases count to Prep phrases count                              |
| 83    | Synta           | PhrF_         | Phrasal Features                     | ra_NoAjP_C   | ratio of Noun phrases count to Adj phrases count                               |
| 84    | Synta           | PhrF_         | Phrasal Features                     | ra_NoAvP_C   | ratio of Noun phrases count to Adv phrases count                               |
| 85    | Synta           | PhrF_         | Phrasal Features                     | to_VePhr_C   | total count of Verb phrases                                                    |
| 86    | Synta           | PhrF_         | Phrasal Features                     | as_VePhr_C   | average count of Verb phrases per sentence                                     |
| 87    | Synta           | PhrF_         | Phrasal Features                     | at_VePhr_C   | average count of Verb phrases per token                                        |
| 88    | Synta           | PhrF_         | Phrasal Features                     | ra_VeNoP_C   | ratio of Verb phrases count to Noun phrases count                              |
| 89    | Synta           | PhrF_         | Phrasal Features                     | ra_VeSuP_C   | ratio of Verb phrases count to Subordinate Clauses count                       |
| 90    | Synta           | PhrF_         | Phrasal Features                     | ra_VePrP_C   | ratio of Verb phrases count to Prep phrases count                              |
| 91    | Synta           | PhrF_         | Phrasal Features                     | ra_VeAjP_C   | ratio of Verb phrases count to Adj phrases count                               |
| 92    | Synta           | PhrF_         | Phrasal Features                     | ra_VeAvP_C   | ratio of Verb phrases count to Adv phrases count                               |
| 93    | Synta           | PhrF_         | Phrasal Features                     | to_SuPhr_C   | total count of Subordinate Clauses                                             |
| 94    | Synta           | PhrF_         | Phrasal Features                     | as_SuPhr_C   | average count of Subordinate Clauses per sentence                              |
| 95    | Synta           | PhrF_         | Phrasal Features                     | at_SuPhr_C   | average count of Subordinate Clauses per token                                 |
| 96    | Synta           | PhrF_         | Phrasal Features                     | ra_SuNoP_C   | ratio of Subordinate Clauses count to Noun phrases count                       |
| 97    | Synta           | PhrF_         | Phrasal Features                     | ra_SuVeP_C   | ratio of Subordinate Clauses count to Verb phrases count                       |
| 98    | Synta           | PhrF_         | Phrasal Features                     | ra_SuPrP_C   | ratio of Subordinate Clauses count to Prep phrases count                       |
| 99    | Synta           | PhrF_         | Phrasal Features                     | ra_SuAjP_C   | ratio of Subordinate Clauses count to Adj phrases count                        |
| 100   | Synta           | PhrF_         | Phrasal Features                     | ra_SuAvP_C   | ratio of Subordinate Clauses count to Adv phrases count                        |
| 101   | Synta           | PhrF_         | Phrasal Features                     | to_PrPhr_C   | total count of prepositional phrases                                           |
| 102   | Synta           | PhrF_         | Phrasal Features                     | as_PrPhr_C   | average count of prepositional phrases per sentence                            |
| 103   | Synta           | PhrF_         | Phrasal Features                     | at_PrPhr_C   | average count of prepositional phrases per token                               |
| 104   | Synta           | PhrF_         | Phrasal Features                     | ra_PrNoP_C   | ratio of Prep phrases count to Noun phrases count                              |
| 105   | Synta           | PhrF_         | Phrasal Features                     | ra_PrVeP_C   | ratio of Prep phrases count to Verb phrases count                              |
| 106   | Synta           | PhrF_         | Phrasal Features                     | ra_PrSuP_C   | ratio of Prep phrases count to Subordinate Clauses count                       |
| 107   | Synta           | PhrF_         | Phrasal Features                     | ra_PrAjP_C   | ratio of Prep phrases count to Adj phrases count                               |
| 108   | Synta           | PhrF_         | Phrasal Features                     | ra_PrAvP_C   | ratio of Prep phrases count to Adv phrases count                               |
| 109   | Synta           | PhrF_         | Phrasal Features                     | to_AjPhr_C   | total count of Adjective phrases                                               |
| 110   | Synta           | PhrF_         | Phrasal Features                     | as_AjPhr_C   | average count of Adjective phrases per sentence                                |
| 111   | Synta           | PhrF_         | Phrasal Features                     | at_AjPhr_C   | average count of Adjective phrases per token                                   |
| 112   | Synta           | PhrF_         | Phrasal Features                     | ra_AjNoP_C   | ratio of Adj phrases count to Noun phrases count                               |
| 113   | Synta           | PhrF_         | Phrasal Features                     | ra_AjVeP_C   | ratio of Adj phrases count to Verb phrases count                               |
| 114   | Synta           | PhrF_         | Phrasal Features                     | ra_AjSuP_C   | ratio of Adj phrases count to Subordinate Clauses count                        |
| 115   | Synta           | PhrF_         | Phrasal Features                     | ra_AjPrP_C   | ratio of Adj phrases count to Prep phrases count                               |
| 116   | Synta           | PhrF_         | Phrasal Features                     | ra_AjAvP_C   | ratio of Adj phrases count to Adv phrases count                                |
| 117   | Synta           | PhrF_         | Phrasal Features                     | to_AvPhr_C   | total count of Adverb phrases                                                  |
| 118   | Synta           | PhrF_         | Phrasal Features                     | as_AvPhr_C   | average count of Adverb phrases per sentence                                   |
| 119   | Synta           | PhrF_         | Phrasal Features                     | at_AvPhr_C   | average count of Adverb phrases per token                                      |
| 120   | Synta           | PhrF_         | Phrasal Features                     | ra_AvNoP_C   | ratio of Adv phrases count to Noun phrases count                               |
| 121   | Synta           | PhrF_         | Phrasal Features                     | ra_AvVeP_C   | ratio of Adv phrases count to Verb phrases count                               |
| 122   | Synta           | PhrF_         | Phrasal Features                     | ra_AvSuP_C   | ratio of Adv phrases count to Subordinate Clauses count                        |
| 123   | Synta           | PhrF_         | Phrasal Features                     | ra_AvPrP_C   | ratio of Adv phrases count to Prep phrases count                               |
| 124   | Synta           | PhrF_         | Phrasal Features                     | ra_AvAjP_C   | ratio of Adv phrases count to Adj phrases count                                |
| 125   | Synta           | TrSF_         | Tree Structure Features              | to_TreeH_C   | total Tree height of all sentences                                             |
| 126   | Synta           | TrSF_         | Tree Structure Features              | as_TreeH_C   | average Tree height per sentence                                               |
| 127   | Synta           | TrSF_         | Tree Structure Features              | at_TreeH_C   | average Tree height per token (word)                                           |
| 128   | Synta           | TrSF_         | Tree Structure Features              | to_FTree_C   | total length of flattened Trees                                                |
| 129   | Synta           | TrSF_         | Tree Structure Features              | as_FTree_C   | average length of flattened Trees per sentence                                 |
| 130   | Synta           | TrSF_         | Tree Structure Features              | at_FTree_C   | average length of flattened Trees per token (word)                             |
| 131   | Synta           | POSF_         | Part-of-Speech Features              | to_NoTag_C   | total count of Noun POS tags                                                   |
| 132   | Synta           | POSF_         | Part-of-Speech Features              | as_NoTag_C   | average count of Noun POS tags per sentence                                    |
| 133   | Synta           | POSF_         | Part-of-Speech Features              | at_NoTag_C   | average count of Noun POS tags per token                                       |
| 134   | Synta           | POSF_         | Part-of-Speech Features              | ra_NoAjT_C   | ratio of Noun POS count to Adjective POS count                                 |
| 135   | Synta           | POSF_         | Part-of-Speech Features              | ra_NoVeT_C   | ratio of Noun POS count to Verb POS count                                      |
| 136   | Synta           | POSF_         | Part-of-Speech Features              | ra_NoAvT_C   | ratio of Noun POS count to Adverb POS count                                    |
| 137   | Synta           | POSF_         | Part-of-Speech Features              | ra_NoSuT_C   | ratio of Noun POS count to Subordinating Conjunction count                     |
| 138   | Synta           | POSF_         | Part-of-Speech Features              | ra_NoCoT_C   | ratio of Noun POS count to Coordinating Conjunction count                      |
| 139   | Synta           | POSF_         | Part-of-Speech Features              | to_VeTag_C   | total count of Verb POS tags                                                   |
| 140   | Synta           | POSF_         | Part-of-Speech Features              | as_VeTag_C   | average count of Verb POS tags per sentence                                    |
| 141   | Synta           | POSF_         | Part-of-Speech Features              | at_VeTag_C   | average count of Verb POS tags per token                                       |
| 142   | Synta           | POSF_         | Part-of-Speech Features              | ra_VeAjT_C   | ratio of Verb POS count to Adjective POS count                                 |
| 143   | Synta           | POSF_         | Part-of-Speech Features              | ra_VeNoT_C   | ratio of Verb POS count to Noun POS count                                      |
| 144   | Synta           | POSF_         | Part-of-Speech Features              | ra_VeAvT_C   | ratio of Verb POS count to Adverb POS count                                    |
| 145   | Synta           | POSF_         | Part-of-Speech Features              | ra_VeSuT_C   | ratio of Verb POS count to Subordinating Conjunction count                     |
| 146   | Synta           | POSF_         | Part-of-Speech Features              | ra_VeCoT_C   | ratio of Verb POS count to Coordinating Conjunction count                      |
| 147   | Synta           | POSF_         | Part-of-Speech Features              | to_AjTag_C   | total count of Adjective POS tags                                              |
| 148   | Synta           | POSF_         | Part-of-Speech Features              | as_AjTag_C   | average count of Adjective POS tags per sentence                               |
| 149   | Synta           | POSF_         | Part-of-Speech Features              | at_AjTag_C   | average count of Adjective POS tags per token                                  |
| 150   | Synta           | POSF_         | Part-of-Speech Features              | ra_AjNoT_C   | ratio of Adjective POS count to Noun POS count                                 |
| 151   | Synta           | POSF_         | Part-of-Speech Features              | ra_AjVeT_C   | ratio of Adjective POS count to Verb POS count                                 |
| 152   | Synta           | POSF_         | Part-of-Speech Features              | ra_AjAvT_C   | ratio of Adjective POS count to Adverb POS count                               |
| 153   | Synta           | POSF_         | Part-of-Speech Features              | ra_AjSuT_C   | ratio of Adjective POS count to Subordinating Conjunction count                |
| 154   | Synta           | POSF_         | Part-of-Speech Features              | ra_AjCoT_C   | ratio of Adjective POS count to Coordinating Conjunction count                 |
| 155   | Synta           | POSF_         | Part-of-Speech Features              | to_AvTag_C   | total count of Adverb POS tags                                                 |
| 156   | Synta           | POSF_         | Part-of-Speech Features              | as_AvTag_C   | average count of Adverb POS tags per sentence                                  |
| 157   | Synta           | POSF_         | Part-of-Speech Features              | at_AvTag_C   | average count of Adverb POS tags per token                                     |
| 158   | Synta           | POSF_         | Part-of-Speech Features              | ra_AvAjT_C   | ratio of Adverb POS count to Adjective POS count                               |
| 159   | Synta           | POSF_         | Part-of-Speech Features              | ra_AvNoT_C   | ratio of Adverb POS count to Noun POS count                                    |
| 160   | Synta           | POSF_         | Part-of-Speech Features              | ra_AvVeT_C   | ratio of Adverb POS count to Verb POS count                                    |
| 161   | Synta           | POSF_         | Part-of-Speech Features              | ra_AvSuT_C   | ratio of Adverb POS count to Subordinating Conjunction count                   |
| 162   | Synta           | POSF_         | Part-of-Speech Features              | ra_AvCoT_C   | ratio of Adverb POS count to Coordinating Conjunction count                    |
| 163   | Synta           | POSF_         | Part-of-Speech Features              | to_SuTag_C   | total count of Subordinating Conjunction POS tags                              |
| 164   | Synta           | POSF_         | Part-of-Speech Features              | as_SuTag_C   | average count of Subordinating Conjunction POS tags per sentence               |
| 165   | Synta           | POSF_         | Part-of-Speech Features              | at_SuTag_C   | average count of Subordinating Conjunction POS tags per token                  |
| 166   | Synta           | POSF_         | Part-of-Speech Features              | ra_SuAjT_C   | ratio of Subordinating Conjunction POS count to Adjective POS count            |
| 167   | Synta           | POSF_         | Part-of-Speech Features              | ra_SuNoT_C   | ratio of Subordinating Conjunction POS count to Noun POS count                 |
| 168   | Synta           | POSF_         | Part-of-Speech Features              | ra_SuVeT_C   | ratio of Subordinating Conjunction POS count to Verb POS count                 |
| 169   | Synta           | POSF_         | Part-of-Speech Features              | ra_SuAvT_C   | ratio of Subordinating Conjunction POS count to Adverb POS count               |
| 170   | Synta           | POSF_         | Part-of-Speech Features              | ra_SuCoT_C   | ratio of Subordinating Conjunction POS count to Coordinating Conjunction count |
| 171   | Synta           | POSF_         | Part-of-Speech Features              | to_CoTag_C   | total count of Coordinating Conjunction POS tags                               |
| 172   | Synta           | POSF_         | Part-of-Speech Features              | as_CoTag_C   | average count of Coordinating Conjunction POS tags per sentence                |
| 173   | Synta           | POSF_         | Part-of-Speech Features              | at_CoTag_C   | average count of Coordinating Conjunction POS tags per token                   |
| 174   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoAjT_C   | ratio of Coordinating Conjunction POS count to Adjective POS count             |
| 175   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoNoT_C   | ratio of Coordinating Conjunction POS count to Noun POS count                  |
| 176   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoVeT_C   | ratio of Coordinating Conjunction POS count to Verb POS count                  |
| 177   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoAvT_C   | ratio of Coordinating Conjunction POS count to Adverb POS count                |
| 178   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoSuT_C   | ratio of Coordinating Conjunction POS count to Subordinating Conjunction count |
| 179   | Synta           | POSF_         | Part-of-Speech Features              | to_ContW_C   | total count of Content words                                                   |
| 180   | Synta           | POSF_         | Part-of-Speech Features              | as_ContW_C   | average count of Content words per sentence                                    |
| 181   | Synta           | POSF_         | Part-of-Speech Features              | at_ContW_C   | average count of Content words per token                                       |
| 182   | Synta           | POSF_         | Part-of-Speech Features              | to_FuncW_C   | total count of Function words                                                  |
| 183   | Synta           | POSF_         | Part-of-Speech Features              | as_FuncW_C   | average count of Function words per sentence                                   |
| 184   | Synta           | POSF_         | Part-of-Speech Features              | at_FuncW_C   | average count of Function words per token                                      |
| 185   | Synta           | POSF_         | Part-of-Speech Features              | ra_CoFuW_C   | ratio of Content words to Function words                                       |
| 186   | LxSem     | VarF_         | Variation Ratio Features             | SimpNoV_S    | unique Nouns/total Nouns (Noun Variation-1)                                    |
| 187   | LxSem     | VarF_         | Variation Ratio Features             | SquaNoV_S    | (unique Nouns**2)/total Nouns (Squared Noun Variation-1)                       |
| 188   | LxSem     | VarF_         | Variation Ratio Features             | CorrNoV_S    | unique Nouns/sqrt(2*total Nouns) (Corrected Noun Variation-1)                  |
| 189   | LxSem     | VarF_         | Variation Ratio Features             | SimpVeV_S    | unique Verbs/total Verbs (Verb Variation-1)                                    |
| 190   | LxSem     | VarF_         | Variation Ratio Features             | SquaVeV_S    | (unique Verbs**2)/total Verbs (Squared Verb Variation-1)                       |
| 191   | LxSem     | VarF_         | Variation Ratio Features             | CorrVeV_S    | unique Verbs/sqrt(2*total Verbs) (Corrected Verb Variation-1)                  |
| 192   | LxSem     | VarF_         | Variation Ratio Features             | SimpAjV_S    | unique Adjectives/total Adjectives (Adjective Variation-1)                     |
| 193   | LxSem     | VarF_         | Variation Ratio Features             | SquaAjV_S    | (unique Adjectives**2)/total Adjectives (Squared Adjective Variation-1)        |
| 194   | LxSem     | VarF_         | Variation Ratio Features             | CorrAjV_S    | unique Adjectives/sqrt(2*total Adjectives) (Corrected Adjective Variation-1)   |
| 195   | LxSem     | VarF_         | Variation Ratio Features             | SimpAvV_S    | unique Adverbs/total Adverbs (AdVerb Variation-1)                              |
| 196   | LxSem     | VarF_         | Variation Ratio Features             | SquaAvV_S    | (unique Adverbs**2)/total Adverbs (Squared AdVerb Variation-1)                 |
| 197   | LxSem     | VarF_         | Variation Ratio Features             | CorrAvV_S    | unique Adverbs/sqrt(2*total Adverbs) (Corrected AdVerb Variation-1)            |
| 198   | LxSem     | TTRF_         | Type Token Ratio Features            | SimpTTR_S    | unique tokens/total tokens (TTR)                                               |
| 199   | LxSem     | TTRF_         | Type Token Ratio Features            | CorrTTR_S    | unique tokens/sqrt(2*total tokens) (Corrected TTR)                             |
| 200   | LxSem     | TTRF_         | Type Token Ratio Features            | BiLoTTR_S    | log(unique tokens)/log(total tokens) (Bi-Logarithmic TTR)                      |
| 201   | LxSem     | TTRF_         | Type Token Ratio Features            | UberTTR_S    | (log(unique tokens))^2/log(total tokens/unique tokens) (Uber Index)            |
| 202   | LxSem     | TTRF_         | Type Token Ratio Features            | MTLDTTR_S    | Measure of Textual Lexical Diversity (default TTR = 0.72)                      |
| 203   | LxSem     | PsyF_         | Psycholinguistic Features            | to_AAKuW_C   | total AoA (Age of Acquisition) of words                                        |
| 204   | LxSem     | PsyF_         | Psycholinguistic Features            | as_AAKuW_C   | average AoA of words per sentence                                              |
| 205   | LxSem     | PsyF_         | Psycholinguistic Features            | at_AAKuW_C   | average AoA of words per token                                                 |
| 206   | LxSem     | PsyF_         | Psycholinguistic Features            | to_AAKuL_C   | total lemmas AoA of lemmas                                                     |
| 207   | LxSem     | PsyF_         | Psycholinguistic Features            | as_AAKuL_C   | average lemmas AoA of lemmas per sentence                                      |
| 208   | LxSem     | PsyF_         | Psycholinguistic Features            | at_AAKuL_C   | average lemmas AoA of lemmas per token                                         |
| 209   | LxSem     | PsyF_         | Psycholinguistic Features            | to_AABiL_C   | total lemmas AoA of lemmas, Bird norm                                          |
| 210   | LxSem     | PsyF_         | Psycholinguistic Features            | as_AABiL_C   | average lemmas AoA of lemmas, Bird norm per sentence                           |
| 211   | LxSem     | PsyF_         | Psycholinguistic Features            | at_AABiL_C   | average lemmas AoA of lemmas, Bird norm per token                              |
| 212   | LxSem     | PsyF_         | Psycholinguistic Features            | to_AABrL_C   | total lemmas AoA of lemmas, Bristol norm                                       |
| 213   | LxSem     | PsyF_         | Psycholinguistic Features            | as_AABrL_C   | average lemmas AoA of lemmas, Bristol norm per sentence                        |
| 214   | LxSem     | PsyF_         | Psycholinguistic Features            | at_AABrL_C   | average lemmas AoA of lemmas, Bristol norm per token                           |
| 215   | LxSem     | PsyF_         | Psycholinguistic Features            | to_AACoL_C   | total AoA of lemmas, Cortese and Khanna norm                                   |
| 216   | LxSem     | PsyF_         | Psycholinguistic Features            | as_AACoL_C   | average AoA of lemmas, Cortese and Khanna norm per sentence                    |
| 217   | LxSem     | PsyF_         | Psycholinguistic Features            | at_AACoL_C   | average AoA of lemmas, Cortese and Khanna norm per token                       |                         
| 242   | ShaTr     | ShaF_         | Shallow Features                     | TokSenM_S   | total count of tokens x total count of sentence                                |
| 243   | ShaTr     | ShaF_         | Shallow Features                     | TokSenS_S   | sqrt(total count of tokens x total count of sentence)                                |
| 244   | ShaTr     | ShaF_         | Shallow Features                     | TokSenL_S   | log(total count of tokens)/log(total count of sentence)                           |
| 245   | ShaTr     | ShaF_         | Shallow Features                     | as_Token_C   | average count of tokens per sentence                                           |
| 246   | ShaTr     | ShaF_         | Shallow Features                     | as_Sylla_C   | average count of syllables per sentence                                        |
| 247   | ShaTr     | ShaF_         | Shallow Features                     | at_Sylla_C         | average count of syllables per token                                           |
| 248   | ShaTr     | ShaF_         | Shallow Features                     | as_Chara_C   | average count of characters per sentence                                       |
| 249   | ShaTr     | ShaF_         | Shallow Features                     | at_Chara_C   | average count of characters per token                                          |
| 250   | ShaTr     | TraF_         | Traditional Formulas         | SmogInd_S    | Smog Index                                                                     |
| 251   | ShaTr     | TraF_         | Traditional Formulas         | ColeLia_S    | Coleman Liau Readability Score                                                 |
| 252   | ShaTr     | TraF_         | Traditional Formulas         | Gunning_S    | Gunning Fog Count Score                                                                    |
| 253   | ShaTr     | TraF_         | Traditional Formulas         | AutoRea_S    | New Automated Readability Index                                                    |
| 254   | ShaTr     | TraF_         | Traditional Formulas         | FleschG_S    | Flesch Kincaid Grade Level                                                           |
| 255   | ShaTr     | TraF_         | Traditional Formulas         | LinseaW_S    | Linsear Write Formula Score                                                                  |
