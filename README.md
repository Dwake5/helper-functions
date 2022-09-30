# helper-functions

This is a list of helper functions I thought were interesting or novel and that I will likely use in the future.

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

## Pull from a weighted array

  const getIndexFromWeightedArray = () => {
  const array = [1, 7, 2];
  const arrayTotal = array.reduce((a, b) => a + b);
  let randomNumber = Math.random() * arrayTotal;

  let totalTraversed = 0;
  for (let i = 0; i < array.length; i++) {
    if (randomNumber < array[i] + totalTraversed) return i + 1;
    totalTraversed += array[i];
  }
};

In this example note that the array = 10, when calling this function the 0th index would be returned 10% of the time, 1st 70% and 2nd 20%.
This can be used with any length array and any numbers. 1 is added here as this was used for weighted dice. 


## Create object with amount of times keys appear in array

const objectMap = arr =>
  arr.reduce((obj, elem) => {
  elem in obj ? obj[elem]++ : obj[elem] = 1
  return obj
},{})

## Is it a Prime Number

const isNumberPrime = n => {

  if (n <= 1) return false
  
  if (n === 2) return true
  
  if (n % 2 === 0) return false
  
  for (let x = 3; x <= Math.sqrt(n); x+=2) {
  
    if(n % x === 0) {
    
      return false;
      
    }
    
  }
  
  return true;  
  
} 
