# Scientific context

Proteins are biological molecules made of amino acids that group into hundreds
of thousands of different families, involved in functions ranging from
structural to chemical roles. They often partner up to fulfill cellular
functions and assemble into macro-molecular systems. An example of such
macromolecular systems are secretion systems, systems used by the bacteria to
interact with their environment for nutrient acquisition, defense, toxin
delivery, …

Often, several subtypes (or variants) of a macro-molecular system exist, which
specialized into different functions along evolution. They can be made of very
similar protein families. Precisely detecting the number of types of
macromolecular systems and which protein families are involved in each subtype
is of crucial importance to properly assess the function of novel proteins in
genomes: a process called "functional annotation."

![NMF for SS](../../assets/img/NMF_for_SS.png)

Current methods to detect and annotate macro-molecular systems encoded by
genomes first, identify proteins of interest from sequence similarity of
proteins families involved in similar systems.  Then, they rely on
investigating a number of properties, such as co-occurrence patterns in large
databases of genomes, co-expression patterns, co-localization of the
corresponding genes on the genome, etc. Thus, such approaches require
substantial manual work to identify patterns of genomic organization specific
to each system and subsystems. 


We propose to **investigate and develop machine learning approaches to tackle
the challenge of functional annotation in an automated fashion**.


**Objectives** Develop statistical learning tools to answer the following
questions: Given a set of candidate proteins involved in a function / complex
for a large number of organisms, can we automatically detect the number of
subtypes of the macromolecular system (e.g., the number of types of secretion
systems) and which protein family is involved in each subtype?

Machine learning approaches are particularly powerful to extract and
generalize new insights from high-dimensional, complex, and noisy data. In
particular, **unsupervised learning approaches** such as non-negative
matrix factorization are used to automatically detect correlation patterns in
large datasets, and are a promising avenue to automatically solve this
problem.

# Methodology 

To achieve this goal, we propose the following roadmap.

- **Deconvolution approaches for detecting system subtypes** Given a matrix X
  where each row corresponds to an organism, each column to a protein family,
  and each entry to the number of times this protein family is found in an
  organism, can we factorize X into two non-negative matrices, one
  corresponding to which homologs are found in which macromolecular system
  subtype, the other corresponding to the number of times each macromolecular
  system is found in each organism? A challenge when using such non-supervised
  approaches is to tune the hyperparameter of the model (e.g., the number of
  subtypes). We propose to investigate two strategies. First, in this
  particular case, some macromolecular systems are well known and well
  studied. We propose to use this knowledge to supervise the learning of the
  hyperparameters. Second, to ensure such an approach can be applied on
  systems for which no partial knowledge is known, we will investigate whether
  stability analysis can be used instead.

- **Feature encoding and n-grams of proteins** Protein families involved in
  these macromolecular systems tend to be related. As such, a "one-hot
  encoding" of each proteins in these protein families may be naive. In
  addition, valuable information can be gathered from protein familiy
  co-localization along the genome. Taking inspiration from natural language
  processing, better feature encoding could leverage this valuable information
  (with dirty category encoding, and / or n-grams of proteins).

- **Facilitate reproducible and open science** by sharing the method in a high
  quality open-source package.


## Datasets

Several macromolecular systems can be annotated using a tool we develop called
MacSyFinder. We have downloaded and annotated roughly 30,000 complete genomes
of bacteria with the following macro-molecular systems:

- **Secretion systems** are crucial for bacterial organisms to interact with
  their environment, such as acquiring nutriments, setting up biotic defenses,
  as well as delivering virulence factors. There are currently 12 bacterial
  secretion systems known varying in size (1 to 15 proteins involved). 

- **Defense systems** used by bacterial organisms to defend themselves against
  viruses and mobile genetic elements.


# Scientific environment

The PhD candidate will be hosted in the TIMC lab, TrEE team
(https://tree-timc. github.io/compbio), co-advised by Nelle Varoquaux and
Sophie Abby. The TIMC lab (https://www-timc.imag.fr/en/) gathers scientists
and clini- cians towards the use of computer science and applied mathematics
for understand- ing and controlling normal and pathological processes in
biology and healthcare. Within the lab, the team TrEE is an interdisciplinary
team, gathering biochemists, biophysicists, molecular microbiologists,
biostatisticians and bioinformaticians, with a common strong interest in
microbial evolution.

The lab is located on the Campus of La Tronche, in close vicinity to Grenoble
city center(Tram B).

- The team website: http://www.timc.fr/en/tree

- The computational biology group website: https://tree-timc.github.io/
  compbio 

This PhD is funded by an ANR grant that aims to develop machine learning
approaches to detect novel secretion systems in collaboration with experts of
these systems.

# Profile

The profile sought is that of a graduate student (Master degree or equivalent)
in Computer Science (Major in Artificial Intelligence, Data Science, or
Bioinformatics) or Applied Mathematics (Major in Signal Processing or
Statistics) who has a strong interest in interdisciplinary work in biology.
They must have programming skills (R or Python) and be fluent in either French
or English.
