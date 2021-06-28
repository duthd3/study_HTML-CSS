# CSS

## CSS기초
- 스타일과 스타일 시트
  - 웹 문서의 디자인과 내용을 분리한다.
  - CSS로 웹 문서의 내용과 상관없이 디자인만 바꿀 수 있다.
  - 다양한 기기에 맞게 탄력적으로 바뀌는 문서를 만들 수 있다.
    - 모바일용 홈페이지, 인쇄용지 등등
  ```html
  p { text-align: center} 
  p:선택자
  {}:중괄호
  속성
  =><p>태그가 적용된 텍스트 단락에 중괄호 사이의 스타일을 적용한다는 뜻
  속성은 ; 으로 구분한다.
  ```
  
  - 내부 스타일
    - 내부 스타일 시트는 웹문서 안에서 사용할 스타일을 문서 안에서 정리한 것이다.
    - \<head>,\</head>태그 안에서 정의해야 하고 \<style>,\</style>태그 사이에 작성한다.
     
  - 외부 스타일   
    - 외부 스타일 시트는 스타일을 별도 파일로 저장하고, 저장해 놓은 스타일 정보를 가져와서 사용한다. '.css'라는 파일 확장자를 사용한다.
    - 외부 스타일 시트를 연결할 때는<stlye>태그 없이 <link>태그만 사용해 미리 만들어 놓은 외부 스타일 시트 파일을 연결한다.

- 주요 선택자
  ```html
    전체 선택자: 모든 요소에 스타일 적용.
    *{속성:속성값; 속성:속성값;...}
  
  ```
  ```html
    태그 선택자: 특정 태그를 사용한 요소에 스타일 적용하기
    태그{스타일}
  ```
  
  ```html
    클래스 선택자: 특정 부분에 스타일 적용하기
    .클래스명{스타일}
    태그에 class="클래스이름"을 적용해서 어느 태그에서나 사용할 수 있다.
    <h2 class = "bluetext">
    텍스트 일부에만 클래스 스타일을 적용할 수도 있다.<span>태그 사용
    <p>.................<span class="bluetext">...</span></p>    
  ```
      
  ```html
    id 선택자: 특정 부분에 스타일 적용하기
    #아이디명{스타일}
    문서 안에서 한번만 적용할 수 있다. 즉, 중복해서 사용할 수 없다.    
  ```
  ```html
    그룹 선택자: 둘 이상 요소에 같은 스타일 적용하기
    h1,h2{
      text-align:center;
      }
  ```    
      
## 텍스트 관련 스타일
- 1.글꼴 관련 스타일
  - font-family속성:글꼴 지정하기
    
  ```html
    font-family:<글꼴이름>
    font-family:"맑은 고딕", 돋움, 굴림 //맑은 고딕이 없을때를 대비
  ```
      
  - @font-face 속성: 웹 폰트 사용하기
    - 웹 문서 안에 글꼴정보도 함께 저장하고 사용자가 웹문서에 접속하면 글꼴을 사용자 시스템으로 다운로드시키는 방식.
    ```html
    @font-face{
      font-family:글꼴 이름;
      src:url.fomat;
    }
    ```
    
   - font-size 속성:글자크기 조절하기
      ```html
      font-size:<절대크기>|<상대크기>|<크기>|<백분율> (4종류의 유형)
      ```
     - px단위 사용
       - 웹에서 주로 사용. 모바일에서 불리.
     - em단위 사용
       - 부모 요소에서 지정한 폰트의 대문자  M의 너비를 1em 기준으로 상대적 값을 계산.
    
   - font-weight 속성:글자 굵기 지정하기
      ```html
      font-weight:normal|bold|bolder|lighter|100|200|300|400|500|600|700|800|900
      ```
   - font-variant 속성: 작은 대문자로 표시하기
      ```html
      font-variant:normal|small-caps
      ```
   - font-style 속성:글자 스타일 지정하기
      ```html
      font-style:normal|italic|oblique
      ``` 
  - 2.텍스트 스타일
      - color속성:글자 색 지정하기
      ```html
      color:<색상>
      ```
      
      - text-decoration속성:텍스트에 줄 표시하기/없애기
      ```html
      text-decoration:none|underline|overline|line-through
      ```
      
      - text-transform속성:텍스트 대,소문자 변환하기
      ```html
      text-transform:none|capitalize|uppercase|lowercase|full-width
      ```
      - capitalize: 시작하는 첫 번째 글자를 대문자로 변환한다.
      - uppercase: 모든 글자를 대문자로 변환한다.
      - lowercase: 모든 글자를 소문자로 변환한다.
      - full-width: 가능한 모든 문자를 전각 문자로 변환한다.
      
      - text-shadow속성: 텍스트에 그림자 효과 추가하기
      ```html
      text-shadow: none|<가로거리><세로거리><번짐 정도><색상>
      ```
      
      - white-space속성: 공백 처리하기
      ```html
      white-space:normal|nowrap|pre|pre-line|pre-wrap
      ```
      
      - letter-spacing, word-spacing속성:텍스트 간격 조절하기
      ```html
      letter-spacing:normal|<크기>
      word-spacing:normal|<크기>
      ```
      
- 3.문단 스타일
    - direction속성:글자 쓰기 방향 지정하기
    ```html
    direction:ltr|rtl
    ```
      - ltr:왼쪽에서 오른쪽으로 텍스트 표시. 기본형.
      - rtl:오른쪽에서 왼쪽으로 텍스트 표시.
    - text-align속성:텍스트 정렬하기
    ```html
    text-align:start|end|left|right|center|justify|match-parent
    ```
     
    - text-justify속성:정렬 시 공백 조절하기
    ```html
    text-justify:auto|none|inter-word|distribute
    ```
    
    - text-indent속성:텍스트 들여쓰기
    ```html
    text-indent:<크기>|<백분율>
    ```
      
    - line-height속성:줄 간격 조절하기
    ```html
    line-height:normal|<숫자>|<크기>|<백분율>|inherit
    ```
      
    - text-overflow속성:넘치는 텍스트 표기하기
    ```html
    text-overflow:clip|ellipsis
    ```
- 4.목록 스타일
    - list-style-type속성:목록의 불릿과 번호 스타일 지정하기
    ```html
    list-style-type:none|<순서 없는 목록의 불릿>|<순서 목록의 번호>
    ```
      
    - list-style-image속성:불릿 대신 이미지 넣기
    ```html
    list-style-image:<이미지>|none
    <이미지>=url(이미지 파일 경로)
    ```
      
