# day01

## HelloJava 
  
```java
package day01;
```
- 모든 파일은 위치 정보를 가장 먼저 작성해야 한다.
- **{}** 영역 표시  /  **;** 실행을 지시

```java
  public class Hello {
```
  - **class**는 자바 프로그램의 가장 기본 단위(파일 이름과 같게 생김)

```java 
	public static void main(String[] args) {
```	
  - **main 메소드**는 프로그램에 반드시 있어야 되는 영역(실행영역)

```java
		System.out.println("Hello!");
	}
}
```
   - **System.out.println();**  화면에 글자를 출력하는 구문


## 출력예시
```java
package day01;

public class Information {
	public static void main(String[] args) {
		System.out.println("박우인");
		System.out.println("황인빈 강사");
		System.out.println("KH정보교육원");
		System.out.println("공공데이터 융합 자바개발자 양성과정5");
	}
}
```
