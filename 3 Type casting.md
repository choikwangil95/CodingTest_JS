![KakaoTalk_20201028_194707587](https://user-images.githubusercontent.com/48672212/97428899-ff3e7880-1959-11eb-86cf-9c1d57e6ac84.png)
#### Reference
[형변환 Casting](https://blog.outsider.ne.kr/361)
<br/>
### Check Point
형변환 Casting 은 다음과 같이 한다<br/>
String(), Number(), parseInt(), parseFloat()
<br/>

```javascript

function solution(n) {
    var answer = [];
    let input = n;
    let num = 0;
    let i;
    
    while(input>0){
        input = parseInt(input/10); // 자릿수 check를 위해 10으로 계속 나눠주며
        num++;                      // 나눠준 횟수 check
    }
    
    console.log(num);
    console.log(n);
    
    for (i=0; i<num; i++){ 
        answer[i] = n%10;           // 각 자리수의 숫자가 무엇인지 확인하기 위해 나머지값
        console.log(answer[i]);
        n = parseInt(n/10);
    }
    
    return answer;
}

```
