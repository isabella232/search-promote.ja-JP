---
description: Adobe Analyticsメニューを使用して、Adobe Analytics指標認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。
seo-description: Adobe Analyticsメニューを使用して、Adobe Analytics指標認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。
seo-title: Adobe Analyticsメニューについて
solution: Target
subtopic: Adobe Analytics
title: Adobe Analyticsメニューについて
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '3448'
ht-degree: 1%

---


# Adobe Analyticsメニューについて{#about-the-adobe-analytics-menu}

Adobe Analyticsメニューを使用して、Adobe Analytics指標認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。

## Adobe Analytics指標認証の設定{#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Adobe Analytics指標をサイトの検索/マーチャンダイジングランキングに組み込むには、まずAdobe Analyticsウェブサービスログインを取得する必要があります。 ログイン情報を取得したら、それを使用して、サイト検索/マーチャンダイジングでのAdobe Analytics認証を設定できます。

**Adobe Analytics指標認証を設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Authentication]**&#x200B;をクリックします。
1. [!DNL Setup Adobe Analytics Metrics Authentication]ページで、各フィールドに要求した情報を指定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>テキストフィールド </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics会社名 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsアカウントへのログインに使用するのと同じ会社名設定です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Web サービスユーザー名 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsアカウントに関連付けられているWebサービスユーザ名。 </p> <p>この情報はAdobe Analyticsで入手できます。 Adobe Analyticsのメニューバーで、<span class="uicontrol"> <b>管理者</b> </span> <span class="uicontrol"> <b>Admin Console</b> </span> <span class="uicontrol"> <b>会社</b> </span> &gt; <span class="uicontrol"> <b>をクリックします。webサービス</b> </span>。 この情報は、APIアクセス情報テーブルにあります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Webサービスの共有暗号鍵(Shared Secret) </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsアカウントに関連付けられているWeb Services Shared Secretです。 </p> <p>この情報はAdobe Analyticsで入手できます。 Adobe Analyticsのメニューバーで、<span class="uicontrol"> <b>管理者</b> </span> <span class="uicontrol"> <b>Admin Console</b> </span> <span class="uicontrol"> <b>会社</b> </span> &gt; <span class="uicontrol"> <b>をクリックします。webサービス</b> </span>。 この情報は、APIアクセス情報テーブルにあります。 </p> </td> 
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

## Adobe Analyticsレポートスイートについて{#concept_1A51AEC5D40E459B813E7891D64B1BAE}

サイト検索/マーチャンダイジング内でAdobe Analyticsレポートスイートのデータを使用するには、まず、サイト検索/マーチャンダイジングアカウントでAdobe Analyticsデータのコピーを作成する必要があります。

新しいAdobe Analyticsレポートスイート定義を作成したり、既存のAdobe Analyticsレポートスイートと関連指標を表示または変更したりできます。

サイト検索/マーチャンダイジング内から初めてAdobe Analyticsにアクセスすると、会社が利用できるレポートスイートのリストがダウンロードされ、キャッシュされます。 新しいレポートスイートが最近追加された場合、または既存のレポートスイートが削除された場合は、レポートスイートリストを更新して、レポートスイートのリストを再度ダウンロードできます。

## Adobe Analyticsレポートスイートの追加{#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

サイト検索/マーチャンダイジングのランクルールの基にするAdobe Analyticsレポートスイートを選択できます。

選択できるリストは、Adobe Analyticsアカウント内で使用可能なレポートスイートに対応している必要があります。 選択したレポートスイートによって、サイト検索/マーチャンダイジングのランキングルール内で使用できる指標が決まります。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

Adobe Analyticsレポートスイートを追加した後、その指標を編集できます。

「[レポートスイートのAdobe Analytics指標の編集](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)」を参照してください。

**Adobe Analyticsレポートスイートを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [Adobe Analyticsレポートスイート]ページで[**[!UICONTROL Add Report Suite]**]をクリックします。
1. 新しく追加された表の行のドロップダウンリストで、目的のレポートスイートを選択します。
1. レポートスイートのAdobe Analytics指標を編集します。

