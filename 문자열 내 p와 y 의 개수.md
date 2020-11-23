# 문자열 내 p 와 y 의 개수.md
##### 문제 설명
- 대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

- 예를 들어 s가 pPoooyY면 true를 return하고 Pyy라면 false를 return합니다.


##### 제한사항
- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.


### 나의 풀이
- 대소문자를 구분하지 않으므로 아예 대문자로 바꿔서 비교를 시도함.
```javascript
function solution(s){    
    const chars = s.toUpperCase().split("");
    return chars.filter(c => c === "P").length === chars.filter(c => c === "Y").length
}
```

### 아쉬웠던 점
- 정규표현식을 이용하면 더 간결하게 풀 수 있다.
- 단, 문자가없으면 null을 리턴하므로 optional chaining 혹은 기본값을 배열로 리턴해서 예외처리를 해야 한다.
```javascript
function solution(s){        
    return (s.match(/p/ig)||[]).length === (s.match(/y/ig)||[]).length
}
```
