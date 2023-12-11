---
title: Fundamentos da [!DNL Marketing Channels]
description: Saiba mais sobre as principais informações [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] os usuários devem entender.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Fundamentos da [!DNL Analytics Marketing Channels]

Esta página explica as principais informações sobre [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] os usuários precisam entender.

Para obter a documentação completa sobre [!DNL Marketing Channels], consulte &quot;[Introdução ao [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Visão geral do [!DNL Marketing Channels]

[!DNL Marketing Channels] são um recurso importante do Adobe Analytics. [!DNL Marketing Channels] os relatórios mostram como os clientes chegam ao seu site pela janela de relatórios e como cada canal afeta a receita ou o comportamento no site.

Considere o exemplo a seguir de uma jornada entre visitas. Cada visita ao seu site é indicada pelo canal de marketing do qual o visitante entrou. A primeira visita, também chamada de Canal de primeiro contato, é email. Exibir na visita dois é um canal participante e a Pesquisa natural é considerada o Canal de último contato. Se você usar [!UICONTROL Last Touch Attribution] no prazo de [!UICONTROL Attribution IQ]No entanto, a Pesquisa natural receberia crédito total pelo evento de conversão de US$ 250. Usando o Serviço de ID de Experience Cloud, é possível unir essas visitas individuais para revelar uma jornada por um único visitante.

![Exemplo de jornada de conversão entre visitas em Canais de marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Ao usar [!UICONTROL Marketing Channels] Regras de processamento, você pode criar conjuntos de lógicas para determinar os canais que direcionam o tráfego e rastrear cada canal à medida que os usuários chegam ao seu site. Por exemplo, a variável [!UICONTROL Email] channel seria indicado por um código de rastreamento exclusivo gerado após o clique que, quando registrado pelo Adobe Analytics, categorizaria a visita como originada de uma campanha de marketing por email.

## Regras de processamento e como os canais de marketing são definidos

Cada vez que um usuário acessa um site, ele o faz por meio de um URL no qual clicou ou digitou diretamente na barra de endereços. Quando o usuário entra no site, [!DNL Analytics] rastreia informações que podem ser usadas para determinar o canal que determinou a visita.

Geralmente, os profissionais de marketing acrescentam códigos de rastreamento de parâmetro da sequência de consulta aos URLs de canal para ajudar a rastrear o impacto do canal em seu site. Você pode configurar [!DNL Marketing Channels] regras de processamento para acompanhar parâmetros e valores de rastreamento específicos para determinar o canal sem nenhum rastreamento adicional. Por exemplo, se todos os URLs de campanha de email seguirem o formato `www.adobe.com?cid=email…` (onde o URL contém o parâmetro e o valor da string de consulta) `cid=email`), será possível criar uma regra para ouvir esse código de rastreamento e agrupar a visita no [!UICONTROL Email] canal.

Outros canais não têm caminhos de URL rastreáveis e precisam de lógica adicional para identificação. Por exemplo, [!UICONTROL Earned Social], em que um usuário clica em um link que outro usuário compartilhou organicamente em uma rede social, é um canal importante para rastrear. No entanto, o profissional de marketing não tem como anexar um código de rastreamento de parâmetro da sequência de consulta ao URL que é compartilhado. Nesse caso, você pode criar uma regra de processamento para ouvir o domínio de referência das redes sociais de interesse e a ausência de códigos de rastreamento pagos para determinar o canal. As visitas que atendem a esses requisitos seriam rastreadas como Ganhos sociais no relatório de Canais de marketing.

A Adobe recomenda trabalhar com a equipe de análise para criar um conjunto abrangente de [!DNL Marketing Channels] regras de processamento para rastrear todos os canais pertinentes à sua empresa. Isso permite criar relatórios de atribuição avançados.

Para entender como o Adobe Advertising pode contribuir para os sinais necessários para criar canais de marketing personalizados, consulte &quot;[Usar IDs de publicidade para criar [!DNL Marketing Channels] Regras](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Utilização de IDs de Adobe Advertising para criar [!DNL Marketing Channels] Regras de processamento](mc-ids.md)
>* [Por que os dados de canal podem variar entre Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usar [!DNL Analytics Marketing Channels] com dados de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: usar [!DNL Marketing Channels] para relatório de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
