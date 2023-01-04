# Summer_of_Bitcoin2021
Summer of Bitcoin code challenge 2021- Maximizing profit to a Bitcoin Miner


# Motivation behind the project:

My motivation for working on this project was to put my knowledge to use and solve a real-world problem. This project was requested as part of the Summer of Bitcoin 2021 challenge, with the problem statement being to select optimal transactions that produce the greatest profit for a bitcoin miner.


# Project Explanation:
This project is based on a real-world problem that a bitcoin miner faces. A Bitcoin miner's job is to create blocks by selecting a set of transactions from their mempool. Each transaction in the mempool now has a fee attached to it, which is collected by the miner if the transaction is included in the block.
In addition, each transaction has a weight that indicates the size of the transaction. Furthermore, it is possible that a transaction contains two or more parent transactions, which means that before accepting a specific transaction, it is necessary to accept all of its parent transactions.

A miner's job now is to select an ordered list of transactions with a combined weight less than the maximum block weight and that also satisfy the parent child constraint.
Naturally, every miner wants to maximise his or her total fee.

So, my job here was to analyse the transactions and create an ordered list of transactions that meet the constraints and maximise the miner's profit.
 
# Challenges faced:

This was a heuristic problem in which the goal was to optimise more and more in order to get as close to the perfect answer as possible.
The min cut max flow algorithm, on the other hand, can find a perfect solution to the problem.
However, due to the time complexity of the min cut max flow algorithm, it cannot be applied to large data sets with transaction ids in excess of 5000. As a result, it was difficult to come close to a perfect solution without using the min cut max flow algorithm. 


# Further Improvement: 

I intend to understand and learn the min cut max flow algorithm, as well as prune the cases further to optimise time and produce an even better answer.

# How does my algorithm work?

Firstly, I was given a CSV file and I extracted the information using File handling and then applied two algorithms to optimize the result.

Initially I started with a Bit Masking technique to iterate over all possible combinations and find the maximum profit to a miner satisfying the constraints. However, it can only be used on a small dataset containing close to 15 transaction ids.

Then to work on a large dataset I applied a knapsack algorithm for implementation of a greedy based technique starting with sorting the transactions in the order of fee/weight  and further implementing a heap based structure for checking the existence of parents in the block. 

# Results of Bit Masking technique:
Transaction count: 15
Total fees in current block: 3,548
Total Weight: 11,952
Transactions in final block: 9

# Results of Knapsack technique:
Transaction count: 5,214
Total fees in current block: 56,96,031
Total Weight: 39,99,936
Transactions in final block: 3,174
