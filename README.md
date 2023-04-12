# MLB-home-attendence-prediction

# Business Problem
<img width="956" alt="image" src="https://user-images.githubusercontent.com/92591719/231561203-4120b213-1cd5-4140-8d75-cb24bd5d05bd.png">

# Solution Map
<img width="812" alt="image" src="https://user-images.githubusercontent.com/92591719/231561421-7c1f9e6c-8370-4ea7-889e-30a48e7faff8.png">

## 1. How to use data to make informed decision for long term strategies
--》**Pre-Season Attendance Prediction Model**

**1. Data Features**
<img width="896" alt="image" src="https://user-images.githubusercontent.com/92591719/231564236-fac767e5-1632-45ec-8683-3ad441535d6d.png">



**2. Model Strategy**

Temporal Fusion Transformer

<img width="524" alt="image" src="https://user-images.githubusercontent.com/92591719/231563045-3a8cd90b-5b0d-44e4-b017-b7ebcfc77beb.png">

advantages:

<img width="354" alt="image" src="https://user-images.githubusercontent.com/92591719/231564403-0609f0f3-b540-42d1-b559-b2745fe3423b.png">

**3. Model Result**

We choose mean absolute percentage error as our key metric. Considering using error like mean absolute error or root mean squared error as measure can be misleading, since for some teams’ mean attendance are relatively lower, which can cause large bias and difference between predicted value and actual value.

To compare our model result, we built a simple linear regression, with MAPE of 35%. And our transformer has a MAPE of 17%, which can provide nearly 20% more accuracy.

<img width="896" alt="image" src="https://user-images.githubusercontent.com/92591719/231565050-b18aba24-dfdb-4ab6-a9a9-a156e0c70660.png">



