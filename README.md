# Results


The analysis of ChatGPT discourse on Mastodon was conducted from two perspectives: content and user. 

Firstly, the ChatGPT-related posts were analyzed with respect to the number of daily posts over time, and the prevalence of different languages in the posts. Furthermore, the main topics in the discussions, as well as the sentiments of the posts, were also investigated via the BERTopic and Twitter-roBERTa-base models, respectively, including analysis of the changes in their prevalence over time. 

Secondly, the users who participated in the discourse were investigated based on their account creation time and bio description. The user interaction network was analyzed by identifying the most influential users via the PageRank centrality algorithm, and communities were detected using the Walktrap algorithm.

##  Content Analysis

Figure 2 shows the daily frequency of ChatGPT-related post creation on Mastodon, and Figure 3 shows the prevalence of posts’ written languages. 

As seen in Figure 2, from the launch of ChatGPT in 2022 until the end of September 2023, the number of new ChatGPT-related posts per day has decreased. The average number of ChatGPT-related posts created on Mastodon per day was 165.9.

*Figure 2 Number of New ChatGPT-Related Posts Created on Mastodon Over Time*
![20_posts_over_time](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/fa8dddea-6f77-4f8f-8d35-f9dc2c6f8a27)

Although 47 languages were used in the discussion, the top 10 languages accounted for 98.1% of the posts, with English being the most common language, contributing more
than 70% of the discussion. Only two of the top 10 most used languages, Japanese and
Chinese (7th and 8th most used, respectively), were non-European languages.

*Figure 3 Mastodon ChatGPT-Related Posts Written Language Prevalence*
![20_post_lang_pre](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/b5de0b4a-e6e6-4e9f-9125-5866a69bb343)

### RQ1 (Salience): Prevalence of Topics

Figure 4 shows the (final) 12 topics identified in the ChatGPT discourse on
Mastodon, as well as the top 10 terms associated with each topic.

*Figure 4 Identified ChatGPT Topics and Top 10 Terms of Topic*
![19_12_term_barchart](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/0c163b9b-1e9a-4d7c-8715-c565a9935754)

As the Figure 5 shows, although all topics have been discussed since the
beginning, the prevalence of each topics was different.

*Figure 5 Prevalence of ChatGPT-Related Topics over time on Mastodon*
![19_topic_pre_over_time](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/2af0a715-adfb-4d69-8471-bca3f4fc5460)


Figure 6 shows a hierarchical clustering of the final identified topics generated by
BERTopic.The hierarchical clustering showed the model’s understanding of the topics’
hierarchical nature and similarities among topics.

*Figure 6 Hierarchical Clustering of Topics Identified in ChatGPT-Related Posts on Mastodon*
![19_12_hier](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/0b088368-f0c8-47b7-b1e7-99cc8c9d39cb)


Figure 7 shows the prevalence of the identified topics in the top 10 most used
languages.

*Figure 7 Prevalence of ChatGPT-Related Topics in Top 10 Most Used Languages on Mastodon*
![20_topic_pre_per_lang](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/4556dd24-8c05-41bc-a7f2-f2153e26dfa9)


### RQ2 (Positioning): Sentiment Evaluation
Figure 8 shows the changes in the proportion of the different sentiments in
Mastodon’s ChatGPT-related posts over time, analyzed by the Twitter-roBERTa-base
model.

*Figure 8 Prevalence of ChatGPT-Related Posts’ Sentiments Over Time on Mastodon*
![20_senti_pre_over_time](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/8ca2451d-623d-4ab2-93c6-12a0fd9c2f9c)


The difference in the different sentiments’ prevalence in each topic was also
investigated. Figure 9 shows that the neutral sentiment was the most common in most
topics.

*Figure 9 Prevalence of ChatGPT-Related Posts’ Sentiments by Topic on Mastodon*
![20_senti_topic](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/491f20b2-24c1-415d-bbd0-4249975a0236)


The sentiment analysis of the posts in the top 10 most used languages displayed
in Figure 10 shows that all the languages had neutral as the most commonly expressed
sentiment and negative as the least common sentiment.

*Figure 10 Prevalence of Sentiments in Top 10 Most Used Languages on Mastodon*
![20_topic_pre_per_lang](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/de17303b-9309-449a-ae33-874279706fdd)


## User Analysis
For analyzing the ChatGPT community on Mastodon, the researcher first
investigated the creation time of the accounts found in the dataset. Figure 11 shows at
which points in time the 15,585 unique accounts posting ChatGPT-related posts were
created.

*Figure 11 Number of New ChatGPT-Related Accounts Created on Mastodon Over Time*
![20_account_over_time](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/26a9423a-e2a9-4287-8358-cb0222683186)


Figure 12 shows a word cloud of the most prevalent relevant words across all the
user descriptions. The size of each word in the figure relates to the prevalence of the
word.

*Figure 12 User Description Word Cloud of Top 35 Most Prevalent Words*
![20_acct_descr_wordcloud](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/6324b25e-e256-409f-8713-f993c0a1a028)


To find the influential users and communities in the ChatGPT discourse on
Mastodon, a directed network was built based on the users’ interactions (specifically,
mentions and replies). The nodes in the network correspond to users and the edges
between nodes represent the interactions between users. The weight of the edges,
indicating the frequency of interaction happened between two users.

Ultimately, the interaction network had 7,045 nodes (Mastodon users) and 6,691
edges (interactions between two users). The network density was 0.00013. The average
edge weight was 3.4, and the edge weight range was from 1.4 to 47.6. Figure 13 shows
the distributions of edge weights, nodes’ indegree and outdegree in the interaction
network of ChatGPT discourse on Mastodon.

*Figure 13 Distribution of Edge Weight, Indegree, Outdegree, of the Interaction Networks of the
ChatGPT Discourse on Mastodon*
![23_network_info](https://github.com/YaruWang-Code/master_thesis_mastodon_gpt/assets/85878984/1cf59e0f-8e56-46ea-a3b8-e08f20942776)


### RQ3 (Actor): Most Influential Users
The researcher applied the PageRank centrality algorithm to the interaction
network and identified the most influential users. The identities of the top 20 most
influential users were manually analyzed by checking the information on their Mastodon
profile pages. The result is shown in Table 1.

### RQ4 (Community): Community Detection
To understand the community structures in the Mastodon ChatGPT discourse,
the researcher performed network visualizations and community detection. The full
interaction network, as well as the central interaction network, are shown in Figure 14.

*Figure 14 Plot of Interaction Network of ChatGPT Discourse on Mastodon*

Then, the researcher applied the Walktrap algorithm with 20,000 steps of
random walks to the central network to identify the different communities, as shown in
Figure 15.

*Figure 15 Walktrap Community Detection*


