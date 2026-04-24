## 1. NLP Techniques Implemented

Describe the NLP techniques you used. Examples:

- Text normalization is used to ensure "Data" and "data" are treated the same way.
- Text cleaning is used to remove punctuation and reduce lift for frequency analysis.
- Tokenization is used to help break text into smaller pieces to aid in a more structured analysis.
- Stop word Removal is used to help filter out higher frequency words that offer little/no information.
- Frequency analysis and unigram counts is used to help understand what the text is about by counting how many times the tokens appear.

## 2. Systems and Data Sources

In this course I've analyzed the following data sources:
- Plain text documents with unstructured narrative text that have no schema or tags, and inconsistent syntax and spacing.
- Web pages where text is embedded and requires extraction from tags.
- APIs which offer structured text easier to validate with text in predicatable fields.

- To handle messy data normalization and nosie removal where vital steps for projects.

## 3. Pipeline Structure (EVTL)

Extract data from source, specificially from https://arxiv.org/abs/2604.15233 for Module 6
Validate: Input type validation was parsed using beautiful soup. Checks for specific elements were also done. For example, Title or authors h1 class="title", dive class="authors".
Transform: The following NLP processing steps were completed:
- Text Cleaning and Normalization to to remove puncuation or special characters or convert the text case.
- Tokenization to break text into smaller more usable pieces
- Stop word removal to filter out filler words
Load (to sink): The outputs included the processed csv file and the logging for the sink path to make the pipeline auditable.

## 4. Signals and Analysis Methods

Word frequency for the top 25 tokens were calculated and prepared in the bar chart and word cloud visuals. Special signals for token_count, unique_token_count, type_token_ratio, abstract_word_count and author_count were all calculated as well.

## 5. Insights

My biggest insights came from the stark differences from the inputs that focused around similar themes but produced widely different top tokens, and signal counts. In hindsight I would reduce the top tokens to 10 for my final abstract in module 6 because the top 9-25 tokens were all used the same number of times, twice. The top token, data, appeared 13 times which is almost double and triple the next most frequent tokens. Data being the top token is unsurprising as it appears 3 times in the title alone. Sentence count was added to help discern the complexity or directness of the author's writing and a ratio or average could be added to help to further draw those conclusions in examples moving forward.

## 6. Representative Work

- https://github.com/tmartin-m/nlp-02-text-processing
  - I felt this project provides a clear understanding of text processing by loading a raw file, cleaning, normalization, tokenization, and frequency analysis.

- https://github.com/tmartin-m/nlp-04-api-text-data
  -I felt this project demonstrated the understanding of a pipeline that follows EVTL. Extracting data from an external API, validating structure, transforming JSON and modifying by adding custom derived columns for things like minimum, maximum or average title length and finally loading the results.

## 7. Skills

- I can extract text data from APIs.
- I can load, clean and transform and analyze semi structured data.
- I can normalize and clean text to extract useful information to build visuals and draw insight.
- I can read and understand structured and repeatable pipelines to be able to modify for further use.
- I can present my observations in clear and direct manner using markdown and visuals for non technical users to draw value.
