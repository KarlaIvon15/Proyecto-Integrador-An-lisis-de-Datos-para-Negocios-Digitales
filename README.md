# Analítica de jugadores y monetización de EcoAventura.

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
**Análisis de Datos**, enfocado en estudiar el comportamiento de los jugadores y la
monetización del videojuego **EcoAventura**.

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

**EcoAventura** es un videojuego educativo de tipo **aventura, exploración y conciencia 
ambiental**, diseñado principalmente para niños de entre 6 y 11 años.

La dinámica principal consiste en que el jugador explora escenarios inspirados en el 
entorno natural de Xicotepec de Juárez, Puebla, mientras completa diferentes retos 
relacionados con el cuidado del medio ambiente.

Las principales actividades dentro del videojuego incluyen:

- Completar niveles y misiones ecológicas.
- Recolectar residuos dentro del escenario.
- Clasificar correctamente los diferentes tipos de basura.
- Obtener puntos y recompensas.
- Desbloquear nuevos escenarios.
- Personalizar personajes mediante skins y accesorios.
- Participar en eventos especiales.

El videojuego se adquiere mediante un pago único. Posteriormente, los jugadores pueden 
comprar artículos cosméticos opcionales que permiten personalizar su experiencia sin 
afectar las habilidades o ventajas dentro del juego.

---

## Planteamiento del problema

El videojuego registra jugadores, sesiones, progreso, visitas a la tienda virtual y
compras de skins. Sin embargo, no se dispone de un sistema analítico que permita
comprender de manera integral:

- En qué localidades se encuentran los jugadores más activos.
- Qué zonas generan mayor cantidad de compras.
- Cuáles skins son las más y menos vendidas.
- Qué jugadores presentan riesgo de abandono.
- En qué días y horarios se utiliza más el videojuego.
- Qué características se relacionan con la compra de skins.
- Qué campañas o promociones generan mejores resultados.
- Cómo evoluciona la retención de los jugadores.

Esta falta de información dificulta tomar decisiones relacionadas con actualizaciones,
diseño de skins, precios, promociones, campañas y experiencia de usuario.

---

## Justificación

El análisis de datos permite transformar registros de actividad y compras en
información útil para la toma de decisiones.

El proyecto permitirá:

- Conocer el comportamiento de los jugadores.
- Identificar localidades con mayor actividad.
- Detectar jugadores activos, ocasionales, en riesgo e inactivos.
- Analizar el rendimiento comercial de las skins.
- Evaluar el ingreso generado por el pago inicial y por compras internas.
- Medir la retención de jugadores.
- Identificar horarios de mayor actividad.
- Diseñar estrategias basadas en resultados.
- Crear dashboards orientados a diferentes usuarios.

Aunque los datos son simulados, se diseñaron con reglas de negocio, tendencias
temporales y relaciones coherentes para representar un escenario analítico realista.

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

El proyecto considera información simulada de jugadores pertenecientes al municipio de
Xicotepec de Juárez, Puebla.

Se utilizará un catálogo de localidades seleccionadas y validadas por el equipo.

Las localidades utilizadas para el análisis son:

- Xicotepec de Juárez.
- Villa Ávila Camacho (La Ceiba).
- San Agustín Atlihuácan
- San Antonio Ocopetlatlán
- Tlaxcalantongo
- Gilberto Camacho
- Santa Rita
- San Pedro Ixtla
- Ahuaxintitla
- Tierra Negra
- Jalapilla
- Los Limones
- Nactanca Grande
- Rancho Nuevo
- Las Pilas
- Tlapehuala

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

### Fuente 1: archivos CSV

Contienen información estructurada de:

- Jugadores.
- Tutores.
- Catálogo de skins.
- Compras del videojuego.
- Compras de skins.
- Campañas.
- Progreso.

### Fuente 2: archivos JSON

Contienen información de:

- Sesiones de juego.
- Eventos dentro del videojuego.
- Visitas a la tienda.
- Visualización de skins.
- Intentos de compra.

### Fuente 3: base de datos SQLite

Esta base de datos permite centralizar la información generada a partir de los archivos CSV y JSON para facilitar las consultas, análisis estadísticos y generación de indicadores.

Las principales entidades almacenadas son:

- Jugadores.
- Tutores responsables.
- Localidades.
- Partidas realizadas.
- Sesiones de juego.
- Progreso del jugador.
- Catálogo de skins.
- Compras realizadas.
- Eventos dentro del videojuego.
- Métricas de actividad y retención.
