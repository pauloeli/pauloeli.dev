---
title: "Gerenciador de Posts Visualizados no Instagram"
date: 2023-11-09
description: "Uma ferramenta para gerenciar e destacar projetos visualizados no Instagram"
tags: [ "instagram", "extension", "chrome" ]
category: "tools"
permalink: "instagram-viewed"
published: true
---

{{< rawhtml >}}
    <img src="/images/ig-posts-view.png" alt="Instagram Viewed Posts Manager" align="left" width="232" height="249" style="margin-right: 5px">
{{< /rawhtml >}}

[Gerenciador de Posts Visualizados no Instagram](https://github.com/pauloeli/ig-viewed-posts) é uma ferramenta projetada
para ajudar os usuários a acompanhar os posts do Instagram que eles visualizaram. Esta ferramenta adiciona dinamicamente
um botão "Visualizado" a cada post no Instagram, permitindo que os usuários marquem manualmente os posts como
visualizados. Além disso, os posts visualizados são modificados visualmente para facilitar a identificação.

## Recursos

- Detecta novos posts do Instagram na página dinamicamente.
- Permite a marcação manual de posts visualizados.
- Distingue visualmente os posts visualizados dos não visualizados.

## Instalação

Para adicionar a extensão Gerenciador de Posts Visualizados no Instagram ao seu navegador Chrome, siga estas etapas
simples:

1. **Baixe o repositório:**
    - Clone o repositório usando o seguinte comando no seu terminal:
   ```bash
   git clone https://github.com/pauloeli/ig-viewed-posts.git
   ```

2. **Instale as dependências do npm:**
    - Navegue até o diretório da extensão usando o terminal:
   ```bash
   cd ig-viewed-posts
   ```
    - Instale as dependências necessárias executando o seguinte comando:
   ```bash
   npm install
   ```

3. **Carregue a extensão no Chrome:**
    - Abra o Google Chrome e vá para `chrome://extensions/`.
    - Ative a alternância "Modo de desenvolvedor" no canto superior direito da página.
    - Clique no botão "Carregar sem compactação" e selecione o diretório `dist` na pasta da extensão (criada após a
      execução de `npm run build`).

Agora, a extensão Gerenciador de Posts Visualizados no Instagram está instalada com sucesso no seu navegador Chrome!

## Uso

Depois de instalar a extensão, você pode começar a usá-la imediatamente:

- Acesse uma página do Instagram.
- O script detectará automaticamente todos os posts e adicionará o botão "Visualizado" a cada um.
- Clique no botão "Visualizado" em qualquer post para alternar seu status de visualização. O post será atualizado
  visualmente para refletir a alteração.

## Aviso para Desenvolvedores

Observe que o desenvolvedor deste script não é responsável por qualquer uso indevido desta ferramenta. Este script é
destinado apenas para uso educacional e pessoal. Ao usar este script, certifique-se de respeitar os termos de serviço do
Instagram e a privacidade de outros usuários. Use-o de forma responsável e por sua própria conta e risco.

## Licença

Este projeto está licenciado sob a [Licença MIT](https://github.com/pauloeli/ig-viewed-posts/blob/main/LICENSE).