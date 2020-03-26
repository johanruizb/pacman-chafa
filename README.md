# framework-canvas

Licencia: MIT

Con el framework he creado pequeñas animaciones usando JavaScript. Se debería usar junto con este [repositorio para manejo de listas](https://github.com/andcastillo/functional-light) 

La documentación de la librería con la cúal realicé los gráficos es [processing.js](http://processingjs.org/reference/).

## pacman

El punto de entrada para entender cómo funciona el framework es el archivo [pacman.html](src/pacman.html). En este ejemplo se pinta un pequeño circulo amarrillo y un triángulo que definimos usando una estructura junto con unos pequeños círculos que simulan ser galletas.

``` js
state = {
			world1: { x: 50, y: 200, ancho: 100, alto: 100 },
			world2: { x1: 50, y1: 200, x2: 100, y2: 150, x3: 100, y3: 250 }
		};
 ...
 // Esta es la función que pinta todo. Se ejecuta 10 veces por segundo
	processing.drawGame = function(world) {
		const w1 = world.world1;
		const w2 = world.world2;
		processing.noStroke();
...
		processing.ellipse(350, 200, 30, 30);
};
```

## pacman_animacion

El segundo ejemplo de este proyecto es [pacman_animacion.html](src/pacman_animacion.html). En este ejemplo podrán encontrar una sencilla animación que mueve la boca del Pacman del ejemplo anterior. Para controlar la velocidad de refresque, debe cambiarse el parámetro **frameRate(ticsPorSegundo)** dentro de la función **setup()**

``` js
	processing.setup = function() {
		processing.frameRate(10);
      ...
``` 

## pacman_moviendose

El tercer ejemplo es [pacman_moviendose.html](src/pacman_moviendose.html) y muestra a Pacman moviéndose de izquierda a derecha y simulando comerse una pequeña galleta. Esto se logra al configurar **processing.onTic = function(world)**

``` js
	processing.onTic = function(world) {
		const w1 = world.world1;
		...
	};
```

## pacman_choca

El cuarto ejemplo es [pacman_choca](src/pacman_choca) y muestra a Pacman chocando o deteniéndose al toparse con una "pared". Esto se logro también configurando **processing.onTic = function(world)**.

``` js
	processing.onTic = function(world) {
		const w1 = world.world1;
		...
	};
```

	
