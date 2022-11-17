# Kokoa Clone 2020

## 6. CLONING TIME

### 6.0 Introduction

`.gitignore` 파일 생성 : `git`에 추가되지 않는 파일이나 폴더

```
.DS_Store
```

### 6.1 Sign Up Screen part One

### 6.2 BEM(Block Element Modifier)

[BEM](https://css-tricks.com/bem-101/)

```css
/* Block component */
.btn {
}

/* Element that depends upon the block */
.btn__price {
}

/* Modifier that changes the style of the block */
.btn--orange {
}
.btn--big {
}
```

```html
<a class="btn btn--big btn--orange" href="https://css-tricks.com">
    <span class="btn__price">$9.99</span>
    <span class="btn__text">Subscribe</span>
</a>
```

### 6.3 Font Awesome

-   [Heroicons](https://heroicons.dev/) : svg 형식의 무료 아이콘 사이트
-   [Font Awesome](https://fontawesome.com/) : 무료, 유료 선택가능 아이콘 사이트

### 6.4 Sign Up Screen part Two

### 6.5 Status Bar CSS

`status-bar` 시계 중앙에 놓는 방법

```css
.status-bar {
    display: flex;
    justify-content: center;
}
.status-bar__column {
    width: 33%;
}
.status-bar__column:nth-child(2) {
    display: flex;
    justify-content: center;
}
.status-bar__column:last-child {
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
```

### 6.6 Sign Up Screen part Three

[Reset CSS](https://meyerweb.com/eric/tools/css/reset/)  
CSS 파일에서 다른 CSS 파일 불러오기

```css
@import url("filename.css");
```

### 6.7 Log In Form part One

CSS 변수 선언

```css
:root {
    --main-color: #fea100;
}
```

CSS 변수 사용

```css
input {
    border-color: var(--main-color);
}
```

### 6.8 Log In Form part Two

`:not` 선택자

```css
#login-form input:not([type="submit"]) {
    /* css */
}
```

### 6.9 Recap and Forms

### 6.10 Navigation Bar part One

구글도 ul 안의 li 의 링크들을 가져온다.  
Visual Studio Code 단축키

```
nav>ul>li*4>a
```

### 6.11 Navigation Bar part Two

`position: fixed;` 을 선언하면 `width` 가 초기화 되기 때문에 다시 선언해주어야 한다.

### 6.12 Border Box

```css
/* 실제 박스 크기 : 250px */
div {
    width: 200px;
    padding-left: 50px;
}

/* 실제 박스 크기 : 200px */
div {
    width: 200px;
    padding-left: 50px;
    box-sizing: border-box;
}
```

### 6.13 Navigation Bar part Three

`position: absolute`를 사용하기 위해서는 부모 엘리먼트에 `position: relative`가 선언되어 있어야 한다.

```css
.parent {
    position: relative;
}
.child {
    position: absolute;
}
```

### 6.14 Screen Header

재사용이 가능하게 만들어보자.

### 6.15 Friends Screen part One

### 6.16 User Component part One

### 6.17 User Component part Two

### 6.18 Finishing Friends Screen

### 6.19 Chats Screen part One

### 6.20 Chats Screen part Two

### 6.21 Find Screen Part One
