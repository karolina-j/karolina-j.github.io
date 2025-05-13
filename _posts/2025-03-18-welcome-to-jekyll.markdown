---
layout: post
title: "What Drives Olympic Success? A Social Data Story!"
date: 2025-03-18 11:20:40 +0100
categories: jekyll update
authors:
    [
        "Tomasz Stępień (s243062)",
        "Mirka Katuscáková (s246259)",
        "Karolina Janyga (s243068)",
    ]
---

<!-- Table of Contents -->
<nav id="toc" style="position:fixed; right:2vw; top:10vh; width:220px; max-height:80vh; overflow-y:auto; background:rgba(250, 250, 250, 0.7); border:1px solid #e0e0e0; padding:16px; border-radius:8px; font-size:0.9em; box-shadow:0 2px 8px rgba(0,0,0,0.05); backdrop-filter:blur(5px);">
  <h4 style="margin-top:0; color:#555; font-weight:500;">Content</h4>
  <ul style="padding-left:0; list-style-type:none; margin-bottom:0;">
    <li><a href="#introduction" style="text-decoration:none; color:#555;">Introduction</a></li>
    <li><a href="#size-matters---population" style="text-decoration:none; color:#555;">Size Matters - Population</a>
      <ul style="padding-left:15px;">
        <li><a href="#china-from-demographic-giant-to-olympic-powerhouse" style="text-decoration:none; color:#777; font-size:0.95em;">China: From Demographic Giant to Olympic Powerhouse</a></li>
        <li><a href="#rethinking-success-medals-per-capita" style="text-decoration:none; color:#777; font-size:0.95em;">Rethinking Success: Medals Per Capita</a></li>
      </ul>
    </li>
    <li><a href="#money-talks--the-economic-engine" style="text-decoration:none; color:#555;">Money Talks - The Economic Engine</a>
      <ul style="padding-left:15px;">
        <li><a href="#brunei-and-kenya-breaking-the-pattern" style="text-decoration:none; color:#777; font-size:0.95em;">Brunei and Kenya: Breaking the Pattern</a></li>
        <li><a href="#japan-wealth-driven-consistency" style="text-decoration:none; color:#777; font-size:0.95em;">Japan: Wealth-Driven Consistency</a></li>
        <li><a href="#hungary-tradition-over-wealth" style="text-decoration:none; color:#777; font-size:0.95em;">Hungary: Tradition Over Wealth</a></li>
        <li><a href="#wealth-helps--but-doesnt-win-medals-alone" style="text-decoration:none; color:#777; font-size:0.95em;">Wealth Helps - But Doesn't Win Medals Alone</a></li>
      </ul>
    </li>
    <li><a href="#nurturing-talent--the-role-of-human-development" style="text-decoration:none; color:#555;">Nurturing Talent - The Role of Human Development</a>
      <ul style="padding-left:15px;">
        <li><a href="#norway-development-as-a-competitive-edge" style="text-decoration:none; color:#777; font-size:0.95em;">Norway: Development as a Competitive Edge</a></li>
        <li><a href="#ethiopia-success-beyond-development-scores" style="text-decoration:none; color:#777; font-size:0.95em;">Ethiopia: Success Beyond Development Scores</a></li>
        <li><a href="#ahdi-adds-context--but-not-certainty" style="text-decoration:none; color:#777; font-size:0.95em;">AHDI Adds Context - But Not Certainty</a></li>
      </ul>
    </li>
    <li><a href="#other-reasons" style="text-decoration:none; color:#555;">Other Reasons</a></li>
    <li><a href="#conclusion" style="text-decoration:none; color:#555;">Conclusion</a>
    </li>
    <li><a href="#references" style="text-decoration:none; color:#555;">References</a></li>
  </ul>
</nav>

{% if page.authors %}

<p class="post-authors" style="margin-top: -10px">
<strong>Authors:</strong> {{ page.authors | join: ", " }}
</p>
{% endif %}

![Illustration of athletes from various sports layered over the Olympic rings](/assets/olympicsPic.webp)  
<span style="font-size: 14px; color: gray;">_Collage of Olympic athletes performing across five disciplines — basketball, diving, badminton, sprinting, and hurdles — set against the five Olympic rings._</span>  
<span style="font-size: 12px; color: gray;">
_Source: Adapted from original Olympic-themed artwork_  
<a href="https://www.christianitytoday.com/2024/07/christian-athletes-paris-2024-olympics-believers/" target="_blank" style="color: gray; text-decoration: none;">
Read more
</a>
</span>

