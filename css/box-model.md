# 박스 모델 box-model

![](https://velog.velcdn.com/images/jmlee9707/post/45a0b0d8-7ebd-4586-9616-f48eb2a036ca/image.png)

문서상의 요소들을 시각적인 목적을 위해서 모든 요소들을 하나의 `직사각형 박스` 로 여기는 모델이다
모든 박스들은 아래의 영역을 가진다

- 컨텐츠 영역(content area) : 글이나 이미지, 비디오 등 요소의 실제 내용 포함
- 안쪽 여백 영역 (padding area) : 내용과 테두리 사이의 간격으로 **컨텐츠 영역을 요소의 안쪽 여백까지 포함하는 크기로 확장**
- 테두리 영역(border area) : 내용과 패딩 주변을 감싸는 테두리로 안쪽 여백 영역을 요소의 테두리까지 포함하는 크기로 확장
- 바깥 여백 영역(margin area) : 테두리와 이웃하는 요소 사이 간격으로 테두리 영역을 확장해 요소가 인근 요소 사이의 빈 공간까지 포함하도록 한다.

## box-sizing

box-sizing 속성을 사용하면, `width` 와 `height`가 컨텐츠 영역의 기준인지, 테두리 영역 기준인지 정할 수 있다

- `box-sizing : content-box` : 기본 값이며 컨텐츠 영역 기준이다. 즉, 안쪽여백 영역부터 포함하지 않는다

- `box-sizing : border-box` : 테두리 영역 기준이며 바깥 여백 영역부터 포함하지 않는다.

## margin 과 padding

- margin : 바깥쪽 여백을 의미
- padding : 안쪽 여백을 의미

---

참고
[https://github.com/baeharam/Must-Know-About-Frontend/blob/main/Notes/css/box-model.md](https://github.com/baeharam/Must-Know-About-Frontend/blob/main/Notes/css/box-model.md)
