# Teste RD - Postam

Para realizar os testes utilizei o Postman (https://www.postman.com/) para realizar e validar as requisições HTTP.

Para a organização e execução dos cenários de teste utilizei o newman https://github.com/postmanlabs/newman) uma ferramenta de linha de comando que executa as requisições da mesma forma que o runner do postman.

## Objetivo

Teste de API para validação do serviço ViaCEP (https://viacep.com.br/) 

![viacep_logo](https://d1muf25xaso8hp.cloudfront.net/https%3A%2F%2Fmeta.cdn.bubble.io%2Ff1633134971072x245531562496913440%2Fviacep.fw.png?w=64&h=64&auto=compress&dpr=1&fit=max)

* Testes realizados
    * Validação de status code
    * Validação de retorno positivo
    * Validação de retorno negativo
    * Validação de retorno nulo
    * Validação de Schema JSON
   


## Requesitos

Para a execurção dos testes é necessário ter instalado o Node.JS (https://nodejs.org/)

## Instalação

Para executar os testes é necessario instalar o ``newman`` com o seguinte comando:

    npm install -G newman

## Executando os testes

Para executar os testes basta executar o comando:

    newman run ./request_viaCEP.postman_collection.json -e ./Teste.postman_environment.json

## Geração de relatório

Para gerar relatório dos testes é necessario ter o lib ``newman-reporter-html`` (https://github.com/postmanlabs/newman-reporter-html) executando o seguinte comando:

    npm install -G newman-reporter-html
    
Após a instalação basta executar o comando:

    newman run ./request_viaCEP.postman_collection.json -e ./Teste.postman_environment.json -r html
