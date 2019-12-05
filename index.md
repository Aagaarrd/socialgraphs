# Introduction

Our project is based on an analysis of the Cartoon Network animated TV-series Adventure Time. The series launched in April 2010 and concluded in September of 2018 with 10 seasons and 283 episodes which on average are about 10 minutes each. We wish to present some questions and hypotheses and try to answer them with network and text analysis.

## Data
We gather a list of characters for each episode from the [Adventure Time Wiki](adventuretime.fandom.com). This already lead us to some choices about how we wanted to model the analysis. We chose to base it on the characters in each episode for which there are two lists in each episode article: 'Major Characters' and 'Minor Characters' - from what we can see these are ordered in approximate importance for the episode. Because of this the links between characters are made up of combinations of the combined list of major and minor characters since it gives a good indication of which characters are the most important.

The Wiki also provides transcripts for a majority of the episodes. They cut off at around season 8. It seems like no one has had the motivation to transcribe these episodes (future work?). This causes us to only work with episode transcripts from season 1-7. 

### Short summary of data
- 956 characters (nodes)
- 14041 relations (links)
- 225 transcripts (season 1-7)

# Network analysis

<table border="1" class="dataframe">\n  <thead>\n    <tr style="text-align: right;">\n      <th></th>\n      <th>Out-degree</th>\n      <th>In-degree</th>\n      <th>Total degree</th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <th>0</th>\n      <td>(Finn, 832)</td>\n      <td>(Snail, 861)</td>\n      <td>(Snail, 1041)</td>\n    </tr>\n    <tr>\n      <th>1</th>\n      <td>(Jake, 820)</td>\n      <td>(BMO, 187)</td>\n      <td>(Jake, 978)</td>\n    </tr>\n    <tr>\n      <th>2</th>\n      <td>(BMO, 363)</td>\n      <td>(Candy People, 174)</td>\n      <td>(Finn, 965)</td>\n    </tr>\n    <tr>\n      <th>3</th>\n      <td>(Princess Bubblegum, 339)</td>\n      <td>(Jake, 158)</td>\n      <td>(BMO, 550)</td>\n    </tr>\n    <tr>\n      <th>4</th>\n      <td>(Ice King, 320)</td>\n      <td>(Finn, 133)</td>\n      <td>(Princess Bubblegum, 461)</td>\n    </tr>\n    <tr>\n      <th>5</th>\n      <td>(Marceline, 237)</td>\n      <td>(Lady Rainicorn, 132)</td>\n      <td>(Ice King, 448)</td>\n    </tr>\n    <tr>\n      <th>6</th>\n      <td>(Lumpy Space Princess, 216)</td>\n      <td>(Ice King, 128)</td>\n      <td>(Marceline, 337)</td>\n    </tr>\n    <tr>\n      <th>7</th>\n      <td>(Snail, 180)</td>\n      <td>(Princess Bubblegum, 122)</td>\n      <td>(Candy People, 304)</td>\n    </tr>\n    <tr>\n      <th>8</th>\n      <td>(Lady Rainicorn, 158)</td>\n      <td>(Gunter, 107)</td>\n      <td>(Lumpy Space Princess, 302)</td>\n    </tr>\n    <tr>\n      <th>9</th>\n      <td>(Gunter, 150)</td>\n      <td>(Tree Trunks, 106)</td>\n      <td>(Lady Rainicorn, 290)</td>\n    </tr>\n  </tbody>\n</table>

![Network of all characters across all episodes\label{network}](https://i.imgur.com/KfCljpy.png)

# Text analysis
