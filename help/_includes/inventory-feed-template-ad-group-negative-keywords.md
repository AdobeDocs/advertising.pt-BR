---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Modelo de anúncio de texto - Configurações de palavras-chave negativas no nível do grupo de anúncios

**[!UICONTROL Delete negative keywords when omitted from list]:** (Todas as redes de anúncios, exceto Yandex; opcional) Exclui palavras-chave negativas existentes no nível do grupo de anúncios criadas anteriormente com o modelo que não estão especificadas nas listas abaixo. **Observação:** palavras-chave negativas criadas por outros meios (como em bulksheets simples, nas exibições [!UICONTROL Campaigns] ou no editor de anúncios da rede de publicidade) nunca são removidas usando o modelo.

**[!UICONTROL Apply these negatives]:** (Todas as redes de anúncios, exceto [!DNL Yandex]; opcional) Qualquer palavra-chave negativa estática de nível de grupo de anúncios a ser adicionada. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Use a sintaxe a seguir, sem um sinal de menos:

* Correspondência ampla negativa: `keyword` (sem suporte de [!DNL Microsoft Advertising])
* Correspondência de frase negativa: `"keyword"`
* Correspondência exata negativa: `[keyword]`

A sintaxe usual para os tipos de frase e correspondência exata é usada no bulksheet gerado ao propagar dados de feed por meio do modelo. **Observação:** você não pode ver as palavras-chave negativas na guia [!UICONTROL Keywords] ou na exibição [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
