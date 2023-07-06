# API REST

## API --> Application Programming Interface

É um conjunto de definições e protocolos usados no **desenvolvimento** e na **integração** de aplicações.  
Basicamente uma **API** é um **contrato** de como os dados serão enviados e quais respostas vamos obter quando um dado específico for solicitado.  


## REST --> REpresentational State Transfer

É um conjunto de *regras* e *limitações* para que a **API** não seja complexa demais.  
Basicamente o que pedimos a uma **API** é o seu **estado** e ela nos retorna uma **representação** dele em uma **transferência** de dados.  

## Ferramentas em Python

- Django;
- Flask;
- FastAPI;
- Vibora;
- Falcon;
- CherryPy;
- AIOHTTP;
- Tornado.

## Como dizer o que eu quero?

### GET

```python
from flask import Flask


app = Flask(__name__)

@app.get('/recurso')
def respondo_estado():
    return OK

if __name__ == '__main__':
    app.run()

```

- Utilizamos **json** para a representação dos dados. É possível utilizar **YAML** e **XML**.

- Filtros podem ser a solução para problemas de performance.
- Em momentos em que precisamos de muitos dados de vários **endpoints** que o **REST** levaria varios requests para resolver podemos usar **GraphQL**;
- Para dados que precisam mudar muitas vezes em curtos períodos de tempo (e em tempo real) podemos utilizar **websockets** para resolver (ferramentas de **chat**).
- Quando precisamos de uma comunicação intensa entre microsserviços, nem utilizamos **HTTP**, utilizamos **RPC** ou **GRPC**. **Nameko** é um **framework** focado em **RPC**.
