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


#### `ndcg_and_stance_ndcg/`

These files provide rankings-method-level means, separately for question and keyword queries and for the three query stances. In each result block, `method` identifies the ranker; the six query columns combine query stance (`pro`, `neutral`, `con`) and query type (`question`, `keyword`); `all_mean` is the overall mean. 

- `ndcg_over_the_eight_topics.csv`: Standard nDCG (topical retrieval effectiveness) over the eight topics with added relevance judgments
- `stance_ndcg_over_the_eight_topics.csv`: Stance-nDCG over the eight topics
- `stance_ndcg_over_all_11_topics.csv`: Stance-nDCG over all 11 topics


#### `pro_documents_ratio_across_controlled_corpora/`

The PDFs show the fraction of pro documents retrieved when the corpus is controlled to pro:con ratios of 3:7, 5:5, and 7:3. Neutral and topically irrelevant documents are excluded in this experiment. Values are macro-averaged over the 11 topics and averaged across question and keyword queries.

- `pro_documents_ratio_at3_controlled_corpora_figure.pdf`: proportion of pro documents at 3 across controlled corpora
- `pro_documents_ratio_at5_controlled_corpora_figure.pdf`: proportion of pro documents at 5 across controlled corpora
- `pro_documents_ratio_at10_controlled_corpora_figure.pdf`: proportion of pro documents at 10 across controlled corpora

