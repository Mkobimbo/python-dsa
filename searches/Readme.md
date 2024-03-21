Given a sorted array of n elements, write a function to search for the index of a given element (target)

Approach

-Search for the array by dividing the array in half repeatedly.
-Initially consider the actual array and pick the element at the middle index
-Keep a lower index i.e. 0 and higher index i.e. length of array
-If it is equal to the target element then return the index
-Else if it is greater than the target element then consider only the left half of array. (lower index = 0, higher = middle - 1)
-Else if it is less than the target element then consider only the right half of array. (lower index = middle + 1, higher = length of array)
-Return -(insertion index + 1) if the target element is not found in the array (If the lower index is greater than or equal to higher index). Some simpler implementations just return -1 if the element is not found. The offset of 1 must be added as the insertion index might be 0 (the searched value might be smaller than all elements in the array). As indexing starts at 0, this must be distinguishable from the case where the target element has the index 0.