---
title: Metadados C2PA no Creative Studio
description: Saiba como os metadados do C2PA são anexados automaticamente ao conteúdo gerado ou editado com IA gerativa no Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# Metadados C2PA em [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] anexa automaticamente metadados C2PA a conteúdo que é gerado ou editado com IA gerativa, de modo que a origem do conteúdo do seu anúncio seja registrada como metadados invisíveis e duráveis. Os metadados seguem o padrão da [Coalition for Content Provenance and Authenticity](https://c2pa.org/) (C2PA).

## Tipos de conteúdo e seu escopo {#cc-content-types}

| Tipo de conteúdo | Suportado? | Serviço de IA que gera o conteúdo | Modelo que gera a credencial |
| --- | --- | --- | --- |
| Imagens | Sim. Os metadados do C2PA são anexados quando as imagens são geradas ou editadas com IA gerativa e preservados por meio de operações de recorte e redimensionamento executadas pelo Assistente de IA. | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## Ações que anexam metadados C2PA

A tabela a seguir resume quando os metadados C2PA são anexados, com base na ação de imagem executada no Assistente de IA do [!UICONTROL Creative Studio].

| Ação | Descrição | Metadados C2PA anexados? | Exemplo de caso de uso |
| --- | --- | --- | --- |
| **Gerar uma imagem** | Criar uma nova imagem usando um prompt de texto | Sempre, porque a imagem é gerada pela IA gerativa. | Use um prompt de texto para gerar uma nova imagem de fundo ou logotipo para um modelo de anúncio.<br><br>Use um prompt de texto para substituir a imagem padrão em um conceito de anúncio por um ativo carregado da biblioteca.<br><br>Use um prompt de texto para gerar variações de uma imagem de fundo em um modelo de anúncio. |

## O que acontece quando o conteúdo se move? {#cc-content-moves}

A cadeia de proveniência completa é preservada quando um usuário baixa um arquivo de imagem ou é enviada para ser veiculada em um anúncio.

## O que os metadados C2PA incluem?

Para cada geração ou alteração de GenAI, os itens a seguir são incluídos nos metadados C2PA. Se um ativo for alterado várias vezes, cada operação será exibida nos metadados C2PA.

* Informações de nome e versão do sistema de IA usado ([!DNL Adobe Firefly C2PA])
* Modelo de IA usado ([!DNL Gemini Flash])
* Uso: se foi gerado ou editado usando GenAI
* Hora e data da criação e/ou modificação do conteúdo com ferramentas de IA geradoras
* Identificador exclusivo (que pode ser usado para distinguir cada uso da IA gerativa)

## Como posso visualizar metadados C2PA de uma imagem?

Para ver o histórico completo de ativos de uma imagem,

* Abra o arquivo de imagem em uma ferramenta de inspeção de autenticidade de conteúdo, como https://contentauthenticity.adobe.com/inspect ou https://verify.contentauthenticity.org/.

* Visualize os metadados da imagem.

* Visualize o código de imagem usando a ferramenta de inspeção de código do seu navegador (geralmente chamada de [!DNL Inspect]).

![Exemplo de metadados C2PA para uma imagem](/help/creative/assets/cs-content-credentials-example.png "Metadados C2PA para uma imagem")

## Recursos adicionais

* [[!DNL Adobe] diretrizes de usuário da IA gerativa](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [Sobre o Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
