### **📌 El DOM (Document Object Model) explicado paso a paso**  

El **DOM (Modelo de Objetos del Documento)** es una representación estructurada de un documento HTML en forma de un **árbol de nodos**. Conocerlo nos permote manipular la estructura, el contenido y el estilo de una página web.  

---

## ** ¿Cómo funciona el DOM?**  
Cuando un navegador carga una página web, hace lo siguiente:  

1. **Lee el código HTML** y lo convierte en una estructura de árbol.  
2. **Interpreta los estilos CSS** y los aplica a los elementos del árbol.  
3. **Ejecuta JavaScript**, que puede modificar el DOM en tiempo real.  

### 📌 **Ejemplo de conversión de HTML a DOM**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Página</title>
</head>
<body>
    <h1>Hola Mundo</h1>
    <p>Este es un párrafo.</p>
</body>
</html>
```
🔽 **Se convierte en esta estructura en el DOM**:  
```
document
 ├── html
 │   ├── head
 │   │   ├── title ("Mi Página")
 │   ├── body
 │       ├── h1 ("Hola Mundo")
 │       ├── p ("Este es un párrafo.")
```

Cada **etiqueta HTML** se convierte en un **nodo** en el árbol del DOM.  

---

## ** Tipos de nodos en el DOM**  
El DOM está compuesto por diferentes tipos de nodos:  

| Tipo de Nodo | Descripción | Ejemplo |
|-------------|------------|---------|
| **Nodo Documento** | Representa todo el documento HTML | `document` |
| **Nodo Elemento** | Representa etiquetas HTML | `<p>, <h1>, <div>` |
| **Nodo Texto** | Representa el contenido dentro de los elementos | `"Hola Mundo"` |
| **Nodo Atributo** | Representa los atributos de los elementos | `class="rojo"` |
| **Nodo Comentario** | Representa comentarios en el código | `<!-- Esto es un comentario -->` |


## ** ¿Dónde aprender más?**
📖 **Documentación oficial de MDN:**  
🔗 [https://developer.mozilla.org/es/docs/Web/API/Document_Object_Model](https://developer.mozilla.org/es/docs/Web/API/Document_Object_Model)  

📖 **Curso interactivo sobre el DOM en W3Schools:**  
🔗 [https://www.w3schools.com/js/js_htmldom.asp](https://www.w3schools.com/js/js_htmldom.asp)  
