---
published: true
layout: post
---
## My CLI Gem Project
cli.rb controls the workflow of the gem providing various command line interaction methods.

The available options from within the CLI are:
* Viewing a list of teaser articles
* Choosing an ID from the teaser list which provides output of the full article
* An added bonus at the end of the full article is the option to open the source article in a browser

https://factcheck.org/fake-new/ was used to scrape the data for the gem output.

I created two methods for scraping the data required for this gem.

* The first method <code>search_results</code> parses out the fields required to make up the initial list of article teasers. This required setting an id for each teaser article that is then used to pull up the full article.

* The second method <code>answers(answer_id)</code> scrapes the full article and is associated with the <code>search_results</code> method via the more_link variable.

"Fake News" CLI Data Gem https://joshuaneedham.github.io/fake-news-cli-gem/
