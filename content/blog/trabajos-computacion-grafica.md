---
title: "Trabajos de Computación Gráfica"
description: "Trabajos realizados para los distintos cursos de computación gráfica en el periodo de pre-grado."
author: "Christiam Mena"
date: 2020-10-15T16:48:37-05:00
draft: false
# Table of content
toc: false
categories:
  - Portafolio Personal
tags:
  - portafolio
  - proyectos
  - trabajos
  - computación Gráfica
  - universidad
  - c++
  - c#
  - OpenGL
  - GLSL
# Cover information
image: /images/portfolio/tesis.jpg
style: "none"
---

Un viejo profesor de matemáticas siempre nos decía: **"recordar... es vivir"**.

Hace poco revisando mis viejos archivos y proyectos de la universidad me di cuenta de que aquel viejo dicho era cierto. Nada más bonito que **"vivir"** al recordar: las noches sin dormir terminando un proyecto, las horas de depuración perdidas al enterarte de que sólo te faltaba una coma, el nombre **tesis-final-ahorasi.docx"**, o aquellos cubos que por alguna razón dejaban de tener 6 caras o simplemente desaparecían del todo.

La computación gráfica es increíble y disfruté mucho esa etapa de mi carrera, tanto que decidí compartir algunos de los mejores proyectos de mi etapa universitaria.

## Trabajo Especial de Grado
**Colocación Virtual del Marco Estereotáctico en la Radiocirugía Estereotáctica**

En el trabajo se desarrolla un sistema que provee al neurocirujano de una guía virtual y cuantitativa para la colocación óptima del Marco Estereotáctico en el cráneo, haciendo uso de las imágenes diagnósticas del paciente obtenidas antes del tratamiento. El sistema desarrollado genera una serie de marcas fiduciales y estereotácticas en los estudios imageneológicos según el posicionamiento virtual del marco, que servirán de entrada para el sistema de planificación.

Suena un poco confuso de entrada, pero acá les muestro algunos aspectos interesantes del sistema:

### El marco

Todas las piezas que por defecto manejaba la aplicación fueron diseñadas con **Google Sketchup 8©**[^sketchup] haciendo uso de aproximaciones a las escalas reales de cada componente y fueron exportadas en formato OBJ por la misma aplicación.

