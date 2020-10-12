# How to encode and decode Korean GET parameter
URL GET 방식으로 한글 파라미터를 넘길 때, 인코딩하고 디코딩하는 JavaScript 및 JAVA 코드를 정리합니다.  
.jsp에서 ajax로 통신을 할 때, 한글 파라미터의 인코딩때문에 외계어가 생기는 문제가 발생했습니다..

## JavaScript로 인코딩
```JavaScript
encodeURI(encodeURIComponent(한글 파라미터));
```
URL에 GET 파라미터를 붙일 때, 위 코드를 이용합니다.

## JAVA로 디코딩
```JAVA
URLDecoder.decode(request.getParameter("한글 파라미터"), "UTF-8"));
```
여기서 decode() 함수는 java.net.URLDecoder에 구현된 static 함수입니다.