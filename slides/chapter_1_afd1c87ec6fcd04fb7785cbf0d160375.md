---
title: Insert title here
key: afd1c87ec6fcd04fb7785cbf0d160375

---
## Intuitive Introduction to Ensemble Methods

```yaml
type: "TitleSlide"
key: "d072191e9a"
```

`@lower_third`

name: Román de las Heras
title: Data Scientist, SAP / Agile Solutions


`@script`
Welcome to the course of Ensemble Methods in Python!
My name is Román de las Heras and I'll be guiding you through this course. Currently, I work as a Data Scientist at SAP & Agile Solutions, mainly building Machine Learning Models.
Our first lesson is an intuitive introduction to Ensemble Methods.


---
## Choosing the best model

```yaml
type: "FullSlide"
key: "7c6b039180"
```

`@part1`
**Which model is the best?**

![2018-10-29_21-25-00.png](http://assets.datacamp.com/production/repositories/3910/datasets/348f0926077b1654f4ecedbc55de1d949291ca9c/2018-10-29_21-25-00.png){{1}}

_Chosen "best" model: Decision Tree_ {{2}}


`@script`
When you're building a model, you want to choose the one that performs the best according to some evaluation metric. Maybe you have already tried some models and then you compare them based on its score.
For instance, consider this example. Here we trained a Decision Tree, a Logistic Regression, and a K-Nearest Neighbors model. 
If we choose the model based on its accuracy, then Decision Tree would be the best choice, right?
The problem of doing this is that we are discarding the other models, which were able to learn different patterns and have additional useful properties.
What can we do about it?


---
## Surveys

```yaml
type: "TwoColumns"
key: "c2d90d2414"
```

`@part1`
![shutterstock_253684528.jpg](http://assets.datacamp.com/production/repositories/3910/datasets/63a78aa6054adae76c9b99965cc42dee2704d3e4/shutterstock_253684528.jpg){{1}}

- **Categorical:** Mode {{2}}
- **Numerical:**   Mean {{3}}


`@part2`
![2018-10-29_22-54-45.png](http://assets.datacamp.com/production/repositories/3910/datasets/9890b3fec955e5aa509767e3055a95913913fad1/2018-10-29_22-54-45.png) {{4}}


`@script`
Well, let's see an analogous case. When you apply a survey, you don't take only the best answers. Actually, you consider a combined response of all the participants. For the categorical variables, the mode is a good representation. And for the numerical variables, the mean is good to go. Actually, these two metrics are the basis of Ensemble Methods.
With our previous example, we could form a new model by combining the existing ones. In an ideal case, the combined model will have better performance than any of the individual models, or at least, be as good as the best of them.
The main purpose of this course, is for you to learn techniques to ensemble those individual models into a new, final, combined model.


---
## Previous Knolewdge

```yaml
type: "TwoColumns"
key: "4dcf93ac5e"
```

`@part1`
![](https://assets.datacamp.com/production/course_1939/shields/original/shield_image_course_1939_20180618-12-158gfc9?1529338815){{1}}


`@part2`
![](https://assets.datacamp.com/production/course_6199/shields/original/shield_image_course_6199_20180612-12-bwy6g0?1528833207){{2}}


`@script`
I am assuming that you are proficient in Supervised Machine Learning, and also that you know the fundamentals of scikit-learn framework. If that is not the case, then you may want to pay a visit first to these courses available at Datacamp: Supervised Learning in Python and Linear Classifiers in Python are a good base before getting deeper into this course.


---
## Technologies

```yaml
type: "TwoColumns"
key: "c18e1f6ec0"
```

`@part1`
![scikit-learn.jpg](http://scikit-learn.org/stable/_static/scikit-learn-logo-small.png) {{1}}

- scikit-learn {{2}}
- numpy {{3}}
- pandas {{4}}
- matplotlib {{5}}

![mlxtend-logo.png](https://rasbt.github.io/mlxtend/img/logo.png) {{6}}


`@part2`
```
from sklearn.ensemble import 
   MetaEstimator
``` {{7}}

```
# Base estimators
clf1 = Model1()
clf2 = Model2()
...
clfN = ModelN()

# Meta estimator
clf_combined = MetaEstimator(
   estimators=[clf1, clf2, ..., clfN],
   # additional parameters
)

# Train and test
clf_combined.fit(X_train, y_train)

pred = clf_combined.predict(X_test)
``` {{8}}


`@script`
We'll be working with scikit-learn as our primary Machine Learning framework, and we will also support on the additional libraries which you already might know: numpy, pandas, matplotlib, ...
In addition, you'll be introduced to a useful Python library for Machine Learning called Mlxtend.
The main module we'll be using from scikit-learn is the scikit-learn.ensemble. You'll notice how we will import one of the meta estimators from that module. Then, we'll build the individual models, which will serve as input parameters for the combined model. The good thing is that this meta estimator will work as the estimators which you already handle, with the standard methods of fit, predict, transform, ...


---
## Learners, ensemble!

```yaml
type: "FinalSlide"
key: "94303c5d88"
```

`@script`
Well, let's start to practice!
Learners, ensemble!

