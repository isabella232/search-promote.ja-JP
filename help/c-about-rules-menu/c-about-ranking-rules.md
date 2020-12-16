---
description: ランキングルールを使用すると、含まれるメタタグコンテンツと関連するAdobe Analytics指標に基づいて、顧客の検索結果の相対的な位置やランクを制御できます。
seo-description: ランキングルールを使用すると、含まれるメタタグコンテンツと関連するAdobe Analytics指標に基づいて、顧客の検索結果の相対的な位置やランクを制御できます。
seo-title: ランキングルールについて
solution: Target
subtopic: Ranking Rules
title: ランキングルールについて
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '4647'
ht-degree: 1%

---


# ランキングルール{#about-ranking-rules}について

ランキングルールを使用すると、含まれるメタタグコンテンツと関連するAdobe Analytics指標に基づいて、顧客の検索結果の相対的な位置やランクを制御できます。

## ランキングルールの使用{#concept_F555C076759B4E81B925441CFE707397}

ランキングルールを定義して、各ドキュメントのコンテンツに基づいて、検索結果内でのドキュメントの相対的な配置を決定します。 ランキングルールは、メタタグコンテンツ、Adobe Analytics指標(アカウントがAdobe Analyticsと連携するように設定されている場合)、Adobe AnalyticsHBX指標(アカウントがAdobe AnalyticsHBXと連携するように設定されている場合)のいずれかに基づいて設定できます。

特定のブランド名や価格など、目的の特性を持つメタタグを含むWebページや、個別視聴者など、Adobe Analyticsの主要業績評価指標が望ましいWebページのランクが、そうでないWebページよりも高くなるように設定できます。 「望ましい」特性は、ランキングルールを追加または編集し、Webサイトのインデックスを再作成することで簡単に更新できます。

タイプ&quot;rank&quot;のmetaタグが複数定義されている場合は、様々なランクフィールドの計算に使用するルールの集合を個別に作成できます。 ランキングルールグループを追加して、定義済みの「ランク」フィールドの1つに割り当てることができます。 ルールグループは通常、1つ以上のルール定義を含みますが、他のルールグループも参照できるので、複数のランクの計算時に共有する、よく使用される1つ以上のルールグループを作成できます。

[ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。

正のランク値は検索結果を上に向かって促進します。負のランク値を指定すると、検索結果が検索結果の一番下に降下します。 ランク付けの値の通常の範囲は1.0で、これは検索結果内の最大プロモーションです。-1.0は最大デモーションです。 メタデータ定義の「ランク」フィールドを編集してこの範囲をカスタマイズできますが、通常、このタイプのカスタマイズは不要です。

[定義について](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620)を参照してください。

設定/メタデータ/定義で複数のランクフィールドを定義した場合は、各ランクフィールドに1つずつ、ランクルールの追加のセットを作成できます。 ランクフィールドに直接関連付けることなく、追加のランク付けルールのセットを定義できます。 この柔軟性により、1つ以上のランク値の計算で共有できる共通ルールのセットを作成できます。

**重要**:ランキングルールを使用する前に、完了する必要があるアカウント設定手順がいくつかあります。

[ランキングの設定](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)を参照

## ランキング{#task_4CEBC13925B047FC95BDC217B48089C5}の設定

ランキングルールを使用する前に、完了する必要があるアカウント設定手順がいくつかあります。

**ランキングを設定するには**

1. 次のいずれかを選択します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>タスク </p> </th> 
      <th colname="col2" class="entry"> <p>設定 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>メタタグに基づくランキングルールを作成するには </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> 製品メニューで、<span class="uicontrol">設定</span>/<span class="uicontrol">メタデータ</span>/<span class="uicontrol">定義</span>をクリックします。 </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> 定義ページで、「<span class="uicontrol">追加新しいフィールド</span>」をクリックします。 </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> フィールド追加ページの「<span class="uicontrol">フィールド名</span>」テキストフィールドに、 
      <code>
        rank 
      </code>;「<span class="uicontrol">メタタグ名</span>」テキストフィールドに、 
      <code>
        rank 
      </code>;「<span class="uicontrol">データタイプ</span>」ドロップダウンリストで、「<span class="uicontrol">ランク</span>」を選択します。 その他のフィールドオプションは、そのままにします。 <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local">バックエンド検索CGIパラメーター</a>のクエリパラメーター<span class="codeph"> sp_sr </span>を参照してください。 </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">「<span class="uicontrol">追加</span>」をクリックします。 </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics指標に基づくランキングルールを作成するには </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> サイト検索/マーチャンダイジング内からのAdobe Analytics認証が設定されていることを確認します。 <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local">Adobe Analytics指標認証の設定</a>」を参照してください。 </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> 利用可能なレポートスイートを選択して追加します。 <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local">Adobe Analyticsレポートスイートの追加</a>」を参照してください。 </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> 新しいランキングルールの作成に使用するAdobe Analytics指標のリストを設定します。 <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local">レポートスイートのAdobe Analytics指標の編集</a>」を参照してください。 </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Webサイトページの初期Adobe Analytics指標を読み込みます。 <p><a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local">Adobe Analyticsデータの読み込み</a>を参照してください。 </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 1つ追加以上のランク付けルールを参照してください。

   [ランキングルールの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)を参照してください。

1. **[!UICONTROL regenerate your staged site index]**&#x200B;をクリックして、Webサイトの完全な再インデックスを実行します（**[!UICONTROL Index]**/**[!UICONTROL Full Index]**&#x200B;から）。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;の「ランク」列の値を確認し、ランキングルールが正しく適用されていたことを確認します。

## 年齢別のドキュメントのランク付けについて{#topic_770815CF1B2A491F83FF765871B6F1B8}

指数減衰関数を使用して、HTMLドキュメントをその年齢でランク付けできます。 減衰率は、選択した半減期定数を使用して指定します。減衰率は、値が初期値の半分になるまでに経過する必要がある時間の長さです。

年齢のランクは、次の2つの式に基づいています。

`K = -ln(2) / H`

`RANK = e^(K * T)`

変数`H`と`T`は、この関数の入力です。`H`は半減期が望ましい期間で、`T`はドキュメントの年齢（秒単位）です。 `K` は、半減期を計算した値で、指定し `RANK` た年齢値の指数減衰を表します。結果の値は0 ～ 1です。 新しいドキュメントのランクの値は、古いドキュメントのランクの値に比べて1に近い値になります。 理論上、ドキュメントは0の値に到達しないはずですが、丸めエラーは結果を0にする可能性があります。

## 年齢のランク{#section_D716507D589442C6B7848892BD28F966}を使用するための要件

* アカウントは、ランキングに対して正しく設定されている必要があります。 設定されていない場合は、[ランキング](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)の設定を参照してください。
* HTMLドキュメントには、生年月日、タイムスタンプとしての開始を表すHTML metaタグフィールド、またはその他の意味のある日付値が含まれている必要があります。
* ランキングルールページまたはランキングルールの編集ページで指定され追加た特殊な組み込み関数`search_get_age_rank()`を使用して、ドキュメントの年齢ランクを計算します。 次の節では、年齢ランキング関数の一般的な使用方法について詳しく説明します。 また、年齢ランク機能の例も示されています。

## ランキングルールページまたは追加ランキングルールの編集ページ{#section_34BC5276F2AB4419AD92872A397CA0AF}でsearch_get_age_rank ()を使用

次のように`search_get_age_rank()`を指定します。

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* 誕生日 — ファイルの生年月日または開始日は、フィールドの日付形式に従って日付形式の文字列にする必要があります。 `{field_name}`のように、この日付形式の文字列はフィールド参照である必要があります。
* Half_Life — 半減期は、値が初期値の半分になるまでに経過する必要がある時間です。 この値は日数で表し、整数または浮動小数点数です。
* Default_Rank — デフォルトランクは、生年月日が無効な場合や日付が未来の場合に、セーフティネットとして使用されます。 関連するメタデータフィールドにも有効なデフォルト値が含まれている場合は、このデフォルト値を使用できません。 この値は、浮動小数点数または整数です。 デフォルト値が使用されている問題が発生した場合の推奨事項については、以下を参照してください。

[ランキングルールの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)を参照してください。

[ランキングルールの編集](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)を参照してください。

**例**

次の例では、

`search_get_age_rank({birthdate}#28#0.20)`

ドキュメントの`birthdate`フィールドに含まれる日付は、タイムスタンプとして渡されます。 半減期は28日だ。 日付が無効な場合、デフォルトのランキング値は0.20です。

[ランキングルールの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)のオプションの表を参照してください。

ランキングルールページまたはランキングルールを編集ページの「値/ランク」セクション追加では、`search_get_age_rank`はカスタムルールでのみ使用できます。 したがって、必ず値/ランクドロップダウンリストから「**カスタム**」を選択してください。 ルールで年齢ランク関数を使用する場合、ルールの値の部分にスペースを含めることはできません。 関数の引数内または引数間にスペースがないことを確認してください。 また、数学演算子や条件演算子の間にスペースはありません。

値/ランクのルールの例を次に示します。値/ランクのルールは、テキストフィールドに関連付けられたルールです。

`regexp .* search_get_age_rank({other_field}#365#0.20)`

この例では、`other_field`に日付値が含まれていると想定しています。 このフィールドがそれ自体が日付型フィールドではない場合、この値は、事前定義された日付フィールドに関連付けられた日付形式を使用して解釈されます。 それ以外の場合は、このフィールドの日付形式が使用されます。 この値/ランクのエントリは、ルールのデータソースで識別されるドキュメントのフィールドが空ではなく、関数の戻り値(0 ～ 1)が割り当てられたランクである場合に常に使用されます。

数値フィールドに関連付けられたルールの場合、特に日付フィールドを使用します。

`9999999999 search_get_age_rank({other_field}#365#0.20)`

各ドキュメントが処理されると、`other_field`の値はUnixの「エポック」形式に変換され、フィールドの日付形式の定義が使用されます。 この値は`search_get_age_rank()`呼び出しで使用されます。 「エポック」の値が99999999999（少なくとも現在は）未満の場合、Ruleは関数の戻り値(0 ～ 1)をランクとして単に指定します。

上記の両方の例で、ルールのデータソースは、この場合`search_get_age_rank()`関数(`other_field`)で使用されるフィールドと同じであることが一般的です。

## 年齢のランクをランキングルール{#section_A86D909687CC45E19D4EA7A4A9283F28}に統合する例

次の例は、年齢のランクをランキングルールに統合する方法を示しています。 この例では、年齢ランク関数の生の結果とランク付けルールの結果も示しています。 この例では、次のことを前提としています。

* クロールされるWebページには、「birstdate」という名前のHTMLメタタグが含まれています。 このタグのコンテンツは、ドキュメントに関連するタイムスタンプです。
* メタデータ定義には、誕生日タグ用に定義されたメタタグフィールドがあります。 このフィールドは「日付」と入力します。

**ランキングルール**

「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」を参照してください。

次に、新しいランキングルールを追加します。 ルールは、ドキュメントの「誕生日」フィールドを使用するように定義されます。 次のプロパティセットを持つ新しいランキングルールが追加されます。

* データソースの種類：メタタグ
* データソース名：誕生日
* 重み付け/条件：10 — 最大重要度
* 値/ランク：999999999search_get_age_rank({birthdate}#14#0.10)
* デフォルトランク：-1

この規則はいくつかのことを行う。 ルールの重み付けは10に設定されます。 ランクの値は、年齢ランク関数の結果（0 ～ 1の値）です。 `search_get_age_rank()`ではスペースを使用できません。 また、「誕生日」フィールドは中括弧で囲まれています。 最後に、このルールを保存すると、値/ランク定義のコンマは`#`文字に置き換えられます。この動作は正常です。

**結果の表示**

データ表示機能を使用すると、年齢ランク関数の結果をすばやく確認できます。 適切追加なMetadataフィールド。 この例では、`age_val`と`myrank`が、データ表示に追加する必要がある2つのメタデータフィールドです。 `myrank`フィールドは、年齢のランクがランキング値にどのように影響するかを示します。 `age_val`フィールドは、そのドキュメントの指数減衰関数の生の出力を示します。

## デフォルト値 {#section_CB109EF78F914E92955D512ACFC3310E}

次の3つのデフォルト値は、関数`search_get_age_rank()`に関連しています。

* `search_get_age_rank()`関数自体に入力できるデフォルト値です。
* ランク付けルールのデフォルトのランク値です。
* メタデータ定義のデフォルト値。

失敗の発生場所に応じて、異なるデフォルト値が取得される場合があります。

例えば、ランキングとフィルタリングが適切に実装されている場合、メタデータ定義のデフォルト値は発生しません。 このデフォルト値は、そのメタデータフィールドに有効なコンテンツまたは既知のコンテンツが存在しない場合の最後のリゾート値です。 ランキングルールのデフォルト値は、`search_get_age_rank()`が独自の関連タグを参照していて、ドキュメントにタグがない場合に表示される場合があります。 この場合、このルールはルールのデフォルト値に直接適用されます。 年齢ランク関数が別のランク付けルールのタグを参照している場合、参照先のタグがないか無効な場合は、その年齢ランク関数に渡すデフォルト値が使用される可能性があります。

## ランキングルールの追加{#task_A132789FD4E5423DAD090DCDA7311E8A}

[!DNL Ranking Rules]を追加すると、各Webページのコンテンツに基づいて、検索結果内でのWebページの相対的な配置に影響を与えることができます。

[ランキング](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)の設定を参照してください。

**ランキングルールを追加するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. （オプション）ルールグループを作成し、ルールをグループに追加した場合は、[!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストで、編集するルールを含むルールグループを選択します。

   [ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。
1. [!DNL Define Ranking Rules]ページで、**[!UICONTROL Add Rule]**&#x200B;をクリックして新しいランキングルールを追加するか、ルールセットへの参照を追加します。
1. [!DNL Add Ranking Rule]ページで、必要なオプションを設定します。 アスタリスク(*)が付いているフィールドは必須です。

   選択するデータソースタイプは、[!DNL Data Source Name]ドロップダウンリストで選択できる選択肢に影響します。 例えば、データソースのタイプとして&#x200B;**[!UICONTROL Meta Tag]**&#x200B;を選択した場合、データソース名はWebサイトページ上のメタタグの名前を参照します。 **[!UICONTROL Adobe Analytics Metric (Number)]**&#x200B;を選択した場合、データソース名は、レポートスイートで選択したAdobe Analytics指標名の1つを参照します。この指標名は、サイト検索/マーチャンダイジングの&#x200B;**[!UICONTROL Edit Adobe Analytics Metrics]**&#x200B;ページに表示されます。

   「[レポートスイートのAdobe Analytics指標の編集](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)」を参照してください。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>データソースタイプ </p> </td> 
      <td colname="col2"> <p>このランキングルールへの入力として使用されるデータソースの特性を決定します。 </p> <p>選択できるデータソースの種類は次のとおりです。 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> メタタグ  </span> <p> このルールは、Webサイトページ上の名前付きのmetaタグ内に格納される数値データまたはテキストデータに基づきます。 </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Adobe Analytics指標（数値）  </span> <p>このルールは、サイトページに関連付けられた数値のAdobe Analytics指標に基づきます。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Data Source Name </p> </td> 
      <td colname="col2"> <p>データソースタイプとして「<span class="uicontrol"> Meta Tag </span> 」を選択した場合、これはWebサイトのページ内にあるmetaタグの名前になります。 ドロップダウンメニューの名前は、設定/メタデータ/定義で設定した定義済みのメタデータ値のリストに基づいています。 </p> <p>「<a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita">新しいmetaタグフィールドの追加</a>」を参照してください。 </p> <p>データソースタイプとして「Adobe Analytics指標（数値）」を選択した場合、これはAdobe Analytics指標の名前です。 ドロップダウンメニューの名前は、設定/Adobe Analytics/指標/編集で設定した、使用可能なAdobe Analytics指標を定義したリストに由来します。 </p> <p>「<a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local">レポートスイートのAdobe Analytics指標の編集</a>」を参照してください。 </p> <p>選択したAdobe Analytics指標名が<span class="uicontrol">設定</span>/<span class="uicontrol">メタデータ</span>/<span class="uicontrol">定義</span>でまだ定義されていない場合は、テキストフィールドと追加ボタンが表示されます。 メタデータフィールド名を入力し（メタデータフィールド名は20文字以内にする必要があります）、<span class="uicontrol"> 追加 </span>をクリックします。 </p> <p>複数のAdobe Analyticsキーを持つページが見つかった場合、複数の製品を表示する製品ページと同様に、複合スキームではそのページに関連付けられた複数のAdobe Analytics指標値の処理方法を指定します。 次のいずれかを選択します。 </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> 合計 </span> <p>指標値の合計を返します。 </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> 平均 </span> <p>値の平均（値の数で割った合計）を返します。 </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> 最大 </span> <p>値の最大値を返します。 </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> 最初 </span> <p>最初のキーに対応する値を返します。 </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> 最後 </span> <p>最後のキーに対応する値を返します。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重み付け/条件 </p> </td> 
      <td colname="col2"> <p>単純な単一のルール重み付け番号、またはルール重み付け番号とテスト条件のペアのリストが含まれます。 </p> <p>ルール重み付け番号は1 ～ 10の値で、ドキュメントの全体的なランクを決定する際に、このランク付けルールが他のランク付けルールに対してどれだけ重要かを示します。 ルールの重み付けが高いほど、重要度が高いことを示します。 重み付けが0の場合、ルールは無視されます。 </p> <p>ドロップダウンリストから「<span class="uicontrol">カスタム</span>」を選択し、ルール重み付け/テスト条件のペアのリストを定義して、様々なページのルール重み付けをカスタマイズします。 テスト条件は、データソースの値のテストに使用されるPerlの一部、またはカスタムフィルタースクリプト内で定義されるグローバル変数(例えば、次の例のように、price、brand、season、page表示ー)です。 テスト条件が「true」と評価された場合は、関連付けられたルール重み付けの値が適用されます。 テスト条件が「false」に評価された場合、リスト内の次の条件が評価されます。 <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>上のカスタム作成重み付け/条件の例では、最初のテスト条件が「true」に評価された場合にルール重み付け0が適用されます。つまり、価格に50より大きい値が含まれ、ブランドには「Kuhl」が含まれます)。 最初のテスト条件が「false」と評価された場合、次の条件が評価されます。 前の条件に一致しなかった場合は、ルール重み付け5が割り当てられます。 </p> <p>常に、リストの最後に条件を指定しないルール重み付けを指定する必要があります。 この操作を行わない場合、「true」と評価される条件が1つもない場合、ルールでは0の重み付けが取得されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>値/ランク </p> </td> 
      <td colname="col2"> <p>組み込みのランク付け関数の1つ、または可能なデータソースのコンテンツと目的のランクで構成されます。 </p> <p>「データソースタイプ」に「<span class="uicontrol">Adobe Analytics指標（数値） </span>」を選択した場合は、次のオプションを含むドロップダウンリストが表示されます。 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> 順序による自動ランク付け（デフォルト）  </span> <p>Adobe Analytics指標に従って、ドキュメントの相対的な位置に基づいてランクを計算します。 例えば、ドキュメントの位置が上位のドキュメントに近いほど、上位のランクが高くなります。 </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> 値による自動ランク付け  </span> <p>Adobe Analytics指標に従って、ドキュメントの相対値に基づいてランクを計算します。 例えば、ドキュメントの値が上位のドキュメントの値に近いほど、上位の値に近いほどランクが高くなります。 </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol">カスタム</span> <p>カスタム設定を指定します。 例えば、「ブランド」という名前のデータソースには、特定の製品のブランド名を含めることができます。 各ブランドのランクと共にリストすることで、各ブランドの相対的な重要度を指定できます。 </p> </li> 
      </ul> </p> <p>自動ランクの計算から返されるランクの値は、0.0（最低）～ 1.0（最高）の範囲です。 設定/メタデータ/定義の下の「ランク」フィールドに定義されている範囲に従って調整されるわけではありません。 </p> <p>次の例では、特定の検索結果のブランドデータソースが「DKNY」と完全に一致する場合、その結果に適用されるランクは0.5です。それ以外の場合、ブランドが「Levis」の場合、適用されるランクは0.1です。データソースのコンテンツは設定値と一致する必要があります。 つまり、データソースのコンテンツが「Levis Corp.」の場合、値「Levis」とは一致しません。 大文字と小文字は区別されないので、「DKNY」は「dkny」と「Dkny」に一致します。<code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>より高度なオプションとして、値を正規式として指定できます。 例えば、サイトの一部のページに「Levis」のブランド値が含まれ、他のサイトのページに「Levis jeans」のブランド値が含まれているとします。 キーワードと共に指定された正規式を使用できます 
      <code>
        regexp 
      </code>. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>を参照してください。 </p> <p>次の例では、ブランドコンテンツ「Levis jeans」を含む検索結果ドキュメントに0.1のランクが割り当てられています。標準的な比較と同様に、正規式では大文字と小文字が区別されません。<code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトランク </p> </td> 
      <td colname="col2"> <p> 指定した値のいずれにも一致しない検索結果ドキュメントに適用するランクを指定します。 上記の例では、「ギャップ」が定義された値のいずれにも一致しないので、「ブランド」データソースに「ギャップ」が含まれる検索結果ドキュメントには、デフォルトのランク値が割り当てられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メモ </p> </td> 
      <td colname="col2"> <p>作成し追加たランキングルール定義またはルールグループ定義に関連する情報。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   有効なランク値の範囲は、次のように、通常は —1.0 ～ 1.0です。

   * `-1.0` は「最小ランク」です（検索結果の下位に表示）。
   * `0.0` は「中立ランク（検索結果の順序を変更しない）」です。
   * `1.0` は「最大ランク」です（検索結果の値が高いほど表示されます）。

   定義されたランクは、すべてのルールで同じ範囲内にある必要があります。 また、ランク範囲は、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;の下の「ランク」フィールドに定義されている範囲と一致する必要があります。

   「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」を参照してください。

   [ランキングルールの編集](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)も参照してください。
1. クリック **[!UICONTROL Add]**.
1. ルールの追加の結果をプレビューするには、**[!UICONTROL regenerate your staged site index]**&#x200B;をクリックして、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールの編集{#task_5EBF55A43D6545FEA46BAE5E586FA275}

既に追加済みの既存のランキングルールを編集できます。

[ランキング](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)の設定を参照してください。

**ランキングルールを編集するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. （オプション）ルールグループを作成し、そのグループにルールを追加した場合は、**[!UICONTROL Define Ranking Rules]**&#x200B;ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストで、編集するルールを含むルールグループを選択します。

   [ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。
1. 表の&#x200B;**[!UICONTROL Actions]**&#x200B;列ヘッダーの下で、変更するデータソース名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Ranking Rule]ページで、必要なオプションを設定します。 アスタリスク(*)が付いているフィールドは必須です。

   [ランキングルールの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. ルール編集の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルール{#task_742A3BCC2A6E4164BE84CC7408807EBB}の削除

不要になったランキングルールは削除できます。

[ランキング](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)の設定を参照してください。

[ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。

**ランキングルールを削除するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. （オプション）ルールグループを作成し、そのグループにルールを追加した場合は、[!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストで、削除するルールを含むルールグループを選択します。
1. 表の&#x200B;**[!UICONTROL Actions]**&#x200B;列ヘッダーの下で、変更するデータソース名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Ranking Rule]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。

   [!DNL Define Ranking Rules]ページに戻ります。
1. ルールの削除の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールグループ{#task_B65081B3CC9E4330A7FEE77B7BCD36C8}の追加

「ランク」タイプのmetaタグを複数定義した場合は、様々なランクフィールドの計算に使用するルールの集合を個別に作成できます。 ランキングルールグループを追加して、定義済みの「ランク」フィールドの1つに割り当てることができます。

通常、ルールグループには、追加した1つ以上のルールが含まれます。 ただし、ルールグループは他のルールグループを参照することもできます。 例えば、1つ以上のルールグループを作成し、各グループによく使用されるルールを追加できます。 その後、複数のランクの計算中に、これらのルールが共有されます。

「[ランキングルールグループの編集](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)」を参照してください。

[ランキングルールグループの削除](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)を参照してください。

[ランキングルールグループの確認](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E)を参照してください。

**ランキングルールグループを追加するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. [!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストの右にある&#x200B;**[!UICONTROL Add]**&#x200B;をクリックします。
1. [!DNL Add Ranking Rule Group]ページの&#x200B;**[!UICONTROL Rule Group Name]**&#x200B;フィールドに、新しいルールグループの一意の名前を入力します。
1. **[!UICONTROL Rank Field Name]**&#x200B;ドロップダウンリストで、新しいルールグループに関連付けるランクメタデータフィールド名を選択します。 ランクを割り当てない場合は、**[!UICONTROL None]**&#x200B;を選択します。

   ランクフィールド名のリストは、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;に追加されたメタデータ定義に基づいています。

   [新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)のオプションの表を参照してください。
1. クリック **[!UICONTROL Add]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールグループ{#task_D3EC0437E47144BC9E754FEF99C725E5}の編集

既存のランキングルールグループの設定を編集できます。

[ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。

**ランキングルールグループを編集するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. [!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストの右にある&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Ranking Rule Group]ページの&#x200B;**[!UICONTROL Rule Group Name]**&#x200B;フィールドに、ルールグループの一意の名前を入力します。
1. **[!UICONTROL Rank Field Name]**&#x200B;ドロップダウンリストで、ルールグループに関連付けるランクメタデータフィールド名を選択します。 ランクを割り当てない場合は、**[!UICONTROL None]**&#x200B;を選択します。

   ランクフィールド名のリストは、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;に追加されたメタデータ定義に基づいています。

   [新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールグループ{#task_BE5BE01F377843BEA9846E094A07F2EA}の削除

不要になったまたは使用しなくなったランキングルールグループは削除できます。 グループを削除すると、そのグループに追加されたルールもすべて削除されます。 デフォルトの「Ranking Rules」グループは削除できません。

削除グループに含まれるルールグループの内容は削除されません。これらのグループへの参照のみが削除されます。

変更が検索結果に正しく反映されるように、Webサイトのインデックスを再作成してください。

[ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。

**ランキングルールグループを削除するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. [!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストで、削除するグループを選択します。
1. **[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストの右側にある&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Ranking Rule Group]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールグループの確認{#task_5694459D050C4254A25186038CD66B6E}

ランキングルールグループの概要を使用すると、各グループのランクフィールド名、関連するデータソースおよび重み付けを表示できます。

[ランキングルールグループの追加](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)を参照してください。

**ランキングルールグループを確認するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. [!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストの右にある&#x200B;**[!UICONTROL Overview]**&#x200B;をクリックします。
1. [!DNL Ranking Rule Groups Overview]ページで、**[!UICONTROL Close]**&#x200B;をクリックして[!DNL Define Ranking Rules]ページに戻ります。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールのテスト{#task_56F64EE7ED5B42E481F0990A9DD98ADB}

設定したランキングルール定義に適したURLテストを指定できます。 計算に使用される指標と計算されたランクの値が表示されます。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

**ランキングルールをテストするには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Edit Rules]**&#x200B;をクリックします。
1. [!DNL Define Ranking Rules]ページの&#x200B;**[!UICONTROL Test URL]**&#x200B;領域に、Webサイト上のWebページのURLを入力します。
1. クリック **[!UICONTROL Test]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ランキングルールに関連付けられた重み付けの調整{#task_3CB6FC92A66F4D99874A42D55825DB64}

個々のランキングルールの相対的な貢献度、およびランキングの最終的な検索結果に対する貢献度を変更できます。

ランキングが定義されていない場合、**[!UICONTROL Adjust Ranking Weights]**&#x200B;ページのルールと関連性スライダーバーの&#x200B;**[!UICONTROL Natural Relevance]**&#x200B;側で検索結果が100%になります。 このバランスは、単に検索結果が検索用語のみに基づいて並べられることを意味します。

ランキングを定義すると、関連付けられたランクメタデータフィールドに関連値(1 ～ 10)が割り当てられます。 値が1の場合、計算されたランクは検索結果の順序の10%を占め、残りの90%が自然関連性を占めます。

ルールグループに複数のルールが定義されている場合は、各ルールの重み付け値によって、そのルールの結果が計算されたランクの合計にどの程度影響するかが決まります。 例えば、自然な関連性が80%で、関連付けられたランクフィールドの関連性が2であるとします。 また、次の2つのルールを定義しています。1つは重み付け3、2つは重み付け7です。 この場合、最終結果に対する最初のルールの貢献度は6%((3 / (3+7)) * 20%)です。 最終結果に対する2番目のルールの貢献度は14% ((7 / (3+7)) * 20%)です。

**ランキングルールに関連付けられた重み付けを調整するには**

1. 製品メニューで、**[!UICONTROL Rules]**/**[!UICONTROL Ranking Rules]**/**[!UICONTROL Adjust Weights]**&#x200B;をクリックします。
1. [!DNL Adjust Ranking Weights]ページの&#x200B;**[!UICONTROL Select Rule Group]**&#x200B;ドロップダウンリストで、ランクの重み付けを調整するグループを選択します。
1. スライダをドラッグして、対応する貢献度の値を変更します。

   円グラフには、変更内容がグラフで反映されます。
1. クリック **[!UICONTROL Save Changes]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   [ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   [ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
