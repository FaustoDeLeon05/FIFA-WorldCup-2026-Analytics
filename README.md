# Proyecto: FIFA World Cup 2026 - Player Performance & Scouting Analytics

Proyecto de análisis de rendimiento de jugadores y selecciones ambientado en la **Copa Mundial FIFA 2026**, desarrollado mediante **Python, Pandas y Power BI**.

> **Nota sobre los datos:** El dataset utilizado es **sintético** y fue construido con una temática relacionada con la FIFA World Cup 2026. Los jugadores, selecciones, partidos y métricas contenidas en el dataset no representan necesariamente personas, equipos o resultados reales de la competición. Por lo tanto, los análisis y visualizaciones presentados en este proyecto tienen un propósito **educativo y demostrativo**, y no deben interpretarse como estadísticas oficiales ni como scouting real de jugadores.
> 
---

## Vista previa de las páginas del reporte

<p align="center">
  
<img width="1552" height="882" alt="Pagina 2" src="https://github.com/user-attachments/assets/0e73c9dc-c68c-4722-ab71-4f6cbb5aff56" />

<img width="1552" height="882" alt="Pagina 1" src="https://github.com/user-attachments/assets/09bd1184-bf69-4a7b-80e7-fd81d2eb8b85" />

<img width="1456" height="822" alt="Pagina 3" src="https://github.com/user-attachments/assets/d561a373-6df8-4f1d-b3a8-dbf0674046fe" />

<img width="1456" height="817" alt="Pagina 4" src="https://github.com/user-attachments/assets/8e261e32-769f-498f-8bae-4c5ee73f8851" />


</p>

## Descripción del proyecto

El objetivo del proyecto es transformar datos sintéticos de rendimiento de jugadores y resultados de partidos en información estructurada para facilitar el análisis de **rendimiento individual, comparación por posiciones y evaluación del desempeño de las selecciones nacionales** dentro del escenario planteado por el dataset.

El dataset trabaja a nivel de **jugador-partido**, permitiendo analizar el comportamiento de los jugadores durante las diferentes fases del torneo.

El flujo implementado es:

**Dataset → Python / Pandas → EDA & Data Quality → Modelo Dimensional → DAX → Power BI**

El proyecto está orientado a demostrar un flujo de trabajo de **Data Analytics y Business Intelligence**, desde la exploración y preparación de los datos hasta la construcción de un dashboard interactivo.

## Objetivos

- Analizar el rendimiento individual de los jugadores dentro del dataset.
- Explorar métricas ofensivas, defensivas y de creación de juego.
- Comparar el rendimiento de jugadores según su posición.
- Analizar el rendimiento de las selecciones nacionales representadas en el dataset.
- Validar la calidad y consistencia de los datos.
- Construir un modelo dimensional para facilitar el análisis en Power BI.
- Desarrollar medidas DAX reutilizables para los principales indicadores.
- Crear un dashboard interactivo orientado al análisis de rendimiento y scouting dentro del escenario sintético del proyecto.
- Aplicar principios de modelado y visualización utilizados en soluciones de Business Intelligence.


## Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| Python | Preparación y análisis de datos |
| Pandas | Manipulación y transformación de datos |
| Matplotlib | Visualización durante el EDA |
| Seaborn | Visualización durante el EDA |
| Jupyter Notebook | Desarrollo del análisis exploratorio |
| Power BI | Modelado, DAX y visualización |
| DAX | Desarrollo de métricas analíticas |

## Estructura del Repositorio

