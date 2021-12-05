# Convert HTML entities
Return an English translated sentence of the passed binary string.
The binary string will be space separated.

## Possible solution

```
function convertHTML(str) {
  const htmlEnti = {
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&apos;"
  };
  // Using a regex, replace characters with it's corresponding html entity
  return str.replace(/[(&<>\"')]/g, match => htmlEnti[match]);
}
```