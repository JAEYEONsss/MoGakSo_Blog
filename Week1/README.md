# 2023-01-10 공부 계획 정리

## 양재연
- 서블릿, JSP, MVC 패턴 학습하기

## 김세현
- 개인 블로그 스택 정리 및 디자인 

## 이상훈
- C++로 백준 DFS / BFS / DP 문제 각각 2개씩 풀기

## 김준서
- 자바스크립트 deep dive 책을 통해 자바스크립트 원리 공부

## 진하윤
-  c++ 백준문제 입력과 계산. 조건, 반복학습하기
</br>
</br>

# 2023-01-10 Week 1 비대면 공부 기록

<img src="1.png">
<img src="2.png">
</br>
</br>

# 2023-01-10 Week 1 공부 내용 정리

## 양재연

### 배운점
* MVC 패턴 학습
* MVC 규칙 정리
### 보완점
- 최초 계획은 서블릿, JSP, MVC 패턴에 대해 모두 학습하는 것이었다. 하지만, 실제로는 MVC 패턴만 학습하게 되어서 계획 실천을 완벽하게 하지 못했다.    
다음 스터디 때는 스터디 계획을 좁게 설정해서 구체적이고 깊게 학습해야겠다고 결심했다.
</br>

## 김세현

### 배운점

- 개인 블로그 스택 정리
- 개인 블로그 디자인
- 인프런 강의 시청

- If smooth Expect

    - BackEnd : express
    - Database : mysql

    - React Structure 및 기본 디자인 완료   
    - 자세한 사항은 https://github.com/NSRBSG/blog commit 참조

</br>


## 이상훈

### 배운점

- MarkDown 문법을 배워 팀 소개 및 공부 계획 마크다운 문서 생성
- DFS (<a href="https://www.acmicpc.net/problem/1388">백준 1388번</a>, <a href="https://www.acmicpc.net/problem/24479">백준 24479</a>) 및 BFS (<a href="https://www.acmicpc.net/problem/17086">백준 17086번</a>, <a href="https://www.acmicpc.net/problem/24444">백준 24444번</a>) 복습
- DP 기초 유형 (<a href="https://www.acmicpc.net/problem/2849">백준 2849번</a>, <a href="https://www.acmicpc.net/problem/1463">백준 1463번</a>) 복습</br></br>

### 보완점

- 문제 풀 때 어떤 알고리즘을 써서 풀지 미리 알고 풀면 난이도가 너무 쉬워지기 때문에 백준 사이트의 난이도 기능을 활용하여 문제를 푸는 것이 좀 더 나을 것 같음

</br>


## 김준서

### 배운점
</br>

### 타입 변환
기존 원시 값 변경이 아니라 원시 값을 사용해 다른 타입의 새로운 원시 값을 생성하는 것
* 명시적 타입 변환 (타입 캐스팅)</br>
개발자가 의도적으로 타입을 변환 (암묵적 타입 변환을 이용)
  - 문자열 타입으로 변환
    - String()
    - toString()
    - 문자열 연결 연산자
  
  - 숫자 타입으로 변환 
    - Number()
    - parseInt()
    - + 단항 산술 연산자
    - * 산술 연산자

  - 불리언 타입으로 변환
    - Boolean()
    - !!   
    
* 암묵적 타입 변환 (타입 강제 변환) </br>
개발자의 의도와 상관 없이 코드 문맥을 고려해(에러를 발생시키지 않기 위해) 타입을 강제 변환
  - 문자열 타입으로 변환
    - 1 + '2' -> "12"
    - `1+1 = ${1+1}` -> "1+1 = 2" (표현식의 평과 결과를 문자열 타입으로 변환)
    - -1 + '' -> "-1"
    - true + '' -> "true"
    - null + '' -> "null"
    - undefined + '' -> "undefined"
    - ({}) + '' -> "[object Object]"
    - Math + '' -> "[object Math]"
    - [] + '' -> ""
    - [10, 20] + '' -> "10, 20"
    - (function(){}) + '' -> "function(){}"
    
  - 숫자 타입으로 변환</br>
  빈 문자열, 빈 배열, null, false 는 0 true 는 1, 객체와 빈 배열이 아닌 배열, undefined 는 변환 x
     - +'1' -> 1
     - +'string' -> NaN
     - +true -> 1
     - +null -> 0
     - +undefined -> NaN
     
  - 불리언 타입으로 변환
  자바스크립트 엔진은 불리언 타입이 아닌 값을 truthy 또는 falsy 값으로 구분한다.
    - falsy 값 (이 외에 모든 값 truthy)
      false, undefined, null, 0, -0, NaN, ''
    

### 단축 평가
논리합 또는 논리곱 연산자 표현식의 평과 결과는 불리언 값이 아닐 수도 있다. 논리합 또는 논리곱 연산자 표현식은 어느 한쪽으로 평가된다. </br>
연산의 결과를 결정하는 피연산자를 타입 변환하지 않고 그대로 반환한다.
- 'cat' && 'dog' -> 'dog'
- 'cat' || 'dog' -> 'cat'
### 옵셔널 체이닝 연산자
옵셔널 체이닝 연산자 ?.은 좌항의 피연산자가 null 또는 undefined인 경우 undefined 반환, 그렇지 않으면 우항의 프로퍼티 참조 (이전엔 && 사용)</br>
falsy 값이어도 null or undefined가 아니면 프로퍼티 참조 이어감

var elem = null; </br>
var value = elem?.value; </br>
console.log(value); //null </br>

var str = ''; </br>
var length = str?.length; </br>
console.log(length); //0 </br>

### null 병합 연산자
null 병합 연산자 ??는 좌항의 피연산자가 null 또는 undefined인 경우 우항의 피연산자를 반환 (이전엔 || 사용) </br>
var foo = null ?? 'default string'; </br>
console.log(foo) // "default string"

</br>

## 진하윤

### 배운점

- c++ 입력과 계산/조건/반복에 대한 문법 공부

- 입력과 계산(백준 1000번, 백준 10869번, 백준 11382번), 조건(백준 1330번, 백준 9498번, 백준 2420번), 반복(백준 2741번, 백준 10872번, 백준 10952번) 문제 풀기

### 보완점
- 프로젝트 소스 실행에 오류가 있어 계획했던 문제를 다 풀지 못하였음. 사소한 오류들을 빠르게 해결해야할 필요가 있음.

