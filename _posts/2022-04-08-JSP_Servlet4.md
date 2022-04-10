---
layout: single
title:  "JSP/Servlet JSP태그 #4"
categories: JSP/Servlet
tag: [JSP/Servlet, 프로젝트, Backend, blog, github]
toc: true
---

# JSP 스크립트
jsp는 html과 같이 작성하므로 java 코드를 중간에 삽입 하기 위해 태그를 작성해줘야 함

## 선언 태그
```jsp
<%!
	int a = 0;
	public void methodTest(){
		return;
	}
%>
```
자바 변수, 메소드를 선언

## 스크립트릿 태그
```jsp
<%
	System.out.println("hello");
%>
```
자바의 모든 코드 가능 (실질적 알고리즘)
## 표현식 태그
```jsp
 표현식은 출력 숫자<%=num%> 입니다. 
```
java의 변수 및 메소드의 반환값을 출력. 위와같이 하면 num이 html로 출려됨

## 지시어
```jsp
<%@ include file= "header.jsp" %>
```
설정에 관한 코드들