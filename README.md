# Research Paper Text Analysis with BERTopic
This project utilizes the **BERTopic** model to analyze topics in financial headlines. The goal is to evaluate the prediction quality for older versus recent news.

**Dataset**

I selected the https://huggingface.co/datasets/raeidsaqur/NIFTY dataset from Hugging Face that contains a variety of financial news from different sources. This dataset was chosen for its large size and exclusive focus on financial sentiments.

**Dataset Details:**
•	Source: Hugging Face 
•	Content: Headlines are sourced from The Wall Street Journal, Reuters News, and Yahoo Finance. The dataset includes ID, date, context, news, conversations, label, pct_change, and published news from January 2010 to July 2017.
•	Size: 1,477 rows

**Preprocessing**

To prepare the dataset for topic modeling, several preprocessing steps were implemented:
1.	Text Splitting:
   All news articles for the same day were concatenated into a single data point.
   The text was split using \n to extract individual news headlines.
2.	Duplicate Removal:
	  Removed duplicate headlines to ensure data uniqueness.
3.	Non-Financial Headline Filtering:
    Removed news that was not related to financial topics.
4.	Short News Removal:
    Data points with fewer than two words were discarded.
5.	Unnecessary Column Removal:
    Dropped irrelevant columns that did not contribute to topic modeling.
6.	Tokenization and Lemmatization:
    Abstracts were tokenized and lemmatized to ensure consistency in word forms.


