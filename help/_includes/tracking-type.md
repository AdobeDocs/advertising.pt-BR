---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Campo Tipo de rastreamento nas configurações da conta e da campanha

**[!UICONTROL Tracking Type]:** O método pelo qual os URLs são gerados:

* *[!UICONTROL EF Redirect]* (o padrão): para clientes que desejam usar o serviço de rastreamento de conversão do Adobe Advertising. Esse método gera IDs exclusivas de rastreamento de cliques e redireciona os usuários para o servidor do Adobe Advertising para fins de rastreamento antes de enviá-los à página inicial do cliente.

   Esse método tem opções de rastreamento padrão que você pode personalizar opcionalmente e também pode especificar parâmetros para anexar a cada URL.

* *[!UICONTROL No EF Redirect]:* Para clientes que desejam usar somente seus próprios códigos de rastreamento de cliques. O Search, Social e Commerce não fornece IDs de rastreamento de cliques ou códigos de redirecionamento. Para contas com URLs de destino, cada URL de destino é o mesmo que o URL de base.

   **Notas:**

   * Somente os usuários de gerente de conta de agência, gerente de conta de Adobe e administrador podem alterar esse valor.
   * Se você alterar o método de rastreamento, deverá gerar novamente as URLs de rastreamento da conta.
   * As opções de rastreamento no nível da campanha substituem as configurações no nível da conta.
