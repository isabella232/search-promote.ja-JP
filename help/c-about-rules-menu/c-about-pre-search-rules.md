---
description: 検索前のルールを使用して、入力クエリを分析し、使用するプレゼンテーションテンプレートを決定します。 検索前のルールは、各クエリに対して順に実行されます。 ルールの順序を変更するには、ドラッグ&ドロップを使用します。 実際の注文は、保存するまで変更されません。
seo-description: 検索前のルールを使用して、入力クエリを分析し、使用するプレゼンテーションテンプレートを決定します。 検索前のルールは、各クエリに対して順に実行されます。 ルールの順序を変更するには、ドラッグ&ドロップを使用します。 実際の注文は、保存するまで変更されません。
seo-title: 検索前のルールについて
solution: Target
title: 検索前のルールについて
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# 検索前のルールについて{#about-pre-search-rules}

検索前のルールを使用して、入力クエリを分析し、使用するプレゼンテーションテンプレートを決定します。 検索前のルールは、各クエリに対して順に実行されます。 ルールの順序を変更するには、ドラッグ&amp;ドロップを使用します。 実際の注文は、保存するまで変更されません。

## 検索前のルールの使用 {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

検索前のルールは、通常、受け取ったクエリに基づいて結果を表示するプレゼンテーションテンプレートを選択するために使用されます。 より高度な機能を使用して、プレゼンテーションテンプレートで行う検索に使用するクエリを変更できます。 必要に応じて、クエリパラメーターの値を追加、削除、または変更できます。 プリサーチ処理モジュールは、入力クエリごとにプリサーチルールを調べ、クエリが変更されたかどうか、およびどのプレゼンテーションテンプレートが使用されているかを判断します。 各検索前ルールは、2つの主要な要素で構成されます。ルールのアクションとオプションの条件。 ルールと条件の数に制限はありません。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールの条件が一致すると、関連付けられたすべてのアクションが実行されます。

事前検索処理モジュールでは、定義済みのすべてのテンプレートと、それに関連する名前付き検索がインスタンス化され、各検索にcgiパラメーターのローカルコピーが与えられます。 その結果、検索で使用するcgiパラメータの1つを追加、削除、または変更して、検索をカスタマイズできます。テンプレートで使用する別の名前付き検索を変更したり、他のテンプレートに影響を与えたりする必要はありません。 その結果、複数の結果セットを表示するプレゼンテーションテンプレートがある場合は、各検索を個別にカスタマイズできます。 各テンプレートの各検索にコピーされる前に、グローバルCGIパラメータに対して変更を行う場合は、クエリクリーニングモジュールを使用します。

## 検索前のルールの条件 {#section_B5568ADEB28546A280720309498B045D}

条件はオプションです。 すべてのクエリに対してアクションを指定する場合は、常にアクションが実行されます。 最初のルールは、デフォルトのプレゼンテーションテンプレートを選択するクエリごとに実行するのがベストプラクティスと考えられます。 この方法を使用すると、入力クエリが何であっても、使用するシナリオプレゼンテーションテンプレートが最悪の場合に選択されていることを確認できます。 条件は、以前のルールで設定されたCGIクエリパラメーター、cookie、またはカスタム変数に基づいて、またはシステム変数に基づくことができます。

## 検索前のルールのアクション {#section_3B8E19D287554C1C969F5B8D81226981}

一致する条件を持つ事前検索ルール内のすべてのアクションが実行されます。 通常、アクションは、操作、操作を実行するデータ、および使用する値で構成されます。 最も簡単なアクションは、クエリが検索前のルールの条件に一致する場合に使用するプレゼンテーションテンプレートを指定することです。 次に、対象のテンプレートをプレゼンテーションテンプレートの名前に設定します。 より複雑なアクションを使用して、テンプレートの検索パラメータに対して操作を実行することで、特定のテンプレートで使用されている検索を変更できます。 テンプレートの検索パラメータに対して操作を実行する場合は、プレゼンテーションテンプレートと検索を指定します。

