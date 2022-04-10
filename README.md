# ProyectoFinalCienciaDatos
Proyecto Final Ciencia de Datos en Python
![Universidad Galileo](https://www.galileo.edu/wp-content/themes/galileo-theme/img/logo-header.png)

•	Marvin Alejandro Diaz Castillo Carné: 9516008
•	Héctor Alfredo Vásquez Alarcón Carné: 21006402
Proyecto Final
Descripción
En este proyecto desarrollaremos un pipeline de Ingeniería de Datos utilizando Python, SQL y AWS para su desarrollo. ira trabajar con un dataset. El motivo del proyecto es poner en práctica lo aprendido en la clase Ciencia de Datos en Python,
Objetivos generales:
Realizar un ETL por medio de AWs Desarrollar un pipeline de Ingeniería de Datos utilizando Python, SQL y AWS para su desarrollo.
Objetivos específicos:
•	Extraer la información,
•	Transformación de los datos por medio de Python, previo a cargar la información a la base de datos. Utilizaremos librerías como Numpy y Pandas, para la exploración y análisis de la información. Para visualización de datos utilizaremos Matplotlib
•	Extraer información de las tablas por medio de SQL.
•	Creación de base de datos en la nube por medio de AWS en RDS
•	Crear ETLs
•	Resolver 5 preguntas con base a la información disponibles
Modelo de Datos
El modelo de datos a utilizar es un dataset de ventas denominado "sales data". Este dataset está disponible en Kaggle, por medio del link: https://www.kaggle.com/datasets/ankitchahal1/sales-data
La serie seleccionada es estructurada, consta de 25 columnas y 2823 filas.
Columnas del dataset:
•	ORDERNUMBER
•	QUANTITYORDERED
•	PRICEEACH
•	ORDERLINENUMBER
•	SALES
•	ORDERDATE
•	STATUS
•	QTR_ID
•	MONTH_ID
•	YEAR_ID
•	PRODUCTLINE
•	MSRP
•	PRODUCTCODE
•	CUSTOMERNAME
•	PHONE
•	ADDRESSLINE1
•	ADDRESSLINE2
•	CITY
•	STATE
•	POSTALCODE
•	COUNTRY
•	TERRITORY
•	CONTACTLASTNAME
•	CONTACTFIRSTNAME
•	DEALSIZE
Preguntas a responder
1.	¿Cuál es la línea de producto con mayores ventas?
2.	¿Qué país vende más?
3.	¿Cuál es el año con mayores ventas?
4.	Ventas por tamaño de Dealer
5.	¿Que Customer tiene mayores compras por año?
Procedimiento
•	Exploración inicial
En esta fase evaluaremos la información disponible y determinaremos los resultados que podríamos obtener
Empezaremos trabajando con un Jupyter Notebook.
Posteriormente importaremos librerías esenciales como NumPy, Pandas, Matplotlib.
Utilizamos Pandas para leer la información, obtener una breve vista de las primeras filas, y realizar análisis estadístico de las columnas numéricas.
•	Datos duplicados y limpieza de información
Identificar si existe información duplicada y si faltan valores en nuestro dataset
Calcular el número de filas duplicadas y borrarlas del modelo utilizando Pandas
•	Creación de Base de Datos en RDS
El motor de la base de datos es MySQL versión MySQL 5.7.37.
El nombre de la base de datos creada es bdproyecto

DETALLES TECNICOS
Análisis Exploratorio
Creación de Clúster en Redshift
o	Para la ejecución del modelo dimensional, se realizo un clúster AWS Redshift.
o	El clúster creado lo nombramos sales-clúster.
o	Para el actual proyecto fue suficiente la configuración de 1 nodo.
o	Habilitamos el permiso para poder acceder al cluster.
o	Agregamos las reglas de entrada para la configuración del puerto y la IP por el cual accederemos.
Extracción, Transformación y Carga (ETL)
Carga de dataset en Python
-	Importación de las librerías Panday y NumPy
-	Carga del dataset de manera local
-	Chequeamos las primeras filas del dataset
Creación de Dimensiones en Python:
-	Dimensión Customer
-	Dimensión Geografía
-	Dimensión Producto
-	Dimensión Dealer
-	Dimensión Tiempo
Creación de Fact Table en Python

Creación del Modelo Dimensional
Para la creación del modelo dimensional se definieron las siguientes dimensiones:
-	Geografía
-	Producto
-	Cliente
-	Distribuidora
-	Tiempo
Para la tabla de hechos definimos las variables:
-	Ventas
-	Cantidad
-	Total de ordenes
Carga de datos a Redshift
-	Cadena de conexión hacia Redshift
Creación de Tablas hacia datawarehouse
Script SQL
Insertar datos de Python hacia Redshift










