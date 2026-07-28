This is the repository for the paper *Analyzing the Effects of Query Type and Ranking Methods on the Stance Distribution of Search Results on Controversial Topics*.

This directory contains the following materials for the controlled experiments reported in the paper.

- `all_queries.csv`: Each row is one validated query pair. The data contain 183 pro, 142 neutral, and 165 con query pairs across 11 topics.


#### `query_pair_generation_prompts/`

This folder contains two prompt variants for each stance condition:

- `pro_query_generation_questionbase_prompt.txt`, `neutral_query_generation_questionbase_prompt.txt`, `con_query_generation_questionbase_prompt.txt`: Generate a question query first, then a matching keyword query. 
- `pro_query_generation_keywordbase_prompt.txt`, `neutral_query_generation_keywordbase_prompt.txt`, `con_query_generation_keywordbase_prompt.txt`: Generate a keyword query first, then a matching question query.


#### `stance_distribution/`

The three CSV files contain one row for every ranking-method/query-pair combination. They report the percentage of the first $k$ topically relevant results labeled pro, neutral, and con for both query formulations. `pro_q(%)`, `neutral_q(%)`, `con_q(%)` columns describe percentage of pro, neutral, and con documents among the top $k$ relevant results for the question query. Likewise, `pro_k(%)`, `neutral_k(%)`, `con_k(%)` indicate corresponding percentages for the keyword query. Additionary, the companion PDFs visualize the macro-averaged stance distributions by ranking method, query type, and query stance.

- `all_stance_distribution_at3.csv`: stance distributions at 3 for all queries
- `all_stance_distribution_at5.csv`: stance distributions at 5 for all queries
- `all_stance_distribution_at10.csv`: stance distributions at 10 for all queries
- `all_stance_distribution_at3_figure.pdf`: macro-averaged stance distributions at 3
- `all_stance_distribution_at5_figure.pdf`: macro-averaged stance distributions at 5
- `all_stance_distribution_at10_figure.pdf`: macro-averaged stance distributions at 10


#### `nmd_and_rnmd/`

For each cutoff, `all_nmd_at{k}.csv` and `all_rnmd_at{k}.csv` store one NMD or rNMD value for each of the 490 query pairs and each ranking method. Additionally, the companion PDFs visualize their distributions across query pairs.

- `all_nmd_at3.csv`: NMD at 3 for each of all validated query pairs
- `all_nmd_at5.csv`: NMD at 5 for each of all validated query pairs
- `all_nmd_at10.csv`: NMD at 10 for each of all validated query pairs
- `all_rnmd_at3.csv`: rNMD at 3 for each of all validated query pairs
- `all_rnmd_at5.csv`: rNMD at 5 for each of all validated query pairs
- `all_rnmd_at10.csv`: rNMD at 10 for each of all validated query pairs
- `nmd_and_rnmd_at3_boxplot_figure.pdf`: boxplots of NMD at 3 and rNMD at 3
- `nmd_and_rnmd_at5_boxplot_figure.pdf`: boxplots of NMD at 5 and rNMD at 5
- `nmd_and_rnmd_at10_boxplot_figure.pdf`: boxplots of NMD at 10 and rNMD at 10


