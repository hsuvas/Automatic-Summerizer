# Automatic-Summarizer
An automatic Summarizer that using Extractive Summarization Technique to find the Summary of n sentences
### Module Description:
 #### 1. Function to find the frequency of the words in the sentences of the corpus
   The function removes the punctuations and unnecessary symbols and uses word tokenizer from NLTK to tokenize the words of the sentence. After all these preprocessing, it creates a frequency table(dictionary based) which contain the frequency of the words according to the occurrence in the text.This process is continued for all the words in the corpus to design the word frequency table and a dictionary containing all the words and their frequency is returned.
     
#### 2. Function to find the score of each sentence based on word frequency table
  This function uses a dictionary to store the sentences as well as their individual scores. The sentence score is calculated based on the individual word scores that it contains, that is,
                  Sentence Score=Σ(word score)
   First it tries to find the word in the frequency table, after which it picks up the score of each individual word from the frquency table and adds with the sentence score, which is then asssigned against each sentence in the sentence score dictionary.
   
#### 3. Function to find  the Highest scored sentences
  This function also uses a dictionary to store the highest scored sentences.  It considers three parameters, the set of sentences, the scores and the number of sentences in the summary that user wants. Then it sorts the sentences in descending order using sorted() and stores the highest scored n sentences in the dictionary and returns it.  
#### 4. Function to organize the summary 
   This function organizes the summary based on the occurrence of sentences in the text for user's convenience. The highest ranked sentences from the previous function is considered and matched with the text, according to which the sentences are ordered and joined together to find the summary. The number of sentences in the summary is equal to n, which is considered as user input.

## The Process
   1. Read the first 1000000 lines of the corpus.
   2. Call create_frequency_table() for preprocessing and find the word frequency. A wordFrequency table is returned.
   3. Call score_sentences() to find the score of the individual senteneces. The set of sentences from the corpus, the frequency of the words are passed to the function. A dictionary of sentences and their individual scores are returned.
   4. Call find_high_score() to find the highest ranked sentences which takes sentences,sentence scores and number of sentences(n) and returns the dictionary with the highest scored n sentences where n is the user input.
   5. Call gen_summary() to create the summary of n sentences. the parameters given are set of sentences, the result from step 4 and number of sentences in which the summary is sought by the user and it returns the summary according to the occurrence of sentences in the text.
