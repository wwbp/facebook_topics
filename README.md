# Facebook Topics

A set of 2000 topics captured in over 14 million Facebook status updates derived via Latent Dirichlet Allocation (LDA).

## Data

* Top 20 words per topic
* All words
* Conditional probabilities (sparse matrix format)

## Example

The goal is to get the probability of a topic given the document: 

```
p(topic|document)=p(topic|tok)xp(tok|document)
```

For example, let's say we have topics with the following condition probabilities for words: 

```
topic 1: a: 0.01, b: 0.02, c: 0.001
topic 2: c: 0.02, d: 0.005
```

and two documents with the following frequencies of words: 

```
document 1: a: 2, b: 10, c: 3, d: 0, e: 6, f: 4
document 2: a: 5, b: 3, c: 8, d: 4, e: 0, f: 10
```

therefore the total word use in the documents are: 

```
document 1: 2 + 10 + 3 + 0 + 6 + 4 = 25
document 2: 5 + 3 + 8 + 4 + 0 + 10 = 30
```

document 1's use of topics is given by summing the weighted relative frequencies: 

```
p(topic1|document1): (2/25)*0.01 + (10/25)*0.02 + (3/25)*0.001 = 0.00892
p(topic2|document1): (3/25)*0.02 + (0/25)*0.005 = 0.0024
```

while document 2's use of topics: 

```
p(topic1|document2): (5/30)*0.01 + (3/30)*0.02 + (8/30)*0.001 = .00393
p(topic2|document2): (8/30)*0.02 + (4/30)*0.005 = 0.006
```

## Citation

Read the full publication [here](http://wwbp.org/publications.html#p7). 


```
@article{schwartz2013personality,
  title={Personality, gender, and age in the language of social media: The open-vocabulary approach},
  author={Schwartz, H Andrew and Eichstaedt, Johannes C and Kern, Margaret L and Dziurzynski, Lukasz and Ramones, Stephanie M and Agrawal, Megha and Shah, Achal and Kosinski, Michal and Stillwell, David and Seligman, Martin EP and others},
  journal={PloS one},
  volume={8},
  number={9},
  pages={e73791},
  year={2013},
  publisher={Public Library of Science}
}
```

## License

Licensed under a GNU General Public License v3 (GPLv3).

## Background

Developed by the [World Well-Being Project](https://www.wwbp.org) based out of the University of Pennsylvania and Stony Brook University.
