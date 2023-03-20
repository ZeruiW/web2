---
title: goals-for-xai
tags: XAI
cover: 'https://s2.loli.net/2022/06/07/r4xqhE1luGmToDM.jpg'
abbrlink: 9666
date: 2023-03-03 15:36:46
---

# Goals for Explainable Artificial Intelligence

DARPA’s XAI program [2] describes the XAI goal as a machine learning model combined with XAI methods that should enable the user to understand, appropriately trust, and manage the latest generation of AI models.

We summarized the XAI goals as follows to provide guidance for the XAI process. 

The first group of goals is about model interpretability and transparency. And follows model tuning, selection
and debugging. These goals must be achieved by the XAI methods, which focus on specific models.

- **Algorithmic Transparency. **

>  XAI assists end-users in understanding how the AI system works by achieving algorithmic transparency. It also helps the user to comprehend the model prediction result.

- **Model Interpretability.**

  > AI researchers and experts are concerned about model interpretability. For example, A toolbox [3] visualizes the activation from each layer of trained convolutional neural networks and feature at each layer of deep neural networks.

- **Model Tuning and Selection.**

> AI Practitioners can further tuneand select models after the XAI process is executed.

- **Model Debugging.** 

> Besides the model tuning, AI experts can optimize and debug the model by obtaining explanations.

Then, the following group of goals describe users’ distrust of the AI model. The XAI method can achieve these goals, which provides enough explanation to convince the user. The suitable methods should allow users to assess the model with the test data and obtain results from statistical analysis.

- **User Trust and Reliance.** 

> The XAI methods allow users to test the reliability and accuracy of the AI system. Therefore, the AI model can obtain user trust and reliance by adequate explanation.

- **Bias Mitigation.** 

> Biased and unfair are the significant drawbacks of AI systems. They could come from train data and feature engineering. As AI increasingly uses big data. We think it is becoming harder to detect bias in the dataset manually. XAI methods provide assessment for bias.

- **Privacy Awareness.** 

> Similarly, personal privacy may be entrapped in big data. Privacy can also be detected using the XAI process.

Lastly, data experts use AI models for analysis and research. Visualization can help data experts to understand the model better.

- **Model Visualization and Inspection.** 

> In the field of computer vision, XAI provides the rationale for predictions by highlighting the critical pixels. As an essential application in medical science [4], doctors can use the XAI with the medical image to validate the AI diagnosis prediction.

There are overlaps in the method to achieve these goals. The XAI goals lead XAI processes decisions such as explanation type, scope, and amount of information.

![Goals](https://s2.loli.net/2022/06/07/r4xqhE1luGmToDM.jpg)

[1]

A. B. Arrieta *et al.*, “Explainable Artificial Intelligence (XAI): Concepts, Taxonomies, Opportunities and Challenges toward Responsible AI,” *arXiv:1910.10045 [cs]*, Dec. 2019, Accessed: Mar. 26, 2022. [Online]. Available: http://arxiv.org/abs/1910.10045

[2]

D. Gunning and D. W. Aha, “DARPA’s Explainable Artificial Intelligence Program,” p. 15.

[3]

Jason Yosinski, Jeff Clune, Anh Nguyen, Thomas Fuchs, and Hod Lipson. 2015. Understanding neural networks through deep visualization. arXiv preprint arXiv:1506.06579 (2015).

[4]

BAS van der Velden, Hugo Kuijf, Kenneth Gilhuijs, and Max Viergever. 2021.Explainable artificial intelligence (XAI) in deep learning-based medical image analysis. (07 2021).
