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
      
      