* **Data/**: Almacena el dataset sintético obtenido de Kaggle, utilizado como fuente principal del proyecto. (FIFA World Cup 2026 Player Performance).
* **Reports/**: Contiene el archivo final del dashboard interactivo en Power BI (`.pbix`).
* **Source/**: Contiene los Jupyter Notebooks (`.ipynb`) con el código en Python para el Análisis Exploratorio de Datos (EDA).


## Dataset

El proyecto utiliza un dataset **sintético** de rendimiento de jugadores ambientado en la **FIFA World Cup 2026**.

Los datos fueron utilizados como escenario para desarrollar un proyecto de Data Analytics y Business Intelligence, permitiendo trabajar con información de jugadores, partidos, selecciones y métricas de rendimiento sin representar estadísticas oficiales de la competición.

### Características principales

| Característica | Valor |
|---|---:|
| Registros | 54,600 |
| Columnas | 75 |
| Jugadores únicos | 1,248 |
| Partidos | 1,050 |
| Selecciones | 48 |
| Posiciones | 4 |
| Fecha inicial | 11 de junio de 2026 |
| Fecha final | 31 de julio de 2026 |
| Registros por partido | 52 |
| Valores nulos | 0 |
| Filas duplicadas completas | 0 |

El nivel de granularidad principal del dataset es: **Jugador × Partido**

### Principales posiciones

- Goalkeeper
- Defender
- Midfielder
- Forward

### Principales grupos de variables

El dataset contiene información relacionada con:

- Identificación del jugador
- Selección y rival
- Partido y fase del torneo
- Goles y asistencias
- Tiros y tiros a puerta
- Expected Goals (xG)
- Expected Assists (xA)
- Pases y pases clave
- Regates
- Entradas e intercepciones
- Despejes y bloqueos
- Duelos aéreos
- Atajadas y goles concedidos
- Distancia recorrida
- Velocidad máxima
- Aceleraciones y desaceleraciones
- Indicadores de rendimiento
- Contribución ofensiva y defensiva
- Creatividad
- Consistencia
- Player of the Match
- Rating del torneo

## Flujo de datos

### 1. Extract — Extracción

Se parte del dataset sintético de rendimiento de jugadores ambientado en la FIFA World Cup 2026.

El archivo original se encuentra dentro de: `Data/`

### 2. Explore — Análisis Exploratorio

El análisis exploratorio fue desarrollado utilizando **Python y Pandas**.

Durante esta etapa se revisaron:

- Dimensiones del dataset.
- Tipos de datos.
- Valores nulos.
- Registros duplicados.
- Cardinalidad de variables.
- Distribución de jugadores.
- Selecciones participantes.
- Posiciones.
- Variables de rendimiento.
- Métricas ofensivas y defensivas.
- Distribución de las principales variables numéricas.

El objetivo fue comprender la estructura del dataset antes de construir el modelo analítico.

### 3. Data Quality — Validación

Como parte del proceso de preparación se realizaron validaciones sobre la calidad del dataset.

Entre las comprobaciones realizadas:

- Validación de valores nulos.
- Identificación de duplicados.
- Revisión de tipos de datos.
- Validación de identificadores.
- Revisión de relaciones entre jugadores, partidos y selecciones.
- Validación de la granularidad jugador-partido.

El dataset utilizado presenta:

- **0 valores nulos**
- **0 filas completamente duplicadas**

### 4. Data Modeling — Modelado

A partir del dataset original se construyó un modelo dimensional orientado al análisis en Power BI.

El modelo utiliza dimensiones y tablas de hechos separadas para facilitar el análisis y mantener una estructura de datos organizada.

## Modelo dimensional

El modelo está compuesto por siete tablas principales.

### Dimensiones

#### Dim_Player

Contiene información descriptiva de los jugadores:

- player_id
- player_name
- age
- nationality
- position
- height_cm
- weight_kg
- preferred_foot
- club_name
- market_value_eur

#### Dim_Team

Contiene la información de las selecciones:

- team_id
- team_name

#### Dim_Match

Contiene información relacionada con los partidos:

- match_id
- match_date
- stadium
- city
- tournament_stage

#### Dim_Date

Dimensión calendario utilizada para el análisis temporal:

- Date
- Year
- Month_Number
- Month
- Quarter
- Year_Month
- Day
- Day_of_Week_Number
- Day_of_Week

#### Dim_Flag

Tabla creada en Power BI para gestionar la visualización dinámica de las banderas de las 48 selecciones representadas en el dataset.

- country_name
- flag_url
- iso2


### Tablas de hechos

#### Fact_Player_Match

Contiene las métricas de rendimiento de cada jugador por partido.

Incluye información como:

- player_id
- match_id
- team
- opponent_team
- minutes_played
- goles
- asistencias
- tiros
- tiros a puerta
- xG
- xA
- pases
- métricas defensivas
- métricas físicas
- indicadores de rendimiento

#### Fact_Team_Match

Contiene información del rendimiento de cada selección por partido:

- match_id
- team_id
- opponent_team_id
- goals_team
- goals_opponent
- match_result
- tournament_stage

## Modelo semántico en Power BI

El modelo semántico fue construido para permitir el análisis de jugadores, posiciones, selecciones y fases del torneo.

Las medidas DAX fueron organizadas mediante Display Folders para separar los principales grupos analíticos:
```text
_Measures
├── 01. Rendimiento
├── 02. Ofensiva
├── 03. Pase y creación
├── 04. Defensa
├── 05. Porteros
├── 06. Selecciones
└── 07. Misc
```

### Métricas principales

#### Rendimiento
- Partidos
- Goles
- Goles por partido
- Asistencias
- Asistencias por partido

#### Ofensiva
- Tiros
- Tiros a puerta
- Goles esperados
- Asistencias esperadas
- Goles vs Goles esperados
- Efectividad de tiro
- Conversión de tiro

#### Pase y creación
- Pases completados
- Pases totales
- Precisión de pase
- Pases clave

#### Defensa
- Entradas
- Intercepciones
- Despejes
- Bloqueos
- Acciones defensivas
- Duelos aéreos ganados
- Duelos aéreos perdidos

#### Porteros
- Atajadas
- Goles concedidos
- Porterías a cero
- Penales atajados
- Promedio de goles concedidos

#### Selecciones
- Partidos de selección
- Goles a favor
- Goles en contra
- Diferencia de goles
- Victorias
- Empates
- Derrotas

#### Misc
- Bandera URL Seleccionada
- Club Seleccionado
- Edad Seleccionada
- Goles a Favor (Ranking)
- Goles en Contra (Ranking)
- Jugador Seleccionado
- Nacionalidad Seleccionada
- Pie Seleccionado
- Posicion Seleccionada
- Valor de Mercado Seleccionado


## Elementos del reporte

El dashboard final está compuesto por 4 páginas analíticas principales, cada una con un menú de navegación que permite desplazarse entre páginas, acceder directamente a cualquier sección del reporte y restablecer los filtros aplicados.

### 1. Delanteros & Mediocampistas

Página orientada al análisis de jugadores de las posiciones Forward y Midfielder.

Incluye:

- Selección de jugador
- Selección de selección nacional
- Filtro por posición
- Perfil del jugador
- Bandera dinámica de la selección
- Goles
- Asistencias
- Goles por partido
- Precisión de pase

#### Principales visualizaciones:

- Goles vs. goles esperados por fase.
- Tiros vs. tiros a puerta por fase.
- Creación de juego por fase.

### 2. Defensas

Página enfocada en el análisis de jugadores de posición Defender.

Incluye:

- Selección de jugador
- Selección de selección nacional
- Perfil del jugador
- Bandera dinámica
- Entradas
- Intercepciones
- Despejes
- Acciones defensivas

#### Principales visualizaciones:

- Entradas vs. intercepciones.
- Despejes vs. bloqueos.
- Duelos aéreos ganados vs. perdidos.

### 3. Porteros

Página dedicada al análisis de jugadores de posición Goalkeeper.

Incluye:

- Selección de jugador
- Selección de selección nacional
- Perfil del jugador
- Bandera dinámica
- Partidos
- Atajadas
- Porterías a cero
- Goles concedidos

#### Principales visualizaciones:

- Atajadas vs. goles concedidos por fase
- Porterías a cero por fase
- Penales atajados por fase

### 4. Selecciones Nacionales

Página orientada al análisis del rendimiento de las selecciones dentro del dataset.

Incluye:

- Selector de selección
- Indicadores generales de rendimiento
- Bandera de la selección
- Diferencia de goles por fase

#### Principales visualizaciones:

- Diferencia de goles por fase
- Goles a favor vs. goles en contra por fase
- Resultados por fase del torneo
- Ranking de selecciones: goles a favor vs. goles en contra
  
## Resultado

El proyecto integra:

- Análisis exploratorio con Python y Pandas.
- Validación de calidad de datos.
- Modelo dimensional.
- Modelo semántico en Power BI.
- Medidas DAX organizadas por categorías.
- Dashboard interactivo de 4 páginas.
- Análisis diferenciado por posición.
- Análisis del rendimiento de selecciones.
- Indicadores de rendimiento ofensivo, defensivo y de porteros.

El resultado es una solución de Data Analytics y Business Intelligence desarrollada sobre un dataset sintético, utilizando un escenario deportivo como contexto para demostrar competencias de análisis, modelado y visualización de datos.

## Análisis de rendimiento del modelo

Como siguiente etapa del proyecto se contempla el análisis de rendimiento del modelo y de las consultas utilizando DAX Studio y VertiPaq Analyzer.  

Esta fase permitirá analizar aspectos como:
- Rendimiento de consultas DAX
- Consumo de memoria
- Tamaño de tablas y columnas
- Cardinalidad
- Eficiencia del modelo
- Posibles oportunidades de optimización

Esta etapa corresponde a una fase posterior del proyecto y no forma parte de los resultados actualmente documentados.

## Videos del reporte/Dashboard
https://github.com/user-attachments/assets/d6cfc176-8895-4ca8-afd9-749326cce011

## Enfoque de portafolio

El proyecto busca demostrar competencias prácticas en:

**Python → EDA → Data Quality → Data Modeling → DAX → Power BI → Business Intelligence**

El objetivo es mostrar un flujo de trabajo de análisis de datos, desde la exploración y validación de un dataset sintético hasta la construcción de un modelo analítico y un dashboard interactivo.

## Autor
**Fausto Xavier De León Pichardo**
**Data Engineering · Data Analytics · SQL · Python · Power BI · ETL · Data Quality**
Estudiante de Ingeniería en Sistemas de Computación, orientado al desarrollo de proyectos en **Data Analytics, Data Engineering y Business Intelligence**.

- GitHub: [FaustoDeLeon05](https://github.com/FaustoDeLeon05)
- LinkedIn: [Fausto X. De León Pichardo](https://www.linkedin.com/in/fausto-xavier-de-leon-pichardo-bi2026/)

## Licencia
Este proyecto está disponible bajo la licencia **MIT**.

