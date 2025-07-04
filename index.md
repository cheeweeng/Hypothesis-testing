---
title: 
---
# Hypothesis-testing  
In this activity, you will explore the data provided and conduct a [hypothesis test](https://github.com/cheeweeng/Hypothesis-testing).  

> * The purpose of this project is to demostrate knowledge of how to conduct a two-sample hypothesis test.  

> * The goal is to apply descriptive statistics and hypothesis testing in Python.  

In the dataset, device is a categorical variable with the labels iPhone and Android.  

In order to perform this analysis, you must turn each label into an integer. The following code assigns a 1 for an iPhone user and a 2 for Android. It assigns this label back to the variable device_new.  

## Mapping text labels with numerical code

![Image](https://github.com/user-attachments/assets/a7a05237-8fee-478f-9e28-63f4c49e8178)
<div></div>

## Explore the relationship between device type and the number of drives  
![Image](https://github.com/user-attachments/assets/08a5c646-c4da-4881-ab0c-06ec161fbc78)
<div></div>

Based on the averages shown, it appears that drivers who use an iPhone device to interact with the application have a higher number of drives on average. However, this difference might arise from random sampling, rather than being a true difference in the number of drives. To assess whether the difference is statistically significant, you can conduct a hypothesis test.  

# Hypothesis Testing
Recall the steps for conducting a hypothesis test:

* State the null hypothesis and the alternative hypothesis  
* Choose a signficance level  
* Find the p-value  
* Reject or fail to reject the null hypothesis  
<strong>Note:</strong> This is a t-test for two independent samples. This is the appropriate test since the two groups are independent (Android users vs. iPhone users).

<strong>𝐻0:</strong> there is no difference between the mean no. of drives btw Android users & iPhone users  
<strong>𝐻𝐴:</strong> there is difference between the mean no. of drives btw Android users & iPhone users

The significant level is set as 5%  
<strong>Technical note:</strong> The default for the argument equal_var in stats.ttest_ind() is True, which assumes population variances are equal. This equal variance assumption might not hold in practice (that is, there is no strong reason to assume that the two groups have the same variance); you can relax this assumption by setting equal_var to False, and stats.ttest_ind() will perform the unequal variances  𝑡 -test (known as Welch's t-test). Refer to the [scipy t-test documentation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html) for more information.

## Two-sample hypothesis test

![Image](https://github.com/user-attachments/assets/836ca1cb-5ac2-40b6-8129-03f064c931b6)
<div></div>

The p-value (0.14) is more than siginificant value 5%, hence fail to reject the null hypothesis.  
In conclusion, there is <strong>not</strong> a statistically significance difference between the mean no. of drives btw Android users & iPhone users.  

Back to [Projects portfolioe](https://cheeweeng.github.io/)