## レポートスイートのAdobe Analytics指標の編集{#task_360904CCBBB140238ADA036C3CC07664}

Adobe Analytics指標をサイト検索/マーチャンダイジングのランキングルールに組み込むには、選択したレポートスイートに関連付けられている1つ以上の指標を選択します。 次に、Adobe Analyticsウェブサービスを介して指標データを取得するために使用するオプションを設定します。

「[Adobe Analyticsレポートスイートの追加](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)」を参照してください。

[高度なAdobe Analyticsオプションの設定](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19)を参照してください。

**レポートスイートのAdobe Analytics指標を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Report Suites]ページの&#x200B;**[!UICONTROL Actions]**&#x200B;列の下で、指標を設定するレポートスイートの&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Adobe Analytics Metrics]ページで、必要な指標を設定します。 指標名の横にアスタリスク(*)が表示されない指標はオプションです。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>レポートスイート </p> </td> 
      <td colname="col2"> <p>追加した現在のレポートスイートの名前が表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>レポートスイート表示名 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsレポートスイート名の「エイリアス」名を指定します。 この代替名は、同じレポートスイートが複数の定義で使用されている場合に便利です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>レポートタイプの選択 </p> </td> 
      <td colname="col2"> <p>選択したレポートスイートで使用するレポートタイプの値を指定します。 この値は、結果の各行のキーを示します。 </p> <p>レポートタイプは、Adobe Analytics要素とも呼ばれます。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>相互参照フィールド名 </p> </td> 
      <td colname="col2"> <p>値がレポートスイートのデータの「キー」の検索に使用されるメタデータフィールドを指定します。 </p> <p>値が選択されていない場合（「 — なし — 」）、このレポートスイートのデータはランキングの計算で使用できません（<span class="uicontrol"> <b>ルール</b> </span> &gt; <span class="uicontrol"> <b>ランキングルール</b> &gt; <span class="uicontrol"> <b>ルールの編集&lt;a1）0/&gt; </span>)。</span></b> </p> <p>値を選択すると、このフィールドの値は、先ほど設定した選択したレポートタイプの値を使用して、このレポートスイートのAdobe Analyticsデータとサイト検索/マーチャンダイジングドキュメントとの相互参照に使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索用語レポート </p> </td> 
      <td colname="col2"> <p>ビジネスルールを作成し、<b>ステージAdobe Analyticsデータプレビュー</b>ページから検索用語をシミュレートするためのアクセスを提供します。 </p> <p><a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Adobe Analyticsデータのプレビュー</a>を参照してください。 </p> <p>2つのオプションを含むすべての行にプルダウンメニューが表示されます。<b>検索語句</b>と<b>新しいビジネスルールを作成</b>をシミュレートします。 </p> <p>どちらのオプションも、レポートタイプのデータを検索用語として使用します。 したがって、この機能は、レポートタイプが検索用語を表す場合にのみ意味を持ちます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>指標 </p> </td> 
      <td colname="col2"> <p>サイト検索/マーチャンダイジングのランキングルール内でダウンロードして使用する指標の値を識別します。 </p> <p>ここで設定した指標は、ルール<span class="uicontrol"><b>ルール</b> </span> &gt; <span class="uicontrol"> <b>ランキングルール</b> </span> <span class="uicontrol">ルールの編集</b> </span>メンバーセンターページ（ルール'Sの時点）に表示されます。データタイプは<span class="uicontrol">Adobe Analytics指標（数値） </span>に設定されます。 <b>レポートスイート名またはレポートスイート表示名（指定した場合）と個々の指標名の組み合わせが表示されます。 </b></p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小指標値 </p> </td> 
      <td colname="col2"> <p>ゼロ以外の値を入力して、指標の最小値を指定できます。 </p> <p>空白またはゼロの場合、指標のすべての値がダウンロードされます。それ以外の場合は、最小指標値が渡されると、この指標のダウンロードが停止します。 </p> <p>Adobe Analytics指標は、降順で取得されます。 </p> <p><span class="uicontrol"> <b>+</b> </span>をクリックして、指標定義を追加します。不要になった指標定義や不要になった指標定義を削除するには、<span class="uicontrol"> <b>-</b> </span>をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics指標集計期間（日） </p> </td> 
      <td colname="col2"> <p> 昨日の日付からカウントバックして取得する、Adobe Analytics指標に相当する日数を制御します。 現在の日付からのデータの取得は試行されません。 </p> <p>デフォルトは 7 です。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analyticsダウンロード更新頻度（日） </p> </td> 
      <td colname="col2"> <p> ランク付けの計算に使用されるAdobe Analyticsデータのダウンロード間隔の最小値を設定します。 </p> <p>ダウンロード更新頻度の間隔で発生するインデックストリガーダウンロードは無視されます。 ただし、手動ダウンロードではこの値は無視されます。 </p> <p>この値をデフォルトの1に設定した場合、Adobe Analyticsのデータは24時間以内に2回以上ダウンロードされません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [ランキングルール](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)についても参照してください。
