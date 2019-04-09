---
title: "Elo Merchant Category Recommendation Silver Medal"
date: 2018-10-27
tags: [machine learning, kaggle]
header:
  image: "/images/icmc.jpg"
categories: kaggle
excerpt: "Details about my silver medal on the Elo Merchant Category Recommendation challenge hosted at Kaggle"

--- 

# Competition

[Elo Merchant Category Recommendation](https://www.kaggle.com/c/elo-merchant-category-recommendation) was a early 2019 competition hosted by Elo on kaggle. After the excitement from [reaching the final of the Data Science Game 2018]({% link _kaggle/2018-10-15-dsg_2018.md %}) and taking Christmas off to rest, I was eager to jump into another data science competition and Elo provided a great chance for that.

After 2 months of a hard competition, all the hard work paid off in winning a silver medal thanks to being in the top 5% oc competitors from all over the world. Below is a copy of my thought process, pipeline and solution from my [original post](https://www.kaggle.com/c/elo-merchant-category-recommendation/discussion/82205) on kaggle.



## Introduction

Hello everyone, thanks for the great competition and discussion. Much was was learned and put into practice.

I went into this competition marked by [Yifan Xie][1] [words][2]: 

&gt; Each and every kaggle competition shall be treated as a work/study project in which you should setup a proper workflow to structure your work.

With that in mind I hope someone can take from this just as I learnt a lot from all the discussions.

## Organization ##
Github for code, reproducible jupyter notebook, lgbm/xgboost for testing things, ensemble of 4 models for submitting. The train_model function [here][3] was a great find.


## Feature Engineering ##
Much feature engineering was done. It would not have been possible with the much used [memory usage script][4] frequently shared here. Here is everything that wen into the final models, in order of what I tried. Since most ideas are not new, I will link to other users example implementation

 - Basic time features were initially done, things [such as this][5]

 - More heavy time feature engineering, things such as [here][6], [here][7] and [here][8].
 
 - Negative [month lag][9] features 

 -  [RFM][10], from both the customer_id and merchant_id, weighted and not weighted

 - Aggregations that only had few examples. For this, a especially consideration was used to not include information from whatever was in the currently validation set, ie, for each pass of the fold I would calculate it from the training data of that fold only.

 - More and more aggregation and stats 

## Models

Final model was based on combining model with and without outliers as mentioned [here][11]  with some extra modifications; basically, with a 3rd model to predict outliers, I found a ideal threshold amount to set as outliers and for those instances, the prediction was the average of the two models; for all others the prediction was based on the model without outliers.

Each model was in itself a ensemble of xgboost, catboost, lightgbm - stacking was tried, but the results weren't a improvement.


## Things I didn't have the time to do ##
Late into the competition I had to take a break due to work/traveling, so some things in the pipeline could not be tried to the end. 

I was playing with the idea of manually identifying states (and possibly a number of cities from correlation of spending/population) and including external economics and social data based on [my findings][12] that category 2 is identifying the 5 different regions in Brasil, which other people also found out.

Neural networks were also one of my next go-to things to try but alas, no time :/


## Ideas that failed ##
FM and [FFM -][13] spent some time understanding the theory, but in the end all the models built were very sub par.

[Featuretools][14] - It kind of worked and some of the features were slightly useful, but not what I expected, although I was also lacking in computing power by this point


  [1]: https://www.kaggle.com/yifanxie
  [2]: https://www.kaggle.com/c/elo-merchant-category-recommendation/discussion/75935
  [3]: https://www.kaggle.com/artgor/elo-eda-and-models
  [4]: https://www.kaggle.com/gemartin/load-data-reduce-memory-usage
  [5]: https://www.kaggle.com/ashishpatel26/lightgbm-goss-dart-parameter-tuning
  [6]: https://www.kaggle.com/rayidura/elo-lag-and-lgbm-scores/code
  [7]: https://www.kaggle.com/tunguz/eloda-with-feature-engineering-and-stacking
  [8]: https://www.kaggle.com/gpreda/elo-world-high-score-without-blending/codea
  [9]: https://www.kaggle.com/rayidura/elo-don-t-forget-the-past/code
  [10]: https://en.wikipedia.org/wiki/RFM_(customer_value)
  [11]: https://www.kaggle.com/waitingli/combining-your-model-with-a-model-without-outlier
  [12]: https://www.kaggle.com/tapioca/category-1-2-3-in-transactions
  [13]: https://www.youtube.com/watch?v=1cRGpDXTJC8&amp;t=1s
  [14]: https://docs.featuretools.com/