#### Every two years, the world tunes in to the Olympic Games, where countries compete for medals and national pride. But if we look beyond the excitement of the competitions, it becomes clear that winning at the Olympics isn’t just about athletic ability. <span style="color:green">Some countries regularly top the medal tables, while others rarely win. What explains this difference?</span>

#### Olympic success is shaped by more than just sports training. Factors like a country’s population, economic resources, and social development all play a part. Sometimes, political events or cultural traditions can also make a difference in how well a country performs.

---

<br>

For the final assignment, we’re focusing on Olympic data from the Olympic Games in 1972 to 2022. Although data is available from the very first modern Olympics in 1896, we chose this period because earlier years saw many changes to country borders due to the world wars and administrative shifts. Additionally, this timeframe is long enough to capture meaningful changes in the data and highlight recent trends.

We also selected 20 focus countries as seen in Table 1 so we can take a closer look at the patterns behind their medal counts. Our selection was designed to cover a full range of Olympic performance from top medal-winning nations to countries that rarely or never win medals. We focused on countries with stable national identities since the 1970s, which allows us to make fair time-series comparisons. The chosen countries also represent a wide variety of population sizes, from less than a million to over a billion, and include nations with different economic strengths and levels of human development index.

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
  <caption>Table 1. 20 Focus Countries.</caption>
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

<div style="background:#eaf7fa;color:#155a6a;border:1px solid #b6e0ef;padding:16px 32px;border-radius:8px;margin-bottom:16px;font-size:1.1em;">
  <strong>ℹ️ Interactive!</strong> All charts in this article are interactive. You can explore them by hovering to reveal more details, zooming in on specific sections of each chart or spinning the globe. 
</div>

<iframe src="/assets/olympic_medals_globe_final.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 1. The map illustrates the total number of Olympic medals won by each country between 1972 and 2022. Darker areas indicate countries with higher medal counts, highlighting significant regional disparities in Olympic success. For instance United States or Russia.</div>

<br />

### Size Matters - Population

A country’s population is one of the most important factors shaping its Olympic results. The basic logic is simple: larger countries have a bigger pool of potential athletes, which increases the likelihood of producing world-class competitors. This is why countries like the United States and China-two of the world’s most populous nations-consistently top the Olympic medal tables.

Figure 2 illustrates this pattern by grouping countries according to population size and showing that nations with the largest populations have dominated the medal counts since 1972. The relationship is further visualized in Figure 3, a scatterplot highlighting the positive correlation between average population and cumulative medals. Yet, this chart also reveals important exceptions: countries like India, despite their vast populations, have historically underperformed, while smaller nations such as the Bahamas have achieved far more Olympic success than their population size would suggest.

<iframe src="/assets/population_medals_chart.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 2. Cumulative Olympic medals won by all countries (not only focus countries) grouped by population bracket (1972–2022). Countries are classified as Low, Medium, High, or Very High based on their average population, using quartile thresholds calculated from the data. The chart shows that very large countries have won the most medals, highlighting the strong influence of population size on overall Olympic success.</div>
<br />

<iframe src="/assets/population_medals_scatter.html" height="700px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 3. Relationship between population size and cumulative Olympic medals (1972–2022): While countries with larger populations like the USA and China tend to win more medals, notable exceptions such as India and the Bahamas show that population alone does not determine Olympic success</div>
<br />

#### China: From Demographic Giant to Olympic Powerhouse

China’s Olympic rise is a clear example of how population and national strategy can boost sporting results. Since returning to the Games in 1984, China’s population has grown by hundreds of millions, and its medal count has increased as well. As shown in Figure 4, this growth became especially sharp in the early 2000s, reaching a peak at the 2008 Beijing Olympics. But can population size alone explain China's remarkable Olympic success?
<br />
<br />
This success is not only about having more people; China also invests heavily in sports schools and talent programs to find and train future champions. The trend in Figure 4 highlights how China’s large population, combined with careful planning, has made the country a major force at the Olympics.

<iframe src="/assets/china_population_vs_summer_and_winter_medals.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 4. China’s population growth and Olympic medal counts over time (1984–2022): As China’s population increased, its number of Summer Olympic medals rose sharply, especially after the 1980s, while Winter Olympic medals grew more gradually.</div>
<br />

#### Rethinking Success: Medals Per Capita

