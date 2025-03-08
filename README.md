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


Well when the Left most Element is the pivot, it has an equal probability of being any one of the the elements in the subarray. If a good pivot means that it is one that falls within the middle 3rd of the sorted order.
THen the chance would be $\frac{n/3}{n}$ --> $\frac{1}{3}$, n is the ammount of elements in the subarray.

For the Median of three version,a good pivot is one that splits the array into two pieces and neither piece is larger than $\frac{3n}{4}$. By choosing just one element we have a probibility of 50% of choosing a good pivot.
There are three pivots and each chould either be a good or bad one, we can represent these as $2^3 = 8$.
GGG, 3g 0b| (1/8) 
GGB, 2g 1b| [1/8]
GBG, 2g 1b| [1/8]
GBB, 1g 2b| {1/8}
BGG, 2g 1b| [1/8]
BGB, 1g 2b| {1/8}
BBG, 1g 2b| {1/8}
BBB, 0g 3b| -1/8-

so we have 1/8 chance for 3 goods and 3 bads, and a 3/8 chace for 2 goods 1 bad and 2 bad 1 good.
we can calculate the probability of a good pivot like this:
$$(\frac{1}{8} \times 1) + (\frac{3}{8} \times 1) + (\frac{3}{8} \times .5) + (\frac{1}{8} \times 0) = \frac{11}{16} = 68.75%$$
The last 1/8 is multiplied by 0 because its always going to be a bad pivot.
The first 3/8 is multiplied by 1 because while there is a bad pivot option the median of it will make even the bad option a good one.
The 2nd 3/8 is multipled by .5 because if the bad pivots are on opposite sides the median will be good but other wise it wont.

68.75% is my final answer for this portion.

I was present while Gage Hepworth described part of his solution infront of everyone.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.