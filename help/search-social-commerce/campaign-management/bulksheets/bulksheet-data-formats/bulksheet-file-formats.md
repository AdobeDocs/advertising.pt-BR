---
title: Formatos de arquivo de bulksheet compatíveis
description: Consulte os requisitos gerais de arquivo para bulksheets.
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Formatos de arquivo de bulksheet compatíveis

## Formatos de arquivo

Você pode baixar, fazer upload e publicar arquivos de bulksheet para redes de anúncios compatíveis em qualquer um dos seguintes formatos:

* CSV (valores separados por vírgula)
* TSV (valores separados por tabulação)
* TXT (texto Unicode), delimitado por vírgulas ou tabulações
* ZIP (compactado) contendo um arquivo no formato CSV, TSV ou TXT delimitado por vírgulas ou tabulações

Ao criar/baixar uma bulksheet, ela é criada no formato de arquivo especificado com todos os dados relevantes incluídos no arquivo. Use as informações a seguir para editar dados no arquivo ou criar seu próprio bulksheet manualmente.

## Conteúdo básico de uma bulksheet

O primeiro registro (linha) de um arquivo de bulksheet contém um conjunto de nomes de coluna específicos, coletivamente conhecidos como <i>cabeçalho</i>. Os nomes das colunas no cabeçalho estão em uma ordem especificada e correspondem a cada um dos campos nos registros de dados subsequentes. Os nomes de coluna necessários no cabeçalho variam de acordo com a rede de anúncios.

Cada registro subsequente (linha) contém dados, com campos contendo valores (ou nenhum valor) para cada coluna no cabeçalho.

## Tamanho máximo do arquivo

Os arquivos de bulksheet podem ter até 2,5 GB, o que corresponde a cerca de 2,5 milhões de linhas.

>[!NOTE]
>
>Quando você gera um bulksheet para várias campanhas e os dados combinados consistem em mais de 500.000 linhas, os dados são divididos por campanha em dois ou mais arquivos, chamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` e assim por diante.

## Requisitos de formatação para diferentes tipos de arquivos

Os campos de dados delimitados por guias e por vírgulas exigem formatação diferente.

### Arquivos TSV e arquivos TXT delimitados com guias

Os campos de dados em arquivos TSV e arquivos TXT delimitados com guias devem ser formatados da seguinte maneira:

* Os campos em cada registro são separados por caracteres de tabulação. Para omitir um valor para um campo, use somente o caractere de tabulação.

  Exemplo: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Os campos não podem conter caracteres de tabulação inseridos.

### Arquivos CSV e TXT delimitados por vírgulas

Os campos de dados em arquivos CSV e TXT delimitados com vírgulas devem ser formatados da seguinte maneira:

* Os campos em um registro são separados por vírgulas. Para omitir um valor para um campo, use apenas a vírgula.

  Exemplo: `Cruises,5000,Caribbean,,,`

* Qualquer campo pode, opcionalmente, estar entre aspas duplas (`""`).

  Exemplo: `"Cruises","5000","Caribbean",`

* Os campos com vírgulas inseridas devem estar entre aspas duplas (`""`).

  Exemplo: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Os campos com aspas duplas incorporadas devem estar entre aspas duplas (`""`).

  Exemplo: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Os campos com espaços à esquerda ou à direita devem estar entre aspas duplas (`""`).

  Exemplo: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](../bulksheet-about.md)
>* [Operações que você pode executar em bulksheets](bulksheet-operations.md)
>* [Apêndice - Erros de bulksheet](../bulksheet-errors.md)
>* [Baixar/Criar um arquivo de bulksheet](../bulksheet-download.md)
