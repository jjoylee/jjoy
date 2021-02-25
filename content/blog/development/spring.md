---
title: 'HTTP'
date: 2021-02-13
category: 'development'
draft: true
---

Servlet이란 : 클라이언트 요청을 처리하고 처리결과를 클라이언트에 전달
html을 사용해 요청에 응답
MVC 패턴 중 Controller 이용
HttpServlet 클래스 상속
html 변경시 서블릿 재컴파일

사용자가 url 클릭
HTTP Request를 Servlet 컨테이너로 전송
Http Request를 전달받은 컨테이너는 HttpServletRequest, HttpServletResponse 생성
어느 서블리에 대해 요청을 한 것인지 확인
service 메소드를 호출한후 doGet doPost 호출
페이지 생성한 후 HttpServletResponse 객체에 응답을 보낸다.

클라이언트 요청을 처리하고 그 결과를 다시 클라이언트에게 전송하는 Servlet 클래스의 구현 규칙을 지킨 자바 프로그램" (클라이언트의 HTTP 요청에 대해 특정 기능을 수행, HTML문서를 생성등의 응답을 하는 인터넷 서버 프로그램)

클라이언트 요청 처리 -> 클라이언트에 전송
서블릿 컨테이너 : 서블릿을 관리
서블릿의 생명주기를 관리.웹 서버와 소켓을 만들어 통신
서블릿과 웹 서버가 통신할 수 있는 손쉬운 방법 제공
톰캣 : 서블릿 컨테이너 

웹 서버 
하드웨어 : Web Server가 설치되어있는 컴퓨터
소프트웨어 : 웹 브라우저 클라이언트로부터 http 요청을 받아 정적인 컨텐츠 제공
정적인 컨텐츠 제공
WAS를 거치지 않고 바로 자원 제공
동적인 컨텐츠를 위한 요청 전달
HTTP 요청 -> 웹 서버 -> WAS _> RESPONSE -> 웹서버 -> HTTP RESPONSE 전달

Web Application Server
DB 조회나 다양한 로직 처리를 요구하는 동적인 콘텐츠를 제공하기 위해 만들어짐.
웹 컨테이너, 서블릿 컨테이너
JSP Servlet 구동환경 제공
was = web server + web container
프로그램 실행 환경과 db 접속 기능 제공
웹 페이지는 정적 컨텐츠와 동적 컨텐츠가 모두 존재한다.
정적 컨텐츠는 웹 서버가 담당
동적 컨텐츠는 웹 어플리케이션 서버가 담당

웹 서버는 클라이언트로부터 HTTP 요청을 받는다.
웹 서버는 클라이언트의 요청을 WAS에 보낸다.
WAS는 관련된 Servlet을 메모리에 올린다.
web.xml을 참조해서 해당 Servlet에 대한 Thread 생성
HttpServletRequest와 HttpServletResponse 객체를 생성해서 Servlet에 전달
Thread는 service()메서드 호출
doGet(), doPost() 호출
생성된 동적 페이지를 Response 객체에 담아 전달
Response객체를 HttpResponse로 바꾸어 Web서버에 전달

