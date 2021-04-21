---
description: クエリクリーニング規則を使用して、入力クエリを分析および変更します。
solution: Target
title: クエリクリーニングルールについて
topic-legacy: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
exl-id: 22ebca58-7687-4c8c-9ac1-bacb321065f3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 1%

---

# クエリクリーニング規則について{#about-query-cleaning-rules}

クエリクリーニング規則を使用して、入力クエリを分析および変更します。

## クエリクリーニング規則の使用{#concept_17F3CDDC3C8A4128AF092A82B777B86C}

この機能は、サイト検索/マーチャンダイジングの動作を変更する場合によく使用されます。 例えば、空白検索を「*」検索ではなく人気のあるキーワードに変更すると、人気のある製品が販促されるようにできます。 また、クエリクリーニングルールを使用して、URLにリダイレクトするダイレクトヒットを実行することもできます。 これは、訪問者が製品のSKUを検索していることを検出し、検索をスキップしてその製品のページにリダイレクトしたい場合に特に便利です。 クエリクリーニングでは、クエリを掘り下げて、後の処理フローステップで使用できるカスタム変数を設定することもできます。 クエリクリーニングルールは、クエリ毎に順に実行される。 ルールの順序を変更するには、ドラッグ&amp;ドロップを使用します。 実際の注文は、保存するまで変更されません。

クエリクリーニングモジュール内のクエリクリーニングルールを調べて、クエリパラメータのいずれかを変更する必要があるか、カスタム変数を設定する必要があるかを判断します。 各クエリクリーニングルールは、2つの主要な要素で構成されています。ルールのアクションとオプションの条件。 指定できるルールと条件の数に制限はありません。 サイト検索/マーチャンダイジングはルールセットのルールをルールごとにループ処理するので、これらのルールの順序は重要です。 ルールの条件が一致する場合は、関連するすべてのアクションが実行されます。

クエリのクリーニングが完了した後、結果のCGIパラメーターが今後使用されます。 設定されたカスタム変数は、処理フローの後の段階で使用できます。 デフォルトでは、クエリ用語の先頭と末尾の空白が自動的に削除されます。

## クエリクリーニング条件について{#section_BF6F25F94FED4DDEA8600D921EA43A66}

条件はオプションです。 すべてのクエリに対してアクションを指定すると、常にアクションが実行されます。 条件は、以前のルールで設定された任意のCGIクエリパラメーター、既存のcookie、またはカスタム変数に基づくことができます。 最初のクエリクリーニングルールは、すべてのクエリで実行され、使用するすべてのカスタム変数を定義し初期化する「ベストプラクティス」と見なされます。

## クエリクリーニング操作について{#section_78F74A9B48DE484191CDA95F5B4E7154}

一致する条件を持つクエリクリーニングルール内のすべてのアクションが実行されます。 通常、アクションは、操作、操作を実行するデータ、および使用する値で構成されます。

[クエリクリーニングルールの追加](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)のオプションの表を参照してください。

## リダイレクトについて{#section_597481E6194440C0A7B9E6FC901A81C0}

ダイレクトヒットインターフェイスを使用すると、受信クエリ用語に基づいてリダイレクトのセットを定義できます。 クエリクリーニング内のリダイレクトは、この考え方を拡張します。 ただし、条件を指定してリダイレクトが行われるタイミングを細かく指定し、リダイレクトによって静的URLではなく動的URLにリダイレクトできます。 リダイレクトアクションを選択すると、行が更新され、リダイレクト先のURLを指定するテキストボックスが表示されます。 URLでは、重複の中括弧で囲んで、置換する変数またはパラメーターを指定できます。 カスタム変数は、置換時のCGIパラメータよりも優先されます。

## 例 {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Webサイトを持つ衣料品店があるとします。 ユーザーが検索語句を一切含めずに「検索」をクリックした場合は、ジーンズに対する検索を返したいとします。これは、国際的に知られているものなのです。 また、性別のクエリ用語を解析して、性別ごとに異なる表示テンプレートを使用するカスタム変数に基づいて、後で検索前のルールを作成できるようにする必要もあります。

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

MegaElectronicは大規模なエレクトロニクス・ストアです。 MegaElectronicは、検索データを分析した結果、優秀な顧客の多くが製品のSKUを使用して製品を検索し、単一の製品の検索結果を返すのではなく、そのSKUに関連付けられたWebページにリダイレクトしたいと考えていました。

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## クエリクリーニング規則の追加{#task_47F43988D3D9485F8AE1DFDA7E00BF54}

顧客からの入力検索クエリをクリーンアップまたは編集するルールを定義できます。

現在存在するテンプレートのみを選択できます。 テンプレートがない場合は、まずテンプレートを定義する必要があります。

[テンプレートについて](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)を参照してください。

