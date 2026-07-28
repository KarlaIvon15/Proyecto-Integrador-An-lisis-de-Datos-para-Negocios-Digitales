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
