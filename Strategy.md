# strategy

## Preprocessing
- EDA
- split posts by `|||`
- create features
- create own stopwords

## Process data
- tfidfvectorizer()
- - base parameters (further tuning with GridSearchCV)
- train, test split

## Model Selection
- create baseline multinomialNB
- choose classifiers
- - list: multinomialNB, Logestic Regression, LinearSVC, DecisionTree, KNN, SGDClassifier
- fit models and score
- - check cross_val_score possible
- Select best 2 or 3 (depending on closeness of score)

## Hyperparameter Tuning
- GridSearchCV
- _define params to tune_

__tfidfvectorizer__
- `ngram_range`[(1,1), (1,2)]
- `stop_words` ['english','my_own']
- `max_df`
- `min_df`
- `norm` ['l1','l2',None]
- `use_idf` [True,False]
- `sublinear_tf` [True,False]