While population is important, it is not the sole determinant of Olympic success. For instance, India, despite having a massive population, has historically won far fewer medals than countries with much smaller populations. Conversely, small nations like San Marino, Jamaica, and the Bahamas have achieved high medal totals despite their small populations, outperforming many larger countries when adjusting for population size.

Many analyses [^1][^2] propose using "medals per capita" or population-adjusted rankings to better assess Olympic performance. These metrics often reveal that small countries excel relative to their size, for example with nations like San Marino, Lichtenstein and Bahamas ranking at the top for medals won per capita in the 2020 Olympic Games in Tokyo, which you can see in the Figure 5.

<iframe src="/assets/2020_Olympics_Medals_per_Capita.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 5. Medals per capita for 20 selected countries at the 2020 Olympics, displayed on a logarithmic scale. The chart highlights the stark differences in Olympic success relative to population size, with small nations like San Marino and Bahamas achieving the highest medals per capita, while more populous countries such as India and Mexico rank lowest by this measure.
</div>
<br />

While population size plays a significant role, it’s clearly not the only factor behind Olympic success. Could a country’s wealth and economic resources be just as important?
<br />
<br />

### Money Talks — The Economic Engine

What if Olympic success is as much about resources as it is about talent? While population gives countries a larger pool of potential athletes, it's often national wealth that determines how far that talent can go. Countries with higher GDP per capita are better positioned to invest in elite athlete development: from world-class training facilities and expert coaching to sports science support, nutrition programs, and recovery infrastructure. These advantages often make the difference at the razor-thin margins of Olympic competition.

To explore this relationship, we first grouped countries into four income brackets based on GDP per capita. The bar chart in Figure 6 shows that countries in the "Very High" income bracket dominate in terms of total medals, showing a strong link between national wealth and Olympic success. However, other income groups — especially the "Medium" bracket — also contribute significantly to global medal counts. This suggests that while money helps, it's not everything.

<iframe src="/assets/gdp_medal_bar_chart.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 6. Olympic Medal Count by GDP per Capita Bracket for all countries. Countries with higher GDP per capita have greater overall Olympic success, but middle-income countries also contribute significantly to global medal totals.</div>
<br />

To examine the trend more closely, the scatterplot in Figure 7 maps GDP per capita against total Olympic medals for our 20 focus countries from 1972 to 2022. A clear trend emerges: wealthier countries like the United States, Japan, and South Korea tend to win more medals. Their economic resources allow them to build and sustain systems that support long-term athletic excellence.

But the pattern is far from perfect — some nations underperform relative to their wealth, while others punch far above their economic weight.

<iframe src="/assets/gdp_medal_scatter.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 7. Relationship between GDP per Capita and Olympic medals (1972–2022): Each dot represents a country. Wealthier countries (right side of the graph) generally win more medals, especially above the $25,000 mark.</div>
<br />

#### Brunei and Kenya: Breaking the Pattern

Some of the most revealing insights come from countries that defy the trend entirely.

-   **Brunei** stands out as a wealthy country with zero Olympic medals. Despite its high GDP per capita, it has not translated economic prosperity into Olympic success. This may reflect a combination of factors, including its small population, limited sporting traditions, or possibly low national prioritization of elite sports infrastructure.

-   **Kenya**, by contrast, is a standout success story at the opposite end of the spectrum. With a relatively low GDP per capita, Kenya consistently wins Olympic medals, especially in middle- and long-distance running. The country’s success is rooted in a combination of natural high-altitude training environments, a deep running culture, and focused investment in athletics. Kenya shows how strategic emphasis on a narrow set of events can overcome broader economic limitations.

#### Japan: Wealth-Driven Consistency

In Japan’s case, decades of rising and stable national wealth helped build a strong foundation for Olympic achievement. As Japan’s GDP per capita rose in the 1980s and stabilized in the 2000s, its medal counts followed a similar upward trend, particularly in the Summer Games, as it is illustrated in Figure 8. This sustained economic prosperity enabled large-scale investment in sports infrastructure, youth development, and coaching systems.

Japan’s strength is especially visible in sports like judo, gymnastics, and swimming — events where the country has established deep competitive traditions and continues to nurture elite talent through well-funded public programs.

<iframe src="/assets/gdp_medal_japan.html" height="700px" width="100%" style="border:none;"></iframe> 
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 8. Japan’s GDP per capita and Olympic medal counts (1972–2022): As Japan’s economic prosperity increased, both Summer and Winter Olympic medal totals generally rose, highlighting the link between national wealth and Olympic success.</div>
<br />

