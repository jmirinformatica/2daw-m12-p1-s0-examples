# 2daw-m12-projecte1

Codi d'exemple que serveix de suport per la part backend pel projecte 1 del M12 de 2n de DAW.

## Setup

### Python Virtual Environment

Crea l'entorn:

    python3 -m venv .venv

L'activa:

    source .venv/bin/activate

Instal·la el requisits:

    pip install -r requirements.txt

Per a generar el fitxer de requiriments:

    pip freeze > requirements.txt

Per desactivar l'entorn:

    deactivate

### Base de dades

La base de dades SQLite s'ha de dir `database.db`. S'ha creat amb l'script [database.sql](./database.sql).

## Run

Executa:

    flask run --debug

I obre un navegador a l'adreça: [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Debug amb Visual Code

Des de l'opció de `Run and Debug`, crea un fitxer animenat `launch.json` amb el contingut següent:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "MY APP",
            "type": "python",
            "request": "launch",
            "module": "flask",
            "env": {
                "FLASK_APP": "app.py",
                "FLASK_DEBUG": "1"
            },
            "args": [
                "run",
                "--no-debugger",
                "--no-reload"
            ],
            "jinja": true,
            "justMyCode": true
        }
    ]
}
```

## Enllaços de referència:

* Codi adaptat a partir d'aquest exemple: https://pythonbasics.org/flask-sqlite/
