---
description: Search&amp;Promote 8.11.0リリースノート。
solution: Target
title: Search&amp;Promote 8.11.0リリースノート（2013年10月29日）
topic: Release Notes,Site search and merchandising
uuid: 973f9608-a5c7-4571-ae2b-6f1fa05bc862
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 57%

---


# Search&amp;Promote8.11.0リリースノート（2013年10月29日）{#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>新機能 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> デンマーク語の復号化解除ツール </p> </td> 
   <td colname="col2"> <p> <span class="keyword">AdobeSearch&amp;Promote</span>が言語（デンマーク語）の検出、複混合、ステミング、およびAdobeが提供するセグメント化サービスにアクセスできるメカニズムが提供されました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**強化された機能および修正点**

* 既存の[!DNL Search&Promote]テーブル一致機能が強化されました。 この機能強化により、ますます複雑になる SKU と製品データとの関係に関する顧客の要件のさらなるサポートを提供します。

   >[!NOTE]
   >
   >この機能は、デフォルトでは有効になっていません。 アドビカスタマーケアに問い合わせて、使用している Search&amp;Promote でこの機能をアクティブ化してください。

* ガイド付き検索で、アカウントの言語設定を使用してファセットを並べ替えることができるオプションが追加されました。

   >[!NOTE]
   この機能は、デフォルトでは有効になっていません。 アドビカスタマーケアに問い合わせて、使用している Search&amp;Promote でこの機能をアクティブ化してください。

* ユーザーが複数選択ファセットに指定できるファセット値の数を増加するオプションが追加されました。

   >[!NOTE]
   この機能は、デフォルトでは有効になっていません。 アドビカスタマーケアに問い合わせて、使用している Search&amp;Promote でこの機能をアクティブ化してください。

* チェックボックスオプション&#x200B;**[!UICONTROL Only allow searches that use HTTPS]**&#x200B;を&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**&#x200B;に追加しました。

   [制限](../c-about-settings-menu/c-about-searching-menu.md#concept_B5B527E04EBF4E9AB5956EEF881DDBF1)についてを参照してください。

* ウィザードの[!DNL File Submission]パネルでタブ文字を保持するためのオプションを&#x200B;**[!UICONTROL Settings]**/**[!UICONTROL Searching]**/**[!UICONTROL Feeds]**/**[!UICONTROL Create Feed]**/**[!UICONTROL Generic Feed]**&#x200B;に追加しました。

   「[フィードの作成](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250)」を参照してください。

* 新しいファセット定義フォームのトップおよびボトムフィールドで許可されるデータのサイズが増加され、80 文字から 1000 文字になりました。

   [ファセット](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)についてを参照してください。

* ガイド付き検索のデバッグパラメーターで、ビジネスルール番号が正しくレポートされるようになりました。
* ビジネスルールがライブ環境に適用されるようになりました。
* Language = &quot;Danish (Denmark)&quot; に設定したアカウントで、緯度／経度で検索する際に近接検索が機能するようになりました。
* スケジュールが割り当てられていない、結果ベースのトリガーが、発動されるようになりました。
* **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**&#x200B;で&#x200B;**[!UICONTROL Ignore Apostrophes]**&#x200B;オプションを使用した場合に、一貫性のある結果がレポートされるようになりました。

   [単語と言語について](../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79)を参照してください。

* オートコンプリートワードリストユーザーインターフェイスが、大量のファセットで動作するようになりました。

