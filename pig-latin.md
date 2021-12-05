# Pig Latin

Pig Latin is a way of altering English Words. The rules are as follows:
- If a word begins with a consonant, take the first consonant or consonant cluster, move it to the end of the word, and add ay to it.
- If a word begins with a vowel, just add way at the end.
Translate the provided string to Pig Latin. Input strings are guaranteed to be English words in all lowercase.

## Possible solution

```
function translatePigLatin(str) {
  let regexVow = /(^[aeiouAEIOU0-9\\W]+)/;
  let regexCos = /(^[^aeiouAEIOU0-9\\W]+)/;
   if(regexVow.test(str)){
     return str += "way";
    }
    let newStr = str
    .replace(str.match(regexCos)[0],"")
    return newStr += `${str.match(regexCos)[0]}ay`
}

translatePigLatin("glove");
```