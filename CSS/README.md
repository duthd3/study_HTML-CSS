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

## 색상과 배경
  - 웹에서 색상 표현하기
    - 1.16진수 표기법
      - ##RRGGBB(빨간색,초록색,파란색)
    - 2.rgb와 rgba표기법
    ```html
      rgb(red 값, green값, blue값);
      rgba(red 값, green값, blue값, alpha값);(alpha는 불투명도 값을 나타낸다.)
      
      color:rgb(255, 0 , 0) //빨간색 표현
    ```
    - 3.hsl과 hsla표기법
      ```html
      hue(색상), saturation(채도), lightness(밝기)
      hsl(<hue 값>, <saturation 값>, <lightness 값>);
      hsla(<hue 값>, <saturation 값>, <lighteness 값>, <alpha 값>);
      ```
    - 4.색상이름 표기법
      - black;
      - red;
  - 배경 색과 배경 이미지
    - 1.background-color속성:배경 색 지정하기
      ```html
      background-color:<색상>
      ```
      - background-color값은 상속x
      
    - 2.background-clip속성:배경 적용 범위 조절하기
      ```html
      background-clip: border-box|padding-box|content-box
      ```
    - 3.background-image속성: 웹 요소에 배경 이미지 넣기
      ```html
      background-image:url(파일경로)
      ```
    - 4.background-repeat속성:배경 이미지 반복 방법 지정하기
      ```html
      background-repeat:repeat|repeat-x|repeat-y|no-repeat
      ```
    - 5.background-size속성: 배경 이미지 크기 조절하기
      ```html
      background-size:auto|contain|cover|<크기 값>|<백분율>
      ```
    - 6.background-position속성: 배경 이미지 위치 조절하기
      ```html
      background-position:<수평위치><수직위치>;
      수평위치: left|center|right|<백분율>|<길이 값>
      수직위치: top|center|bottom|<백분율>|>길이 값>
      ```
      
    - 7.background-origin속성:배경 이미지 배치할 기준 조절하기
      ```html
      background-origin:border-box|padding-box|content-box
      ```
      
    - 8.background-attachment속성: 배경 이미지 고정하기
      ```html
      background-attachment:scroll|fixed
      ```
     
    - 9.background속성: 속성 하나로 배경 이미지 제어하기
      
## 그라데이션효과로 배경 꾸미기
  - 1. 그라데이션과 브라우저 접두사
    - -webkit-:사파리5.1~6.0
    - -moz-:파이어폭스3.6~15
    - -o-:오페라11.1~12.0
  - 2. 선형그라데이션
    ```html
      linear-gradient(<각도> to <방향>, color-stop, [color-stop,...]);
    ```
    - 방향
      - to top:아래에서 위로
      - to left:오른쪽에서 왼쪽으로
      - to right:왼쪽에서 오른쪽으로
      - to bottom:위에서 아래로
  - 3. 원형그라데이션
    - 동심원을 그리며 바깥 방향으로 색상이 바뀐다.
      - 모양
      ```html
      radial-gradient(<최종모양><크기>at<위치>, color-stop, [color-stop...])
      ```
      - 위치
      - 크기
        - closest-side속성 값(가장 가까운 요소의 수평축이나 수직축)
        - closest-corner속성 값(가장 가까운 요소의 코너)
        - farthest-side속성 값(가장 먼 모서리)
        - farthest-corner속성 값(가장 먼 코너)
      
 ## CSS와 박스모델
   - 1.블록 레벨 요소와 인라인 레벨 요소
     - 블록 레벨 요소는 태그를 사용해 요소를 삽입했을 때 혼자 한 줄을 차지
     - 인라인 레벨 요소는 줄을 차지하지 않는 요소.
     ```html
      블록 레벨 태그:<p>,<h1>~<h6>,<ul>,<ol>,<div>,<blockquote>,<form>,<hr>,<table>,<fieldset>,<adress>
      인라인 레벨 태그:<img>,<object>,<br>,<sub>,<sup>,<span>,<input>,<textarea>,<label>,<button>
     ```
   - 2.박스 모델 - 박스 형태의 콘텐츠
     - 박스모델은 실제 콘텐츠영역, 패딩, 테두리, 마진등의 요소로 구성된다.
     ```html
      -콘텐츠 영역의 크기지정
      width:<크기>|<백분율>|auto
      height:<크기>|<백분율>|auto
     ```
   - 3.display속성:화면 배치 방법 결정하기
     - 블록 레벨 요소를 인라인 레벨 요소로, 인라인 레벨 요소를 블록 레벨 요소로 바꿀 수 있다.
     ```html
      display: none|contents|block|inline|inline-block|table|table-cell
     ```
      