1. クリック **[!UICONTROL Save Changes]**.

   ステージ[!DNL Adobe Analytics Report Suites]ページに戻ります。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## Adobe Analyticsレポートスイートの削除{#task_0ACA172214D14654ABDB139F417B9F7D}

「削除」を使用すると、[!DNL Adobe Analytics Report Suites]ページからレポートスイートを削除できます。 レポートスイートを削除すると、サイト検索/マーチャンダイジングサーバーからデータのコピーのみが削除されます。データはAdobe Analytics系に影響を与えません。

**Adobe Analyticsレポートスイートを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Report Suites]ページの&#x200B;**[!UICONTROL Actions]**&#x200B;列の下で、削除するレポートスイートの&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Delete Report Suite]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## Adobe Analyticsデータのプレビュー{#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

プレビューを使用して、最も最近読み込んだAdobe Analytics指標を表示できます。

表の行列には、指標データの各行の数が表示され、Adobe Analytics指標が読み込まれた元の順序が示されます。

「Product」列には、指標データの各行に関連付けられたAdobe Analytics要素が表示されます。 この列の値は、ランクの定義で設定した、サイトの検索/マーチャンダイジングページと、対応する指標の値を関連付けるために使用されます。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

[ランキング](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)の設定を参照してください。

残りの列には、各エントリに関連付けられている指標値が表示されます。

テーブルが空の場合は、まだAdobe Analyticsデータをロードしていないことを意味します。 [!DNL Adobe Analytics Data Preview]ページを閉じてから、Adobe Analyticsのデータを読み込むことができます。

