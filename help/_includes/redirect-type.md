---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Campo Tipo de redirecionamento nas configurações da conta e da campanha

**[!UICONTROL Redirect Type]:** (Somente para [!UICONTROL EF Redirect]) O método de redirecionamento de usuários finais para a URL final ou de destino. A opção selecionada é aplicável a todos os anúncios, palavras-chave e posicionamentos na conta ou campanha. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante, e a configuração padrão no nível da campanha é herdada das configurações da conta.

* *[!UICONTROL Standard]:* Para redirecionar o usuário final para a URL especificada.

* *[!UICONTROL Token]:* Para redirecionar o usuário final para a URL e também gravar a ID de Pesquisa, Social e Commerce para o clique (`ef_id`) como um parâmetro de sequência de consulta, que é usado como um token. Escolha esta opção se for relatar transações offline, se quiser que o Search, Social e Commerce troquem dados com o Adobe Analytics ou se quiser rastrear todas as conversões que ocorrem nos navegadores [!DNL Apple Safari].

**Notas:**

* Se você alternar de [!UICONTROL Standard] para [!UICONTROL Token], ou vice-versa, será necessário regenerar as URLs de rastreamento da conta.
* Você pode substituir a configuração no nível da conta no nível da campanha.
