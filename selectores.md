A lo largo de este video vamos a ver las formas que tenemos de asignar estilos al HTML, tanto con etiquetas genéricas, como a un grupo de ellas o a una específica.

## **TIPOS DE SELECTORES**

### **ETIQUETA**

Tenemos la opción de aplicar un estilo asignándoselo a una etiqueta. Este estilo recaerá sobre todas las etiquetas del documento.

```html
<!-- Los dos títulos serán de color azul-->

<h1>Título</h1>
<h1>Título2</h1>
```

```css
h1{
	color: blue;
}
```

El color azul se asignará a todas las etiquetas **<h1>** del documento.

Estos selectores son sencillos de usar pero no hacen una selección específica. La ventaja, podemos usarlos para estilos de página homogéneos. Por ejemplo, estilos de párrafos, títulos o tipografía.

### **CLASES**

Las clases nos sirven para asignar una propiedad a un grupo de atributos que nosotros queramos (Las etiquetas pueden ser diferentes). En HTML utilizamos el atributo **class**

```html
<h2 class="titulo-rojo">Subtítulo 1</h2>
<h3 class="titulo-rojo">Subtítulo 2</h3>
```

En CSS las clases se identifican con un punto .

```css
.titulo-rojo {
	color: red;
}
```

Cabe destacar que el atributo class acepta multiples nombres de clases separados por espacios. Esto es genial ya que podemos aplicar varios estilos a un mismo elemento.

### **ID**

El id es un identificador único, por lo que nos valdrá para asignarle un valor a una etiqueta concreta. Al ser un identificador único, no puede duplicarse

 

```html
<p id="parrafo-principal">Este es el párrafo principal</p>
```

 

En CSS las clases se identifican con una almohadilla #

 

```css
#parrafo-principal{
	color:green;
}
```

 

### **SELECTORES MÚLTIPLES**

Podemos aplicar una regla sobre varios elementos separándolos por comas.

  

```css
h1, h2{
	color:green;
}
```

  

Es más podemos indicar únicamente los h2 que contengan una clase especial

   

```css
h1, h2.especial {
	color:green;
}
```

 

### **SELECTORES POR RELACIÓN**

Podemos combinar también selectores. Indicando que todos los elementos de un elemento pueden tener un estilo específico

   

```css
nav a {
	text-decoration:none;
}
```

 

## **PESO Y HERENCIA DE LOS SELECTORES**

Una etiqueta puede tener estilos asignados por etiqueta, clase o id. Estos se compaginan, y en caso de coincidir, se prioriza desde el más específico al más amplio.

> ID > CLASE > ETIQUETA
> 

Como podemos  tener varias clases asignadas a una etiqueta, puede darse el caso que ambas clases asignen un color distinto al texto. Como la hoja de estilos se lee de arriba a abajo, se asignará el valor de la última clase. En este ejemplo el título saldrá verde. Hay que tener mucho cuidado con esto para evitar pisar propiedades.

```html
<h1 class="titulo-rojo titulo-verde">Título>/h1
```

```css
.titulo-rojo {
	color: red;
}

.titulo-verde {
	color: green;
}
```

Cuando vimos la estructura de HTML explicamos que se trataba de una estructura de árbol con padres, hijos… 

Esto cobra importancia también ahora, ya que algunos valores se heredan de los padres y abuelos. Hay otras que no se heredan. Las iremos viendo conforme trabajemos.

```html
<div class="texto-verde">
	<h1>Título</h1>
	<h1>Título</h1>
</div>

```

```css
.texto-verde {
	color: green;
}
```