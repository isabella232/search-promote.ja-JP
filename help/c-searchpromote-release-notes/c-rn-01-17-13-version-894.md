---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.9.4リリースノート（2013年1月18日）
solution: Target
title: Search&Promote 8.9.4リリースノート（2013年1月18日）
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 8.9.4 Release Notes (01/17/2013){#search-promote-release-notes}

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
   <td colname="col2"> <p> クエリ消去ルール、検索前のルールおよび検索後のルールの作成時に、インラインメモを作成できる機能を追加しました。このメモフィールドによって、ルールを文書化しルールについて説明することができます。 </p> <p>詳しくは、 <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> クエリクリーニング規則についてを参照し</a>。 </p> <p>See <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> About Pre-Search Rules</a>. </p> <p>See <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> About Post-Search Rules</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ガイド付き検索 </p> </td> 
   <td colname="col2"> <p> 検索にかかった合計時間を示すガイド付き検索タグを追加しました。 </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> — 検索にかかった時間を示します。 返される検索時間の値はミリ秒単位で指定します。 </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> — 検索結果のページを作成する際に使用されるコア検索の数を返します。 </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> — コア検索の数が1より大きいかどうかをテストします。 </p> <p>プレゼンテーションテンプレートタグのその他の <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> 言語も参照してくださ</a>い。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* キーワードレポートで、アスタリスクが無視されるようになりました。

   「キーワ [ードレポートの表示」または「検索キーワードが空の場合」を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Open **[!UICONTROL Reports > Null Search Terms Report]**, select a time slot and then view the report. レポート内のある単語をクリックして検索を開始し、その後「View Report」を再度クリックすると、クリックしたキーワードの検索数が 2 回増加します。この現象が修正されました。

   「キーワ [ードレポートの表示」または「検索キーワードが空の場合」を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* ビジネスルールをライブにプッシュした場合のパフォーマンスの最適化が行われました。

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* The ability to remove in [!DNL Breadcrumbs] did not work all the time.

   詳しくは、パ [ンくずリストについてを参照してくださ](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03)い。

* regenerateを使用しない限り、再ランク機能では、変更されたランク付けルールを検索結果で有効にできませんでした。

   [ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

   Re-Rank [Indexについてを参照してください](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692)。

