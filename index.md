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

<table border="1" class="dataframe">  <thead>    <tr style="text-align: center;">      <th></th>      <th>Out-degree</th>      <th>In-degree</th>      <th>Total degree</th>    </tr>  </thead>   <tbody>    <tr>      <th>0</th>      <td>(Finn, 832)</td>      <td>(Snail, 861)</td>      <td>(Snail, 1041)</td>    </tr>    <tr>      <th>1</th>      <td>(Jake, 820)</td>      <td>(BMO, 187)</td>      <td>(Jake, 978)</td>    </tr>    <tr>      <th>2</th>      <td>(BMO, 363)</td>      <td>(Candy People, 174)</td>      <td>(Finn, 965)</td>    </tr>    <tr>      <th>3</th>      <td>(Princess Bubblegum, 339)</td>      <td>(Jake, 158)</td>      <td>(BMO, 550)</td>    </tr>    <tr>      <th>4</th>      <td>(Ice King, 320)</td>      <td>(Finn, 133)</td>      <td>(Princess Bubblegum, 461)</td>    </tr>    <tr>      <th>5</th>      <td>(Marceline, 237)</td>      <td>(Lady Rainicorn, 132)</td>      <td>(Ice King, 448)</td>    </tr>    <tr>      <th>6</th>      <td>(Lumpy Space Princess, 216)</td>      <td>(Ice King, 128)</td>      <td>(Marceline, 337)</td>    </tr>    <tr>      <th>7</th>      <td>(Snail, 180)</td>      <td>(Princess Bubblegum, 122)</td>      <td>(Candy People, 304)</td>    </tr>    <tr>      <th>8</th>      <td>(Lady Rainicorn, 158)</td>      <td>(Gunter, 107)</td>      <td>(Lumpy Space Princess, 302)</td>    </tr>    <tr>      <th>9</th>      <td>(Gunter, 150)</td>      <td>(Tree Trunks, 106)</td>      <td>(Lady Rainicorn, 290)</td>    </tr>  </tbody></table>  ![Network of all characters across all episodes\label{network}](https://i.imgur.com/KfCljpy.png)

# Text analysis
