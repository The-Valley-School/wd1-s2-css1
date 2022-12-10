## **Display y Position**

### **DISPLAY**

Ahora que entendemos que los elementos de HTML funcionan como cajas, vamos a ver como podemos definir el tipo de caja que queremos mostrar. La propiedad display nos ayuda con ello.

Tenemos muchos valores que podemos asignar a `display`, aunque los más importantes son:

- Inline
- Block
- Inline-block
- Flex
- None

Con el siguiente ejemplo vamos a ver cada uno de ellos:

 

```html
<body>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
</body>
```

```css
.box{
	width: 300px;
	height: 300px;
	background-color: green;
	border: 2px solid black;
	margin: 10px;
}
```

 

### **DISPLAY BLOCK**

Por defecto, los `<divs>` tienen la propiedad 'display:block' lo que hacen que ocupen todo el ancho de nuestra página.

### **DISPLAY INLINE**

Si ponemos dentro de la clase box → display:inline vemos que todo desaparece. ¿Qué ha pasado?

Esto se debe a que la propiedad inline no acepta las propiedades `width` y `height`, el tamaño viene definido por lo que haya dentro de esos contenedores.

```html
<body>
	<div class="box">TENGO QUE PONER CONTENIDO</div>
	<div class="box">TENGO QUE PONER CONTENIDO CONTENIDO</div>
	<div class="box">TENGO QUE PONER CONTENIDO </div>
	<div class="box">TENGO QUE PONER CONTENIDO CONTENIDO</div>
</body>
```

```css
.box{
	display: inline;
	background-color: green;
	border: 2px solid black;
	margin: 10px;
}
```

Si inspeccionamos ahora, vemos que la caja ocupa lo que contiene, en cambio con `display:block` ocupábamos el 100% del ancho.

### **DISPLAY INLINE-BLOCK**

Con `display:inline-block` los elementos pueden mantener un ancho y alto predefinido ocupando ese espacio. Sería un mix entre `inline` y `block`.

 

```html
<body>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
</body>
```

```css
.box{
	display: inline-block;
	width: 300px;
	height: 300px;
	background-color: green;
	border: 2px solid black;
	margin: 10px;
}
```

 

### **DISPLAY FLEX**

Con display flex los elementos se hacen flexibles y se posicionan uno al lado del otro.

  

```html
<body class="contenedor">
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
</body>
```

```css
.contenedor{
	display:flex;
}

.box{
	width: 300px;
	height: 300px;
	background-color: green;
	border: 2px solid black;
	margin: 10px;
}
```

 

### **DISPLAY NONE**

Nos vale para ocultar un elemento.

  

```html
<body>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box2"></div>
	<div class="box"></div>
</body>
```

```css
.box2{
	display:none;
}

.box{
	width: 300px;
	height: 300px;
	background-color: green;
	border: 2px solid black;
	margin: 10px;
}
```

 

## **POSITION**

La propiedad position nos sirve para especificar la forma en la que se posiciona cada uno de los elementos. Puede ser:

- static
- relative
- absolute
- fixed

### **STATIC**

Posicionamiento por defecto, acorde al flujo normal de la web. Con `static` propiedades como `top`, `right` y demás no tienen efecto.

 

```html
<body>
	<div class="primer bloque">Primer bloque</div>
	<div class="segundo bloque">Segundo bloque</div>
</body>
```

```css
.bloque {
  margin: 15px 0;
  border: 2px solid black;
  width: 300px;
}

.primer {
	background-color:green;
	position:static;
}

.segundo {
	background-color:red;
}

```

 

### **RELATIVE**

Posicionamiento relativo al flujo normal de la web. Con `relative` propiedades como `top`, `right`, `bottom` y `left` se iniciarán desde las coordenadas 0,0 del elemento en cuestión.

 

```html
<body>
	<div class="primer bloque">Primer bloque</div>
	<div class="segundo bloque">Segundo bloque</div>
</body>
```

```css
.bloque {
  margin: 15px 0;
  border: 2px solid black;
  width: 300px;
}

.primer {
  background-color: green;

}

.segundo {
  position: relative;
  background-color: red;
  top: 20px;
  left: 20px;
}

```

 

### **ABSOLUTE**

Se posiciona en función del primer padre que encuentre con `relative`.

 
```html
<html>
<body>
	<div class="primer bloque">Primer bloque</div>
	<div class="segundo bloque"> Segundo Bloque
		<div class="tercer bloque">Tercer Bloque
		</div>
	</div>
</body>
</html>
```

```css
.bloque {
  margin: 15px 0;
  border: 2px solid black;
  width: 300px;
}

.primer {
  background-color:green;

}

.segundo {
  background-color:red;
  position:relative;
}

.tercer {
  position:absolute;
  top: 10px;
}
```


### **FIXED**

El elemento se mantiene en la misma posición aunque hagamos scroll.

 

```html
<html>
<body>
	<div class="primer bloque">Primer bloque</div>
</body>
</html>
```

```css
.bloque {
  margin: 15px 0;
  border: 2px solid black;
  width: 300px;
}

.primer {
  background-color:green;
  position:fixed;
  bottom:0;
}
```

 