#### Hungary: Tradition Over Wealth

Hungary tells a different story. Although the country has seen steady economic growth since the early 1990s, its Olympic medal counts have fluctuated, sometimes diverging from GDP trends, as it is shown in Figure 9. And yet, Hungary remains a consistent overachiever in select disciplines like water polo, fencing, and canoe sprinting.

Rather than depending on broad-based wealth, Hungary’s success reflects a long-standing cultural emphasis on specific sports, backed by targeted support and a sense of national pride. In water polo, for instance, Hungary has won more Olympic gold medals than any other country — a testament to its enduring dominance in the sport.

This kind of focused legacy shows how deep-rooted traditions and strategic investment in niche disciplines can sustain Olympic success, even without the economic muscle of larger nations.

<iframe src="/assets/gdp_medal_hungary.html" height="600px" width="100%" style="border:none;"></iframe>  
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 9. Hungary’s GDP per capita and Olympic medal counts (1972–2022): Despite steady economic growth, Hungary’s Summer Olympic medal totals have fluctuated, suggesting that rising national wealth does not always directly translate to increased Olympic success.</div>
<br />

#### Wealth Helps — But Doesn't Win Medals Alone

GDP per capita is a strong predictor of Olympic success. Wealthy countries are better equipped to train, support, and sustain elite athletes — and the data makes that clear. But as Brunei and Kenya show, money alone doesn’t guarantee medals, and a lack of it doesn’t automatically hold a country back.

Japan and Hungary underline this point in different ways. Japan uses its wealth to build deep, well-funded systems across a wide range of sports. Hungary, on the other hand, leans on tradition and focused support in specific events. Both approaches work — but not because of GDP alone.

So if size and money aren’t everything, what else could be driving Olympic success?
<br/><br/>

### Nurturing Talent — The Role of Human Development

What if the key to Olympic success isn’t just wealth or size, but how well a country supports its people? Human development offers a different lens.

Instead of focusing solely on economic strength, we examined broader factors - like life expectancy, access to education, and overall standard of living - to understand their influence on Olympic success. For a historical perspective, we used the Augmented Human Development Index (AHDI), developed by the Rafael del Pino Foundation [^8]. AHDI expands upon the traditional HDI by including political and civil freedoms, providing a more holistic view of a country's development. Could this be the missing piece in explaining why some countries consistently outperform others?

The bar chart presented in Figure 10 categorizes Olympic medal counts into four AHDI brackets, revealing a clear pattern: countries in the 'Very High' bracket overwhelmingly lead in medal counts. This supports the idea that development plays a significant role in Olympic success. However, the presence of medals in lower brackets suggests that development alone does not fully determine outcomes, raising questions about the role of other factors.

<iframe src="/assets/ahdi_barPlot.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 10. 
This chart categorizes Olympic medal counts into four AHDI brackets: Low (< 0.26), Medium (0.26–0.37), High (0.37–0.52), and Very High (> 0.52). Countries in the 'Very High' bracket overwhelmingly lead in medal counts, supporting the idea that development plays a significant role in Olympic success. However, the presence of medals in lower brackets suggests that development alone does not fully determine outcomes.
</div><br>

To explore these nuances further, the scatterplot from Figure 11 compares the average AHDI of our 20 focus countries with their total Olympic medal counts over the last fifty years. This visualization highlights the general trend that countries with higher AHDI - such as Japan, Norway, and the USA - tend to dominate the medal tables. These nations tend to have robust education systems, good public health infrastructure (apart from the USA ;) ), and widespread access to recreational sports, all of which help nurture athletic talent from a young age.

But just like with GDP, AHDI doesn’t tell the whole story. To dig deeper, we take a closer look at two countries that illustrate both sides of this dynamic: _Norway_ and _Ethiopia_.

<iframe src="/assets/ahdi_scatterPlot.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 11. 
This scatter plot compares the average AHDI of 20 focus countries with their total Olympic medal counts over the last 50 years. Countries with higher AHDI, such as Norway, Japan, and the USA, tend to win more medals. However, outliers like Ethiopia and China demonstrate that factors beyond development - such as cultural focus, geographic advantages, and historical legacies - can also drive Olympic success.

</div>
<br>

#### Norway: Development as a Competitive Edge

