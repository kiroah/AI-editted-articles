# Analyzing articles editted by AI (namely, chatGPT)

Repository to store jupyter notebooks used to analyze the differences between Medium articles with or without chatGPT edits. For now, the analysis is limited to word occurance filtered by POS (Part of Speech). 

__Discoveries__
* There are noticeable differences in adjectives that are used more favorably by chatGPT when asking it to edit articles, which are arguably more attractive. Some of the top adjectives are: valuable, essential, cruical, comprehensive
* On the other hand, simpler adjectives have decreased after chatGPT edit. Some of the adjectives are: other, same, many, more, different
* When comparing 2022 articles (pre-chatGPT era) VS 2023 articles (post-chatGPT era), the adjectives that are used more in 2023 are strikingly similar to the chatGPT editted articles adjectives for data science tagged articles

Analysis is done with \~10,000 articles for chatGPT edit analysis, and \~3500 per year for 2022 VS 2023 analysis. The notebook has 2016~2021 data as well.

As a high level summary of what the notebooks do: 

* __[scrape_medium.ipynb](https://nbviewer.org/github/kiroah/AI-editted-articles/blob/main/scrape_medium.ipynb)__
  * Scrape article list from Medium by tag (currently using _"data-science"_)
  * Scrape articles based on the article list (after random sampling)
* __[chatgpt.ipynb](https://nbviewer.org/github/kiroah/AI-editted-articles/blob/main/chatgpt.ipynb)__
  * Run the scraped articles against chatGPT with a prompt to edit the article
  * Run POS tagging using nltk and see term occurance difference by type of POS (e.g. adjective, adverb)
* __[trend_analysis.ipynb](https://nbviewer.org/github/kiroah/AI-editted-articles/blob/main/trend_analysis.ipynb)__
  * Additionally run yearly trend analysis of the original articles and its term occurance by type of POS, to see article trend diffs between pre-chatGPT VS. post-chatGPT (after 1/22/2023)