[Adobe Analyticsデータの読み込み](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。
テーブルが検索語レポートとして指定されている場合は、各行に小さな三角形が表示されます。 ドロップダウンリストをクリックし、「検索語句をシミュレート」**または「新しいビジネスルールを作成」**&#x200B;を選択します。 ****&#x200B;選択したアクションは、2列目のデータである行の検索語句に適用されます

**Adobe Analyticsプレビューへ**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。 [!DNL Adobe Analytics Report Suites]ページの[!DNL Actions]列の下で、表示するダウンロードデータを含むレポートスイートの&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。

   * クリック **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. [!DNL Adobe Analytics Terms Report]ページの[!DNL Actions]列の下で、表示するダウンロードデータを含むレポートスイートの&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。

1. [!DNL Adobe Analytics Data Preview]ページで、ページの上部と下部にあるナビゲーションと表示のオプションを使用して、データを表示します。

   表の列見出しをクリックして、昇順または降順でデータを並べ替えます。
1. 次のいずれかの操作を行います。

   * **[!UICONTROL Download to Desktop]**&#x200B;をクリックして、テーブルを`.xlt`ファイルとしてダウンロードし、保存します。

   * Adobe Analyticsデータのプレビューが終了し、前に表示したページに戻ったら、ページを閉じます。

## 最新のAdobe Analytics・データ・ロードからログを表示{#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

表示ログを使用すると、最新のダウンロードプロセスのAdobe Analyticsデータログファイルを調べることができます。 ログ表示を使用して、実行中のダウンロードを監視することもできます。

[Adobe Analyticsデータの読み込み](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

**最新のAdobe Analytics・データ・ロードからログを表示するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Report Suites]ページで、**[!UICONTROL View Log]**&#x200B;をクリックします。 ログページ、
1. [!DNL Adobe Analytics Data Log]ページで、ページの上部と下部にあるナビゲーションと表示のオプションを使用して、ログ情報を表示します。
1. 終了したら、ページを閉じて[!DNL Adobe Analytics Report Suites]ページに戻ります。

## Adobe Analyticsデータを読み込み中{#task_2F3C55189B0A4049AB2113F2291CC181}

設定済みのAdobe Analyticsレポートスイートのデータは、サイト検索/マーチャンダイジングにダウンロードできます。

[データロード]ページには、最後のAdobe Analyticsデータロード操作のステータスが次の情報と共に表示されます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ステータスフィールド </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ステータス </p> </td> 
   <td colname="col2"> <p>最後に行われたデータ読み込みの成功または失敗を示します。 または、既に進行中のデータ読み込み操作のステータスを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>結果 </p> </td> 
   <td colname="col2"> <p>最後のデータ読み込み試行時にダウンロードされた指標データの行数を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>開始時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ読み込み操作が開始された日時を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>停止時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ・ロード操作の完了日時を表示します。 または、現在のデータ読み込み操作がまだ進行中であることを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Adobe Analyticsデータを読み込むには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [!DNL Stage Adobe Analytics Report Suites]ページで、**[!UICONTROL Load Adobe Analytics Data]**&#x200B;をクリックします。
1. **[!UICONTROL Adobe Analytics Data Load]**&#x200B;ページで、次のいずれかの操作を行います。

   * **[!UICONTROL Start Load]**&#x200B;をクリックして、読み込み操作を開始します。

      データの読み込み操作中、**Progress**&#x200B;行には進行状況に関する情報が表示されます。

   * **[!UICONTROL Stop Load]**&#x200B;をクリックして、読み込み操作を停止します。

1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL Stage Adobe Analytics Reports Suite]ページに戻ります。

## レポートスイートリストの更新{#task_EA6215D438CA4185B106657D9712ED34}

サイト検索/マーチャンダイジングのユーザーインターフェイスからAdobe Analyticsに初めてアクセスすると、会社が利用できるAdobe Analyticsレポートスイートのリストがダウンロードされ、キャッシュされます。 新しいレポートスイートが最近追加された場合、または既存のレポートスイートが削除された場合は、「レポートスイートの更新リスト」を使用して、サイト検索/マーチャンダイジングに現在表示されているリストを更新できます。

「[Adobe Analyticsレポートスイートの追加](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)」を参照してください。

「[Adobe Analyticsレポートスイートの削除](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D)」を参照してください。

**レポートスイートリストを更新するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Metrics]**&#x200B;をクリックします。
1. [!DNL Adobe Analytics Report Suites]ページで、**[!UICONTROL Refresh Report Suite List]**&#x200B;をクリックします。

## アドバンスAdobe Analyticsオプションの設定{#task_C0FF2D69F59D44D8943A7831ED7FEC19}

[!DNL Advanced Adobe Analytics Options]を使用して、Adobe Analyticsレポートスイートのダウンロードプロセスの動作を微調整するための設定を制御できます。

「[レポートスイートのAdobe Analytics指標の編集](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)」を参照してください。

