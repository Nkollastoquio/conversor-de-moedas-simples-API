## Conversor de Moedas
Este é um projeto simples de conversão de moedas utilizando JavaScript e uma API de taxas de câmbio. O aplicativo permite que o usuário insira um valor em uma moeda de origem e converta esse valor para uma moeda de destino, utilizando as taxas de câmbio mais recentes.

## visão Geral
O Conversor de Moedas consulta a API pública exchangerate-api.com para obter as taxas de câmbio em tempo real. O usuário pode inserir um valor e escolher entre várias moedas para realizar a conversão.



## Funcionalidades principais:
Conversão de valores entre USD, EUR, e BRL.
Exibição do valor convertido com base nas taxas de câmbio mais recentes.
Formulário para entrada do valor e escolha das moedas.
Interface simples e intuitiva.




## Tecnologias Utilizadas
HTML5: Estrutura básica da página.
CSS3: Estilo e layout.
JavaScript (ES6): Lógica de conversão e interação com a API.
API exchangerate-api.com: Fornece as taxas de câmbio em tempo real.



*  Explicação Geral:
Este código permite que o usuário converta valores de uma moeda para outra (por exemplo, de reais para dólares) utilizando a API exchangerate-api.com. Ele captura o valor inserido pelo usuário, busca a taxa de câmbio entre as moedas selecionadas, e exibe o resultado da conversão.

## Como Funciona:

1. Configuração Inicial:
* apiKey e apiURL: O código começa definindo a chave da API (apiKey) e a URL base (apiURL) para buscar as taxas de câmbio da API exchangerate-api.com. A chave da API é uma credencial necessária para autenticar a solicitação da API.

2. Função getExchangeRate:
Esta função assíncrona faz a busca pela taxa de câmbio entre duas moedas.

* Parâmetros:
* deMoeda: a moeda de origem (de qual moeda estamos convertendo).
* paraMoeda: a moeda de destino (para qual moeda estamos convertendo).
* O que acontece na função:
* A função faz uma requisição HTTP à API utilizando a URL apiURL, que inclui o valor da moeda de origem.
* Se a resposta for bem-sucedida (data.result === 'success'), ele retorna a taxa de câmbio da moeda de origem para a moeda de destino (acessando data.conversion_rates[paraMoeda]).

* Caso contrário, um erro é lançado.

Como Usar:
## 1 O usuário insere o valor a ser convertido no campo de texto.
## 2 O usuário seleciona a moeda de origem e a moeda de destino.
## 3 O usuário clica no botão de envio do formulário.
## 4 O código faz a requisição à API e retorna o valor convertido.