Proyecto ETL + EDA de Ventas (Reglas de Negocio)

📚 Descripción General

Este proyecto tiene como objetivo aplicar un proceso ETL (Extract, Transform, Load) y un Análisis Exploratorio de Datos (EDA) sobre un conjunto de datos de ventas.
El análisis permite obtener métricas clave del negocio, evaluar la calidad de los datos y generar visualizaciones que aporten insights sobre el rendimiento comercial.

⚙️ Tecnologías Utilizadas

Python 3.10+

Pandas — Limpieza, transformación y análisis de datos.

NumPy — Cálculos numéricos y estadísticos.

Matplotlib / Seaborn — Visualización de datos.

🧩 Proceso ETL

1️⃣ Extract (Extracción)

Se carga el dataset ventas_reglas_negocio.csv con 2000 registros y 11 columnas.
Variables principales:

fecha, cliente, producto, categoria, cantidad, precio_unitario, descuento, metodo_pago, ciudad, total_venta.

2️⃣ Transform (Transformación)

Se realiza una limpieza y estandarización de datos:

Eliminación de duplicados: No se detectaron registros duplicados.

Manejo de nulos:

cliente, categoria, ciudad, metodo_pago → se reemplazaron por "Desconocido".

descuento → valores nulos reemplazados por 0.

precio_unitario y fecha → filas eliminadas por regla de negocio.

Conversión de tipos: fecha convertida a formato datetime.

Creación de nuevas columnas:

año/mes → período de la venta.

dia → nombre del día de la semana.

margen → calculado como el 20% del total de venta (total_venta * 0.2).

3️⃣ Load (Carga)

El dataset limpio se exportó como:

ETL_EDA_limpio.csv

📊 Análisis Exploratorio (EDA)
📈 Métricas principales
Indicador	Valor
💰 Total de ventas	$11.694.537,10
🧾 Ticket promedio	$6.171,26
📉 Margen total estimado	$2.338.907,38
🏆 Participación por categoría
Categoría	Participación (%)
Electrónica	38,49
Tecnología	27,02
Muebles	20,25
Oficina	9,82
Desconocido	4,41
📊 Visualizaciones Clave

Ventas por Categoría
Gráfico de barras que muestra el total de ventas acumuladas por tipo de producto.

Ciudades con más ventas
Ranking de las 5 ciudades con mayores ingresos, excluyendo los registros “Desconocido”.

Evolución de Ventas por Mes
Línea temporal que representa la tendencia de ventas a lo largo del tiempo (año/mes).

💡 Conclusiones

Las ventas totales ascienden a $11,7 millones, con un margen promedio del 20 %, lo que indica una estructura rentable.

Tecnología (27 %) y Electrónica (38 %) concentran el 65 % de las ventas, mostrando una fuerte dependencia del segmento tecnológico.

El grupo “Desconocido” (4,4 %) sugiere que existe margen de mejora en la calidad de los datos durante el proceso de carga o recolección.

🚀 Recomendaciones

Gestión de datos:

Reclasificar o eliminar la categoría “Desconocido” para mejorar la precisión de los reportes.

Estrategia comercial:

Potenciar las categorías Tecnología y Electrónica (mayor aporte de ingresos).

Implementar promociones o descuentos en Oficina y Muebles para diversificar las ventas.

Análisis futuro:

Incorporar métricas de evolución trimestral o por provincia.

Evaluar el ticket promedio por categoría para identificar productos más rentables.

🧠 Autor

Bruno Argañaraz
📊 Analista de Datos | Power BI | Python | SQL | ETL
🔗 GitHub

<img width="922" height="546" alt="descarga (1)" src="https://github.com/user-attachments/assets/625e984a-1448-4f39-bf81-6e0ea92006cc" />
<img width="833" height="622" alt="descarga" src="https://github.com/user-attachments/assets/03d6a95d-1c8f-4138-a3c8-2c1a35b02e54" />
<img width="857" height="563" alt="descarga (2)" src="https://github.com/user-attachments/assets/9306be48-0d02-44e3-99de-957926410344" />
