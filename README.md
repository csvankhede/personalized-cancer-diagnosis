# personalized cancer diagnosis
![bg-masthead](https://user-images.githubusercontent.com/25454660/62774311-feee5f00-bac1-11e9-887d-77f776c8c6b9.jpg)

Case study of personalized cancer diagnosis

### Description
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/

Data: Memorial Sloan Kettering Cancer Center (MSKCC)

Download training_variants.zip and training_text.zip from Kaggle.

Context:
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462

### Data Overview
* Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
* We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.
* Both these data files are have a common column called ID
* Data file's information:

  * training_variants (ID , Gene, Variations, Class)
  * training_text (ID, Text)

### Problem statement :
Classify the given genetic variations/mutations based on evidence from text-based clinical literature.

### Type of Machine Learning Problem
There are nine different classes a genetic mutation can be classified into => Multi class classification problem

### Results 

<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th>Model</th>
      <th>Train log loss</th>
      <th>cv log loss</th>
      <th>Test log loss</th>
      <th>% of miss classified points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10</th>
      <td>Logistic regression(after feature engineering)</td>
      <td>0.408338</td>
      <td>0.929123</td>
      <td>0.982035</td>
      <td>33.08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Logistic Regression(with balancing)(onehot)</td>
      <td>0.555892</td>
      <td>1.066875</td>
      <td>1.059586</td>
      <td>34.58</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Logistic Regression(without balancing)(onehot)</td>
      <td>0.553413</td>
      <td>1.084771</td>
      <td>1.080800</td>
      <td>35.90</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Linear SVM(with balancing)(onehot)</td>
      <td>0.789318</td>
      <td>1.157685</td>
      <td>1.188844</td>
      <td>35.90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Maximum Voting classifier(LR,SVM,RF)(onehot)</td>
      <td>0.936042</td>
      <td>1.237586</td>
      <td>1.235425</td>
      <td>38.19</td>
    </tr>
    <tr>
      <th>1</th>
      <td>KNN</td>
      <td>0.477219</td>
      <td>1.103969</td>
      <td>1.138304</td>
      <td>38.34</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Logistic regression(unigrams and bigrams)</td>
      <td>0.851810</td>
      <td>1.175451</td>
      <td>1.203757</td>
      <td>38.72</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Stacking (NB,SVM,LR)(onehot)</td>
      <td>0.806473</td>
      <td>1.213838</td>
      <td>1.191858</td>
      <td>38.94</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Naive Bayes(onehot)</td>
      <td>0.739496</td>
      <td>1.254597</td>
      <td>1.237384</td>
      <td>42.85</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Random Forest Classifier(onehot)</td>
      <td>0.843210</td>
      <td>1.208020</td>
      <td>1.254444</td>
      <td>44.36</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Random Forest Classifier(response coding)</td>
      <td>0.069349</td>
      <td>1.412670</td>
      <td>1.402561</td>
      <td>47.93</td>
    </tr>
  </tbody>
</table>
