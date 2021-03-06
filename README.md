## Data-Analysis-Tasks
#### Tasks assessment for Fundamentals of Data Analysis 2020

This repository contains my submission of the four tasks as part of the assessment for the Fundamentals of Data Analysis module. In this README I will briefly explain each of the tasks and the method I used to complete them.

### Task 1: Counts
---
This task involved writing a Python function that takes a list as input and returns a dictionary of the distinct items that appear in the list as keys and the frequency they appear in the list as the values. 
The code used to create this function consists of a for loop containing an if statement. The for loop iterates through each item in the list, and the if statementfirst determines if the item has been encountered before, if so 1 is added to the frequency for that item and if not then its frequency is set to 1.
```
                            freq = {} 
                            for item in lists: 
                                if (item in freq): 
                                    freq[item] += 1
                                else: 
                                    freq[item] = 1
                            return freq
```
Above is the code used for the counts function. The empty 'freq' dictionary must be created first so that when an item is encountered the if statment can add 1 to its frequency and store it in the dictionary wehere it can be called again if the item is encountered in the list again.



### Task 2: Dicerolls
---
The purpose of this task was to write a Python function that simulates rolling $k$ number of die, $n$ times with $k$ and $n$ input as parameters by the user. The function should return a dictionary with the total face value and the frequency with which that value appeared in the set number of rolls. 
A for loop was used to implement this function, which simulated the rolling of the die to the number of times specified by the input parameter. Each time the function looped a number was generated between the max and min possible total face values for the specified number of die. An if statement was used to determine if the number had already been generated before, if so 1 was added to it to keep count of the number of times it appeared and if not it was added to the dictionary and was assigned with the frequency 1.
The dictionay was then sorted and returned cotaining each total face value with the number of times it appeared.


### Task 3: Coin Flip
---
This task involved writing Python code that simulates flipping a coin 100 times, running the code 1000 times to produce 1000 results for the number of times heads landed face up out of the 100 coin flips. Then plot the results showing that they roughly follow a bell-shaped curve. 
The code used to simulalte flipping a coin is show below. An empty list called count is made first to store the values for head (which I made = 1). The for loop runs the code the specified number of times, so here it is 1000. 'rng.binomial' is a NumPy.random function that can be used to simulate flipping a coin as the probability can be set so that there is an equal chance of heads or tails winning. This will produce 100 0's or 1's representing tails or heads. The NumPy function count is then used to count the number of 1s (heads) from the 100 coin flips and saves this number into the list called count.
```
                        count = []
                        for i in range(1000):
                            x = rng.binomial(1, 0.5, 100)  
                            y = np.count_nonzero(x ==1)
                            count.append(y)
```
When the for loop is finished the count list will contain 1000 numbers each representing the number of times heads landed face up out of 100 coin flips. To view this graphically, matplot.lib is used to create a histogram. I follows a rough bell-shaped curve, as expected, with a mean value of 50 sugesting most of the 100 coin flips resulted in 50 heads and 50 tails landing face up.

![CoinFlips](https://user-images.githubusercontent.com/60262898/101989087-e1bd3800-3c95-11eb-9f64-a6356b230a20.png)



### Task 4: Simpson's Paradox
---
The aim of this task was to use NumPy to create data sets that demonstrate Simpson's Paradox. Simpson's Paradox is an occurence in probability and statistics in which a trend that appears in several groups is reversed or disappears when the groups are combined. Simpson's Paradox is not technically a paradox, rather a feature of combined data that is contrary to what you would expect, which emerges when causal inferences are drawn across different levels, i.e. from populations to subgroups. Another way to define the Simpson's Paradox is an event in which the correlation between two variables reverses or disappears when examining combined versus segregated data via a third variable. The third variable is sometimes called a confounding variable and is most often the cxause of the correlation among the variables. 

To demonstrate Simpson's Paradox, four data sets were created that when graphed each showed a positive correlation however when the groups were combined into one large data set, the trend was reversed.

![SimpsonsParadox](https://user-images.githubusercontent.com/60262898/102015089-53a68780-3d51-11eb-9a4c-87dbda76fd58.png)
                    























