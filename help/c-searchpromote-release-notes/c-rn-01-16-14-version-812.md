---
description: Search&amp;Promote 8.12.0リリースノート。
solution: Target
title: Search&amp;Promote 8.12.0リリースノート（2014年1月17日）
topic-legacy: Release Notes,Site search and merchandising
uuid: 4db10eb4-11bf-4483-a7f2-87981d9c7a50
exl-id: 8ea76d7e-6675-4ba3-8f93-1895476f7017
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 74%

---

# Search&amp;Promote8.12.0リリースノート（2014年1月17日）{#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>新機能および機能強化 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ストリーミングディレクトリの追加 </p> </td> 
   <td colname="col2"> <p> </p> <p> インドネシア語およびトルコ語で、ストリーミングディレクトリが追加されました。 </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" format="dita" scope="local">辞書について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>レポートの書き出し </p> </td> 
   <td colname="col2"> <p> 
     <!--3683368-->次のレポートからデータをCSVに書き出せるようになりました。 
     <ul id="ul_93B619DBB3444F64BD6D7F9E969AB1E1"> 
      <li id="li_96DDE1A196834845A0FA319903C5934B"> <p>「キーワード」レポート </p> </li> 
      <li id="li_4F1A19DE98C84F8CAD963EEA2B38ED7A"> <p>ヌル検索用語レポート </p> </li> 
      <li id="li_A7716C62C4D44CD69D411C3FEE246D96"> <p>検索リクエストレポート </p> </li> 
     </ul> </p> <p>「<a href="../c-about-reports-menu/c-about-reports-menu.md#concept_5F901459C7AB461BAB30B305957EB00C" format="dita" scope="local">レポートメニューについて</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>関連付けの禁止 </p> </td> 
   <td colname="col2"> <p>検索結果で関連付けてはならない 2 つの単語を制御できるようになりました。 </p> <p> <p>注意：この機能は、デフォルトでは有効になっていません。アドビカスタマーケアに問い合わせて、使用している Search&amp;Promote でこの機能をアクティブ化してください。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正点**

* 選択されたファセット条件以外の推奨領域に結果が追加されない問題を修正しました。
* HTTPS のみで検索できるアカウントの結果ベースのルールを保存できない問題を修正しました。
* 「携帯電話でない」のビジネスルールの設定が機能しなかった問題を修正しました。

   [ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

* 在庫のフィルター検索を実行しても結果が返ってこなかった問題を修正しました。
* 「サイズ」ファセットオーダーが更新されていなかった問題を修正しました。
* クエリクリーニングページに「カスタム」ルール定義のオプションが追加されました。

   [クエリクリーニング規則について](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C)を参照してください。

* 十分なデータが含まれていない場合に用語レポートがエントリをレポートしていた問題を修正しました。

   [キーワードレポートまたはNULL検索キーワードレポートの表示を参照してください。](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* 単一のビジネスルールを押すとライブがステージングモードで動作しますが、ライブモードに失敗していた問題を修正しました。
* 「以下を含む」または「以下を除外する」リストのオートコンプリート編集が履歴に保存されず、その結果、元に戻せなかった問題を修正しました。

   [オートコンプリートについて](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578)を参照してください。
