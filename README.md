# FoldHashing
This repo contains functions and classes used for hashing numbers / lists of numbers based on a basic folding method. The main function of interest is loadFactorOptimizer, which will create a hashtable for numbers in a list of numbers, with the goal of maximizing the loadFactor of our hashtable, with the loadFactor being equal to: (nonEmpty items in hashtable) / (total items in hashtable). We achieve this by returning the first hashtable for which all of our numbers in our num list are granted an entry in our hashtable.

Our .add() method in FoldHasher utilizes chain collision resolution. This means that add firs identifies the slot where we should insert item. If that slot is None, then we insert item there. If slot is int, then we create a new instance of FoldHasher, and insert it into that slot with parameters numList = [original entry, item]. If slot is a FoldHasher, then we recursively call add for that slot
