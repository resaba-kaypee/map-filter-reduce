# map-filter-reduce

//#map
const square = [1, 2, 3, 4, 5];
const squared = square.map(arg => arg * arg)
//squared is [1, 4, 9, 25]

//#filter
const myNum = [2, 3.5, 5, 6, -9, 3.14, 10, -4]
const integers = myNum.filter(int => int > 0 && Number.isInteger(int))
//integers [2, 5, 6, 10]

//#map + #filter in action
const realNumbers = [2, -4, 5.15, 6, -7, 8.9, 10];
const squareList = (arr) => {
const squaredIntegers = arr.filter(integer => Number.isInteger(integer) && integer > 0).map(square => square * square);
return squaredIntegers;
}
// squaredIntegers in not affected by the changes inside the function scope
const squaredIntegers = squareList(realNumbers);
console.log(squaredIntegers)
