---
layout: post
title:  "Entendiendo EPLAN"
date:   2022-03-07
tags: EPLAN
description: > 
  En cualquier proyecto de automatización, sí o sí,  tendremos que lidiar con esquemas eléctricos. 
  Conocer bien como se estructuran, qué símbolos se utilizan y como se interpretan es clave para entender el proyecto, agilizar el desarrollo y cumplir con las especificaciones.
---
En esta entrada aprenderas lo básico de lo básico que hay que saber al leer un esquem en EPLAN.

En cualquier proyecto de automatización, sí o sí,  tendremos que lidiar con esquemas eléctricos.
Conocer bien como se estructuran, qué símbolos se utilizan y como se interpretan es clave para entender el proyecto, agilizar el desarrollo y cumplir con las especificaciones.

EPLAN se ha convertido en el standard, por lo que aunque se utilice cualquier otro software, estos seguirán seguirán (seguramente) los principios de diseño de EPLAN

## Símbolos de EPLAN

EPLAN utiliza diferentes símbolos para itentificar los bloques dentro de un conjunto de esquemas:


| Simbolo | Descripción |
| :---: | ----------- |
| **==** | ***Asignacion funcional*** / Sirve para identificar la relación funcional entre instalaciones, instalaciones técnicas y medios de explotación. Pocas veces lo he visto.|
| **=** | ***Intalación*** / Sirve para identificar instalaciones, secciones de planta e instalaciones técnicas |
| **++** | ***Lugar de instalación*** / Sirve para identificar los lugares topográficos de los medios de explotación o las instalaciones técnicas, p. ej. edificio, pasillo, sala, etc.|
| **+** | ***Lugar de montaje*** / Sirve para identificar los lugares físicos de los medios de explotación o las instalaciones técnicas, p. ej. armario, pupitre de mando, etc.|
| **-** | ***Medio de explotación*** / Sirve para identificar la unidad más pequeña de producto técnico que cumple una tarea determinada. Según eplan, los medios de explotacion son cada unidades lógicas que interactúan a nivel electrotécnico o de técnica de fluidos. Los medios de explotación se designan con un identificador de medio de explotación (IME), por ejemplo M1, K1, X1, XS1, W1|
|**&**|***Tipo de documento*** / Sirve para identificar tipos de documentos a fin de diferenciar contenidos informativos (p. ej. esquema de circuitos, esquema de conexiones del sistema, plano de bornes). En lugar de «&» en EPLAN también se puede seleccionar un espacio en blanco|
|**#**| Definido por el usuari.|
  
  
## Identificación de los medios de explotación (IME)

Eplan distingue entre medios de explotacion «generales» (que vienen a ser componentes) como motores, válvulas, fusibles, etc. y medios de explotación «especiales» que serian bornes de conexión, cables, mangueras de cables, conexiones a PLC y un largo etc.

Cada «componente» tiene una forma de identificarlo, la que yo he visto más veces es:

```
NoPágina Letra Contador (-subcontador)
```
Lo mejor para entenderlo,un ejemplo:

Un IME completo como el que sigue =AP+ST1-M1 significa que el motor -M1 se encuentra en el armario +ST1 de la instalación =AP. En este caso no hay subcontador.

Otro ejemplo podría ser el que sigue: =17436+APC1-35A2. En este caso, se trataría del armario +APC1 la instalación =17436 y el componente seria el -35A2. La única info que nos da el IME de componentes es que está en la página 35 de los esquemas.


## Letras identificativas
Para finalizar, os dejamos algunas letras identificativas más comunes:

| Letra | Descripción |
| :---: | :--- |
| A | Equipo en general |
| F |Funciones de protección. Normalmente fusibles, limitadores de sobretensiones, pararayos |
| FU |Fusible |
| G |Generadores, fuentes de alimentación |
| H |Dispositivos de señalización. Suelen ser lámparas y pulsadores luminosos |
| K  |Relés y contactores |
| KM |Caso particular del anterior para contactores de motor |
| KA |Caso particular para relés de funciones generales |
| KT |Relé temporizado |
| M | Motores |
| P |Aparatos de medida. Amperímetros, contadores de pulsos, etc |
| Q |Aparamenta para circuito de potencia en general |
| QF |Interruptor automático |
| QM |Guardamotor |
| QS |Seccionadores |
| T |Transformadores |
| U |Moduladores, convertidores. Lo que viene a ser variadores de frecuencia |
| X |Bornes, clavijas y zócalos |