## 汎用ルール {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

テンプレートの検索パラメータに対して操作を実行する場合、次の2つの特別な値が存在します。*プレゼンテーションテンプレートのターゲットと*プライマリ、および名前付き検索のそれぞれ。 これらの値を使用して、現在のターゲットテンプレートのプライマリ検索に基づいてルールを作成できます。 これらの構成を使用すると、現在のターゲットテンプレートやプライマリ検索が何と呼ばれているかを気にする必要がない、一般的なルールを作成できます。 明らかに、以前の検索前のルールは、現在のターゲットテンプレートが何であるかを定義しています。 それ以外の場合は、最初のプレゼンテーションテンプレートが選択され、望ましくない結果が生じます。

## 例 {#section_EA153A151987454EA44A4A6862466DF6}

デフォルトのテンプレートをguided.tmplに設定します。ユーザーがcgiパラメーターlangを渡したときに、既知の言語に設定し、その言語のテンプレートを使用します。

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## ベストプラクティス {#section_31EBAE5E54174DEE8986CBB636746A98}

* 最初のルールでは、すべてのクエリのデフォルトのテンプレートが選択されます。
* クエリのデータマイニングは、クエリクリーニングルール内で行われます。 これらは、検索前の処理で参照できます。
* 検索前ルールで導入した新しいカスタム変数を、他の検索前ルールが参照する前にすべてのクエリに対して実行される検索前ルールに追加します。

## 新しい検索前ルールの追加 {#task_182B95918462490D8BDA7F16A81CAC11}

を使用して、入力ク [!DNL Pre-Search Rules] エリに基づいて検索結果を表示するために使用するプレゼンテーションテンプレートを選択できます。

