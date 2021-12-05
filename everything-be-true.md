# All be true
Check if the predicate (second argument) is true in all elements of a collection (first argument).

In other words, you are given an array collection of objects. The predicate will preserve an object property and must return trues if its value is truthy. Otherwise return false.

In JavaScript, truth and values are values that translate true when evaluated in a Boolean context.

Remember, you can access the object's properties using dot notation or [] notation.

## Possible solution

```
function truthCheck(collection, pre) {
  let len = collection.length
  let cont = 0;
    for(let i = 0 ; i < len ; i++){
        console.log(collection[i].hasOwnProperty(pre))
        if(collection[i].hasOwnProperty(pre) && Boolean(collection[i][pre])){ cont++
        }
    }
  return cont === len;
}

truthCheck([{"user": "Tinky-Winky", "sex": "male"}, {"user": "Dipsy", "sex": "male"}, {"user": "Laa-Laa", "sex": "female"}, {"user": "Po", "sex": "female"}], "sex");
```