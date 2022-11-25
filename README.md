# Explainable-ML

What is 

## Part 1

 
## Part 2- 
Inherently interpretable models
1. Rule based models: 
     Bayesian Rule list: A generative model designed to produce rule list (if-else-if) that strikes a 
balance between accuracy, interpretability and computation. 
2. Risk scores: Assign points to predefined condition of models and sum up as per the case. 
Application: Medicine & criminal justice- How risky it is to release a defendent/approving the loan to a 
requirement: domain expertise

3. Generalized additive models: To interpret how outcome variable changes when input variable changes. 
Picture: courtesy
GAM square: it also includes pairwise dependency of inout variables. 
refer to the video(26:39) to know how to derive this type of model. 
According to me, the interpretability of the GAM/GAM square models are quite debatable when the number of input features are high. 

4. Prototype based models: To identify K prototypes/instances from dataset.
A new instance will be assigned the same label as closest prototype with high probability
each instance will cover some -epsilon neighborhood around it. 
simiar nearest neighbor classifier. 
Prototype layers in Deep learning models

5. Attention based models: 
Attention layers in DL models-

## PART 3: 
Post hoc explanation: How complex models should be faithfully interpretable and understanble by End user. 
Ways to communicate the simplicity of the complex models. 

Local vs Global Explanations
Explain individual prediction vs explain complete behaviour of the model

Approaches for Post hoc explainability:
  for local interpretable methods: 
  *. help unearth biases in the local neighborhood of a given instance
  *. help vet if individual predictions are being made for thr right reason
1. Feature Importance: 
LIME and SHAP method
2. Rule based
Achors: finding the rules to predict theneighborhood
3. Saliency Maps: (Image processing and CV) (What parts of input are more contributing to the prediction)
4. Prototype/example based
5. Counterfactuals

for global explanations
  *. help shed light on big pictures biases affecting larger subgroups
  *. help vet if the model at high level, is suitable for deployemnt
1. Collection of local explanation: SP-LIME(to collect the subsets of k-explanations)& Sp-ANCHOR
2. Representation based (deals how important the human concept is for the neural network)
  TCAV
3. Model distillation
4. Summaries of counterfactuals

## PART 4
Evaluating model interpretations:
1.1 evaluating the meaningfulness or correctness of explanations
1.2 Evaluating the interpretabili of explanations

Challenges of evaluating interpretable models/post hoc explanation methods

Emipirical and theoritically analyzing interpretations/explanations

## Part 5: Future of model understanding

> * Methods for more reliable post hoc explanations: limitations of post hoc explanation are unstable, inconsistent, fragile not faithful. 
> * Challenges with LIME: unstable, consistency (same method run on same point can generate drastically explanation, but only no of perturbation is small.), what if we use large perturbations?  the issue will scalability then. 
>>  Use of BayesLIME & BayesSHAP
> * Theroritical analyiss of the behavious of interpretable models & explanation methods
>> There are various open question roaming around: 
>>> Can we characterize the condition under which each post hoc explanation method successfully/unsucessfully captures the behaviour of the underlying model.
>>> Given the prop of model, data dist ca we theoriticaly determine which explanation method should be employed. 
>>> Can we theoritically analyze the nature of prototype/attention weights learned by deep nets with added layers? when are these meaningful/when are they spurious?
> * empirical evaluation of the correctness & utility of model interpretation/explanation: no clear characterizing of which methods are correct/incorrect under what condition?
   
> * Characterizing similarities and difference between various methods: under what conditions, different post hoc ecplanations methods generate the  similar outputs

> * model understanding beyond classification
>> what about interpretibility of large language models/ RL/GNN/foundation models. 
>> will the explanation be reliable for more complex models

> * intersection with model robustness: Inherently interpretable models with prototype/attentions layers more robust without these layers
   
> * intersction woth model fairness
> * intersetion with model privacy 


One very inetresting question which is usually not very discussed is *What are the new tools, interfaces, benchamarking for end users to understand the model better?*
It is important to make the model understandable to other stakeholders which are not involved in the development of it but are end users of it. They are usually not very familiar with technical terms of ML and AI. 
One solution that Hima has shown at the end of the seminar was a chatbot through which we can explainability of ML can be very easily expressed in sentences. 

