# Data Visualization with D3.js Final Project 
by Darui Zhang
## Summary 
In the tragic sinking of the Titanic, 68% of the passengers on board perished. However, there is a large difference in the chance of survival across passenger class as well as in gender and whether one and a child. This visualization aims to emphasis the difference survival chance across categories, so that the viewers can compare it easily. Moreover, interactive chart allows the viewers to explore the category of interest on their own.

## Design 
Objective:
The story in the visual is how the chance of survival varies across different passenger class and between children women and men. The data I want to encode in the charts includes passenger class, gender, whether they are children,  whether they survived or perished in this catastrophe.

Data Cleaning:
The original data is already cleaned. I only need to identify when a passenger is a child by looking at if the age is less than 18.

Chart Selections:
Bar chart is easy to understand and good for comparison. So a bar chart is used to show the differences across the passenger class. 
Stacked bar chart uses color to encode the category of data. I use it to present whether one was survived or perished.
Stacked 100% bar chart are used to show the comparison of the chance of survival.
Interaction is used to one more dimension, the category of data aggregated by gender and whether one is a child.


### Visual Encoding:
*x position: passenger class.
*y position: the counts or the percentage of passenger. 
color hue: survived or perished.
additional: interactive chart is used to show data aggregated by gender and whether a passenger is a child.

Library Selecting
dimple.js is the primary visual library used in creating this chart. One of the advantages of dimple.js is that it is very easy to create visuals in terms of lines of code need to write. The other advantage is that it has the feature of showing data values when mouse is moved on a chart. 
d3 is also used in this project. compare to dimple.js it is at lower level of abstraction. So it is not as efficient as dimple when creating charts, but it has more flexibility. 

## Design Changes
The initial chart uses the margarita glasses storytelling structure. An animation of the survival chance between each category is show as first. Then, at the second stage, viewers can explore the data more by choosing with the category to show.
From the feedback, I learned that animation is could be confusing and hard to follow. People need different time to perceive and absorb the information presented in the chart. So in the final version, the animation part is removed. The viewers will start with a chart shows the data of “All Passenger” he can further interact with chart through the buttons to explore the data of different categories, such as “Children”,”Women” and “Men”.
Another change is adding a feature showing the data in percentage. Viewers can look at the stacked bar chart to see the count  and use the stacked 100% column chart to compare the survival rate.
The color and the order of axis are keep consistent over different charts. Lighter color are used to encode people, survive,  darker color for people perished.

## Feedback
Feedbacks are collected through in person interview and the suggestion for improvements are considered in the final chart.

Feedback 1
The categories on the x axis is not consistent. The order varies between different charts. It is confusing and could be misleading.
Similarly, the colors that represent “survived” and “perished” are also not consistent. In some charts red represents “survived” and others it represents “perished”. It can be confusing for the viewers.
Feedback 2
It would be better to have charts show percentage. So when people want to compare survival chance across different categories, they can easily see it through a percentage chart.
The animation is hard to follow. Besides the information present in the animation is the same as in the interactive chart. so just the interactive chart would be good enough, the viewers can explore the data by themselves.
Feedback 3
The animation is too fast. viewers don’t have enough time to absorb the information.  
The color chosen to represent “survived” and “perished” is not straightforward. One need to look at the legend to know which category it stands. A better way is to use more scales darker hue to represent people perished and lighter hue to represent people survived, so that people can easily associate the color and the category.

## Resources 
Titanic data set: https://www.kaggle.com/c/titanic-gettingStarted
dimple js examples: http://dimplejs.org/examples_index.html
RGB color chart:  http://www.rapidtables.com/web/color/RGB_Color.htm
