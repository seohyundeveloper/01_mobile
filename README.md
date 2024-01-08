- **반응형**에 대해 배우면서 배운 내용에 대해 기록하는 곳입니다.  
  - **CSS Nesting**
    - 예) 버튼만들기
           목적별로 나누기 (다중클래스) 사용하기
    - 예) 갤러리 형태 만들기
            갤러리의 형태에 따라 나눠서 코드짜기
  - **layer** 이용해서 우선순위를 정하기
    - layer이용한 사용법 익히기
    - layer이용한 nesting을 할때 & 기호를 사용하여 그 안에 자식을 나타내준다.
      태그를 직접적으로 써주는것보다 클래스를 선택해서 사용하는것을 추천한다.
    - 클래스명 다음에 & 기호가 오는경우 해당클래스를 부모로 가지는 경우 해당된다.
  - 예)
     ```
      <div style="--order:1"><button class="btn-search" aria-label="검색"></button></div>
      <div style="--order:3">
        <button class="btn-menu" aria-label="메뉴"></button>
        <button class="btn-menu" aria-label="메뉴"></button>
      </div>
    ```
    ```
     @layer 레이어이름 {
        > div {
            &[style*="1"] {
              스타일 속성중에 1이 들어있는경우를 잡아준다.
            }
          }        
     }
    해당 layer이름 안의 div들 중에서 해당 속성에 따라 스타일줄때 사용해준다.
    ```


