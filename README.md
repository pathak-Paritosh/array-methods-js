# Array Methods in JS

**1. Filter Method** : *Used to filter out some elements from an array based on some conditions. It returns a new array.*
> For ex : Given an array of integers, create a new array which contains only the elements those are greater than 50.
>>Lets say: 
>>
>>Given array = [14, 65, 90, 34, 48, 73]
>>
>>Output array should be: [65, 90, 73]

```
let arr = [14, 65, 90, 34, 48, 73];

let filteredArr = arr.filter((ele) => {
    return ele > 50;
});

console.log(filteredArr);

```
Below is the shorter code to do the same.
```
let arr = [14, 65, 90, 34, 48, 73];

let filteredArr = arr.filter(ele => ele > 50);

console.log(filteredArr);

```

**2. Map Method** : *Used to create a new array(of same size) by modifying the current array elements.*
> For ex : Given an array of costs(int), return a new array by applying 10% discount to each item.
>> Lets say:
>>
>> Given array = [100, 40, 25, 50, 80]
>>
>> Output array should be: [90, 36, 22.5, 45, 75]

```
let costs = [100, 40, 25, 50, 80];

let finalCosts = costs.map((cost) => {
    return cost - cost*0.1;
});

console.log(finalCosts);
```


Below is the shorter way to do the same.
```
let costs = [100, 40, 25, 50, 80];

let finalCosts = costs.map(cost => cost - cost*0.1);

console.log(finalCosts);
```


**3. Reduce Method** : *Can be used to do some calculations related to the array.*
> For ex : Given an array of integers, count number of elements which are greater than 10 and are even.
>> Lets say:
>>
>> Given array = [13, 20, 4, 6, 23, 17, 19, 14]
>>
>> Output array should be: 2. (20 and 14 are greater than 10 and are even).

```
let arr = [13, 20, 4, 6, 23, 17, 19, 14];

// takes two arguments, first: a callback fun which has counter(in this case) and curr as current element, second: initial value of counter which is zero
let res = arr.reduce((counter, curr) => {
    if(curr > 10 && curr % 2 == 0){
        counter++;
    }
    return counter;
}, 0);

console.log(res);
```



**4. Sort Method** : *By default, in JS sort method sorts the array by in lexicographical order considering each element as a string.*
For ex:
```
let arr = [10, 200, 5, 30];
arr.sort();
console.log(arr);
// output will be: [10, 200, 30, 5]
// To do numeric sort we need to pass a comparator function
```

Sorting in increasing order:
```
let arr = [10, 200, 5, 30];
arr.sort((a, b) => a-b);
console.log(arr);
// output: [5, 10, 30, 200]
```

Sorting in decreasing order: 

*Method1*
```
let arr = [10, 200, 5, 30];
arr.sort((a, b) => b-a);
console.log(arr);
```

*Method2*
```
let arr = [10, 200, 5, 30];
//first sort in increasing order then reverse
arr.sort((a, b) => a-b);
arr.reverse();
console.log(arr);
```



