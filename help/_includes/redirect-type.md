---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Campo Tipo de redirecionamento nas configurações da conta e da campanha

**[!UICONTROL Redirect Type]:** (Para [!UICONTROL EF Redirect] somente) O método de redirecionar usuários finais para o URL final ou de destino. A opção selecionada é aplicável a todos os anúncios, palavras-chave e posicionamentos na conta ou campanha. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante, e a configuração padrão no nível da campanha é herdada das configurações da conta.

* *[!UICONTROL Standard]:* Para redirecionar o usuário final para o URL especificado.

* *[!UICONTROL Token]:* Para redirecionar o usuário final para o URL e também registrar a ID de pesquisa, social e comércio para o clique (`ef_id`) como parâmetro de sequência de consulta, que é usado como token. Escolha esta opção se for relatar transações offline, se desejar que o Search, Social e Commerce troquem dados com o Adobe Analytics ou se quiser rastrear todas as conversões que ocorrem no [!DNL Apple Safari] navegadores.

**Notas:**

* Se você alternar de [!UICONTROL Standard] para [!UICONTROL Token], ou vice-versa, você deverá gerar novamente as URLs de rastreamento da conta.
* Você pode substituir a configuração no nível da conta no nível da campanha.
