<!--
title: 'Serverless Framework Python Flask API backed by DynamoDB on AWS'
description: 'This template demonstrates how to develop and deploy a simple Python Flask API service backed by DynamoDB running on AWS Lambda using the traditional Serverless Framework.'
layout: Doc
framework: v3
platform: AWS
language: Python
priority: 2
authorLink: 'https://github.com/serverless'
authorName: 'Serverless, inc.'
authorAvatar: 'https://avatars1.githubusercontent.com/u/13742415?s=200&v=4'
-->

# Test AWS Amazon

Progetto base che consiste in 2 endpoint REST per la creazione e la lettura di utenti memorizzati su DynamoDB. Il progetto è stato costruito customizzando uno dei template offerti dal framework `serverless`. 




## Struttura del template

Gli endpoint REST sono stati sviluppati con linguaggio python, avvalendomi della libreria Flask. Attualmente gli endpoint disponibili sono i seguenti: 

`/getUserById/<string:user_id>`
Chiamata di tipo di GET che restituisce, se esiste, l'utente con un dato id. 

`/createUser` 
Crea un utente accettando come Body della POST un json così strutturato: 

```json
{
    "userId":3,
    "username":"giulio",
    "password":"pwd"
}
```

## Servizi AWS Utilizzati per il test
Per il test sono utilizzati i seguenti servizi
* [API Gateway](https://aws.amazon.com/it/api-gateway/) per fornire l'accesso alle REST
* [AWS Lambda](https://aws.amazon.com/it/lambda/) per la definizione delle funzioni
* [DynamoDB](https://aws.amazon.com/it/dynamodb/) per memorizzare e leggere le informazioni tramite DB NoSQL