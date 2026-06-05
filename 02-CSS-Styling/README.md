# 🎨 CSS Styling - Panduan Lengkap

**CSS (Cascading Style Sheets)** adalah bahasa untuk styling dan layout halaman web. Pelajari selectors, box model, flexbox, grid, dan animations.

---

## 📋 Daftar Isi

1. [CSS Syntax](#css-syntax)
2. [Selectors](#selectors)
3. [Box Model](#box-model)
4. [Flexbox](#flexbox)
5. [Grid](#grid)
6. [Animations & Transitions](#animations--transitions)
7. [Best Practices](#best-practices)

---

## CSS Syntax

### Cara Menggunakan CSS:

#### 1. Inline CSS
```html
<p style="color: red; font-size: 20px;">Teks merah</p>
```
**Catatan:** Hindari inline CSS, gunakan external CSS!

#### 2. Internal CSS
```html
<head>
    <style>
        p {
            color: blue;
            font-size: 18px;
        }
    </style>
</head>
```

#### 3. External CSS (Rekomendasi!) ✅
```html
<head>
    <link rel="stylesheet" href="/css/style.css">
</head>
```

### CSS Rule Structure:

```css
selelector {
    property: value;
    property: value;
}
```

**Contoh:**
```css
p {
    color: blue;              /* Warna teks */
    font-size: 16px;          /* Ukuran font */
    margin: 10px;             /* Jarak luar */
    padding: 5px;             /* Jarak dalam */
}
```

---

## Selectors

### 1. Element Selector

```css
p {
    color: blue;
}
```

### 2. Class Selector

```css
.highlight {
    background-color: yellow;
}
```

```html
<p class="highlight">Teks dengan highlight</p>
```

### 3. ID Selector

```css
#header {
    background-color: navy;
}
```

```html
<div id="header">Header Section</div>
```

### 4. Attribute Selector

```css
input[type="email"] {
    border: 2px solid blue;
}
```

### 5. Pseudo-Class Selector

```css
/* Saat di-hover */
a:hover {
    color: red;
}

/* Link yang sudah dikunjungi */
a:visited {
    color: purple;
}

/* Focus state */
input:focus {
    outline: 2px solid blue;
}

/* First child */
li:first-child {
    font-weight: bold;
}
```

### 6. Combinator Selectors

```css
/* Descendant Combinator */
div p {
    color: gray;
}

/* Child Combinator */
div > p {
    color: blue;
}

/* Sibling Combinator */
h2 + p {
    color: red;
}
```

---

## Box Model

Setiap element memiliki box model: margin → border → padding → content

### Contoh Box Model:

```css
.box {
    /* Content */
    width: 200px;
    height: 100px;
    
    /* Padding (jarak dalam) */
    padding: 20px;              /* Semua sisi */
    padding: 10px 20px;         /* Top/Bottom, Left/Right */
    padding: 10px 20px 15px 5px;/* Top, Right, Bottom, Left */
    
    /* Border */
    border: 2px solid black;
    border-radius: 8px;
    
    /* Margin (jarak luar) */
    margin: 30px;               /* Semua sisi */
    margin: 20px auto;          /* Center horizontally */
    
    background-color: lightblue;
}
```

### Important Properties:

```css
.box {
    /* Ukuran */
    width: 300px;
    height: 200px;
    max-width: 100%;            /* Responsive */
    min-width: 50px;
    
    /* Background */
    background-color: #f0f0f0;
    background-image: url('/image.jpg');
    background-size: cover;     /* cover, contain, 100px */
    background-position: center;/* center, top, bottom */
    
    /* Text */
    color: #333;
    font-family: Arial, sans-serif;
    font-size: 16px;
    font-weight: bold;          /* 100-900 atau bold, normal */
    line-height: 1.5;           /* Spacing antar baris */
    text-align: center;         /* left, center, right, justify */
    text-decoration: underline;  /* none, underline, overline */
}
```

---

## Flexbox

Flexbox membuat layout responsif lebih mudah!

### Container Properties:

```css
.container {
    display: flex;
    
    /* Arah items */
    flex-direction: row;        /* row, column, row-reverse */
    
    /* Horizontal alignment */
    justify-content: center;    /* flex-start, center, space-between */
    
    /* Vertical alignment */
    align-items: center;        /* flex-start, center, stretch */
    
    /* Wrapping */
    flex-wrap: wrap;            /* nowrap, wrap, wrap-reverse */
    
    /* Gap between items */
    gap: 20px;                  /* 20px vertical dan horizontal */
    gap: 10px 20px;             /* 10px vertical, 20px horizontal */
}
```

### Item Properties:

```css
.item {
    /* Growth factor */
    flex: 1;                    /* Grow equally */
    flex-grow: 1;               /* How much to grow */
    flex-shrink: 1;             /* How much to shrink */
    flex-basis: auto;           /* Base size */
    
    /* Order */
    order: 1;                   /* Change visual order */
}
```

---

## Grid

CSS Grid untuk layout 2D yang kompleks.

### Container Properties:

```css
.grid-container {
    display: grid;
    
    /* Define columns */
    grid-template-columns: 200px 1fr 200px;  /* 3 columns */
    grid-template-columns: repeat(3, 1fr);   /* 3 equal columns */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    
    /* Define rows */
    grid-template-rows: 100px auto 50px;
    
    /* Gap */
    gap: 20px;
    grid-column-gap: 20px;      /* Horizontal gap */
    grid-row-gap: 20px;         /* Vertical gap */
}
```

### Item Properties:

```css
.grid-item {
    /* Span columns */
    grid-column: 1 / 3;         /* From column 1 to 3 */
    grid-column: span 2;        /* Span 2 columns */
    
    /* Span rows */
    grid-row: 1 / 3;            /* From row 1 to 3 */
    grid-row: span 2;           /* Span 2 rows */
}
```

---

## Animations & Transitions

### Transitions (Smooth Changes):

```css
.button {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    
    /* Smooth transition */
    transition: background-color 0.3s ease;
}

.button:hover {
    background-color: darkblue;
}
```

### Animations (Keyframe):

```css
/* Define animation */
@keyframes slideIn {
    from {
        transform: translateX(-100%);
        opacity: 0;
    }
    to {
        transform: translateX(0);
        opacity: 1;
    }
}

/* Use animation */
.slide-element {
    animation: slideIn 0.5s ease-in;
}
```

---

## Best Practices

### 1. Gunakan External CSS
```html
<!-- ✅ Benar -->
<link rel="stylesheet" href="/css/style.css">

<!-- ❌ Hindari -->
<style>...</style>
<p style="color: red;">...</p>
```

### 2. Mobile-First Approach
```css
/* Mobile styles dulu */
.container {
    width: 100%;
}

/* Tablet and above */
@media (min-width: 768px) {
    .container {
        width: 750px;
    }
}
```

---

## 🔗 Resources

- [MDN CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS-Tricks](https://css-tricks.com/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

[← Kembali ke HTML](../01-HTML-Basics/README.md) | [← Main](../README.md) | [Lanjut ke JavaScript →](../03-JavaScript/README.md)