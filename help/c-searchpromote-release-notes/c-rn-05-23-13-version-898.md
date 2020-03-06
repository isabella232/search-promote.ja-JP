---
description: 'null'
seo-description: 'null'
seo-title: Search&Promote 8.9.8リリースノート（2013年5月24日）
solution: Target
title: Search&Promote 8.9.8リリースノート（2013年5月24日）
topic: Release Notes,Site search and merchandising
uuid: ff4bfc53-1d0e-4b7d-83ad-54c81d3f9769
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.8 Release Notes (05/23/2013){#search-promote-release-notes}

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
   <td colname="col2"> <p> 共通フレーズには、「boot cut」や「tank top」など、全体として検索される複数の単語の用語が含まれ、別々の部分としては検索されません。 共通フレーズには、それぞれ個別の語とは異なる独自の意味があります。 </p> <p> 貴社のビジネスに関連する共通フレーズのディクショナリをお客様がメンテナンスします。複数の語を含む検索クエリを実行すると、ディクショナリに対して完全に一致するかを調べる検索が実行されます。 </p> <p>共通フレーズは、追加、編集または削除できます。また、ドメインディクショナリと同様に、共通フレーズをグループ化することもできます。例えば、アパレル、布地、ジュエリー、サイズ、ショッピング、一般というグループで、共通フレーズをグループ化できます。 </p> <p>一般的なフレ <a href="../c-about-linguistics-menu/c-about-common-phrases.md#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local"> ーズについてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点および改良点**

* The backend search CGI parameter `sp_date_range_#` did not work for user-defined fields.

   バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。

* Reverting **[!UICONTROL History]** version did not update the URL entrypoints field content.

   詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   URL入力ポイントにつ [いても参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

* JSON エンコーディングで、誤ってエンコードされた文字に対処されませんでした。
* ステージングされたインデックスをリモートからプッシュして有効にするためのサポートを追加しました。

   About Remote Control for Indexingを参照し [てください](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)。

