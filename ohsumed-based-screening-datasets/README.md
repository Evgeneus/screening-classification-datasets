# ohsumed-based screening datasets
This repository contains datasets for 2-predicate document screening that built upon OHSUMED test collection.
There are 3 datasets which correspond to the following queries:
1) "Find all papers that study Cardiovascular Diseases and describe Pathological Conditions, Signs, and Symptoms". -> two predicates (C14) and (C23).
2) "Find all papers that study Nervous System Diseases and describe Pathological Conditions, Signs, and Symptoms". -> two predicates (C10) and (C23).
3) "Find all papers that study Neoplasms and Urologic and Male Genital Diseases". -> two predicates (C04) and (C12).

The datasets are highly imbalanced. For the (C14)+(C23) dataset, 1750 positives (5%); for the (C10)+(C23) dataset, 1200 positives (3.5%); for the (C04)+(C12) dataset, 547 positives (1.6%) .
- The total number of documents: 34389
- Selectivity* of (C10): 0.11
- Selectivity of (C14): 0.18
- Selectivity of (C04): 0.18
- Selectivity of (C12): 0.07
- Selectivity of (C23): 0.28

*Selectivity is the proportion of documents to which a category(predicate) applies.


Repository structure:
-  data-original/ - original dataset
- data-processed/ - transformed the shape of the original dataset, 1/2-grams for the 2 predicate screening datasets
- data-preprocessing.ipynb - preprocessing original data, cleaning data, and creating N-grams
- data-exploration.ipynb - exploration of dataset properties

-----------------------------------------------------
"Ohsumed collection: it includes medical abstracts from the MeSH categories of 
the year 1991. In [Joachims, 1997]. As current computers can easily manage larger number of 
documents we make available all 34,389 cardiovascular diseases abstracts 
out of 50,216 medical abstracts contained in the year 1991." source: http://disi.unitn.it/moschitti/corpora.htm

The abstracts belong to a subset of the following 23 disease categories:
<pre>
Bacterial Infections and Mycoses                      C01
Virus Diseases                                        C02
Parasitic Diseases                                    C03
Neoplasms                                             C04
Musculoskeletal Diseases                              C05
Digestive System Diseases                             C06
Stomatognathic Diseases                               C07
Respiratory Tract Diseases                            C08
Otorhinolaryngologic Diseases                         C09
Nervous System Diseases                               C10
Eye Diseases                                          C11
Urologic and Male Genital Diseases                    C12
Female Genital Diseases and Pregnancy Complications   C13
Cardiovascular Diseases                               C14
Hemic and Lymphatic Diseases                          C15
Neonatal Diseases and Abnormalities                   C16
Skin and Connective Tissue Diseases                   C17
Nutritional and Metabolic Diseases                    C18
Endocrine Diseases                                    C19
Immunologic Diseases                                  C20
Disorders of Environmental Origin                     C21
Animal Diseases                                       C22
Pathological Conditions, Signs and Symptoms           C23
</pre>
