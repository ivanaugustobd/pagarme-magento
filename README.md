# Módulo de integração Pagar.me para Magento 1.x
[![Build Status](https://travis-ci.org/pagarme/pagarme-magento.svg?branch=v2)](https://travis-ci.org/pagarme/pagarme-magento)
[![Coverage Status](https://coveralls.io/repos/github/pagarme/pagarme-magento/badge.svg?branch=v2)](https://coveralls.io/github/pagarme/pagarme-magento?branch=master)

## Requisitos

- [Magento Community](https://magento.com/products/community-edition) 1.5.x, 1.6.x, 1.7.x, 1.8.x ou 1.9.x.
- [PHP](http://php.net) >= 5.4.x

## Instalação

1. Baixe a última versão do nosso módulo clicando [aqui](https://github.com/pagarme/pagarme-magento/archive/v2.zip)
2. Descopacte o arquivo **zip** e copie as pastas `app`, `js` e `skin` para a a pasta raiz da sua instalação do Magento
3. Limpe o cache em `Sistema > Gerenciamento de Cache`

## Configuração

1. Acesse o painel administrativo da sua loja
2. Vá em `Sistema > Configuração > Métodos de Pagamento > Pagar.me`
3. Informe sua **Chave de API** e sua **Chave de criptografia**
4. Salve as configurações

## Como testar o módulo

### Requisitos

- [Docker Compose](https://docs.docker.com/compose/)


### Executando os testes

1. Execute o comando `docker-compose up -d` para iniciar os containers
2. Execute o comando `docker-compose exec magento install` para executar a instalação do Magento. Caso queira alguma configuração específica, verifique o arquivo `.env`.
3. Execute o comando `docker-compose exec magento install-modules` para instalar o módulo **Pagar.me para Magento 1.x**
4. Execute o comando `docker-compose exec magento php vendor/bin/phpunit` para iniciar os testes
