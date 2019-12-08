# 1. Motivation

* **What is your dataset**

The data we're working with is from the [Adventure Time Wiki](http://adventuretime.fandom.com/) which is a fanmade wiki containing descriptions, facts, trivia for every character, episode etc.
We've chosen to focus on the characters for each episode and modelled our data to reflect importance of character per episode, which then easily translates into per season and entire series.


* **Why did you choose this particular dataset?**

We're fans of the show and have noticed that it evolved from being a simple show for kids to incorperating fairly deep lore and intricate storytelling when approaching the later seasons. This seemed interesting to explore with the tools we've been taught in the course.


* **What was your goal for the end user's experience?**

Present some questions and hypothesis and hopefully draw meaningful conclusions from our data. This includes, but not limited to, if the important characters' in the earlier seasons roles in the show evolves throughout the show,  if the characters' dialog somehow changes and if so in what manner. (EXPAND)


# 2. Basic stats. Let's understand the dataset better

* **Write about your choices in data cleaning and preprocessing**

Our preliminary data exploration caused us to notice some anomalies. Firstly, a character called 'Snail'. This character had an absurdly large Out-degree, which was caused by the Snail being in *every single episode* waving at the viewer as a sort of easter egg for the attentive fan. Those who've made the list of present characters in each episode deemed this to be enough for the Snail to be a minor character in every episode thus leading to a high out-degree. The character does have some relevance in a few episodes, but we concluded that the overall importance of the character to the story was minimal as opposed to the skew in data.

Secondly, the series finaly 'Come Along With Me' is 45 minutes long as opposed to the regular \~10 minutes. This also caused the data to skew quite a bit since exluding the episode caused the average degree to go from \~37 to \~27. Since the episode wasn't very representative of the average episode, we decided to drop it from our network.


* **Write a short section that discusses the dataset stats**

For the network analyss, we're working with 956 nodes and 13075 edges.

For text analysis we have gathered transcripts from season 1 to 7 which ended up being 225 transcripts.

# 3. Tools, theory and analysis

* **Talk about how you've worked with text, including regular expressions, unicode, etc.**

* **Describe which network science tools and data analysis strategies you've used, how those network science measures work, and why the tools you've chosen are right for the problem you're solving**

To gain an understanding of the characters, we looked at their degrees along with a few centrality measures. These being Betweenness, Eigenvector and degree centrality.

Betweenness centrality is a measure of how often a node is part of the shortest path between two other nodes.

Eigenvector centrality is used to get see if important characters are often linked with other important characters, thus making them more important.

Degree centrality is the simplest form of centrality measure. This is the propability that a node is passed through.



* **How did you use the tools to understand our dataset?**

Both betweenness and degree centrality doesn't really tell us anything too interesting since it's the same bunch of central characters to the show which have the highest of those measures. Eigenvector centrality, however, seems to favor characters which are often *associated* with important characters while not actually being a central character. The Candy People and Peppermint Butler is very often with Princess Bubblegum since she governs the Candy Kingdom where the Candy People recides and Peppermint Butler is following her every step. BMO is very often with Finn and Jake since they all live together in the tree house. Tree Trunks and Mr. Pig is married and somewhat often run into problems which Finn and Jake solves (Wyatt, who's Tree Trunks ex-husband, is also shown to have a high Eigenvector centrality).

# 4. Discussion

* **What went well?**

* **What is still missing? What could be improved? Why?**

# 5. Contributions