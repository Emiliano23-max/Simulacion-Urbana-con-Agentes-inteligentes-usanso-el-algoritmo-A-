Un entorno de simulación computacional avanzado diseñado para modelar, analizar y optimizar el flujo de tráfico multimodal (interacción entre peatones y vehículos) en una red urbana mallada. El sistema utiliza un enfoque basado en Modelado Basado en Agentes (ABM) mediante la librería AgentPy y toma de decisiones de ruta autónomas mediante el algoritmo de búsqueda A*.

📑 Tabla de Contenidos

Características Principales

Arquitectura del Sistema

Requisitos del Sistema y Dependencias

Instalación y Uso

Estructura del Proyecto

Parámetros de Simulación

Contribución

Licencia

🚀 Características Principales

Movilidad Multimodal: Modela agentes con comportamientos diferenciados (peatones y vehículos), cada uno con sus propias restricciones de velocidad, radios de percepción y reglas de movimiento.

Enrutamiento Inteligente (A*): Los agentes calculan el camino más eficiente a través de la red de calles/aceras utilizando heurísticas de distancia euclidiana/Manhattan, adaptándose a la topología de la malla urbana.

Dinámica Emergente: Permite observar fenómenos de congestión vehicular, embotellamientos en intersecciones y patrones de densidad peatonal a partir de reglas de interacción local simples.

Visualización Interactiva: Generación de gráficos dinámicos paso a paso y animaciones incrustadas compatibles con Jupyter Notebook y Google Colab.

🏗️ Arquitectura del Sistema

El proyecto se estructura bajo el paradigma de programación orientada a objetos y sistemas complejos:

El Entorno (Grid / Network): Representa el espacio geográfico o la red de nodos y aristas por donde transitan los agentes.

Los Agentes (Agent):

Vehículos: Se desplazan por la red vial respetando la infraestructura de transporte y la presencia de otros vehículos.

Peatones: Se desplazan con mayor flexibilidad espacial, priorizando aceras o zonas peatonales.

El Planificador de Rutas: Implementación optimizada del algoritmo A* sobre un grafo de conectividad que actualiza dinámicamente los destinos.

📦 Requisitos del Sistema y Dependencias

El proyecto está desarrollado en Python y requiere las siguientes librerías principales:

agentpy (Simulación de sistemas multi-agente)

networkx (Manejo de grafos y redes viales)

numpy (Operaciones numéricas y matrices)

matplotlib / seaborn (Visualización de datos y gráficos dinámicos)

pandas (Estructuras y análisis de datos de simulación)

💻 Instalación y Uso

Puedes ejecutar este proyecto de dos formas: directamente en la nube mediante Google Colab o de forma local en tu máquina.

Opción A: Google Colab (Recomendado para pruebas rápidas)

Haz clic en el botón superior para abrir el notebook directamente en Colab y ejecutar las celdas de simulación paso a paso sin instalar nada localmente.

Opción B: Instalación Local

Sigue estos pasos en tu terminal para clonar y ejecutar el repositorio:

# 1. Clona el repositorio
git clone https://github.com/tu_usuario/nombre-del-repositorio.git
cd nombre-del-repositorio

# 2. Crea un entorno virtual (opcional pero recomendado)
python -m venv venv
source venv/bin/activate  # En Windows usa: venv\Scripts\activate

# 3. Instala las dependencias necesarias
pip install agentpy networkx numpy matplotlib pandas

# 4. Ejecuta el entorno de Jupyter o abre el archivo .ipynb
jupyter notebook


🗂️ Estructura del Proyecto

├── simulacion_urbana_con_agentes_inteligentes__con_algoritmo_A_.ipynb  # Notebook principal de Colab
├── README.md                                                          # Documentación detallada del proyecto
└── requirements.txt                                                   # Lista de dependencias del proyecto


⚙️ Parámetros de Simulación

Dentro del código del notebook, puedes modificar los parámetros iniciales para experimentar con diferentes escenarios urbanos:

Parámetro

Descripción

Valor por Defecto / Rango

steps

Número de iteraciones/pasos temporales de la simulación

100 - 500

density_vehicles

Número inicial o tasa de generación de vehículos

Variable

density_pedestrians

Número inicial o tasa de generación de peatones

Variable

grid_size

Dimensiones de la malla urbana (ancho x alto)

Ej. (50, 50)

🤝 Contribución

¡Las contribuciones son bienvenidas! Si deseas proponer mejoras, optimizar el algoritmo A*, añadir nuevos tipos de agentes o mejorar la visualización:

Haz un Fork del repositorio.

Crea una rama para tu nueva característica (git checkout -b feature/NuevaCaracteristica).

Realiza el Commit de tus cambios (git commit -m 'Añadida nueva característica X').

Sube la rama (git push origin feature/NuevaCaracteristica).

Abre un Pull Request.

📄 Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.