**新しい検索前のルールを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Pre-Search Rules]**&#x200B;す。
1. ページ上で、 [!DNL Pre-Search Rules] をクリックしま **[!UICONTROL Add New Rule]**&#x200B;す。
1. 新しいク [!DNL Name] エリ消去ルールの名前をフィールドに入力します。
1. ページ上 [!DNL Add Pre-Search Rule] で、コンボボックスとテキストフィールドを使用してクエリを作成します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>HTTP cookie。 Cookieの名前と値は、Uniform Resource Identifierエンコードが必要です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>カスタム変数 </p> </td> 
      <td colname="col2"> <p>ユーザー定義の変数。 ユーザー定義変数の追加、削除、設定は無制限です。 </p> <p>検索前ルール内のクエリ消去モジュールで定義した変数を参照できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>システム変数 </p> </td> 
      <td colname="col2"> <p>チェック可能な内部システムによって設定された読み取り専用変数。 次のシステム変数がサポートされています。 </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname </span> <p>サーバーホストの名前。 </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>クエリ文字列を含まない、要求されたURI。 </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>クエリ文字列全体。 </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> 環境 </span> <p>受信クエリがステージング環境に送信されたか、実稼働環境に送信されたかに応じて、「ステージ」または「ライブ」。 </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>顧客のURL。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセット </p> </td> 
      <td colname="col2"> <p>特定のファセットに関連付けられている、グローバルコレクション内の特殊なCGIパラメーター。 すべてのCGIパラメーターは、クエリクリーニングの後、テンプレート内の各名前付き検索にコピーされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>クエリパラメーター </p> </td> 
      <td colname="col2"> <p>グローバルコレクション内のCGIパラメーター。 これらのパラメーターは、クエリーのクリーニング後、テンプレート内の各名前付き検索にコピーされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テンプレートの検索パラメータ </p> </td> 
      <td colname="col2"> <p>プレゼンテーションテンプレートに関連付けられた名前付き検索に対してローカルなCGIパラメーター。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テンプレートのバックエンドパラメータ </p> </td> 
      <td colname="col2"> <p>着信クエリパラメーターは、最終的に、検索の実行に使用されるバックエンドパラメーターに変換されます。 </p> <p>バックエンド <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 検索のCGIパラメーターを参照してくだ </a>さい。 </p> <p>バックエンドパラメーターは、ナビゲーション要素に表示されません。 その結果、検索に適用する追加のパラメーターを顧客から非表示にすることができます。 パラメータは、プレゼンテーションテンプレート内の特定の検索に対してローカルです。 バックエンドパラメーターに対するアクションは遅延バインディングです。つまり、検索が送信される直前に適用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ターゲットテンプレート </p> </td> 
      <td colname="col2"> <p>削除できないシステム定義のカスタム変数の特殊なインスタンス。 この変数には、現在のターゲットプレゼンテーションテンプレートが含まれます。 この変数は、カスタム変数「targeted_template」を指定することで読み取りまたは設定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ランク </p> </td> 
      <td colname="col2"> <p>検索に使用するランキングルールを指定できます。 このオプションは、ランキングフィールドとランキングルールを定義した場合にのみ表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ストア </p> </td> 
      <td colname="col2"> <p>検索エンジンは、ホスト名または <span class="codeph"> gs_storeクエリパラメータに基づいて、顧客がどのストアにいるかを自動的に検出し、 </span> 後者の方が優先されます。 店の条件を作れる。 クエリクリーニングのみでは、アクションを使用して現在のストアを上書きすることもできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最後のルール </p> </td> 
      <td colname="col2"> <p>このチェックボックスをオンにすると、検索前処理モジュールは、一致ルールのアクション後に追加のルールを実行しません。 このアクションは、後のルールが一致するが、後のルールを実行したくないアクションを設定した場合に便利です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>停止 </p> </td> 
      <td colname="col2"> <p>ルールの実行をオフにしますが、ルールは削除しません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Editing a pre-search rule {#task_25F77050C5DA42B29DFD1C9718FB8C64}

ページに追加した既存の検索前のルールを編集でき [!DNL Pre-Search Rules] ます。

**検索前のルールを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Pre-Search Rules]**&#x200B;す。
1. ページ [!DNL Pre-Search Rules] の表の列の下 **[!UICONTROL Actions]** で、編集する関連 **[!UICONTROL Edit]** 付けられたルールをクリックします。
1. ページ上 [!DNL Edit Pre-Search Rule] で、コンボボックスとテキストフィールドを使用してクエリを作成します。

   新しい検索前ルールの追加のオ [プションの表を参照してください](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索前のルールの削除 {#task_128B6A79CA6C451C991AEDAD58F51743}

不要になったり使用しなくなったりした事前検索ルールは削除できます。

ルールを削除すると、残りのルールが実行される順序が、削除に合わせて自動的に調整されます。

**検索前のルールを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Pre-Search Rules]**&#x200B;す。
1. ページ [!DNL Pre-Search Rules] の表の列の下 **[!UICONTROL Actions]** で、削除する関連 **[!UICONTROL Delete]** 付けられたルールをクリックします。
1. ダイアログボッ [!DNL Confirmation] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索前ルールの実行順序の変更 {#task_C18817276A3C459089C97448076365D1}

プレゼンテーションテンプレートで実行する順序を変更するには、検索前のルールの順序を変更します。

事前検索ルールは、定義された順序で実行されます。 ルールの順序番号が大きいほど、プロセスで後から実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、ページ上のテーブルの「順序」列に新しい番号を入力 [!DNL Pre-Search Rules] します。 ルールのドラッグ&amp;ドロップを使用して、ルールの実行順序を変更することもできます。

**事前検索ルールの実行順序を変更するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Pre-Search Rules]**&#x200B;す。
1. ページで、 [!DNL Pre-Search Rules] 次のいずれかの操作を行います。

   * Click the **[!UICONTROL Order]** column header to sort the rules in ascending or descending order.
   * 検索前 **[!UICONTROL Order]** ルール名の左側にあるテキストフィールドの列に、ルールを実行する注文番号を入力します。
   * ルールを実行する位置にテーブル行をドラッグ&amp;ドロップします。 すべての注文番号が更新され、ルールが実行される新しい順序が反映されます。

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

