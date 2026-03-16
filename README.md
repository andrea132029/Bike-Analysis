# 🚲 Bike Analysis - Análisis de viajes en bicicleta

## 📊 Descripción del proyecto

Este proyecto consiste en el análisis de datos de un sistema de bicicletas compartidas con el objetivo de identificar patrones de uso entre dos tipos de usuarios:
* Usuarios miembros (member)
* Usuarios casuales (casual)

El análisis busca comprender cómo utilizan el servicio ambos tipos de usuarios para detectar diferencias en su comportamiento.

Este tipo de análisis puede ayudar a las empresas de bicicletas compartidas a desarrollar estrategias para **convertir usuarios casuales en miembros**.

---

## 🛠 Herramientas utilizadas

En este proyecto se utilizaron las siguientes herramientas:

* **SQL** → para realizar consultas y obtener métricas del dataset
* **R** → para el análisis de datos
* **ggplot2** → para la visualización de datos
* **CSV** → para almacenar los resultados de las consultas
* **GitHub** → para el control de versiones y publicación del proyecto

---


## 🔎 Proceso de análisis

### 1- Extracción de datos

Se realizaron consultas SQL sobre la base de datos de viajes para obtener métricas relevantes.

Ejemplo de consulta utilizada:

```sql
SELECT 
MIN(ride_length) AS min_ride,
MAX(ride_length) AS max_ride
FROM trips;
```

Los resultados de estas consultas fueron exportados en formato **CSV**.

---

### 2- Análisis de datos en R

Los archivos CSV fueron importados en R para su análisis.

Ejemplo:

```r
df <- read.csv("ride_length_stats.csv")
```

Posteriormente se realizaron transformaciones y cálculos necesarios para generar visualizaciones.

---

### 3- Visualización de datos

Se utilizaron gráficos para representar la información obtenida.

Ejemplo de visualización en R:

```r
ggplot(df_long, aes(x = metric, y = value, fill = metric)) +
  geom_bar(stat = "identity") +
  theme_minimal()
```

---

## 📈 Resultados del análisis

A partir del análisis se pudieron observar algunos patrones:

* Existen diferencias en la **duración de los viajes** entre usuarios miembros y casuales.
* Los usuarios miembros suelen realizar **viajes más frecuentes**.
* Algunos registros presentan valores extremos en la duración del viaje, lo que puede indicar **outliers**.

---

## 🎯 Conclusión

El análisis permite identificar comportamientos diferentes entre los tipos de usuarios.
Estos resultados pueden ser útiles para diseñar estrategias que incentiven a los usuarios casuales a convertirse en miembros.

---

## 👩‍💻 Autor

**Andrea Avalo**

Estudiante de Técnica en Sistemas de la Información
Interesada en análisis de datos, SQL y visualización de datos.

GitHub:
https://github.com/andrea132029
Linkedin: 
https://www.linkedin.com/in/andrea-avalo?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BZlX0HnwdQj%2BKLzqd4Z5new%3D%3D
