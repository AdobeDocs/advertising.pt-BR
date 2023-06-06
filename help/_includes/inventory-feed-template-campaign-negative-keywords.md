---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Modelo de anúncio de texto - Configurações de palavras-chave negativas no nível da campanha

**[!UICONTROL Delete negative keywords when omitted from list]:** (Todas as redes de anúncios, exceto Yandex; opcional) Exclui palavras-chave negativas existentes no nível da campanha criadas anteriormente usando o modelo que não estão especificadas nas listas abaixo. **Nota:** Palavras-chave negativas criadas usando outros meios (como em bulksheets simples, a variável [!UICONTROL Campaigns] ou no editor de anúncios da rede de publicidade) nunca são removidos usando o modelo.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Todas as redes de anúncios, exceto Yandex; opcional) Permite que você especifique palavras-chave negativas para campanhas cujo nome inclua uma sequência especificada. Ao selecionar essa opção, você pode adicionar até três sequências de caracteres de nome de campanha e palavras-chave correspondentes.

Para cada string, clique em **[!UICONTROL Add (Up to 3)]** e insira as seguintes informações:

* **[!UICONTROL If campaign name contains]:**  Uma string de texto para procurar em qualquer lugar dentro do nome da campanha. A consulta diferencia maiúsculas e minúsculas (por exemplo, &quot;[!DNL Car]&quot; corresponde ao nome da campanha &quot;[!DNL Car Parts]&quot; mas não &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Qualquer palavra-chave negativa estática em nível de campanha que deve ser adicionada em campanhas cujo nome inclua a cadeia de caracteres especificada. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Use a sintaxe a seguir, sem um sinal de menos:

   * Correspondência ampla negativa: `keyword` (não suportado pelo [!DNL Microsoft Advertising])
   * Correspondência de frase negativa: `"keyword"`
   * Correspondência exata negativa: `[keyword]`

A sintaxe usual para os tipos de frase e correspondência exata é usada no bulksheet gerado ao propagar dados de feed por meio do modelo. **Nota:** Você não pode ver as palavras-chave negativas no [!UICONTROL Keywords] ou na guia [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] exibição.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Todas as redes de publicidade, exceto [!DNL Yandex]; opcional) Quaisquer palavras-chave negativas estáticas em nível de campanha que devem ser adicionadas em campanhas cujo nome não corresponda a uma sequência de caracteres especificada. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Use a sintaxe a seguir, sem um sinal de menos:

* Correspondência ampla negativa: `keyword` (não suportado pelo [!DNL Microsoft Advertising])
* Correspondência de frase negativa: `"keyword"`
* Correspondência exata negativa: `[keyword]`

A sintaxe usual para os tipos de frase e correspondência exata é usada no bulksheet gerado ao propagar dados de feed por meio do modelo. **Nota:** Você não pode ver as palavras-chave negativas no [!UICONTROL Keywords] ou na guia [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] exibição.
