---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Campo Parâmetros personalizados nas configurações de campanha do GGL e do MS, configurações de grupo de anúncios do MS e configurações de anúncios responsivos e multimídia do MS

**[!UICONTROL Custom Parameters]:** (Opcional; aplicável a campanhas de público-alvo somente para [!DNL Microsoft Advertising]) Pares de nome e valor para até três parâmetros personalizados. O comprimento máximo dos nomes é de 16 caracteres alfanuméricos; o comprimento máximo dos valores é de 200 caracteres, incluindo parâmetros incorporados.

Você pode incluir seus nomes de parâmetros personalizados nos modelos de rastreamento da entidade e de suas entidades filhas. Quando um usuário clica em um anúncio relevante, a rede de anúncios substitui o nome do parâmetro pelo valor do parâmetro definido. Por exemplo, se você criar um parâmetro de cliente `{_color}=red` e seu modelo de rastreamento inclui `http://tracker.example.com/?color={_color}&u={lpurl}`, em seguida, &quot;vermelho&quot; é inserido no parâmetro de cor quando um usuário clica em um anúncio.

Parâmetros personalizados no grupo de publicidade ou ([!DNL Microsoft Advertising] somente) o nível do anúncio substitui os parâmetros personalizados do nível da campanha com o mesmo nome.
