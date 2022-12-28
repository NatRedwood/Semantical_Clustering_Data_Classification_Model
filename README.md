# Semantical Clustering Data Classification Model

Natalia Wojarnik, Cutter Dalton
Final Project Presentation
Neural Networks and Deep Learning
Fall 2022, CU Boulder

# What and why?
## Motivations and Improved Solutions

Recent Developments in machine learning have shown significant improvements in
the development of complex and robust models capable of solving multiple NLP.
More complicated models demand larger datasets and stronger computational
power. Recently, focus has shifted towards data quality in an attempt to eschew
more cumbersome models. This project observes the change in performance in
models when ordering data by semantic-relatedness during training.
Data-ordering is the intentional grouping of data points when feeding data into the
model. In this experiment we observe the efficacy of ordering data by
semantic-relatedness where data points (in this case, news pieces) are grouped
together by topic, and then fed into a model which predicts the news category.

# What inspired us?
## Related Work
The idea that humans learn faster and more efficient when the examples
given are clustered together in some kind of semantic way. The idea of data
ordering is not new to the field of NN and DL but it’s mostly used in
Curriculum Learning approach. We wanted to examine the human-inspired
semantic clustering of the training data and its impact on the model’s
performance.

# What did we work on?
## Data and Modality
News Category Prediction
Around 210k news headlines from 2012 to 2022 from HuffPost.

# How did we approach this?
## Data Orderings
Alphabetic Clustering
● ordering by superclass alphabetically - EXPERIMENTAL
ORDER 1
● ordering by class alphabetically - EXPERIMENTAL ORDER
2

Semantic Clustering
● ordering by class hierarchically; descending number of
texts assigned to one superclass - EXPERIMENTAL
ORDER 3 (the opposite of Curriculum Learning)
● ordering by class hierarchically; ascending number of texts
assigned to one superclass - EXPERIMENTAL ORDER 4
(Curriculum Learning approach)
● ordering by class hierarchically; shuffled within one
superclass- EXPERIMENTAL ORDER 5 (the opposite of
Curriculum Learning)

# How did we build the models?
## Methods and Architecture

Experiments were conducted on 2 different models (below) and with the use
of 5 different Data Ordering and Clustering techniques (above). The
architecture of the models were chosen as the ones used to establish the
performance on the randomly shuffled data. We treat the randomly shuffled
data as a baseline for Model1 and Model2. Model architecture was not the
main focus of our project, although Model2 performed significantly better.

# What did we learn?
## Conclusions
● All the models trained on the experimental data orderings did better than the baseline
models with randomly shuffled training data examples.
● The best performing data ordering (ORDER 4) was semantically clustered within one
superclass and also ordered in the ascending order where the first superclass had the
most number of headlines and the last one - the least number of headlines.
● Second best model was also clustered within one superclass but surprisingly, the data
examples were shuffled within one cluster.
● ORDER 1 had the poorest performance. This data ordering was not clustered
semantically but only alphabetically to group together same news headlines within one
superclass. Semantically clustered data did better than alphabetically ordered.
● Curriculum Learning seems to be the key component to data ordering techniques
bringing best results to the models.
● LSTM and GRU layers improved the performance and helped to process long
sequences and preserve the features of previous input at each time step.
● Further experiments with data ordering and clustering combined with the Curriculum
Learning approach are planned to be conducted to explore the presented phenomenon.