[^sketchup]: [Google Sketchup](https://www.sketchup.com/es)

{{< figure class="fit-width" src="/images/tesis/tesis-2.jpg" caption="Marco Estereotáctico y todos sus componentes" >}}

La razón principal por la cual los modelos fueron exportados en formato OBJ es porque éste es aceptado universalmente por un gran número de visualizadores de modelos 3D y aplicaciones tipo CAD lo cual permite la edición de las piezas usadas en cualquier momento.

### La interfaz

La interfaz gráfica de la aplicación estaba dividida en cinco grandes secciones. Cada una de estas secciones estba agrupada en sub-elementos según sus características, funcionalidades y similitudes.

{{< figure src="/images/tesis/tesis-7.jpg" caption="Elementos que conformaban la interfaz gráfica de la aplicación Virtual Stereotactic Frame" >}}

### Los _viewports_

Los cuatro _viewports_ conformaban la sección más grande de toda la aplicación y proveían diferentes maneras de visualizar todos los elementos de la escena. Cada uno de los _viewports_ era perfectamente configurable por el usuario y eran independientes entre ellos (en términos de configuración). Esta sección de la aplicación era la más importante de todas.

Un _viewport_ puede definirse como una ventana pequeña en donde se despliega la escena vista desde cierta perspectiva. Los cuatro _viewports_ poseían numerosas opciones que proveían a la aplicación de diferentes maneras de visualizar la escena, por ejemplo: vista perspectiva u ortográfica (también llamada ortogonal).

{{< figure src="/images/tesis/tesis-9.jpg" caption="Elementos que conforman el viewport" >}}

Otros elementos visibles en el _viewport_ era: el ***ViewCube***, el cual permite el cambio de vista de manera rápida y sencilla, ubicado en la esquina superior derecha; las reglas que indican las medidas del volumen, ubicada a la derecha y abajo del _viewport_; y la visualización de los ejes cartesianos tridimensionales, ubicados en la esquina inferior izquierda.

### Rotación

El componente de rotación estaba conformado por un aro o circunferencia centrada en el Marco Estereotáctico y dos líneas indicadoras principales. La circunferencia actuaba como interfaz que permitía al usuario hacer clic sobre ella para realizar una rotación específica y las dos líneas funcionaban de guías que indican la posición inicial de la rotación (donde se hizo clic) y la posición final de la rotación (donde se encuentra actualmente el cursor del ratón). Adicionalmente, se desplegaba una etiqueta que indicaba el ángulo actual expresado en grados.

{{< figure class="fit-width" src="/images/tesis/tesis-3.jpg" caption="Visualización del componente de rotación" >}}

### Traslación

El componente estba formado por tres flechas paralelas a los ejes X, Y y Z; una etiqueta para el despliegue de las medidas y tres selectores triangulares.

Para interactuar con esta herramienta el usuario debía hacer clic sobre las flechas o los se-lectores de plano. Cada uno de los elementos tienía comportamientos distintos. Al hacer clic sobre las flecha el usuario solo tenía permitido trasladar el marco sobre el eje seleccionado, mientras que si seleccionaba los otros indicadores podía desplazar el marco por el plano que corresponda (XY, XZ o YZ).

{{< figure class="fit-width" src="/images/tesis/tesis-4.jpg" caption="Visualización de la herramienta de traslación" >}}

Al iniciar el movimiento se mostraba una etiqueta que indicaba la distancia desplazada en cada eje con respecto a la posición inicial. Dicha distancia estaba expresada en milímetros.

### Clipping

Este componente era el encargado de realizar cortes transversales a un elemento 3D haciendo uso del procedimiento de **“recorte”** (_clipping_, en inglés) definido en el API de **OpenGL**. Esta componente era utilizado en la aplicación como una herramienta para la visualización interior del volumen desplegado. El procedimiento de _clipping_ se encargaba de identificar una porción del volumen que se encuentra dentro o fuera de una región tridimensional definida por la intersección de tres planos perpendiculares entre sí. Luego, toda la porción dentro del área definida se mostraba en pantalla y el resto simplemente no se desplegaba.

{{< figure class="fit-width" src="/images/tesis/tesis-6.jpg" caption="Visualización del componente de Clipping del volumen. En **(A)** se muestran los planos de clipping y en **(B)** se muestra el componente que permite ajustar las posiciones de los planos" >}}

### El volumen (a.k.a. el paciente)

La mayoría de las veces cuando se trabaja con despliegue de volúmenes en el área de medicina es necesario visualizar tejidos o zonas específicas del cuerpo humano. Para lograr esto se utilizó una **función de transferencia**.

> Una **función de transferencia** se encarga de asignar propiedades ópticas, como color y transparencia, a las muestras del volumen desplegado.

En éste caso se uso una función de transferencia de una dimensión. Dicho procedimiento se logra asignando valores de color (rojo, verde, azul y transparencia; o _RGBA_ por sus siglas en inglés) a cada iso-valor del volumen utilizando alguna función de correspondencia.

{{< figure src="/images/tesis/tesis-5.jpg" caption="Ventana de Función de Transferencia" >}}

Una función de transferencia puede ser diseñada para visualizar capas de piel, huesos u otros tejidos internos de dos maneras diferentes:
- La primera es definiendo de forma manual cada valor de correspondencia entre un iso-valor y un color RGBA, lo cual deriva en un proceso tedioso y poco práctico, por lo que no fue considerado como una solución factible para éste trabajo.
- La segunda manera es diseñando un control interactivo que permita definir de manera rápida, práctica y lo más importante, en tiempo real, cualquier función de transferencia.

{{< figure class="fit-width" src="/images/tesis/tesis-10.jpg" caption="Las diferentes configuraciones por defecto de la Función de Transferencia" >}}

### Detección de la lesión

En esta ventana se podía apreciar todos los detalles referentes a las imágenes DICOM cargadas en el sistema, así como la información básica del paciente, permitía hacer mediciones, localizar y marcar la lesión en el cráneo y cambiar los valores en la función lineal para la visualización de los cortes (ancho y centro de la ventana).

{{< figure src="/images/tesis/tesis-11.jpg" caption="Elementos que conforman la interfaz gráfica del visor DICOM" >}}

**Tecnologías usadas:** C#, OpenGL, OpenTK, Forms Apps, lectura de imágenes DICOM, Google Sketch-up.

## My2Cents
**XNA Game Studio**

Proyecto desarrollado bajo el marco del **Microsoft Imagine Cup** con el objetivo de contribuir a alcanzar los _Objetivos de Desarrollo del Milenio_ en desarrollo un juego llamado **My2Cents**. Este nombre surgió teniendo en cuenta nuestra contribución al mundo utilizando las tecnologías actuales (_Mi Granito de Arena_).

{{< figure src="/images/portfolio/my-2-cents.jpg" >}}

El juego **My2Cent** consiste en utilizar un Kinect y una pantalla de una sola salida (monitor, proyector, TV, etc) que se ejecuta en un PC. Con **My2Cents**, queremos contribuir al logro de varios objetivos, básicamente, utilizando las tecnologías de Microsoft.

{{< youtube aaPVtksDaeo >}}

**Tecnologías usadas:** C#, XNA, OpenGL, Blender, Photoshop, Kinect.

**Nota:** En esta participación del **Microsoft Imagine Cup 2012**, pudimos llegar a la tercera ronda en la categoría de Game Design **entre los 100 mejores países del mundo**.

## LOD y GeoMipMapping
**Despliegue de terreno con nivel de detalle**

Proyecto con fines académicos para el curso de Tópicos en Computación Gráfica. El proyecto consistía en generar un terreno de forma **procedural** utilizando el algoritmo de **Perlin Noise** y desplegarlo utilizando la técnica de **GeoMipMapping** con 3 niveles de detalle (LOD).

{{< youtube YBqaOQzYEfA >}}

Entre las características extras cabe mencionar el despliegue de **billboards**, **nubes procedurales** animadas, **generación procedural de la textura** del terreno con diferentes niveles (agua, lodo, tierra, grama, roca y hielo) y la **generación de sombras** usando la técnica de **"Fast computation of terrain shadow maps"**.

**Tecnologías usadas:** C++, OpenGL, Shaders.

## Simulación básica del agua
**OpenGL y C++**

Desarrollado para el curso de Tópicos en Computación Gráfica. Dentro de las características de este proyecto están:
- Reflección y refracción del agua usando GLSL.
- Lens flare.
- Simulación de efecto cáustico debajo del agua.
- Billboards en árboles.
- Domo animado con nubes procedurales.
- Movimiento del sol simulando el tiempo.
- Generación procedural del terreno usando Perlin Noise.
- Generación procedural de las texturas del terreno.
- Detección de colisiones.
- Generación de sombras con la técnica de **"Fast computation of terrain shadow maps"**.
- Vertex Buffer Object (VBO) para el despliegue del terreno.
- Cargador de archivos OBJ.
- Atenuación ambiental.
- Animación de modelos.

{{< youtube 8Ts8h8gEUIU >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Estereoscopía
**Técnica de anaglifos**

Desarrollado para el curso de Tópicos en Computación Gráfica con fines académcos. El objetivo del proyecto era desplegar una escena con la técnica estereoscópica de anaglifos (para lentes rojo/azul) utilizando dos y tres despliegues de la misma. Entre de las funcionalidades cabe destacar que la aplicación permite cambiar la posición del ZPS y la apertura de los ojos.

{{< youtube qXxM7akDA90 >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Cargador de mapas
**Mapas BSP y técnica de Frustum Culling**

Proyecto con fines académicos para el curso de Fundamentos y Técnicas en Computación Gráfica. El objetivo del proyecto era cargar un mapa BSP y desplegarlo utilizando una técnica de aceleración. En este caso se utilizó el **Frutum Culling** para descartar ramas del **árbol BSP** al momento de hacer el despliegue. Entre las características adicionales están el uso de multitextura haciendo uso del lightmap que viene contenido en el archivo BSP.

{{< youtube WDk4we8bk0Q >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Técnicas de iluminación
**Parallax Mapping, Normal Mapping y Phong Shading**

Desarrollado para el curso de Fundamentos y Técnicas en Computación Gráfica con fines académcos. Se implementaron las técnicas de Parallax Mapping, Normal Mapping, Phong Shading, mapeo de textura esférico y planar con GLSL, interacción con el mouse (rotar, escalar y trasladar) y carga de archivos OFF.

{{< youtube Ng9DQNaipoc >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Despliegue de volúmenes
**Marching Tetracubes**

Desarrollado para el curso de Tópicos en Computación Gráfica. El objetivo del proyecto era cargar y desplegar volúmenes utilizando la ténica de **Marching Tetracubes** (Tetracubos Marchantes) y permitir al usuario seleccionar el umbral que deseaba. Se debían calcular las normales de cada triángulo con el fin de generar Gouraud Shading en el mallado además de poder visualizar el volúmen de manera estereoscópica.

{{< youtube pa9XC05TC8c >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Despliegue de volúmenes
**Object-aligned planes**

Desarrollado para el curso de Fundamentos y Técnicas en Computación Gráfica con fines académcos. Se utilizo la técnica de despliegue de volumenes llamada Planos Alineados al Objeto (una técnica de textura 2D).

{{< youtube nmdlGlJ-2G0 >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

## Desarrollo de un video juego
**“The Lay Of Leithian”**

Video juego desarrollado en mes y medio con propósitos académicos para el curso de Introducción a la Computación Gráfica. El objetivo del juego es recolectar los tres diamantes azules repartidos a lo largo de tres niveles en donde se deberán utilizar las habilidades de los tres personajes de la historia.

{{< youtube 7cEKSXrrxMU >}}

**Tecnologías usadas:** C++, OpenGL, GLSL, efectos de sonido y sonido ambiental.

## Sombras volumétricas, reflexión y detección de colisiones
**OpenGL y C++**

Proyecto con fines académicos para el curso de Fundamentos y Técnicas en Computación Gráfica. El proyecto consistía en recrear una escena en donde se puduera apreciar las sombras volumétricas generadas por una fuente de luz y la reflección de ciertos elementos sobre una superficie pulida. El proyecto fue realizado haciendo uso del Stencil Buffer. Como caracerística adicional cabe destacar que se aplico la técnica de Nomal Mapping a las paredes, el techo y el piso del escenario y la detección de colisiones.

{{< youtube NVvh9aPDsAc >}}

**Tecnologías usadas:** C++, OpenGL, GLSL.

