# 임의의 문자열에서 홀수로 나오는 문자의 개수 출력하기

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
