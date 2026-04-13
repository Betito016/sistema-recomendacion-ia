# sistema-recomendacion-ia
# Sistema de Recomendación de Películas con IA

[![Streamlit App]([https://sistema-recomendacion-ia-fdgiy8syu7kpbu7vmt8o2o.streamlit.app/](https://sistema-recomendacion-ia-fdgiy8syu7kpbu7vmt8o2o.streamlit.app/))

## 📝 Descripción del Proyecto
Este repositorio contiene una aplicación web interactiva que utiliza Inteligencia Artificial para recomendar películas de forma personalizada. A través de un enfoque de **Filtrado Colaborativo**, el sistema analiza las preferencias del usuario en tiempo real y predice matemáticamente su afinidad con cientos de títulos que aún no ha visto.

Puedes probar la aplicación en vivo haciendo clic en el botón de Streamlit de arriba.

## 🧠 ¿Cómo funciona el algoritmo?
El motor de recomendación está construido desde cero utilizando **Completación de Matrices** y **SVD (Descomposición en Valores Singulares)**. 

1. **Resolución del Cold Start:** El usuario interactúa con la interfaz web para evaluar 5 películas clásicas.
2. **Inyección de Datos:** Estas calificaciones se inyectan en una matriz dispersa (User-Item Matrix) generada a partir del dataset histórico *MovieLens 100k*.
3. **Reducción de Dimensionalidad:** A través del algoritmo SVD, comprimimos el catálogo en 20 "factores latentes", descubriendo patrones ocultos de correlación entre usuarios y géneros cinematográficos.
4. **Predicción y Filtrado:** El sistema reconstruye la matriz completa, predice las calificaciones de las celdas vacías (RMSE comprobado de ~0.97) y filtra las películas previamente vistas para entregar un Top 3 de descubrimientos.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.11
* **Frontend & Hosting:** Streamlit Community Cloud
* **Manipulación de Datos:** Pandas, NumPy
* **Matemáticas y Machine Learning:** SciPy (SVD)
* **Dataset:** MovieLens (`u.data`, `u.item`)

## 🚀 Cómo ejecutarlo localmente
Si deseas clonar este proyecto y explorar el código o correrlo en tu propia máquina:

1. Clona el repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/sistema-recomendacion-ia.git](https://github.com/TU_USUARIO/sistema-recomendacion-ia.git)
