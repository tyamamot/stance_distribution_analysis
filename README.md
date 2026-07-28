This is the repository for the paper *Analyzing the Effects of Query Type and Ranking Methods on the Stance Distribution of Search Results on Controversial Topics*.

This directory contains the following materials for the controlled experiments reported in the paper.

- `all_queries.csv`: Each row is one validated query pair. The data contain 183 pro, 142 neutral, and 165 con query pairs across 11 topics.

###`query_pair_generation_prompts/`

This folder contains two prompt variants for each stance condition:

- `pro_query_generation_questionbase_prompt.txt`, `neutral_query_generation_questionbase_prompt.txt`, `con_query_generation_questionbase_prompt.txt`: Generate a question query first, then a matching keyword query. 
- `pro_query_generation_keywordbase_prompt.txt`, `neutral_query_generation_keywordbase_prompt.txt`, `con_query_generation_keywordbase_prompt.txt`: Generate a keyword query first, then a matching question query.

- `all_stance_distribution_at3.csv`: stance distributions at 3 for all queries
- `all_stance_distribution_at5.csv`: stance distributions at 5 for all queries
- `all_stance_distribution_at10.csv`: stance distributions at 10 for all queries
