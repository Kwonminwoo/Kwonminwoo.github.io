---
layout: single
title:  "JSP/Servlet mapping #2"
categories: JSP/Servlet
tag: [JSP/Servlet, 프로젝트, Backend, blog, github]
toc: true
---


# Servlet mapping
매핑이란 요청하는 path를 쉽게 하기 위해서이고, 정보 노출을 최소화 하면서 보안을 좋게 해준다. <br>
ex)폴더명/파일명.jsp 이런식으로 작성하던 것을 -> 폴더명/a 이런식으로 매핑이 가능하다. <br>

## web.xml파일을 이용한 mapping
web.xml은 웹 환경을 설정하는 파일이다.
```xml
<servlet>
	<servlet-name>servletEx</servlet-name>
	<servlet-class>com.servlet.ServletEx</servlet-class>
</servlet>
```
위와 같은 방식으로 servlet을 등록해주고
```xml
<servlet-mapping>
		<servlet-name>servletEx</servlet-name>
		<url-pattern>/SE</url-pattern>
</servlet-mapping>
```
위와 같이 등록된 서블릿을 SE라는 이름으로 매핑시켜준다.
## Annotation을 이용한 mapping
```java
@WebServlet("/Hello")
```
위 방식으로 servlet 파일에서 매핑을 해줄 수 있다. 
<br>
<br>
위 처럼 두가지 방식으로 하면 두 이름모두 사용이 가능해진다. 매핑의 개수 제한은 없다.
