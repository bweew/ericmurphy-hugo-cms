---
title: 'js for tabular data processing'
date: 2024-01-27T04:51:00.000-05:00
draft: false
url: /2024/01/js-for-tabular-data-processing.html
---

uses for 2d arrays and nested loops
-----------------------------------

to work with a csv in vim you could create objects by doing some find and replace substitutions.

#### tsv

it may or may not be a good idea to swap commas for tabs for this operation.

*   tabs are less common  
    they offer consistent field separation
*   prevent splitting values  
    wrapping the lines with square brackets
*   facilitate subsequent transformations

###### replacing commas w tabs

```
:%s/,/\t,/g 
```

###### preparing the object

behold the substitution:

```
:%s/^/\t{ / | %s/$/ },/ | %s/\t/"/g | %s/":/": "/ | %s/,\s*$/,/g 
```

###### square brackets

this puts square brackets at the start and end which isnt object notation but looks nore like whats in the later examples

```
:%s/^/[/g
:%s/$/]/g 
```

another way is to use the vim surround plugin VS\]  
yss\] to just do 1 line

### summing values

finding sum of columns and rows

```
const table = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

// Calculate row sums
for (let i = 0; i < table.length; i++) {
  let rowSum = 0;
  for (let j = 0; j < table[i].length; j++) {
    rowSum += table[i][j];
  }
  console.log(`Sum of row ${i + 1}: ${rowSum}`);
}

// Calculate column sums
for (let j = 0; j < table[0].length; j++) {
  let colSum = 0;
  for (let i = 0; i < table.length; i++) {
    colSum += table[i][j];
  }
  console.log(`Sum of column ${j + 1}: ${colSum}`);
} 
```

### filtering data

```
const data = [
  ['John', 25, 'Developer'],
  ['Jane', 30, 'Designer'],
  ['Bob', 35, 'Manager']
];

// Filter employees older than 25
const filteredData = [];
for (let i = 0; i < data.length; i++) {
  if (data[i][1] > 25) {
    filteredData.push(data[i]);
  }
}
console.log(filteredData); 
```