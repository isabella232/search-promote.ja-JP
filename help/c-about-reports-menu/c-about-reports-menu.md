---
description: レポートメニューを使用して、顧客の検索クエリのレポートを表示またはリセットします。
solution: Target
title: レポートメニューについて
topic: Reports,Site search and merchandising
uuid: 3ea856d7-dc07-455f-8dc7-c7f7f56355d7
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 2%

---


# [レポート]メニュー{#about-the-reports-menu}について

レポートメニューを使用して、顧客の検索クエリのレポートを表示またはリセットします。

+ [データ表示](/help/c-about-reports-menu/c-about-data-views.md)
+ [アラート](/help/c-about-reports-menu/c-about-alerts.md)

## キーワードレポートまたはNULL検索用語レポートの表示{#task_53B7ED1582DD4B0E8376546A7AFC789A}

顧客の検索用語がログに記録され、日、週、月ごとにレポートが作成されます。 これらの用語レポートは、Webサイトで顧客が何を探しているかを把握するのに役立ちます。

この情報を使用して、サイトデザインを改善したり、顧客の検索結果をさらに改善したりします。

レポートの表には、次の情報が表示されます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>グラフ </p> </td> 
   <td colname="col2"> <p>特定の単語または句の相対検索数を視覚的に表します。 </p> <p>これを使用して、顧客にとって最も重要な検索クエリをすばやく判断できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カウント数 </p> </td> 
   <td colname="col2"> <p>選択したレポートの期間中に、顧客がサイトで特定のフレーズまたは単語を検索した回数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>単語 </p> </td> 
   <td colname="col2"> <p>1つの単語または完全なフレーズを訪問者が検索した検索回数。 </p> <p>各顧客が入力したフレーズまたは語句が含まれます。 各フレーズまたは単語はハイパーリンクされているので、実際の検索結果を簡単に確認できます。 この列には、値を空白のクエリでも含めることができます。これは、顧客が検索語句を入力せずに「<span class="uicontrol">検索</span>」をクリックしたことを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>結果数 </p> </td> 
   <td colname="col2"> <p>各検索フレーズまたは単語に対して表示される検索結果の平均数が含まれます。 </p> <p>カウントがゼロ（またはゼロに近い）の場合、通常、顧客は検索結果を見つけません。 </p> <p>数が多い場合は、検索設定を調整して、正しいページがトップランクになるようにします。 関連性または同義語の設定を使用して、フレーズまたは単語の検索結果を調整できます。 </p> <p><a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620" type="concept" format="dita" scope="local">定義について</a>を参照してください。 </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local">辞書について</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**キーワードレポートまたはヌル検索キーワードレポートを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Terms Report]**.

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Null Terms Report]**.

1. レポートページのドロップダウンリストで、トップフレーズまたはトップワードのレポートを選択します。
1. クリック **[!UICONTROL View Report]**.
1. （オプション）テーブルの[!DNL Words]列の下で、単語をクリックして[!DNL Live Simulator for Today]ページを開きます。

   検索用語の表示とテストが可能なシミュレーターについて[を参照してください。](../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E)
1. （オプション）**[!UICONTROL Reset Terms Report]**&#x200B;をクリックして、現在ログインしているアカウントのすべての用語レポート情報をクリアします。

   顧客が入力した検索用語はすべて、永久に削除されます。

## Adobe Analyticsレポートスイートの設定{#task_4A80D97030684C65AC2978B2524DE7F5}

サイト検索/マーチャンダイジングでAdobe Analyticsレポートスイートのデータを使用するには、アカウントでAdobe Analyticsのデータのコピーを作成します。

[Adobe Analyticsレポートスイートについて](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_1A51AEC5D40E459B813E7891D64B1BAE)を参照してください。

[Adobe Analyticsデータの読み込み](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

[!DNL Staged Adobe Analytics Terms Report]ページと[!DNL Staged Adobe Analytics Report Suites]ページは、次の情報を表に表示します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>レポートスイート </p> </td> 
   <td colname="col2"> <p>Adobe Analyticsレポートスイートの名前を識別します。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local">Adobe Analyticsレポートスイートの追加</a>」を参照してください。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local">レポートスイートのAdobe Analytics指標の編集</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>レポートタイプ(Adobe Analytics要素) </p> </td> 
   <td colname="col2"> <p>レポートスイートリクエストで使用されるAdobe Analytics要素、分類値またはその両方。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local">レポートスイートのAdobe Analytics指標の編集</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>相互参照フィールド </p> </td> 
   <td colname="col2"> <p>オプションのメタデータフィールド。値は、レポートスイートの「キー」の参照に使用されます。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local">レポートスイートのAdobe Analytics指標の編集</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アクション </p> </td> 
   <td colname="col2"> <p>レポートスイートのデータの最新のコピーをプレビューできます。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Adobe Analyticsデータのプレビュー</a>」を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Adobe Analyticsレポートスイートを設定するには**

1. 製品メニューで、次のいずれかの操作を行います。

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Report]**.

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Report Suites]**.

1. クリック **[!UICONTROL View Live Settings]**.

## 検索要求レポートまたはコンテンツ要求レポートの表示{#task_4C6EFB4D51474FC1BDE4326D1A726ECC}

[!DNL Search Requests Report]を表示して、指定した期間の検索要求数を確認できます。 また、[!DNL Content Requests Report]を表示して、指定した期間のコンテンツリクエスト数を確認することもできます。

>[!NOTE]
>
>各レポートで最新の検索リクエストデータまたはコンテンツリクエストデータが使用可能になるまで、最大48時間かかります。

