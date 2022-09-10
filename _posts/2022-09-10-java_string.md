---
date : 2022-09-10
title : "[Java] Java String Method Basic"
comments : true
categories : 
    - Java
---

###### Java String 클래스의 기본적인 메소드들에 관한 정리입니다.
```java
public class Main
{
	public static void main(String[] args) {
// 		String str = new String("Hello");
		String str = "Hello";
		System.out.println(str.length());
        // 문자열 길이 출력
		System.out.println(str.concat("World!"));
        // 문자열 합치기
		System.out.println(str.substring(2,3));
        // 문자열 자르기
		
	}
}

```