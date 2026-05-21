# NATICUSdroid Android Permissions Dataset

Repositorio organizado para la entrega del proyecto de Modelos y Simulación de Sistemas II 

## Estructura

- `data/raw/`: CSV original del dataset.
- `data/processed/`: particiones generadas por el script de preparación.
- `src/prepare_data.py`: carga, validación y split reproducible 70/30 estratificado.
- `notebooks/01_preprocesamiento.ipynb`: preprocesamiento y generación de artefactos.
- `notebooks/02_random_forest.ipynb`: base del modelo Random Forest.

## Cómo ejecutar

1. Abrir cualquier notebook de modelo en `notebooks/`.
2. Ejecutar la primera celda de arranque para detectar la ruta del repositorio o clonar el proyecto en Colab.
3. Ejecutar la celda de preprocesado interna del notebook, que llama al script compartido en `src/prepare_data.py`.
4. Continuar con el entrenamiento y evaluación del modelo correspondiente.

## Notas

La celda de arranque detecta si el notebook corre en Colab. Si el repositorio no está disponible localmente, clona automáticamente `https://github.com/Claudia-Rocha-H/NATICUSTest.git` en `/content/NATICUSTest`.

## Reproducibilidad

- Partición: 70/30.
- Estratificación: sí.
- Semilla fija: 42.
- Variable objetivo: `Result`.
