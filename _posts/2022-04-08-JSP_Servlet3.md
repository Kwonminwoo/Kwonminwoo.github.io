---
layout: single
title:  "JSP/Servlet Servlet #3"
categories: JSP/Servlet
tag: [JSP/Servlet, 프로젝트, Backend, blog, github]
toc: true
---

# Servlet request, response
request = 클라이언트의 요청<br>
요청방식에 따라 doGet, doPost 메소드에서 처리한다.<br>
requset.getParameter()등의 메소드를 이용해 처리<br>
response = 서버가 클라이언트에게 보내줄 메시지 (뷰)<br>
마찬가지로 보내줄 방식을 정해 doGet, doPost 메소드에서 처리한다.<br>
response.getWriter() 등의 메소드를 이용해 처리<br>

# Servlet Life-Cycle
1. @PostConstruct
2. init()
3. service()
4. destroy()
5. @PreDestroy

- @PostConstruct는 Annotation으로 작성하고자 하는 메소드 위에 달아주면 기능을 하게됨.
준비단계이다.
- init()메소드는 생성되었을 때 콜백 보통 초기화하는데 많이 씀
- service()메소드는 실질적인 처리를 하는 메소드 doGet, doPost메소드로 대처하기도 함
- destroy()메소드는 종료되었을 때 콜백 자원을 해체 (.close)와 같은 것을 할 때
- @PreDestroy도 Annotation으로 사용하고 종료 이후 할 것을 작성.
