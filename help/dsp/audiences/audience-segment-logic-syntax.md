---
title: Sintaxe da lógica do segmento de público-alvo
description: Faça referência à sintaxe que pode ser usada para definir a lógica dos segmentos de público-alvo.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 141
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
>* Você pode [encontrar a ID de segmento para uma audiência](reusable-audience-clipboard.md) de [!UICONTROL Audiences] > [!UICONTROL All audiences].

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
>Nas configurações de posicionamento, é possível usar os públicos salvos como públicos-alvo para direcionar explicitamente ou como públicos-alvo separados para excluir do direcionamento. Certifique-se de que a lógica do segmento reflita a finalidade de uso do público-alvo.

>[!MORELIKETHIS]
>
>* [Copiar a chave de segmento de um público-alvo reutilizável para a área de transferência](reusable-audience-clipboard.md)
>* [Sobre o gerenciamento de público-alvo](audience-about.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
