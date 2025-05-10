---
layout: post
title: "Welcome to Jekyll!"
date: 2025-03-18 11:20:40 +0100
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
<br />

### Money Talks — The Economic Engine

While population size gives countries a head start, it’s often wealth that helps them reach the finish line. Nations with higher GDP [^3] per capita can invest in elite athlete development: world-class facilities, full-time coaching, sports science support, nutrition programs, and recovery infrastructure. These resources matter — especially at the razor-thin margins of Olympic competition.

This link is clear in Figure 6, which shows the relationship between GDP per capita and total Olympic medals for 20 focus countries. Nations like the USA, Japan, and South Korea consistently outperform in total medals and also rank among the world’s richest countries.

<iframe src="/assets/gdp_medal_scatter.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 6. Relationship between GDP per Capita and Olympic medals (1972–2022): Each dot represents a country. Wealthier countries (right side of the graph) generally win more medals, especially above the $25,000 mark.</div>


However, this trend isn’t perfect. A few key exceptions challenge the idea that money guarantees Olympic success. Consider:

* Brunei: Despite being a high-income country, it has never won an Olympic medal. This may reflect limited investment in competitive sports, a small population, or lack of sports infrastructure and tradition.

* Kenya: In contrast, Kenya has a relatively low GDP per capita but consistently earns Olympic medals, especially in long-distance running. Strong cultural focus, natural training conditions, and targeted investment have helped Kenya punch above its economic weight.

To zoom out, we can examine overall Olympic performance by grouping countries into income brackets. In **Figure 7**, countries are divided into four GDP categories. The "Very High" income group (> $25k) accounts for the greatest number of medals, but the "Medium" income group also performs strongly, showing that strategic investment and sports focus can partially offset limited national wealth.

<iframe src="/assets/gdp_medal_bar_chart.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 7. Olympic Medal Count by GDP per Capita Bracket for all countries. Countries with higher GDP per capita have greater overall Olympic success, but middle-income countries also contribute significantly to global medal totals.</div>

For a closer look at how wealth helps sustain Olympic success over time, we can examine two economic success stories:

<iframe src="/assets/gdp_medal_japan.html" height="600px" width="100%" style="border:none;"></iframe> 
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 8. Japan – GDP and Medals Over Time</div>
As Japan’s economy grew in the 1980s and stabilized in the 2000s, its Olympic performance also remained strong, particularly in Summer Games.

<iframe src="/assets/gdp_medal_hungary.html" height="600px" width="100%" style="border:none;"></iframe>  
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 9. Hungary – GDP and Medals Over Time</div>
Despite a more modest GDP, Hungary has remained a strong Summer Olympics participant, showing how cultural tradition, sports specialization, and targeted support can rival economic advantages.

Together, these visualizations show that while wealth doesn’t guarantee Olympic success, it offers a clear advantage — especially when combined with national investment, sports infrastructure, and cultural support.

If population size and economic strength both matter — but don’t fully explain the differences in Olympic outcomes — what else could be influencing success?<br/>

### Nurturing Talent — The Role of Human Development

What if the key to Olympic success isn’t just wealth or size, but how well a country supports its people? Human development offers a different lens.

Instead of focusing solely on economic strength, we examined broader factors - like life expectancy, access to education, and overall standard of living - to understand their influence on Olympic success. For a historical perspective, we used the Augmented Human Development Index (AHDI), developed by the Rafael del Pino Foundation [^8]. AHDI expands upon the traditional HDI by including political and civil freedoms, providing a more holistic view of a country's development. Could this be the missing piece in explaining why some countries consistently outperform others?

In the bar chart, we compare our 20 focus countries by their average AHDI and their Olympic medal counts over the last fifty years [Fig. XX].

<div>
CHART 1
</div></br></br>

Countries with higher AHDI tend to win more medals, but there are clear outliers in both directions, suggesting that development matters, but doesn’t fully determine success.

There is a general trend: countries with higher AHDI scores - like Japan, Norway, and the USA - often have strong Olympic track records. These nations tend to have robust education systems, good public health infrastructure, and widespread access to recreational sports, all of which help nurture athletic talent from a young age. But just like with GDP, AHDI doesn’t tell the whole story. To dig deeper, we take a closer look at two countries that illustrate both sides of this dynamic: Norway and Ethiopia.

<div>
CHART 2
</div>

#### Norway: Development as a Competitive Edge

