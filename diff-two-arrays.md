# Diff Two Arrays
Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.
Note: You can return the array with its elements in any order.

## Possible solution

```
function diffArray(arr1, arr2) {
  const newArr = [];
  for(let value of arr1){
    if(arr2.indexOf(value) === -1){
      newArr.push(value);
    }
  }
  for(let value of arr2){
    if(arr1.indexOf(value) === -1){
      newArr.push(value);
    }
  }
  console.log(newArr)
  return newArr;
}
```