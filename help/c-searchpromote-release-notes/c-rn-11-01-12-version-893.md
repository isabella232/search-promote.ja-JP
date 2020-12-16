---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 8.9.3リリースノート（2012年11月1日）
solution: Target
title: Search&amp;Promote 8.9.3リリースノート（2012年11月1日）
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 84%

---


# Search&amp;Promote8.9.3リリースノート（2012年11月1日）{#search-promote-release-notes}

## Search&amp;Promote8.9.3リリースノート（2012年11月1日） {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>新機能および機能強化 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Facet Rail </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390-->「<span class="uicontrol">Facet Rail</span>」オプションが追加され、ファセット群およびファセット名の順序をより詳細（数順、アルファベット順）に制御できるようになりました。 </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">「Facet Rail」について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ネストされたファセット </p> </td> 
   <td colname="col2"> <p> ネストされたファセットの代替の並べ替えへのサポートを追加しました。 </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">「Facet Rail」について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ランキングルールの「メモ」フィールド </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772-->ランキングルールおよびルールグループの定義で使用する <span class="wintitle">Add Ranking Metric</span> ダイアログボックスおよび <span class="wintitle">Edit Ranking Metric</span> ダイアログボックスに、複数行の「<span class="wintitle">Notes</span>」フィールドを追加しました。 </p> <p>ランキングルールのメモは、<span class="wintitle">Define Ranking Rules</span> ページに表示されます。ルールグループのメモは、定義の編集時に表示されます。 </p> <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local">ランキングルールについて</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ビジネスルール </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637-->ランディングページのサポートを改善しました。ビジネスルールで新しい「<span class="uicontrol">Remove All Results</span>」オプションを使用して自然検索の結果を削除できるようになりました。 </p> <p>この新しいオプションを、他のビジネスルールのアクションと組み合わせて使用し、「定型化されたランディングページ」を作成します。つまり、ビジネスルールのアクションだけを使用してページのコンテンツを作成する場合は、「自然」検索の結果を破棄する必要があります。 </p> <p><a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local">新しいビジネスルールの追加</a>または<a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local">ビジネスルールの編集</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バナーおよびビジネスルール </p> </td> 
   <td colname="col2"> <p> サポートのオプションを追加し、バナーを参照しているビジネスルールがライブにプッシュされたとき、バナーをライブにプッシュすることを条件付きで解除できるようにしました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* [!DNL Stage] インデックスがある場合、ビジネスルールの動作に一貫性がなくなる問題を修正しました。
* 自動ランキングルールが、定型化されたランディングページに適用されるようになりました。

   [ランキングルールの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)のオプションの表を参照してください。

* [!DNL promosearch.cgi] がプロモーションを返さなかった問題を修正しました。

   [検索について](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)を参照してください。

* 多数のバナーを参照したプッシュルールが失敗する場合がある問題を修正しました。

   [バナーについて](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA)を参照してください。

* **[!UICONTROL Did You Mean]** 検索クエリのキャッシュが無効になりました。

   [「Did You Mean」について](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)を参照してください。

