# day03 실수와 논리연산

## 1. 실수(Floating Number)
- 소수점이 있는 숫자
- float, double 두 종류가 존재
- 기본형태가 double로 설정됨
- 정확하게 계산되지 않음 (부정확성)	-> 정수와 구분해서 사용하는 이유, so 자주사용X
- int < long < float < double

```java
//  float a = 1.234;  -> ERROR, 기본형태가 double 	이므로
		float a = 1.234f;	//선언값 뒤에 f(F) 표기를 해야됨
		double b = 2.345;
	
		System.out.println(a);
		System.out.println(b);
		
		float c = 1.2345468754635451356f;
		double d = 1.2345468754635451356;	//float, double -> 출력되는 소수 자리수 차이
	
		System.out.println(c);
		System.out.println(d);
		
		//(*중요) 실수가 포함된 계산은 결과가 실수
		System.out.println(1.5 + 2.5);	// 4와 4.0은 다르다
		System.out.println(10 / 3.0);		// 소수점 끝에 5가 나오는 이유 -> 부정확성
		System.out.println(10 / 3d);	
		System.out.println(10 / 3f);
```

## 2. 논리
- true(참), false(거짓)을 저장하기 위한 형태
- 자료형의 이름은 boolean

```java
    boolean a = true;
		boolean b = false;
		
		System.out.println(a);
		System.out.println(b);

		//(Q) 가진돈이 2만원일 때, 8천원짜리 자장면과 1만5천원짜리 탕수육을 시킬 수 있나요?
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
(Q) 어떤 사람의 나이가 "청소년" 에 해당 하는지 판정하세요
  청소년이란, 나이가 14살 이상 20살 미만을 의미한다.
		
			int age = 17;
			
//		boolean teenager = 14 <= age <20;	-> ERROR!!
			boolean teenager = 14 <= age && age < 20;	// and 연산 사용
			
			System.out.println("청소년 인가?");
			System.out.println(teenager);
		
			
(Q) 어떤 사람의 나이가 "무임승차" 대상인지 판정하세요
  영유아(8세 미만) 또는 어르신(65세 이상)인 경우
		 
			boolean free = age < 8 || age >= 65;
			
			System.out.println("무임승차 대상인가?");
			System.out.println(free);
