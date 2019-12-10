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

x.sort((a, b) => return a > b ? 1 : -1);

## Efficient fibonacci sequence

const fib(n) => {
  let arr = [1, 1];
  for(let i = 0; i <= n; i++) {
    arr.push(arr[arr.length - 1] + arr[arr.length - 2]);
  }
}

## Sum numbers from X to Y 

const sumFromXtoY = (x,y) => {
  return (y ** 2 - x ** 2 + y + x)/2
}

sumFromXtoY(1,10) => 55
