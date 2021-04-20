---
description: 「除外された単語」を使用すると、検索結果から除外する頻度の高い語句や、「a」や「the」などの共通語を指定できます。
solution: Target
title: 除外された単語について
topic: Linguistics,Site search and merchandising
uuid: 1c879462-1b19-44f6-a3b2-20aa786b3221
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# 除外された単語について{#about-excluded-words}

「除外された単語」を使用すると、検索結果から除外する頻度の高い語句や、「a」や「the」などの共通語を指定できます。

## 除外された単語の使用{#concept_9DB67BD2F0DC43AC88741003D9F39812}

[検索について](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)も参照してください。

「除外された単語」を使用しないと、これらの単語を含む検索では、無関係な結果が多数見つかる場合があります。 単語やフレーズを除外すると、指定した除外された用語のみに一致する検索結果は除外されます。 検索クエリに除外された単語が含まれる場合は、除外されない単語だけがドキュメントの検索に使用されます。

除外された検索語は、検索結果でハイライトされません。 ただし、各結果の関連度スコアは、除外された単語の影響を受けます。 つまり、除外された単語は検索ドキュメントの場合は無視されますが、検索結果ページでドキュメントをランク付けする際には引き続き使用されます。 「除外単語」設定（またはこれらの設定への変更）の効果をユーザーが利用できるようにする前に、サイトインデックスを再生成してください。

検索結果から除外する単語を入力する場合は、語句をコンマで区切ります。 1行に1つ以上の除外する単語を入力できます。 次に、個別の行で除外された単語をコンマで割った例を示します。

![](assets/excluded_words_1.jpg)

上記の除外された単語のリスト例を使用して、顧客が「the united states of america」を検索した場合、「the」と「of」という単語は検索から除外されます。 代わりに、「united」、「states」および「america」という語を含むすべてのページが検索されます。 「of」または「the」という語のみを含むページは表示されません。

サイトによっては、ページの大部分またはすべてに特定のフレーズが含まれる場合があります。 例えば、ニューヨーク市の観光に関するWebサイトでは、各ページのタイトルに「ニューヨーク」という語を含めることができます。 このフレーズなどをexcludeリストに追加することを検討します。

![](assets/excluded_words_2.jpg)

フレーズを除外しても、それを構成する個々の単語は検索用語として引き続き使用されます。 訪問者が完全一致の語句を検索した場合に限り、除外された語句の正確な順序で、その語句が検索結果から除外されます。 上記の例を使用して、顧客が「ニューヨークバレエ」を検索した場合、「the」と「new york」という語は除外されます。「baleet」という単語を含むページのみが検索結果として返されます。 一方、「new buildings」や「duke of york」を検索すると、それぞれ「new」や「york」という語を含むページが検索されます。

## 除外単語の設定{#task_60BF6BB7A66C48479D2BBB32C0F38CDE}

頻繁に使用するフレーズや共通語を検索結果から除外できます。

1行に1つ以上の単語を入力できます。 次の例のように、各単語はコンマで区切ります。

![](assets/excluded_words_1.jpg)

顧客の検索に含まれるすべての単語が除外されている場合に、検索結果を表示するように選択できます。 例えば、「the」という語を除外し、顧客が「the」のみを検索することを選択した場合、検索結果には「the」という語を含むページが表示されます。 この結果は、「the」という単語が除外されている場合でもtrueになります。 このオプションを選択しないと、顧客は検索結果を一切得られません。 この設定は、除外されない単語が1つ以上含まれる場合は無効です。

**除外する単語を設定するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Excluded Words]**&#x200B;をクリックします。
1. [!DNL Excluded Words]ページの&#x200B;**[!UICONTROL Words and Phrases]**&#x200B;テキストフィールドに、検索結果から除外する単語を入力します。
1. （オプション）**[!UICONTROL Show results when all words in the query are excluded words]**&#x200B;をクリックします。

   顧客の検索内のすべての単語が除外された場合、すべての単語が一緒に使用されて検索が実行されます。
1. クリック **[!UICONTROL Save Changes]**.
1. 変更の結果をプレビューするには、**[!UICONTROL regenerate your staged site index]**&#x200B;をクリックして、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）製品メニューで&#x200B;**[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]**&#x200B;をクリックし、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

