# Observaciones

Querida Sofi, felicitaciones por tu trabajo. Tu portfolio se ve muy lindo y se nota muchísimo el esfuerzo por hacer que se asemeje al modelo de Ada. Recorriendolo, una tiene la sensación de una web hecha con esmero.

El mayor problema en tu portfolio es que el responsive no funciona del todo bien, lo que afecta negativamente tu nota a pesar de que se nota que pusiste esfuerzo. Una web sin responsive no está completa: la mayoría de nuestros usuarios van a ver nuestra web desde el celular, por lo que es absolutamente necesario poder ofrecerles la misma experiencia a ellos. Noto el interés por hacer que el responsive funcione, por lo que me pregunto si lo que faltó es tiempo o si no pudiste resolver algunas cosas: si es el segundo caso, por favor, no dejes de consultarme. 

Te dejo varios comentarios para mencionar cositas puntuales. Como comentamos en clase, este trabajo no se hace para que constates conocimientos, sino para que aprendas: en ese sentido, mi intencion es que estos comentarios te sirvan para aprender, mejorar tu codigo a futuro e ir apreciando mejor qué se espera de nosotras como desarrolladoras front end.

## Estructura correcta de documento HTML

Tu HTML esta muy bien. Claro, prolijo, sin elementos de más, muy bien comentado. 

Algo que me llama la atención es tu `head`, dado que allí repetís innecesariamente el link de google fonts. No es necesario escribilo dos veces

```html
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.gstatic.com">
```

Cada uno de esos links "preconnect" hace exactamente lo mismo - traerse el css de google fonts para poder usar los fonts en tu sitio. Quizá estés bajo la impresión de que por cada uno de los fonts de tu web es necesario traerse nuevamente el css, pero no, no es necesario agregarlo más de una vez. Agregar muchos de estos links innecesarios impacta negativamente en la velocidad de carga de tu web, ya que por cada uno de ellos se hace un llamado a un css externo y se lo carga. 

Tenés cierta tendencia a tener divs de más. Algunas estructuras de tu web se podrían resolver con menos divs. Dicho esto, yo prefiero que los divs sobren antes de que falten: un div de más se soluciona muy fácil, un div menos puede ser un gran dolor de cabeza cuando estamos recién arrancando. Este sería un comentario que quizá me reservaría para futuros trabajos, pero veo tan bien tu código que me siento confiada en recomendarte que empieces a ver estas cosas desde ya. 

Si tenés ganas, con tiempo, te diría que valdría la pena recorrer tu html y notar que estructuras como esta se pueden hacer más breves.

```html 
    <div class="barra-de-navegacion-principal">
        <div class="barrasuperior">
            <nav>
                <ul class="bar1">
                    <li class="list"><a class="link-tarjetas" href="#about">HOLA</a></li>
                    <li class="list"><a class="link-tarjetas" href="#mis_conocimientos">CONOCIMIENTOS</a></a></li>
                    <li class="list"><a class="link-tarjetas" href="#proyectos">PROYECTOS</a></li>
                    <li class="list contacto"><a href="#contacto">CONTACTO</a></li>
                </ul>
            </nav>
        </div>
    </div> 
```

No necesitamos ninguno de los dos divs: podriamos poner los estilos en nav y ul y tu html funcionaría igual de bien. 


## Respeta la consigna 

- El portfolio cuenta con las secciones solicitadas 

Cumplido

- Al clickear en los links de navegación, debe llevar a la sección correspondiente

Cumplido. 

- Al clickear en los links de contacto, debe llevar a la página externa
correspondiente 

Cumplido. 

- El portfolio debe tener un diseño responsivo y verse correctamente en distintos dispositivos 

No cumplido del todo. Veo el intento, pero te juega en contra varias cosas faltantes. 

Entre 900 y 1000px tu formulario rompe: rebalsa su contenedor y hace que aparezca un scroll horizontal en toda la pagina. Este scroll horizontal es muy, muy habitual y muy molesto. Ocurre cuando un elemento ocupa mas espacio del que le da el body, ya sea por un width, un margin, un padding o la combinacion de los tres. Encontrarlo es dificil, requiere recorrer con paciencia cada uno de nuestros elementos. Pero es un ejercicio necesario. en este caso justo es facil de encontrar: son el padding y margin de "datos". Quiza la media query que tenes para datos en pantallas menores a 900px podria estar en 1100, para evitar esto. 

