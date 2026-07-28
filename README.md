This repository contains the experimental materials for the paper *Analyzing the Effects of Query Type and Ranking Methods on the Stance Distribution of Search Results on Controversial Topics*.

- `all_queries.csv`: The 490 manually validated question–keyword query pairs used in the experiments. The file contains 183 pro, 142 neutral, and 165 con query pairs across 11 topics.

## `query_pair_generation_prompts/`

This directory contains two query-generation prompt variants for each stance condition:

- `pro_query_generation_questionbase_prompt.txt`, `neutral_query_generation_questionbase_prompt.txt`, and `con_query_generation_questionbase_prompt.txt`: Generate a question query first and then a keyword query expressing the same information need.
- `pro_query_generation_keywordbase_prompt.txt`, `neutral_query_generation_keywordbase_prompt.txt`, and `con_query_generation_keywordbase_prompt.txt`: Generate a keyword query first and then a question query expressing the same information need.

## `stance_distribution/`

The CSV files report the stance distributions of the top-$k$ topically relevant results for every ranking method and query pair combination.

The columns `pro_q(%)`, `neutral_q(%)`, and `con_q(%)` give the percentages of pro, neutral, and con documents for the question query. The corresponding `pro_k(%)`, `neutral_k(%)`, and `con_k(%)` columns report the values for the keyword query. The PDF files visualize the stance distributions by ranking method, query type, and query stance, macro-averaged over the 11 topics.

- `all_stance_distribution_at3.csv`
- `all_stance_distribution_at5.csv`
- `all_stance_distribution_at10.csv`
- `all_stance_distribution_at3_figure.pdf`
- `all_stance_distribution_at5_figure.pdf`
- `all_stance_distribution_at10_figure.pdf`

## `nmd_and_rnmd/`

For each cutoff, the CSV files contain one NMD or rank-biased NMD (rNMD) value for each validated query pair and ranking method. The PDF files show the corresponding distributions across query pairs.

- `all_nmd_at3.csv`
- `all_nmd_at5.csv`
- `all_nmd_at10.csv`
- `all_rnmd_at3.csv`
- `all_rnmd_at5.csv`
- `all_rnmd_at10.csv`
- `nmd_and_rnmd_at3_boxplot_figure.pdf`
- `nmd_and_rnmd_at5_boxplot_figure.pdf`
- `nmd_and_rnmd_at10_boxplot_figure.pdf`

## `ndcg_and_stance_ndcg/`

These CSV files report mean values for each ranking method, separately by query type and query stance. The six query-specific columns combine the three stance conditions (`pro`, `neutral`, and `con`) with the two query types (`question` and `keyword`). The `all_mean` column reports the overall mean.

- `ndcg_over_the_eight_topics.csv`: Standard nDCG over the eight topics with explicit irrelevant-document judgments.
- `stance_ndcg_over_the_eight_topics.csv`: Stance-nDCG over the same eight topics.
- `stance_ndcg_over_all_11_topics.csv`: Stance-nDCG over all 11 topics.

## `pro_documents_ratio_across_controlled_corpora/`

The PDF files show the proportion of pro documents among the top-$k$ results for controlled corpora with pro:con ratios of 3:7, 5:5, and 7:3. Neutral and topically irrelevant documents are excluded. The values are macro-averaged over the 11 topics and averaged across question and keyword queries.

- `pro_documents_ratio_at3_controlled_corpora_figure.pdf`
- `pro_documents_ratio_at5_controlled_corpora_figure.pdf`
- `pro_documents_ratio_at10_controlled_corpora_figure.pdf`
