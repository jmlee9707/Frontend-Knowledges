# Position

**Position 속성은 문서 상에 요소를 배치하는 방법을 지정해주는 속성**

기본값은 static 이며 이외에도 `relative`, `absolute`, `fixed`, `stickey`이 있다.

- `static` : 요소를 왼쪽에서 오른쪽, 위에서 아래로 일반적인 문서 흐름에 따라 배치

- `relative` :
  - 일반적인 문서의 흐름을 유지하면서 자신을 기준으로 top, right, bottom, left의 값에 따라 오프셋을 적용
    - static 위치였을 때를 기준으로 offset을 통해 상대적인 위치에 배치
    - `position : relative` 로 설정 후 offset을 주지 않으면 static과 동일한 위치에 존재
- `absolute` :
  - 요소를 일반적인 문서 흐름에서 제거하고, 가장 가까운 위치 지정 조상 요소에 대해 상대적으로 배치
    - `position : absolute` 인 요소에 offset을 주지 않으면 auto 값(static이였을때 기준으로 위치), 반드시 조상 요소 기준으로 offset 값을 주어 원하는 곳에 위치하도록 함
- `fixed` : 요소를 일반적인 문서 흐름에서 제거하고, 뷰포트의 초기 컨테이닝 블록을 기준으로 삼아 고정 배치
- `sticky` : static + fixed 특징을 동시에 가짐

## 오프셋 (offset)

top, bottom, left, right 값을 의미하고 기준이 되는 곳으로부터 **얼마만큼 떨어져 있는지**를 나타내기 위해 필요한 속성

## 뷰포트 (viewport)

화면에서 실제 내용이 표시되는 영역으로 데스크톰은 사용자가 설정한 해상도가 뷰포트 영역이 되고
스마트 기기는 기본으로 설정되어 있는 값이 뷰포트 영역이 된다.

## 컨테이닝 블록 (containing block)

요소의 위치나 크기를 지정하는데 사용하는 블록
상대적인 값이나 요소의 위치를 지정하는 기준이 필요할 때 사용
