# NLPAssignment01
>>> import nltk
>>> from nltk.corpus import brown
>>> nps = nltk.ConditionalFreqDist(
...           (genre, word)
...           for genre in brown.categories()
...           for word in brown.words(categories=genre))
>>> genres = ['news', 'religion', 'hobbies', 'science_fiction', 'romance', 'humor']
>>> modals = ['can', 'could', 'may', 'might', 'must', 'will']
>>> nps.tabulate(conditions=genres, samples=modals)
