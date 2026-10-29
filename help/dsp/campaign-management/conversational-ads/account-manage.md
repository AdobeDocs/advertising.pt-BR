---
title: Gerenciar contas de anúncios conversacionais de [!DNL ChatGPT Ads]
description: Saiba como criar e gerenciar contas para [!DNL ChatGPT Ads] anúncios de cartão de chat, um recurso beta que coloca anúncios dentro de conversas do assistente de IA.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# Gerenciar contas de anúncios conversacionais de [!DNL ChatGPT Ads]

*recurso do Beta*

Por meio da integração do Adobe DSP com o [!DNL OpenAI Ads], você pode executar [!DNL ChatGPT Ads] anúncios de cartões de chat, que aparecem dentro de [!DNL ChatGPT] conversas. Para esse recurso, a DSP cria uma conta de anúncio conversacional e compra mídia em nome de sua organização. Você não poderá acessar a conta de anúncio em ads.openai.com. Use este recurso para testar a mídia de IA sem estabelecer uma relação direta com [!DNL ChatGPT Ads].

Você gerenciará suas contas de anúncios conversacionais do [!DNL ChatGPT Ads], incluindo campanhas, grupos de anúncios e anúncios, separadamente das campanhas regulares do DSP, que são estruturadas de forma diferente. Você também [visualizará dados de desempenho de [!DNL ChatGPT Ads] campanhas, grupos de anúncios e anúncios](campaign-manage.md#campaign-views-about) separadamente de suas campanhas do DSP.

## Elegibilidade

Os itens a seguir determinam a qualificação para esse recurso:

* **Clientes [!DNL Search, Social, & Commerce] existentes:** se seu anunciante já usa o [!DNL Search, Social, & Commerce], [crie e gerencie suas [!DNL ChatGPT Ads] campanhas no Search, Social e Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) em vez de no DSP.

* **Setores restritos:** anunciantes em categorias restritas (por exemplo, finanças ou assistência médica) não podem criar contas de anúncios conversacionais ou campanhas.

Se o anunciante selecionado não estiver qualificado, as guias [!UICONTROL Accounts] e [!UICONTROL Campaigns] indicarão o motivo. Você ainda pode alternar para um anunciante diferente usando o seletor de anunciante.

Para usar o recurso, entre em contato com a equipe de conta da Adobe para iniciar o processo de integração.

## Faturamento

Você é cobrado pelo uso de [!DNL ChatGPT Ads] no final do mês com suas outras faturas, usando a moeda de cobrança e o fuso horário de cobrança para sua conta da DSP (independentemente da [moeda e do fuso horário usados para a [!DNL ChatGPT Ads] conta](#account-settings)). Em caso de dúvidas sobre cobrança, entre em contato com a equipe de conta da Adobe.

## A visualização [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] {#accounts-view}

A guia [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] lista as contas [!DNL OpenAI] do anunciante selecionado. As informações de cada conta incluem:

**[!UICONTROL Status]:** Se a conta está oferecendo anúncios: *Ativa* ou *Pausada*. Não é possível alterar o status de uma conta; entre em contato com a equipe de conta da Adobe se desejar pausar ou reativar uma conta.

**[!UICONTROL Review status]:** O estado de revisão [!DNL OpenAI]: *Em Revisão*, *Aprovado* ou *Desaprovado*. Mantenha o cursor sobre o status do motivo, se disponível.

**[!UICONTROL Active campaigns]:** O número de campanhas ativas atualmente na conta.

**[!UICONTROL Cost]:** O gasto total da conta.

### Ações disponíveis

* [Exibir limites de conta](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [Criar uma conta](#account-create)

* [Editar uma conta](#account-edit)

* [Atualizar a lista de contas](#account-refresh)

* [Retornar ao menu principal do DSP](#return-to-menu)

## Gerenciar contas

### Exibir limites de conta {#account-limits}

Um limite de conta limita o gasto total de uma conta em um intervalo de datas específico. É possível visualizar os limites de uma conta, mas somente a equipe de conta da Adobe pode criar, editar ou remover os limites.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. Na exibição **[!UICONTROL Accounts]**, mantenha o cursor sobre a linha da conta e clique em **[!UICONTROL ...]>[!UICONTROL View account limit]**.

A página [!UICONTROL Account limits] lista cada limite da conta:

**[!UICONTROL Name]:** O nome do limite.

**[!UICONTROL Amount]:** O limite de gastos total para o período de limite.

**[!UICONTROL Period]:** O intervalo de datas ao qual o limite se aplica.

**[!UICONTROL Status]:** *Ativo*, *Futuro* ou *Concluído*.

**[!UICONTROL Spent]:** O valor gasto até o momento dentro do período de limite.

>[!NOTE]
>
>Não é possível editar ou remover limites concluídos, e os períodos de limite para a mesma conta não podem se sobrepor.

### Crie uma conta de anúncio conversacional [!DNL ChatGPT Ads] {#account-create}

Para criar mais de duas contas do [!DNL ChatGPT Ads] para um anunciante, entre em contato com a equipe de conta da Adobe.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. Siga um destes procedimentos:

   * (Somente sua primeira conta) Na tela de boas-vindas, clique em **[!UICONTROL Create an Account]**.

   * Na exibição **[!UICONTROL Accounts]**, selecione um anunciante e clique em **[!UICONTROL Create Account]**.

1. Especifique as [configurações da conta](#account-settings).

1. Marque a caixa de seleção **[!UICONTROL I agree to the Terms and Conditions]**.

1. Clique em **[!UICONTROL Create account]**.

Novas contas são criadas em um estado pausado enquanto [!DNL OpenAI] as analisa. A DSP ativa a conta após ser aprovada.

### Editar uma conta de anúncio conversacional [!DNL ChatGPT Ads] {#account-edit}

Você pode editar o nome comercial legal e o site de uma conta depois de criá-la.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. Na exibição **[!UICONTROL Accounts]**, mantenha o cursor sobre a linha da conta e clique em **[!UICONTROL ...]>[!UICONTROL Edit account]**.

1. Edite o **[!UICONTROL Legal Business Name]** e/ou **[!UICONTROL Advertiser Website]**. Para obter mais informações sobre os campos, consulte &quot;[Configurações da conta](#account-settings)&quot;.

1. Clique em **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>Salvar alterações reinicia a revisão de [!DNL OpenAI] para a conta. A conta não veiculará os anúncios novamente até que seja aprovada novamente.

### Atualizar a lista de contas {#account-refresh}

Exibe novamente a lista de contas quando outros usuários podem ter feito alterações ou adições.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. Na exibição **[!UICONTROL Accounts]**, clique em **[!UICONTROL Refresh]** acima da lista de contas.

### Retornar ao menu principal do DSP {#return-to-menu}

* Acima do menu principal, clique em **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] configurações de conversação e conta {#account-settings}

**[!UICONTROL Legal Business Name]:** O nome comercial registrado da organização.

**[!UICONTROL Advertiser Website]:** A URL do site do anunciante, começando com `http://` ou `https://`.

**[!UICONTROL Country]:** O país no qual a organização está legalmente registrada (não o país no qual você executará anúncios). Deve ser o mesmo que o país usado para o contrato DSP da organização. Você não pode alterar esse valor depois de salvar a conta.

**[!UICONTROL Currency]:** (Somente leitura) A moeda que sua Equipe de Conta da Adobe configura para a conta [!DNL ChatGPT Ads]. Pode ser diferente da moeda da sua conta do DSP, que pode ser vista em outro lugar no DSP. **Observação:** independentemente desse valor, todas as faturas de uso estarão na *moeda de cobrança* usada para a conta da DSP.

**[!UICONTROL Timezone]:** (Somente leitura) O fuso horário que sua equipe de conta da Adobe configura para a conta [!DNL ChatGPT Ads]. Pode ser diferente do fuso horário usado para sua conta do DSP, que é visível em outro lugar no DSP. **Observação:** independentemente desse valor, todas as faturas de uso representarão o *fuso horário de cobrança* usado para a conta do DSP.

**[!UICONTROL Favicon]:** Um arquivo de imagem a ser usado como favicon de site para a conta.<!-- How is this used within this context? --> O navegador exibe o favicon em vários locais, como barra de endereços, guia ou marcadores. O arquivo deve estar no formato JPG, PNG ou WEBP e ter no mínimo 256x256 pixels.

Para carregar um ícone, clique em **[!UICONTROL Upload favicon]**, localize e selecione um arquivo em seu dispositivo ou rede.

**[!UICONTROL I agree to the Terms and Conditions]:** Uma caixa de seleção para indicar que você concorda com todos os termos legais. Marque a caixa de seleção para criar uma conta ou atualizar as configurações da conta.

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas de anúncios conversacionais](campaign-manage.md)
