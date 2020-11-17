# Name to Matrix

Given a name, turn that name into a perfect square matrix (nested array with the amount of arrays equivalent to the length of each array).

You will need to add periods (`.`) to the end of the name if necessary, to turn it into a matrix.

If the name has a length of 0, return `"name must be at least one letter"`



## Examples

```js
"Bill" ==> [ ["B", "i"],
             ["l", "l"] ]

"Frank" ==> [ ["F", "r", "a"],
              ["n", "k", "."],
              [".", ".", "."] ]
```



## Solution : 내 풀이

```javascript
const matrixfy = str =>{		
    const strLen = str.length;
    if(strLen < 1) {return 'name must be at least one letter';}

    const width = Math.ceil(Math.sqrt(strLen));
    const matrix =[];	

    for(let i = 0; i < width ; i++){
        matrix[i]=[];
        for(let j = 0; j < width ; j++){
            matrix[i][j] = str[i*width+j] || '.'
        }
    }
    
    return matrix;
}

```

