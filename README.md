//BITONIC SORT IN C++(DESCENDING ORDER)

  % OVERVIEW %
-This program implements the Bitonic Sort algorithm which is a comparrison-Based algorithm mainly used in parallel processing systems.The bitonic algorithm works by sorting a sequence that is bitonic.

   % OBJECTIVES %
- Implement a sorting algorithm manually (Bitonic Sort)
- Sort integers in **descending order**
- Count and display **comparisons and swaps**
- Analyze algorithm efficiency

    %HOW THE PROGRAM WORKS %
  
   //Bitonic Sort works by:
1. Dividing the list into two halves
2. Sorting:
   - First half in **ascending order**
   - Second half in **descending order**
3. Combining them into a **bitonic sequence**
4. Repeatedly comparing and swapping elements to produce a fully sorted list.

NB-Bitonic Sort works best when the number of elements (n) is a power of 2.

*For non-power-of-2 inputs:
     -The array may need to be padded
     -Performance may not be optimal

     
The program keeps track of the number of comparisons and swaps performed during execution. A comparison is counted each time two elements are compared, while a swap is counted each time two elements exchange positions. These metrics help in analyzing the efficiency of the sorting algorithm.For instance;

-Sorted array (Descending):
8 7 4 3

Total Comparisons: 6
Total Swaps: 2


%---Step-by-Step Demonstration of Bitonic Sort (Descending)---%

             sample list:
                -[3, 7, 4, 8]

            step1
            -split into two halves
                 >[3,7]
                 >[4,8]
             step2
             -[3, 7]->already ascending

             step4
             -[4, 8]->descending->[8,4]

             step4
             -combine both halves:
               [3, 7, 8, 4]
               
             Step 5: First Compare and Swap

             - Compare elements at distance k = n/2 = 2:

             -Compare 3 and 8 → correct (no swap)

             -Compare 7 and 4 → swap
              → [3, 4, 8, 7]
              
           Step 6: Recursively Merge First Half
                 [3, 4] → descending → [4, 3] 
                 
            Step 7: Recursively Merge Second Half
                  [8, 7] → already descending    
            Final Result

           Combine:
             [8, 7, 4, 3]     

            
                TIME COMPLEXITY AND SPACE COMPLEXITY
   -Bitonic Sort is a divide-and-conquer algorithm. 
   -Its recursive nature guarantees that every element is compared at each merge stage, regardless of input order. Hence, all    cases (best, average, worst) take    O(n log² n) time.
   -Space complexity is O(log n) due to recursion stack usage, and no extra  memory is used for storing elements since the        algorithm works in-place.
     

   
