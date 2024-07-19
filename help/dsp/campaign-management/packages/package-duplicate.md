---
title: Duplicar um pacote
description: Saiba como duplicar um pacote.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicar um pacote

Duplique um pacote para criar um pacote com configurações semelhantes. Você pode:

* Duplicar o pacote no anunciante e na campanha originais ou em anúncios diferentes
* Opcionalmente, duplicar os posicionamentos no pacote
* (Para pacotes duplicados nas campanhas originais) Opcionalmente, duplique os anúncios originais e os pixels do evento no nível do posicionamento
* Modificar as datas de início e término do novo pacote

Consulte &quot;[O que não está duplicado](#package-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha para abrir a exibição [!UICONTROL Packages].

1. Ao lado do nome do pacote, clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de pacote:

   1. Insira o novo nome do pacote.

   1. (Opcional) Altere as configurações padrão.

      Por padrão:

      * O novo pacote é atribuído ao anunciante e à campanha originais.

      * O novo pacote fica ativo no dia atual.<!-- and the flight continues for NN  days. -->

      * Os posicionamentos dentro do pacote original são copiados para o novo pacote.

      * Os pixels do evento de nível de posicionamento e dos anúncios não são copiados para o novo pacote.

1. Clique em **[!UICONTROL Submit]**.

## O que não está duplicado {#package-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações de experimento
* (Se você alterar as datas de veiculação) Programação de anúncios personalizada
* (Se você não anexar anúncios) Peso e agendamento personalizados de anúncios
* Posicionamentos padrão para ofertas programáticas garantidas (PG) e posicionamentos para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Destinos geográficos
   * Pixels de evento
   * Anúncios
   * Segmentos no nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] (que substituem os segmentos no nível do anunciante)

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Exibir o Log de Alterações de um Pacote](package-change-log.md)
>* [Configurações do pacote](package-settings.md)
