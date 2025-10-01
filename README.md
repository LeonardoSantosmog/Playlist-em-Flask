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