**検索要求レポートまたはコンテンツ要求レポートを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Search Requests]**.

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Content Requests]**.

1. レポートページの&#x200B;**[!UICONTROL Period]**&#x200B;ドロップダウンリストで、レポートに含める時間を選択します。
1. **[!UICONTROL Chart Type]**&#x200B;ドロップダウンリストで、選択したレポートに基づいて次のいずれかのオプションを選択します。

   | オプション | 説明 |
   |--- |--- |
   | 日別検索要求数または日別コンテンツ要求数 | 1日あたりのリクエスト数が表示されます。 |
   | 毎月の検索要求数または毎月のコンテンツ要求数 | 1か月あたりのリクエスト数が表示されます。 |
   | 日別検索リクエスト帯域幅または日別コンテンツリクエスト帯域幅 | 日別検索要求または日別コンテンツ要求の処理に必要な帯域幅の量を表示します。 |

1. **[!UICONTROL Chart Style]**&#x200B;ドロップダウンリストで、レポートでのデータの表示方法を選択します。

## 検索インデックスサイズレポートの表示{#task_90CF717A53D341F49E8DE17505321950}

検索インデックスサイズレポートは、指定した期間の検索インデックスのサイズを表示します。

>[!NOTE]
>
>最新の検索インデックスサイズデータがレポートで使用可能になるまで、最大48時間かかります。

**検索インデックスサイズレポートを表示するには**

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Index Size]**&#x200B;をクリックします。
1. レポートページの&#x200B;**[!UICONTROL Period]**&#x200B;ドロップダウンリストで、レポートに含める時間を選択します。
1. **[!UICONTROL Chart Style]**&#x200B;ドロップダウンリストで、レポートでのデータの表示方法を選択します。

## クロールのパフォーマンスレポートまたはステージングされたクロールのパフォーマンスレポートの表示{#task_60ED9FD9769C48B1B5EEE7099B1D1899}

インデックスクローラーのパフォーマンスは、クロールの進行中に様々な指標を記録することで記録されます。 ライブクロールまたはステージングクロールのパフォーマンスレポートを表示する際に、クロール期間、指標、グラフのスタイル、クロールのタイプを選択できます。

**クロールのパフォーマンスレポートまたはステージングされたクロールのパフォーマンスレポートを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Crawl Performance]**.

      レポートページの&#x200B;**[!UICONTROL Crawl Ending]**&#x200B;ドロップダウンリストで、レポートに含める時間を選択します。

   + クリック **[!UICONTROL Reports]** > **[!UICONTROL Staged Crawl Performance]**.

      レポートページの&#x200B;**[!UICONTROL Staged Crawl Ending]**&#x200B;ドロップダウンリストで、レポートに含める時間を選択します。

1. **[!UICONTROL Metric]**&#x200B;ドロップダウンリストで、次のいずれかの指標を選択します。

   | オプション | 説明 |
   |--- |--- |
   | ダウンロードされたドキュメント | ダウンロードされたドキュメントの数。 |
   | ダウンロードされたページ | ダウンロードされたページ数。 |
   | ダウンロードバイト数(KB) | ダウンロードされたキロバイト数。 |
   | インデックス付きページ | インデックスが作成されたページ数。 |
   | インデックス付きバイト数(KB) | インデックスが作成されたキロバイト数。 |
   | 平均CPS | インデックス作成クロール中の1秒あたりの平均文字数です。 |
   | 接続MS | TCP/IP接続が完了するのを待機するのに費やした合計時間（ページあたり）。 |
   | 最初のバイトミリ秒 | ページごとに、フェッチ要求と最初に受け取ったバイトを送信する間隔。 |
   | ダウンロードMS | ページごとの合計ドキュメントダウンロード時間。 |
   | 集計 | [ダウンロードミリ秒]、[1バイトミリ秒]、[接続ミリ秒]、および残りのダウンロード時間が、各ページに表示されます。 |
   | プロセスmsのフィルタ | ページごとの合計フィルタースクリプト処理時間。 |
   | プロセスmsのダウンロード | 合計ダウンロード処理時間（ダウンロードとフィルターを含む）（ページあたり）。 |
   | インデックスプロセスms | ページごとのインデックス作成処理の合計時間。 |

1. **[!UICONTROL Chart Style]**&#x200B;ドロップダウンリストで、レポートでのデータの表示方法を選択します。 **[!UICONTROL Bars]**&#x200B;または&#x200B;**[!UICONTROL Area]**&#x200B;を選択できます。
1. **[!UICONTROL Chart Type]**&#x200B;ドロップダウンリストで、レポートするインデックスレベルを選択します。 **[!UICONTROL Full]**、**[!UICONTROL Incremental]**&#x200B;または&#x200B;**[!UICONTROL Full & Incremental]**&#x200B;を選択できます。

## 変更ログの表示 {#task_166F1156719F4B3D834BEA8E249C8057}

変更ログには、アカウント内で行われた最近の変更の履歴が表示されます。

[!DNL History]の下に表示される変更のみが表示されます。 変更は、新しい順に表示されます。 各エントリには、変更されたページ、履歴内のバージョン番号、変更を行ったユーザーの電子メールアドレス、変更の時刻、変更が保存かページの設定がライブにプッシュされたかが表示されます。

[ステージングについて](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)を参照してください。

1. 製品メニューで、**[!UICONTROL Reports]**/**[!UICONTROL Change Log]**&#x200B;をクリックします。
1. [!DNL Change Log]ページで、ページの上部と下部にあるナビゲーションと表示のオプションを使用して、ログ情報を表示します。