Norway is one of the most developed countries in the world, consistently ranking near the top of global AHDI charts [^10]. With a small population (around 5.5 million), Norway doesn’t have the advantage of scale, but it more than makes up for it in terms of development.

<iframe src="/assets/ahdi_Norway.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 1px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 12. 
This line chart shows Norway’s AHDI and Olympic medal counts over time. Norway’s dominance in Winter Olympics is evident, with medal counts far exceeding those in Summer Games. The steady increase in AHDI reflects the country’s investment in youth sports, public programs, and gender equality in sports participation, which have enabled strong Olympic performance despite its small population.
</div>
<br>

Olympic success here isn’t just about elite training, it’s deeply tied to the country’s social policies. Norway invests heavily in youth sports, prioritizes physical activity in schools, and provides widespread access to facilities and coaching [^9]. It also promotes strong gender equality in sports participation, which helps boost its medal potential across both men’s and women’s events.

While Norway is better known for dominating the Winter Olympics, it has also performed well in the Summer Games relative to its size. Over the years, it has excelled in sports like sailing, speed skating, and cross country skiing - often with athletes who train through public programs rather than private academies [^11].

In Norway’s case, AHDI appears to work as a clear enabler: a high standard of living, access to health care and education, and a culture of participation combine to support strong Olympic performance, even without a large population or the world’s biggest sports budget.

#### Ethiopia: Success Beyond Development Scores

At the other end of the spectrum is Ethiopia - a country with one of the lowest AHDI scores among our 20 focus nations. Life expectancy and income remain below global averages, and access to public infrastructure, including sports facilities, is limited in many areas.

<iframe src="/assets/ahdi_Ethiopia.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 5px; color: #666; text-align: left; padding: 4px; font-weight: normal; font-style: italic;">Fig 13. 
This line chart shows Ethiopia’s AHDI and Olympic medal counts over time. Despite its low AHDI, Ethiopia has consistently excelled in Summer Olympics, particularly in long-distance running. The chart highlights Ethiopia’s gradual increase in AHDI, but its Olympic success is primarily driven by cultural focus, geographic advantages, and a strong running tradition.
</div>
<br>

Yet Ethiopia is a consistent Olympic medal winner, particularly in long-distance running [^13]. Since the 1960s, the country has produced a long line of legendary athletes, including Abebe Bikila, Haile Gebrselassie, Kenenisa Bekele, and Tirunesh Dibaba, who have dominated global competitions despite limited resources [^12].

Ethiopia’s success defies expectations set by its AHDI. Instead, it’s driven by a unique mix of factors: natural altitude training conditions, a strong running culture, and the presence of national heroes who inspire the next generation [^14]. In rural communities, running is not just a sport - it’s a pathway to international recognition and economic opportunity. Despite lacking widespread sports infrastructure, Ethiopia has built an enduring tradition in a narrow set of Olympic events, showing how cultural focus can sometimes overcome development gaps.
<br>

#### AHDI Adds Context — But Not Certainty

AHDI helps explain some of the differences in Olympic performance. Countries with higher AHDI generally have the systems and support in place to develop elite athletes. But it’s not a rule, as the stories of Norway and Ethiopia show.

High development can help create consistent, broad-based success. But strong athletic cultures, historical legacies, and geographic advantages can allow countries to thrive even when development indicators are low [^15].

In other words, AHDI adds another important piece to the Olympic puzzle, but just like population and GDP, it doesn’t complete it.

### Other Reasons

When we look at Olympic performance over the past fifty years, it’s tempting to focus purely on medal counts. But zooming out to compare how many athletes each country has sent to the Games since 1972 alongside how many medals they’ve actually won offers a bigger picture. In one key visualization, we see this relationship laid out on a plot: countries that send more athletes tend to win more medals—no surprise there.

<iframe src="/assets/atlete_medal_bar_chart.html" height="600px" width="100%" style="border:none;"></iframe>  
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 1px; color: #666; text-align: left; padding: 1px; font-weight: normal; font-style: italic;">Fig 14. Total Olympic Medals vs. Total Athletes Sent (1972–2022). This scatter plot displays the relationship between the total number of athletes sent to the Olympics and the total medal count for each of the 20 focus countries from 1972 to 2022. Each point represents a country, showing how larger delegations generally correspond to higher medal totals. The United States stands out as a clear outlier, sending the most athletes and winning the most medals by a wide margin.  </div>
<br>

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

