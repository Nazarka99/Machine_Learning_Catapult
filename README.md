## Project everview

The goal is to accurately predict the launch distance of the catapult with minimal deviation. This precision will enable the catapult to consistently hit a target, such as a small basket. The challenge lies in gathering the necessary variables to create a prediction model that delivers a high degree of accuracy.

<img width="1536" height="1024" alt="catapult setting" src="https://github.com/user-attachments/assets/fdbabd2b-8383-475f-9769-5c7736d34d09" />

## Data collection

Several adjustable variables for the catapult, including the stop pin, tower pin, rubber band attachment, and cup position. Initially, these variables will be roughly examined for their deviation and impact. Based on this preliminary analysis, 2-3 variables that have the greatest impact will be selected.

## Preliminary analysis
### Identification of High Impact Variables

The following approach is taken to collect the most impactful variables:
1. Gather data set with all possible impact variables.
2. Scale each input variable, the approach selected to scale variables is scaling to unit length.
Where the variables are compared by dividing the variable coefficient by the Euclidean length
of the vector [1].
3. Make an equation for the data from the data set collected.
4. Make the Pareto-plot, regarding each coefficient [2].
5. Two to three variables with the biggest absolute value are then identified. These variables
are considered the most impactful variables in the process.

![pareto](https://github.com/Nazarka99/Machine_Learning_Catapult/assets/77903394/16507832-a817-44e0-bbda-5ed5aa857e98)

## Design of experiments (DoE)

According to the figure above variables with the biggest impact are:

- Pull back angle
- Tower pin
- Rubber pin

There were three variations in each variable: lowest, medium, and the highest. For the Full Factorial Experiment, there should be:
3 in power of 3 = 27 (experiments). a large amount of experiments is required to gather the data for the investigation of variables required to hit a specific target in distance. Since time is the most essential factor, a fractional factorial design is utilized to assure that time is spent effectively. 

According to the amount of experiments, the amount of runs were calculated, from which it is possible to predict with precise accuracy the missing rows, that if needed would be possible to check. The amount of experiments decreased to 18 runs. Additionally, in a real manufacturing process, running the full experiment will cause can a higher economic burden when the result of the experiment is not predetermined to be successful.

## Result

In the initial setting, the catapult was fixed to the table using two clamps, in such a way that the side of the catapult opposite to the shooting direction was flush with the edge of the table. The starting point of the ruler was also placed at the edge of the table. The table tennis ball was used because it was intuitively thought to be the most consistent in terms of hitting a set target. For the same reason, the green rubber band was used, because it was thought that it felt looser than the other rubber bands, and therefore it would be less sensitive to small variations caused by the operator. The operator was choosing the pullback angle simply by looking at the angle scale on the catapult.

In order to improve from the initial performance figures in terms of consistently hitting desired targets, some measures needed to be taken. The A3 problem-solving method is used. Which is a well-known systematic and science-based problem-solving method, developed by Toyota Motor Corporation. completely or change the sentence to: It is a step-by-step method that allows a possibility to completely remove problems from a process.

A summarized example of applying the A3 problem-solving method to the optimization of the catapult:

First, the problem was identified: The current error in shooting the ball was far too big to consistently hit the specified target, a basket with an outer diameter of 210 millimeters. Next, it was decided that the goal should be that 95 percent of the fired shots should hit the target. A brainstorming session was held, where several potential causes of the big error were listed, and it was concluded that the human error in repeating the same pullback angle for each shot was deemed the biggest cause of the error. Next, a root cause analysis was done.

Why was the pull-back angle different each time? Because the arrow on the catapult's arm pointing at the scale was relatively far away from the scale and therefore hard to read.

So only after asking "why?" once, it didn't make sense to go further with the "5 times why?" methodology used in A3 problem-solving. So, a countermeasure needed to be developed. It was thought that the most promising countermeasure would be the solid angles that would help the operator to constantly fix the pull-back angle. After making the solid angles and testing them out, this was seen as a functioning solution, and it was added as a permanent part of the Standard Operating Procedure of the catapult.

## Final prediction model

the variables for predictions are (While set label of the variable is written in bracket):

1. tower pin (A)
3. pull back angle (B)
4. rubber pin (C)

After trying a few times, a polynomial regression power of 2 was picked.

<img width="1075" height="219" alt="image" src="https://github.com/user-attachments/assets/42dabdc3-6605-4c26-845d-5610cf1da4dc" />

The model, equation is above, was trained with the data set stated in Table:

<img width="462" height="183" alt="image" src="https://github.com/user-attachments/assets/05c8ff52-7f63-484f-a8fa-de810be3b09b" />

## Conclusion

### Relevance of Results to the Target
During the great shoot-off, three different targets were given to us within our range (1-4 meters) categorized by short, medium, and long distance. A 3D-printed basket with a 210-millimeter outer diameter was used for the purpose of the experiment which was placed at the desired distance (target distance). The ball must hit the inside or outside wall of the basket in order to be counted.
A small tennis ball and a red rubber band were selected based on the previous experiments used to investigate the optimal setup for the shoot-off. The range of the angle was chosen by using the observed outcomes in the previous experiments that landed the ball close to the target. The final shooting result is consistently able to hit the basket with 100 % accuracy, although there were some struggles with the long-range shooting of 380 centimeters but by the third try the shot hit 90\%\ of the target of 100 %. 

### Future Implications and Recommendations

In this catapult experiment, three variables (tower pin, stop pin, and pull-back angle) were considered although the catapult itself had five variables, because these three variables were found the most impactful in terms of the performance of the catapult experiment. So, it is recommended to explore the experiment by investigating all the variables or factors that may have an impact on the performance of the catapult, in order to find further possibilities of optimization, if the budget allows. It is also recommended to explore alternative release mechanisms and use different rubber bands with different elasticity in order to understand the behavior of the catapult and to investigate its design optimization. One form of risk mitigation could also be to have backups of the rubber bands, since they are the parts that are believed to have the highest risk of breaking, especially if much of the shooting is done from close to the maximum pull back angle.


## Reference

[1] - When to perform a feature scaling, [Online; accessed 18-June-2023], 2023. [Online].
Available: https://atoti.io/articles/when-to-perform-a-feature-scaling/.
[2] - Pareto Chart, [Online; accessed 18-June-2023], 2023. [Online]. Available: https://asq.
org/quality-resources/pareto.

