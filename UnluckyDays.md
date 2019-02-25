### 년도가 주어지면, 해당 년도에 13일의 금요일이 몇개나 포함되어 있는지 검사하는 문제
- .getMonth() 함수가 0부터 시작한다는 사실을 잊어서 잠시 헤매었음.
```js
function unluckyDays(year){     
  let yearObj = new Date(year, 0, 13);
  let unluckyDayCnt = 0;
  while(yearObj.getFullYear() === year){
    if(yearObj.getDay() === 5){
      unluckyDayCnt++;
    }
    yearObj = new Date(yearObj.getFullYear(), yearObj.getMonth()+1, 13);
  }
  return unluckyDayCnt;
}
```
