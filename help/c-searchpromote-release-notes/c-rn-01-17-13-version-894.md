---
description: Search&amp;Promote 8.9.4リリースノート。
solution: Target
title: Search&amp;Promote 8.9.4リリースノート（2013年1月18日）
topic-legacy: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
exl-id: cb5d93d9-54ac-4b41-96ad-66f18ee1e934
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 30%

---

# Search&amp;Promote8.9.4リリースノート（2013年1月18日）{#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>新機能および機能強化 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ルール </p> </td> 
   <td colname="col2"> <p> クエリ消去ルール、検索前のルールおよび検索後のルールの作成時に、インラインメモを作成できる機能を追加しました。このメモフィールドによって、ルールを文書化しルールについて説明することができます。 </p> <p><a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local">クエリクリーニング規則について</a>を参照してください。 </p> <p><a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local">事前検索ルールについて</a>を参照してください。 </p> <p><a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local">検索後のルールについて</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ガイド付き検索 </p> </td> 
   <td colname="col2"> <p> 検索にかかった合計時間を示すガイド付き検索タグを追加しました。 </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span>  — 検索に要した時間を示します。返される検索時間の値はミリ秒単位で指定されます。 </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span>  — 検索結果のページを作成するのに使用されるコア検索の数を返します。 </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span>  — コア検索の数が1より大きい場合にテストします。 </p> <p>「<a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local">プレゼンテーションテンプレートタグ</a>のその他の言語」も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* キーワードレポートで、アスタリスクが無視されるようになりました。

   [キーワードレポートまたはNULL検索キーワードレポートの表示を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* **[!UICONTROL Reports > Null Search Terms Report]**&#x200B;を開き、時間帯を選択して、レポートを表示します。 レポート内のある単語をクリックして検索を開始し、その後「View Report」を再度クリックすると、クリックしたキーワードの検索数が 2 回増加します。この現象が修正されました。

   [キーワードレポートまたはNULL検索キーワードレポートの表示を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* ビジネスルールをライブにプッシュしたときのパフォーマンスの最適化が行われました。

   [ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

* [!DNL Breadcrumbs]での削除機能は、常に機能していませんでした。

   [パンくずリスト](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03)を参照してください。

* re-rank機能では、regenerateを使用しない限り、ランク付けルールの変更を検索結果に反映させることができませんでした。

   [ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

   [Re-Rank Index](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692)を参照してください。