Norway is one of the most developed countries in the world, consistently ranking near the top of global AHDI charts [^10]. With a small population (around 5 million), Norway doesn’t have the advantage of scale, but it more than makes up for it in terms of development.

<div>
CHART 3
</div>

Olympic success here isn’t just about elite training, it’s deeply tied to the country’s social policies. Norway invests heavily in youth sports, prioritizes physical activity in schools, and provides widespread access to facilities and coaching [^9]. It also promotes strong gender equality in sports participation, which helps boost its medal potential across both men’s and women’s events.

While Norway is better known for dominating the Winter Olympics, it has also performed well in the Summer Games relative to its size. Over the years, it has excelled in sports like sailing, speed skating, and cross country skiing - often with athletes who train through public programs rather than private academies [^11].

In Norway’s case, AHDI appears to work as a clear enabler: a high standard of living, access to health care and education, and a culture of participation combine to support strong Olympic performance, even without a large population or the world’s biggest sports budget.

#### Ethiopia: Success Beyond Development Scores

At the other end of the spectrum is Ethiopia - a country with one of the lowest AHDI scores among our 20 focus nations. Life expectancy and income remain below global averages, and access to public infrastructure, including sports facilities, is limited in many areas.

<div>
CHART 4
</div>

Yet Ethiopia is a consistent Olympic medal winner, particularly in long-distance running [^13]. Since the 1960s, the country has produced a long line of legendary athletes, including Abebe Bikila, Haile Gebrselassie, Kenenisa Bekele, and Tirunesh Dibaba, who have dominated global competitions despite limited resources [^12].

Ethiopia’s success defies expectations set by its AHDI. Instead, it’s driven by a unique mix of factors: natural altitude training conditions, a strong running culture, and the presence of national heroes who inspire the next generation [^14]. In rural communities, running is not just a sport - it’s a pathway to international recognition and economic opportunity. Despite lacking widespread sports infrastructure, Ethiopia has built an enduring tradition in a narrow set of Olympic events, showing how cultural focus can sometimes overcome development gaps.

#### AHDI Adds Context — But Not Certainty

AHDI helps explain some of the differences in Olympic performance. Countries with higher AHDI generally have the systems and support in place to develop elite athletes. But it’s not a rule, as the stories of Norway and Ethiopia show.

High development can help create consistent, broad-based success. But strong athletic cultures, historical legacies, and geographic advantages can allow countries to thrive even when development indicators are low [^15].

In other words, AHDI adds another important piece to the Olympic puzzle, but just like population and GDP, it doesn’t complete it.

### Other Reasons

When we look at Olympic performance over the past fifty years, it’s tempting to focus purely on medal counts. But zooming out to compare how many athletes each country has sent to the Games since 1972 alongside how many medals they’ve actually won offers a bigger picture. In one key visualization, we see this relationship laid out on a plot: countries that send more athletes tend to win more medals—no surprise there.

<iframe src="/assets/atlete_medal_bar_chart.html" height="600px" width="100%" style="border:none;"></iframe>  
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Figure xx: Total Olympic Medals vs. Total Athletes Sent (1972–2022) </div>

The United States dominates on both axes, sending more than 11,000 athletes and collecting over 1,500 medals. China, Italy, and Japan also follow the trend, with large delegations and high returns.

What’s more revealing is where the pattern breaks. Countries like Kenya and Jamaica, despite relatively modest delegation sizes, show high medal efficiency—winning far more than expected given how few athletes they send. Meanwhile, countries such as India and Mexico have sent large numbers of athletes across the years, but with comparatively low medal totals. Toward the lower left of the plot, small nations like San Marino, Liechtenstein, and the Bahamas stand out for managing to win medals despite sending only a handful of athletes.

These outliers highlight an important point: Olympic success is not just a function of scale. It’s shaped by deeper, often less visible forces—history, politics, priorities, and culture.

Consider the Cold War era. Countries like the Soviet Union, East Germany, and Cuba treated Olympic medals as proof of **ideological supremacy** [^4]. Their governments invested heavily in state-controlled training systems, with athletes selected and groomed from a young age. That approach left a lasting legacy, still visible today in countries where sports development remains closely tied to state institutions.

**Colonial history** has also left its mark [^5]. Nations emerging from colonial rule often inherited uneven sports infrastructures—developed for a narrow set of disciplines or concentrated in urban centers. These imbalances shaped which sports gained traction and which were left behind, and in many cases they still define athletic opportunity today.

