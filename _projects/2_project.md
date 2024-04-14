---
layout: page
title: Long-term Traffic Flow Forecasting with Graph Neural Network
description: Research on traffic speed prediction
img: assets/img/Traffic.png
importance: 2
category: academic
#giscus_comments: true
---

<h2>Abstract</h2>

Traffic speed prediction is an incredibly important subject of Intelligent transportation system (ITS). Efficient speed prediction methods greatly contribute to reducing traffic congestion. Most existing models focus on short term while the long-term speed prediction for a whole day is not completely developed. In this paper, a Geometric Algebra Convolutional LSTM and Graph Attention (GAConvLSTM-GAT) model is proposed to raise a potential for achieving long-term speed prediction. The proposed model is composed of a Geometric Algebra ConvLSTM (GAConvLSTM) module to extract the spatial-temporal feature, and a Graph Attention (GAT) module to make speed predictions based on the features. The experiments are evaluated by two elevated highway traffic datasets. The presented results illustrate that our GAConvLSTM model outperforms multiple baseline neural network methods.

<h2>Method</h2>

• A long-term method is proposed for fulfilling all-day speed prediction of elevated highways.

• We apply geometric algebra convolution method, which enables more effective representation of high-dimensional spatial-temporal data.

• We validate the precision and robustness of our proposed model through experiments on two elevated highway traffic datasets.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Traffic.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Structure of Geometric Algebra Convolutional LSTM and Graph Attention (GAConvLSTM-GAT) model
</div>

