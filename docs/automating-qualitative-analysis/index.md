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
* removal of words without clear meaning for analysis, such as `a`, `an', `the`, `in`, `of` etc. Commonly such words are known as stopwords.
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

## Data-driven classifications

## Example papers

Sometimes it is easier to understand how the methods are used by examining papers showing how it has been used. The papers have been chosen so that the teaching team has been involved in analysing and writing them and we are happy to discuss any details in these and show how computers were used in write-up of this process.

* (Toivanen, P., Nelimarkka, M., & Valaskivi, K. (2021). Remediation in the hybrid media environment: Understanding countermedia in context. New Media & Society)[https://doi.org/10.1177/1461444821992701] (supervised machine learning)
* (Pantti, M., Nelimarkka, M., Nikunen, K., & Titley, G. (2019). The meanings of racism: Public discourses about racism in Finnish news media and online discussion forums. European Journal of Communication, 34(5), 503–519.)[https://doi.org/10.1177/0267323119874253]

## Computational tools
