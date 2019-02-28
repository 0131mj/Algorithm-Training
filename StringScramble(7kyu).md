### 문장과, 주어진 배열에 따라 단어 재배치하기 

```js
function scramble(str, arr) {
  let newStr = [];
  str.split('')
    .map( (char,idx) => {
      newStr[arr[idx]] = char;
  });
  return newStr.join('');
};
```
