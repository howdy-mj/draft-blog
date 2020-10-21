---
title: 'RxJS'
date: 2020-10-22 23:42:29
category: 'rxjs'
draft: true
---

## Functional Programming

함수형 프로그래밍은 함수로 선언적이고 불변(immutable)하며 부수효과(side effects)가 없는 프로그램 만들기를 강조하는 소프트웨어 패러다임이다. 

시계를 예로 들면, 오후 1시부터 오후 2시까지 계속 시간이 가 변화한다. 하지만 이를 함수형 관점에서 본다면, 매일 단일 시계 인스턴스를 변경하는 대신 1초마다 새로운 시계 인스턴스를 반환하는 것이다. 이론적으로 둘은 동시에 도착하고, 결국 단일 상태가 된다. 

특징

- 선언적(declarative) 함수형 코드는 특수한 비즈니스 로직을 적용하고자 자바스크립트의 고차 함수를 활용하는 독특한 스타이이 있다. 함수 체인(파이프라인)은 데이터 변화 단계를 관용적인 방식으로 묘사한다. 

- 불변성(immutable) 불변 프로그램(불변 함수, 모듈 또는 전체 프로그램)은 데이터를 생성한 후나 변수가 선언된 후에 이를 변경하거나 수정하지 않는 프로그램이다. FP는 데이터 불변의 일정한 값으로 다룬다. 익숙한 모듈 중 좋은 예는 string 타입이다. 어떠한 작업도 이 타입이 작업하는 문자열을 바꾸지 않기 때문이다. 오히려 새로운 문자열을 반환한다. const로 변수를 할당하여 블록 범위의 불변 변수로 만들면, 모든 문제가 해결되는 건 아니지만, 데이터와 함수들을 전역으로 공유할 때 어느 정도 추가 지원을 받을 수 있다. 

- 부수 효과(side effects) 부수 효과이 있는 함수는 지역 범위 밖에 있는 데이터에 따라 결과가 달라진다. 함수의 범위는 인수와 그 안에 선언된 모든 지역 변수로 구성된다. 이 외의 작업(파일 읽기, 콘솔 출력, html 페이지 요소 렌더링 등)은 부수효과로 간주하므로 피하거나 최소한으로 격리해야 한다. 

## RxJS


데이터 스트림(data streams)
변화의 전달(the propagation of change)

데이터 스트림은 데이터의 흐름. 보통 정적인 데이터 스트림은 배열을, 동적인 데이터 스트림은 이벤트 이미터(event emitter)를 뜻함. 정적이든 동적이든 여러 개의 데이터 흐름이 존재할 수 있는데, 동적인 데이터 스트림의 예로는 마우스 클릭처럼 여러 번 발생할 수 있는 이벤트가 있다. 
변화의 전달은 데이터 스트림 안에서 어떤 값이 변했을 때의 전달이 바로 이루어지는 것을 뜻한다. 예를 들어 명령형 프로그래밍에서는 c=a+b를 실행한 후, a 값이 바뀐다면 a만 바뀔 뿐 c가 같이 바뀌지 않는다. 하지만 리액티브 프로그래밍은  a 값이 바뀌었을 때 바로 c 값도 변한다. 엑셀에서 특정 셀 값을 바꿨을 때 해당 셀을 이용하는 다른 셀 값도 같이 변하는 것과 같다. 즉, 리액티브 프로그래밍은 정적/동적인 데이터 흐름의 변화에 곧바로 반응하는 프로그램을 만드는 것이라 할 수 있다. 

RxJS는 FP에서 여러가지 원칙, 특히 함수 체인(function chain), 지연 평가(lazy evaluation), 데이터 흐름을 조정하기 위한 추상형 데이터 타입 사용 개념을 차용한다. 이 개념들은 Observable 데이터 타입을 통해 RxJS의 스트림 프로그래밍 개발을 주도하는 디자인 의사 결정이다. 


---

참고 자료

- https://m.blog.naver.com/PostView.nhn?blogId=bkcaller&logNo=221627461671&proxyReferer=https:%2F%2Fwww.google.com%2F

- https://books.google.co.kr/books?id=DUJvDwAAQBAJ&pg=PA25&lpg=PA25&dq=rxJS+%EC%86%8C%EA%B0%9C&source=bl&ots=_wQSOUho2h&sig=ACfU3U2qrNRjMACtAmSWsUHLyyg7jT-6_Q&hl=en&sa=X&redir_esc=y#v=onepage&q=rxJS%20%EC%86%8C%EA%B0%9C&f=false

- https://thebook.io/006934/part01/ch02-02/
- https://tienne.gitbooks.io/learnrxjs/content/

- https://tech.kakao.com/2017/01/09/daummovie-rxjs/