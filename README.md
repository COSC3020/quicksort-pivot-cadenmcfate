[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/IF3rQO50)
# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

## Answer

When choosing our pivot to be a median of 3 elements, we ensure that the worst case pivots are avoided: the least and greatest elements. Hence, we have a new equation: Our chosen pivot in this strategy is equally likely to be the $i\text{th}$ smallest for any $i=2,3,...n-1$, so our chances of choosing a pivot from the middle $\frac{n}{2}$ portion of the array are now greater than $\frac{1}{2}$. 

The new probability is $\frac{1}{2}+\frac{2}{n}$ since the chance of choosing the least or greatest element is avoided. Therefore, this method is more likely to pick a good pivot.