**クエリ消去ルールを追加するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Query Cleaning]**&#x200B;をクリックします。
1. [!DNL Query Cleaning Rules]ページで、**[!UICONTROL Add New Rule]**&#x200B;をクリックします。
1. [!DNL Name]フィールドに、新しいクエリクリーニング規則の名前を入力します。
1. [!DNL Add Query Cleaning Rule]ページで、ドロップダウンリストとテキストフィールドを使用してクエリを作成します。

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
      <td colname="col2"> <p>HTTP cookie。 ドメインに関連付けられているcookieに基づいて条件を定義できます。 または、送信検索結果で書き込まれるcookieを設定できます。 Cookieの名前と値は、Uniform Resource Identifierをエンコードする必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>カスタム変数 </p> </td> 
      <td colname="col2"> <p>ユーザー定義の変数。 追加ユーザー定義変数の数に制限はありません。 ここでは、事前検索ルールおよび検索後ルール内のユーザ定義変数を参照できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>システム変数 </p> </td> 
      <td colname="col2"> <p>チェックできる内部システムによって設定された読み取り専用の変数。 次のシステム変数がサポートされています。 </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname </span> <p>サーバーホストの名前。 </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>クエリ文字列を含まない、要求されたURI。 </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>クエリ文字列全体。 </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> 環境 </span> <p>"ステージ"または"ライブ"。どちらを指定するかは、着信クエリがステージング環境に送信されたか、ライブに送信されたかによって異なります。 </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>顧客の送信元のURL。 </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> ユーザーエージェント  </span> <p>顧客のブラウザーの「user-agent」文字列。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>クエリパラメーター </p> </td> 
      <td colname="col2"> <p>クエリに渡されるCGIパラメーター。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>バックエンドパラメータ </p> </td> 
      <td colname="col2"> <p>着信クエリのパラメーターは、最終的に、検索の実行に使用されるバックエンドパラメーターに変換されます。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local">バックエンド検索CGIパラメーター</a>を参照してください。 </p> <p>バックエンドパラメーターは、ナビゲーション要素に表示されません。 その結果、顧客から検索に適用する追加のパラメーターを非表示にできます。 バックエンドパラメーターに対するアクションは遅延バインディングです。つまり、検索が送信される直前に適用されます。 </p> </td> 
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
      <td colname="col1"> <p>格納 </p> </td> 
      <td colname="col2"> <p>検索エンジンは、ホスト名または<span class="codeph"> gs_store </span>クエリパラメーターに基づいて、ユーザーがどのストアにいるかを自動的に検出し、後者の方が優先されます。 店の条件を作ることができます。 クエリクリーニングのみでは、現在のストアを上書きするアクションも使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最後のルール </p> </td> 
      <td colname="col2"> <p>最後のルールセットを持つルールに対して条件が満たされた場合、クエリクリーニング処理モジュールは、一致ルールのアクション後に追加のルールを実行しません。 これは、後のルールが一致するが、後のルールを起動したくないアクションを設定した場合に便利です。 ルールのアクションがリダイレクトを実行する場合、リダイレクトは直ちに行われるので、基本的には最後のルールが設定されたかのように動作します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>停止 </p> </td> 
      <td colname="col2"> <p>ルールの実行をオフにしますが、ルールは削除されません。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## クエリクリーニング規則の編集{#task_FA2FF1A7E2634350AD703485CBC27CB3}

クエリ消去ルールページに追加した既存のクエリ消去ルールを編集できます。

**クエリクリーニングルールを編集するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Query Cleaning]**&#x200B;をクリックします。
1. [!DNL Query Cleaning Rules]ページのテーブルの&#x200B;**[!UICONTROL Actions]**&#x200B;列の下で、編集する関連ルールの&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Query Cleaning Rule]ページで、ドロップダウンリストとテキストフィールドを使用してクエリを作成します。

   「[クエリクリーニングルールの追加](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## クエリクリーニング規則{#task_C52D17226B824590B087CAB6970CBB01}の削除

不要になった、または使用しなくなったクエリ消去ルールは削除できます。

ルールを削除すると、残りのルールが実行される順序が、削除を考慮して自動的に調整されます。

**クエリクリーニングルールを削除するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Query Cleaning]**&#x200B;をクリックします。
1. [!DNL Query Cleaning Rules]ページのテーブルの&#x200B;**[!UICONTROL Actions]**&#x200B;列の下で、削除する関連ルールの&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Confirmation]ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## クエリクリーニングルールの実行順序を変更する{#task_C24012C45A4445468A7FD998017388CA}

クエリ消去ルールの順序を変更して、プレゼンテーションテンプレートで実行する順序を変更できます。

クエリクリーニングルールは、定義された順に実行されます。 ルールの順序番号が高いほど、プロセス内で後で実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、[!DNL Query Cleaning Rules]ページのテーブルの順序列に新しい番号を入力します。 ルールのドラッグ&amp;ドロップを使用して、ルールの実行順序を変更することもできます。

**クエリクリーニングルールの実行順序を変更するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Query Cleaning]**&#x200B;をクリックします。
1. [!DNL Query Cleaning Rules]ページで、次のいずれかの操作を行います。

   * [!DNL Order]列ヘッダーをクリックして、ルールを昇順または降順に並べ替えます。
   * [!DNL Order]列のクエリクリーニングルール名の左にあるテキストフィールドに、ルールを実行する順序番号を入力します。
   * ルールを実行する位置にテーブル行をドラッグ&amp;ドロップします。 ルールが実行される新しい順序を反映するために、すべての注文番号が更新されます。

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
