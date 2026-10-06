# deep-learning
Proyecto para explorar e implementar conceptos tale cómo: como redes neuronales artificiales, redes neuronales convolucionales, redes neuronales recurrentes, Transformers para lenguaje y para visión,

## Entorno Python compartido

Todos los notebooks del proyecto pueden usar el entorno virtual `.env`, ubicado
en la raíz de `deep-learning`. Esta carpeta contiene el intérprete de Python y
las dependencias; se excluye de Git. Las dependencias se definen en
`requirements.txt`.

Para crear el entorno en macOS o Linux, ejecuta desde la raíz del proyecto:

```bash
python3 -m venv .env
.env/bin/python -m pip install -r requirements.txt
.env/bin/python -m ipykernel install --prefix .env --name deep-learning --display-name "deep-learning (.env)"
```

### Seleccionar el entorno en VS Code

1. Abre la carpeta `deep-learning` completa en VS Code e instala las extensiones
   recomendadas de Python y Jupyter.
2. Ejecuta **Python: Select Interpreter** desde la paleta de comandos y selecciona
   `.env/bin/python`. Si no aparece, usa **Enter interpreter path** para buscarlo.
3. Abre cualquier notebook y pulsa **Select Kernel** en la esquina superior derecha.
   En **Select Another Kernel → Python Environments**, selecciona el intérprete
   de `.env`. Si aparece **deep-learning (.env)** entre los kernels de Jupyter,
   también puedes seleccionarlo.
4. Ejecuta las celdas con **Run All**.

Para confirmar el intérprete utilizado en cualquier notebook:

```python
import sys
print(sys.executable)  # Debe terminar en deep-learning/.env/bin/python
```

### Usar el entorno desde la terminal

```bash
source .env/bin/activate
python -m pip install -r requirements.txt
deactivate
```

Para añadir dependencias de otros notebooks, agrégalas a `requirements.txt` y
vuelve a ejecutar `.env/bin/python -m pip install -r requirements.txt`.
Reinicia el kernel después de instalar o actualizar paquetes.

Para ejecutar el tutorial desde la raíz del proyecto y guardar el resultado en
`/tmp`, sin sustituir el notebook original:

```bash
.env/bin/python -m nbconvert --to notebook --execute 1-Pytorch/TutorialPytorch.ipynb --ExecutePreprocessor.kernel_name=deep-learning --ExecutePreprocessor.timeout=300 --output TutorialPytorch-ejecutado --output-dir /tmp
```
