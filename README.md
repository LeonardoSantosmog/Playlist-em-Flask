# Flask Projects

Este repositório contém dois exemplos básicos de aplicações **Flask** em Python.

---

## 1️⃣ Hello Flask

Um exemplo simples de servidor Flask que responde "Ola, Flask!" na rota raiz (`/`).

### Código
```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
    return "Ola, Flask!"

if __name__ == '__main__':
    app.run(debug=True)

```
## Segundo codigo
```python
from flask import Flask, jsonify, request

app = Flask(__name__)

playlists = [
    {
        "id": 1,
        "name": "o lado bom de ser gay",
        "artista": "Pabllo Vittar",
    },
    {
        "id": 2,
        "name": "E o amor",
        "artista": "Zeze de camargo e Luciano",
    },
    {
        "id": 3,
        "name": "Acorda Pedrinho",
        "artista": "Luan Santana",
    }
]

@app.route('/playlists', methods=['GET'])
def get_playlists():
    return jsonify({'playlists': playlists, "total": len(playlists)})

if __name__ == '__main__':
    app.run(debug=True)
