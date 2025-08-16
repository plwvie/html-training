# Hướng Dẫn CSS - Thuộc Tính và Tag

## 1. Các Loại Thuộc Tính CSS Chính

### 1.1 Thuộc Tính Layout (Bố cục)

- **display**: `block`, `inline`, `inline-block`, `flex`, `grid`, `none`
- **position**: `static`, `relative`, `absolute`, `fixed`, `sticky`
- **float**: `left`, `right`, `none`
- **clear**: `left`, `right`, `both`, `none`
- **z-index**: Số nguyên (độ sâu lớp)

### 1.2 Thuộc Tính Box Model

- **width**: `auto`, `100px`, `50%`, `100vw`
- **height**: `auto`, `100px`, `50%`, `100vh`
- **margin**: `10px`, `10px 20px`, `10px 20px 30px 40px`
- **padding**: `10px`, `10px 20px`, `10px 20px 30px 40px`
- **border**: `1px solid black`, `2px dashed red`
- **box-sizing**: `content-box`, `border-box`

### 1.3 Thuộc Tính Typography (Chữ)

- **font-family**: `Arial`, `Times New Roman`, `sans-serif`
- **font-size**: `16px`, `1.2em`, `120%`
- **font-weight**: `normal`, `bold`, `100-900`
- **font-style**: `normal`, `italic`, `oblique`
- **text-align**: `left`, `center`, `right`, `justify`
- **text-decoration**: `none`, `underline`, `line-through`
- **line-height**: `1.5`, `20px`, `150%`

### 1.4 Thuộc Tính Màu sắc và Nền

- **color**: `red`, `#ff0000`, `rgb(255,0,0)`, `rgba(255,0,0,0.5)`
- **background-color**: `white`, `#ffffff`, `transparent`
- **background-image**: `url('image.jpg')`
- **background-size**: `cover`, `contain`, `100% 100%`
- **background-position**: `center`, `top left`, `50% 50%`
- **background-repeat**: `no-repeat`, `repeat-x`, `repeat-y`

### 1.5 Thuộc Tính Flexbox

- **flex-direction**: `row`, `row-reverse`, `column`, `column-reverse`
- **justify-content**: `flex-start`, `center`, `flex-end`, `space-between`
- **align-items**: `stretch`, `center`, `flex-start`, `flex-end`
- **flex-wrap**: `nowrap`, `wrap`, `wrap-reverse`
- **flex**: `1`, `1 1 auto`, `0 0 200px`

### 1.6 Thuộc Tính Grid

- **grid-template-columns**: `repeat(3, 1fr)`, `200px 1fr 200px`
- **grid-template-rows**: `100px 1fr 100px`
- **grid-gap**: `20px`, `20px 10px`
- **grid-column**: `1 / 3`, `span 2`
- **grid-row**: `1 / 4`, `span 3`

### 1.7 Thuộc Tính Animation và Transition

- **transition**: `all 0.3s ease`
- **animation**: `slide 2s infinite`
- **transform**: `rotate(45deg)`, `scale(1.2)`, `translateX(100px)`
- **opacity**: `0.5`, `1`, `0`

## 2. Các Tag CSS Selector

### 2.1 Selector Cơ bản

```css
/* Tag selector */
p {
  color: blue;
}

/* Class selector */
.highlight {
  background-color: yellow;
}

/* ID selector */
#header {
  font-size: 24px;
}

/* Universal selector */
* {
  margin: 0;
  padding: 0;
}
```

### 2.2 Selector Kết hợp

```css
/* Descendant selector */
div p {
  margin: 10px;
}

/* Child selector */
div > p {
  padding: 5px;
}

/* Adjacent sibling */
h1 + p {
  font-weight: bold;
}

/* General sibling */
h1 ~ p {
  color: gray;
}
```

### 2.3 Pseudo-classes

```css
/* Link states */
a:link {
  color: blue;
}
a:visited {
  color: purple;
}
a:hover {
  color: red;
}
a:active {
  color: orange;
}

/* Form states */
input:focus {
  border-color: blue;
}
input:disabled {
  opacity: 0.5;
}

/* Position-based */
:first-child {
  font-weight: bold;
}
:last-child {
  border-bottom: none;
}
:nth-child(odd) {
  background-color: #f0f0f0;
}
```

### 2.4 Pseudo-elements

```css
/* Before and after content */
p::before {
  content: "→ ";
}
p::after {
  content: " ←";
}

/* First line and letter */
p::first-line {
  font-variant: small-caps;
}
p::first-letter {
  font-size: 3em;
}
```

## 3. Ví dụ Thực tế

### 3.1 Card Component

```css
.card {
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 20px;
  margin: 10px;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
}
```

### 3.2 Responsive Grid

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  padding: 20px;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

### 3.3 Navigation Menu

```css
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: #333;
}

.nav a {
  color: white;
  text-decoration: none;
  padding: 0.5rem 1rem;
  transition: background-color 0.3s;
}

.nav a:hover {
  background-color: #555;
  border-radius: 4px;
}
```

## 4. Best Practices

1. **Sử dụng CSS Variables**: `--primary-color: #007bff;`
2. **Mobile-first approach**: Viết CSS cho mobile trước
3. **Sử dụng Flexbox/Grid** thay vì float
4. **Tối ưu hóa selector**: Tránh selector quá sâu
5. **Sử dụng shorthand properties**: `margin: 10px 20px;`

## 5. Công cụ Hỗ trợ

- **CSS Validator**: Kiểm tra CSS hợp lệ
- **CSS Grid Generator**: Tạo grid layout
- **Flexbox Froggy**: Học flexbox
- **CSS-Tricks**: Tài liệu tham khảo
- **MDN Web Docs**: Tài liệu chính thức

---

_Tài liệu này sẽ giúp bạn hiểu rõ các thuộc tính và tag CSS cơ bản. Hãy thực hành nhiều để thành thạo!_

