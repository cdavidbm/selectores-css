### **Todos los tipos de selectores en CSS**  

En CSS, los **selectores** permiten aplicar estilos a elementos HTML de manera precisa. Se dividen en varias categorías: **básicos, combinadores, de atributos, de pseudo-clases y de pseudo-elementos**. Aquí tienes una lista completa:  

---

## **1️⃣ Selectores básicos**  
Son los más comunes y se usan para seleccionar elementos por su nombre, clase o ID.  

### 🔹 **Selector de tipo (etiqueta)**
Selecciona todos los elementos de un tipo específico.  
```css
p {
    color: blue;
}
```
Afecta a **todos los `<p>`** de la página.  

### 🔹 **Selector de clase (`.`)**
Selecciona todos los elementos que tengan una clase específica.  
```css
.destacado {
    font-weight: bold;
}
```
Afecta a:  
```html
<p class="destacado">Texto en negrita</p>
```

### 🔹 **Selector de ID (`#`)**
Selecciona un solo elemento por su `id` (debe ser único).  
```css
#titulo {
    font-size: 30px;
}
```
Afecta a:  
```html
<h1 id="titulo">Este es el título</h1>
```

### 🔹 **Selector universal (`*`)**
Selecciona **todos los elementos** de la página.  
```css
* {
    margin: 0;
    padding: 0;
}
```

---

## **2️⃣ Combinadores de selectores**  
Los combinadores permiten seleccionar elementos en función de su relación con otros.

### 🔹 **Selector de descendientes (`A B`)**
Selecciona todos los elementos `B` dentro de `A`, sin importar el nivel de anidamiento.  
```css
div p {
    color: red;
}
```
Afecta a cualquier `<p>` dentro de un `<div>`.  

### 🔹 **Selector de hijo directo (`A > B`)**
Selecciona solo los elementos `B` que son hijos **directos** de `A`.  
```css
div > p {
    color: blue;
}
```
Afecta a:  
```html
<div>
    <p>Este sí será azul</p>
    <section>
        <p>Este NO será azul</p>
    </section>
</div>
```

### 🔹 **Selector de hermano adyacente (`A + B`)**
Selecciona el **primer** elemento `B` que aparece justo después de `A` (en el mismo nivel).  
```css
h1 + p {
    color: green;
}
```
Afecta a:  
```html
<h1>Encabezado</h1>
<p>Este párrafo será verde</p>
<p>Este NO</p>
```

### 🔹 **Selector de hermanos generales (`A ~ B`)**
Selecciona **todos los elementos `B`** que sean hermanos de `A` (en el mismo nivel).  
```css
h1 ~ p {
    color: purple;
}
```
Afecta a todos los `<p>` que estén después de `<h1>`, sin importar si hay otros elementos entre ellos.  

```html
<h1>Encabezado</h1>
<p>Párrafo 1 (púrpura)</p>
<div>Otro elemento</div>
<p>Párrafo 2 (púrpura)</p>
```

---

## **3️⃣ Selectores de atributos**  
Permiten seleccionar elementos según sus atributos HTML.

### 🔹 **Selector de atributo (`[atributo]`)**
Selecciona elementos que tienen un atributo específico.  
```css
input[disabled] {
    background-color: gray;
}
```
Afecta a:  
```html
<input type="text" disabled>
```

### 🔹 **Selector de atributo con valor exacto (`[atributo="valor"]`)**
Selecciona elementos con un atributo que tenga un valor exacto.  
```css
input[type="text"] {
    border: 1px solid black;
}
```

### 🔹 **Selector de atributo que contiene un valor (`[atributo*="valor"]`)**
Selecciona elementos cuyo atributo contenga cierta cadena de texto.  
```css
a[href*="facebook"] {
    color: blue;
}
```
Afecta a cualquier enlace que contenga "facebook" en su URL.  

### 🔹 **Selector de atributo que empieza con (`[atributo^="valor"]`)**
```css
a[href^="https"] {
    color: green;
}
```
Afecta a todos los enlaces que **empiezan** con "https".  

### 🔹 **Selector de atributo que termina con (`[atributo$="valor"]`)**
```css
img[src$=".png"] {
    border: 2px solid red;
}
```
Afecta a todas las imágenes `.png`.  

---

## **4️⃣ Selectores de pseudo-clases**  
Son selectores dinámicos que afectan a los elementos en ciertos estados.

### 🔹 **`:hover` (cuando el mouse está encima)**
```css
button:hover {
    background-color: yellow;
}
```

### 🔹 **`:focus` (cuando el elemento está enfocado)**
```css
input:focus {
    border-color: blue;
}
```

### 🔹 **`:nth-child(n)` (selecciona el `n`-ésimo hijo)**
```css
tr:nth-child(odd) {
    background-color: lightgray;
}
```
Afecta a las filas impares de una tabla.  

### 🔹 **`:first-child` y `:last-child`**
```css
p:first-child {
    font-weight: bold;
}
```
Afecta al **primer** `<p>` dentro de su contenedor.  

---

## **5️⃣ Selectores de pseudo-elementos**  
Permiten seleccionar partes específicas de un elemento.

### 🔹 **`::first-letter` (primera letra)**
```css
p::first-letter {
    font-size: 2em;
    color: red;
}
```

### 🔹 **`::first-line` (primera línea)**
```css
p::first-line {
    font-weight: bold;
}
```

### 🔹 **`::before` y `::after` (añadir contenido antes o después)**
```css
h1::before {
    content: "🔥 ";
}
h1::after {
    content: " 💡";
}
```
Esto agrega emojis antes y después del `<h1>`.  

---

## **🌟 Resumen general**
| Tipo de Selector | Ejemplo | Descripción |
|-----------------|---------|-------------|
| **Básicos** | `p, .clase, #id` | Seleccionan elementos por etiqueta, clase o ID |
| **Combinadores** | `A B`, `A > B`, `A + B`, `A ~ B` | Seleccionan elementos según su relación con otros |
| **Atributos** | `[atributo]`, `[atributo="valor"]` | Seleccionan elementos con atributos específicos |
| **Pseudo-clases** | `:hover`, `:nth-child(n)` | Aplican estilos según estados o posición |
| **Pseudo-elementos** | `::before`, `::first-letter` | Afectan partes específicas de un elemento |

---

## **📖 ¿Cómo investigar más?**
Puedes aprender más sobre cada selector en estos enlaces:
- [MDN Web Docs - Selectores CSS](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Selectors)
- [W3Schools - CSS Selectors](https://www.w3schools.com/cssref/css_selectors.asp)
- [CSS Tricks - A Complete Guide to CSS Selectors](https://css-tricks.com/the-complete-guide-to-css-selectors/)
