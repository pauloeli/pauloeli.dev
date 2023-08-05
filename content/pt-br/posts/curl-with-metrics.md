---
title: "cURL com métricas"
date: 2023-06-14
description: "cURL com métricas"
tags: [ "curl", "metricas", "shell" ]
category: "programming"
permalink: "curl-metricas"
published: true
---

Para executar o comando cURL e obter métricas da requisição, basta criar um arquivo texto com o template abaixo e salvar
como “metrics.template.txt” (por exemplo).

```bash
time_namelookup: %{time_namelookup}s\n
time_connect: %{time_connect}s\n
time_appconnect: %{time_appconnect}s\n
time_pretransfer: %{time_pretransfer}s\n
time_redirect: %{time_redirect}s\n
time_starttransfer: %{time_starttransfer}s\n
time_total: %{time_total}s\n
```

E então executar o seguinte comando, substituindo pelo endereço desejado:

```bash
curl -w "@metrics.template.txt" -o /dev/null -s "http://wordpress.com/"
```

Se preferir, pode executar diretamente sem o arquivo de template, apenas adicionando o conteúdo do template no
parâmetro `-w`, conforme exemplo:

```bash
curl -w "time_namelookup: %{time_namelookup}s\n time_connect: %{time_connect}s\n time_appconnect: %{time_appconnect}s\n time_pretransfer: %{time_pretransfer}s\n time_redirect: %{time_redirect}s\n time_starttransfer: %{time_starttransfer}s\n time_total: %{time_total}s\n" -o /dev/null -s "http://wordpress.com/"
```

Você pode ler mais na [documentação do cURL](https://curl.se/docs/manpage.html).
