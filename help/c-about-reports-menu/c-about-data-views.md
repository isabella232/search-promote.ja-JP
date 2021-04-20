---
description: データ表示には、検索結果とメタフィールドが表示されます。 各列はメタフィールドで、各行は検索クエリの結果です。 列の選択と並べ替えを行って、データ表示をカスタマイズします。 データ表示には、カスタムのタイトルと説明を付けることもできます。
solution: Target
title: データ表示について
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 1%

---


# データ表示について{#about-data-views}

データ表示には、検索結果とメタフィールドが表示されます。 各列はメタフィールドで、各行は検索クエリの結果です。 列の選択と並べ替えを行って、データ表示をカスタマイズします。 データ表示には、カスタムのタイトルと説明を付けることもできます。

## データ表示の使用{#concept_DCA897D074464BC1861AA47B40CC86C3}

各アカウントでは、複数のデータ表示を作成する便利性があります。 データ表示ページを使用して、これらのデータ表示を作成および編集します。

データ表示を追加した後は、その表示を編集して設定およびカスタマイズする必要があります。

「[データ表示の編集](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)」を参照してください。

既存のデータ表示をコピーして、新しいデータ表示を作成する際の基本として使用できます。

「[データ表示のコピー](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF)」を参照してください。

## データ表示の追加{#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

[!DNL Data Views]ページにデータ表示を追加して、各メタフィールドの値を検索クエリと共に表示できます。

データ表示を追加した後は、その表示を編集して設定およびカスタマイズする必要があります。

「[データ表示の編集](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)」を参照してください。

**データ表示を追加するには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Data Views]**&#x200B;をクリックします。
1. [!DNL Data Views]ページで、**[!UICONTROL Add New Data View]**&#x200B;をクリックします。
1. [!DNL Add New Data View]ダイアログボックスの[!DNL Title]フィールドに、作成するデータ表示の名前を入力します。
1. クリック **[!UICONTROL Add]**.

## データ表示の編集{#task_258A367896C24DD498C755925EA8F516}

データ表示を[!DNL Data Views]ページに追加する場合は、「編集」を使用して、データ表示の名前と説明を変更したり、各メタフィールドの表示を移動、表示または非表示にしたりします。

また、選択したデータ表示をロックまたはロック解除することもできます。

「[データ表示の追加](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D)」を参照してください。

**データ表示を編集するには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Data Views]**&#x200B;をクリックします。
1. [!DNL Data Views]ページのテーブルの[!DNL Actions]列で、変更するデータ表示の行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Data Views Editor]ページで、必要なオプションを設定します。

   データ表示エディターには、データ表示ページのフィールド列の非表示、表示、移動を行うためのすべてのコントロールがあります。

   データ表示を表示すると、結果の表に、編集できない次の列フィールドも表示されます。ランキング、関連性、スコア（全体）。 これらの3つの特別なフィールドは、各結果の関連度スコア、ランクスコア、および全体的なスコアを表します。

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
      <td colname="col2"> <p>データ表示の名前。 名前は、データ表示を表示すると右上に表示されます。 </p> <p>「<a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local">データ表示の表示</a>」を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>説明 </p> </td> 
      <td colname="col2"> <p>（オプション）データ表示の説明が含まれます。 この説明は、データ表示のタイトル名と「<span class="wintitle">新規検索</span>」テキストフィールドの間に表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索パラメータ </p> </td> 
      <td colname="col2"> <p>初期設定の検索パラメーターを指定できます。 データ表示が初めて表示されるときは、これらのCGIパラメーターが自動的に追加されます。 </p> <p><span class="codeph"> sp_cs</span>や<span class="codeph"> sp_f</span>は変更または削除しないでください。 これらのパラメーターは、アカウントで推奨される文字セットに関係なく、データ表示に不可欠です。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local">バックエンド検索のCGIパラメーター</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ロック状態 </p> </td> 
      <td colname="col2"> <p>データ表示をロックまたはロック解除できます。 </p> <p>ロックされたデータ表示は、パスワードとユーザー名を使用してのみ表示できます。 ユーザーは、アカウントの現在のメンバーである必要があります。 </p> <p>ロック解除されたデータ表示には、パスワードやユーザーアカウントを使用せずにアクセスできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Order </p> </td> 
      <td colname="col2"> <p> 「<span class="wintitle">順序</span>」テキストボックスの数値を編集して、列の順序を変更できます。 行をドラッグ&amp;ドロップして列の順序を変更することもできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>以下を含む </p> </td> 
      <td colname="col2"> <p> 列の表示/非表示を切り替えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLを画像として表示 </p> </td> 
      <td colname="col2"> <p>この列の検索結果がURLを返す場合は、この列にサムネールと画像を表示します。 </p> <p>イメージタグの<span class="codeph"> src</span>属性の値になる前に、URLはそのスキーム名またはプロトコルを削除します。 </p> <p>再検索結果が画像へのURLに似ていない場合は、が表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールドの長さ </p> </td> 
      <td colname="col2"> <p>データ表示に結果として表示する文字の数を設定します。 </p> <p>デフォルトは100文字です。 </p> <p>ランクスコアや日付フィールドなど、フィールドの長さに調整できないフィールドもあります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## データ表示のコピー{#task_78D4C2799BC84677843ED4CA1CD205AF}

[!DNL Data Views]ページの既存のデータ表示をコピーして、新しいデータ表示を作成する際の基本として使用できます。

データ表示をコピーした後、表示を編集してさらにカスタマイズできます。

「[データ表示の編集](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)」を参照してください。

**データ表示をコピーするには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Data Views]**&#x200B;をクリックします。
1. [!DNL Data Views]ページのテーブルの[!DNL Actions]列で、コピーするデータ表示の行の&#x200B;**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Copy Data View]ページの[!DNL New Title]テキストフィールドに、データ表示を割り当てる新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## データ表示の削除{#task_61C32F8F00A549A5A3E7EDDA6F537098}

不要になった、または使用しなくなったデータ表示は[!DNL Data Views]ページから削除できます。

**データ表示を削除するには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Data Views]**&#x200B;をクリックします。
1. [!DNL Data Views]ページのテーブルの[!DNL Actions]列で、削除するデータ表示の行の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Data View]ページで、「**削除**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## データ表示の表示{#task_FD0D2CE53DF84CBD9220AD7CA920011F}

[!DNL Data Views]ページの[!DNL View]を使用すると、選択したデータ表示を表示できます。

選択したデータ表示が別のブラウザーウィンドウに開きます。

**データ表示を表示するには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Data Views]**&#x200B;をクリックします。
1. 次のいずれかの操作を行います。

   * [!DNL Data Views]ページのテーブルの[!DNL Title]列で、開くデータ表示の名前をクリックします。

   * [!DNL Data Views]ページのテーブルの[!DNL Actions]列で、開くデータ表示の行の&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

