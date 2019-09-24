# helper-functions

This is a list of helped functions I thought were interesting or novel and that I will likely use in the future.

## Make an x by y array and fill it with z

const fillArray = (rows, columns, fill) => {
  return Array(rows).fill().map(() => Array(columns).fill(fill));
}

fillArray(3,3,0) => [ [ 0, 0, 0 ], [ 0, 0, 0 ], [ 0, 0, 0 ] ]

## Repeat a string x times

const repeat = (str,x) => {return Array(x+1).join(str) }

repeat('Hello ', 4) => 'Hello Hello Hello Hello '

## Sort an array by numbers

x.sort(function(a, b) { return a > b ? 1 : -1});

