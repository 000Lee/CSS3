#  CSS 박스 모델, 리스트, 테이블, 마진 정리

##  색상 표현 (16진수)

| 색상  | 코드 | 축약형 |
|-------|------|--------|
| 검정 | `#000000` | `#000` |
| 흰색 | `#ffffff` | `#fff` |

---

##  줄 간격 - `line-height`

- 수직 중앙 정렬 가능
- 텍스트가 포함된 요소에 `height`와 동일한 값을 주면 정렬됨

```css
line-height: 100px;
height: 100px;
```

---

##  리스트 스타일

###  리스트 없애기

```css
list-style-type: none;
list-style: none; /* 동일 */
```

###  대문자 리스트

```css
list-style-type: upper-alpha;
```

###  리스트에 이미지 사용

```css
list-style-image: url(../images/dot.png);
```

---

##  표 스타일

###  테두리 병합

```css
border-collapse: collapse; /* 기본값은 separate */
```

- `collapse`: 셀 사이 테두리 합쳐짐
- `separate`: 테두리 따로 적용 (기본)

###  표 캡션 위치

```css
caption-side: bottom;
```

- 설명을 표 아래쪽에 배치

###  테두리 스타일 예시

```css
border: 1px solid black;
border: 1px dotted black;
```

---

##  박스 모델

- `div`: 박스 모델을 형성하는 기본 블록 요소
- 기본적으로 `html`, `body`는 `height`를 갖지 않음

###  퍼센트 단위 height 적용하려면?

```css
html, body {
  height: 100%;
}

.child {
  height: 50%; /* 위가 있어야 아래도 비율 적용 가능 */
}
```

---

##  여백 (margin & padding)

###  차이점

| 속성    | 설명                   |
|---------|------------------------|
| `margin`  | 요소 **바깥쪽** 여백 (border 바깥) |
| `padding` | 요소 **안쪽** 여백 (border 안쪽) |

###  축약형 표현법

```css
margin: 상 좌우 하;
padding: 위 오른쪽 아래 왼쪽;
```

- 예시: `margin: 30px 20px 50px;`
  → 위 30px, 좌우 20px, 아래 50px

###  방향별 지정

```css
margin-top, margin-right, margin-bottom, margin-left
padding-top, padding-right, padding-bottom, padding-left
```

---

##  margin 상쇄 (겹침 현상)

1. **형제 요소 사이**
   - 인접한 블록 요소들의 `margin-top`, `margin-bottom` 겹치면 → 큰 값만 적용

2. **부모와 자식 사이**
   - 자식의 `margin-top`이 부모 밖으로 튀어나감 → 큰 값만 적용

3. **빈 블록 요소**
   - 내용이 없어도 상하 마진 겹침 발생

---

##  가로 중앙 정렬

```css
margin: 0 auto;
```

- 반드시 `width`가 지정되어 있어야 적용됨

---

