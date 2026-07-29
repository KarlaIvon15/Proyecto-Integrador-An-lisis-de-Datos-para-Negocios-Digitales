# Analítica de jugadores y monetización de EcoAventura

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Análisis_de_datos-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red)
![GitHub](https://img.shields.io/badge/GitHub-Colaborativo-black)
![Status](https://img.shields.io/badge/Estado-En_desarrollo-yellow)

## Índice

1. [Descripción del proyecto](#descripción-del-proyecto)
2. [Contexto del videojuego](#contexto-del-videojuego)
3. [Planteamiento del problema](#planteamiento-del-problema)
4. [Justificación](#justificación)
5. [Objetivos](#objetivos)
6. [Preguntas de negocio](#preguntas-de-negocio)
7. [Público objetivo](#público-objetivo)
8. [Modelo de monetización](#modelo-de-monetización)
9. [Alcance geográfico](#alcance-geográfico)
10. [Stakeholders](#stakeholders)
11. [Fuentes de datos](#fuentes-de-datos)
12. [Arquitectura de datos](#arquitectura-de-datos)
13. [Entidades principales](#entidades-principales)
14. [Periodo y volumen de los datos](#periodo-y-volumen-de-los-datos)
15. [Proceso ETL](#proceso-etl)
16. [Análisis exploratorio](#análisis-exploratorio)
17. [Mecanismos analíticos](#mecanismos-analíticos)
18. [Indicadores KPI](#indicadores-kpi)
19. [Dashboards](#dashboards)
20. [Tecnologías utilizadas](#tecnologías-utilizadas)
21. [Estructura del repositorio](#estructura-del-repositorio)
22. [Requisitos previos](#requisitos-previos)
23. [Instalación](#instalación)
24. [Configuración](#configuración)
25. [Ejecución](#ejecución)
26. [Resultados principales](#resultados-principales)
27. [Hallazgos y recomendaciones](#hallazgos-y-recomendaciones)
28. [Pruebas y validaciones](#pruebas-y-validaciones)
29. [Metodología de trabajo en GitHub](#metodología-de-trabajo-en-github)
30. [Integrantes](#integrantes)
31. [Uso responsable de inteligencia artificial](#uso-responsable-de-inteligencia-artificial)
32. [Privacidad y tratamiento de datos](#privacidad-y-tratamiento-de-datos)
33. [Limitaciones](#limitaciones)
34. [Trabajo futuro](#trabajo-futuro)
35. [Licencia](#licencia)
36. [Referencias](#referencias)

---
## Descripción del proyecto

Este repositorio contiene el desarrollo del proyecto integrador de la materia de
*Análisis de Datos*, enfocado en estudiar el comportamiento de los jugadores y la
monetización del videojuego *EcoAventura*.

El videojuego está dirigido a niños de entre 6 y 11 años y utiliza un modelo de
monetización basado en:

- Un pago único para obtener acceso al videojuego.
- Compras opcionales de skins y artículos cosméticos dentro del juego.

El proyecto utiliza datos completamente simulados correspondientes al municipio de
Xicotepec de Juárez, Puebla, y a distintas localidades pertenecientes al municipio.

A través de técnicas de simulación, limpieza, transformación, análisis exploratorio,
segmentación, retención, cálculo de indicadores y visualización, se busca identificar
patrones que ayuden a mejorar la actividad, retención y monetización del videojuego.

---
## Contexto del videojuego

EcoAventura es un videojuego educativo diseñado principalmente para niños de entre 6 y 11 años.

La dinámica principal consiste en:

- Completar niveles.
- Superar misiones.
- Obtener logros.
- Desbloquear contenido.
- Personalizar personajes mediante skins.
- Participar en eventos temporales.
- Explorar escenarios relacionados con el cuidado del medio ambiente y la conservación de los recursos naturales.

Los escenarios del videojuego están inspirados en distintos entornos naturales. En cada escenario, el jugador debe resolver actividades educativas relacionadas con la separación de residuos.

El videojuego se adquiere mediante un pago único. Una vez dentro, el jugador puede comprar artículos cosméticos, como skins, accesorios y elementos de personalización. Estos artículos no proporcionan ventajas competitivas ni modifican directamente la capacidad del jugador para completar los niveles.

---
## Planteamiento del problema 

El videojuego registra jugadores, sesiones, progreso y compras de skins. Sin embargo, no se dispone de un sistema analítico que permita comprender de manera integral: 

- En qué localidades se encuentran los jugadores más activos.
- Qué zonas generan mayor cantidad de compras. 
- Cuáles skins son las más y menos vendidas. 
- Qué jugadores presentan riesgo de abandono. 
- En qué días y horarios se utiliza más el videojuego. 
- Qué características se relacionan con la compra de skins. 
- Qué campañas o promociones generan mejores resultados. 
- Cómo evoluciona la retención de los jugadores. 

Esta falta de información dificulta tomar decisiones relacionadas con actualizaciones, diseño de skins, precios, promociones, campañas y experiencia de usuario.

---

## Justificación

El desarrollo de este proyecto se realiza debido a la necesidad de contar con un sistema de análisis de datos que permita transformar la información generada por el videojuego EcoAventura en indicadores útiles para la toma de decisiones. Aunque el videojuego registra datos sobre jugadores, sesiones, progreso y compras de artículos cosméticos, estos datos por sí solos no proporcionan información estratégica si no son procesados y analizados.

Desde una perspectiva técnica, el proyecto implementa un proceso de análisis de datos que incluye la simulación, limpieza, transformación, integración y visualización de la información, permitiendo identificar patrones de comportamiento, medir la retención de jugadores, analizar el rendimiento de las campañas promocionales y evaluar la aceptación de los artículos cosméticos. Estos resultados facilitan la generación de indicadores clave (KPIs) que apoyan la optimización de la experiencia del usuario y de las estrategias de monetización.

Asimismo, el proyecto permite aplicar metodologías y herramientas de análisis de datos para convertir grandes volúmenes de información en conocimiento útil, demostrando la importancia del procesamiento y análisis de datos como apoyo para la toma de decisiones basada en evidencia dentro del desarrollo y la gestión de videojuegos.

---

## Objetivos

### Objetivo general

Analizar el comportamiento de los jugadores, las sesiones de juego, el progreso y las
compras de skins mediante herramientas de analítica de datos, con la finalidad de
identificar patrones de actividad, retención y monetización que apoyen la toma de
decisiones relacionadas con contenido, precios, promociones y experiencia de usuario.

### Objetivos específicos

1. Identificar las localidades con mayor cantidad de jugadores registrados.
2. Determinar en qué localidades se juega durante más tiempo.
3. Clasificar a los jugadores de acuerdo con su nivel de actividad.
4. Calcular la retención de jugadores a 7, 30 y 90 días.
5. Analizar cuáles skins generan más unidades vendidas.
6. Identificar cuáles skins generan mayores ingresos.
7. Detectar skins con baja demanda.
8. Analizar la relación entre tiempo de juego y compras.
9. Evaluar la conversión de jugadores activos a compradores.
10. Construir dashboards para el administrador y para el jugador o tutor.
11. Formular recomendaciones sustentadas en los resultados.

---

## Preguntas de negocio

El proyecto busca responder las siguientes preguntas:

1. ¿En qué localidades se concentra la mayor cantidad de jugadores?
2. ¿En qué localidades se acumula más tiempo de juego?
3. ¿Cuáles son los días y horarios de mayor actividad?
4. ¿Qué porcentaje de jugadores se encuentra activo, ocasional, en riesgo o inactivo?
5. ¿Qué skins son las más vendidas?
6. ¿Qué skins generan más ingresos?
7. ¿Qué skins presentan menor demanda?
8. ¿Qué porcentaje de jugadores activos compra al menos una skin?
9. ¿Existe relación entre tiempo de juego, nivel alcanzado y compra de skins?
10. ¿Qué jugadores presentan mayor riesgo de abandono?

---

## Público objetivo

El videojuego está dirigido principalmente a:

- Niños de entre 6 y 11 años.
- Padres, madres o tutores responsables de las compras.
- Usuarios ubicados en Xicotepec de Juárez y localidades pertenecientes al municipio.

Para proteger la privacidad de los menores, los datos utilizados en el proyecto son
simulados y no incluyen nombres, direcciones, teléfonos, correos electrónicos ni otros
datos personales reales.

---

## Modelo de monetización

El videojuego utiliza dos fuentes principales de ingresos.

### Pago inicial

El usuario realiza un pago único para adquirir el videojuego.

Ejemplo de precios simulados:

- Precio normal: $249 MXN.
- Precio promocional: $199 MXN.

### Compras internas

Los jugadores pueden adquirir artículos cosméticos opcionales.

| Tipo de artículo | Rango de precio simulado |
|---|---:|
| Skin común | $19 a $29 MXN |
| Skin poco común | $35 a $49 MXN |
| Skin especial | $55 a $69 MXN |
| Skin de evento | $79 MXN |
| Paquete de skins | $99 a $149 MXN |

Las skins no proporcionan ventajas competitivas y su función es únicamente estética.

---

## Alcance geográfico
 
El presente proyecto tiene como alcance geográfico el municipio de Xicotepec de Juárez, ubicado en el estado de Puebla, México, incluyendo sus principales localidades. Los datos utilizados para el análisis corresponden a información simulada representativa de esta región, con el propósito de estudiar el comportamiento de los jugadores, la retención y la monetización del videojuego EcoAventura en un contexto local.

La delimitación geográfica permite realizar un análisis enfocado y generar resultados que sirvan como base para la toma de decisiones durante la etapa inicial del videojuego. No obstante, la arquitectura del proyecto y la metodología de análisis están diseñadas para facilitar su escalabilidad, permitiendo incorporar información de otras regiones de México e incluso de otros países conforme el videojuego amplíe su cobertura y disponibilidad en el futuro.

---

## Stakeholders

Los principales interesados en los resultados del proyecto son:

| Stakeholder | Necesidad |
|---|---|
| Responsable del videojuego | Conocer el desempeño general |
| Equipo de desarrollo | Identificar problemas de uso y retención |
| Responsable de monetización | Evaluar ventas e ingresos |
| Responsable de marketing | Analizar campañas y promociones |
| Analista de datos | Procesar e interpretar la información |
| Jugador | Consultar progreso, logros y artículos |
| Padre, madre o tutor | Revisar tiempo de juego y compras |

---
## Fuentes de datos

El proyecto integra datos simulados desde diferentes formatos.
