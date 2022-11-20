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

### 6.22 Find Screen Part Two

같은 코드가 반복된다면 변수로 만들어 놓는것이 좋다.  
똑같은 코드를 여러번 사용하지 않도록 하는것이 좋다.

```css
:root {
    --main-border: 1px solid rgba(0, 0, 0, 0.2);
}
div {
    border-bottom: var(--main-border);
}
```

### 6.23 Find Screen Part Three

CSS에서 영문소문자를 대문자로 바꾸는 방법

```css
.open-post__hashtags {
    text-transform: uppercase; /* 대문자로 바꿔준다. */
}
```

### 6.24 Find Screen Part Four

### 6.25 More Screen part One

### 6.26 More Screen part Two

### 6.27 Settings Screen part One

컬럼 3개가 있을경우 정중앙 맞추기

```css
.alt-header__column:first-child {
    margin-right: auto;
}
/* 중앙은 아무것도 작업안함 */
.alt-header__column:last-child {
    margin-left: auto;
}
```

### 6.28 Settings and Chat Screen part One

### 6.29 Chat Screen part Two

### 6.30 Chat Screen part Three

### 6.31 Chat Screen part Four

### 6.32 Chat Screen part Five

`Modifier` 적용

```html
<div class="message-row message-row--own">
    <!-- Code -->
</div>
```

### 6.33 Write Message Input

### 6.34 Splash Screen part One

### 6.35 Splash Screen part Two

부모에 `position: relative`가 없으면 `body`를 기준으로 삼는다.

```css
#splash-screen {
    /* 부모에 position: relative가 없으면 body를 기준으로 삼는다. */
    position: absolute;
}
```

`forwards` => 애니메이션이 끝난상태를 유지한다.

```css
#splash-screen {
    /* forwards => 애니메이션이 끝난상태를 유지한다. */
    animation: hideSplashScreen 1s ease-in-out forwards;
}
```

### 6.36 Navigation Animation

### 6.37 More Animations

`will-change` => 브라우저에게 어떠한 것이 변할지 미리 알려주는 것  
그래픽카드를 이용해서 애니메이션을 가속화한다.

```css
.open-post__heart-count:hover i {
    will-change: transform;
    animation: heartBeat 1s ease-in-out infinite;
}
```

### 6.38 Animating Chats Screen

`:focus-within` => 엘리먼트 내부에 focus 된게 있으면 작동한다.

```css
.reply:focus-within .reply__column:first-child {
    opacity: 0;
}
```

### 6.39 Recap

### 6.40 No Mobile Media Query

### 7. PUBLISHING OUR WEBSITE

### 7.0 Branches on Git

---

Git에서 branch는 코드들의 평행세계  
master branch에는 stable한 (잘 작동하는 것으로 어느정도 검증이 된) code를 올린다.  
그리고 실험하고 싶거나 새로운 기능을 추가할 때는 새로운 branch를 만든다.  
merge는 branch끼리 합치는 것을 말한다.

---

Github Desktop에서 branch 만들기  
Current branch 클릭 => New branch 클릭 => 이름적고 => Create branch 클릭

---

branch merge하기  
master brach를 현재 branch로 놓고 상단메뉴 `branch` => `merge into current branch`

### 7.1 Publishing on Github Pages

github에서는 static website 호스팅을 무료로 제공한다.

1. 저장소가 `public`으로 되어 있는지 확인한다.
2. `gh-pages` branch를 만든다.
3. github 저장소에 push 한다.
4. https://사용자이름.github.io/저장소이름/
    1. 만약에 주소를 못 찾겠다면 github의 해당 저장소에 들어가서 `Environments` - `github-pages` - `View deployment` 로 가면 알수있다.
