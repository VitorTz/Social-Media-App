# Hello, World!

>  app = FastAPI()

>  uvicorn main:app --reload

- main: arquivo main.py (modulo Python).
- app: o objeto criado dentro de main.py -> app = FastAPI().
- --reload: Faz o servidor reiniciar após as alterações do no código. Apenas para fins de desenvolvimento.

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello, World!"}
```

> async serve para calls a base de dados ou a outras apis,
> é necessário quando a função depende de um input externo.

Aqui está sendo definido o que é chamado de Path operator ou route. Digamos que a url base de nosso dominio seja dominio.org. O path operator "/" irá retorna um json para o usuário quando um método HTTP get for requisitado junto da url dominio.org/. Se mudarnos o Path operator para /imagens estamos mudando a url para dominio.org/imagens.
