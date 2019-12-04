# Automatic-Summerizer
An automatic Summerizer that using Extractive Summerization Technique to find the Summary of n sentences
### Module Description:
 #### 1.A function to find the frequency of the words in the sentences of the corpus
   The function uses word tokenizer from NLTK to tokenize the words of the sentence. Then it finds the lemmas of the words using WordnetLemmatizer which is required to bring all the words into lemma form, thus removing ambiguities. After all these preprocessing, it creates a frequency table(dictionary based) which contain the frequency of the words according to the occurance in the text. The logic is as follows:
   
              if word has occured before then
                    wordFrequency=wordFrequency+1
              else
                    wordFrequency=1
                  
   This process is continued for all the words in the corpus to design the word frequency table
     
#### 2. Function to find the score of each sentence based on word frequency table
  This function uses a dictionary to store the sentences as well as their individual scores. The sentence score is calaculated based on the individual word scores that it contains, that is,
                  Sentence Score=Σ(word score)
   First it tries to find the word in the frequency table, after which it picks up the score of each individual word from the frquency table and adds with the sentence score, which is then asssigned against each sentence in the sentence score dictionary.
   
#### 3. Function to find  the Highest scored sentences
  This function also uses a dictionary to store the highest scored sentences.  It considers three parameters, the set of sentences, the scores and the number of sentences in the summary that user wants. Then it sorts the sentences in descending order using sorted() and stores the highest scored n sentences in the dictionary and returns it.  
