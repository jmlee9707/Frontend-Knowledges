> javascript를 사용하여 스타일을 선언적이고, 유지보수 가능한 방식이다.

>     대표적인 라이브러리로 `styled-component`와 `Emotion`이 있다.

**javascript를 css로 전환하는 고성능 컴파일러로 런타임 및 서버 사이트에서 작동하게 된다.**

기존 웹 사이트는 html, css, javascript를 각자 별도의 파일로 두었는데, react나 vue, angular와 같은 모던 javascript 라이브러리가 인기를 끌고 컴포넌트 기반 개발 방법의 주류가 됨에 따라 한 컴포넌트에서 html, css, javascript를 모두 포함하는 패턴이 많이 사용되고 있다.

단 인라인 스타일과 css in javascript는 같지 않다.

## inline-style & css in javascript

### inline style이 동작하는 방법

```
const textStyles = {
  color: white,
  backgroundColor: black
}

<p style={textStyles}>inline style!</p>
```

브라우저에서 DOM 노드를 아래와 같이 연결하고 DOM 노드에 속성으로 추가

```
<p style="color: white; backgrond-color: black;">inline style!</p>
```

### css in javascript 가 동작하는 방법

```
import styled from 'styled-components';

const Text = styled.div`
  color: white,
  background: black
`

<Text>Hello CSS-in-JS</Text>
```

브라우저에서 DOM 노드를 아래와 같이 연결하고 DOM의 상단에 <style>태그를 추가.
실제 CSS가 생성되기 때문에 *미디어 쿼리(Media Query) *가상 선택자(Pseudo Selector)도 사용할 수 있게 된다.

```
<style>
.hash136s21 {
  background-color: black;
  color: white;
}
</style>

<p class="hash136s21">Hello CSS-in-JS</p>

```

## CSS in Javascipt의 특징

- 컴포넌트로 생각할 수 있다 -> CSS의 컴포넌트화로 스타일 시트의 파일을 유지보수 할 필요가 없다.
- 코드 공유 -> javascript 와 css 사이에 상수와 함수를 쉽게 공유할 수 있다.
- 현재 사용중인 스타일만 DOM에 표현
- 진정한 분리법칙을 따른다. CSS-in-JS의 경우 부모 요소의 속성을 상속하지 않는다.
