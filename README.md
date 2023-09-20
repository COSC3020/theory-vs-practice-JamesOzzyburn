[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11859462&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.


## Answers
(1a): Since we remove all of the constants when talking about asymptotic analysis we could have something represented as $\Theta(n)$ which is very quick but in reality its $10000000000 * \Theta(n)$ which is painfully slow.

(1b): We also need to consider how fast the hardware takes to do a iteration. For example if we have something that is $1000 * \Theta(n^2)$ and n is $100$ it may seem very very slow but if the hardware its running on does $1000$ iterations per picosecond its completed in $10$ nanoseconds which is arguably a negligable about of runtime.

(1c): This kinda goes off of (1) but since we also get rid of lower order terms our fast looking search could actually turn out to be terribly long.

(2): I think it would take about $15$ seconds as from what I remember a binary tree search is O(log n) so $1000$ elements at $5$ seconds gives us $200$ elements/second. Then when you take 10,000/1,000 and then put it into log you get three for the ratio so then 5 * 3 is $15$. So then $10,000$ elements takes $15$ seconds.

(3a): It could be a constant.

(3b): It could be a lower order term that is now growing big enough to largely affect the results.

(3c): It could have been the case that the inital time measurement got messed up by the OS doing background tasks so this is the "real" time complexity.
