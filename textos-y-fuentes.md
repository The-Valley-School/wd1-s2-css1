Teniendo claro como aplicar estilos mediante los selectores, vamos ahora a darle chicha con los fundamentos para el estilado de textos y fuentes tipográficas.

Los estilos de texto pueden dividirse en un par de categorías:

- Etilos de tipo de letra: En los que aplicamos propiedades que afectan al texto (tamaño, fuente color….)
- Disposición del texto: Espaciado, alineación….

Tenemos que tener en cuenta que existen infinidad de propiedades que van a permitir modificar el estilo de nuestra página web. Os dejamos una web que tiene un listado completo de propiedades para que curioseéis:

> https://css-tricks.com/almanac/properties


## **TIPOS DE LETRA**

## **COLOR**

Es la propiedad que establece el color de los elementos seleccionados. Ya hemos ido trabajando con el, veamos un ejemplo.

```html
<p> Esto es un párrafo </p>
```

```css
p {
	color:green;
} 
```

A demás de poder introducir una serie de colores predefinidos podemos utilizar varias formas de nombrar estos colores:

- **Nombre**

Es el que acabamos de utilizar. Existe un listado reservado de colores básico para su uso.

- **Códigos hexadecimales**

Mediante el código hexadecimal podemos elegir un color específico, por ejemplo cuando tengamos que trabajar con la identidad corporativa de una marca.

```html
<p> Color Tiffany  </p>
```

```css
p {
	color: #81d8d0; /* otro color de verde */
} 
```

**Códigos RGB**

De igual manera, podemos aplicar un código de color rgb para darle estilo a nuestro HTML

 

```html
<p> Color Tiffany </p>
```

```css
p {
	color: rgb(129, 216, 208); /* color Tiffany en RGB */
} 
```

 

Si a parte de color queremos establecer una opacidad trabajando con **rgb**, existe la posibilidad de definir un color con **rgba**, siendo este último argumento la opacidad que queramos darle.

  

```html
<p> Color Tiffany </p>
```

```css
p {
	color: rgba(129, 216, 208, 0.5); /* color Tiffany con opacidad 50% */
} 
```

  

Esta página es muy interesante para trabajar con colores: 

> https://htmlcolorcodes.com/es

### **FONT-FAMILY**

La propiedad font-family nos permite cambiar la fuente de nuestra página a una que nuestro navegador la soporte por defecto. 

```html
<h2 class="titulo-seccion-a"> Título1 </h2>
<h2 class="titulo-seccion-b"> Título1 </h2>
```

```css
.titulo-seccion-a {
	font-family: monospace;
} 

.titulo-seccion-b {
	font-family: sans-serif;
}
```

 

A partir de este estilo, las secciones aplicarán diferentes tipos de letra. Es importante saber que para que un navegador muestre un tipo de letra específico el ordenador que accede debe disponer de ella, de no ser así se utilizará el tipo por defecto.

**Web safe fonts**

Hay cierto número de fuentes que están disponibles por defecto en todos los ordenadores. Este listado de fuentes va evolucionando.

Podemos revisarlo en el siguiente enlace:

> https://www.cssfontstack.com/


 

**Fuentes Predeterminadas**

CSS define 5 fuentes predeterminadas y genéricas que se pueden utilizar en todos los navegadores. El tipo de letra exacta dependerá del navegador.

- serif
- sans-serif
- monospace
- cursive
- fantasy

Podemos trabajar nuestra propiedad font-family con un listado de tipos de letra, en el caso de no encontrar la primera pasará a la segunda, y así sucesivamente. En caso de no encontrar ninguna trabajará con la letra por defecto.

  

```css
p {
	font-family: Helvetica, Arial, sans-serif;
} 
```

 

### **FONT-SIZE**

Nos permite cambiar el tamaño de los textos dentro de nuestra web. Por defecto, cada etiqueta tiene asociados unos tamaños de texto que podemos cambiar. Existen diferentes medidas con las que podemos trabajar a la hora de ajustar tamaños:

- PX (píxeles): Con la que ya hemos trabajado. Es una unidad absoluta en función del alto que queramos que tenga el texto.
- EM y REM: Ya las veremos cuando trabajemos con responsive, básicamente son unidades relativas.

Para cambiar el tamaño de letra sería de la siguiente forma:

```css
p {
	font-size: 20px; 
} 
```

 

### **FONT-WEIGHT**

Nos permite cambiar el grosor de nuestra fuente. Permite seleccionar valores del 100 al 900 y atributos como (normal, lighter, bold, bolder)

```html
<h2 class="titulo-seccion-a"> Título1 </h2>
<h2 class="titulo-seccion-b"> Título1 </h2>
```

```css
.titulo-seccion-a {
	font-weight: lighter;
} 

.titulo-seccion-b {
	font-weigth: bold;
}
```

 

### **TEXT-DECORATION**

La propiedad text decoration nos sirve para poder darle una decoración a un texto pudiéndolo subrayar, tachar…

```html
<h2 class="titulo-seccion-a"> Título1 </h2>
<h2 class="titulo-seccion-b"> Título1 </h2>
```

```css
.titulo-seccion-a {
	text-decoration: underline;
} 

.titulo-seccion-b {
	text-decoration: line-through;
}
```

 

La propiedad text-decoration nos es de gran ayuda también cuando trabajamos con enlaces. Las etiquetas tienen propiedades asignadas por defecto y el enlace tiene un underline que podemos quitar usando el text-decoration

 

```css
a {
	text-decoration: none;
} 
```

 

### **TEXT-TRANSFORM**

Propiedad que nos permite transformar un texto, poniéndolo todo en mayúsculas, minúsculas, capitalizarlo…

```html
<h2 class="titulo-seccion-a"> Título1 </h2>
<h2 class="titulo-seccion-b"> Título1 </h2>
```

```css
.titulo-seccion-a {
	text-transform: uppercase;
} 

.titulo-seccion-b {
	text-decoration: lowercase;
}
```

 

## **DISEÑO DEL TEXTO**

### **TEXT-ALIGN**

Propiedad que nos permite alinear el texto dentro de la caja que lo contiene.

```html
<div class="contenedor">
	<h2 class="titulo-seccion-a"> Título1 </h2>
</div>
```

```css
.contenedor{
	width:600px;
	border: 2px solid black;
}

.titulo-seccion-a {
	text-align:center;
} 

```

 

### **LINE-HEIGHT, LETTER-SPACING, WORD-SPACING**

Para establecer una altura entre cada línea de texto, un espacio entre letras y un espacio entre palabras.

```html
<p>Párrafo 1</p>
<p>Párrafo 2</p>
<p>Párrafo 3</p>
```

```css
p{
	line-height: 1.5;
	letter-spacing: 2px;
	word-spacing: 2px;
}
```

 

### **FUENTES NIVEL AVANZADO**

Ya sabemos aplicar fuentes por defecto a nuestros estilos CSS, vamos ahora a aprender a aplicar nuestras propias fuentes que es lo que normalmente usaremos para trabajar en un proyecto grande.

### **FONT-FACE**

Para aplicar esta personalización usaremos font-face y las siguientes propiedades:

  

```css
@font-face{
	font-family: 'thevalley';
	src: url('fonts/roboto.eot');
	font-weight: 500;
	font-style: italic;
}
```

 

Google fonts tiene infinidad de fuentes que nos podemos descargar:

> https://fonts.google.com/

 