## 테두리 관련 속성들
  - 1.border-style속성:테두리 스타일 지정하기
    ```html
      border-style:none|hidden|dashed|dotted|double|groove|inset|outset|ridghe|solid
      dashed:직선으로 된 점선
      dotted:점선
      double:이중선    
      solid:실선
    ```
  - 2.border-width속성:테두리 두께 지정하기
    ```html
      border-top-width:<크기>|thin|medium|thick
      border-right-width:<크기>|thin|medium|thick
      border-bottom-width:<크기>|thin|medium|thick
      border-left-width:<크기>|thin|medium|thick
      border-width:<크기>|thin|medium|thick
    ```
  - 3.border-color속성:테두리 색상 지정하기
    ```html
      border-top-color:<색상>
      border-right-color:<색상>
      border-bottom-color:<색상>
      border-left-color:<색상>
      border-color:<색상>    
    ```
  - 4.border-radius속성:박스 모서리 둥글게 만들기
    ```html
      border-top-left-radius:<크기>|<백분율>
      border-top-right-radius:<크기>|<백분율>
      border-bottom-right-radius:<크기>|<백분율>
      border-bottom-left-radius:<크기>|<백분율>
      border-radius:<크기>|<백분율>
    ```
  - 5.box-shadow속성:선택한 요소에 그림자 효과 내기
    ```html
      box-shadow:none|<그림자 값>
      <그림자 값>:<수평거리> <수직거리> <흐림 정도> <번짐정도> <색상> 
    ```    
      
## 여백을 조절하는 속성들
  - 1.margin속성:요소 주변 여백 설정하기
    ```html
      margin-top:<크기>|<백분율>|auto
      margin-right:<크기>|<백분율>|auto
      margin-bottom:<크기>|<백분율>|auto
      margin-left:<크기>|<백분율>|auto  
    ```   
  - 2.padding속성:콘텐츠 영역과 테두리 사이 여백 설정하기
    ```html
      padding-top:<크기>|<백분율>|auto
      padding-right:<크기>|<백분율>|auto
      padding-bottom:<크기>|<백분율>|auto
      padding-left:<크기>|<백분율>|auto
      padding:<크기>|<백분율>|auto  
    ```     
        
## CSS 포지셔닝과 주요 속성들
  - 1.CSS 포지셔닝
    - 여러 요소를 적절한 위치에 배치.
  - 2.box-sizing속성:박스 너비 기준 정하기
    ```html
      box-sizing:content-box|border-box
      
      content-box:width속성 값을 콘텐츠 영역 너비 값으로 사용. 기본값
      border-box:width속성 값을 콘텐츠 영역에 테두리까지 포함한 박스 모델 전체 너비 값으로 사용.
    ```    
  - 3.float속성:왼쪽이나 오른쪽으로 배치하기
    ```html
      float:left|right|none
    ```
  - 4.clear속성:float속성 해제하기
    - float속성이 더 이상 유용하지 않다고 알려주는 속성이 clear속성이다.
    ```html
      clear:none|left|right|both
    ```
  - 5.position속성:배치 방법 지정하기
    - 웹 문서 안의 요소들을 자유자재로 배치해 주는 속성.
    ```html
      position:static|relative|absolute|fixed
      (static:요소를 문서의 흐름에 맞추어 배치.)
      (relative:이전 요소에 자연스럽게 연결해 배치하되 위치를 지정할 수 있다.)-좌표
      (absolute:원하는 위치를 지정해 배치.)-좌표
      (fixed:지정한 위치에 고정해 배치.)-좌표
    ```
    - absoulte속성 값을 사용하려면 그 요소를 감싸는\<div>를 만들고 position을 relative로 지정해 놓고 사용해야 한다.
        
  - 6.visibility속성:요소를 보이게 하거나 보이지 않게 하기      
    ```html
      visibility:visible|hidden|collapse
    ```    
  - 7.z-index속성:요소 쌓는 순서 정하기
    ```html
      z-index:<숫자>
    ```
    - 숫자가 작을수록 아래에 쌓이고 클수록 위에 쌓인다.    
        
## 다단으로 편집하기
  - column-width:단의 너비 고정하고 다단 구성하기
    ```html
      column-width:<크기>|auto
    ```
  - column-count속성:단의 개수 고정하고 다단 구성하기
    ```html
      column-count:<숫자>|auto
    ```
  - column-gap속성:단과 단 사이 여백 지정하기
    ```html
      column-gap:<크기>|normal
    ```
  - column-rule속성:구분선의 색상, 스타일, 너비 지정하기
    ```html
      column-rule-color:<색상>
      column-rule-style:none|hidden|dotted|dashed|solid
      column-rule-width:<크기>|thin|medium|thick
      column-rule:<너비><스타일><색상>
    ```
  - break-after속성: 다단 위치 지정하기
    ```html
      break-after:column|avoid-column
      break-before:column|avoid-column
      break-inside:column|avoid-column
    ```
  - column-span속성:여러 단을 하나로 합치기
    ```html
        column-span:1|all
    ```
      
      
      
      
    
  
      
      
