# 2023-01-30 공부 계획 정리

## 양재연
- AWS EC2를 활용해서 스프링 프로젝트 배포
---
## 김세현
- 블로그 동영상 및 이미지 수정
- 블로그 소개페이지 제작
---
## 이상훈
- 삼성 A형 기출 풀기
---
## 김준서
- 자바스크립트 deep dive 책을 통한 자바스크립트 원리 공부 
---
## 진하윤
- c++문자열 백준 문제 풀이
- c++함수 공부
- c++함수 백준 문제 풀이
---
</br>
</br>

# 2023-01-30 Week 4 비대면 공부 기록

<img src="1.png">
</br>
</br>

# 2023-01-30 Week 4 공부 내용 정리

## 양재연

### 배운점
* EC2와 RDS 인스턴스를 생성하고 둘의 연결을 진행하는 과정을 배웠다.
* EC2에 프로젝트를 배포하다가 발생할 수 있는 문제점에 대해서 배웠다.

### 보완점
* 스터디 시간 내에 오류를 해결하지 못한 점이 가장 아쉽다. 다음 스터디 진행 전까지 오류 해결 뒤 프로젝트 배포를 진행할 것이다.

</br>

## 김세현

### 배운점
- 블로그 동영상 및 이미지 수정 완성도 [ 1 / 3 ]
- 블로그 이미지 크로마키 처리 구현
- 블로그 코드 최적화 완성도 [ 1 / 3 ]
- 블로그 소개페이지 미완

</br>

## 이상훈

### 배운점
- <a href="https://www.acmicpc.net/problem/17135">백준 17135번</a> 소요시간 : 98분 23초 시도 횟수 : 3회
    * 백트래킹을 사용하여 3개를 뽑는 경우의 수를 전부 진행하였음
    * 적의 위치를 vector 자료구조로 저장하였음
</br>
</br>

- <a href="https://www.acmicpc.net/problem/17070">백준 17070번</a> 소요시간 : 58분 13초 시도 횟수 : 2회
    * dfs와 재귀함수를 사용하여 모든 경우의 수를 진행하였음
    * 파이프가 (N, N)에 도달하면 count 수를 1 늘려주었음
</br>
</br>

### 보완점

- 아직 구현력이 부족하여 코딩할 때 시간이 많이 걸리는 것 같음. 더 많은 구현 문제를 풀어야겠다는 생각이 들었음.

</br>


## 김준서

### 배운점
#### 자바스크립트에서의 this


* this 키워드</br>
  - this는 자신이 속한 객체 또는 자신이 생성할 인스턴스를 가리키는 자기 참조 변수이다. 
  - this를 통해 자신이 속한 객체 또는 자신이 생성할 인스턴스의 프로퍼티나 메서드를 참조 가능
  - this가 가리키는 값, 즉 this 바인딩은 함수 호출 방식에 의해 동적으로 결정
    
* 함수 호출 방식과 this 바인딩 </br>
  1. 일반 함수로 호출된 모든 함수(중첩, 콜백 함수 포함)에서 this -> 전역 객체 window 
  2. 메서드 내부에서 this -> 호출한 객체
  3. 생성자 함수 내부에서 this -> 생성자 함수가 생성할 인스턴스

``` javascript 

function foo() {
    console.log(this) // window
    function bar() {
      console.log(this); //window
  };
};

const obj = {
  value:100,
  foo(){
    console.log(this) // {value: 100, foo: f}
  };
};

function Person(name){
    this.name = name;
}

Person.prototype.getName = function() {
    return this.name;
}
const me = new Person('kim');

Person.prototype.name = 'Lee';

console.log(me.getName()); //kim
console.log(Person.prototype.getName()); //Lee
```

* Function.prototype.apply/call/bind 메서드에 의한 간접 호출
  - 메서드 첫번째 인수로 전달한 객체가 this
``` javascript
function getThisBinding() {
    return this;
};

const thisArg = { a:1 };

console.log(getThisBinding()); //window

console.log(getThisBinding.apply(thisArg)); // {a:1}
console.log(getThisBinding.call(thisArg)); // {a:1}

```
</br>

## 진하윤

### 배운점
- c++ 함수 공부
- 문자열(백준 10809번, 백준 11718번, 백준 2908번) 문제 풀기
- c++ 함수 (백준 15964번) 문제 풀기

### 보완점
- 문자열 함수를 이용하면 간단한 문제들이 있었다. 문자열 함수에 대해 더 공부해야겠다. 아직 함수의 틀만 공부해서 다음시간에 더 보충해야겠다.