**アドバンスAdobe Analyticsオプションを設定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL Advanced Options]**&#x200B;をクリックします。
1. [!DNL Advanced Adobe Analytics Options]ページで、次のオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>最大行数、任意の指標 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsのデータが多すぎる場合にダウンロードを防ぐ最適化設定です。 </p> <p>このオプションを0以外の値に設定した場合、各指標に対してフェッチされた合計行数が指定した値を超えると、Adobe Analytics・データ・フェッチは停止します。 </p> <p>デフォルト値は0です。最大値が適用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>指標の繰り返しの取得サイズ（行） </p> </td> 
      <td colname="col2"> <p> 一度に取得するAdobe Analytics指標値の数を制御します。 指標データ行は、すべてのデータが取得されるか、最大行数に達するまで、繰り返しフェッチされます。 </p> <p>通常は、この設定を変更する必要はありません。 ただし、サイトの完全な再インデックスの指標のダウンロードフェーズを最適化すると役立つ場合があります。 </p> <p>デフォルト値は 5000 です。 </p> </td> 
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

## SAINT分類フィードについて{#concept_C55609DA24914BBC92CD90ED0259199D}

Adobe AnalyticsSAINTを使用すると、外部のソースから表形式のデータを受け入れて、分析レポートを強化できます。 例えば、サイト検索/マーチャンダイジングを使用して、独自のインデックスからデータを取得し、そのデータをAdobe Analyticsにエクスポートできます。

サイト検索/マーチャンダイジングでAdobe AnalyticsSAINT機能を正しく使用するには、次の要件に注意してください。

* Adobe Analytics会社とレポートスイートが必要です。

   [Adobe Analyticsのメニューについて](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411)を参照してください。
* Adobe Analyticsのユーザーアカウントは、レポートスイートを変更する権限が必要です。

   「[Adobe Analytics指標認証の設定](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42)」を参照してください。
* Adobe Analyticsユーザは、Adobe AnalyticsウェブAPIを使用できるように、ウェブAPIグループに属している必要があります。
* 検索インデックスには、正しい形式のデータなど、Adobe Analyticsが使用できるデータが必要です。

フィードを作成する前に、次の質問と情報を確認し、SAINTフィードウィザードを正常に完了できるようにします。

* どのレポートスイートで作業を行いますか。
* 製品、e-varなど、どの分類セットに対してデータを提供しますか。
* レポートにはどのような分類が存在しますか。 この質問に対する答えは、サイト検索/マーチャンダイジングで容易に利用できるデータのタイプと、Adobe Analyticsが望ましいと報告するレポートのタイプによって決まります。
* SAINTは、サイト検索/マーチャンダイジングのデータをテキストタイプとして受け入れます。 そのデータの形式は、Adobe Analyticsのレポートの表示に影響を与える。

## Adobe AnalyticsSAINTフィードの作成{#task_914B5AB821E84627953D8EF9339A7DD0}

Adobe AnalyticsSAINTを使用すると、外部ソースから表形式のデータを受け取ることで、Adobe Analyticsのレポートを強化できます。

例えば、サイト検索/マーチャンダイジングを使用して、独自のインデックスからデータを取得し、そのデータをAdobe Analyticsにエクスポートできます。

**Adobe AnalyticsSAINTフィードを作成するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL SAINT Classification Feeds]ページで、**[!UICONTROL Create SAINT Feed]**&#x200B;をクリックします。
1. [!DNL Create Feed]ダイアログボックスの「**フィード名**」テキストフィールドに新しいフィード名を入力し、「**[!UICONTROL Next]**」をクリックします。

   この時点で、フィードが保存され、[!DNL SAINT Classification Feed]ページに追加されます。 選択した場合は、終了し、後でフィードを編集してウィザードを完了できます。
1. [!DNL Authentication]ページで、それぞれのテキストフィールドにAdobe Analytics会社名、ユーザー名、Webシークレットを指定し、**[!UICONTROL Next]**&#x200B;をクリックします。

   Web APIをAdobe Analyticsで使用する権限があることを確認します。
