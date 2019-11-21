# Count of positives / sum of negatives

## Problem 

Create a function that takes an array of integers as an argument and returns an array, where the first element is the count of positive numbers and the second element is sum of negative numbers.

---
## Example

Input: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15].

Output: [10, -65].


//Solution 

function integers(numbers){
  let sum =0;
  for(i = 0; i < numbers.length; i++){
    if(numbers[i] > 0){
      console.log(numbers[i]);
    }else{
         sum += numbers[i];
         //console.log(sum);
    }
  }
  return sum;
}

console.log(integers([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]));




---
## Bonus
If the input array is empty or null, return an empty array.

//Solution 
function integers(numbers){
  
  let sum = 0;
  var res = [];
var r = 0;
  
  if(numbers == null || numbers.length == 0)
      return numbers=[];
  
  for(i = 0; i < numbers.length; i++){
      
    if(numbers[i] >= 0){
       res.push(numbers[i]);
  
    }else{
         sum += numbers[i];
         //console.log(sum);
    }
  }

  r = res.length;
  res = [];
  res.push(r);
  res.push(sum);
 return res;
}

console.log(integers([1, 2, 0, 4, 5, 6, 7, -8, 9, 10, -11, -12, -13, -14, -15]));

console.log(integers([]));