
 

## **INTRODUCCIÓN**

Como ya sabéis, CSS es un lenguaje de estilado que nos permite asignar estilos a nuestro HTML.

Su propio nombre lo indica, las siglas son Cascading Style Sheets (hoja de estilos en cascada). 

Con CSS podremos aplicar un montón de propiedades de visualización (tamaños, fuentes, colores…) a nuestros elementos de HTML. Para ello seguimos la siguiente sintaxis:

 

```css
SELECTOR {
	PROPIEDAD: VALOR;
}
```

 

- El SELECTOR indica al navegador que elementos modificaremos.
- La PROPIEDAD qué vamos a modificar (color, tamaño, fuente...).
- Y el VALOR será el valor que queramos aplicar a esta propiedad.

Por ejemplo, podemos aplicar un color rojo a los elementos **p**

 

```css
p {
	color: red;
}
```

 

## **¿CÓMO INCLUIMOS CSS EN NUESTRO PROYECTO?**

Para trabajar con CSS tenemos 3 opciones. SPOILER → Las dos primeras no las recomendamos.

### **ESTILOS IN-LINE**

La primera opción es incluir directamente el atributo style dentro de nuestro código html, por ejemplo para cambiar el color de un título

 

```html
 <h1 style="color:blue;">Este es un título azul<h1>
```

    

No son recomendables por varias razones:

- No son reutilizables. Cada vez que queramos aplicar un estilo en linea a otro elemento tendremos que copiarlo y pegarlo.
- Perdemos el control de estilos desde CSS. Siempre es recomendable que toda la personalización de estilos esté en el CSS para llevar un mejor control.
- Aumentamos el tamaño del HTML sin sentido.

### **DENTRO DEL HEAD**

La segunda opción es incluir directamente código CSS dentro de nuestro HTML con la etiqueta **<style>**

```html
<style>
	h1{
		color: blue;
	}
</style>
```

No es recomendable por varias razones:

- No podemos reutilizar en otras páginas HTML estos estilos.
- Aumentamos sin sentido el tamaño del HTML.

### **FICHEROS EXTERNOS**

La tercera opción  [  ESTA ES LA BUENA  ] es mediante un fichero CSS. Para ello lo creamos con la extensión .css dentro de nuestro proyecto. Una vez lo tengamos, lo referenciamos dentro de nuestro documento HTML dentro de la etiqueta <head>

```html
<link rel="stylesheet" href="./estilos.css">
```

En el siguiente vídeo vamos a ver cómo podemos seleccionar las diferentes etiquetas para aplicarles estilos.
