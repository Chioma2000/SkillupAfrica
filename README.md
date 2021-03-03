# SkillupAfrica

Simply put, polymorphism gives a way to use a class exactly like its parent so there’s no confusion with mixing types. But each child class keeps its own methods as they are.

This typically happens by defining a (parent) interface to be reused. It outlines a bunch of common methods. Then, each child class implements its own version of these methods.

Any time a collection (such as a list) or a method expects an instance of the parent (where common methods are outlined), the language takes care of evaluating the right implementation of the common method — regardless of which child is passed.


Algorithm Assignment

Given an array with integers of length 6. Write a bubble sort algorithm to arrange the integers from smallest to largest.

<?php  
// PHP program for implementation of Bubble Sort 
  
function bubbleSort(&$arr) 
{ 
    $n = sizeof($arr); 
  
    // Traverse through all array elements 
    for($i = 0; $i < $n; $i++)  
    { 
        // Last i elements are already in place 
        for ($j = 0; $j < $n - $i - 1; $j++)  
        { 
            // traverse the array from 0 to n-i-1 
            // Swap if the element found is greater 
            // than the next element 
            if ($arr[$j] > $arr[$j+1]) 
            { 
                $t = $arr[$j]; 
                $arr[$j] = $arr[$j+1]; 
                $arr[$j+1] = $t; 
            } 
        } 
    } 
} 
  
// Driver code to test above 
$arr = array(6, 5, 4, 3, 2, 1); 
  
$len = sizeof($arr); 
bubbleSort($arr); 
  
echo "Sorted array : \n"; 
  
for ($i = 0; $i < $len; $i++) 
    echo $arr[$i]." ";  
   
?> 

Output:
Sorted array:
1 2 3 4 5 6

