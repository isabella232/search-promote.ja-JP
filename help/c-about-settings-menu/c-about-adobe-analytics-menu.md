---
description: Adobe Analyticsメニューを使用して、Adobe Analytics指標の認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。
seo-description: Adobe Analyticsメニューを使用して、Adobe Analytics指標の認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。
seo-title: Adobe Analyticsメニューについて
solution: Target
subtopic: Adobe Analytics
title: Adobe Analyticsメニューについて
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Adobe Analyticsメニューについて{#about-the-adobe-analytics-menu}

Adobe Analyticsメニューを使用して、Adobe Analytics指標の認証の設定、レポートスイートのAdobe Analytics指標の管理、またはSAINTを使用して、外部のソースから表形式のデータを受け入れ、Adobe Analyticsレポートを強化します。

## Adobe Analytics指標認証の設定 {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Adobe Analytics指標をサイトの検索/マーチャンダイジングのランクに組み込むには、まずAdobe Analytics Webサービスのログインを取得する必要があります。 ログイン情報を取得したら、それを使用して、サイト検索/マーチャンダイジングでAdobe Analytics認証を設定できます。

**Adobe Analytics指標認証を設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Authentication]**。
1. ページで、 [!DNL Setup Adobe Analytics Metrics Authentication] 各フィールドで要求された情報を指定します。

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
      <td colname="col2"> <p>Adobe Analyticsアカウントへのログインに使用するのと同じ会社名設定。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Web サービスユーザー名 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsアカウントに関連付けられているWebサービスのユーザー名。 </p> <p>この情報は、Adobe Analyticsで取得できます。 Adobe Analyticsメニューバーで、管理者/管理コンソール/管理コンソール/会社Webサービス <span class="uicontrol"> Webサービスをクリックし <b>ま</b> す。 </span> 管理者/管理コンソール/管理コンソール/会社Webサービ <span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span>スをクリックします。 この情報は、「APIアクセス情報」テーブルにあります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Webサービスの共有暗号鍵 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsアカウントに関連付けられているWebサービスのShared Secret。 </p> <p>この情報は、Adobe Analyticsで取得できます。 Adobe Analyticsメニューバーで、管理者/管理コンソール/管理コンソール/会社Webサービス <span class="uicontrol"> Webサービスをクリックし <b>ま</b> す。 </span> 管理者/管理コンソール/管理コンソール/会社Webサービ <span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span>スをクリックします。 この情報は、「APIアクセス情報」テーブルにあります。 </p> </td> 
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

## Adobe Analyticsレポートスイートについて {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

サイト検索/マーチャンダイジング内でAdobe Analyticsレポートスイートのデータを使用するには、まず、サイト検索/マーチャンダイジングアカウントでAdobe Analyticsデータのコピーを作成する必要があります。

新しいAdobe Analyticsレポートスイートの定義を作成したり、既存のAdobe Analyticsレポートスイートおよび関連指標を表示または変更したりできます。

サイト検索/マーチャンダイジング内から初めてAdobe Analyticsにアクセスすると、会社で使用可能なレポートスイートのリストがダウンロードされ、キャッシュされます。 新しいレポートスイートが最近追加されたか、既存のレポートスイートが削除された場合は、レポートスイートのリストを更新して、レポートスイートのリストを再度ダウンロードできます。

## Adobe Analyticsレポートスイートの追加 {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

サイト検索/マーチャンダイジングのランク付けルールの基となるAdobe Analyticsレポートスイートを選択できます。

選択できるリストは、Adobe Analyticsアカウント内で使用可能なレポートスイートに対応している必要があります。 選択したレポートスイートによって、サイト検索/マーチャンダイジングのランキングルール内で使用できる指標が決まります。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

Adobe Analyticsレポートスイートを追加した後、その指標を編集できます。

「レポ [ートスイートのAdobe Analytics指標の編集」を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)。

