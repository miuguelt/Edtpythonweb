Despliegue de aplicación

* Crear carpeta contenedora del proyecto
* crear ambiente virtual con python
    * (con conda)   conda create --name flask_deploy
    * (con python) python -m venv flask_env

* activar el ambiente
    * con conda conda activate flask_env
    * con python en bash: source flask_env/Scripts/activate


* touch Procfile -> ( web: gunicorn indexi:app)
* touch runtime.txt -> (python-3.8)
* crear carpeta app
* dentro de carpeta app crear main.py


```python
from flask import Flask 
  
app = Flask(__name__) 
  
@app.route("/") 
def index(): 
    return "<h1>Hola Mundo!</h1>"
```

* de nuevo en el directorio del proyecto  
* touch index.py

```python
from app.main import app 
  
if __name__ == "__main__": 
        app.run() 
```

* pip install flask gunicorn
* pip freeze > requirements.txt

* git init
* git add .
* git commit -m "primer commit"
