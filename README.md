# API-CORE

**Este repositório tem fins exclusivamente educacionais.**

O objetivo deste repositório é criar uma API no Design Center, importá-la no Anypoint Studio e testar os endpoints da API no Postman.

Para a criação da API, utilizamos o RAML (RESTful API Modeling Language), uma linguagem baseada em YAML que permite descrever os fluxos da nossa API.
Root File: No Root File, temos a descrição dos métodos presentes na nossa API:
````
/search:
  get:
    queryParameters:
       keyword:
         type: string
         minLength: 3
         maxLength: 10
    responses:
      200:
        body:
          application/json:
             example:  !include /examples/searchExample.raml
````

Nesta parte do código, temos o endpoint search, que recebe o método HTTP GET, seguido dos parâmetros de pesquisa (queryParameters), que são usados para enviar dados para o servidor. No exemplo selecionado, o parâmetro de consulta keyword é definido como uma string com um comprimento mínimo de 3 e um comprimento máximo de 10 caracteres. Se este resultado obtiver um retorno positivo, teremos um status code 200 com uma mensagem de sucesso, em RAML a especificação desta mensagem é mais ou menos da seguinte maneira:
```
#%RAML 1.0 NamedExample
  {"message": "result returned sucessfull"}
```

Em seguida, vamos para o nosso banco de dados (database), que define um tipo de dados com duas propriedades: username e password.

A propriedade username é definida como obrigatória e deve ter um comprimento mínimo de 5 e um comprimento máximo de 10 caracteres.

A propriedade password também é definida como obrigatória e deve ter um comprimento mínimo de 6 e um comprimento máximo de 10 caracteres.


## Demonstração

API NO DESIGN CENTER:
![Captura de Tela (16)](https://github.com/benetesla/api-core/assets/78994881/858df8db-83c5-4ed9-9120-ea8ac84617b3)

UTLIZAÇAO DO CONTRATO NO ANYPOINT STUDIO:
![Captura de Tela (17)](https://github.com/benetesla/api-core/assets/78994881/3ac24f17-7123-4c93-a3d3-8a514f25fe13)

REALIZAÇÂO DO TESTE NO POSTMAN:


![Captura de Tela (18)](https://github.com/benetesla/api-core/assets/78994881/3b2f7c00-775b-42d1-88a9-58e8243eebe9)

