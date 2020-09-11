# window.location
개발 도중 현재 페이지의 프로토콜과 GET으로 보낸 파라미터 등을 이용해야 했다.  
그래서 알아본 결과, window.location 객체 내부에 활용할 수 있는 변수들이 몇 가지 존재한다.
1. window.location.href : GET으로 보낸 파라미터를 포함해 현재 페이지의 전체 주소를 리턴한다.  
e.g. https://search.naver.com/search.naver?sm=top_hty&fbm=1&ie=utf8&query=%EA%B2%80%EC%83%89%EC%96%B4
1. window.location.hostname : 현재 페이지의 도메인 이름을 리턴한다.  
e.g. search.naver.com
1. window.location.pathname : 현재 페이지의 경로를 리턴한다.  
안타깝게도 GET으로 보낸 파라미터는 포함하지 않는다.  
e.g. /search.naver
1. window.location.protocol : 현재 사용중인 프로토콜을 리턴한다.  
e.g. http: 혹은 https: