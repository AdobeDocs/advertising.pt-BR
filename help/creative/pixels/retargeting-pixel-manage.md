---
title: Gerenciar pixels de redirecionamento
description: Saiba como criar e implementar pixels de redirecionamento para usar como destinos para experiências de anúncio.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: 1d0a1640eb2d19b8765150226e7185602bbfd495
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Gerenciar pixels de redirecionamento

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Você pode criar um pixel de redirecionamento para identificar os visitantes das páginas de aterrissagem ou de conversão de um anunciante usando cookies do usuário ou IDs universais e para capturar atributos específicos que as páginas estão rastreando para esses visitantes. O pixel rastreia o evento mais recente que o visitante executa na página. Depois de criar o pixel, você pode gerar uma marca de pixel para inserir nas páginas da Web relevantes para começar a rastrear visitantes.<!-- Note to self: surfer id=cookie or universal ID -->

Em seguida, você pode usar o pixel como destino de qualquer criativo em uma experiência de anúncio para mostrar anúncios somente a usuários com atributos especificados que visitaram anteriormente as páginas da Web associadas ao pixel. Por exemplo, você pode direcionar os visitantes que observam sapatos vermelhos no tamanho 10, se as páginas da Web rastrearem esses valores de atributo.<!-- better example? Make sure they match attribute examples below -->

Os perfis de redirecionamento são armazenados por 180 dias.

Exemplo de pixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * Atualmente, o [!DNL Creative] oferece suporte a IDs universais apenas para Advertising DSP. Uma versão futura oferecerá suporte a IDs universais para DSPs de terceiros.<!-- Clarify this and reword as needed  -->
>* Você também pode usar seus públicos-alvo primários da Adobe Audience Manager e da Adobe Analytics como [alvos criativos para suas experiências](/help/creative/experiences/experience-settings-targeting.md).
>* Ao usar uma experiência como um anúncio em um posicionamento do Advertising DSP, você pode direcionar o posicionamento para todos os públicos-alvo disponíveis no DSP. Você também pode [criar tags personalizadas de segmento de público-alvo](/help/dsp/audiences/custom-segment-create.md) para rastrear todos os visitantes de páginas de aterrissagem específicas e, em seguida, usar esses segmentos como alvos criativos para um posicionamento.
>* Os visitantes do site que optaram por não ser rastreados para direcionamento de anúncios não recebem anúncios com conteúdo criativo personalizado com base no segmento de público-alvo ou no perfil de redirecionamento.

## Criar um pixel de redirecionamento

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Creative]** e selecione > **[!UICONTROL Retargeting Pixel]**.

1. Especifique as [configurações de pixel de redirecionamento](#retargeting-pixel-settings).

1. Clique em **[!UICONTROL Save]**.

1. [Gere a marca de pixel](#retargeting-pixel-generate) a ser fornecida ao anunciante ou ao contato do site.

   A marca de pixel de redirecionamento deve ser a última ação na página.<!-- verify here and below -->

   O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

## Editar um pixel de redirecionamento

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenha o cursor sobre o nome do pixel e clique em **[!UICONTROL Edit]**.

1. Edite as [configurações de pixel de redirecionamento](#retargeting-pixel-settings).

1. Clique em **[!UICONTROL Save]**.

1. [Gere a marca de pixel](#retargeting-pixel-generate) para fornecer ao anunciante ou ao contato do site para que ele possa substituir a marca original.

   A tag de pixel de redirecionamento deve ser a última ação na página de destino.

   O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

## Gerar uma tag para um pixel de redirecionamento {#retargeting-pixel-generate}

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenha o cursor sobre o nome do pixel e clique em **[!UICONTROL Generate Tag]**.

1. Clique em **[!UICONTROL Copy to Clipboard]** para copiar a marca para a área de transferência do computador, da qual você pode colar o texto em um arquivo para salvar.

1. Na marca de pixel, especifique um valor para cada atributo nas seções `<img src>` e `<script src>` substituindo cada &quot;`Insert <attribute>`&quot; por um valor. Especifique uma ID de parceiro ID5 se a tag capturar uma ID universal.

   Se você adicionar outros atributos manualmente, deverá incluir a codificação do URL.

   Por exemplo, se você incluiu os atributos &quot;category&quot;, &quot;color&quot; e &quot;size&quot; e capturou IDs universais de ID5, a marca de pixel incluirá os seguintes parâmetros: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` e `&id5pid=--Insert ID5_PARTNER_ID--`. Para direcionar os usuários que selecionam sandálias vermelhas no tamanho 10, por exemplo, altere os parâmetros da marca de imagem e da marca de script para `&ut1=sandals&ut2=red&ut3=10` e insira sua ID de parceiro de ID5 na marca de script, como `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Forneça a tag de pixel concluída ao anunciante ou contato do site, juntamente com uma lista das páginas de aterrissagem relevantes nas quais inseri-la.

   A tag de pixel de redirecionamento deve ser a última ação na página de destino.

   O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

## Excluir um pixel de redirecionamento

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenha o cursor sobre o nome do pixel e clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Configurações de pixel de redirecionamento {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** O nome do pixel. **Observação:** a marca de pixel inclui a identificação de pixel (`pxId=<ID>`), não o nome do pixel.

**[!UICONTROL Advertiser]:** (Somente leitura para pixels existentes) O anunciante para o qual o pixel é rastreado.

**[!UICONTROL Attribute 1]:** Um atributo a ser incluído na marca de pixel, como &quot;SKU&quot;, &quot;categoria&quot;, &quot;tamanho&quot; ou outros atributos da página ou do produto exibido na página. Especifique um valor para o atributo na tag de pixel antes de inseri-lo nas páginas da Web relevantes.

Ao direcionar experiências de anúncios para usuários expostos ao pixel, as configurações de direcionamento especificam os valores de atributo que devem estar presentes para exibir as criações.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Opcional) Atributos adicionais a serem incluídos na marca de pixel. Especifique um valor para cada atributo adicional na tag de pixel antes de inseri-la nas páginas da Web relevantes.

Ao direcionar experiências de anúncios para usuários expostos ao pixel, as configurações de direcionamento especificam os valores de atributo que devem estar presentes para exibir as criações.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (Somente novos pixels; opcional) Tipos de IDs universais para a marca de pixel a ser rastreada:

* *[!UICONTROL ID5]:* A marca de pixel rastreia [!DNL ID5] IDs. Nenhuma taxa é incorrida para impressões entregues a IDs universais.

* *[!UICONTROL Ramp ID]:* A marca de pixel rastreia [!DNL Ramp IDs]. Nenhuma taxa é incorrida para impressões entregues a IDs universais.

Para usar esse recurso, você ou outro usuário na conta da DSP deve aceitar os termos do contrato de serviço para usar IDs universais uma vez antes de usar IDs universais para um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta da Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **[!UICONTROL Terms of Service]**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Configurações de experiência de anúncio direcionado](/help/creative/experiences/experience-settings-targeting.md)
>* [Sobre experiências de publicidade](/help/creative/experiences/experience-about.md)
