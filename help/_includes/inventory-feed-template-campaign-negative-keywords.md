---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Modelo de anúncio de texto - Configurações de palavras-chave negativas no nível da campanha

**[!UICONTROL Delete negative keywords when omitted from list]:** (Todas as redes de anúncios, exceto Yandex; opcional) Exclui palavras-chave negativas existentes no nível de campanha criadas anteriormente usando o modelo que não estão especificadas nas listas abaixo. **Observação:** palavras-chave negativas criadas por outros meios (como em bulksheets simples, nas exibições [!UICONTROL Campaigns] ou no editor de anúncios da rede de publicidade) nunca são removidas usando o modelo.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Todas as redes de anúncios, exceto Yandex; opcional) Permite que você especifique palavras-chave negativas para campanhas cujo nome inclua uma cadeia de caracteres especificada. Ao selecionar essa opção, você pode adicionar até três sequências de caracteres de nome de campanha e palavras-chave correspondentes.

Para cada cadeia de caracteres, clique em **[!UICONTROL Add (Up to 3)]** e insira as seguintes informações:

* **[!UICONTROL If campaign name contains]:** Uma cadeia de texto a ser procurada em qualquer lugar dentro do nome da campanha. A consulta diferencia maiúsculas e minúsculas (por exemplo, &quot;[!DNL Car]&quot; corresponde ao nome da campanha &quot;[!DNL Car Parts]&quot;, mas não &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:** Qualquer palavra-chave negativa estática em nível de campanha a ser adicionada para campanhas cujo nome inclua a cadeia de caracteres especificada. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Use a sintaxe a seguir, sem um sinal de menos:

   * Correspondência ampla negativa: `keyword` (sem suporte de [!DNL Microsoft Advertising])
   * Correspondência de frase negativa: `"keyword"`
   * Correspondência exata negativa: `[keyword]`

A sintaxe usual para os tipos de frase e correspondência exata é usada no bulksheet gerado ao propagar dados de feed por meio do modelo. **Observação:** você não pode ver as palavras-chave negativas na guia [!UICONTROL Keywords] ou na exibição [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

**[!UICONTROL All other campaigns: Apply these negatives]:** (Todas as redes de anúncios, exceto [!DNL Yandex]; opcional) Quaisquer palavras-chave negativas estáticas em nível de campanha a serem adicionadas para campanhas cujo nome não corresponda a uma cadeia de caracteres especificada. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Use a sintaxe a seguir, sem um sinal de menos:

* Correspondência ampla negativa: `keyword` (sem suporte de [!DNL Microsoft Advertising])
* Correspondência de frase negativa: `"keyword"`
* Correspondência exata negativa: `[keyword]`

A sintaxe usual para os tipos de frase e correspondência exata é usada no bulksheet gerado ao propagar dados de feed por meio do modelo. **Observação:** você não pode ver as palavras-chave negativas na guia [!UICONTROL Keywords] ou na exibição [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
