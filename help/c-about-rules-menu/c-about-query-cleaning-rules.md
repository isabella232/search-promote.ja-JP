---
description: クエリ消去ルールを使用して、入力クエリを分析および変更します。
seo-description: クエリ消去ルールを使用して、入力クエリを分析および変更します。
seo-title: クエリー・クリーニング・ルールについて
solution: Target
title: クエリー・クリーニング・ルールについて
topic: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# クエリー・クリーニング・ルールについて{#about-query-cleaning-rules}

クエリ消去ルールを使用して、入力クエリを分析および変更します。

## クエリ消去ルールの使用 {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

この機能は、サイト検索/マーチャンダイジングの動作を変更する場合によく使用されます。 例えば、空白の検索を「*」検索の代わりに人気のあるキーワードに変更して、人気のある製品を促進することができます。 また、クエリ消去ルールを使用して、URLにリダイレクトするダイレクトヒットを実行することもできます。 これは、誰かが製品SKUを検索していることを検出し、検索をスキップしてその製品のページにリダイレクトする場合に特に便利です。 クエリクリーニングでは、クエリを掘り下げ、後の処理フロー手順で使用できるカスタム変数を設定することもできます。 クエリクリーニングルールは、クエリごとに順に実行されます。 ルールの順序を変更するには、ドラッグ&amp;ドロップを使用します。 実際の注文は、保存するまで変更されません。

クエリクリーニングモジュール内のクエリクリーニングルールを調べ、クエリパラメータのいずれかを変更する必要があるか、カスタム変数を設定する必要があるかを判断します。 各クエリ消去ルールは、2つの主要な要素で構成されます。ルールのアクションとオプションの条件。 指定できるルールと条件の数に制限はありません。 サイト検索/マーチャンダイジングがルール別のルールセットルールをループ処理するので、これらのルールの順序は重要です。 ルールの条件が一致すると、関連付けられたすべてのアクションが実行されます。

クエリのクリーニングが完了すると、結果のCGIパラメータが今後も使用されます。 設定されたカスタム変数は、処理フローの後の段階で使用できます。 デフォルトでは、クエリー用語の先頭と末尾の空白が自動的に削除されます。

## クエリーのクリーニング条件について {#section_BF6F25F94FED4DDEA8600D921EA43A66}

条件はオプションです。 すべてのクエリに対してアクションを指定すると、常にアクションが実行されます。 条件は、CGIクエリパラメーター、既存のcookie、または以前のルールで設定されたカスタム変数に基づくことができます。 最初のクエリクリーニングルールを実行する場合は、「ベストプラクティス」と見なされ、使用するすべてのカスタム変数を定義し初期化します。

## クエリーのクリーニング・アクションについて {#section_78F74A9B48DE484191CDA95F5B4E7154}

一致する条件を持つクエリ消去ルール内のすべてのアクションが実行されます。 通常、アクションは、操作、操作を実行するデータ、および使用する値で構成されます。

クエリ消去ルールの追加のオプシ [ョンの表を参照してください](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)。

## リダイレクトについて {#section_597481E6194440C0A7B9E6FC901A81C0}

ダイレクトヒットインターフェイスを使用すると、受信クエリ用語に基づいてリダイレクトのセットを定義できます。 「クエリのクリーニング」内のリダイレクトは、この考え方を拡張します。 ただし、リダイレクトでは、条件を指定することで、リダイレクトが実行されるタイミングをより細かく設定でき、静的URLではなく動的URLにリダイレクトできます。 リダイレクトアクションを選択すると、行が更新され、リダイレクト先のURLを指定するテキストボックスが表示されます。 URLでは、二重中括弧で囲んで、置き換える変数またはパラメーターを指定できます。 カスタム変数は、置換時のCGIパラメータよりも優先されます。

## 例 {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Webサイトを持つ衣料品店があるとします。 検索語句なしで検索をクリックした場合は、ジーンズに対する検索を返す必要があります。これは、国際的に知られている検索キーワードです。 また、性別ごとに異なるプレゼンテーションテンプレートを使用するカスタム変数に基づいて、後で検索前のルールを作成できるように、性別のクエリ用語を解析する必要もあります。

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

MegaElectronicは大規模なエレクトロニクスストアです。 MegaElectronic社は、検索データの分析から、熟練した顧客の多くが製品のSKUを使用して製品を検索し、単一の製品の検索結果を返すのではなく、そのSKUに関連付けられたWebページにリダイレクトすることに気づきました。

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## クエリ消去ルールの追加 {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

顧客からの入力検索クエリをクリーンアップまたは編集するルールを定義できます。

選択できるのは、現在存在するテンプレートのみです。 テンプレートがない場合は、まず定義する必要があります。

テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)い。

