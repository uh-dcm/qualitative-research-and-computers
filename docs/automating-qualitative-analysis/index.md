# Automating qualitative analysis work

A whole movement of social scientists seek to engage _text as data_ ([Grimmer & Stewart, 2013](https://doi.org/10.1093/pan/mps028)): approach text in a form of quantitative asset.
Various computer-based tools can be used in this, including machine learning, network analysis or corpus linguistics tools.
Broadly speaking, these all all methods for **text mining** (for a more extensive exploration of these methods, see [Ignatow & Michalcea, 2018](https://methods.sagepub.com/book/an-introduction-to-text-mining)), we will below explore fundamental ideas related to quantifying text and analysing it using automated tools.

## Text to data

Humans read text as words, sentences and paragraphs.
Computers cannot similarly read and understand such content.
Instead, computers can _count_ frequencies of certain words (or word combinations, or words in certain context) and in this manner approach text as numerical data.
For example,

>   Alice was beginning to get very tired of sitting by her sister on the bank, and of having nothing to do: once or twice she had peeped into the book her sister was reading, but it had no pictures or conversations in it, `and what is the use of a book,' thought Alice `without pictures or conversations?'
> (from _Alice's Adventures in Wonderland_, by Lewis Carroll)

could be transformed into data by counting frequencies of words on the quote

| word | frequency |
| - | - |
| a | 1 |
| Alice | 2 |
| had | 2 |
| having | 1 |
| without | 1 |
| of | 2 |

However, already this example shows the challenge of transforming text to data:
words such as `a` or `of` do not convey clear meaning,
and words such `having` and `had` clearly have the same meaning but due to grammar rules, they are weitten in different format.

Therefore, most automated analysis process start with preprocessing of text data, including steps such as
* removal of words without clear meaning for analysis, such as `a`, `an`, `the`, `in`, `of` etc. Commonly such words are known as stopwords.
* transforming the words into their base forms (`had` and `having` would be `have`, `cats`, `cat` would be `cat`) using stemmer or lemmatization
* transforming content into lower case
* removal of punctuation

However, there currently is no stable process which must be applied.
Rather, it has been shown that different preprocessing choices lead to sligtly different outcomes ((Denny & Spirling, 2018)[https://doi.org/10.1017/pan.2017.44], (Schofield & Mimno, 2016)[https://direct.mit.edu/tacl/article/43370]).
Therefore, for now I suggest that you try to examine how text preprocessing is described in your own field and wait for further methodological research in this area.

### Finnish language in text preprocessing

There are various good tools fot text preprocessing in English language.
Finnish language works differently: for example, instead of using prefixes (`from a house`, `in a house`) we use postfixes attached to the work (`talolta`, `talossa`).
Such words are not usually well processed by most tools, tuned for English.
Instead, it is recommended to use spesific tools more suitable for Finnish language.

## Classifying based on examples

Computers can be taught to replicate classifications already classified text data.
This is helpful if the data set is large (such as 10,000s of units of analysis): human labour to classify such data set is large but classifying part of it (such as 500 units) and then using computing to power other classifications is doable.
This process is known as **supervised machine learning**: the computer uses statistical analysis to determine how much different words (or, in machine learning terminology: **features**) predict each class.
Note that the process involves humans only at the level of choosing category for each unit of analysis: the exact mechanism is left for computers to determine.
This may allow some less obvious connections to emerge compared with researcher-driven keyword selection.

There are various statistical approaches to conduct supervised machine learning (also known as algorithms): support vector machines, neural networks, or Bayesian classifier to name a few.
It is common to test all of these on the data set and examine which method performs best on these.
The best performance is measured by comparing the human-classified data (labelled data) to computer classified data using measures of inter-rater reliability, similar to [closed coding process](../closed-coding/#what-about-validity).

There are some novel practices in supervised machine learning to improve the quality of the classification.
Most importantly, it is common to split the data to train and test data sets:
models are trained using the training data set (such as 400 units of the above mentioned 500 units of labelled data) and model evaluation is conducted using data not previously seen but labelled data (the remaining 100 units).
This process is used to ensure the model is not **overfitting** to the small data set.
Another approach is to apply cross-folding: instead of running the analysis algorithm once on the 400 units, the algorithm is run several times over subsamples of the 400 units and an "average" model is produced.

## Data-driven classifications

## Example papers

Sometimes it is easier to understand how the methods are used by examining papers showing how it has been used. The papers have been chosen so that the teaching team has been involved in analysing and writing them and we are happy to discuss any details in these and show how computers were used in write-up of this process.

* (Toivanen, P., Nelimarkka, M., & Valaskivi, K. (2021). Remediation in the hybrid media environment: Understanding countermedia in context. New Media & Society)[https://doi.org/10.1177/1461444821992701] (supervised machine learning)
* (Pantti, M., Nelimarkka, M., Nikunen, K., & Titley, G. (2019). The meanings of racism: Public discourses about racism in Finnish news media and online discussion forums. European Journal of Communication, 34(5), 503–519.)[https://doi.org/10.1177/0267323119874253]

## Computational tools
