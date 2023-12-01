---
name: Final Project Showcase
tools: [Python, HTML, Altair, NumPy, Pandas]
image: assets/pngs/positive_and_negative_words.jpg
description: Showcase project using Python/Altair
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Final Project Showcase: Does the rate of images, negative, or positive words influence the amount of shares a particular article has?

The data from this project comes from this [website from the UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/332/online+news+popularity). 

This project was made by Otniel Fernandez, Colton Keiser, and Josh Kahn at the University of Illinois at Urbana-Champaign.

<!-- We can use a vegachart HTML tag like so:-->
<!-- ```do this once, then again at the end of the HTML tag-->






# What Gets Attention? Background information.

[A recent study](https://www.socialmediatoday.com/news/new-study-finds-that-including-negative-terms-in-headlines-drives-more-clic/645632/#:~:text=According%20to%20a%20new%20study%2C%20which%20analyzed%20over,positive%20terms%20decrease%20engagement%2C%20based%20on%20user%20response.), as reported by Social Media Today, delves into the intriguing dynamics of online content dissemination, specifically focusing on the impact of negative language within article headlines on overall shares. 

### Figure 1. socialmediatoday claims a higher number of clicks for more negative words <img src="https://www.socialmediatoday.com/imgproxy/85SUeEM4ugdupxuDxXBpJaUtGRB1cEUqNYo0Vwbegus/g:ce/rs:fill:685:182:0/bG9jYWw6Ly8vZGl2ZWltYWdlL3Vwd29ydGh5X2FuYWx5c2lzMi5wbmc.png"> 
<span style="font-size: smaller;">(Hutchinson, 2023).</span>



The study, which analyzed a substantial dataset comprising diverse articles, revealed a compelling correlation between the inclusion of negative terms in headlines and heightened engagement, as evidenced by increased click-through rates and shares. This unexpected finding prompts a closer examination of how negative wording might contribute to the proliferation of disinformation, as it seems that, counterintuitively, such content garners more attention and interaction from online audiences. The implications of this phenomenon raise critical questions about the psychology behind user response to negativity and its role in shaping the digital information landscape. Moreover, as the study establishes a link between negative terms and increased shares, it opens avenues for further research into whether alternative factors, such as the quantity of images or other content attributes, similarly influence the virality of online articles. In an era dominated by the rapid dissemination of information across social platforms, understanding the nuances of content engagement becomes pivotal in addressing concerns related to disinformation and its potential societal impact. So, our initial question was: does the amount of negative words in an article convince someone to share it with others?

For our initial question, we wanted to address this using the machine learning algorithm from UC Irvine to determine whether 2,000 articles (brought down from 39,645) demonstrated this phenomenon. The results are shown in Figure 1:




### Figure 2.

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot_negative.json" style="width: 100%"></vegachart>

Contrary to initial expectations, our analysis uncovered a nuanced relationship between the prevalence of negative words in article headlines and the corresponding share counts. While one might assume that a higher rate of negative language universally drives more shares, our findings challenge this assumption. Surprisingly, only a limited number of articles featuring a substantial proportion of negative words exhibited a significant surge in shares. In fact, the majority of articles that garnered high share counts hovered around a more moderate rate of negative words, approximately at the .5 mark. This suggests a unique dynamic where an optimal balance, rather than an extreme concentration, of negative language is associated with heightened engagement and shareability. The nuanced nature of this relationship prompts a reevaluation of conventional wisdom regarding the impact of negative language on digital content dissemination, highlighting the need for a more nuanced understanding of the factors influencing online audience behavior. However, does the rate of positive words exhibit the same nature?

### Positivity is Key?

In a surprising twist to the conventional narrative, our investigation into the interplay between the frequency of positive words in article headlines and their corresponding share counts challenges preconceived notions. Contrary to the premise that negativity commands sustained attention, our data reveals a compelling trend – articles featuring a higher rate of positive words, typically within the .6 to .8 range, consistently outshine their counterparts in terms of shares. This not only contradicts the prevailing assumption but also underscores the enduring allure of positivity in the digital landscape. Intriguingly, while content laced with hateful words may attract a significant initial surge of attention, this allure often proves superficial, failing to translate into sustained engagement and shares. The data suggests a nuanced user preference for uplifting and positive content, emphasizing the enduring appeal of optimism in capturing and retaining the attention of online audiences.

### Figure 3.

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot_positive.json" style="width: 100%"></vegachart>


### Pixels of Persuasion: What about images?

Drawing insights from a comprehensive analysis of one million articles, the correlation between the number of images and the subsequent shares becomes a compelling focal point. As shown by the research presented in [Moz's article on shareability factors](https://moz.com/blog/content-shares-and-links-insights-from-analyzing-1-million-articles), the impact of images on shareability is intricate and nuanced. This is consistent with the findings and that, generally, a higher number of images can enhance an article's shareability, yet the relationship is not uniformly linear. For instance, a particular article featuring only four images garnered a staggering 57,800 shares, while another with 28 images amassed 53,800 shares (as seen in figure 2 and 3). This underscores the importance of relevance, surprise, and entertainment value in images, as the Moz article aptly notes, "Surprising...entertaining images, quizzes, and videos have the potential to go viral with high shares" (Rayson, 2015). In essence, images play a pivotal role in content virality, but their impact is contingent on various factors, urging content creators to strike a delicate balance. 

In conclusion, the intricate interplay of language, positivity, negativity, and images unveils the multifaceted nature of content engagement. This article was created to demonstrate that it is imperative to exercise caution in the face of disinformation, recognizing the responsibility we bear in shaping a digital environment rooted in accuracy and credibility.

### Works Cited:

1. Fernandes,Kelwin, Vinagre,Pedro, Cortez,Paulo, and Sernadela,Pedro. (2015). Online News Popularity. UCI Machine Learning Repository. <https://doi.org/10.24432/C5NS3V>
2. Hutchinson, A. (2023, March 21). New Study Finds that Including Negative Terms in Headlines Drives More Clicks. Socialmediatoday. Retrieved 01 December. 2023, from <https://socialmediatoday.com/news/new-study-finds-that-including-negative-terms-in-headlines-drives-more-clic/645632/#:~:text=According to a new study, which analyzed over,positive terms decrease engagement, based on user response>
3. Rayson, S. (2015, September 08). Content, Shares, and Links: Insights from Analyzing 1 Million Articles - Moz. Moz. Retrieved 01 December. 2023, from <https://moz.com/blog/content-shares-and-links-insights-from-analyzing-1-million-articles>

Below is some links to both the data and the analysis code as buttons:

<!--```
<div class="left">
{% include elements/button.html link="https://github.com/otnielfernandez/otnielfernandez.github.io/blob/main/assets/json/newplot.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/otnielfernandez/otnielfernandez.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
```-->

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/otnielfernandez/otnielfernandez.github.io/blob/main/assets/json/newplot.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/otnielfernandez/otnielfernandez.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

