# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification
<br>
<h1>Analyzing the Content of Dreams</h1>

<h3>Project File</h3>
<a href="https://bit.ly/38JbFMf">Google Presentation Slides</a>

### How Project 3 Notebooks are Structured

Notebook 1 Webscraping subreddit r/Dreams
<br>
Notebook 2 Webscraping subreddit r/schizophrenia
<br>
Notebook 3 Pre-Processing and Exploratory Data Analysis(EDA)
<br>
Notebook 4 Classification Modeling
<br>
- Code lines will have annotated explanations located right above.
- Imported Libraries are found at the top of each Notebook. 
   - Annotations may not have complete description of what a library or function does. Annotations serve only to be snippets of the whole. 
   - If more than one function, etc is being called from a library, the annotated explanations for the code may be read from top to bottom, and the code from left to right. 
   - For example...
 <font color="gray"> "# A does this"
   <br>
  "# B does this"
   <br>
  "# C does this"
   <br>
  <font color="red"> from X import A, B, C
<br>
<h2>Problem Statement</h2>
Compile common dream language that can be referenced by those with Schizophrenia in order to aid in differentiating a psychotic episode from reality. 

Because Schizophrenia is episodic and the exact cause is still unknown, this study aims to identify when individuals are in a dream state and if the langauge used to describe dreams may be used as reference for individuals to "wake up" and/or become self-aware when experiencing a psychotic episode.

By examining Reddit's subreddits "r/Dreams" and "r/schizophrenia", this study will use classification models to determine whether a Reddit post should be in "r/Dreams" or "r/schizophrenia". The models that will be used are Logistic Regression and Multinomial Naive Bayes. This study will evaluate the models' success based on accuracy score. The accuracy score will reflect a the total number of a model's correct predictions. 

The study will then act as the building blocks in gathering insight on the commonalities, but more importantly, key indicators which differentiate a psychotic episode from a dream. The results can be used for future evaluation on a person's mental health based on person's dreams and the threshold of psychosis. 
<br>
<h2>Executive Summary</h2>
The models performed fairly well. Multinomial Naive Bayes performed slightly less better. This could be due to MultinomialNB assumes each feature is independent from one another but that's not always the case. Ultimately, <b>Logistic Regression with TfdifVectorizer is the optimal model</b> to use in predicting whether a post goes into subreddit r/Dreams or r/schizophrenia. The optimal model reached a final accuracy score of 96%.

Logistic Regression model had a higher "f1 score" with CountVectorizer as well as TfidfVectorizer. It was important to calculate the "f1 score" as it takes False Negatives and False Positives. Given that schizophrenia is a medical condition, False Negatives and False Negatives are critical to highlight. It's worst to misdiagnose someone and say they don't have schizophrenia if that person actually does have schizophrenia. If someone isn't diagnosed but should be, then person may not be able to receive the proper treatment needed. 

Additionally, this study was able to identify most frequent unigrams and bigrams found in the subreddits which noted the invaluable observation on the language for psychotic episodes was often in "present-tense" whereas the words used for dreams were more so in "past tense". In the context of Reddit, this study successfully built a model that was able to place if a post should be in subreddit "r/Dreams" or "r/schizophrenia". With that said, the larger goal to wholly compile a thorough reference in which schizophreniacs and/or their loved ones may reference in order to "wake" from a psychotic episode was not accomplished. Of course, this endeavor is quite ambitious and requires more analysis both qualitative and quantitative outside of the realm of this project. 

<br>
<h4>Possible next steps for this project include:</h4>
<br>
- Sentiment Analysis
  - This could give a deeper more detailed analysis of language in negative words, positives words, common phrases, idioms, etc.
<br>
- Try out other models
<br>
- Look into other similar subreddits to scrape more text for analysis
<br>

<h3>Resources</h3>
<a href="https://www.reddit.com/r/Dreams/">Subreddit: dreams</a>
<br>
<a href="https://www.reddit.com/r/schizophrenia/">Subreddit: schizophrenia</a>
<br>
<a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3395964/">Iranian Journal of Psychiatry</a>
<br>
<a href="https://www.psychologytoday.com/us/blog/beautiful-minds/200903/are-people-schizophrenia-living-dream">Psychology Today: Are People with Schizophrenia Living a Dream?</a>
