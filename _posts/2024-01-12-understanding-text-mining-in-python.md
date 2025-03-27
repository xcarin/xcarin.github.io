---
layout: post
---
Data is everywhere, and it take different forms such as numbers, text, pictures, videos, etc. With digital transformation growing, data is also expected to grow exponentially. Organisations will face increasing challenges to store and handle large volumes of data. These led to the rise of different industries use technology to gain customer insights from various sources:

- Customer relationship management (CRM)
- Email
- Social media
- Websites
- Forms

In this article, we will understand the basic of how text mining techniques work to extract data (number of times words appear, etc.) or remove unnecessary characters.

### What is Text Mining?
Text mining (text analysis) is an automated technique which uses natural language processing that converts unstructured text (customer feedback, ratings & reviews, etc.) to structured data.
Natural language processing (NLP) is a machine learning (artificial intelligence) technology that helps machine to understand, analyse and transform text into human language (words, sentences, etc.).

### NLP techniques & basic steps
Import and download libraries using colab or jupyter notebook.

    import nltk

<br/>

    # punkt: a sentence tokenizer which divide text into sentences
    nltk.download('punkt')

    # stopwords: words that are not in use
    nltk.download('stopwords')

    # wordnet: English dictionary
    nltk.download('wordnet')

    # omw - 1.4: process words in different languages
    nltk.download('omw-1.4')

    # average_perception_tagger: tag word of a sentence with part of speech
    nltk.download('averaged_perception_tagger')

<br/>

#### Tokenization
Tokenization is the first step of NLP and is classified into two types known as sentence tokenization and word tokenization. It is the process of breaking complex sentence into words or phrases.

    # import sentence_tokenize from nltk
    from nltk.tokenize import sent_tokenize

    # example text
    text = "2 updates from the app store? I have updated my mobile and installed the latest app, but still unable to login with my existing account. In addition, the site is down and could not access, and the link does not attach any document. There are bugs in the app and web. The site is not user friendly."

    # convert string text into sentence tokenize
    tokenize_text = sent_tokenize(text)
    tokenize_text

<br/>

    ['2 updates from the app store?',
    'I have updated my mobile and installed the latest app, but still unable to login with my existing account.',
    'In addition, the site is down and could not access, and the link does not attach any document.',
    'There are bugs in the app and web.',
    'The site is not user friendly.']

<br/>

    # import word_tokenize from nltk
    from nltk.tokenize import word_tokenize

    # example text
    text = "2 updates from the app store? I have updated my mobile and installed the latest app, but still unable to login with my existing account. In addition, the site is down and could not access, and the link does not attach any document. There are bugs in the app and web. The site is not user friendly."

    # convert string text into word tokenize
    tokenize_word = word_tokenize(text)    tokenize_word

<br/>

    ['2',
    'updates',
    'from',
    'the',
    'app',
    'store',
    '?',
    'I',
    'have',
    'updated',
    'my',
    'mobile',
    'and',
    'installed',
    'the',
    'latest',
    'app',
    ',',
    'but',
    'still',
    'unable',
    'to',
    'login',
    'with',
    'my',
    'existing',
    'account',
    '.',
    'In',
    'addition',
    ',',
    'the',
    'site',
    'is',
    'down',
    'and',
    'could',
    'not',
    'access',
    ',',
    'and',
    'the',
    'link',
    'does',
    'not',
    'attach',
    'any',
    'document',
    '.',
    'There',
    'are',
    'bugs',
    'in',
    'the',
    'app',
    'and',
    'web',
    '.',
    'The',
    'site',
    'is',
    'not',
    'user',
    'friendly',
    '.']

#### Frequency distribution & Common words
A frequency distribution is used to analyse the distribution of tokens within text and record the number of times each word appears within a given text.

