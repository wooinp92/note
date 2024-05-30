# 데이터와 변수
  
## 1. 데이터(Data, 자료)
- 계산을 위해 필요한 값 (돈, 키, 체중, 넓이 등)
- 종류별로 구분 됨
- 프로그래밍에서는 단위는 쓰지 않음(상식으로 커버)
- 단위 대신 데이터의 형태를 가지고 구분
- 정수(소수점X), 실수(소수점O), 문자, 논리, 문자열 등으로 구분

```java
System.out.println(10 + 300);		//정수끼리 계산(괄호 안에 ""쓰면 문자로 인식)
System.out.println(10.0 + 300.0);	//실수끼리 계산

(Q)자장면 8천원, 짬뽕 1만원일 때 자장면 2그릇, 짬뽕 3그릇 가격은?
System.out.println(8000 * 2 + 10000 * 3);
		
소계까지 같이 보여주려면?
System.out.println(8000 * 2);	//자장면 금액 합계
System.out.println(10000 * 3);	//짬뽕 금액 합계
System.out.println(8000 * 2 + 10000 * 3);	//전체 합계 -> 중복코드
```

## 2. 변수(Variable)
- 값 또는 식의 결과를 잠시 저장해두는 도구
- 만들 때 형태와 이름을 지정해야 함

```java
int a = 8000 * 2;	//a에 8000 * 2를 계산한 결과를 넣어라!
int b = 10000 * 3;	//b에 10000 * 3을 계산한 결과를 넣어라!
System.out.println(a);	// a에 저장된 값을 출력해라!
System.out.println(b);	// b에 저장된 값을 출력해라!
System.out.println(a + b);
		
// 더 완벽한 구조가 되려면... 자장면 금액, 수량, 짬뽕 금액, 수량을 전부 다 따로 저장해야 함
int jja = 8000;		//자장면 금액
int jjam = 10000;	//짬뽕 금액
int jjaCount = 2;	//자장면 수량
int jjamCount = 3;	//짬뽕 수량	
		
int jjaTotal = jja * jjaCount;		//자장면 합계
int jjamTotal = jjam * jjamCount;	//짬뽕 합계
int total = jjaTotal + jjamTotal;	//전체 합계	
		
System.out.println(jjaTotal);
System.out.println(jjamTotal);
System.out.println(total);
```

## 3. 정수 특징
- 정수끼리 계산하면 정수가 나옴
- '/'는 몫을 구할 수 있고, '%'는 나머지를 구할 수 있다.

```java
System.out.println(10 / 3);	// 3
System.out.println(10 % 3);	// 1
```
		 	
- 정수는 종류가 여러 가지이고, 표현 가능한 범위가 다르다.
- 실제로는 4종류가 있다 (byte / short / int / long) 
- 정수의 기본값은 int 이다. 따라서 더 큰값에는 long임을 표시해야 한다. 
- 만약 계산하다 범위가 넘어가면 뒤집힘 현상이 있다.

```java
int a = 1234567 * 1234567;	//int 범위 초과, ERROR!!
long a = 1234567L * 1234567L;	//계산하다가 커진 경우 long 사용
long b = 9999999999L;	//처음부터 값이 큰 경우 long 사용

System.out.println(a);
System.out.println(b);
```




[문제풀이01 - 영화금액계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test03%EC%98%81%ED%99%94%EA%B8%88%EC%95%A1%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이02 - 술집계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test04%EC%88%A0%EC%A7%91%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이03 - 시간계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test06%EC%8B%9C%EA%B0%84%EA%B3%84%EC%82%B0%EA%B8%B02.java)

[문제풀이04 - 주차장계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test07%EC%A3%BC%EC%B0%A8%EC%9E%A5%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이05 - 숫자자르기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test08%EC%88%AB%EC%9E%90%EC%9E%90%EB%A5%B4%EA%B8%B0.java)

[문제풀이06 - 나이계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test09%EB%82%98%EC%9D%B4%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이07 - 편의점행사상품](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test10%ED%8E%B8%EC%9D%98%EC%A0%90%ED%96%89%EC%82%AC%EC%83%81%ED%92%88.java)

[문제풀이08 - 커피숍계산기](https://github.com/wooinp92/kh14/blob/main/day02/src/data/Test11%EC%BB%A4%ED%94%BC%EC%88%8D%EA%B3%84%EC%82%B0%EA%B8%B0.java)