**Gender equality** is another important factor. Countries that actively support women’s participation in public life tend to have more balanced Olympic teams—and better results to show for it [^6]. Nordic nations are prime examples, where institutional support has long been in place for female athletes. Meanwhile, countries where gender barriers persist tend to lag in both representation and performance.

In some cases, governments have made Olympic achievement a **national mission**. China’s system of state-run sports schools and early talent identification is designed for maximum results. Australia and the UK ramped up Olympic investment after disappointing years, and both saw dramatic improvements. These weren’t accidental successes—they were planned, funded, and pursued with focus.

Finally, there’s the **cultural element**. Some countries excel in sports that are tied deeply to national identity. Kenya has built a legacy in long-distance running. Japan in martial arts [^7]. Hungary in water polo and fencing. These aren’t just athletic preferences—they’re reflections of what a country values, trains for, and celebrates.

So yes, countries with more people and more money often win more medals—but not always. The most interesting stories are often found where the trend breaks: where small nations defy the odds, or where history and policy leave a bigger mark than wealth ever could.

### Conclusion

Olympic success is shaped by a complex mix of factors - population size, wealth, development, and culture. While larger countries with higher GDPs tend to perform well, smaller nations often defy expectations. This suggests that while resources and size matter, they aren't the sole drivers of success.

The correlation matrix [Fig. XX] demonstrates the relationships between key metrics: population, GDP per capita, AHDI, and Olympic medal counts. It highlights that while wealth and population have some influence on medal counts, the strongest correlation is with AHDI. This suggests that development plays a significant role in Olympic success, but it’s not the only factor. Countries with targeted investments in certain sports or strong athletic cultures can outperform larger, wealthier nations.

<div>
MATRIX
</div>

**Reflecting on Merit and Fairness** \\
Olympic achievement raises the question: What truly defines merit in sport? Is it only about individual ability, or is it influenced by the systems, resources, and opportunities that a country provides its athletes? The disparities in resources across nations suggest that the Games, while competitive, are not entirely fair.

**Looking Ahead** \\
As the Olympics evolve, it's important to consider how the playing field can be leveled. Ensuring equitable access to resources for athletes in underdeveloped countries could provide a more even chance for success, regardless of a nation's size or wealth.

The Olympic Games are about more than just medals. They reflect the deeper forces at play in each country’s development, priorities, and investments.

#### References:

[^1]: https://journals.sagepub.com/doi/10.3233/JSA-240874
[^2]: https://www.topendsports.com/events/summer/medal-tally/medals-country-size.html
[^3]: https://data.worldbank.org/indicator/NY.GDP.PCAP.PP.CD
[^4]: https://nationalpost.com/sports/olympics/why-communist-countries-used-to-utterly-dominate-the-olympics
[^5]: https://www.academia.edu/22617135/Colonial_Olympism_Puerto_Rico_and_Jamaica_s_Olympic_movement_in_Pan_American_sport_1930_to_the_1950s
[^6]: https://www.olympics.com/ioc/news/closing-the-gender-equality-gap
[^7]: https://cotoacademy.com/olympics-in-japan/
[^8]: Rafael del Pino Foundation: Augmented Human Development Index (AHDI). https://frdelpino.es/investigacion/en_gb/world-economy/human-development-world-economy/
[^9]: How Norway Won All That Olympic Gold (Again). https://www.aspeninstitute.org/blog-posts/how-norway-won-all-that-olympic-gold-again/
[^10]: Norway, most successful Olympic nation per capita? A surprise? https://www.linkedin.com/pulse/norway-most-successful-olympic-nation-per-capita-surprise-drijard/
[^11]: The secret behind Norway’s Winter Olympic success. https://edition.cnn.com/2018/02/24/sport/norway-winter-olympic-success-intl/index.html
[^12]: Why Ethiopia's running success is about more than poverty and altitude. https://www.theguardian.com/lifeandstyle/the-running-blog/2018/aug/15/why-ethiopias-running-success-is-about-more-than-poverty-and-altitude
[^13]: London 2012: Olympic medals 'reflect human development'. https://www.bbc.com/news/uk-17908290
[^14]: Golden Past, Troubled Present. https://ethiopianbusinessreview.net/golden-past-troubled-present/
[^15]: Kenyan and Ethiopian Distance Runners: What Makes Them So Good? https://www.researchgate.net/publication/225064362_Kenyan_and_Ethiopian_Distance_Runners_What_Makes_Them_So_Good
