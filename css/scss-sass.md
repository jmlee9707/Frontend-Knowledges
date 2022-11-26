# sass의 장점

### 1. 변수 사용 가능

선언 가능 변수 타입 : 숫자, 문자열, 색상, boolean, null, lists, maps

```
$변수명 : 속성값;
```

### 2. nesting(중첩) 가능

중첩해서 선언 및 사용 가능
상위요소 참조시에는 & 문자 사용

```
/* CSS */
.container {
  width: 100%;
}

.container h1 {
  color: red;
}
```

```/* Sass */
.container {
  width: 100%;
  h1 {
    color: red;
  }
}
```

### 3. import와 extend

`@import` 지시어를 사용해서 다른 scss 파일을 import 할 수 있다
`@extend` 지시어를 사용해서 특정 선택자의 속성을 상속 받을 수 있다

### 4. 믹스인(mixin)

공통적으로 쓰이는 css 속성들을 묶어서 재사용이 가능하게 하는 기능
`parameter`를 받을 수 있다

선언 : @mixin
사용 : @include

```
/* SASS */
@mixin headline($color, $size) {
  color: $color;
  font-size: $size;
}

h1 {
  @include headline(green, 12px);
}

// 인자에 default값 적용
@mixin headline($color: #eee, $size: 10px) {
  width: 50px;
}
```

```
/* CSS */
h1 {
  color: green;
  font-size: 12px;
}
```

```
/* SASS */

@mixin media($queryString) {
  @media #{$queryString} {
    @content;
  }
}

.container {
  width: 900px;
  @include media('(max-width: 767px)') {
    width: 100%;
  }
```

```
/* CSS */
.container {
  width: 900px;
}
@media (max-width: 767px) {
  .container {
    width: 100%;
  }
}
```

### 5. 커스텀 함수 사용

함수 정의는 `@function` ,리턴값은 `@return`

### 6. 흐름 제어 가능

분기문 : `@if` 절 사용

- `@if` 표현식 {...} `@else`
- `if` 표현식{...} `@else` {...}

반복문

- `@for` : n~m 까지의 숫자 범위에 대해 각 정수값에 대해 순회
- `@each` : 주어진 리스트나 맵의 각 원소에 대해 순회 -`@while` : 주어진 조건을 만족하는 동안 반복

---

참고
[https://github.com/Esoolgnah/Frontend-Interview-Questions/blob/main/Notes/important-3/sass-scss.md](https://github.com/Esoolgnah/Frontend-Interview-Questions/blob/main/Notes/important-3/sass-scss.md)
