# Adobe Acrobat Sign 및 PDF Service 이용하기 
 
Adobe Acrobat Sign과 PDF 서비스 구성하기  
 
## 준비단계 
- Adobe Sign 계정에서 OAuth 어플리케이션 등록하기  
- Adob Sign ClientID 와 ClientSecret 사용하기 
- Adobe 개발자 계정 등록 및 PDF Service API 구성하기 
- UiPath Integration 서비스 등록하기 

### 1. Adobe Acrobat Sign OAuth 등록하기 
아래 그림처럼 Adobe Sign 사이트 로그인 > 계정 선택  
<img src=./img/adobe-sign.png width=600 height=150 alt='Adobe Sign'>  <br/>
Acrobat Sign API 선택 후  API 응용 프로그램 선택  
<img src=./img/adobe-sign-application.png width=300 height=300 alt='Adobe Sign Application'> <br/>
새로운 OAuth 응용 프로그램 성성후 리다이렉션 URL에 (https://integrations.uipath.com/authcallback/authorize/) 입력 후 필요한 항목에 대해서 활성화 선택  
<img src=./img/adobe-sign-oauth-config.png width=600 height=500> <br/>

### 2. Adobe Sign ClientID 와 ClientSecret 사용하기 
아래 그림과 같이 Adobe Sign Scope에서  Base URL을  https://api.na4.adobesign.com 사용하고 필요한 clientId 및 clientSecret 사용  
clientSecret은 SecureString이여 Credential을 사용하는 것이 편리 함  
<img src=./img/adobe-sign-scope.png width=600 height=400> <br/>  
예제에서는 Adobe Folder에 AbobeSignCredential 을 사용함  
<img src=./img/adobe-sign-credential.png width=600 height=150> <br/>

### 3. Adobe 개발자 계정 등록 및 PDF Service API 구성하기  
adobe.com 에 회원 가입 후 console 사이트로 이동  
<img src='./img/adobe-pdf-api.png' width=600 height=466> <br/> 
사용할 키 생성하기  
<img src='./img/adobe-pdf-genkey.png' width=600 height=210> <br/>
API 구성 완료하기  
<img src='./img/adobe-pdf-config-api.png' width=600 height=226> <br/>
Integration 서비스에 등록할 인증 정보는 아래와 같습니다.  
<img src='./img/adobe-pdf-jwt.png' width=600 height=510> <br/> 


### 4. UiPath Integration 서비스에 등록하기 
UiPath Automation Cloud에서 Integration Service에서 Adobe PDF 서비스 선택 
<img src='./img/uipath-integration.png' width=600 height=336> <br/>
Adobe 사이트에서 확인한 값을 입력하면 됩니다. 개인키 부분에 대해서는 키 생성 관련해서 만들어 놓은 private key를 사용. 이때 header/tail 부분인 -----BEGIN PRIVATE KEY----- 와 -----END PRIVATE KEY----- 를 제거하고 입력  
<img src='./img/uipath-integration-setup.png' width=400 height=614> <br/>





