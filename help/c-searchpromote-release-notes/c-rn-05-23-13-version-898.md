---
description: Search&amp;Promote 8.9.8リリースノート。
solution: Target
title: Search&amp;Promote 8.9.8リリースノート（2013年5月24日）
topic: Release Notes,Site search and merchandising
uuid: ff4bfc53-1d0e-4b7d-83ad-54c81d3f9769
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 55%

---


# Search&amp;Promote8.9.8リリースノート（2013年5月24日）{#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>新機能 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 共通フレーズ - 完全一致のサポート </p> </td> 
   <td colname="col2"> <p> 共通フレーズには、「boot cut」や「tank top」など、個別の部分ではなく、全体として検索される2語以上の語句が含まれます。 共通フレーズには、それぞれ個別の語とは異なる独自の意味があります。 </p> <p> 貴社のビジネスに関連する共通フレーズのディクショナリをお客様がメンテナンスします。複数の語を含む検索クエリを実行すると、ディクショナリに対して完全に一致するかを調べる検索が実行されます。 </p> <p>共通フレーズは、追加、編集または削除できます。また、ドメインディクショナリと同様に、共通フレーズをグループ化することもできます。例えば、アパレル、布地、ジュエリー、サイズ、ショッピング、一般というグループで、共通フレーズをグループ化できます。 </p> <p><a href="../c-about-linguistics-menu/c-about-common-phrases.md#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">共通フレーズについて</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点および改良点**

* バックエンド検索CGIパラメータ`sp_date_range_#`は、ユーザ定義フィールドに対しては動作しませんでした。

   [バックエンド検索のCGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)を参照してください。

* **[!UICONTROL History]**&#x200B;バージョンを元に戻しても、URL入力ポイントフィールドの内容が更新されませんでした。

   [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   [URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)も参照してください。

* JSON エンコーディングで、誤ってエンコードされた文字に対処されませんでした。
* ステージングされたインデックスをリモートからプッシュして有効にするためのサポートを追加しました。

   [インデックス作成のためのリモートコントロールについて](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)を参照してください。

