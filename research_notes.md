# Testing Pipelines

baseline
```
pipe1 = Pipeline([('count_vec',CountVectorizer()),
                  ('bayes',MultinomialNB())])
```
adding TfidfTransformer
```
pipe2 = Pipeline([('count_vec',CountVectorizer()),
                  ('tfidf',TfidfTransformer()),
                  ('bayes',MultinomialNB())])
```
pipe | score
---|--
pipe1 | 0.2690043700310641
pipe1 with stop | 0.26970989311851734
pipe2 with stop | 0.24183646606644554
pipe1 with mystop | 0.27033117464328965
logreg | 0.2693729268677934

|precision |   recall | f1-score   
---|---|---|---|---
pipe1|0.25   |   0.27   |   0.21    
pipe1 with stop|0.27 | 0.27 |  0.21
pipe1 with mystop | 0.26 | 0.27 | 0.22
logreg |  0.26   |   0.27   |   0.24
---
