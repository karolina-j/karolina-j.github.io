---
layout: post
title:  "Welcome to Jekyll!"
date:   2025-03-18 11:20:40 +0100
categories: jekyll update
---
Every four years, the world tunes in to the Olympic Games, where countries compete for medals and national pride. But if we look beyond the excitement of the competitions, it becomes clear that winning at the Olympics isn’t just about athletic ability. Some countries regularly top the medal tables, while others rarely win. What explains this difference?

Olympic success is shaped by more than just sports training. Factors like a country’s population, economic resources, and social development all play a part. Sometimes, political events or cultural traditions can also make a difference in how well a country performs.

For the final assignment, we’re focusing on Olympic data from the Olympic Games in 1972 to 2022. Although data is available from the very first modern Olympics in 1896, we chose this period because earlier years saw many changes to country borders due to the world wars and administrative shifts. Additionally, this timeframe is long enough to capture meaningful changes in the data and highlight recent trends.

We also selected 20 focus countries so we can take a closer look at the patterns behind their medal counts. Our selection was designed to cover a full range of Olympic performance-from top medal-winning nations to countries that rarely or never win medals. We focused on countries with stable national identities since the 1970s, which allows us to make fair time-series comparisons. The chosen countries also represent a wide variety of population sizes, from less than a million to over a billion, and include nations with different economic strengths and levels of human development index.

<br />
<br />
<style>
  .olympic-table {
    width: 100%;
    border-collapse: collapse;
    font-family: Arial, sans-serif;
    margin-bottom: 20px;
  }
  
  .olympic-table th, .olympic-table td {
    border: 1px solid #a8c9a8;
    padding: 8px;
    text-align: left;
  }
  
  .olympic-table th {
    background-color: #e6f5e6;
    font-weight: bold;
  }
  
  .olympic-table tr:nth-child(even) {
    background-color: #f2f9f2;
  }
  
  .olympic-table caption {
    caption-side: bottom;
    font-size: 0.9em;
    margin-top: 5px;
    color: #666;
    text-align: left;
    padding: 4px;
    font-weight: normal;
    font-style: italic;
  }
  
  summary {
    cursor: pointer;
    font-weight: bold;
    padding: 8px;
    background-color: #e6f5e6;
    border: 1px solid #a8c9a8;
    margin-bottom: 10px;
  }
  
  summary:hover {
    background-color: #d1e8d1;
  }
</style>

<table class="olympic-table">
  <thead>
    <tr>
      <th>#</th>
      <th>Country</th>
      <th>Pop. (M)</th>
      <th>GDP/Capita (USD)</th>
      <th>HDI</th>
      <th>Olympic Success</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>🇺🇸 USA</td>
      <td>330</td>
      <td>Very High</td>
      <td>Very High</td>
      <td>🥇 Top performer</td>
    </tr>
  </tbody>
  <caption>Table 1. 20 Focus Countries</caption>
</table>

<details>
  <summary>Show more countries</summary>
  <table class="olympic-table">
    <tbody>
      <tr>
        <td>2</td>
        <td>🇯🇵 Japan</td>
        <td>125</td>
        <td>High</td>
        <td>Very High</td>
        <td>🥈 Strong, consistent</td>
      </tr>
      <tr>
        <td>3</td>
        <td>🇨🇳 China</td>
        <td>1,400</td>
        <td>Medium/High</td>
        <td>High</td>
        <td>🥇 Top performer (since 1984)</td>
      </tr>
      <tr>
        <td>4</td>
        <td>🇮🇳 India</td>
        <td>1,400</td>
        <td>Low/Medium</td>
        <td>Medium</td>
        <td>⚠️ Underperformer historically</td>
      </tr>
      <tr>
        <td>5</td>
        <td>🇧🇷 Brazil</td>
        <td>215</td>
        <td>Medium</td>
        <td>High</td>
        <td>🥉 Medium performer</td>
      </tr>
      <tr>
        <td>6</td>
        <td>🇲🇽 Mexico</td>
        <td>130</td>
        <td>Medium</td>
        <td>High</td>
        <td>🥉 Medium/low</td>
      </tr>
      <tr>
        <td>7</td>
        <td>🇮🇹 Italy</td>
        <td>60</td>
        <td>High</td>
        <td>Very High</td>
        <td>🥇 High performer</td>
      </tr>
      <tr>
        <td>8</td>
        <td>🇰🇷 South Korea</td>
        <td>52</td>
        <td>High</td>
        <td>Very High</td>
        <td>🥇 High performer</td>
      </tr>
      <tr>
        <td>9</td>
        <td>🇳🇴 Norway</td>
        <td>5.5</td>
        <td>Very High</td>
        <td>Very High</td>
        <td>🥇 Top Winter Olympics performer</td>
      </tr>
      <tr>
        <td>10</td>
        <td>🇭🇺 Hungary</td>
        <td>10</td>
        <td>High</td>
        <td>Very High</td>
        <td>🏅 Overachiever</td>
      </tr>
      <tr>
        <td>11</td>
        <td>🇹🇭 Thailand</td>
        <td>71</td>
        <td>Low/Medium</td>
        <td>Medium</td>
        <td>🥉 Low/medium</td>
      </tr>
      <tr>
        <td>12</td>
        <td>🇰🇪 Kenya</td>
        <td>55</td>
        <td>Low</td>
        <td>Low</td>
        <td>🏅 Overachiever</td>
      </tr>
      <tr>
        <td>13</td>
        <td>🇯🇲 Jamaica</td>
        <td>3</td>
        <td>Low/Medium</td>
        <td>Medium</td>
        <td>🏅 Overachiever</td>
      </tr>
      <tr>
        <td>14</td>
        <td>🇪🇹 Ethiopia</td>
        <td>120</td>
        <td>Low</td>
        <td>Low</td>
        <td>🏅 Overachiever</td>
      </tr>
      <tr>
        <td>15</td>
        <td>🇧🇩 Bangladesh</td>
        <td>170</td>
        <td>Low</td>
        <td>Medium</td>
        <td>🚫 No medals</td>
      </tr>
      <tr>
        <td>16</td>
        <td>🇳🇵 Nepal</td>
        <td>30</td>
        <td>Low</td>
        <td>Low</td>
        <td>🚫 No medals</td>
      </tr>
      <tr>
        <td>17</td>
        <td>🇧🇸 Bahamas</td>
        <td>0.4</td>
        <td>High</td>
        <td>High</td>
        <td>🏅 Very high per capita</td>
      </tr>
      <tr>
        <td>18</td>
        <td>🇸🇲 San Marino</td>
        <td>0.03</td>
        <td>High</td>
        <td>High</td>
        <td>🏅 Highest medals per capita (2020)</td>
      </tr>
      <tr>
        <td>19</td>
        <td>🇱🇮 Liechtenstein</td>
        <td>0.04</td>
        <td>Very High</td>
        <td>Very High</td>
        <td>❄️ Winter medals only</td>
      </tr>
      <tr>
        <td>20</td>
        <td>🇧🇳 Brunei</td>
        <td>0.45</td>
        <td>Very High</td>
        <td>High</td>
        <td>🚫 No medals</td>
      </tr>
    </tbody>
  </table>
