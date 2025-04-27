# {Tutorial: Pick and place con URSim}

El siguiente tutorial tiene como objetivo desarrollar "Pick and place" para el brazo róbotico colaborativo "UR5", todo el programa desarrollado a través de la aplicación oficial de Universal Robots "URSim" mismo programa el cual podrá ser utilizado en el robot físico.

Así pues, a lo largo de este tutorial estudiaremos los distintos tipos de movimiento que el robot puede realizar, además, aprenderemos a configurar el entorno virtual, programar los movimientos del robot a realizar y ejecutar una sencilla tarea de recogida y colocación de objetos.

---

## 📋 Requisitos Previos

- Instalación de URSim (guía de instalación: https://drive.google.com/file/d/1XBEqzTVAYYV9bFNBp0DkKGqSmh7_G8Jh/view?usp=sharing)
- Computadora con 2 nucleos mínimo
- 4 RAM mínimo
- Recomendado tener gráfica 

---

## 📖  Introducción

Universal Robots (o mejor conocido como "UR") es una empresa danesa fundada en 2005, líder mundial en el desarrollo de robots colaborativos, robots los cuales, a diferencia de los robots industriales, están diseñados para trabajar junto con personas a su alrededor, esto al tener implementado protocolos y sistemas de seguridad en su programación, quitando la necesidad de implementar barreras físicas en el espacio de trabajo (en muchas aplicaciones).

<p align="center">
  <img src="media/images/UR5.png" alt="Image Open" style="width:35%;"> 
</p>

<p align="center"> UR5 fabricado por Universal Robots

Así pues, el tema que abordaremos en este tutorial es el diseño y programación de una rutina "Pick and Place" en el entorno de simulación URSim. Para ello, primero debemos saber que es un "Pick and Place", el cual se refiere a una tarea fundamental y ampliamente utilizada dentro de la robótica industria, misma la cual consiste en tomar un objeto de un punto A y colocarlo en un punto B de forma automática, precisa y repetitiva, esto a través de distintos tipos de movimientos programados, movimientos que constan de 3 principales:
- MoveL: consiste en un movimiento en línea recta del punto central de la herramienta a un punto deseado.
- MoveJ: consiste en un movimiento a través de la rotación de las juntas del robot, se utiliza principalmente para mover el robot de la forma más rápida y efectiva posible.
- MoveC: consiste en un movimiento circular del punto central de la herramienta a través de un arco deseado.

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

<p align="center">
  <img src="media/images/home.png" alt="Image Open" style="width:35%;"> 
</p>

<p align="center"> Sección donde se encuentra la opción "Home"


**Paso 2:** Mandar al robot a "Home" de manera automatica

Despues de dar click a la opción "Home", mandaremos al robot a esa posición de manera automática, para ello, le daremos click y mantendremos presionado en la sección que dice "Auto", cabe mencionar que la sección "Manual" es para mandar al robot a su posición "Home" moviendolo de manera física:

<p align="center">
  <img src="media/images/Auto.png" alt="Image Open" style="width:35%;"> 
</p>

<p align="center"> Sección donde se encuentra la opción "Auto"

**Paso 3:** Configurar el primer movimiento

Una vez posicionado el robot en "Home" podemos empezar a programar el primer movimiento, para ello daremos click en la sección "Program" y despues en "Structure":


<p align="center">
  <img src="media/images/Auto.png" alt="Image Open" style="width:35%;"> 
</p>

<p align="center"> Sección donde se encuentra la opción "Auto"
  
---
## ✅ Conclusión

Resumen de lo aprendido y posibles extensiones o proyectos relacionados.

---

## 📚 Referencias y Recursos Adicionales


Enlace a documentación oficial

Tutoriales relacionados

Repositorio de código fuente

---

## 📬 Contacto

Para preguntas o sugerencias:

* 📧 Correo electrónico: ejemplo@correo.com
---
