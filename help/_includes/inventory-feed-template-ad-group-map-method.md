---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Modelo de anúncio de texto - Método de mapa de grupo de anúncios

**[!UICONTROL Map Method]:** (Quando [!UICONTROL Map Only] está habilitado para grupos de anúncios; todas as redes de anúncios, exceto [!DNL Yandex]) O método pelo qual novas palavras-chave e anúncios são mapeados para grupos de anúncios existentes:

* *[!UICONTROL Contains Anywhere]:* Adiciona dados a um grupo de anúncios existente cujo nome inclui a cadeia de caracteres especificada, se ela existir.

* *[!UICONTROL Contains Exactly]:* Adiciona dados a um grupo de anúncios existente cujo nome inclui a cadeia de caracteres especificada, se ela existir.

* *[!UICONTROL Exactly Matches]* (padrão): adiciona dados a um grupo de anúncios existente com o mesmo nome, se existir.

Quando nenhuma correspondência é encontrada, todos os dados do grupo de anúncios são ignorados. Se os dados do grupo de anúncios no feed não incluírem dados de campanha, o grupo de anúncios será mapeado para um grupo de anúncios com o mesmo nome em qualquer campanha, se existir. Se várias correspondências de grupos de anúncios forem encontradas, as palavras-chave e os anúncios serão mapeados para todas elas.
