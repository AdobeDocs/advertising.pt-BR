---
title: Configurações de destino do relatório
description: Veja os detalhes necessários para os destinos do seu relatório, por tipo de destino.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '261'
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
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Criar um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Editar um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Excluir um [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
