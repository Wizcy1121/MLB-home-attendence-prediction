# MLB-home-attendence-prediction

# Business Problem
<img width="956" alt="image" src="https://user-images.githubusercontent.com/92591719/231561203-4120b213-1cd5-4140-8d75-cb24bd5d05bd.png">

# Solution Map
<img width="812" alt="image" src="https://user-images.githubusercontent.com/92591719/231561421-7c1f9e6c-8370-4ea7-889e-30a48e7faff8.png">

## 1. How to use data to make informed decision for long term strategies
--> **Pre-Season Attendance Prediction Model**

**1. Data Features**

To better predict attendance, we believe thinking in sports fans’ shoes can help us target which factors can be good candidates for the use of prediction, since fans may decide whether or not to attend a specific game after think through those factors. Considering in this perspective, we categorize factors into three categories, including team performance, players, and calendar. 

<img width="896" alt="image" src="https://user-images.githubusercontent.com/92591719/231564236-fac767e5-1632-45ec-8683-3ad441535d6d.png">

**2. Model Strategy**

Temporal Fusion Transformer

<img width="1222" alt="image" src="https://user-images.githubusercontent.com/92591719/231565720-265e771f-b62d-4122-9f3e-f809514ac659.png">

advantages of implement TFT as Pre-Season attendance prdiction model:

<img width="354" alt="image" src="https://user-images.githubusercontent.com/92591719/231564403-0609f0f3-b540-42d1-b559-b2745fe3423b.png">

**3. Model Result**

We choose mean absolute percentage error as our key metric. Considering using error like mean absolute error or root mean squared error as measure can be misleading, since for some teams’ mean attendance are relatively lower, which can cause large bias and difference between predicted value and actual value.

To compare our model result, we built a simple linear regression, with MAPE of 35%. And our transformer has a MAPE of 17%, which can provide nearly 20% more accuracy.

<img width="896" alt="image" src="https://user-images.githubusercontent.com/92591719/231565050-b18aba24-dfdb-4ab6-a9a9-a156e0c70660.png">


## 2. During the season, how can we leverage new data to optimize short-term decisions
--> **In-Season Attendance Prediction Model**

**1. Data Features**

To do that, here we added several new features into each category. For team performance, we have in-season game performance and add previous games’ attendance directly as lag terms; For player, we add average batter and pitcher age as proxies for player popularity and fan base, now that we get the full list of players in new season. For the calendar, we also include NBA, NFL and NHL game schedules. It makes sense that if on the same day, there are multiple sports games, the clash can impact the attendance on each side.

<img width="559" alt="image" src="https://user-images.githubusercontent.com/92591719/231566268-44c9fef0-ddb3-42d0-b854-3b85bf29bbf2.png">

**2. Model Strategy**

LightGBM

<img width="360" alt="image" src="https://user-images.githubusercontent.com/92591719/231566599-c73ade13-82b4-488d-b55b-5961a6593e00.png">

advantages of implement LightGBm as In-Season attendance prdiction model:

<img width="353" alt="image" src="https://user-images.githubusercontent.com/92591719/231566901-ee89c366-d17e-45d8-a140-21d8e64a1cd1.png">

**3. Model Result**

<img width="858" alt="image" src="https://user-images.githubusercontent.com/92591719/231567037-135edeb2-6698-4bbf-a51a-a80b3e96bedc.png">


## 3. Besides attendance number, How can we use Important factors to inform better operational strategies
--> **Interpret Important Factors from Feature Importance Graph**

Following features can be categorized into the following 6 groups of statistics: 

<img width="794" alt="image" src="https://user-images.githubusercontent.com/92591719/231567994-51d5bb4c-1d45-4efe-865c-d70c72376a08.png">

