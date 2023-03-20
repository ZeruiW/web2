---
title: >-
  Checking out the Taxonomy is a key starting step to implementing Explainable
  Artificial Intelligence
tags: XAI
cover: 'https://s2.loli.net/2022/06/06/kebDyN2a8dj4Icv.jpg'
abbrlink: 14953
date: 2023-01-15 15:22:46
---




# Checking out the Taxonomy is a key starting step to implementing Explainable Artificial Intelligence



## What is XAI?

As black-box Machine Learning (ML) models are increasingly being employed to make important predictions in critical contexts, the demand for transparency is increasing from the various stakeholders in AI.

In order to avoid limiting the effectiveness of the current generation of AI systems, eXplainable AI (XAI) proposes creating a suite of ML techniques that:

- produce more explainable models while maintaining a high level of learning performance.
- enable humans to understand, appropriately trust, and effectively manage the emerging generation of artificially intelligent partners.



## What can we expected form XAI?

The XAI goals has been discussed in [the post](https://zeruiw.github.io/post/64804.html) . XAI methods should enable the user to understand, appropriately trust, and manage the latest generation of AI models.



## Why  the taxonomy is a necessary starting step?

Many XAI methods focus on solving particular questions or attributes of the explainability of the specific type of model. With the diversities of XAI methods, the decision to select an XAI method and the following up development with the XAI method with the model evaluation is beyond a single task but involves a complete process. Driving by such motivation, we consider researching the existing XAI methods, categorizing those methods, identifying what can be the goals of XAI, and seeking evaluation of the XAI project. And we further construct an XAI process that can handle most of the XAI projects.



![XAI taxonomy](https://s2.loli.net/2022/06/06/kebDyN2a8dj4Icv.jpg)

Each XAI method has a purpose and its functionality is suitable for certain AI models. An XAI goal of AI models is mostly achievable by more than one XAI methods. Therefore the understanding of commonalities and discrepancy of XAI methods is essential to drive a XAP process that is oriented by XAI goals.  In this section, we present a taxonomy of XAI methods to guide the definition of a general purpose XAI process.   



## Structure of the Taxonomy

The taxonomy has a tree-based topology to structure the levels of categories. The overall taxonomy is shown in Figure. 

The taxonomy was first expressed based on the distinction between **interpretability and explainability**. Besides building interpretable models, **the Post-hoc methods** provide explanations of the AI model. Then, a review [1] focuses on local and global scope classification in this step. Considering model selection for the process, we check the relationships between the methods and the models instead.

**The Model-Specific methods** utilize the model properties and take advantage for provide explanations. Hence, these methods are applied to specific models and are not generic. The further diversity is mainly according to the type of model.

**The Model-Agnostic methods** provide explanations from three aspects: Feature Importance, Visualization, and Simplification. They offer different approaches and goals. Furthermore, we propose and categorize feature masking and feature mutation methods based on the strategies used for the Feature Importance explanation. We also investigated and summarized other methods, shown in Figure, into Rule-based Learner and Additional Interpretable Models, which explain the AI models by simplifying.



## Definition of the Categories

The taxonomy summarizes the XAI technologies we have investigated. The category can also add new methods developed in the future. As a contribution, this study provides the basis for method selection and helps AI practitioners clarify the XAI methods for processing. Therefore, the taxonomy appropriately answers the first research question. What follows are the described definitions for the branch of the taxonomy.

### Build Interpretable Models.

The interpretable model is an AI model built with a relatively simple and interpretable structure.
The machine learning model such as Linear regression, Logistic regression, Decision trees and Decision rules are commonly used.

A study from [2] argues that algorithms with better interpretability have a limitation on performance, for there is a between interpretability and model performance. The human can understand these models during data preparation and training. More precisely, humans can give the exact predictions of the model based on the sample. 

However, this is a trade-off between interpretability and model performance. These models do not perform well in complicated situations. With the development of deep learning, the model becomes more and more complicated and contains billions of parameters. An interpretable model cannot be an alternative [3]. Then, the Post-hoc explanation method is the solution.

### Post hoc Explanation Methods.

Post-hoc explanation methods indicate the techniques that explain the model with independent algorithms or AI models. Models such as Deep Neural Networks are not interpretable as no one can have a picture of their inner structure. With post-hoc methods, people can still explain why the models make such predictions.

Post-hoc explanation methods can mainly divide into two groups: **model-specific** and **model-agnostic**.

#### Model-Specific Methods.

Model-Specific Methods means the XAI approach is only working on the specific type of methods. 

Those methods attend to using the property of the underlying algorithm of the model. Hence, it can not be generalized to other models.

Model-Specific Methods are designed with the specific properties of the machine learning model.

#### Model-Agnostic Methods.

Meanwhile, Model-Agnostic methods show wide application.

Model-Agnostic methods focused on the model's input and output instead of the model itself. They are applicable in most cases, even for the black-box model.

Under this classification, we further the XAI methods by how they present the explanations. Here, many explanations are achieved by visualization; building a simplified explanation model; or illustrating feature importance.

##### Explain by Feature Importance.

This classification indicates methods that explain the influence of the features for prediction based on the feature masking method or feature mutation method.

##### Explain by Visualization.

This classification indicates methods that can provide charts that help humans understand the model.

##### Explain by Simplification.

Explain by simplification means training a new simple or interpretable model to describe the complex black-box model.

###### Feature Masking.

Feature masking methods remove the input feature or set the element to the default value. The idea is to observe how the model predicts with the masked information.

###### Feature Mutation.

Feature mutation methods assign the other value from the dataset to the input feature and show how the individual prediction changes during the data variation.

###### Rule-based Learner.

Decision sets are sets of classification rules. Rule-based models are initially developed as decision rules that explain how they arrive at a particular prediction. By understanding the branches of these decisions, humans can understand the reasons for the predictions.

###### Additional Interpretable Model.

Additional interpretable model methods can explain the classification model locally by learning other interpretable models.

Some particular methods that work on specific case models or requirements may not appear in this taxonomy. New methods can be developed and added to the taxonomy in the future.

XAI Taxonomy

https://drive.google.com/file/d/18jg52s2P0s9aCQxRqd5koHFMYpYfmpxI/view?usp=sharing


Reference:

[1]

Marcinkevičs, Ričards, and Julia E. Vogt. "Interpretability and explainability: A machine learning zoo mini-tour." *arXiv preprint arXiv:2012.01805* (2020).

[2]

Mohseni, Sina, Niloofar Zarei, and Eric D. Ragan. "A multidisciplinary survey and framework for design and evaluation of explainable AI systems." *ACM Transactions on Interactive Intelligent Systems (TiiS)* 11.3-4 (2021): 1-45.

[3]

Ribeiro, Marco Tulio, Sameer Singh, and Carlos Guestrin. "" Why should i trust you?" Explaining the predictions of any classifier." *Proceedings of the 22nd ACM SIGKDD international conference on knowledge discovery and data mining*. 2016.