**クエリ消去ルールを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Query Cleaning]**&#x200B;す。
1. ページ上で、 [!DNL Query Cleaning Rules] をクリックしま **[!UICONTROL Add New Rule]**&#x200B;す。
1. 新しいク [!DNL Name] エリ消去ルールの名前をフィールドに入力します。
1. ページ上 [!DNL Add Query Cleaning Rule] で、コンボボックスとテキストフィールドを使用してクエリを作成します。

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
      <td colname="col2"> <p>HTTP cookie。 ドメインに関連付けられたcookieに基づいて条件を定義できます。 または、送信検索結果と共に書き込まれるcookieを設定できます。 Cookieの名前と値は、Uniform Resource Identifierエンコードが必要です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>カスタム変数 </p> </td> 
      <td colname="col2"> <p>ユーザー定義の変数。 ユーザー定義変数の追加、削除、設定は無制限です。 「検索前のルール」と「検索後のルール」内で、任意のユーザ定義変数を参照できます。 </p> </td> 
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
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> ユーザーエージェント </span> <p>顧客のブラウザーの「user-agent」文字列。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>クエリパラメーター </p> </td> 
      <td colname="col2"> <p>クエリに渡されるCGIパラメータ。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>バックエンドパラメータ </p> </td> 
      <td colname="col2"> <p>着信クエリパラメーターは、最終的に、検索の実行に使用されるバックエンドパラメーターに変換されます。 </p> <p>バックエンド <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 検索のCGIパラメーターを参照してくだ </a>さい。 </p> <p>バックエンドパラメーターは、ナビゲーション要素に表示されません。 その結果、検索に適用する追加のパラメーターを顧客から非表示にすることができます。 バックエンドパラメーターに対するアクションは遅延バインディングです。つまり、検索が送信される直前に適用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセット </p> </td> 
      <td colname="col2"> <p>特定のファセットに関連付けられた特殊なCGIパラメーター。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ランク </p> </td> 
      <td colname="col2"> <p>検索に使用するランキングルールを指定できます。 このオプションは、一部のランキングフィールドとランキングルールが定義されている場合にのみ表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ストア </p> </td> 
      <td colname="col2"> <p>検索エンジンは、ホスト名または <span class="codeph"> gs_storeクエリパラメータに基づいて、ユーザがどのストアにいるかを自動的に検出し、 </span> 後者の方が優先されます。 店の条件を作れる。 クエリクリーニングのみでは、アクションを使用して現在のストアを上書きすることもできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最後のルール </p> </td> 
      <td colname="col2"> <p>前回のルールセットを持つルールに対して条件が満たされた場合、クエリクリーニング処理モジュールは、照合ルールのアクションの後に追加のルールを実行しません。 これは、後のルールが一致するが、後のルールを実行したくないアクションを設定した場合に便利です。 ルールのアクションがリダイレクトを実行する場合、リダイレクトは直ちに行われるので、基本的には最後のルールが設定された場合と同じ働きをします。 </p> </td> 
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

## クエリ消去ルールの編集 {#task_FA2FF1A7E2634350AD703485CBC27CB3}

[クエリクリーニングルール]ページに追加した既存のクエリクリーニングルールを編集できます。

**クエリ消去ルールを編集するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Query Cleaning]**&#x200B;す。
1. ページ [!DNL Query Cleaning Rules] の表の列の下 **[!UICONTROL Actions]** で、編集する関連 **[!UICONTROL Edit]** 付けられたルールをクリックします。
1. ページ上 [!DNL Edit Query Cleaning Rule] で、コンボボックスとテキストフィールドを使用してクエリを作成します。

   「クエリ消去ルールの追加」のオ [プションの表を参照してください](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## クエリ消去ルールの削除 {#task_C52D17226B824590B087CAB6970CBB01}

不要になったクエリ消去ルールを削除したり、使用したりできます。

ルールを削除すると、残りのルールが実行される順序が、削除に合わせて自動的に調整されます。

**クエリ消去ルールを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Query Cleaning]**&#x200B;す。
1. ページ [!DNL Query Cleaning Rules] の表の列の下 **[!UICONTROL Actions]** で、削除する関連 **[!UICONTROL Delete]** 付けられたルールをクリックします。
1. ダイアログボッ [!DNL Confirmation] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## クエリ消去ルールの実行順序の変更 {#task_C24012C45A4445468A7FD998017388CA}

クエリ消去ルールの順序を変更して、プレゼンテーションテンプレートで実行する順序を変更できます。

クエリ消去ルールは、定義された順序で実行されます。 ルールの順序番号が大きいほど、プロセスで後から実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、ページ上のテーブルの「順序」列に新しい番号を入力 [!DNL Query Cleaning Rules] します。 ルールのドラッグ&amp;ドロップを使用して、ルールの実行順序を変更することもできます。

**クエリ消去ルールの実行順序を変更するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Rules]** クしま **[!UICONTROL Query Cleaning]**&#x200B;す。
1. ページで、 [!DNL Query Cleaning Rules] 次のいずれかの操作を行います。

   * Click the [!DNL Order] column header to sort the rules in ascending or descending order.
   * クエリ [!DNL Order] 消去ルール名の左側のテキストフィールドに、ルールを実行する順序番号を入力します。
   * ルールを実行する位置にテーブル行をドラッグ&amp;ドロップします。 すべての注文番号が更新され、ルールが実行される新しい順序が反映されます。

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