</details>
<br />
<br />


Building on this foundation, we use data visualizations and analysis to investigate how population size, GDP, and other influences help explain Olympic success. Our goal is to understand what’s really driving the results and to see why some countries keep winning while others struggle to reach the podium.
<br />
<br />


<iframe src="/assets/olympic_medals_globe_final.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 1. Global Distribution of Olympic Medals (1972–2022): Each circle represents a country, with size and color indicating the total number of medals won during this period.</div>

<br />

### Size Matters - Population

A country’s population is one of the most important factors shaping its Olympic results. The basic logic is simple: larger countries have a bigger pool of potential athletes, which increases the likelihood of producing world-class competitors. This is why countries like the United States and China-two of the world’s most populous nations-consistently top the Olympic medal tables. 

Fig 2 illustrates this pattern by grouping countries according to population size and showing that nations with the largest populations have dominated the medal counts since 1972. The relationship is further visualized in Fig 3, a scatterplot highlighting the positive correlation between average population and cumulative medals. Yet, this chart also reveals important exceptions: countries like India, despite their vast populations, have historically underperformed, while smaller nations such as the Bahamas have achieved far more Olympic success than their population size would suggest.

<iframe src="/assets/population_medals_chart.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 2. Cumulative Olympic medals won by all countries (not only focus countries) grouped by population bracket (1972–2022). Countries are classified as Low, Medium, High, or Very High based on their average population, using quartile thresholds calculated from the data. The chart shows that very large countries have won the most medals, highlighting the strong influence of population size on overall Olympic success.</div>
<br />

<iframe src="/assets/population_medals_scatter.html" height="700px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 3. Relationship between population size and cumulative Olympic medals (1972–2022): While countries with larger populations like the USA and China tend to win more medals, notable exceptions such as India and the Bahamas show that population alone does not determine Olympic success</div>
<br />

To see how population trends can shape Olympic performance over time, Fig 4 focuses on China. The chart shows that as China’s population has grown, so too has its Olympic medals it has won-especially since the country’s return to the Games in the 1980s. 


<iframe src="/assets/china_population_vs_summer_and_winter_medals.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 4. China’s population growth and Olympic medal counts over time (1984–2022): As China’s population increased, its number of Summer Olympic medals rose sharply, especially after the 1980s, while Winter Olympic medals grew more gradually.</div>
<br />

While population is important, it is not the sole determinant of Olympic success. For instance, India, despite having a massive population, has historically won far fewer medals than countries with much smaller populations. Conversely, small nations like San Marino, Jamaica, and the Bahamas have achieved high medals considering their small population outperforming many larger countries when adjusting for population size. 

Many analyses [^1][^2] propose using "medals per capita" or population-adjusted rankings to better assess Olympic performance. These metrics often reveal that small countries excel relative to their size, for example with nations like San Marino, Lichtenstein and Bahamas ranking at the top for medals won per capita in the 2020 Olympic Games in Tokyo, which you can see on the fig 5.

<iframe src="/assets/2020_Olympics_Medals_per_Capita.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 5. Medals per capita for 20 selected countries at the 2020 Olympics, displayed on a logarithmic scale. The chart highlights the stark differences in Olympic success relative to population size, with small nations like San Marino and Liechtenstein achieving the highest medals per capita, while more populous countries such as India and Brazil rank lowest by this measure.
</div>
<br />

While population size plays a significant role, it’s clearly not the only factor behind Olympic success. Could a country’s wealth and economic resources be just as important?



#### Citations:


[^1]: https://journals.sagepub.com/doi/10.3233/JSA-240874
[^2]: https://www.topendsports.com/events/summer/medal-tally/medals-country-size.htm