1. **[!UICONTROL Report Suite]**&#x200B;ページで、レポートスイートとその分類データセットを選択し、**[!UICONTROL Next]**&#x200B;をクリックします。
1. [!DNL Field Maps]ページで、Adobe Analytics分類をサイト検索/マーチャンダイジングメタデータフィールドにマッピングし、**[!UICONTROL Next]**&#x200B;をクリックします。

   Adobe Analytics分類を調整するには、[**[!UICONTROL Edit]** Adobe Analytics分類]をクリックしてAdobe Analyticsにログインします。 変更が完了したら、**[!UICONTROL Refresh Classifications]**&#x200B;をクリックして分類の選択を更新します。
1. [!DNL Search Criteria]ページでは、サイト検索/マーチャンダイジングからのデータを、Adobe AnalyticsSAINTに送信する前にフィルタリングできます。 ここでルールビルダーインターフェイスを使用してフィルタールールを作成し、**[!UICONTROL Next]**&#x200B;をクリックします。
1. [!DNL Configure FTP]ページで、FTPサーバーを選択します。 データのアップロード頻度を指定し、[**[!UICONTROL Next]**]をクリックします。

   ベストプラクティスとして、各フィードには、誤ってデータを失うのを防ぐための独自のFTPアカウントがあります。 ここで、新しいAdobe AnalyticsFTPアカウントを作成できます。
1. [!DNL Verification]ページで、**[!UICONTROL Show Data View]**&#x200B;をクリックして、出力のデータ表示表現を確認します。 実際のフィードファイルが存在する場合は、それらがここにリストされ、ダウンロードできます。
1. クリック **[!UICONTROL Close]**.

## Adobe AnalyticsSAINTフィードの編集{#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

作成した既存のSAINTフィードのすべての要素を編集できます。

**Adobe AnalyticsSAINTフィードを編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL Saint Classification Feeds]ページの&#x200B;**[!UICONTROL Name]**&#x200B;列の下のフィードの横のドロップダウンリストで、**[!UICONTROL Edit feed]**&#x200B;をクリックします。
1. SAINTフィードダイアログボックスの「**フィード名**」テキストフィールドに新しいフィード名を入力し、「**[!UICONTROL Next]**」をクリックします。

   この時点で、フィードが保存され、[!DNL SAINT Classification Feed]ページに追加されます。 選択した場合は、終了し、後でフィードを編集してウィザードを完了できます。
1. [!DNL Authentication]ページで、それぞれのテキストフィールドにAdobe Analytics会社名、ユーザー名、Webシークレットを指定し、**[!UICONTROL Next]**&#x200B;をクリックします。

   Web APIをAdobe Analyticsで使用する権限があることを確認します。
1. **[!UICONTROL Report Suite]**&#x200B;ページで、レポートスイートとその分類データセットを選択し、**[!UICONTROL Next]**&#x200B;をクリックします。
1. [!DNL Field Maps]ページで、Adobe Analytics分類をサイト検索/マーチャンダイジングメタデータフィールドにマッピングし、**[!UICONTROL Next]**&#x200B;をクリックします。

   Adobe Analytics分類を調整するには、[**[!UICONTROL Edit]** Adobe Analytics分類]をクリックしてAdobe Analyticsにログインします。 変更が完了したら、**[!UICONTROL Refresh Classifications]**&#x200B;をクリックして分類の選択を更新します。
1. [!DNL Search Criteria]ページでは、サイト検索/マーチャンダイジングからのデータを、Adobe AnalyticsSAINTに送信する前にフィルタリングできます。 ここでルールビルダーインターフェイスを使用してフィルタールールを作成し、**[!UICONTROL Next]**&#x200B;をクリックします。
1. [!DNL Configure FTP]ページで、FTPサーバーを選択します。 データのアップロード頻度を指定し、[**[!UICONTROL Next]**]をクリックします。

   ベストプラクティスとして、各フィードには、誤ってデータを失うのを防ぐための独自のFTPアカウントがあります。 ここで、新しいAdobe AnalyticsFTPアカウントを作成できます。
