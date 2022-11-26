# float가 어떻게 작동하는지 설명하시오

> float는 CSS 위치 지정 속성이다

float된 요소는 페이지 흐름의 일부가 되며, 페이지의 흐름에서 제거되는 position : absolute 요소와 달리 다른 요소의 위치에 영향을 준다

CSS clear 속성은 float 요소에 left/right/both에 위치하도록 사용될 수 있습니다.

부모 요소에 float 요소만 있으면 그 높이는 무효가 된다.
컨테이너의 float 요소 다음에 있지만 컨테이너가 닫히기 전에 float clear 하면 해결할 수 있다.
