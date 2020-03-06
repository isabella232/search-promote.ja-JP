---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 15.1.1リリースノート（2015年1月16日）
solution: Target
title: Search&Promote 15.1.1リリースノート（2015年1月16日）
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.1.1 Release Notes (01/15/2015){#search-promote-release-notes}

## 新機能 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* これまでは、ガイド付き検索ルールのキーワードに語幹解釈や同義語といった言語学的調整が常に適用されていました。この拡張を無効にして、キーワードがそのまま使われるようにすることができます。

   ビジネス・ルールにトリガー条件を適用する場合は、次の「 [!DNL Advanced Rule Builder], **[!UICONTROL If any/all of the following conditions are met]**」の最初のドロップダウン・リストでを選択し、2番目のドロップダウン・リストで新しい演算子 **[!UICONTROL keyword]****[!UICONTROL equal exact]** を選択します。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] に設定さ [!DNL Advanced Rule Builder] れ、「MDI(Merchandising Document ID)」フィールドの値が切り捨てられなくなりました。
* RBTA 関連のインデックスエラーを修正しました。
* ステータスが「承認済み」の既存のビジネスルールを編集すると、「承認済み」ステータスが失効するようになりました。 You must use [!DNL Advanced Rule Builder] to recheck the option **[!UICONTROL Approved]**, and then save the rule as usual. If you do not reapprove an edited rule, the rule&#39;s status is automatically set to WIP (Work In Progress) on the [!DNL Business Rules] page.
* A new **[!UICONTROL Advanced Search]** option is now available on the [!DNL Business Rules] page for improved filtering of rules.
* 、、およ **[!UICONTROL contains word]** びのルールトリガーに条 [!DNL Query Cleaning]件を追 [!DNL Pre-Search Rules]加し、単語の改行を [!DNL Post Search Rules][!DNL Business Rules]簡単に指定できるようにしました。
* ルールの表示時など、ビジネスルールのメモに対して行われた改良点で、そのルールのメモ履歴を取得できるようになりました。 また、メモは、>にログインされるようにな **[!UICONTROL Reports]** りまし **[!UICONTROL Change Log]**&#x200B;た。
* Queries with nonzero `sp_i` values are no longer run through the [!DNL Adobe Analytics] redirector.

   バックエンド検索CGIパラメータの表の15 [行目を参照してください](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)。

