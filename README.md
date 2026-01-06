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

According to the figure above variables with the biggest impact are:

• Pull back angle
• Tower pin
• Rubber pin

## Design of experiments (DoE)


## Model building
## Result
## Conclusion
## Reference

[1] - When to perform a feature scaling, [Online; accessed 18-June-2023], 2023. [Online].
Available: https://atoti.io/articles/when-to-perform-a-feature-scaling/.
[2] - Pareto Chart, [Online; accessed 18-June-2023], 2023. [Online]. Available: https://asq.
org/quality-resources/pareto.

