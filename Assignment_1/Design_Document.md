```
Group members:
Dinank Vashistha | 2018B5A71055H
Edwin Thomas | 2018A4PS0696H
Jamal | 2018A8PS1092H
```

## The step by step architecture of the application

1. Import necessary libraries, change the directory to corpus data directory.
2. Load the corpus.
3. Use dictionary and list data structures to create mappings for title + data and mapping from title to docID and vice versa.
4. Clean the data, remove punctuations, redundant metadata, single chars with the help of regex expression matching.
5. Split the data into tokens, count them over the whole corpus and determine stopwords by frequency analysis.
6. Remove the stopwords from the dictionary mappings we created, and convert every words to it's stemmed form.
7. Assign the cleaned and stemmed token lists to respective dictionary keys (title)
8. Create postings and permuterms both using dictionary data structure.
9. Define functions to handle wildcard search forms, and for fetching the matched keys.
10. Define function to handle the key with or without wildcard character \*
11. Define functions to perform AND, OR, NOT operations on list(s).
12. Take the input from the user, in bracket free form.
13. Parse the query first splitting on 'or' keyword, then processing the both sides of 'or'.
14. If the query contains AND, NOT operators. Parse them with the help of different cases.

    - 2 not operators with and
    - 1 not operators with and
    - 0 not operatos with and
    - only not operator
    - no operators

15. Join the lists recieved with OR operation, and display the result.
