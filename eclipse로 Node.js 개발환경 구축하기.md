# eclipse로 Node.js 개발환경 구축하기

1. JDK를 설치한다.

2. 환경변수 JAVA_HOME을 등록한다.

3. PATH에 %JAVA_HOME%\bin;을 추가한다.

4. eclipse를 JAVA EE를 다운받아 압축을 해제한다.

5. eclipse를 실행한 후 [Help] - [Eclipse Maketplace...] 에서 Nodeclipse 플러그인을  검색하여 설치한다.

6.  프로젝트 종류 중에서 “Node.js Project”를 선택 하여 프로젝트를 생성한다.

7.  [New] - [Java script File]을 선택하여 app.js파일을 생성하고 아래의 내용을 입력합니다.

   ```
   [app.js]
   var http = require('http');
   var fs = require("fs");
   http.createServer(function(req, res) {
    res.writeHead(200, {'Content-Type' : 'text/html'});
    res.write("Hellow Nod1e.js");
    res.end();
   }).listen(4000, function() {
    console.log("server is listening on 4000");
   });
   ```

8. 마우스 우측버튼을 눌러 [Run As] - [Node Application]으로 실행해 봅니다.

9. 웹브라우저를 실행하여 http://localhost:4000 으로 접속해 봅니다.

10.  nodemon 설치하기

     기본적으로 Node.js를 설치하면 수정시 바로 반영되지 않습니다.  
     계속 서버를 재기동시켜야하는 불편함이 있습니다.  
     이 문제를 해결하기 위해서 Nodemon이라는 것을 설치해보도록 하겠습니다.  
     Node.js npm이라는 것을 제공합니다.  
     npm을 이용해서 아래의 빨간 네모처럼 명령어를 입력해줍시다.  
       
     npm install nodemon -g  
          

11.  다음의 위치에 설치가 됩니다.

    C:\Users\Administrator\AppData\Roaming\npm\node_modules\nodemon\bin
    
12.  이후 [Run As] ->[Run Configurations] -> [Arguments] -> [Node Arguments]에 Nodemon의 경로를 입력해 줍니다.  
    
    C:\Users\Administrator\AppData\Roaming\npm\node_modules\nodemon\bin\nodemon.js
    

     

