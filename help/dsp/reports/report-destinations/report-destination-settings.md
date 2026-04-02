---
title: Configurações de destino do relatório
description: Veja os detalhes necessários para os destinos do seu relatório, por tipo de destino.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# Configurações de destino do relatório

Os detalhes necessários para destinos que não são de relatório de email variam de acordo com o tipo de destino.

>[!NOTE]
>
> Você também pode enviar seus relatórios personalizados para destinatários de email, que não exigem um destino de relatório salvo. Você pode especificar destinatários de email nas configurações do relatório, em vez de destinos salvos.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Um nome para ajudá-lo a identificar o destino.

**[!UICONTROL S3 Bucket URL]:** O caminho completo para a pasta no bucket [!DNL Amazon Simple Storage Service] (S3) para o qual o relatório é carregado. Exemplo: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** A ID da Chave de Acesso para o bucket ([!DNL Amazon S3]) (fornecida por [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** A Chave de Acesso Secreta para o bucket ([!DNL Amazon S3]) (fornecida por [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Um nome para ajudá-lo a identificar o destino.

**[!UICONTROL Server]:** O nome de host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usada no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para entrar no servidor.

**[!UICONTROL Password]:** A senha para entrar no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos são carregados.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Um nome para ajudá-lo a identificar o destino.

**[!UICONTROL Server]:** O nome de host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usada no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para entrar no servidor.

**[!UICONTROL Password]:** A senha para entrar no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos são carregados.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Um nome para ajudá-lo a identificar o destino.

**[!UICONTROL Server]:** O nome de host do servidor.

**[!UICONTROL Port]:** O número da porta a ser usada no servidor. O padrão é *[!UICONTROL 21]*.

**[!UICONTROL Username]:** O nome de usuário para entrar no servidor.

**[!UICONTROL Password]:** A senha para entrar no servidor.

**[!UICONTROL Path (Optional)]:** O caminho do servidor para o qual os arquivos são carregados.

>[!MORELIKETHIS]
>
>* [Sobre destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Criar um destino de relatório](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Editar um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Excluir um destino de relatório](/help/dsp/reports/report-destinations/report-destination-delete.md)
