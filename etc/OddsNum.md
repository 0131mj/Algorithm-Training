# 임의의 문자열에서 홀수 문자가 등장하는 개수 출력하기

```JavaScript
const getOddsCnt = (str) => {
    const odds = new Set();            
    for(char of str){
        if (odds.has(char)) {
            odds.delete(char);
        } else {
            odds.add(char)
        }
    }
    return odds.size;
}
```
