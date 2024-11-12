
* *Maps* : stores value in key-value pairs 
* stores only unique keys 
*OBJECTS cannot be iterated   through the for of loop. 
* Maps are not iterable .

```js
Syntax : 

const map = new Map()

map.set('IN',"India")
map.set('US',"America")
map.set('Fr',"France")

for (const [k,v]  of map) {
    console.log(k+":-"+v);   
}
```

* _for-in loop_ : can be used to iterate the objects

```js
EX:

const obj ={
    name : "AM",
    std : 3,
    sec : "B",
    id : "22btcs0229"
}

for (const key in obj) {
    
    console.log(`${key} has the value ${ obj[key] } `);
      
}
```

* AND IN ARRAYS IT RETURN INDEXES OF THE ARRAYS I.E FROM 0 -> N

* _forEach loop_ :- is and Higher Order Function 
* Does not returns any value so we cannot perform any operations on the acessed value

```
Syntax : <datatype_name>.forEach ( <callbackFn>(item, idx, arr) )

    Ex:-  const arr = ["A", "B", "C", "D"]

```

```js
1. arr.forEach( function (i){
    console.log(i);
} ) ---> prints the arrays ele. one by one

2.  arr.forEach( (item) => {
    console.log(item);
    
} )

OR arr.forEach((i)=>console.log(i))

3.  function abc(item, idx){
    console.log(`${idx} :- ${item}`);
}

arr.forEach(abc) //---> prints the index with array_ele
```

* _filter ( )_ :- with this we can perform operations on the acessed value

* It returns values , so we need to store this in a variable

```js
Ex:  const arr = [1,2,3,4,5,6]

1.  
let res = arr.filter( (i)=> {
    return i>3;
})  ---> [ 4, 5, 6 ]

2.  let r = arr.filter( (i)=> (i%2==0) )  ---> [ 2, 4, 6 ]

```

 * _map ( )_ : [ why better than forEach ? ]

```js
EX :-

const r = [1,2,3,4,5,6,7,8,9,10]

let res =  r.map( (i) => i*10 )
            .map( (i) => i+1 )
            .filter( (i)=> i>50 )

console.log(res); 

Output :- [ 51, 61, 71, 81, 91, 101 ]
```

* reduce() :- [ https://youtu.be/sscX432bMZo?t=31743 ]

```js

    Syntax :
    <var_name>.reduce ((accumalator , currValue ) => acc+curr,
    initial_val );

Ex :    const arr = [1,2,3,4,5,6,7,8,9,10]

// Adds array elements
let res = arr.reduce( (acc,curr) => acc+curr,0 ); 

Output --> Sum : 55
```