1. [!DNL Verification]ページで、**[!UICONTROL Show Data View]**&#x200B;をクリックして、出力のデータ表示表現を確認します。 実際のフィードファイルが存在する場合は、それらがここにリストされ、ダウンロードできます。
1. クリック **[!UICONTROL Close]**.

## Adobe AnalyticsSAINTフィードの削除{#task_5319B1F4CA1A406393CFD7AE97258CEB}

不要になった、または使用しなくなった既存のAdobe AnalyticsSAINTフィードを削除できます。

**Adobe AnalyticsSAINTフィードを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL Saint Classification Feeds]ページの&#x200B;**[!UICONTROL Name]**&#x200B;列の下の、削除するフィードの横にあるドロップダウンリストで、**[!UICONTROL Delete feed]**&#x200B;をクリックします。
1. 削除ダイアログボックスで、「**はい**」をクリックして、フィードの削除を確認します。

## Adobe AnalyticsSAINTフィードファイルの表示{#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

既存のSAINTフィードの[!DNL Verification]ページを開いて、出力のデータ表示表現を確認できます。

実際のフィードファイルが存在する場合は、それらがここに表示され、テキストファイルとしてダウンロードできます。

**Adobe AnalyticsSAINTフィードファイルを表示するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL Saint Classification Feeds]ページの&#x200B;**[!UICONTROL Name]**&#x200B;列の下のフィードの横のドロップダウンリストで、**[!UICONTROL View Feed Files]**&#x200B;をクリックします。
1. （オプション）**[!UICONTROL Download File]**&#x200B;をクリックして、フィードファイルをテキストファイルとして保存します。
1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL SAINT Classification Feeds]ページに戻ります。

## Adobe AnalyticsSAINTフィードのテスト{#task_9864D69BE3824FC29C10B36EE4855D25}

ファイルをアップロードせずに、既存のAdobe AnalyticsSAINTフィードをテストできます。

「[Adobe AnalyticsSAINTフィードの生成とアップロード](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A)」を参照してください。

「[Adobe AnalyticsSAINTフィードファイルの表示](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)」を参照してください。

**Adobe AnalyticsSAINTフィードファイルをテストするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL Saint Classification Feeds]ページの&#x200B;**[!UICONTROL Name]**&#x200B;列の下のフィードの横のドロップダウンリストで、**[!UICONTROL Test Feed (No file upload)]**&#x200B;をクリックします。
1. フィードの処理が終了したら、フィード名のドロップダウンリストで&#x200B;**[!UICONTROL View Feed Files]**&#x200B;をクリックします。
1. [!DNL Verification]ページで、**[!UICONTROL Download File]**&#x200B;をクリックしてフィードファイルをダウンロードします。
1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL SAINT Classification Feeds]ページに戻ります。

## Adobe AnalyticsSAINTフィードの生成とアップロード{#task_47AED946AA964334A877FDC8D4F6F00A}

作成した既存のAdobe Analyticsフィード用のフィードファイルを生成し、アップロードできます。

「[Adobe AnalyticsSAINTフィードのテスト](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25)」を参照してください。

「[Adobe AnalyticsSAINTフィードファイルの表示](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)」を参照してください。

**Adobe AnalyticsSAINTフィードファイルを生成してアップロードするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Adobe Analytics]**/**[!UICONTROL SAINT Classification Feeds]**&#x200B;をクリックします。
1. [!DNL Saint Classification Feeds]ページの&#x200B;**[!UICONTROL Name]**&#x200B;列の下のフィードの横のドロップダウンリストで、**[!UICONTROL Generate and Upload Feed]**&#x200B;をクリックします。
1. フィードの処理が終了したら、フィード名のドロップダウンリストで&#x200B;**[!UICONTROL View Feed Files]**&#x200B;をクリックします。
1. [!DNL Verification]ページで、**[!UICONTROL Download File]**&#x200B;をクリックしてフィードファイルをダウンロードします。
1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL SAINT Classification Feeds]ページに戻ります。
