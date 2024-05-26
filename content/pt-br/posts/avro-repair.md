---
title: "Reparador de Avro"
date: 2024-05-26
description: "Aplicativo NodeJs para conectar e baixar avro do bucket S3, testar e reparar"
tags: [ "nodejs", "aws", "S3", "avro" ]
category: "tools"
permalink: "avro-repair"
published: true
---

# S3 Avro Repair

[Aplicação NodeJs](https://github.com/pauloeli/s3-avro-repair) para conectar e baixar arquivos Avro de um bucket S3,
testar e reparar. Você pode configurar para fazer o upload do arquivo recuperado, se desejar. Esta aplicação foi criada
para
resolver um problema específico, portanto, melhorias podem ser feitas.

Desejo que este projeto possa ser usado como ponto de partida para outras necessidades. De forma alguma posso ser
responsabilizado por qualquer perda de dados ou problemas que a aplicação possa causar **(use por sua própria conta e
risco)**.

### Ferramentas Avro

Documentação sobre a ferramenta e detalhes podem ser
vistos [aqui](https://www.michael-noll.com/blog/2013/03/17/reading-and-writing-avro-files-from-the-command-line/).

Mais sobre o comando `cat` pode ser lido
nesta [documentação](https://www.mail-archive.com/dev@avro.apache.org/msg07299.html).

### Configurações

É necessário definir o caminho do Java que será usado para executar as Ferramentas Avro. Para configurar, edite
o [application.yml](resources/application.yml). 

Se você não souber onde está o Java, pode usar o comando `whereis` no Linux para mostrar.

### Instalação

```bash
npm install --no-optional 
```

### Parâmetros

Os parâmetros devem ser configurados via variáveis de processo para NodeJS. Aqui estão as configurações disponíveis:

| Variável              | Descrição                                                                                                                                                           |
|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AWS_ACCESS_KEY_ID     | Especifica uma chave de acesso AWS associada a um usuário ou função IAM.                                                                                            |
| AWS_REGION            | Especifica a Região AWS para enviar a solicitação.                                                                                                                  |
| AWS_SECRET_ACCESS_KEY | Especifica a chave secreta associada à chave de acesso. Esta é essencialmente a "senha" para a chave de acesso.                                                     |
| AWS_SESSION_TOKEN     | Especifica o valor do token de sessão que é necessário se você estiver usando credenciais de segurança temporárias que obteve diretamente das operações do AWS STS. |
| DEBUG_LEVEL           | Especifica o nível de registro de logs da aplicação.                                                                                                                |

### Execução

```bash
DEBUG_LEVEL="debug" AWS_ACCESS_KEY_ID="" AWS_REGION="" AWS_SECRET_ACCESS_KEY="" AWS_SESSION_TOKEN="" node --require ts-node/register src/app.ts
```

### Projetos relacionados

- [Avro Tools AWS](https://github.com/Segence/avro-tools-aws)