**Adobe Analyticsレポートスイートを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. Adobe Analyticsレポートスイートページで、をクリックしま **[!UICONTROL Add Report Suite]**&#x200B;す。
1. 新しく追加されたテーブル行のドロップダウンリストで、目的のレポートスイートを選択します。
1. レポートスイートのAdobe Analytics指標を編集します。

## レポートスイートのAdobe Analytics指標の編集 {#task_360904CCBBB140238ADA036C3CC07664}

サイト検索/マーチャンダイジングのランキングルールにAdobe Analytics指標を組み込むには、選択したレポートスイートに関連付けられている1つ以上の指標を選択します。 次に、Adobe Analytics Webサービスを使用して指標データを取得するために使用するオプションを設定します。

詳しくは、 [Adobe Analyticsレポートスイートの追加を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)。

詳しくは、 [Adobe Analyticsのアドバンスオプションの設定を参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19)い。

**レポートスイートのAdobe Analytics指標を編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. ページ [!DNL Adobe Analytics Report Suites] の列の下で、指 **[!UICONTROL Actions]** 標を設定す **[!UICONTROL Edit]** るレポートスイートのをクリックします。
1. ページ [!DNL Edit Adobe Analytics Metrics] で、必要な指標を設定します。 指標名の横にアスタリスク(*)が表示されない指標はオプションです。

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
      <td colname="col1"> <p>レポートスイートビュー名 </p> </td> 
      <td colname="col2"> <p>Adobe Analyticsレポートスイート名の「エイリアス」名を指定します。 この代替名は、同じレポートスイートが複数の定義で使用されている場合に便利です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>レポートタイプの選択 </p> </td> 
      <td colname="col2"> <p>選択したレポートスイートで使用するレポートタイプの値を指定します。 この値は、結果の各行のキーを示します。 </p> <p>レポートタイプは、Adobe Analytics要素とも呼ばれます。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>相互参照フィールド名 </p> </td> 
      <td colname="col2"> <p>値がレポートスイートのデータの「キー」の参照として使用されるメタデータフィールドを指定します。 </p> <p>値が選択されていない場合(「 — None — 」)、このレポートスイートのデータはランク付け計算で使用できません( <span class="uicontrol"> Ranking <b>calculations (</b> ) </span> &gt; <span class="uicontrol"> Ranking <b>&gt; Ranking</b> Rules &gt; Rules </span><span class="uicontrol"><b></b></span>&gt; Edit Rules &gt; Rules </p> <p>値を選択すると、このフィールドの値を使用して、このレポートスイートのAdobe Analyticsデータでサイト検索/マーチャンダイジングドキュメントを相互参照し、以前に設定した選択したレポートタイプの値を使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>検索用語レポート </p> </td> 
      <td colname="col2"> <p>ビジネスルールを作成し、Adobe Analyticsデータプレビューページで検索用語をシミュレ <b>ートするアクセス権を与えます</b> 。 </p> <p>詳しくは、 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Adobe Analyticsデータのプレビューを参照してくださ</a>い。 </p> <p>プルダウンメニューが各行に表示され、次の2つのオプションが表示されます。「検索語句をシミュ <b>レート</b> 」および「新 <b>しいビジネスルールを作成</b>」を参照。 </p> <p>どちらのオプションでも、検索用語として「レポートタイプ」のデータを使用します。 したがって、この機能は、レポートタイプが検索用語を表す場合にのみ意味を持ちます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>指標 </p> </td> 
      <td colname="col2"> <p>サイト検索/マーチャンダイジングのランキングルール内でダウンロードして使用する指標の値を識別します。 </p> <p>ここで設定した指標は、 <span class="uicontrol"> Rules <b>&gt;&gt;</b> Ranking Rules&gt;RulesRulesCenter&gt;EditRulesCenter </span> 、Data Type <span class="uicontrol"> Adobe AnalyticsData Analytics <b></b></span><span class="uicontrol"><b></b></span><span class="uicontrol"></span>,Adobe AnalyticsData RulesTypeの各ページに選択肢として表示されます。 選択肢には、レポートスイート名またはレポートスイートビュー名（指定されている場合）と個々の指標名の組み合わせが表示されます。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小指標値 </p> </td> 
      <td colname="col2"> <p>ゼロ以外の値を入力して、指標の最小値を指定できます。 </p> <p>空白（ゼロ）の場合、指標のすべての値がダウンロードされます。それ以外の場合は、最小指標値が渡されると、この指標のダウンロードが停止します。 </p> <p>Adobe Analytics指標は、降順で取得されます。 </p> <p>指標の定義を追加するには <span class="uicontrol"> 、[+] <b></b></span> をクリックします。不要に <span class="uicontrol"> なった <b>、または不要になった指標の定義を削除するには、「</b></span> — 」をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics指標の集計期間（日数） </p> </td> 
      <td colname="col2"> <p> 昨日の日付からカウントバックして取得するAdobe Analytics指標の日数を制御します。 現在の日付からデータを取得する試みは行われません。 </p> <p>デフォルトは 7 です。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analyticsダウンロードの更新頻度（日） </p> </td> 
      <td colname="col2"> <p> ランク付けの計算で使用されるAdobe Analyticsデータのダウンロード間隔の最小値を設定します。 </p> <p>ダウンロード更新頻度の間隔内で発生するインデックスによってトリガーされるダウンロードは無視されます。 ただし、手動ダウンロードではこの値は無視されます。 </p> <p>この値をデフォルトの1に設定した場合、Adobe Analyticsのデータは24時間以内に2回以上ダウンロードされません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> <p>この指標は必須です。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   See also [About Ranking Rules](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. クリック **[!UICONTROL Save Changes]**.

   「ステージ済み」ページに戻り [!DNL Adobe Analytics Report Suites] ます。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Adobe Analyticsレポートスイートの削除 {#task_0ACA172214D14654ABDB139F417B9F7D}

「削除」を使用して、ページからレポートスイートを削除で [!DNL Adobe Analytics Report Suites] きます。 レポートスイートを削除すると、サイト検索/マーチャンダイジングサーバーからデータのコピーのみが削除されます。データはAdobe Analyticsシステムに影響を与えません。

**Adobe Analyticsレポートスイートを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. ページ [!DNL Adobe Analytics Report Suites] の列の下で、削 **[!UICONTROL Actions]** 除するレポ **[!UICONTROL Delete]** ートスイートのをクリックします。
1. ページ上で、 [!DNL Adobe Analytics Delete Report Suite] をクリックしま **[!UICONTROL Delete]**&#x200B;す。

## Adobe Analyticsデータのプレビュー {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

プレビューを使用して、最も最近読み込まれたAdobe Analytics指標を表示できます。

表の「行」列には、指標データの各行の数が表示され、Adobe Analytics指標が読み込まれた元の順序が示されます。

「製品」列には、指標データの各行に関連付けられたAdobe Analytics要素が表示されます。 この列の値は、ランキングの定義で設定された、サイトの検索/マーチャンダイジングページと、対応する指標値との関連付けに使用されます。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

ランキングの [設定を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)い。

残りの列には、各エントリに関連付けられている指標値が表示されます。

テーブルが空の場合は、まだAdobe Analyticsデータを読み込んでいないことを意味します。 ページを閉じてか [!DNL Adobe Analytics Data Preview] ら、Adobe Analyticsデータを読み込むことができます。

詳しくは、 [Adobe Analyticsデータの読み込みを参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)い。
テーブルが検索語レポートとして指定されている場合は、各行に小さな三角形が表示されます。 ドロップダウンリストをクリックし、「検索語句をシミュレート」ま **たは「新しいビジネス** ・ルール **を作成」を選択できます**。 選択したアクションは、2列目のデータである行の検索語句に適用されます

**Adobe Analyticsデータをプレビューするには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. ページの [!DNL Adobe Analytics Report Suites] 列の下で、ダウ [!DNL Actions] ンロードしたデ **[!UICONTROL Preview]** ータを表示するレポートスイートのをクリックします。

   * クリック **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. ページの [!DNL Adobe Analytics Terms Report] 列の下で、ダウ [!DNL Actions] ンロードしたデ **[!UICONTROL Preview]** ータを表示するレポートスイートのをクリックします。

1. ページ上 [!DNL Adobe Analytics Data Preview] 部および下部のナビゲーションと表示オプションを使用して、データを表示します。

   データを昇順または降順で並べ替えるには、テーブルの列見出しをクリックします。
1. 次のいずれかの操作を行います。

   * をクリック **[!UICONTROL Download to Desktop]** して、テーブルをダウンロードし、ファイルとして保 `.xlt` 存します。

   * Adobe Analyticsデータのプレビューが終了したら、ページを閉じ、前に表示したページに戻ります。

## 最新のAdobe Analyticsデータ読み込みからのログの表示 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

「ログを表示」を使用して、最新のダウンロードプロセスのAdobe Analyticsデータログファイルを調べることができます。 また、ログビューを使用して、実行中のダウンロードを監視することもできます。

詳しくは、 [Adobe Analyticsデータの読み込みを参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)い。

**最新のAdobe Analyticsデータ読み込みのログを表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. ページ上で、 [!DNL Adobe Analytics Report Suites] をクリックしま **[!UICONTROL View Log]**&#x200B;す。 ログページ、
1. ページ上 [!DNL Adobe Analytics Data Log] 部および下部のナビゲーションと表示オプションを使用して、ログ情報を表示します。
1. 完了したら、ページを閉じてページに戻り [!DNL Adobe Analytics Report Suites] ます。

## Adobe Analyticsデータの読み込み {#task_2F3C55189B0A4049AB2113F2291CC181}

設定したAdobe Analyticsレポートスイートのデータをサイト検索/マーチャンダイジングにダウンロードできます。

データ読み込みページには、最後に実行したAdobe Analyticsのデータ読み込み操作のステータスと次の情報が表示されます。

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
   <td colname="col2"> <p>最後のデータ読み込みの成功または失敗を示します。 または、既に進行中のデータ読み込み操作のステータスを表示します。 </p> </td> 
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
   <td colname="col2"> <p>最後のデータ・ロード操作の完了日時が表示されます。 または、現在のデータ読み込み操作がまだ進行中であることを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Adobe Analyticsデータを読み込むには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. ページ上で、 [!DNL Stage Adobe Analytics Report Suites] をクリックしま **[!UICONTROL Load Adobe Analytics Data]**&#x200B;す。
1. ページで、 **[!UICONTROL Adobe Analytics Data Load]** 次のいずれかの操作を行います。

   * をクリック **[!UICONTROL Start Load]** して、読み込み操作を開始します。

      データの読み込み操作中、 **Progress** 行には進行状況に関する情報が表示されます。

   * をクリック **[!UICONTROL Stop Load]** して、読み込み操作を停止します。

1. をクリッ **[!UICONTROL Close]** クして、ページに戻 [!DNL Stage Adobe Analytics Reports Suite] ります。

## レポートスイートリストの更新 {#task_EA6215D438CA4185B106657D9712ED34}

サイト検索/マーチャンダイジングのユーザーインターフェイスから初めてAdobe Analyticsにアクセスすると、会社で使用可能なAdobe Analyticsレポートスイートのリストがダウンロードされ、キャッシュされます。 新しいレポートスイートが最近追加された場合や、既存のレポートスイートが削除された場合は、「レポートスイートリストの更新」を使用して、サイト検索/マーチャンダイジングに現在表示されているリストを更新できます。

詳しくは、 [Adobe Analyticsレポートスイートの追加を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)。

詳しくは、 [Adobe Analyticsレポートスイートの削除を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D)。

**レポートスイートリストを更新するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Metrics]**。
1. ページ上で、 [!DNL Adobe Analytics Report Suites] をクリックしま **[!UICONTROL Refresh Report Suite List]**&#x200B;す。

## Adobe Analyticsの高度なオプションの設定 {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

を使用して、Adobe Analytics [!DNL Advanced Adobe Analytics Options] レポートスイートのダウンロードプロセスの動作を微調整するのに役立つ設定を制御できます。

「レポ [ートスイートのAdobe Analytics指標の編集」を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)。

**Adobe Analyticsのアドバンスオプションを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL Advanced Options]**。
1. ページで、 [!DNL Advanced Adobe Analytics Options] 次のオプションを設定します。

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
      <td colname="col2"> <p>Adobe Analyticsデータのダウンロードが多すぎないようにする最適化設定。 </p> <p>このオプションを0以外の値に設定した場合、各指標に対してフェッチされた行の合計数が指定値を超えると、Adobe Analyticsのデータフェッチが停止します。 </p> <p>デフォルト値は0です。最大値が適用されていません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>指標の繰り返しフェッチサイズ（行） </p> </td> 
      <td colname="col2"> <p> 一度に取得するAdobe Analytics指標の値の数を制御します。 指標データ行は、すべてのデータが取得されるか、行の上限に達するまで、繰り返しフェッチされます。 </p> <p>通常は、この設定を変更する必要はありません。 ただし、サイトの完全なインデックス再作成の指標のダウンロード段階を最適化すると役に立つ場合があります。 </p> <p>デフォルト値は 5000 です。 </p> </td> 
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

## SAINT分類フィードについて {#concept_C55609DA24914BBC92CD90ED0259199D}

Adobe Analytics SAINTを使用すると、外部のソースから表形式のデータを受け入れることで、分析レポートを強化できます。 例えば、サイト検索/マーチャンダイジングを使用して、独自のインデックスからデータを取得し、そのデータをAdobe Analyticsにエクスポートできます。

サイト検索/マーチャンダイジングでAdobe Analytics SAINT機能を正しく使用するには、次の要件に注意してください。

* Adobe Analyticsの会社とレポートスイートが必要です。

   Adobe Analyticsメ [ニューについてを参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411)。
* Adobe Analyticsユーザーアカウントは、レポートスイートを変更する権限を持っている必要があります。

   詳しくは、 [Adobe Analytics指標認証の設定を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42)。
* Adobe AnalyticsユーザーがAdobe Analytics Web APIを使用できるようにするには、Web APIグループに属している必要があります。
* 検索インデックスには、データが正しい形式であるなど、Adobe Analyticsで使用できるデータが含まれている必要があります。

フィードを作成する前に、次の質問と情報を確認し、SAINTフィードウィザードを正常に完了できるようにします。

* どのレポートスイートで作業しますか。
* どの分類セット（製品、e-varなど）に対してデータを提供しますか。
* レポートにはどのような分類が存在しますか。 この質問に対する答えは、サイト検索/マーチャンダイジングで簡単に利用できるデータのタイプと、Adobe Analyticsが望ましいとレポートするレポートのタイプによって決まります。
* SAINTは、サイト検索/マーチャンダイジングのデータをテキストタイプとして受け付けます。 そのデータの形式は、Adobe Analyticsレポートの表示に影響します。

## Adobe Analytics SAINTフィードの作成 {#task_914B5AB821E84627953D8EF9339A7DD0}

Adobe Analytics SAINTを使用すると、外部のソースから表形式のデータを受け入れることで、Adobe Analyticsレポートを強化できます。

例えば、サイト検索/マーチャンダイジングを使用して、独自のインデックスからデータを取得し、そのデータをAdobe Analyticsにエクスポートできます。

**Adobe Analytics SAINTフィードを作成するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ上で、 [!DNL SAINT Classification Feeds] をクリックしま **[!UICONTROL Create SAINT Feed]**&#x200B;す。
1. ダイアログ [!DNL Create Feed] ボックスの「フィー **ド名** 」テキストフィールドに新しいフィード名を入力し、をクリックしま **[!UICONTROL Next]**&#x200B;す。

   この時点で、フィードが保存され、ページに追加され [!DNL SAINT Classification Feed] ます。 選択した場合は、フィードを終了し、後で編集してウィザードを完了できます。
1. ページ [!DNL Authentication] で、Adobe Analyticsの会社名、ユーザー名およびWebシークレットをそれぞれのテキストフィールドに指定し、をクリックしま **[!UICONTROL Next]**&#x200B;す。

   Adobe AnalyticsでWeb APIを使用する権限があることを確認します。
1. ページで、 **[!UICONTROL Report Suite]** レポートスイートとその分類データセットを選択し、をクリックしま **[!UICONTROL Next]**&#x200B;す。
1. ページで、Adobe Analytics分 [!DNL Field Maps] 類をサイト検索/マーチャンダイジングメタデータフィールドにマッピングし、をクリックしま **[!UICONTROL Next]**&#x200B;す。

   Adobe Analytics分類を調整するには、「Adobe Analytics分類」 **[!UICONTROL Edit]** をクリックしてAdobe Analyticsにログインします。 変更が完了したら、をクリックして分 **[!UICONTROL Refresh Classifications]** 類の選択を更新します。
1. このページで [!DNL Search Criteria] は、サイト検索/マーチャンダイジングのデータをフィルタリングしてから、Adobe Analytics SAINTに送信できます。 ここにルールビルダーインターフェイスを使用してフィルタールールを作成し、をクリックしま **[!UICONTROL Next]**&#x200B;す。
1. ページで、 [!DNL Configure FTP] FTPサーバーを選択します。 データをアップロードする頻度を指定し、をクリックします **[!UICONTROL Next]**。

   ベストプラクティスとして、各フィードには、データの誤った損失を防ぐための独自のFTPアカウントがあります。 ここで、新しいAdobe Analytics FTPアカウントを作成できます。
1. ページで、 [!DNL Verification] をクリックし **[!UICONTROL Show Data View]** て、出力のデータビュー表現を確認します。 実際のフィードファイルが存在する場合は、このリストに表示され、ダウンロードできます。
1. クリック **[!UICONTROL Close]**.

## Adobe Analytics SAINTフィードの編集 {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

作成した既存のSAINTフィードのすべての要素を編集できます。

**Adobe Analytics SAINTフィードを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ [!DNL Saint Classification Feeds] の列の下のフ **[!UICONTROL Name]** ィードの横のドロップダウンリストで、をクリックします **[!UICONTROL Edit feed]**。
1. SAINTフィードダイアログボックスの「フィード名 **」テキストフィールドに新しいフィード名を入力し、をクリックしま****[!UICONTROL Next]**&#x200B;す。

   この時点で、フィードが保存され、ページに追加され [!DNL SAINT Classification Feed] ます。 選択した場合は、フィードを終了し、後で編集してウィザードを完了できます。
1. ページ [!DNL Authentication] で、Adobe Analyticsの会社名、ユーザー名およびWebシークレットをそれぞれのテキストフィールドに指定し、をクリックしま **[!UICONTROL Next]**&#x200B;す。

   Adobe AnalyticsでWeb APIを使用する権限があることを確認します。
1. ページで、 **[!UICONTROL Report Suite]** レポートスイートとその分類データセットを選択し、をクリックしま **[!UICONTROL Next]**&#x200B;す。
1. ページで、Adobe Analytics分 [!DNL Field Maps] 類をサイト検索/マーチャンダイジングメタデータフィールドにマッピングし、をクリックしま **[!UICONTROL Next]**&#x200B;す。

   Adobe Analytics分類を調整するには、「Adobe Analytics分類」 **[!UICONTROL Edit]** をクリックしてAdobe Analyticsにログインします。 変更が完了したら、をクリックして分 **[!UICONTROL Refresh Classifications]** 類の選択を更新します。
1. このページで [!DNL Search Criteria] は、サイト検索/マーチャンダイジングのデータをフィルタリングしてから、Adobe Analytics SAINTに送信できます。 ここにルールビルダーインターフェイスを使用してフィルタールールを作成し、をクリックしま **[!UICONTROL Next]**&#x200B;す。
1. ページで、 [!DNL Configure FTP] FTPサーバーを選択します。 データをアップロードする頻度を指定し、をクリックします **[!UICONTROL Next]**。

   ベストプラクティスとして、各フィードには、データの誤った損失を防ぐための独自のFTPアカウントがあります。 ここで、新しいAdobe Analytics FTPアカウントを作成できます。
1. ページで、 [!DNL Verification] をクリックし **[!UICONTROL Show Data View]** て、出力のデータビュー表現を確認します。 実際のフィードファイルが存在する場合は、このリストに表示され、ダウンロードできます。
1. クリック **[!UICONTROL Close]**.

## Adobe Analytics SAINTフィードの削除 {#task_5319B1F4CA1A406393CFD7AE97258CEB}

不要になった、または使用しなくなった既存のAdobe Analytics SAINTフィードを削除できます。

**Adobe Analytics SAINTフィードを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ [!DNL Saint Classification Feeds] の列の下で、 **[!UICONTROL Name]** 削除するフィードの横のドロップダウンリストで、をクリックします **[!UICONTROL Delete feed]**。
1. 削除ダイアログボックスで、「 **Yes** 」をクリックしてフィードの削除を確認します。

## Adobe Analytics SAINTフィードファイルの表示 {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

既存のSAINTフィードのペ [!DNL Verification] ージを開いて、出力のデータビュー表現を確認できます。

実際のフィードファイルが存在する場合は、このリストに表示され、テキストファイルとしてダウンロードできます。

**Adobe Analytics SAINTフィードファイルを表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ [!DNL Saint Classification Feeds] の列の下のフ **[!UICONTROL Name]** ィードの横のドロップダウンリストで、をクリックします **[!UICONTROL View Feed Files]**。
1. （オプション）をクリックし **[!UICONTROL Download File]** て、フィードファイルをテキストファイルとして保存します。
1. をクリッ **[!UICONTROL Close]** クして、ページに戻 [!DNL SAINT Classification Feeds] ります。

## Adobe Analytics SAINTフィードのテスト {#task_9864D69BE3824FC29C10B36EE4855D25}

ファイルをアップロードせずに、既存のAdobe Analytics SAINTフィードをテストできます。

詳しくは、 [Adobe Analytics SAINTフィードの生成とアップロードを参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A)い。

詳しくは、 [Adobe Analytics SAINTフィードファイルの表示を参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)い。

**Adobe Analytics SAINTフィードファイルをテストするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ [!DNL Saint Classification Feeds] の列の下のフ **[!UICONTROL Name]** ィードの横のドロップダウンリストで、をクリックします **[!UICONTROL Test Feed (No file upload)]**。
1. フィードの処理が完了したら、フィード名のドロップダウンリストで、をクリックしま **[!UICONTROL View Feed Files]**&#x200B;す。
1. ページで、をク [!DNL Verification] リックしてフィー **[!UICONTROL Download File]** ドファイルをダウンロードします。
1. をクリッ **[!UICONTROL Close]** クして、ページに戻 [!DNL SAINT Classification Feeds] ります。

## Adobe Analytics SAINTフィードの生成とアップロード {#task_47AED946AA964334A877FDC8D4F6F00A}

作成した既存のAdobe Analyticsフィードのフィードファイルを生成し、アップロードできます。

詳しくは、 [Adobe Analytics SAINTフィードのテストを参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25)い。

詳しくは、 [Adobe Analytics SAINTフィードファイルの表示を参照してくださ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)い。

**Adobe Analytics SAINTフィードファイルを生成してアップロードするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Adobe Analytics]** ます **[!UICONTROL SAINT Classification Feeds]**。
1. ページ [!DNL Saint Classification Feeds] の列の下のフ **[!UICONTROL Name]** ィードの横のドロップダウンリストで、をクリックします **[!UICONTROL Generate and Upload Feed]**。
1. フィードの処理が完了したら、フィード名のドロップダウンリストで、をクリックしま **[!UICONTROL View Feed Files]**&#x200B;す。
1. ページで、をク [!DNL Verification] リックしてフィー **[!UICONTROL Download File]** ドファイルをダウンロードします。
1. をクリッ **[!UICONTROL Close]** クして、ページに戻 [!DNL SAINT Classification Feeds] ります。
