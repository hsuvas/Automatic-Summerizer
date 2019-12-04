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
     
#### 2. 
