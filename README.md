# latam_challenge
El el presente repositorio se encuentra el challenge_latam con el cuál se está postulando al cargo de Data Scientist.

En primer lugar, se crea un documento PPT en el que se presentan todos los pasos, resultados y conclusiones del trabajo realizado. Sin embargo, se puede encontrar la misma información en el notebook _solution.ipynb_

Para poder ejecutar el notebook _solution.ipynb_ se debe crear un nuevo entorno virtual e instalar los paquetes necesarios. Este entorno se puede crear a través de Anaconda o de Python en una terminal.

- Anaconda environment: ```conda create --name env_name```
- Python environment: ```python3 -m venv env_name```

Una vez creado el entorno virtual procedemos a activarlo:
- Anaconda environment: ```conda activate env_name```
- Python environment: ```source env_name/bin/activate```

Finalmente instalamos los paquetes en el archivo requirements.txt: ```pip install -r requirements.txt```

En caso de que el entorno virtual de anaconda no venga con pip instalado se puede instalar con el siguiente comando:```conda install pip```. Luego, se puede ejecutar el comando anterior.

Con los requerimientos de paquetes ya instalados se puede proceder a correr el notebook _solutions.ipynb_

Cabe destacar que si bien el notebook está diseñado para poder ser ejecutado de inicio a fin sin problemas, se aconseja inicializar los modelos con los hiperparámetros ya encontrados, debido a que la optimización de hiperparámetros para los 3 modelos (SVM no optimiza hiperparámetros) toma un par de horas.

Los hiperparámetros son los siguientes:
#### Naive Bayes:
```python
{
    'var_smoothing': 0.1
}
```

#### Random Forest:
```python
{
    'n_estimators': 600,
    'min_samples_split': 5,
    'min_samples_leaf': 1,
    'max_features': 'log2',
    'max_depth': 90,
    'bootstrap': False
}
```

#### XGBoost:
```python
{
    'subsample': 0.7142857142857143,
    'reg_alpha': 2.113157894736842,
    'min_child_weight': 3,
    'max_depth': 6,
    'learning_rate': 0.3,
    'gamma': 1,
    'colsample_bytree': 0.8571428571428571,
    'colsample_bylevel': 0.5714285714285714
}
```