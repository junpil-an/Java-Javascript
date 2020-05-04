# eclipse 환경 

#### 1. 폰트 설정
- perspective -general- appearance - colors and pont
  - textfile 설정
  - web/encoding 설정
  -server runtime environments -tomcat 버전에 맞게 설정
  - webserver - serverruntimes 버전 설정

#### 2. servers 새로 만들기 
- `servers` - `new` - `tomcat` 버전에 맞게 생성 

#### 3. project 생성
- `file` - `new` -`Dynaminc web project` - `project web module version` **3.1**으로 지정


#### 4. project html 생성
- `first_project`  - `WebContent` - `index.html`(맨 기본 창 이름은 `index`로 설정해 둘 것)



#### 5. 생성된 html , 서버에 연동 
- `servers` - `add and remove`   - 서버 실행


#### 6. html 실행
- "http://www.localhost:8080" 
  - "8080" 은 port 번호

#### 7. ip 주소확인 방법
- `cmd`창에다  `ipconfig` 입력 
  - IPv4 주소 `192.169.0.133`

#### 8. server 환경 settings

`server.xml` - `source`
서버가 사용하는 포트를 변경하기 위해
- 63  <Connector connectionTimeout="20000" port="8080" protocol="HTTP/1.1" redirectPort="8443"/>
  - 8080 -> 80 변경
  - 80으로 설정하면 굳이 80을 생략하고 입력 가능하다
  - "http://www.localhost/first_project/"  8080 없이 80으로 실행**(80 은 생략이 가능하다)**

## 방화벽 설정

- `네트워크` - `폴더` - `속성 하단 윈도우 방화벽` - `고급설정`

-`인바운드 규칙`(접속하려는 새로은 port 생성) - `새 규칙` - `포트(O)` - `특정 로컬 포트`(설정)




- server   <-  client  /request
- server	 ->	 client  /response


#sigle pair wise?

meta -정보 charset(charactor set) 
8bit = 1byte

utf -8  사용하는 이유
+
- server   <-  client  /request
- server	 ->	 client  /response

피코세컨드??

