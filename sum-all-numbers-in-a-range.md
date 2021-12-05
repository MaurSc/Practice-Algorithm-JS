# Sum All Numbers in a Range

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. The lowest number will not always come first.
For example, sumAll([4,1]) should return 10 because sum of all the numbers between 1 and 4 (both inclusive) is 10.

```
function sumAll(arr) {
  arr.sort((a,b) => a-b); // sort the array
  let sum = 0, start = arr[0], end = arr[1];// create new variables to have the start and end values.
  for(let i = start; i <= end; i++){
    sum += i;
  }
  return sum;
}

sumAll([4, 1]);

```