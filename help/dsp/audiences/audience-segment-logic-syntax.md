---
title: Sintaxe da lógica do segmento de público-alvo
description: Faça referência à sintaxe que pode ser usada para definir a lógica dos segmentos de público-alvo.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 97f5e8913afb2f71505512bf8e4ab5bf56c1d7f8
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Sintaxe da lógica do segmento de público-alvo

Ao criar públicos-alvo reutilizáveis, você pode definir manualmente a lógica do segmento usando IDs de segmento alfanuméricos (chaves) e a seguinte sintaxe:

* () para indicar um grupo
* `||` para [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; para [!DNL AND]
* ! para [!DNL NOT] (excluir)

>[!NOTE]
>
>* Todos os grupos de segmentos especificados são incluídos, a menos que sejam precedidos por ! (o que os exclui).
>* Você pode [encontrar a ID de segmento para um público-alvo](reusable-audience-clipboard.md) de [!UICONTROL Audiences] > [!UICONTROL All audiences].

Por exemplo, a seguinte lógica:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (em inglês simples)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Nas configurações de posicionamento, é possível usar os públicos salvos como públicos-alvo para direcionar explicitamente ou como públicos-alvo separados para excluir do direcionamento. Verifique se a lógica do segmento reflete a finalidade para a qual você usará o público-alvo.

>[!MORELIKETHIS]
>
>* [Copiar a chave de segmento de um público-alvo reutilizável para a área de transferência](reusable-audience-clipboard.md)
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público](audience-settings.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
