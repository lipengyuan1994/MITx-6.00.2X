# Exercise 3 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX

[Source](https://courses.edx.org/courses/course-v1:MITx+6.00.2x+1T2020/courseware/44b64e16aa524037be90cd2aa3552ef6/979cf9747f8d4f759ffac3e756b0842c/?activate_block_id=block-v1%3AMITx%2B6.00.2x%2B1T2020%2Btype%40sequential%2Bblock%40979cf9747f8d4f759ffac3e756b0842c "Permalink to Exercise 3 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX")

1. The following image shows the average low and average high temperature in from the data in [julytemps.txt](https://courses.edx.org/assets/courseware/v1/90561ea2cddec85a90057512d6182415/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/julytemps.txt). 

![vertical bar 1 with top at 95 and bottom at 70 and midpoint at 82 and vertical bar 2 with top at 75 and bottom at 59 and midpoint at 65](https://courses.edx.org/assets/courseware/v1/15569781abd0a10ad2d7cf79ebd001ee/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/temps.png)

  The errorbars represent the 95% confidence interval. The 95% confidence interval for the average high is 83.5 +/- 12.9 and the 95% confidence interval for the average low is 67.2 +/- 7.3. Are these two means statistically significant at the 95% confidence interval?

incorrect

Explanation

The confidence intervals overlap, so no.

2. Are these two means statistically significant at the 99.7% confidence interval?

correct

Explanation

From the first question, you can tell that the standard deviation is about 6.5 (for high temp) and 3.6 (for low temp). The 99.7% confidence interval says that 99.7% of the data falls within 3 standard deviations of the mean. Calculating mean+/-3\*sigma for the high and low temps gives an overlap in the error bars.

3. Are these two means statistically significant at the 68% confidence interval?

correct

Explanation

From the first question, you can tell that the standard deviation is about 6.5 (for high temp) and 3.6 (for low temp). The 68% confidence interval says that 68% of the data falls within one standard deviation of the mean. Calculating mean+/-sigma for the high and low temps does not give an overlap in the error bars.


# Exercise 4 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX

[Source](https://courses.edx.org/courses/course-v1:MITx+6.00.2x+1T2020/courseware/44b64e16aa524037be90cd2aa3552ef6/979cf9747f8d4f759ffac3e756b0842c/?activate_block_id=block-v1%3AMITx%2B6.00.2x%2B1T2020%2Btype%40sequential%2Bblock%40979cf9747f8d4f759ffac3e756b0842c "Permalink to Exercise 4 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX")

Ace, Bree, and Chad are each tasked with finding the standard error for three different problems. Each person only has a sample size of 100 data points for each of their problem. 

Ace: the winning bonus number in the lottery
 Bree: the average women's shoe size
 Chad: the number of mold bacteria on bread over time

1. Which person's sample standard deviation will be the closest to the actual population standard deviation?

correct

2. Which person's sample standard deviation will be the farthest to the actual population standard deviation?

correct

3. Now suppose Chad used a sample size of 10,000 instead of 100 but the other two people still use a sample size of 100. Mark all that are correct.

correct

Explanation

Q1 and Q2: The lottery problem is a uniform distribution. The shoe problem is a normal distribution. The mold problem is an exponential distribution. The skew for the uniform distribution is the smallest and the skew for the exponential distribution is the largest. 

Q3: The more samples you take, you will get closer to the actual population, so the difference in stddevs decreases. Without knowing exactly how to model the curves of the difference in sample stddev and the population stddev, you can't tell how the mold stddev difference behaves relative to the shoe and lottery stddevs.



# Exercise 5 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX

[Source](https://courses.edx.org/courses/course-v1:MITx+6.00.2x+1T2020/courseware/44b64e16aa524037be90cd2aa3552ef6/979cf9747f8d4f759ffac3e756b0842c/?activate_block_id=block-v1%3AMITx%2B6.00.2x%2B1T2020%2Btype%40sequential%2Bblock%40979cf9747f8d4f759ffac3e756b0842c "Permalink to Exercise 5 | Lecture 9 - Sampling and Standard Error | 6.00.2x Courseware | edX")

You are given two data files. Each file contains 1800 data points measuring the heart rate (in beats per minute, every 0.5 seconds) of a subject prforming comparable activities for the duration of 15 minutes: [hr1.txt](https://courses.edx.org/assets/courseware/v1/f9dab9708eb2b15e087d9dc169e1e50f/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/hr1.txt) and [hr2.txt](https://courses.edx.org/assets/courseware/v1/47a3b91c5ff3e2e4a587634e42273ee3/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/hr2.txt). The data is plotted in the figures below. (note that the data is taken from the [MIT-BIH Database](http://ecg.mit.edu/time-series/))

![graph with xaxis label (time sec\*2) and yaxis label (heart rate bpm) and noisy jagged graph around y=90 and from x=0 to x=1750](https://courses.edx.org/assets/courseware/v1/8b08b2af6d18e44ff1c22515cb551ed5/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/ts1.gif)![graph with xaxis label (time sec\*2) and yaxis label (heart rate bpm) and graph with frequency of 100 around y=90 and from x=0 to x=1750](https://courses.edx.org/assets/courseware/v1/c5c4028a1c95f7a4e9fa38916a796ab1/asset-v1:MITx+6.00.2x+1T2020+type@asset+block/ts2.gif)

Using a sample size of 250, decide whether the following methods of drawing samples will yield samples where the examples are independent of each other. 

1. Using `random.sample`

correct

2. Getting a random number between 1 and 1800, 250 times.

correct

This method might get repeat values because it it performing selection with replacement

3. Starting at the first example and going until the 500th example.

correct

Looking at the data in h1, you can see that the samples from 0 to 250 are higher than the examples between 250 and 500. In the hr2 data, the examples occur with a frequency of 125, so taking the first 250 and then the next 250 will give almost the same average but the standard deviation will be different.
