# Word Indexer

* This is a very helpful and easy to use function that can index words or characters when you have Big Data.
* It batches the data, so is VERY fast and uses very little memory
* Returns Keras type Tokenizer
* It uses the keras Tokenizer: 

  * **num_words**: the maximum number of words to keep, based on word frequency. Only the most common num_words *  *  will be kept.
  * **filters**: a string where each element is a character that will be filtered from the texts. The default is all punctuation, plus tabs and line breaks, minus the ' character.
  * **lower**: boolean. Whether to convert the texts to lowercase.
  * **split**: str. Separator for word splitting.
  * **char_level**: if True, every character will be treated as a token.
  * **oov_token**: if given, it will be added to word_index and used to replace out-of-vocabulary words during text_to_sequence calls


[Keras Text Preprocessing](https://keras.io/preprocessing/text/)


### Function Setup

```
from keras.preprocessing.text import Tokenizer

def FitTokenizer(data, n_words, batch_size, data_size):

      data - any array of strings. It can even be a generator
   n_words - how many words to use when indexing
batch_size - any value smaller than data size 
 data_size - how many strings you have in your data
 
```
**NOTE:** A string is treated as a document of text.
 

```
tk = FitTokenizer(my_data, n_words, batch_size, len(my_data))

tk.word_counts - dictionary word : word count
tk.document_count - number of documents (should match data size)
tk.word_index - dictionary word : index ascending order from moest frequent
tk.word_docs - dictionary word : how many documents it appears in
```

## Please see tokenizer_fit.ipynb

**Thank you for using my code!**

Check out more useful tools: 
[GeorgeM](https://gmihaila.github.io)
