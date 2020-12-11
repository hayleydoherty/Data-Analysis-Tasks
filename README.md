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