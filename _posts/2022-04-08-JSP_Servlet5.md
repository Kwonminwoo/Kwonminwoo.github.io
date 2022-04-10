---
layout: single
title:  "JSP/Servlet JSP #5"
categories: JSP/Servlet
tag: [JSP/Servlet, 프로젝트, Backend, blog, github]
toc: true
---

# JSP request, response
- request.getParameter()메소드를 이용해 클라이언트가 보낸 데이터를 받음
- requset.getParameterValues()메소드는 배열로 데이터를 받음
<br>
- response.sendRedirect()메소드를 이용해 클라이언트에게 메시지를 전달함
```jsp

<%
	response.sendRedirect("abc.jsp");
%>
```
위 처럼 하면 abc.jsp 파일이 호출되어짐 (조건문을 이용해 활용 가능할 듯) 

# JSP 내장 객체

## config
- web.xml에서 원하는 파일에 데이터를 공유하기 위해사용
```xml
<servlet>

	<init-param>
		<param-name>adminId</param-name>
		<param-value>qwer</param-value>
	</init-param>
</servlet>
```
servlet태그 안에 넣음 (넣은 servlet파일 에서만 공유가 가능)<br>
name - value값으로 사용됨.
```jsp
config.getInitParameter(name값);
```
위와 같이 호출함.

## application
```xml
<context-param>
	<param-name>imgDir</param-name>
	<param-value>/upload/img</param-value>
</context-param>
```
servelt 태그 안에 작성하지 않는다. app에 속해 있는 모든 파일에서 공유가 됨<br>
```jsp
application.getInitParameter(name값);
```
위와 같이 호출함.
```jsp
application.setAttribute(name, value);
(String) application.getAttribute(name);
```
위와 같이 값들을 설정도 가능하고 불러오는것도 가능하다 불러올 때는 String으로 형변환이 필요하다.