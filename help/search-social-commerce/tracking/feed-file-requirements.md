---
title: Requisitos de arquivo para arquivos de feed de conversão
description: Consulte os requisitos para arquivos de feed de conversão.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Requisitos de arquivo para arquivos de feed de conversão

A seguir estão os requisitos para o formato de arquivo, campos de dados obrigatórios e opcionais, nome do arquivo e protocolo de transferência de arquivos para arquivos de feed.

## Formato de arquivo

O arquivo de dados deve estar no formato de texto simples (TXT), valores separados por vírgula (CSV) ou valores separados por tabulação (TSV). O arquivo pode consistir em uma linha de cabeçalho e linhas de dados com valores separados por guias, vírgulas ou outro caractere (mas não espaços):

* **Linha de cabeçalho:** (Opcional) A primeira linha do arquivo é um cabeçalho, que especifica os nomes de campo necessários (ou nomes de coluna) em uma ordem específica, separados por guias ou vírgulas. Os nomes de coluna necessários incluem as métricas de conversão que o Adobe Advertising está rastreando como conversões.

* **Linhas de dados:** Cada linha subsequente inclui campos de dados na mesma ordem do cabeçalho e separados por guias ou vírgulas. Se o primeiro registro não for um cabeçalho, cada linha de dados deverá incluir todos os campos possíveis, em uma ordem especificada. Os valores de todas as IDs e métricas de conversão devem ser alfanuméricos.

  Quando vários cliques em um ou vários anúncios levam a uma transação, é necessário determinar a ID do clique e a ID de rastreamento à qual atribuir a transação. Como um identificador exclusivo é relatado para cada transação, você pode atualizar transações individuais.

## Convenção de nomenclatura de arquivo

O nome do arquivo deve incluir a data e ser consistente. Por exemplo, se você usar o formato AAAAMMDD.txt, um arquivo enviado em 15 de maio de 2011 deverá se chamar 20110515.txt.

## Protocolo de transferência de arquivos

Envie o arquivo por meio do protocolo de transferência SFTP, usando a Porta 22. Você precisará fornecer suas informações de chave pública.  Sua equipe de conta do Adobe ou a equipe de implementação fornecem o local do servidor, juntamente com as credenciais necessárias para que o sistema transfira os arquivos.

>[!TIP]
>
>Os feeds de dados de conversão são processados várias vezes por dia. Carregue o feed diário o mais rápido possível depois da meia-noite hora local, para que o Adobe Advertising possa processar seus dados e disponibilizá-los na interface do usuário de relatórios no início da manhã.

>[!MORELIKETHIS]
>
>* [Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
