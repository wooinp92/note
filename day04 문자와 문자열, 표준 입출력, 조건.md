# day04 문자와 문자열, 표준 입출력, 조건
  
## 1. 문자(char)
- 글자에 숫자를 붙여놓은 형태(글자로 써도 되고 숫자로 써도 됨)
- 글자로 쓸 떄는 외따옴표에 한 글자만 넣을 수 있다
- 기본적으로 MS949(CP949) 방식을 따름(윈도우 기준)
- 2byte의 크기를 가짐 (자바는 유니코드 생성 이후에 개발되어 전세계 모든 언어를 지원 함, C언어는 1byte)
  
```java
    char a = 'A';
    char b = 65;
    System.out.println(a);
    System.out.println(b);
		
    char c ='가';	// 한글의 첫번째 글자
    System.out.println(c);
    System.out.println((int)c);
		
    char d= '힣';	// 한글의 마지막 글자	// '힣' 값 - '가' 값 == 한글 총 글자수
    System.out.println(d);
    System.out.println((int)d);
```

## 1-1. 문자열(String)
- 참조형 데이터(reference type)
- 글자수에 따라 크기가 정해지며 예측이 불가능하므로 주문제작 방식
- 참조변수(리모컨)와 객체(본체)로 나눠져서 제작된다

 ```java
    String a = "Hello";
    System.out.println(a);
    System.out.println(a.length());	// a 리모컨에 length 버튼을 눌러라
    System.out.println(a.charAt(0));
 ```

## <문자열의 특징>
- 다른건 안되도 덧셈은 가능
- 특수문자(Escape Sequence)를 사용할 수 있다
- \n : 줄바꿈(NewLine)
- \t : 탭이동(Tab)

```java
    String b = "자바";
    System.out.println(a+b);
//  System.out.println(a-b); -> 불가능한 연산
    System.out.println("a = " + a);
    System.out.println("b = " + b);
		
    System.out.println("안\n녕\n하\n세\n요");

    System.out.println("개수\t\t유료\t\t무료");	//"개수	유료	무료" 탭을 직접 넣어도 되지만 띄어쓰기와 구분이 안되므로 \t 표기를 해주는 것 권장
		
//  (Q)나는 "피자"를 점심에 먹을 예정입니다  를 화면에 출력
    System.out.println("나는 \"피자\"를 점심에 먹을 예정입니다");	//쌍따옴표가 중복되므로 \로 구분 없이 그냥작성하면 ERROR
```

## 2. 표준 입출력(Input/Output, I/O)
- System.out.println은 무슨 뜻인가?
- System.out 은 표준 출력 통로를 의미 (Standard Output Stream)

```java
    System.out.println("한 줄에 걸쳐 출력하는 명령");
    System.out.println(100 + 200 + 300);	//계산을 하면서 출력 가능, but 권장하지 않음
		
    System.out.print("메세지를");
		System.out.print("계속해서");
		System.out.print("이어서 출력합니다");
		
		System.out.print("\n");	// ("\n"); == ();
		
		System.out.printf("%d + %d = %d\n", 10, 20, 30);	//C언어 스타일 출력구문(사용안함)
```

  
      
