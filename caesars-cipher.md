# Caesars Cipher
One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.
A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus A ↔ N, B ↔ O and so on.
Write a function which takes a ROT13 encoded string as input and returns a decoded string.
All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

## Possible solution

```
function rot13(text) {
  return text
              .replace(/[A-Za-z]/g, function (char){
    return String.fromCharCode((char.charCodeAt(0) % 26) + 65);
  })
}

rot13("SerR Pav PNZC");
```
