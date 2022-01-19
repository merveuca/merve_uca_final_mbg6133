# merve_uca_final_mbg6133

First of all, needed libraries have been called by using the followings:
Import numpy as np
Import matplotlib.pylab as plt
Import seaborn as sns
In order to obtain my plots in poster format, I called seaborn library and used it set_context attribution. sns.set_context('poster').

Question 1
1= To create an array with the [0,100] interval and in the 100x100 size that consists of random integers, I’ve used  the following: 
random_array= np.random.randint(0,101, size=(100,100))
Since we want to include 100,  I wrote the interval as 0,101 as the last number in that case 101 is not included in python. After creating the array, I called it as random_array.
I want to see my array that’s why in an empty cell, I just wrote down random_array and run it, I saw my array, Later on, to control its size I wrote random_array.shape and saw that my array is in correct size that is (100,100) means 100 rows and 100 columns
2= Then to create a heatmap of it I used seaborn library like this:
fig,ax = plt.subplots(figsize=(20,20))
The above command is setting up the scale of the figure.
sns.heatmap(random_array)
plt.show()
After calling sns.heatmap, in paranthesis I wrote the name of the array that I want to obtain its heatmap. Then to eliminate, the line shows up above the figure that is <matplotlib.axes._subplots.AxesSubplot at 0x19aab0a3b20>  
I wrote plt.show() and run the whole cell then obtained the heatmap.  It is one of the ways to visualize data in a color encoded matrix.  The color bar on the right shows the intensity of the numbers exist in the array. This heatmap has a lot of color inside of it since the array created it lying in a long interval that is [0,100]. As can be seen in the color bar the the bigger number the lightest color as goes from 0 to 100.
Question 2
1= If a number is divided by 2 and gave a remainder of 0 then the number is known as even number, otherwise  it is an odd number. So to filter out odd numbers I used the condition random_array % 2 != 0. Since it is a Boolean condition, it gave me true and false, If a number obeys my condition (if the number is divided by 2 and is not giving 0) means it is odd, the result is true. If a number doesn’t obey my condition means it is even, the result is false. There exists 2 ways of converting true/false statement to 0,1.  One is assigning a new name to the condition and multiplying each element of the array with 1 gives 0,1. I obtained the result by following :

a = random_array % 2 != 0
x = np.multiply(a, 1)
print(x)
The second and the easiest way to changing the type of newly named array to integer by using   a.astype(int). When it runs it gave 0 and 1 only.
2= Lastly to plot it as heatmap, I again used seaborn library where x is the name of new array that I created in the first way of the solution. The heatmap has only  the lightest and darkest color that belongs to 0 and 1 as can be seen at the color bar. Since the array has only 2 values (0,1) it is logical to have such kind of a heatmap.
fig,ax = plt.subplots(figsize=(20,20)) # to set the figure size	
sns.heatmap(x) # to obtain heatmap
plt.show()

