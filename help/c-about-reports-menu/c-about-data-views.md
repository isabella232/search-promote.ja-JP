---
description: 「データ・ビュー」に、検索結果とメタ・フィールドが表示されます。 各列はメタフィールドで、各行は検索クエリの結果です。 列の選択と並べ替えを行って、データビューをカスタマイズします。 データビューには、カスタムのタイトルや説明を含めることもできます。
seo-description: 「データ・ビュー」に、検索結果とメタ・フィールドが表示されます。 各列はメタフィールドで、各行は検索クエリの結果です。 列の選択と並べ替えを行って、データビューをカスタマイズします。 データビューには、カスタムのタイトルや説明を含めることもできます。
seo-title: データビューについて
solution: Target
title: データビューについて
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5

---


# データビューについて{#about-data-views}

「データ・ビュー」に、検索結果とメタ・フィールドが表示されます。 各列はメタフィールドで、各行は検索クエリの結果です。 列の選択と並べ替えを行って、データビューをカスタマイズします。 データビューには、カスタムのタイトルや説明を含めることもできます。

## データビューの使用 {#concept_DCA897D074464BC1861AA47B40CC86C3}

各アカウントには、複数のデータビューを作成する便利な機能があります。 データビューページを使用して、これらのデータビューを作成および編集します。

データビューを追加した後は、編集してビューを設定およびカスタマイズする必要があります。

詳しくは、 [データビューの編集を参照してくださ](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)い。

既存のデータビューをコピーして、新しいデータビューを作成する際の基本として使用できます。

データビ [ューのコピーを参照してください](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF)。

## データビューの追加 {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

ページにデータビューを追加して、各 [!DNL Data Views] メタフィールドの値を検索クエリで表示することができます。

データビューを追加した後は、編集してビューを設定およびカスタマイズする必要があります。

詳しくは、 [データビューの編集を参照してくださ](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)い。

**データビューを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Reports]** クしま **[!UICONTROL Data Views]**&#x200B;す。
1. ページ上で、 [!DNL Data Views] をクリックしま **[!UICONTROL Add New Data View]**&#x200B;す。
1. ダイアログ [!DNL Add New Data View] ボックスのフィー [!DNL Title] ルドに、作成するデータビューの名前を入力します。
1. クリック **[!UICONTROL Add]**.

## データビューの編集 {#task_258A367896C24DD498C755925EA8F516}

ページにデータビューを追加する場合は、「編集」を使用し [!DNL Data Views] て、データビューの名前と説明を変更したり、各メタフィールドの表示を移動、表示または非表示にしたりします。

また、選択したデータビューをロックまたはロック解除することもできます。

詳しくは、 [データビューの追加を参照してくださ](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D)い。

**データビューを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Reports]** クしま **[!UICONTROL Data Views]**&#x200B;す。
1. ページ [!DNL Data Views] の表の列で、 [!DNL Actions] 変更するデー **[!UICONTROL Edit]** タビューのある行をクリックします。
1. ページで、 [!DNL Data Views Editor] 必要なオプションを設定します。

   データビューエディターには、フィールド列の非表示、表示、移動をデータビューページで行うためのすべてのコントロールが用意されています。

   データビューを表示すると、編集できない次の列フィールドも表示されます。ランキング、関連性、スコア（全体）を参照してください。 これらの3つの特別なフィールドは、各結果の関連度スコア、ランクスコア、および全体的なスコアを表します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>タイトル </p> </td> 
      <td colname="col2"> <p>データビューの名前。 データビューを表示すると、名前が右上に表示されます。 </p> <p>詳しくは、 <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> データビューの表示を参照してください</a>。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>説明 </p> </td> 
      <td colname="col2"> <p>（オプション）データビューの説明が含まれます。 説明は、データビューのタイトル名と「新規検索」テキストフィールドの間 <span class="wintitle"> に表示され</span> ます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索パラメータ </p> </td> 
      <td colname="col2"> <p>デフォルトの検索パラメータを指定できます。 データビューを初めて表示すると、これらのCGIパラメーターが自動的に追加されます。 </p> <p>sp_csまたは <span class="codeph"> sp_fは変更または削除しな</span> いでください <span class="codeph"></span>。 これらのパラメーターは、アカウントで推奨される文字セットに関係なく、データビューに不可欠です。 </p> <p>バックエンド <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 検索のCGIパラメーターを参照してくださ</a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ロックの状態 </p> </td> 
      <td colname="col2"> <p>データ表示をロックまたはロック解除できます。 </p> <p>ロックされたデータ表示は、パスワードとユーザー名でのみ表示できます。 ユーザーは、アカウントの現在のメンバーである必要があります。 </p> <p>ロック解除されたデータ表示には、パスワードやユーザーアカウントなしでアクセスできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Order </p> </td> 
      <td colname="col2"> <p> 「順序」テキストボックスの数値を編集して、列の順序を変 <span class="wintitle"> 更でき</span> ます。 行をドラッグ&amp;ドロップして、列の順序を変更することもできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p> 列の表示をオンまたはオフにできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列の検索結果がURLを返す場合は、サムネールと画像をこの列に表示します。 </p> <p>URLは、イメージタグのsrc属性の値になる前に、スキーム名またはプロトコ <span class="codeph"> ルから</span> 削除されます。 </p> <p>検索結果が画像のURLに似ていない場合は、が表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>データビューで結果として表示される文字数を設定します。 </p> <p>デフォルトは100文字です。 </p> <p>ランクスコアや日付フィールドなど、一部のフィールドには、調整可能なフィールド長がありません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## データビューのコピー {#task_78D4C2799BC84677843ED4CA1CD205AF}

ページ上の既存のデータビューをコピーして、 [!DNL Data Views] 新しいデータビューを作成する際の基本として使用することができます。

データビューをコピーした後、ビューを編集してさらにカスタマイズできます。

詳しくは、 [データビューの編集を参照してくださ](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)い。

**データビューをコピーするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Reports]** クしま **[!UICONTROL Data Views]**&#x200B;す。
1. ページ [!DNL Data Views] の表の列で、 [!DNL Actions] コピーするデ **[!UICONTROL Copy]** ータビューの行をクリックします。
1. ページ [!DNL Copy Data View] のテキストフ [!DNL New Title] ィールドに、データビューを割り当てる新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## データビューの削除 {#task_61C32F8F00A549A5A3E7EDDA6F537098}

不要になったページ上のデータビ [!DNL Data Views] ューや使用しなくなったデータビューは削除できます。

**データビューを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Reports]** クしま **[!UICONTROL Data Views]**&#x200B;す。
1. ページ [!DNL Data Views] のテーブルの [!DNL Actions] 列で、削除するデ **[!UICONTROL Delete]** ータビューのある行をクリックします。
1. ページで、「 [!DNL Delete Data View] 削除」をクリッ **クします**。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## データビューの表示 {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

ページ上でを使 [!DNL View] 用して、選 [!DNL Data Views] 択したデータビューを表示できます。

選択したデータビューが別のブラウザウィンドウで開きます。

**データビューを表示するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Reports]** クしま **[!UICONTROL Data Views]**&#x200B;す。
1. 次のいずれかの操作を行います。

   * ページ [!DNL Data Views] の表の列で、 [!DNL Title] 開くデータビューの名前をクリックします。

   * ページ [!DNL Data Views] の表の列で、 [!DNL Actions] 開くデータビ **[!UICONTROL View]** ューのある行をクリックします。

