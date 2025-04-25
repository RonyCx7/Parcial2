# Parcial2 

##Estructura del proyecto 

```text
📦 Parcial2/
├── 📂 datos/
│   ├── 📄 productos.csv                 # Dataset
│   └── 📄 datos_ejemplo.json            # Opcional: versión JSON del dataset
├── 📂 docs/
│   ├── 📄 informe.pdf                   # Documento formal del proyecto
│   └── 📄 screenshots/                  # Capturas de Neo4j Browser
├── 📂 notebooks/
│   ├── 📄 1_exploracion_datos.ipynb     # Análisis inicial
│   └── 📄 2_pruebas_algoritmos.ipynb    # Experimentos con algoritmos
├── 📂 src/
│   ├── 📄 config/
│   │   └── 📄 neo4j_config.py           # Configuración de conexión
│   ├── 📄 models/
│   │   └── 📄 grafo_model.py            # Modelado de nodos/relaciones
│   ├── 📄 services/
│   │   ├── 📄 grafo_service.py          # Funciones de creación del grafo
│   │   └── 📄 recomendacion_service.py  # Lógica de recomendación
│   └── 📄 main.py                       # Punto de entrada
├── 📄 .gitignore                        # Archivos a ignorar en Git
├── 📄 requirements.txt                  # Dependencias
└── 📄 README.md                         # Guía básica del proyecto
```

##Diseño del Grafo
```text
(Usuario)-[COMPRADO_POR]->(Producto)-[PERTENECE_A]->(Categoría)
(Producto)-[SIMILAR_A {peso: float}]->(Producto)
```

## Requisitos
- Neo4j Desktop 4.4+
- Python 3.8+
- Bibliotecas: `py2neo pandas python-dotenv`

## Configuración
1. Renombrar `.env.example` a `.env` y configurar credenciales
2. Ejecutar `pip install -r requirements.txt`
3. Iniciar Neo4j Desktop y crear base de datos

## Ejecución
```bash
python src/main.py
