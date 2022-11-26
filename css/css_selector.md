## CSS selector

> CSS 선택자란 말 그대로 선택을 해주는 요소이며 이를 통해 특정 요소들을 선택하여 스타일을 적용할 수 있다

## 종류

- id(id 선택자): `#header`, `#footer`
  - `#` 사용
    - id 속성을 가진 모든 태그를 선택해 css 적용
    - 한 페이지 내에서 단 한번, 유일하게 적용될 스타일은 id selector 사용
    - class selector 보다 우선순위가 높아 우선적으로 사용되어야 할 스타일에 지정
- class(클래스 선택자): `.container`
  - `.` 사용
    - class 속성을 가진 모든 태그를 선택해 css 적용
    - 한 페이지 내에서 여러번 반복될 필요가 있는 스타일은 class selector 시용
    - 속성 값을 두개 이상 가질 수 있음
    - 다른 곳에도 적용할 수 있는 스타일을 지정
- tag(태그 선택자): `div`, `a`, `p`

- universal(전체 선택자) : `*`
  - html 페이지 내부의 모든 요소에 같은 css 속성 적용
    - 기본값을 정해줄 때 사용

## 우선 순위

1. 속성 값 뒤에 !important를 붙인 속성 : 강제하는 것
2. HTML의 각 태그에서 style을 직접 지정한 속성
3. id selector
4. class selector
5. tag selector
6. 상위 객체에 의해 상속된 속성
