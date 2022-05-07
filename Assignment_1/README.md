```
Group members:
Dinank Vashistha | 2018B5A71055H
Edwin Thomas | 2018A4PS0696H
Jamal | 2018A8PS1092H
```

# PROCEDURE

First make sure to maintain this folder heirarchy:  
root ->  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;code -> the code which is to be run  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'corpus' -> the corpus data files. folder name should be exactly 'corpus'.

Second, make sure you have the necessary imported libraries.

Press the run all button in python jupyter notebook, it will run all the blocks sequentially, performing the needed actions.
These actions are written in detail in the notebook and the documentation as well.

1. Stopword removal and display : Block 2 & 3
2. Stemming : Block 3
3. Index building : Block 4
4. Querying: Block 6 & 7

Wait for the notebook to ask for the input, and enter your query:

### Query format :

keywords separated with or a acombnation of AND, OR, NOT boolean operators.  
Query should not contain brackets, resolve brackets manually before entering query.

### Results

Results in the form of docIDs will be displayed in the output of the last block in the notebook.

### Sample Testcases

1. brutus and casesar
2. calphurnia
3. caes* and b\*s not cal*
4. ca\* or lord