<br/>

    # import word_tokenize from nltk
    from nltk.tokenize import word_tokenize

    # example text
    text = "2 updates from the app store? I have updated my mobile and installed the latest app, but still unable to login with my existing account. In addition, the site is down and could not access, and the link does not attach any document. There are bugs in the app and web. The site is not user friendly."

    # convert string text into word tokenize
    tokenize_word = word_tokenize(text)
    tokenize_word

    # find word frequency distribution
    from nltk.probability import FreqDist
    frequency_distribution = FreqDist(tokenize_word)
    frequency_distribution

<br/>

    FreqDist({'the': 5, 'and': 4, '.': 4, 'app': 3, ',': 3, 'not': 3, 'my': 2, 'site': 2, 'is': 2, '2': 1, ...})

<br/>

    # find frequency of top 3 words
    frequency_distribution1 = frequency_distribution.most_common(3)
    frequency_distribution1

<br/>

    [('the', 5), ('and', 4), ('.', 4)]

<br/>

    # import library
    import matplotlib.pyplot as plt

    # plot chart
    frequency_distribution.plot(20, cumulative=False)
    plt.show()

![Image](https://raw.githubusercontent.com/xcarin/xcarin.github.io/refs/heads/main/images/mining.png)

The line chart display the most common words are ‘the’, ‘and’ as well as punctuation ‘full stop’.

#### Stop words
Stop words are words that involve filtering common and contain less useful information such as “a”, “i”, “the”, “at”, “is”, “of”, “on”, “in”, “to”, “are”, “and”, “from”, etc. from text.

    # import sentence_tokenize from nltk
    from nltk.tokenize import sent_tokenize
    # import word_tokenize from nltk
    from nltk.tokenize import word_tokenize
    # import stopwords from nltk
    from nltk.corpus import stopwords

    # example text
    text = "2 updates from the app store? I have updated my mobile and installed the latest app, but still unable to login with my existing account. In addition, the site is down and could not access, and the link does not attach any document. There are bugs in the app and web. The site is not user friendly."
    stop_words = set(stopwords.words("english"))
    stop_words

<br/>

     {'a',
     'about',
     'above',
     'after',
     'again',
     'against',
     'ain',
     'all',
     'am',
     'an',
     'and',
     'any',
     'are',
     'aren',
     "aren't",
     'as',
     'at',
     'be',
     'because',
     'been',
     'before',
     'being',
     'below',
     'between',
     'both',
     'but',
     'by',
     'can',
     'couldn',
     "couldn't",
     'd',
     'did',
     'didn',
     "didn't",
     'do',
     'does',
     'doesn',
     "doesn't",
     'doing',
     'don',
     "don't",
     'down',
     'during',
     'each',
     'few',
     'for',
     'from',
     'further',
     'had',
     'hadn',
     "hadn't",
     'has',
     'hasn',
     "hasn't",
     'have',
     'haven',
     "haven't",
     'having',
     'he',
     'her',
     'here',
     'hers',
     'herself',
     'him',
     'himself',
     'his',
     'how',
     'i',
     'if',
     'in',
     'into',
     'is',
     'isn',
     "isn't",
     'it',
     "it's",
     'its',
     'itself',
     'just',
     'll',
     'm',
     'ma',
     'me',
     'mightn',
     "mightn't",
     'more',
     'most',
     'mustn',
     "mustn't",
     'my',
     'myself',
     'needn',
     "needn't",
     'no',
     'nor',
    'not',
    'now',
    'o',
    'of',
    'off',
    'on',
    'once',
    'only',
    'or',
    'other',
    'our',
    'ours',
    'ourselves',
    'out',
    'over',
    'own',
    're',
    's',
    'same',
    'shan',
    "shan't",
    'she',
    "she's",
    'should',
    "should've",
    'shouldn',
    "shouldn't",
    'so',
    'some',
    'such',
    't',
    'than',
    'that',
    "that'll",
    'the',
    'their',
    'theirs',
    'them',
    'themselves',
    'then',
    'there',
    'these',
    'they',
    'this',
    'those',
    'through',
    'to',
    'too',
    'under',
    'until',
    'up',
    've',
    'very',
    'was',
    'wasn',
    "wasn't",
    'we',
    'were',
    'weren',
    "weren't",
    'what',
    'when',
    'where',
    'which',
    'while',
    'who',
    'whom',
    'why',
    'will',
    'with',
    'won',
    "won't",
    'wouldn',
    "wouldn't",
    'y',
    'you',
    "you'd",
    "you'll",
    "you're",
    "you've",
    'your',
    'yours',
    'yourself',
    'yourselves'}

<br/>

    filtered_sent = []
    for word in tokenize_text:
      if word not in stop_words:
        filtered_sent.append(word)
    print("Tokenized sentence", tokenize_text)
    print("Filtered sentence", filtered_sent)

    print("Tokenized word:", tokenize_word)
    print("Filtered word:", filtered_sent)

<br/>

    Tokenized sentence ['2 updates from the app store?', 'I have updated my mobile and installed the latest app, but still unable to login with my existing account.', 'In addition, the site is down and could not access, and the link does not attach any document.', 'There are bugs in the app and web.', 'The site is not user friendly.']
    Filtered sentence ['2 updates from the app store?', 'I have updated my mobile and installed the latest app, but still unable to login with my existing account.', 'In addition, the site is down and could not access, and the link does not attach any document.', 'There are bugs in the app and web.', 'The site is not user friendly.']
    Tokenized word: ['2', 'updates', 'from', 'the', 'app', 'store', '?', 'I', 'have', 'updated', 'my', 'mobile', 'and', 'installed', 'the', 'latest', 'app', ',', 'but', 'still', 'unable', 'to', 'login', 'with', 'my', 'existing', 'account', '.', 'In', 'addition', ',', 'the', 'site', 'is', 'down', 'and', 'could', 'not', 'access', ',', 'and', 'the', 'link', 'does', 'not', 'attach', 'any', 'document', '.', 'There', 'are', 'bugs', 'in', 'the', 'app', 'and', 'web', '.', 'The', 'site', 'is', 'not', 'user', 'friendly', '.']
    Filtered word: ['2 updates from the app store?', 'I have updated my mobile and installed the latest app, but still unable to login with my existing account.', 'In addition, the site is down and could not access, and the link does not attach any document.', 'There are bugs in the app and web.', 'The site is not user friendly.']

    #### Stemming
    Text normalization technique, stemming is used to normalise the word into a common root form or base form and will result in incorrect meanings due to remove last few characters of a word.

    # import Porterstemmer from nltk
    from nltk.stem import PorterStemmer
    # import word_tokenize from nltk
    from nltk.tokenize import word_tokenize
 
    ps = PorterStemmer()
 
    # words to be stemmed
    words = ["edit", "edits", "editing", "edited"]
 
    for word in words:
        print(word, " : ", ps.stem(word))

<br/>

    edit  :  edit
    edits  :  edit
    editing  :  edit
    edited  :  edit

#### Lemmatization
Similarly, lemmatization is also a text normalization technique that is used to convert a word into a root form or base form. However, it is often the preferred technique as it provides better results.

    # import Porterstemmer from nltk
    from nltk.stem import PorterStemmer
    # import Lemmatizer from nltk
    from nltk.stem import WordNetLemmatizer
 
    ps = PorterStemmer()

    lemmatizer = WordNetLemmatizer() 

    word = "updating"
    print("Lemmatized word:", lemmatizer.lemmatize(word, "v")) 
    print("Stemmed word:", ps.stem(word))

<br/>

    Lemmatized word: update
    Stemmed word: updat

#### Part-of-speech tagging
POS tagging system is a process of labeling each word according to the part of speech such as (nouns, verbs, adjectives, adverbs, pronouns, etc.) within a sentence.


