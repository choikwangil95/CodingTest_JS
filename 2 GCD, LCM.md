## 최소공배수, 최대공약수
### 1) 최대공약수
M mod N을 하여 나머지가 0일때의 M값을 값을 최대공약수로 한다<br/>
M mod N -> N mod ( M mod N ) -> ...
```javascript
function gcd(num1, num2){
    if(num1 > num2){
        if(num2 == 0){
            return num1;
        }else{
            return gcd(num2, num1 % num2);
        }
    }else if(num1 < num2){
        if(num1 == 0){
            return num2;
        }else{
            return gcd(num1, num2 % num1);
        }
    }
}

function solution(n, m) {
    var answer = [];
    let numGcd, numLcm;
    numGcd = gcd(n, m);
    numLcm = n*m/numGcd
    
    console.log(numGcd);
    
    answer[0] = numGcd;
    answer[1] = numLcm;
    return answer;
}

```
### 2) 최소 공배수
M * N / 최대공약수 = 최소공배수
