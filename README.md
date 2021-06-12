# Testes-API-Postman

### É possível criar testes de API no Postman, executá-los via linha de comando com o _newman_ e adicioná-los ao Pipeline do Jenkins.

# Configuração do ambiente

## Instale o [Postman](https://www.postman.com/downloads/).

O Postman permite testar uma API, criar coleções, ambientes, monitores, etc.

Os testes no Postman são escritos em JavaScript.

![Postman](https://user-images.githubusercontent.com/50729163/121768828-bf1db600-cb36-11eb-8b9b-66ebbf6e2cbe.jpg)

## Instale o [Node.je](https://nodejs.org/en/download/)

## Instale o [_newman_](https://learning.postman.com/docs/running-collections/using-newman-cli/command-line-integration-with-newman/) através do npm

No terminal cmd execute _npm install -g newman_


## Export a coleção com os testes e salve no diretório de sua preferência

![Collection Export](https://user-images.githubusercontent.com/50729163/121769167-77982980-cb38-11eb-8146-7c9db2978b49.jpg)


## Execute o teste no terminal

No cmd execute: _newman run "mycollection.json"_

Caso esteja trabalhando com variáveis de ambiente é necessário também exportar o environment

![Envrionment Export](https://user-images.githubusercontent.com/50729163/121769369-a8c52980-cb39-11eb-97d1-911e44706928.jpg)

Neste caso, adicione o parâmetro -e ao comando: _newman run "mycollection.json" -e "DEV.postman_environment.json"_

O resultado da execução será exibido no terminal.

![Terminal](https://user-images.githubusercontent.com/50729163/121769455-11140b00-cb3a-11eb-8881-3555076c7a1e.jpg)

## Agora para integrar os testes ao Pipeline do Jenkins, basta seguir o [tutorial](https://learning.postman.com/docs/running-collections/using-newman-cli/integration-with-jenkins/). 

