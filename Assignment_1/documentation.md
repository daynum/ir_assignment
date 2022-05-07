```
Group members:
Dinank Vashistha | 2018B5A71055H
Edwin Thomas | 2018A4PS0696H
Jamal | 2018A8PS1092H
```

## Block 1

Libraries needed:

- PorterStemmer -> from nltk.stem
- Counter -> from Collections
- OrderedDict -> from Collections
- os
- re

Libraries are imported and directory set to corpus data directory.

## Block 2

1. Creating mappings from files names to docIDs and vice-versa.
2. Removing words such as: ACT 1, SCENE 1, redundant beginning metadata, single chars, punctuations.
3. Splitting the whole data into tokens, and storing them as a dictionary with key as title and value as a list of tokens.

4. Scanning the whole corpus, counting their frequencies, and removing top 30 most common words. So this is corpus specific stopword removal.

## Block 3

1. This is the most time taking task with complexity: O( D \* (N+N) ).  
   Hence, the complexity of the whole code would be:  
   O (number of documents \* average number of words in documents)
2. Creating a new list with stopwords removed, and then stemming all of them

3. Then assignning this cleaned and stemmed list of tokens back to the dictionary with title as key.

## Block 4

1. Creating postings with keys as word tokens, and value as a list of docIDs.
2. Creating permuterm indices with adding a dollar sign and rotating the word.
3. Try catch block if the key doesn't exist, to add it.

## Block 5

### Defining lambda expressions and functions needed for further processing.

1. get_matched_keys (wildcard key with \* at end): lambda expression to fetch keys which match with our wildcard searching format.
2. get_wild (key entered by user in wildcard format): function to handle different cases of wildcard searching formats.
3. sanitize_key (key entered by user): function to handle whether entered key has wildcard format or plain.
4. listAND (list 1, list 2): function to join 2 lists with AND operator.
5. listOR (list 1, list 2): function to join 2 lists with OR operator.

6. listNOT (list 1): function to negate a list with NOT operator.

## Block 6

1. Block to just take input from the user.
2. Input must be in bracket free form.

3. Query first split on 'or' keyword, both sides are resolved and then added with listOR function.

## Block 7

1. Processing the parts recieved after OR splitting. Only 'and', 'not' keywords remain.
2. Handling 'and' cases: either both keywords need to be negated, or only one of them needs to be negated, or none of them needs to be negated.
3. If the part doesn't contain 'and' then we directly procees to check for NOT and process the keyword.
4. Finally, join final list of lists with OR operator between all of them.

5. Remove duplicates and sort them and display.
