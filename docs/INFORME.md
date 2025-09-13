# Informe de proyecto: Análisis Exploratorio de Ventas E-commerce

## Indice

1. [Introducción](#1-introducción)
2. [Objetivos del Proyecto](#2-objetivos-del-proyecto)
3. [Descripción Temática de los Datos](#3-descripción-temática-de-los-datos)
4. [Hipótesis iniciales](#4-hipótesis-iniciales)
5. [Usuario Final y Nivel de Aplicación del Análisis](#5-usuario-final-y-nivel-de-aplicación-del-análisis)
6. [Análisis Exploratorio de Datos](#6-análisis-exploratorio-de-datos)
   - [6.1. Ventas Generales](#61-ventas-generales)
   - [6.2. Productos](#62-productos)
   - [6.3. Categorías](#63-categorías)
   - [6.4. Clientes](#64-clientes)
   - [6.5. Regiones o zonas](#65-regiones-o-zonas)
   - [6.6. Dispositivos](#66-dispositivos)
   - [6.7. Logística y Entregas](#67-logística-y-entregas)
7. [Conclusiones y Recomendaciones](#7-conclusiones-y-recomendaciones)
8. [Anexo y Recursos](#8-anexo-y-recursos)

## 1. Introducción

En el contexto actual del comercio digital, comprender el comportamiento de los clientes y el desempeño de los productos es clave para tomar decisiones informadas que impulsen las ventas y mejoren la eficiencia operativa. Este proyecto tiene como objetivo realizar un análisis exploratorio de un conjunto de datos reales de ventas de e-commerce, utilizando herramientas de Python y buenas prácticas de análisis de datos.

El análisis se centra en identificar patrones relevantes en las transacciones, detectar oportunidades comerciales no explotadas y generar insights accionables para áreas como marketing, ventas y logística. A lo largo del proyecto se aplicarán técnicas de limpieza, transformación, visualización y segmentación de datos, buscando responder preguntas clave del negocio tales como: ¿qué productos o categorías conviene promocionar?, ¿quiénes son los mejores clientes?, ¿cómo influyen los descuentos en el comportamiento de compra?, ¿qué regiones tienen mayor potencial comercial?, entre otras.

La información analizada proviene de un dataset disponible públicamente en Kaggle, que reúne un año de operaciones comerciales en una plataforma de e-commerce en América. Este conjunto de datos incluye variables como fecha de compra, producto, categoría, precio, cliente, ciudad de envío, tipo de dispositivo, tipo de inicio de sesión y tiempo de entrega.

En este informe se presenta un análisis exploratorio de un conjunto de datos de ventas de e-commerce con el objetivo de identificar patrones, tendencias y relaciones entre las variables. El conjunto de datos incluye información sobre transacciones, productos, clientes y categorías. Se utilizarán bibliotecas de Python como Pandas, Matplotlib y Seaborn para realizar el análisis.

## 2. Objetivos del Proyecto

El propósito principal de este proyecto es llevar a cabo un análisis exploratorio y visual de un conjunto de datos reales de ventas de e-commerce, con el fin de identificar patrones de comportamiento, evaluar el rendimiento comercial y generar conclusiones accionables que puedan apoyar la toma de decisiones estratégicas.

A través del uso de herramientas del ecosistema Python, se buscará responder una serie de preguntas clave del negocio vinculadas a productos, clientes, regiones y canales de compra. Este análisis incluirá desde la limpieza y transformación de los datos hasta la elaboración de visualizaciones que permitan comunicar hallazgos de forma clara y efectiva.

## 3. Descripción Temática de los Datos

Este proyecto se basa en un conjunto de datos reales de transacciones de e-commerce a lo largo de un año en América. El dataset refleja operaciones de compra online que contienen información tanto del cliente como del producto adquirido, la categoría, la cantidad y precio, el dispositivo utilizado y la región de destino.

El análisis está orientado a comprender los hábitos de consumo, identificar productos y categorías clave, evaluar el desempeño por regiones, y descubrir oportunidades de negocio a través de la visualización y exploración de datos.

Fuente: [Dataset de E-commerce](https://www.kaggle.com/datasets/mervemenekse/ecommerce-dataset)

## 4. Hipótesis inicales

Previo al análisis de datos, se plantean una serie de hipótesis que guían el enfoque exploratorio del proyecto. Estas hipótesis surgen tanto del conocimiento previo sobre dinámicas comunes del e-commerce como de preguntas estratégicas clave para áreas de marketing, ventas y logística.

Se parte de la idea de que las ventas presentan patrones estacionales, con meses de mayor actividad comercial —como diciembre— debido a campañas o eventos especiales. Asimismo, se espera que algunas categorías de productos concentren una parte significativa de los ingresos, ya sea por alto volumen de ventas o por su rentabilidad individual.

También se presupone que ciertas regiones o zonas presentan un bajo volumen de ventas pero un ticket promedio elevado, lo cual podría indicar oportunidades comerciales no explotadas. Del mismo modo, se plantea que los clientes frecuentes y con comportamiento repetitivo aportan más valor al negocio, y que estos podrían identificarse para estrategias de fidelización.

En cuanto a los factores operativos, se cree que el tiempo de entrega impacta en la satisfacción del cliente, y que puede variar significativamente entre regiones o meses. Por otro lado, se anticipa que el tipo de dispositivo (móvil o web) y el tipo de inicio de sesión (miembro o invitado) pueden influir en el comportamiento de compra, como el monto gastado o la cantidad de productos adquiridos.

Finalmente, se buscará explorar si existen diferencias relevantes por género, tanto en los productos comprados como en las categorías preferidas, así como patrones de compra relacionados con la fecha y la hora (como días de mayor tráfico o franjas horarias más activas).

## 5. Usuario Final y Nivel de Aplicación del Análisis

**Uuario Final**: Equipos de marketing, ventas y analistas de negocio en una empresa de e-commerce.

**Nivel de Aplicación**: Estratégico-operativo. El análisis busca dar soporte a decisiones tácticas sobre promociones, segmentación de clientes, optimización logística y diseño de campañas comerciales.

## 6. Análisis Exploratorio de Datos

### 6.1. Ventas Generales

**Objetivo**: Analizar el volumen y la evolución total de ventas, así como identificar patrones según el calendario y el horario.

#### Total de ventas ($ y unidades).

Se vendieron un total de $7.812.164 y 128.357 unidades en el período analizado. Este valor nos da un panorama inicial sobre el volumen del negocio, permitiendo evaluar estrategias comerciales o presupuestarias.

#### Ventas mensuales

El gráfico de línea muestra que las ventas tienen un comportamiento creciente a lo largo del año, con picos notables en los meses de mayo, julio y noviembre. Esto puede reflejar estacionalidad, promociones u otras campañas comerciales.

![Ventas mensuales](../images/graph_1.png)

#### Ventas por hora y día

Según el mapa de calor, las ventas se concentran mayormente entre las 10:00 y las 22:00, especialmente los días martes y miércoles. Esto es coherente con los picos vistos en el gráfico anterior y sugiere que los usuarios compran más en horario laboral/tarde.

![Ventas por hora y día - mapa de calor](../images/graph_2.png)

Preguntas que responde:

**¿Cómo influyen la fecha y la hora en las ventas?**

Se observa un patrón semanal donde martes y miércoles concentran las mayores ventas, y un patrón horario que indica más actividad entre las 10:00 y las 22:00. Además, se identifica una evolución mensual creciente, con ciertos picos estacionales que podrían relacionarse con campañas o fechas comerciales.

### 6.2. Productos

Objetivo: Evaluar el desempeño de los productos según cantidad vendida, rentabilidad y efecto de los descuentos.

#### Top 10 productos más vendidos

![Top 10 productos más vendidos](../images/graph_3.png)

El gráfico muestra que los productos más vendidos en unidades fueron:

- Titan Watch (6.254 unidades),
- Formal Shoes, Sports Wear y Running Shoes (más de 6.000 cada uno),
- así como Fossil Watch, Sneakers y T-Shirts.

Esto indica una alta rotación de estos productos, lo que puede deberse a popularidad, precio accesible o campañas efectivas.

#### Productos más rentables

En cuanto a ganancia total, los T-Shirts lideran el ranking con más de $340.000, seguidos por Titan Watch, Running Shoes y Jeans. A pesar de no ser los más vendidos en unidades, algunos productos (como Jeans, Towels y Sofa Covers) destacan por su alto margen unitario.

![Productos más rentables](../images/graph_4.png)

#### Comparación de productos con y sin descuentos

Al analizar los 10 productos más vendidos en valor, se observa que todos fueron vendidos exclusivamente con descuentos. Esto evidencia una fuerte dependencia del precio promocional para alcanzar altos niveles de venta. Es probable que estos productos tengan una alta sensibilidad al precio, por lo que las promociones cumplen un rol clave en su desempeño.

![Productos con y sin descuentos](../images/graph_5.png)

Preguntas que responde:

**¿Qué productos conviene promocionar?**
Los productos que aparecen en el Top 10 de unidades vendidas y ganancia total (como "T-Shirts", "Titan Watch", "Formal Shoes") muestran un buen rendimiento general. Además, al venderse completamente con descuento, se sugiere continuar promocionándolos para mantener su volumen.

**¿Qué producto obtiene más beneficios por unidad?**

Aunque no se muestra en forma directa, productos como "T-Shirts" y "Running Shoes" aparecen tanto en los rankings de volumen como en el de ganancia, lo que indica una alta rentabilidad por unidad.

**¿Cómo afectan los descuentos a las ventas?**

Se observa que en todos los casos del Top 10 de ventas en valor, las ventas se lograron solo cuando se aplicaron descuentos, lo que sugiere que los descuentos fueron determinantes para el volumen de ventas.

### 6.3. Categorías

Objetivo: Evaluar el desempeño de las categorías.

#### Ventas totales por categoría

![Ventas totales por categoría](../images/graph_6.png)

- Fashion lidera con más de **$4.35M**, duplicando a Home & Furniture **($1.98M)**.
- Esto demuestra que la categoría de moda es claramente la más relevante en términos de facturación.

#### Ticket promedio por categoría.

![Ticket promedio por categoría](../images/graph_7.png)

- Fashion también tiene el ticket promedio más alto: $169.46, lo que indica que las compras individuales en esta categoría son de mayor valor.
- Las demás rondan entre $127.98 y $146.15, con Home & Furniture como la de menor ticket promedio.

#### Productos más vendidos dentro de cada categoría.

| Id  | Product_Category   | Product                | Quantity |
| --- | ------------------ | ---------------------- | -------- |
| 2   | Auto & Accessories | Car Body Covers        | 2040.0   |
| 5   | Auto & Accessories | Car Pillow & Neck Rest | 2012.0   |
| 8   | Auto & Accessories | Tyre                   | 2010.0   |
| 18  | Electronic         | Speakers               | 581.0    |
| 10  | Electronic         | Fans                   | 523.0    |
| 17  | Electronic         | Samsung Mobile         | 501.0    |
| 31  | Fashion            | Titak watch            | 6254.0   |
| 22  | Fashion            | Formal Shoes           | 6154.0   |
| 28  | Fashion            | Sports Wear            | 6093.0   |
| 33  | Home & Furniture   | Beds                   | 3908.0   |
| 36  | Home & Furniture   | Dinning Tables         | 3874.0   |
| 38  | Home & Furniture   | Sofa Covers            | 3852.0   |

Esto muestra que dentro de cada categoría hay productos estrella con alto desempeño.

#### Distribución por género dentro de cada categoría

![Distribución por género dentro de cada categoría](../images/graph_8.png)

- Fashion es la categoría más comprada por ambos géneros, aunque con mayor volumen por hombres (14.281) que mujeres (11.365).

- Home & Furniture tiene una distribución más pareja.

- En Auto & Accessories, predominan los hombres.

- En Electronic, la diferencia es mínima.

Preguntas que responde:

**¿Qué categorías conviene promocionar?**

Fashion, por su volumen total de ventas, alto ticket promedio y fuerte demanda en ambos géneros. También puede convenir Auto & Accessories, por su buen ticket y alto interés masculino.

**¿Qué categorías de productos vendo?**

Fashion, Home & Furniture, Auto & Accessories, y Electronic.

**¿Distribución por género/categoría?**

Hombres compran más en todas las categorías menos en Home & Furniture, donde hay un equilibrio. Fashion es dominante en ambos géneros, ideal para campañas generales.

### 6.4. Clientes

Objetivo: Conocer el comportamiento de los clientes.

¿Quiénes son los que más compran?

Ticket promedio por cliente.

Frecuencia de compra (n° de compras por cliente).

Análisis por tipo de login (Guest vs Member).

Distribución por género.

Preguntas que responde:

¿Quiénes conforman mi base de clientes?

¿Qué clientes deberían estar en un programa de fidelización?

¿Qué tipo de inicio de sesión prefieren mis clientes?

¿A quién le vendo qué categorías? (cruce cliente-género-producto)

### 6.5. Regiones o zonas

Objetivo: Analizar ventas por ubicación.

Ventas por ciudad o región.

Ticket promedio por región.

Mapa (si tenés coordenadas o ciudad/estado).

Preguntas que responde:

¿En qué región se vende más?

¿Qué zonas están poco explotadas?

### 6.6. Dispositivos

Objetivo: Ver patrones por canal de acceso.

Ventas por tipo de dispositivo (web vs mobile).

Comportamiento comparado: ticket promedio, cantidad de productos.

Pregunta que responde:

¿Qué dispositivos usan mis clientes para contactarme?

### 6.7. Logística y Entregas

Objetivo: Evaluar eficiencia en la entrega.

Distribución de “Aging” (días de entrega).

Comparación por mes / producto / región.

Pregunta que responde:

¿Cuál es mi velocidad de entrega y cómo varía?

## 7. Conclusiones y Recomendaciones

## 8. Anexo y Recursos
