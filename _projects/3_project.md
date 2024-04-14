---
layout: page
title: Prediction for Loan Default based on Machine Learning
description: Computer Federation Big Data&Computing Intelligence Contest
img: assets/img/ccf-4.webp
#redirect: https://www.datafountain.cn/competitions/530
importance: 3
category: academic
---
<h2>Background</h2>

To further promote financial inclusion, financial institutions need to serve many new customer groups. As an industry with high requirements for risk control, banks lack understanding of new customer groups, and risk control of new customer segments often becomes an important obstacle to financial inclusion. How to use banks' existing credit behavior data to serve new scenarios and new customer groups has become a valuable research direction, and transfer learning is one of the important means.

<h2>Task</h2>

This competition requires the use of another batch of existing credit data that is slightly different from the target customer group to assist in the creation of the target business risk control model. There are a large number of identical fields and very few common users between the two data sets. I hope you can use transfer learning to capture the correlation between users' basic information and default behaviors in different businesses, and help predict user defaults in new businesses.

<h2>Method</h2>

<h4>Exploratory Data Analysis</h4>

Several techniques are applied to the dataset. From the figure below, we can know the distribution of training and testing data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ccf-3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Distribution of training and testing data
</div>

<h4>Modelling</h4>

Two data sets are given with a slightly different customer group. Therefore, if we use the dataset directly, it will introduct a lot of noise. To mitigate the deficiencies, a two-phase modelling process is build.

First, by using training data public and Internet and utilizing feature engineering, a model is built based on LightGBM. Setting the thershold of 0.15, new training data is generated.

After that, a stacking model based on LightGBM, Xgboost and GBDT is created to predict whether the customer will pay the loan.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ccf-1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Flow Chart of Data
</div>

<h2>Result</h2>

The Accuracy of the model is 0.838 and the F1 score is 0.913.

From the model we built, we can know the importance of features. The highest 20 features are shown in the figure.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ccf-2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Feature Importance
</div>


