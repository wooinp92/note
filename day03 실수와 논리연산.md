# day03 실수와 논리연산

## 1. 실수(Floating Number)
- 소수점이 있는 숫자
- float, double 두 종류가 존재
- 기본형태가 double로 설정됨
- 정확하게 계산되지 않음 (부정확성) -> 정수와 구분해서 사용하는 이유, so 자주사용X
- int < long < float < double

```java
// 	float a = 1.234;  -> ERROR, 기본형태가 double 이므로..
	float a = 1.234f;	//선언값 뒤에 f(F) 표기를 해야됨
	double b = 2.345;
	
	System.out.println(a);
	System.out.println(b);
		
	float c = 1.2345468754635451356f;
	double d = 1.2345468754635451356;	//float, double -> 출력되는 소수 자리수 차이
	
	System.out.println(c);
	System.out.println(d);
		
//	(*중요) 실수가 포함된 계산은 결과가 실수
	System.out.println(1.5 + 2.5);	// 4와 4.0은 다르다
	System.out.println(10 / 3.0);	// 소수점 끝에 5가 나오는 이유 -> 부정확성
	System.out.println(10 / 3d);	
	System.out.println(10 / 3f);
```

[문제풀이01 - 성적계산기](https://github.com/wooinp92/kh14/blob/main/day03/src/data2/Test02%EC%84%B1%EC%A0%81%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이02 - 체질량지수BMI계산기](https://github.com/wooinp92/kh14/blob/main/day03/src/data2/Test03%EC%B2%B4%EC%A7%88%EB%9F%89%EC%A7%80%EC%88%98BMI%EA%B3%84%EC%82%B0%EA%B8%B0.java)

[문제풀이03 - 급여계산기](https://github.com/wooinp92/kh14/blob/main/day03/src/data2/Test04%EA%B8%89%EC%97%AC%EA%B3%84%EC%82%B0%EA%B8%B02.java)

[문제풀이04 - PC방계산기](https://github.com/wooinp92/kh14/blob/main/day03/src/data2/Test05PC%EB%B0%A9%EA%B3%84%EC%82%B0%EA%B8%B02.java)


## 2. 논리
- true(참), false(거짓)을 저장하기 위한 형태
- 자료형의 이름은 boolean

```java
	boolean a = true;
	boolean b = false;
		
	System.out.println(a);
	System.out.println(b);

//	(Q) 가진돈이 2만원일 때, 8천원짜리 자장면과 1만5천원짜리 탕수육을 시킬 수 있나요?
	int money = 20000;
	int jja = 8000;
	int tang = 15000;

//	boolean order = 가진 돈이 자장면+탕수육 금액보다 많나요?;
//	boolean order = 가진돈 >= 자장면값 + 탕수육값;
	boolean order = money >= jja + tang;
		
	System.out.println(order);
```
		
## 2-1. 비교연산
- 숫자를 비교하여 논리를 만들어내는 연산(계산)
- 크다(>), 작다(<), 이상(>=), 이하(<=), 같다(==), 다르다(!=)

## 3. 논리연산
- &&(and) 연산을 하면 좌,우가 모두 참일 때 참이 나온다. (참참참)
- ||(or) 연산을 사용하면 하나만 참이어도 결과가 참이 나온다. (하나만 걸려라)

```java
//	(Q) 어떤 사람의 나이가 "청소년" 에 해당 하는지 판정하세요
//  	청소년이란, 나이가 14살 이상 20살 미만을 의미한다.

	int age = 17;
			
//	boolean teenager = 14 <= age <20;	-> ERROR!!
	boolean teenager = 14 <= age && age < 20;	// and 연산 사용
			
	System.out.println("청소년 인가?");
	System.out.println(teenager);
		
			
//	(Q) 어떤 사람의 나이가 "무임승차" 대상인지 판정하세요
//	영유아(8세 미만) 또는 어르신(65세 이상)인 경우
		 
	boolean free = age < 8 || age >= 65;
			
	System.out.println("무임승차 대상인가?");
	System.out.println(free);
```

[문제풀이01 - 성인인증프로그램](https://github.com/wooinp92/kh14/blob/main/day03/src/data3/Test02%EC%84%B1%EC%9D%B8%EC%9D%B8%EC%A6%9D%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A82.java)

[문제풀이02 - 숫자판정](https://github.com/wooinp92/kh14/blob/main/day03/src/data3/Test03%EC%88%AB%EC%9E%90%ED%8C%90%EC%A0%95.java)

[문제풀이03 - 건강검진대상자판정](https://github.com/wooinp92/kh14/blob/main/day03/src/data3/Test05%EA%B1%B4%EA%B0%95%EA%B2%80%EC%A7%84%EB%8C%80%EC%83%81%EC%9E%90%ED%8C%90%EC%A0%95.java)

[문제풀이04 - 윤년판정계산기](https://github.com/wooinp92/kh14/blob/main/day03/src/data3/Test06%EC%9C%A4%EB%85%84%ED%8C%90%EC%A0%95%EA%B3%84%EC%82%B0%EA%B8%B0_%EC%A0%9C%EC%B6%9C%EC%9A%A9.java)
