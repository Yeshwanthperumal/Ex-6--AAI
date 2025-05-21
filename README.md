
<H3>NAME: YESHWANTH P </H3>
<H3>REGISTER NO: 212222230178 </H3>
<H3>EX NO: 6 </H3>
<H3>DATE: 18/05/25 </H3>
<H1 ALIGN =CENTER>Implementation of Semantic Analysis</H1>

## <h3>Aim:</h3>
To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.
 
 
## <h3>Algorithm:</h3>

Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.

## <H3>Program:</H3>

```python
!pip install nltk

import nltk
#import wordnet
nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )

sentence=input ()

# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)

# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)

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

## <H3>Output</H3>
![443562875-a4d6f8ec-2f42-4d0a-b1fb-40cdc63b33e7](https://github.com/user-attachments/assets/71c73ccf-7626-4df7-8dc4-73e2abbfdfdd)

![443562937-b0754620-2e0c-4dde-8036-10c42d84ffd3](https://github.com/user-attachments/assets/08b8c101-ea23-41a4-bb00-ca95e33fe71e)

![443562999-453a7084-c781-4827-bbbf-048fabf0a7d6](https://github.com/user-attachments/assets/3c9db87c-475c-4611-b22e-e513294b4de5)


## <H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
