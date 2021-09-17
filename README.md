# CS 4420/6422 Lab 1: External Sort
## Implementation Details
In this mini project, I implement the External Sort algorithm based on two steps:
* Diveded the input file into k files while ```k=std::ceil(input.size()/mem_size) ``` then use ```std::sort ``` to sort the numbers in each file
* The next step is the k-way merge, which use a ```std::priority queue``` to build a heap from the first number in each file. Then the top in the queue is written in the output file. I also use the  ```std::pair``` to keep track of which file has already been processed and then determine the next number to read from this file or the other one. 

## Missing parts
In this project, I do not implement the iterative two-way merge algorithm as this project assume that ```mem_size>k*sizeof(uint64_t)```. I will try to implement the two-way merge algorithm later to try on self-generated test cases if possible.  
