# Create a Maven project
이 가이드는 윈도우 환경에서 JDK, Maven을 설치하고, Maven 프로젝트를 생성하기까지의 과정을 다룹니다.

## JDK 설치
혹시 컴퓨터에 Java SE Development Kit (이하 JDK) 가 설치되어 있지 않다면, 우선적으로 JDK를 설치해야 합니다.
1. 아래 URL에서 원하는 버전의 JDK 설치 파일을 다운받아, 설치를 진행합니다.  
[JDK 다운로드 URL](https://www.oracle.com/java/technologies/javase-downloads.html)
1. 시스템 속성에서 환경 변수를 설정합니다.  
(윈도우 검색에서 '환경 변수'를 입력하면 편리하게 찾을 수 있습니다.)
    - JAVA_HOME : $설치한_JDK_폴더의_경로 (e.g. C:\Program Files\Java\jdk-14.0.2)
    - Path에 추가 : %JAVA_HOME%\bin
1. cmd에 아래 명령어를 입력한 후, 설치된 Java 버전의 정보가 나오면 성공입니다.
```cmd
C:\Users\nhlnhl>java -version
java version "14.0.2" 2020-07-14
Java(TM) SE Runtime Environment (build 14.0.2+12-46)
Java HotSpot(TM) 64-Bit Server VM (build 14.0.2+12-46, mixed mode, sharing)
```

## Maven 설치
Maven이란 프로젝트를 빌드하고 라이브러리를 관리해주는 도구입니다.  
Maven 프로젝트를 생성하기에 앞서, Maven을 설치해야 합니다.
1. 아래 URL에서 원하는 버전의 Maven 압축 파일을 다운받습니다.  
이 가이드는 윈도우 환경을 기반으로 하므로, .zip 파일을 다운받습니다.  
[Maven 다운로드 URL](http://maven.apache.org/download.cgi)
1. 원하는 위치로 다운받은 압축 파일을 압축해제시킵니다.
1. 시스템 속성에서 환경 변수를 설정합니다.
    - Path에 추가 : $압축해제한_폴더내_bin_폴더의_경로 (e.g. D:\apache-maven-3.6.3\bin)
1. cmd에 아래 명령어를 입력한 후, 설치된 Maven 버전의 정보가 나오면 성공입니다.
```cmd
C:\Users\nhlnhl>mvn -v
Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)
Maven home: D:\apache-maven-3.6.3\bin\..
Java version: 14.0.2, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-14.0.2
Default locale: ko_KR, platform encoding: MS949
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```

## Maven 프로젝트 생성
이상 JDK와 Maven의 설치가 완료되었으니, 본격적으로 Maven 프로젝트를 생성해봅니다.
1. 원하는 경로로 이동한 후, cmd에 아래 명령어를 입력합니다.
```cmd
mvn archetype:generate
```
2. 필터, 버전, 그룹 아이디, 프로젝트 아이디, 패키지 등 프로젝트를 생성하는 데 필요한 정보들을 기입해줍니다.  
일부 정보의 경우, default 설정을 원한다면 엔터를 클릭합니다.
