---
title: Acesso FTP a relatórios
description: Saiba como receber relatórios em um local FTP somente leitura.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Acesso FTP a relatórios

Opcionalmente, é possível receber relatórios em um local FTP somente leitura, do qual você pode recuperar os arquivos para processos automatizados adicionais (por exemplo, para analisar os dados com outro programa). Todos os relatórios básicos, exceto o [!UICONTROL Search Engine Account Report] e todos os relatórios avançados podem ser entregues a um local FTP como arquivos TSV compactados (o padrão) ou arquivos CSV, com uma extensão de arquivo .ZIP. Todos os cabeçalhos de arquivo TSV ou CSV estão incluídos e não podem ser suprimidos.

O acesso FTP a relatórios requer acesso a uma conta FTP especificada, e você deve configurar modelos de relatório usando uma convenção de nomenclatura específica e um agendamento.

## Configurar uma conta FTP para acessar relatórios

* Entre em contato com a equipe de conta do Adobe para configurar uma conta FTP para acesso ao relatório.

   A equipe fornecerá seu nome de usuário e senha.

## Configurar modelos de relatório para entrega por FTP

Para gerar relatórios no diretório FTP designado, crie um [modelo de relatório](templates/template-create.md) com as seguintes convenções de nomenclatura e programação.

>[!NOTE]
>
>Todos os relatórios avançados e todos os relatórios básicos, exceto [!UICONTROL Search Engine Account Report] pode ser entregue a um local FTP.

1. No modelo de relatório, inclua as seguintes informações em qualquer lugar no nome do modelo:

   * `FTP` (em letras maiúsculas).

   * (Opcional) Qualquer uma das três datas do sistema, usando a seguinte sintaxe que diferencia maiúsculas de minúsculas, incluindo colchetes:

      * `[TODAY]` — Para incluir data, hora e minuto em que o relatório foi executado. Como isso inclui a hora exata, o mesmo modelo pode ser executado várias vezes por dia sem substituir o relatório anterior.

      * `[SDATE]` — Para incluir a data inicial do intervalo de datas do relatório.

      * `[EDATE]` — Para incluir a data final do intervalo de datas do relatório.
   * (Opcional) `[CSV]` (em letras maiúsculas e entre parênteses) para criar arquivos no formato CSV em vez do formato TSV padrão.

   Exemplo: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` criaria um arquivo como 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Agendar o relatório para execução em um horário específico.

   Os relatórios são entregues à conta FTP em uma hora após serem concluídos.

>[!NOTE]
>
>* Para enviar relatórios concluídos por email, basta inserir os endereços de todos os destinatários de email ao gerar o relatório ou modelo.
>* Os relatórios são executados de acordo com os cronogramas especificados e entregues à conta FTP dentro de uma hora após a sua conclusão.


## Acessar relatórios em um repositório FTP

Para acessar seus relatórios, conecte-se a um dos hosts FTP a seguir usando o logon da sua conta FTP (`amo<userID>rpt`, como amo1234rpt) e uma senha ou uma chave de conexão privada, se configurada:

* Clientes internacionais: `ftp3.adobe.net`
* Clientes dos EUA: `ftp5.adobe.net`

>[!NOTE]
>
>O repositório de relatórios é somente leitura e é removido a cada 15 dias.


>[!MORELIKETHIS]
>
>* [Criar um modelo de relatório](/help/search-social-commerce/reports/automation/templates/template-create.md)

