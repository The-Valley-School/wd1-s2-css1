[EJERCICIO](recursos/ejercicio.zip)

---

Vamos a poner a prueba todo lo que hemos aprendido a lo largo de la sesión con la home de ¡Jimmy Lion!

Tras analizar cada una de las secciones empezamos con el header:

```html
<header>
	<div class="logo-container">
		<img src="./assets/logo.webp">
	</div>
	<nav class="menu">
		<ul class="menu-list">
			<li class="menu-list-item"><a href="#">HOMBRE</a></li>
			<li class="menu-list-item"><a href="#">MUJER</a></li>
			<li class="menu-list-item"><a href="#">NIÑOS</a></li>
			<li class="menu-list-item"><a href="#">PACKS</a></li>
			<li class="menu-list-item"><a href="#">COLLABS</a></li>
			<li class="menu-list-item"><a href="#">OUTLET</a></li>
			<li class="menu-list-item"><a href="#">ABOUT</a></li>
		</ul>
	</nav>
</header>
```

```css
body{
    font-family: sans-serif;
    color: #373737;
    margin: 0;
    letter-spacing: 2px;
}

/* header */

header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
}

.menu{
    display: block;
}

.menu-list{
    list-style: none;
}

.menu-list-item{
    display: inline-block;
}

.menu-list-item a{
    text-decoration: none;
    font-size: 18px;
    color: #373737;
    margin-right: 30px;
}

.logo-container img{
    width: 120px;
}
```

 

Le toca el turno al gif:

```html
<section class="main-banner">
	<img src="./assets/principal.gif">
</section>
```

```css
.main-banner img{
    width: 100%;
}
```

Y por último las colecciones:

```html
<section class="collections">
	<div class="collection">
		<img src="./assets/calcetinesHombre.webp">
		<div class="collection-description">
			<p class="collection-description-buy">Comprar</p>
			<p class="collection-description-text">HOMBRE</p>
		</div>
	</div>
	<div class="collection">
		<img src="./assets/calcetinesMujer.webp">
		<div class="collection-description">
			<p class="collection-description-buy">Comprar</p>
			<p class="collection-description-text">MUJER</p>
		</div>
	</div>
	<div class="collection">
		<img src="./assets/calcetinesNino.webp">
		<div class="collection-description">
			<p class="collection-description-buy">Comprar</p>
			<p class="collection-description-text">NIÑO</p>
		</div>
	</div>
</section>
```

```css
.collections{
    display: flex;
    justify-content: space-between;
    margin: 20px;
}

.collection{
    position: relative;
}

.collection img{
    width: 450px;
}

.collection-description{
    position: absolute;
    top: 115px;
    left: 30px;
}

.collection-description-buy{
    font-size: 30px;
    font-weight: lighter;
    margin: 0 0 10px 0;
}

.collection-description-text{
    font-size: 40px;
    font-weight: bolder;
    margin: 0;
}
```