The correlation matrix in Figure 15 demonstrates the relationships between key metrics: population, GDP per capita, AHDI, and Olympic medal counts. It highlights that while wealth and population have some influence on medal counts, the strongest correlation is with AHDI. This suggests that development plays a significant role in Olympic success, but it’s not the only factor. Countries with targeted investments in certain sports or strong athletic cultures can outperform larger, wealthier nations.

<iframe src="/assets/corrMatrix.html" height="600px" width="100%" style="border:none;"></iframe>
<div style="caption-side: bottom; font-size: 0.9em; margin-top: 1px; color: #666; text-align: left; padding: 2px; font-weight: normal; font-style: italic;">Fig 15. 
This heatmap visualizes the relationships between key metrics—population, GDP per capita, AHDI, and Olympic medal counts. The strongest correlation is between AHDI and medal counts (0.42), suggesting that development plays a significant role in Olympic success. At the same time, weaker correlations with population (0.19) and GDP per capita (0.08) highlight that size and wealth alone do not fully determine outcomes.
</div>
<br>

It's no wonder, then, that Olympic achievement raises the question: What truly defines merit in sport? Is it only about individual ability, or is it influenced by the systems, resources, and opportunities that a country provides for its athletes? The disparities in resources across nations suggest that the Games, while competitive, are not entirely fair.

And as the Olympics evolve, it's important to consider how to level the playing field. Ensuring equitable access to resources for athletes in underdeveloped countries could provide a more even chance for success, regardless of a nation's size or wealth.
<br>

In the end, the Olympic Games are about so much more than just medals. They reflect the deeper forces at play in each country’s development, priorities, and investments. This is why true Olympic spirit lies in creating a world where every athlete, regardless of where they call home, has the opportunity to reach for gold.
<br><br><br><br>

#### References:

[^1]: Sage Journals Home. Population-adjusted national rankings in the Olympics. https://journals.sagepub.com/doi/10.3233/JSA-240874
[^2]: Topend Sports. Summer Olympic Games: Medals by Country Size. https://www.topendsports.com/events/summer/medal-tally/medals-country-size.html
[^3]: The World Bank. GDP per capita, PPP (current international $). https://data.worldbank.org/indicator/NY.GDP.PCAP.PP.CD
[^4]: National Post. Why communist countries used to utterly dominate the Olympics. https://nationalpost.com/sports/olympics/why-communist-countries-used-to-utterly-dominate-the-olympics
[^5]: Academia.edu. Colonial Olympism: Puerto Rico and Jamaica’s Olympic movement in Pan American sport, 1930 to the 1950s. https://www.academia.edu/22617135/Colonial_Olympism_Puerto_Rico_and_Jamaica_s_Olympic_movement_in_Pan_American_sport_1930_to_the_1950s
[^6]: International Olympic Committee. Closing the gender equality gap. https://www.olympics.com/ioc/news/closing-the-gender-equality-gap
[^7]: Coto Academy. Olympics in Japan. https://cotoacademy.com/olympics-in-japan/
[^8]: Rafael del Pino Foundation. Augmented Human Development Index (AHDI). https://frdelpino.es/investigacion/en_gb/world-economy/human-development-world-economy/
[^9]: Aspen Institute. How Norway Won All That Olympic Gold (Again). https://www.aspeninstitute.org/blog-posts/how-norway-won-all-that-olympic-gold-again/
[^10]: LinkedIn. Norway, most successful Olympic nation per capita? A surprise? https://www.linkedin.com/pulse/norway-most-successful-olympic-nation-per-capita-surprise-drijard/
[^11]: CNN. The secret behind Norway’s Winter Olympic success. https://edition.cnn.com/2018/02/24/sport/norway-winter-olympic-success-intl/index.html
[^12]: The Guardian. Why Ethiopia's running success is about more than poverty and altitude. https://www.theguardian.com/lifeandstyle/the-running-blog/2018/aug/15/why-ethiopias-running-success-is-about-more-than-poverty-and-altitude
[^13]: BBC. London 2012: Olympic medals 'reflect human development'. https://www.bbc.com/news/uk-17908290
[^14]: Ethiopian Business Review. Golden Past, Troubled Present. https://ethiopianbusinessreview.net/golden-past-troubled-present/
[^15]: ResearchGate. Kenyan and Ethiopian Distance Runners: What Makes Them So Good? https://www.researchgate.net/publication/225064362_Kenyan_and_Ethiopian_Distance_Runners_What_Makes_Them_So_Good
