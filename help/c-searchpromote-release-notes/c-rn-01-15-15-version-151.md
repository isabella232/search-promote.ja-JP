---
description: Search&amp;Promote 15.1.1リリースノート。
solution: Target
title: Search&amp;Promote 15.1.1リリースノート（2015年1月16日）
topic: リリースノート，サイト検索とマーチャンダイジング
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 16%

---


# Search&amp;Promote15.1.1リリースノート（2015年1月16日）{#search-promote-release-notes}

## 新機能 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* これまでは、ガイド付き検索ルールのキーワードに語幹解釈や同義語といった言語学的調整が常に適用されていました。この拡張を無効にして、キーワードがそのまま使われるようにすることができます。

   ビジネスルールにトリガー条件を適用する場合、[!DNL Advanced Rule Builder]の&#x200B;**[!UICONTROL If any/all of the following conditions are met]**&#x200B;の後ので、最初のドロップダウンリストで「**[!UICONTROL keyword]**」を選択し、2番目のドロップダウンリストで新しい演算子「**[!UICONTROL equal exact]**」を選択します。

   [ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

## 修正点と機能強化{#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] MDI(マーチャンダイジングドキュメントID)フィールドの値が切り捨てら [!DNL Advanced Rule Builder] れなくなりました。
* RBTA 関連のインデックスエラーを修正しました。
* ステータスが「承認済み」の既存のビジネスルールを編集すると、「承認済み」ステータスが取り消されるようになりました。 [!DNL Advanced Rule Builder]を使用して&#x200B;**[!UICONTROL Approved]**&#x200B;オプションを再確認し、通常どおりルールを保存する必要があります。 編集したルールを再度承認しない場合、[!DNL Business Rules]ページで、ルールのステータスが自動的にWIP(Work In Progress)に設定されます。
* 新しい&#x200B;**[!UICONTROL Advanced Search]**&#x200B;オプションが[!DNL Business Rules]ページで利用できるようになり、ルールのフィルター機能が強化されました。
* [!DNL Query Cleaning]、[!DNL Pre-Search Rules]、[!DNL Post Search Rules]および[!DNL Business Rules]のルールトリガーに、単語の区切りを簡単に指定できるように、**[!UICONTROL contains word]**&#x200B;条件を追加しました。
* ルールを表示する際に、そのルールのメモ履歴を取得できるようになりました。 また、メモは現在&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Change Log]**&#x200B;に記録されます。
* `sp_i`以外の値を持つクエリは、[!DNL Adobe Analytics]リダイレクターで実行されなくなりました。

   [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)の表の15行を参照してください。

