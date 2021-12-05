# DNA Pairing
The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.
Base pairs are a pair of AT and CG. Match the missing element to the provided character.
Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"], ["G", "C"]]
The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

## Possible solution

```
function pairElement(str) {
  let arrStr = [];
  let arrSing = [];
  let nStr = str.split("");
  for(let char of nStr){
    switch(char){
      case 'G':
        arrSing.push(char)
        arrSing.push('C')
        break; 
    
      case 'C':
        arrSing.push(char)
        arrSing.push('G')
        break; 
    
      case 'A':
        arrSing.push(char)
        arrSing.push('T')
        break; 
    
      case 'T':
        arrSing.push(char)
        arrSing.push('A')
        break; 
      default:
        break; 
    }
    arrStr.push(arrSing);
    arrSing = []
  }
  console.log(nStr)
  console.log(arrStr)
  return arrStr;
}
pairElement("ATCGA");
```