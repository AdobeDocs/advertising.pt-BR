---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---
# Modelo de anúncio de texto - Feed e colunas

**[!UICONTROL Feed & Columns]:** A [arquivo de feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md) ou conta de comerciante associada ao modelo e as colunas (cabeçalhos) do arquivo ou conta selecionada:

* *[!UICONTROL Feed File]:* Faça upload de um arquivo ou selecione um arquivo na lista de arquivos de feed disponíveis.

* *[!UICONTROL Google Merchant Center]:* Selecione um [sincronizado [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Pesquisa, Social e Comércio cria somente grupos de produtos; [!DNL Google Ads] gera automaticamente os anúncios de compras para os grupos de produtos. Colunas personalizadas não são suportadas.

* *[!UICONTROL Microsoft Merchant Center]:* ([!DNL Microsoft Advertising] modelos de compras somente) Selecione um [sincronizado [!DNL Microsoft Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Pesquisa, Social e Comércio cria somente grupos de produtos; [!DNL Microsoft Advertising] gera automaticamente os anúncios de produto para os grupos de produtos. Colunas personalizadas não são suportadas.

Associar o modelo a um arquivo de feed ou conta de comerciante é opcional até que você esteja pronto para criar anúncios usando o modelo.

Ao inserir uma coluna de feed em um campo de modelo, o valor inserido é indicado como `[field_name]`, onde &quot;field_name&quot; é o nome de campo especificado, para indicar que o valor é uma variável.

>[!NOTE]
>
>* Se você alterar o arquivo de feed ou a conta de um modelo existente, talvez precise ajustar os parâmetros do modelo se o novo arquivo contiver cabeçalhos diferentes.
>* Se o arquivo de feed ou a conta associada ao modelo for excluída ou desabilitada, a associação também será excluída e você deverá selecionar um novo arquivo de feed antes de criar mais anúncios usando o modelo. Se o novo arquivo ou conta de feed não incluir os mesmos cabeçalhos do arquivo original, talvez seja necessário ajustar os parâmetros do modelo adequadamente.

