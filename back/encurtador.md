# Encurtador de URL

Seu serviço irá receber inicialmente como parâmetro uma URL que deverá ser encurtada seguindo as seguintes regras:

1. Mínimo de 5 e máximo de 10 caracteres.
2. Apenas letras e números. 
3. Retornar apenas a url gerada, respeitando códigos HTTP.
4. A url retornada deverá ser salva no banco de dados e possuir um prazo de validade - você poderá escolher quanto tempo.

#### Exemplo ao encurtar

Seu sistema recebe uma chamada POST para encurtar a url `jusfy.com.br`:

REQUEST
```
POST http://localhost:8080/
{
    "url": "https://www.jusfy.com.br"
}
``` 

RESPONSE
``` 
{
    "original": "https://www.jusfy.com.br",
    "short": "http://localhost:8080/abc123ab"
}
```

#### Exemplo ao redirecionar

Ao receber uma chamada GET para `http://localhost:8080/abc123ab` você irá retorna um redirecionamento para a url 
salva no banco originalmente, os critérios de aceitação são:

- caso não seja encontrada ou expirada, retornar HTTP 404
- caso seja encontrada e ainda dentro da validade, redirecionar com HTTP 302 ou 200


## O que esperamos

### Desenvolvedor Júnior

- Docker & Docker Compose 
- Framework atual
- Documentação de como subir e utilizar a aplicação


### Desenvolvedor Pleno

- Ítens acima
- Testes unitários
- Testes funcionais
- Seguir as boas práticas
- Design Pattern


### Desenvolvedor Sênior

- Ítens acima
- Github Actions, Travis-CI ou outro serviço 
- Coleção no Postman (também pode ser Swagger ou outro de sua preferência)


### Desejável para todos os níveis

### Diferenciais (para todos os níveis)

- Aplicação dos princípios SOLID
- Organização
- Arquitetura
