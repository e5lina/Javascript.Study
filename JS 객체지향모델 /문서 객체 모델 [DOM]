# 객체 모델

## 문서 객체 모델 ( *DOM* )

- **이벤트(*Event*)**
    - 마우스 이벤트
        
        ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF%20cb19095e59594ff0a1b52506c0a191a0/Untitled.png)
        
    - 문서 로딩 이벤트
    - 폼 이벤트
    - 이벤트 핸들러
        
        ***Event Handler*는 이벤트가 발생했을 때 실행되는 함수입니다. 이벤트를 감지하고, 해당 이벤트에 대응하여 원하는 동작을 수행하는 역할을 합니다.**
        
- **문서 객체 모델 ( *DOM* )**
    - ***DOM* 트리**
        
        *DOM* 구조는 나무처럼 생겼다
        *DOM*은 *body*를 부모 요소로 *h1*, *p*를 자식 요소로 이해하고 구조화함
        
        - *DOM* 트리(*Tree*)라고 칭함
        
        ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF%20cb19095e59594ff0a1b52506c0a191a0/Untitled%201.png)
        
        *DOM* 트리는 가지와 노드로 표현
        
        - *DOM* 트리는 웹 문서의 모든 것을 표현
        *ex*) *HTML*의 요소가 품고 있는 텍스트, 이미지 등
        - ***HTML*은 시작 노드 (나무의 뿌리)**
    - **노드**(***Node***)
        - 웹 문서에 있는 모든 요소 ( ***Element*** )나 속성을 나타냄
    - **가지**
        
        노드와 노드 사이의 연결 관계
        
    - ***CSS*** 선택자
        - ***id*** 선택자
            
            해당 태그의 *id* 속성
            id 속성 값은 한 문서 안에서 유일하기 때문에 자주 사용
            => getElementById()로 DOM 요소에 접근
            
            ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF%20cb19095e59594ff0a1b52506c0a191a0/Untitled%202.png)
            
        - ***class*** 선택자
            - ***getElementsByClassName***()로 *DOM* 요소에 접근
            => *class* 선택자는 *id* 선택자와 다르게 웹 문서 안에서 여러 번 사용 가능
            
            ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF%20cb19095e59594ff0a1b52506c0a191a0/Untitled%203.png)
            
            - 만약 1개의 요소만 접근하고 싶다면 배열의 인덱스 사용
            
            ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF%20cb19095e59594ff0a1b52506c0a191a0/Untitled%204.png)
            
        - ***getElementById*()**와 ***querySelector*()** 차이
            - ***getElementById***()는 단순히 id 선택자를 사용해서 요소에 접근하지만 ***querySelector***()는 *id* 선택자뿐만 아니라 ***querySelector***("#*container* > *ui*")처럼 둘 이상의 선택자를 사용해서 요소에 접근 가능!
    - ***Node*** 만들기
        - ***createElement()***
        - ***createTextNode()***
        - ***appendChild()***
        - ***getAttribute()***
        - ***setAttribute()***
            
            해당 요소에 속성 값 설정(세팅)
            
            ```jsx
            //큰 이미지를 선택하여 변수에 저장
            var bigPic = document.querySelector("#cup")
            //작은 이미지를 선택하여 변수에 저장 (All을 안하면 첫번째꺼만 저장됨)
            var smallPic = document.querySelectorAll(".small")
            
            for(var i =0; i<smallPic.length; i++) {
                smallPic[i].onclick = showBig;
            }
            
            function showBig () {
                var newPic = this.src;
                bigPic.setAttribute("src", newPic);
            }
            
            //setAttribute를 사용하여 작은 이미지중에 클릭하는 이미지를 크게 띄우는 기능코드
            ```
            
        - ***createAttribute*()**
        - ***removeChild()***
    - ***addEventListener*()**
        - 여러개의 이벤트를 처리할때 사용하는 함수
        - ***EventListener***는 DOM 객체에서 이벤트가 발생할 경우 해당 이벤트 처리 핸들러를 추가할 수 있는 오브젝트이다.
        - ***addEventListener***를 이용하면 특정 DOM에 위에 말한 Javascirpt 이벤트가 발생할 때 특정 함수를 호출한다.
            - ***EventListener***를 삭제할때는 ***removeEventListener***를 사용한다
        
        ```jsx
        var pic = document.querySelector('#pic');
            pic.addEventListener("mouseover", changePic, false) 
            // ("어떤행동", 어떤이미지, 캡쳐링)
            pic.addEventListener("mouseout", originPic, false)
            // ("어떤행동", 어떤이미지, 캡쳐링)
            document.addEventListener("click", function() {
              alert("안녕")
            })
        
        		function changePic() {			
        			pic.src = "images/boy.png";
            }
            function originPic() {
              pic.src = "images/girl.png";
            }
        
        //마우스를 올리면 남자이미지가 내리면 여자이미지가 보이게 코드 작성
        ```
        
    - ****버블링과 캡처링****
        - **버블링**(***bubbling***)
            - 이벤트 버블링이란 한 요소에 이벤트가 발생하면 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작하고 최상단의 부모 요소를 만날 때까지 반복되면서 핸들러가 동작하는 현상을 말한다.
                
                ```jsx
                <body>
                    <div class="DIV1">
                      DIV1
                      <div class="DIV2">
                        DIV2
                        <div class="DIV3">DIV3</div>
                      </div>
                    </div>
                  </body>
                const divs = document.querySelectorAll("div");
                
                const clickEvent = (e) => {
                  console.log(e.currentTarget.className);
                };
                
                divs.forEach((div) => {
                  div.addEventListener("click", clickEvent);
                });
                /* div를 클릭하면 해당하는 클래스의 이름이 콘솔로 출력되는 코드이다. 자바스크립트는 기본적으로 버블링이 발생하기 때문에 <div class="DIV3">DIV3</div>를 클릭한다면 콘솔에는 DIV3, DIV2, DIV1이 순서대로 출력이 될 것이다. */
                ```
                
        - **캡쳐링**(***capturing***)
            - 캡처링은 버블링과는 반대로 최상위 태그에서 해당 태그를 찾아 내려간다.
        - ***event.stopPropagation*()**
            
            이벤트 전파를 막는 함수
            
        
    - **노드 활용**
        - ***childNodes***
        - ***hasChildNodes()***
        - ***insertBefore()***
            
            첫번째인수 - 추가하는함수, 기존노드
            
            추가하고 싶은 자리에 추가가능
            
        - ***removeChild()***
        - ***appendChild()***
        
