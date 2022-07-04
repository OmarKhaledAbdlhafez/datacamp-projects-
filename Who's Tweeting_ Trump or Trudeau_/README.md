### working with Tweet classification: Trump vs. Trudeau data set which contain tweets of Trump and Trudeau the main task is to make a classification model which can guess who's is tweet ?
#### Frist Text pre-processing is needed for transferring text from human language to machine-readable format for further processing. The following pre-processing steps are applied to texts :
- Convert all words to lowercase
- Remove non-alphabet characters and urls using regx
- Remove short word (length less than 3)
- Tokenization: breaking sentences into words
- Part-of-speech (POS) tagging: process of classifying words into their grammatical category
- Lemmatization: converting a word to its base using pos tagging
- Remove stop words ( English + French ) and adding french as Trudeau speak some french words
Apply all those steps on the dataset and then collect all tweets words and get the bigram ( each two sequence words ) and counter them to see which common bigram words each person talk about .
Using  CountVectorizer and TfidfVectorizer approach to vectorize the data , CountVectorizer creates a dictionary containing the occurrence number of tokens, while TfidfVectorizer generates a dictionary with the tf-idf values of tokens.
use the Multinomial Naïve Bayes model and SVC model to learn from the training data and classify the testing data and get the the confusion matrix for each one
Adding  some improvements ( Pipline , GridSearcCv ) which make better score .

