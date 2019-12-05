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

We look at the top ten degrees for in, out and total degree to get a sense of which characters are the most important for the series.
<table border="1" class="dataframe">  <thead>    <tr style="text-align: center;">      <th></th>      <th>Out-degree</th>      <th>In-degree</th>      <th>Total degree</th>    </tr>  </thead>  <tbody>    <tr>      <th>0</th>      <td>Finn: 832</td>      <td>Snail: 861</td>      <td>Snail: 1041</td>    </tr>    <tr>      <th>1</th>      <td>Jake: 820</td>      <td>BMO: 187</td>      <td>Jake: 978</td>    </tr>    <tr>      <th>2</th>      <td>BMO: 363</td>      <td>Candy People: 174</td>      <td>Finn: 965</td>    </tr>    <tr>      <th>3</th>      <td>Princess Bubblegum: 339</td>      <td>Jake: 158</td>      <td>BMO: 550</td>    </tr>    <tr>      <th>4</th>      <td>Ice King: 320</td>      <td>Finn: 133</td>      <td>Princess Bubblegum: 461</td>    </tr>    <tr>      <th>5</th>      <td>Marceline: 237</td>      <td>Lady Rainicorn: 132</td>      <td>Ice King: 448</td>    </tr>    <tr>      <th>6</th>      <td>Lumpy Space Princess: 216</td>      <td>Ice King: 128</td>      <td>Marceline: 337</td>    </tr>    <tr>      <th>7</th>      <td>Snail: 180</td>      <td>Princess Bubblegum: 122</td>      <td>Candy People: 304</td>    </tr>    <tr>      <th>8</th>      <td>Lady Rainicorn: 158</td>      <td>Gunter: 107</td>      <td>Lumpy Space Princess: 302</td>    </tr>    <tr>      <th>9</th>      <td>Gunter: 150</td>      <td>Tree Trunks: 106</td>      <td>Lady Rainicorn: 290</td>    </tr>  </tbody></table>'

<table border="1" class="dataframe">  <thead>    <tr style="text-align: center;">      <th></th>      <th>Betweenness</th>      <th>Eigenvector</th>      <th>Degree centrality</th>    </tr>  </thead>  <tbody>    <tr>      <th>0</th>      <td>Snail: 0.4</td>      <td>Snail: 0.401</td>      <td>Snail: 1.09</td>    </tr>    <tr>      <th>1</th>      <td>Jake: 0.152</td>      <td>Candy People: 0.178</td>      <td>Jake: 1.024</td>    </tr>    <tr>      <th>2</th>      <td>Finn: 0.129</td>      <td>BMO: 0.139</td>      <td>Finn: 1.01</td>    </tr>    <tr>      <th>3</th>      <td>BMO: 0.109</td>      <td>Peppermint Butler: 0.128</td>      <td>BMO: 0.576</td>    </tr>    <tr>      <th>4</th>      <td>Princess Bubblegum: 0.076</td>      <td>Lady Rainicorn: 0.125</td>      <td>Princess Bubblegum: 0.483</td>    </tr>    <tr>      <th>5</th>      <td>Ice King: 0.05</td>      <td>Tree Trunks: 0.121</td>      <td>Ice King: 0.469</td>    </tr>    <tr>      <th>6</th>      <td>Lady Rainicorn: 0.041</td>      <td>Princess Bubblegum: 0.116</td>      <td>Marceline: 0.353</td>    </tr>    <tr>      <th>7</th>      <td>Marceline: 0.04</td>      <td>Ice King: 0.113</td>      <td>Candy People: 0.318</td>    </tr>    <tr>      <th>8</th>      <td>Candy People: 0.034</td>      <td>King of Ooo: 0.112</td>      <td>Lumpy Space Princess: 0.316</td>    </tr>    <tr>      <th>9</th>      <td>Gunter: 0.031</td>      <td>Jake: 0.109</td>      <td>Lady Rainicorn: 0.304</td>    </tr>  </tbody></table>

![Network of all characters across all episodes\label{network}](https://i.imgur.com/KfCljpy.png)

# Text analysis