Una vez que pasamos a celulares, el dispositivo mas usado y mas importante, tenemos el mismo problema. Tu web se ve bien entre los 600 y 550px: esa es la absoluta minoría entre celulares. La mayoría están entre 360 y 440px. Notá que aparece de nuevo el scroll horizontal: "imagen-de-notebook" tiene un width de 500px, asi que en cualquier resolucion menor a 500 va a rebalsar. Va a ocurrir algo similar con tu formulario y con los iconos de redes sociales del footer. 

- El portfolio debe estar deployado y ser accesible desde una URL 

Cumplido. 

- El repositorio en GitHub debe tener un readme adecuado 

Cumplido. 

### Respeta el diseño dado 

Cumplido. 

### Buena estructura de proyecto 

Usás muchas imágenes en tu proyecto, y viéndolo a primera vista en github no es tan fácil ver cuáles son los archivos principales. Siempre que uses imágenes locales, como en este caso, agregalas a una carpeta que se llame por ejemplo "imgs", "imagenes" o "assets". De esta manera solo los archivos principales - html, readme y css - son los que están en la carpeta principal. La excepción a esta regla es el favicon, que siempre debería ir en la carpeta principal. 

### Código bien indentado 

Cumplido. 

### Comentarios que permiten mejorar la legibilidad del código 

Ausentes. Es buena idea comentar cada seccion en HTML y CSS para que quede bien claro donde comienza una cosa y termina otra.

### Uso correcto de etiquetas semánticas 

Cumplido 

### Buenos nombres de clases 

Cumplido en general, pero evitá usar cosas como "bar1" y "bar2", ya que es mejor encontrar nombres descriptivos. Cuando decimos que un nombre de clase debe ser descriptivo, lo decimos en un sentido funcional: qué rol cumple este elemento en el código. Los colores de los elementos, su forma, su estilo, su posición, todas esas cosas pueden cambiar y efectivamente cambian todo el tiempo en las webs que hacemos. La sección que estaba a la arriba mañana estará abajo, por lo que "uno" y "dos" no son buenas guias. 

### Código CSS bien estructurado 

Cumplido. Noto muchos estilos innecesarios o confusos, que te voy indicando en tu archivo de css. A veces no dejas el espaciado correcto en cada orden. En lugar de escribir por ejemplo `.name{`, deja un espacio entre el nombre de la clase y la llave: `.name {`

### Reutilización de estilos 

Cumplido la mayoría de las veces, noto muchos intentos por reutilizar los estilos. Hay varios estilos que no necesitas, y te pediria que en algun momento recorras tu CSS viendo todas las cosas que se pueden borrar sin consecuencias. Los divs ya tienen por defecto width de 100%, en la mayoria de los casos eso se puede sacar.


### Cumple con criterios básicos de accesibilidad 

- Los colores tienen un contraste adecuado 

Cumplido

- Las imágenes tiene el atributo `alt` que corresponde 

Está la intención, pero a fines prácticos esto está cumplido a medias . Como vimos en clase el lector de pantalla dice "Imagen" antes de leerlo asi que agregar "imagen" es repetitivo y molesto para el usuario. En tu seccion principal, el lector de pantalla diria: "Imagen: imagen computadora". Una pésima experiencia para el usuario no vidente. 

El alt debe ser un texto que pueda leer el software, por lo que evitá guiones o simbolos que puedan confundir la lectura. Las descripciones deben ser adecuadas: "imagen computadora" no comunica nada, es casi mejor que no estén a que sean inadecuados. Tu imagen principal le comunica muchisimo a tus usurios videntes acerca de qué se trata esta pagina - una mujer programadora - y tu objetivo al agregar alt en las imagenes es comunicarle lo mismo, o lo más posible, a tus usuarios no videntes: "Mujer junto a un monitor" identifica mejor la imagen y permite que todos entiendan qué es lo que querés comunicar. 


- Los íconos y elementos que no presentan texto agregan la información correspondiente por otros medios (etiquetas aria, texto oculto) 

Incumplido

- Los íconos y elementos que no necesitan ser anunciados por un lector de pantalla tienen la etiqueta aria
correspondiente 

Incumplido

- Commits con mensajes adecuados 

Cumplido, noto muchos y buenos commits en tu proyecto, lo que siempre se agradece. 

- Cuenta con un favicon

No cumplido. 

### Nota: 8