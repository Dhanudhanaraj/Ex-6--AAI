## NAME:Dhanumalya D
## REGISTER NO:212222230030
## EX. NO.6
## DATE:
# Implementation of Semantic ANalysis

## Aim:
To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.

## Algorithm:
Step 1: Import the nltk library.

Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.

Step 3:Accept user input for the text.

Step 4:Tokenize the input text into words using the word_tokenize function.

Step 5:Iterate through each word in the tokenized text.
• Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.
• Print each word along with its corresponding part-of-speech tag.
• For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).
• Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.
• Print the unique sets of synonyms and antonyms.
## Program:
```
!pip install nltk

import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
nltk.download('punkt_tab')

sentence=input ()

https://colab.research.google.com/drive/1tAVjhge2LhGFz_bHNyhkmfpjg_Syk_Jv#scrollTo=V7Rn79_3Zxio

# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)

# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)

from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```
## Output
![Screenshot 2024-11-15 122505](https://github.com/user-attachments/assets/35218563-8b5e-49f1-a127-aae3195d2cc0)

![Screenshot 2024-11-15 122524](https://github.com/user-attachments/assets/6ea36faf-4bad-4c87-9f9e-b18cd335eb13)

## Result:
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
