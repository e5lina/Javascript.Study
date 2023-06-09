## 브라우저 객체 모델( *BOM* )

- 브라우저에 계층적으로 내장된 객체들을 브라우저 객체 모델이라 한다.
- window는 브라우저 객체의 최상위 객체가 된다.
- ***BOM* 종류**
    
    
    | window | 최상위객체, 각 프레임 별로 하나씩 존재 |
    | --- | --- |
    | navigator | 브라우저명, 버전 정보를 속성으로 가짐 |
    | document | 현재 문서에 대한 정보 |
    | location | 현재 URL에 대한 정보, 브라우저에서 사용자가 요청하는 URL |
    | history | 현재의 브라우저가 접근했던 URL history |
    | screen | 브라우저의 외부환경에 대한 정보 제공 |
    - ***open()***
        
        ```html
        <!DOCTYPE html>
        <html><head><title>open()</title></head><body>
        
            <button onclick="mySite()">naver</button>
            <script>
              function myFunction() {
                window.open("https://www.naver.com", "_blank", "toolbar=yes,scrollbars=yes,resizable=yes,top=500,left=500,width=400,height=400");
              }
            </script>
          </body></html>
        ```
        
- ***Form***
    - 폼은 웹 페이지에서 사용자로부터 데이터를 입력받는 데 사용되는 요소입니다. 폼은 주로 사용자가 텍스트, 숫자, 체크박스 등의 입력 필드를 작성하고, 이를 서버로 전송하거나 클라이언트 측에서 처리하는 데 사용됩니다.
    - 폼 요소는 각각 고유한 식별자(ID)를 가지고 있으며, JavaScript를 사용하여 이 식별자를 통해 폼 요소에 접근하고 조작할 수 있습니다. 예를 들어, 폼 데이터의 값을 읽어오거나 변경할 수 있습니다.
    - 폼은 웹 애플리케이션에서 매우 중요한 부분이며, JavaScript를 통해 동적으로 조작할 수 있습니다. 이를 통해 사용자와의 상호작용을 개선하고 데이터의 유효성을 검사하며, 서버로 데이터를 전송하는 등 다양한 작업을 수행할 수 있습니다.
    - **<*input*>**
        
        텍스트 입력, 비밀번호 입력, 체크박스 등 다양한 형태의 입력 필드를 제공합니다.
        
    - **<*select*>**
        
        드롭다운 목록을 생성하여 선택 옵션을 제공합니다.
        
    - **<*textarea*>**
        
        여러 줄의 텍스트를 입력할 수 있는 텍스트 영역을 제공합니다.
        
    - **<*button*>**
