# Grupo4---Reconocimento-de-Patrones
## Miembros
- Gomez Hormaza, Leonardo Fabio
- Lazares Salcedo, Brayam Joe
- Soto Concha, Kimberly Cristel
## Proyecto - Decodificación de Intención Motora a partir de Actividad Neuronal

Decodificación de dirección de movimiento (8 clases angulares) a partir de registros de spikes 
de corteza premotora (PMd/M1) durante la fase de planificación motora. Dataset: MC_Maze (monkey Jenkins, NWB format).

## Estructura del repositorio
El repositorio tiene 4 Avances del proyecto. Cada uno tiene un conjunto decódigos de prueba, test y/o exploración de los datos del dataset en relación al objetivo del proyecto. Cada avance contiene la siguiente información:
- **Avance 1**: 
	- **EDA**:Exploración de información del dataset (EDA) con respecto a la variedad de trials presentes en el dataset
- **Avance 2**:
	- **Exploración de Datos** :Programa de exploración de información del dataset (EDA) con respecto a la dirección cinemática de la mano del mono durante los primeros 500ms de movimiento
	- **Preprocesamiento:** Preprocesamiento de la data binaria de los disparos neuronales por unidad de tiempo. Se aplica un filtro gaussiano para expresar la actividad neuronal en Hz
- **Avance 3:**
	- **Gráficas:** Programa generador de gráficos informativos sobre las 8 clases cinemáticas
- **Avance 4:**
	- **Modelo SVM**: Entrenamiento del modelo SVM, recibe como entrada un tensor (2295,500,182) de la ventana de tiempo de actividad neuronal alrededor del momento en el que se ejecuta el movimiento
	- **Modelo_LSTM_Base**: Entrenamiento del modelo LSTM, recibe como entrada un tensor (2295,500,182) de la ventana de tiempo de actividad neuronal alrededor del momento en el que se ejecuta el movimiento
	- **Modelo_LSTM_rdcd**: Entrenamiento del modelo LSTM, recibe como entrada un tensor (1795,400,62) de la ventana de tiempo de actividad neuronal durante la fase de planificación del movimiento
- **Avance 5:** 
	- **Huggin Face**: Programa generador de la interfaz Hugging Face con el modelo LSTM cargado
	- **Pipeline_LSTM:** Pipeline completo de procesamiento, entrenamiento y evaluación del modelo LSTM  y  SVM con respecto a la actividad neuronal durante la fase de planificación del movimiento
