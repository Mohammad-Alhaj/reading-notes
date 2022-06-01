# Implementation: Linked Lists

## Big O: Analysis of Algorithm Efficiency

Big O(oh) : used to describe the efficiency of an algorithm or function and
the big o describe the worst case of efficiency an algorighem It specifically looks at the factors `Running Time` and `space Time` the evaluted it's depended to things :

**Running Time**: t's time effecinc /complisity the amount of time of a function need to complete

**space Time** : also known as space efficiency / complexity

* The amount of memory resources a function uses to store data and instructions.

In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:

* Input Size
* Units of Measurement
* Orders of Growth
* Best Case, Worst Case, and Average Case

### **1.Input Size**

whenever the size increas the space time and running time it's increases 
the size like size of the an array We will use the letter **n** to refer to the Input Size value.


### **2.Units of Measurement**

#### In order to ***quantify the Running Time*** in our analysis, we will consider **Three** Measurements of time:



* The time in milliseconds from the start of a function execution until it ends

* he number of operations that are executed , Think of this as the number of lines of code that are executed from start to finish of a function.

* The number of “Basic Operations” that are execute,This is usually the most time consuming operation within the inner most loop.

### In order to ***quantify Memory Space***, we can consider **Four** Sources of Memory Usage during function run-time :

* the amount of space needed to hold the code for the algorithm.
this as the number of bytes require to store the characters .
* The amount of space needed to hold the input data .

* The amount of space needed for the output data .

* The amount of space needed to hold working space during the calculation.
 thats will also include **stack space**  of recursive function calls  … specifically how memory usage scales relatively with the size of the input.

 **It’s also worth noting that contemporary computing affords most machinees with multiple GigaBytes of working memory, so algorithm space complexity is not as much of a concern as it used to be.**

### **3.Orders of Growth**

![](./typical%20orders%20of%20growth.png)

### **4.Worst Case, Best Case, Average Case**

**Worst Case:** The efficiency for the worst possible input of size **n**
Big O(oh): This notation describes the Worst Case

**Best Case:** The efficiency for the best possible input of size **n**
Big Omega: This notation describes the Best Case

**Average Case:** The efficiency for a “typical” or “random” input of size **n**
Big Theta: This notation describes the Average Case



## Review
**Big O:** The worst case analysis of algorithm efficiency.

**Running Time:** The amount of time required for an algorithm to complete.

**Memory Space:** The amount of memory resources required for an algorithm to complete.

**Input Size:** Represented by the variable n, the total size of values used as parameters in an algorithm.

**Big Omega:** The best case analysis of algorithm efficiency.

**Big Theta:** The typical or random case used for analysis of algorithm efficiency.

## resorses 

[To read more](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)


