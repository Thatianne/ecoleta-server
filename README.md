# API Ecoleta
API para site e app Ecoleta criados durante a Next Level Week

## Rodando o projeto
Instruções de como obter e rodar o projeto

### Pré-requisitos
É necessário ter o `node` instalado. Pode-se usar o `npm` ou o `yarn` para instalar os pacotes.

### Instalando
Clone o repositório com 
```
git clone https://github.com/Thatianne/ecoleta-server.git
```
ou fazendo o download do ZIP do repositório.

Entre no diretório do projeto e rode
```
yarn
```
ou
```
npm install
```
Tendo finalizado a instalação dos pacotes rode o projeto com
```
yarn dev
```
ou
```
npm run dev
```
## Endpoints:
 - [GET] `/items`:
 
 É retornado um `array` de `items` que podem ser recolhidos nos pontos de coleta.
 
 ```javascript
   [
    {
     id: {id},
				 title: {title},
				 image_url: {url}
    },
    {
     id: {id},
				 title: {title},
				 image_url: {url}
    }
   ]
```
 
 - [GET] `/points`:
 
 Retorna um `array`de `points`(pontos de coleta) e aceita as `queries`: `city`, `uf` e `item` (ids separados por vírgula).
 
  ```javascript
   [
    {
     "id": 4,
     "image": {url},
     "name": "Mercado Seu Zé",
     "email": "contato@imp.com.br",
     "whatsapp": "12345678",
     "city": "Feira de Santana",
     "uf": "BA",
     "latitude": -32.1234343,
     "longitude": -12.1234343
    },
    {
     "id": 5,
     "image": {url},
     "name": "Mercado Seu Zé",
     "email": "contato@imp.com.br",
     "whatsapp": "12345678",
     "city": "Feira de Santana",
     "uf": "BA",
     "latitude": -32.1234343,
     "longitude": -12.1234343
    }
   ]
```

 - [POST] `/points`:
 
 Cria um ponto de coleta. Aceita no `body` o `payload` abaixo.
 
 ```javascript
 {
  "name": {namePoint},
  "email": {emailPoint},
  "whatsapp": {whatsapp},
  "latitude": {latitude},
  "longitude": {longitude},
  "city": {city},
  "uf": {uf},
  "items": [{idItem1}, {idItem2}]
 }
 
 - [GET] `/points/{id}`:
 
 Retorna um ponto de coleta.
 
 ```javascript
   [
    {
     "id": 4,
     "image": {url},
     "name": "Mercado Seu Zé",
     "email": "contato@imp.com.br",
     "whatsapp": "12345678",
     "city": "Feira de Santana",
     "uf": "BA",
     "latitude": -32.1234343,
     "longitude": -12.1234343
    },
 ```
 
