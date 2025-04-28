# {Tutorial: Pick and place con URSim}

El siguiente tutorial tiene como objetivo desarrollar "Pick and place" para el brazo róbotico colaborativo "UR5", todo el programa desarrollado a través de la aplicación oficial de Universal Robots "URSim" mismo programa el cual podrá ser utilizado en el robot físico.

Así pues, a lo largo de este tutorial estudiaremos los distintos tipos de movimiento que el robot puede realizar, además, aprenderemos a configurar el entorno virtual, programar los movimientos del robot a realizar y ejecutar una sencilla tarea de recogida y colocación de objetos.

---

## 📋 Requisitos Previos

- Instalación de URSim ([Guía de instalación de URSim](https://drive.google.com/file/d/1XBEqzTVAYYV9bFNBp0DkKGqSmh7_G8Jh/view?usp=sharing))
- Computadora con 2 nucleos mínimo
- 4 RAM mínimo
- Recomendado tener gráfica 

---

## 📖  Introducción

Universal Robots (o mejor conocido como "UR") es una empresa danesa fundada en 2005, líder mundial en el desarrollo de robots colaborativos, robots los cuales, a diferencia de los robots industriales, están diseñados para trabajar junto con personas a su alrededor, esto al tener implementado protocolos y sistemas de seguridad en su programación, quitando la necesidad de implementar barreras físicas en el espacio de trabajo (en muchas aplicaciones).

![UR5](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/UR5.png)

Así pues, el tema que abordaremos en este tutorial es el diseño y programación de una rutina "Pick and Place" en el entorno de simulación URSim. Para ello, primero debemos saber que es un "Pick and Place", el cual se refiere a una tarea fundamental y ampliamente utilizada dentro de la robótica industria, misma la cual consiste en tomar un objeto de un punto A y colocarlo en un punto B de forma automática, precisa y repetitiva, esto a través de distintos tipos de movimientos programados, movimientos que constan de 3 principales:
- MoveL: consiste en un movimiento en línea recta del punto central de la herramienta a un punto deseado.
- MoveJ: consiste en un movimiento a través de la rotación de las juntas del robot, se utiliza principalmente para mover el robot de la forma más rápida y efectiva posible.
- MoveP: consiste en un movimiento circular del punto central de la herramienta a través de un arco deseado.

Además, tenemos que saber que el robot puede poseer distintos tipos de herramienta, los cuales pueden ser:
- Pistolas de pintura
- Pinstolas de soldadura (tanto para soldadira en arco, como para soldadira de puntos)
- Herramientas de sujeción
- Herramientas de corte
- Lasers
- Ventosas
- Artornilladores
- Scaners
- Fresadoras
- Taladros
  
Entre otras herramientas, no obstante, la herramienta que nosotros utilizaremos para el "Pick and Place" serán unas pinzas de agarre.

---

## 🛠️ Configuración del Entorno

Pasos para configurar el entorno de desarrollo:

* Abriremos el simulador siguiendo la guía de instalación. 

* Damos click en el simulador para "UR5"

* Seleccionamos la opción "program robot"
  
* Seleccionamos la opción "empty program"
  
---
## 🏗️ Instrucciones
**Paso 1:** Mandar el "UR" a su posición "home"

Antes de comenzar a programar movimientos en el brazo robótico debemos moverlo en su posición "Home", para ello damos click en la pestaña "Move" y después damos click en la opción "Home":

![Home](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/home.png)

**Paso 2:** Mandar al robot a "Home" de manera automatica

Despues de dar click a la opción "Home", mandaremos al robot a esa posición de manera automática, para ello, le daremos click y mantendremos presionado en la sección que dice "Auto", cabe mencionar que la sección "Manual" es para mandar al robot a su posición "Home" moviendolo de manera física:

![Auto](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/Auto.png)

**Paso 3:** Configurar el primer movimiento

Una vez posicionado el robot en "Home" podemos empezar a programar el primer movimiento, para ello daremos click en la sección "Program" y despues en "Structure":

![Movimiento](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/Movimiento.png)

<p align="center"> Sección donde se encuentran las distintas opciones para programar el robot

En esta sección encontraremos todas las funciones que puede realizar el robot dentro de la rutina. Así pues, nostros estamos interesados en el movimiento del robot, por lo tanto le damos click en la opción "Move". Después, nos aparecerá nuevas opciones en el arbol de programación, lo que nos indicará que se agregó el comando "Move" de manera correcta:

![MoveJ](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveJ.png)
  
Cómo podemos ver, ahora podemos ver dos opciones: "MoveJ" y "Waypoint 1", comenzaremos a abordar el primer comando "MoveJ". Así pues, si damos click sobre el comando "MoveJ" y después damos click en la sección "Command", nos desplegará un menú donde podrás configurar el movimiento a realizar:

![MoveJP](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveJP.png)

![Command](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/Command.png)
 
En esta sección puedes configurar tanto el tipo de movimiento (MoveJ, MoveL y MoveP), así como la velocidad y la acelareación de la articulación. En nuestro caso, dejaremos la misma configuración, con la velocidad, aceleración y el movimeinto ya establecidos.

Así pues, una vez configurado el tipo de movimeinto, continuamos con la sección "Waypoint 1", para ello, le damos click en "Waypoint 1" y de la misma forma le damos click en la sección "Command":

![Waypoint](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/Waypoint.png)

En esta sección podremos configurar los punto de paso, es decir, podemos mover el robot para configurar el primer punto por el cual pasará el brazo, para ello le damos click en "Set Waypoint":

![1Move](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/1Move.png)
  
Aquí podremos mover el robot con las flechas que están disponibles o podremos directamente dar un ángulo especifico a cada articulación. Así pues y como lo habiamos mencionado anteriormente, ubicaremos el robot encima del objeto a tomar, para ello, yo utilicé la siguiente configuración para cada articulación:

![P1](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/P1.png)

Le demas click en "OK" y tendremos listo el primer movimiento.

**Paso 4:** Configurar el segundo movimiento

Una vez programado el primer movimiento, el resto se basa en el mismo procedimiento. Para el segundo movimeinto ahora utilizaremos un "MoveL", ya que ahora con acercaremos al objeto de manera lineal, entonces, de la misma forma agregamos otro comando "Move" y lo configuramos como "MoveL":

![MoveL](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveL.png)

Del mismo modo, en el arbol de programación se verá reflejado el cambia. Así pues, del mismo modo que lo hicimos anteriormente, configuramos el segundo punto de paso, por lo tanto, seleccionamos "Waypoint_2" y le damos click en "Set Waypoint". Dentro de esa pestaña yo configuramos un movimiento el cual se acerque al punto donde agarraría el objeto:

![MoveLP](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveLP.png)

Le damos click en "OK" y tenemos el segundo movimiento listo

Cabe mencionar que en la simulación no poseemos comandos para simular una pinza, no obstante, en el robot físico podremos tener esa configuración y, del mismo modo que agregamos movimientos, podemos agregar un comando que haga cerrar la pinza.

**Paso 5:** Configurar el tercer movimiento

Una vez programado el segundo movimiento, ahora programaremos el tercer movimiento, para ello, seguiremos el recorrido normal de un "Pick and Place", es decir, despues de bajar y tomar el objeto necesitamos de una salida para asegurarnos de que el robot no choque con ningún objeto del entorno, para ello solo movemeremos el brazo hacia arriba a través de un "MoveL", así pues, seguimos los mismos pasos anteriormente vistos:

![MoveL2](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveL2.png)

![MoveLP2](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveLP2.png)

**Paso 6:** Configurar el cuarto movimiento

Para el cuarto movimiento ahora mandaremos al brazo al lugar donde dejaremos el objeto tomado, para ello utilizaremos un "MoveJ" y, en mi caso, movere la base del robot 180°, así pues, agregamos un nuevo movimiento y configuramos el punto de paso:

![MoveJ2](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveJ2.png)

![MoveJP2](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveJP2.png)

**Paso 7:** Configurar el quinto movimiento

Para el quinto movimiento y del mismo modo que lo hicimos anteriormente, bajaremos el brazo para dejarlo en el lugar deseado, todo esto a través de un "MoveL":

![MoveL3](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveL3.png)

![MoveLP3](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveLP3.png)

Aquí, fisicamente, podremos configurar la pinza para que abra.

**Paso 8:** Configurar el sexto y último movimiento

Para el sexto movimiento ahora necesitamos la salida para que el brazo no choque con el entorno, para ello agregamos un "MoveL" y configuramos el punto del paso arriba de donde dejamos el objeto:

![MoveL4](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveL4.png)

![MoveLP4](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/MoveLP4.png)

**Paso 9:** Simulación

Ya tendremos nuestro programa completo, el cual ahora podremos simular. Para ello, nos vamos al apartado de "Graphics", le damos click en "Simulation" y la damos click en el boton de play:

![Simulacion](https://github.com/EinarCordova/tutorial-Pick_and_Place_con_URSim-/blob/main/media/images/Simulacion.png)

Con esto habremos finalizado con nuestra programación del "UR5" para un programa "Pick and Place"

---
## ✅ Conclusión

En este tutorial aprendimos los distintos tipos de movimientos que realizar un robot industrial, además aprendimos sobre la interfaz de simulación del "URSim" a través de la programación del un "Pick and Place", mostrando paso a paso todos los movimientos que tiene que realizar el brazo "UR5" para poder realizar el programa.

Este proyecto tuvo como principal proposito enseñar e interesar al lector a continuar programando el robot colabortivo "UR5", mostrando lo básico que se debe comprender para empezar en este mundo, con lo anterior dicho, ahora el lector puede interesarse aún más en los otros comandos que el "UR5" puede ofrecer, llegando a implmentar programas con sensores, realizar palets con el comando "Palet" o incluso agregar una estructura más compleja como con "If" o "While"

---

## 📚 Referencias y Recursos Adicionales

[Sitio Oficial para descargar URSim](https://www.universal-robots.com/download/software-cb-series/simulator-non-linux/offline-simulator-cb-series-non-linux-ursim-3158/)

[Guía de instalación de URSim](https://drive.google.com/file/d/1XBEqzTVAYYV9bFNBp0DkKGqSmh7_G8Jh/view?usp=sharing)


---

## 📬 Contacto

Para preguntas o sugerencias:

* Asesor encargado de la página: César Martínez Torres
  
   📧 Correo electrónico: cesar.martinez@udlap.mx

* Redactor del tutorial: Einar Córdova Reyes
  
   📧 Correo electrónico: einar.cor.rey@gmail.com
  
---
