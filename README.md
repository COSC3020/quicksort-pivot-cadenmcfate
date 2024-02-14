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
//Redid probability to not depend on $n$.

//Briefly glanced at previous student repositories to undertand how to go about finding the probability.

Using the suggestion from slide 34, we can divide an array of size $n$ into three chunks: < pivot, good pivot, > pivot, which we can denote as A,B,C, respectively. A accounts for 1/4 of the array, B is 1/2, and C is 1/4. We want to determine the probability of finding an element of B using the median of three strategy. When we are choosing our 3 elements, we can have any possible arrangement of elements from A, B, or C. Finding a bad pivot means our median of three doesn't belong in B. Permutations that would lead to this outcome can be denoted as follows:

AAA, AAC, ACA, ACC, CAA, CAC, CCA, CCC (these each have a probability of $\frac{1}{4^3}$ = 1/64)

AAB, ABA, BAA, CCB, CBC, BCC. (these each have a probability of $\frac{1}{4^2}*\frac{1}{2}$ = 1/32)

Adding it up we get 8/64 + 6/32 = 5/16

The probability of getting a bad pivot is 5/16, so the probability of getting a good pivot is 11/16, or 68.75%.

This is greater than 50%, so the median of three method makes it more likely to select a good pivot.





