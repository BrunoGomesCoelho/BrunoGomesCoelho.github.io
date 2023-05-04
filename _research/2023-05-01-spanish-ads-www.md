---
title: "Further details - Propaganda Política Pagada: Exploring U.S. Political Facebook Ads en Español"
classes: wide
date: 2023-05-01
tags: []
toc: true
toc_label: "Summary:"
categories: research
excerpt: ""

--- 

This post includes further information about our paper, [Propaganda Política Pagada: Exploring U.S. Political Facebook Ads en Español]({{ site.baseurl }}{% link download/spanish-ads-www2023.pdf %}) accepted at the [2023 ACM Web Conference (WWW 2023)](https://www2023.thewebconf.org/) in May 2023 and done in collaboration with amazing collaborators, ***Bruno Coelho***, Tobias Lauinger, Laura Edelson, Ian Goldstein, Damon McCcoy / [doi](https://doi.org/10.1145/3543507.3583425).

Presentation slides from the conference [here](https://docs.google.com/presentation/d/e/2PACX-1vQfsObOOW-38hkRbu_2ohfgJ3Km4sq4gZhlwodFD-MJ65UP3V55w-T09AGzSRwnNEArRByo5VMVjfNa/pub?start=false&loop=false&delayms=60000).

## A different way of categorizing the ads - "Ad Types"

**TLDR: Advertisers do not appear to conduct much fundraising through Spanish-language Facebook ads.**

This is further research that did not fit into the main paper.

- Methodology

One way of differentiating advertiser activity by language is the intent behind ads. 
We classify ads into three categories: Ads asking for donations (Donate); ads seeking to sell a commercial product, such as T-shirts with political slogans, “TrumpCare,” or promoting an app (Commercial); and ads informing, persuading, and connecting with users (Influence). 

The latter category includes ads that may at the same time inform about mail-in voting or ask to vote for a certain candidate or proposition, while the link leads to a form collecting contact information, thus they are difficult to subdivide in a more fine-grained way.

To classify ads, we leverage an ad’s call-to-action button text, which is selected by the advertiser among 44 predefined options (thus is likely to reflect the advertiser’s intent). 
This methodology is inspired by the paper `An Analysis of United States Online Political Advertising Transparency`.
We map the 20 most frequent buttons (such as “Donate Now”), accounting for 98 % of all button occurrences. Button texts retrieved through the Ad Library API are always in English, even when they are presented to the user in Spanish.

With this mapping, we classify 83 % of all ads, accounting for 85 % of spend across all ads (80 % of monolingual Spanish ads’ spend). We find this mapping is consistent even for ads with multiple ad creatives, with only 0.1 % of ads (0.4 % of spend) having multiple classifications due to different button types.  
Two labelers fluent in English and Spanish labeled 150 ads (75 per language) for correctness of the ad
type prediction. We find a Fleiss Kappa of 0.83, which indicates “almost perfect agreement”. When conservatively
considering an ad type as incorrect when at least one of the labelers marked it as incorrect, we find a total of 13 errors in the sample, for an accuracy of 95 %.

- Analysis

When we look at the intentions of advertisers (based on
the call-to-action buttons they selected for their ads), the
largest category in both languages are ads seeking to inform, 
persuade, or collect contact information from the audience
(78.0 % of impressions in Spanish and 63.4 % in English, or
78.0 % and 62.2 % of spend, respectively).
Notable differences emerge for commercial ads (aiming to sell
products or have users install apps), and especially donation
ads. While donation ads make up nearly 9.63 % of impressions
of all monolingual English ads, the share in Spanish is almost
two orders of magnitude smaller, at 0.14 %, for a total spend
of just $ 31 k. (Bilingual donation ads are almost nonexistent,
at only $ 594 spent for 17 k impressions.) Advertisers do
not appear to conduct much fundraising through Spanish-
language Facebook ads.


## Could lower impression numbers explain the differences observed?

TLDR: We do not believe impression-cost economics explains the differences observed.

This was one of the analysis that we performed that didn't fit into the paper - We built a statistical model to predict impression from an ad's type (see above), it's language and some other attributes. 
Our statistical significant results showed that in general, Spanish-language ads actually led to more impressions for the same cost, compared to their English counterparts. 
One difficulty of this research is not having exact numbers for both cost or impressions and instead having to rely on broad ranges - This meant we had to rely on ordinal models (ordinal both in one of it's input, the cost variable, and it's output, impression) and the result's were less directly interpretable than something like CPI (cost-per-impression).


## Productionization: Ad Observatory
Part of this research was used by the [Ad Observatory](https://adobservatory.org) team to perform multilingual topic modeling across English and Spanish.
You can read about that work [here](https://medium.com/cybersecurity-for-democracy/lab-notebook-improving-topic-modeling-for-digital-political-ads-15e5adf5d6a). 

There is a different set of requirements for a production environment, the biggest one being that we need to add new topics as they appear during an election season, unlike in our paper where we had a fixed dataset to work on. Because of that the implementation and details are slightly different, although the core use of keyword rules enhanced by aligned embeddings is the same.

## News articles

- [Spending on 2020 Spanish-language political ads on Meta lagged behind English-language ads](https://medium.com/cybersecurity-for-democracy/spending-on-2020-spanish-language-political-ads-on-meta-lagged-behind-english-language-ads-772fd22d4cee)


