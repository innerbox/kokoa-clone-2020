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
