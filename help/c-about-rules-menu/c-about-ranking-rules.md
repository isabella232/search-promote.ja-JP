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
source-git-commit: f4f69e6bdb37fb39045f8f25cffa4bf616834e54

---


# ランキングルールについて{#about-ranking-rules}

ランキングルールを使用すると、含まれるメタタグコンテンツと関連するAdobe Analytics指標に基づいて、顧客の検索結果の相対的な位置やランクを制御できます。

## ランキングルールの使用 {#concept_F555C076759B4E81B925441CFE707397}

各ドキュメントのコンテンツに基づいて、検索結果内でのドキュメントの相対的な配置に影響を与えるランキングルールを定義します。 ランキングルールは、メタタグコンテンツ、Adobe Analytics指標（アカウントがAdobe Analyticsで機能するように設定されている場合）またはAdobe Analytics HBX指標（アカウントがAdobe Analytics HBXで機能するように設定されている場合）に基づいて設定できます。

特定のブランド名や価格など、目的の特性を持つメタタグを含むWebページや、望ましいAdobe Analyticsの主要業績評価指標を持つWebページ（個別ビューアなど）を含まないWebページよりも高いランクを受け取るように設定できます。 「望ましい」特性は、ランキングルールを追加または編集し、Webサイトのインデックスを再作成することで簡単に更新できます。

タイプ「rank」のmetaタグが複数定義されている場合は、様々なランクフィールドの計算に使用するルールのコレクションを個別に作成できます。 ランキングルールグループを追加し、定義した「ランク」フィールドの1つに割り当てることができます。 通常、ルールグループには1つ以上のルール定義が含まれますが、他のルールグループも参照できるので、複数のランクの計算時に共有される、一般的に使用される1つ以上のルールグループを作成できます。

ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。

正のランク値を指定すると、検索結果がトップに近づきます。負のランク値を指定すると、検索結果が検索結果の一番下に降格されます。 ランク付けの値の通常の範囲は1.0で、これは検索結果内の最大プロモーションです。-1.0は最大デモーションです。 メタデータ定義の「ランク」フィールドを編集してこの範囲をカスタマイズできますが、通常、このタイプのカスタマイズは不要です。

定義につ [いてを参照](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620)。

設定/メタデータ/定義で複数のランクフィールドを定義した場合は、各ランクフィールドに1つずつ、追加のランクルールのセットを作成するオプションがあります。 ランクフィールドに直接関連付けることなく、追加のランキングルールのセットを定義できます。 この柔軟性により、1つ以上のランク値の計算で共有できる共通ルールのセットを作成できます。

**重要**:ランキングルールを使用する前に、いくつかのアカウント設定手順を実行する必要があります。

ランキングの [設定を参照](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## ランキングの設定 {#task_4CEBC13925B047FC95BDC217B48089C5}

ランキングルールを使用する前に、いくつかのアカウント設定手順を実行する必要があります。

**ランクを設定するには**

1. 次の中から選択します。

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
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> 製品メニューで、設定/メタデ <span class="uicontrol"> ータ/ </span> 定義 <span class="uicontrol"> をク </span> リッ <span class="uicontrol"> クしま </span>す。 </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> 定義ページで、「新しいフィールドの追加」 <span class="uicontrol"> をクリックしま </span>す。 </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> フィールドの追加ページの「フィールド名」テ <span class="uicontrol"> キストフィ </span> ールドに、次のように入力します。 
      <userinput>
        ランク 
      </userinput>;「メタタ <span class="uicontrol"> グ名」テキ </span> ストフィールドに、 
      <userinput>
        ランク 
      </userinput>;「データタ <span class="uicontrol"> イプ」ド </span> ロップダウンリストで、「ランク」を <span class="uicontrol"> 選択しま </span>す。 その他のすべてのフィールドオプションはそのままにします。 <p>バックエンド検索CGIパラメ <span class="codeph"> ータのクエ </span> リパラメ <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> ータsp_srを参照してくださ </a>い。 </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">「<span class="uicontrol">追加</span>」をクリックします。 </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics指標に基づくランキングルールを作成するには </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> サイト検索/マーチャンダイジング内からAdobe Analytics認証が設定されていることを確認します。 <p>詳しくは、 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Adobe Analytics指標認証の設定を参照してくださ </a>い。 </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> 使用可能なレポートスイートを選択して追加します。 <p>詳しくは、 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Adobe Analyticsレポートスイートの追加を参照してくださ </a>い。 </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> 新しいランキングルールの作成に使用できるAdobe Analytics指標のリストを設定します。 <p>詳しくは、 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> レポートスイートのAdobe Analytics指標の編集を参照してくださ </a>い。 </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Webサイトページの初期Adobe Analytics指標を読み込みます。 <p>詳しくは、Adobe Analytics <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> データの読み込みを参照してくだ </a>さい。 </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 1つ以上のランキングルールを追加します。

   ランキング [ルールの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)い。

1. をクリ **[!UICONTROL regenerate your staged site index]** ックして、Webサイトの完全な再インデックスを実行します(> **[!UICONTROL Index]** から **[!UICONTROL Full Index]**)。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. >の「ランク」列の値を確認し、ランキングル **[!UICONTROL Settings]** ールが正し **[!UICONTROL Metadata]** く適 **[!UICONTROL Definitions]** 用されていることを確認してください。

## 年齢別のドキュメントのランク付けについて {#topic_770815CF1B2A491F83FF765871B6F1B8}

指数減衰関数を使用して、HTMLドキュメントをその年齢でランク付けできます。 減衰率は、選択した半減期定数を使用して指定します。この定数は、値が初期値の半分に下がるまでに経過する必要がある時間です。

年齢のランクは、次の2つの式に基づいています。

`K = -ln(2) / H`

`RANK = e^(K * T)`

変数と `H` は、 `T` この関数の入力です。は、 `H` 目的の半期の期間で、 `T` はドキュメントの年齢を秒単位で表します。 `K` は、計算された半減期で、指 `RANK` 定された年齢の値の指数減衰です。 結果の値は0 ～ 1です。 より新しいドキュメントのランク値は、より古いドキュメントに比べて1に近い値です。 理論的には、ドキュメントは0の値に到達しないはずですが、丸めエラーは結果を0にする可能性があります。

## 年齢のランクを使用するための要件 {#section_D716507D589442C6B7848892BD28F966}

* アカウントは、ランク付け用に既に正しく設定されている必要があります。 設定されていない場合は、ランキングの設定を参 [照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)い。
* HTMLドキュメントには、生年月日やタイムスタンプとしての開始を表すHTMLメタタグフィールド、またはその他の意味のある日付値が含まれている必要があります。
* 「ランキングルールの追加」また `search_get_age_rank()`は「ランキングルールの編集」ページで指定された特殊な組み込み関数を使用して、ドキュメントの年齢のランクを計算します。 次の節では、年齢のランク付け関数の一般的な使用方法について詳しく説明します。 また、年齢のランク付け機能を示す例も示されています。

## Using search_get_age_rank () on the Add Ranking Rule page or Edit Ranking Rule page {#section_34BC5276F2AB4419AD92872A397CA0AF}

次のように `search_get_age_rank()` 指定します。

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* 誕生日 — ファイルの生年月日は、フィールドの日付形式に従って日付形式の文字列で指定する必要があります。 この日付形式の文字列は、のようにフィールド参照である必要がありま `{field_name}`す。
* Half_Life — 半減期は、値が初期値の半分に下がるまでに経過する必要がある時間です。 この値は日数で表し、整数または浮動小数点数です。
* Default_Rank：デフォルトのランクは、生年月日が無効な場合や未来の日付の場合に、セーフティネットとして使用されます。 関連するメタデータフィールドにも有効なデフォルト値が含まれている場合は、このデフォルト値を使用できません。 ここでの値は、浮動小数点数または整数です。 デフォルト値が使用されている問題が発生した場合は、以下を参照してください。

ランキング [ルールの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)い。

See [Editing a ranking rule](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**例**

次の例では、

`search_get_age_rank({birthdate}#28#0.20)`

ドキュメントのフィールドに含まれる日 `birthdate` 付がタイムスタンプとして渡されます。 半減期は28日。 日付が無効な場合、デフォルトのランキング値は0.20です。

ランキングルールの追加のオプションの [表を参照してください](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)。

ランキングルールの追加ページまたはランキングルールの編集ページの「値/ランク」セクションでは、カスタム作成のル `search_get_age_rank` ールでのみ使用できます。 したがって、必ず「値/ランク」ドロ **ップダウン** ・リストから「カスタム」を選択してください。 ルールで年齢ランク関数を使用する場合、ルールの値の部分にスペースを含めることはできません。 関数の引数または引数の間にスペースがないことを確認します。 また、数学演算子と条件演算子の間にスペースはありません。

次に、値/ランクのルールの例を示します。このルールは、テキストフィールドに関連付けられたルールです。

`regexp .* search_get_age_rank({other_field}#365#0.20)`

この例では、に日付値が含ま `other_field` れていることを前提としています。 このフィールド自体が日付型フィールドではない場合、この値は、事前定義された日付フィールドに関連付けられた日付形式を使用して解釈されます。 それ以外の場合は、このフィールドの日付形式が使用されます。 この値/ランクエントリは、ルールのデータソースで識別されるドキュメントのフィールドが空ではなく、関数の戻り値(0 ～ 1)が割り当てられたランクである場合に常に使用されます。

数値フィールドに関連付けられたルールの場合、具体的には日付フィールド：

`9999999999 search_get_age_rank({other_field}#365#0.20)`

各ドキュメントの処理時に、の値は、フ `other_field` ィールドの日付形式の定義を使用してUnixの「エポック」形式に変換されます。 この値は呼び出しで使用され `search_get_age_rank()` ます。 すべての「エポック」値が9999999999（現時点では最低）未満なので、Ruleは関数の戻り値(0 ～ 1)をランクとして指定します。

上記の例では、ルールのデータソースが、関数で使用されているフィールドと同じであるこ `search_get_age_rank()` とが `other_field` 一般的です。

## 年齢のランク付けをランキングルールに統合する例 {#section_A86D909687CC45E19D4EA7A4A9283F28}

次に、年齢のランクをランキングルールに統合する方法の例を示します。 この例では、年齢ランク付け関数の生の結果とランク付けルールの結果も示しています。 この例では、次の点を想定しています。

* クロールされるWebページには、「誕生日」というHTMLメタタグが付いています。 このタグのコンテンツは、ドキュメントに関連するタイムスタンプです。
* メタデータ定義には、誕生日タグ用に定義されたメタタグフィールドが含まれます。 このフィールドは「日付」と入力します。

**ランキングルール**

詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。

次に、新しいランキングルールを追加します。 ルールは、ドキュメントで「誕生日」フィールドを使用するように定義されています。 次のプロパティセットを持つ新しいランキングルールが追加されます。

* データソースの種類：メタタグ
* データソース名：誕生日
* 重み/条件：10 — 最大重要度
* 値/ランク：99999999search_get_age_rank（{誕生日}#14#0.10）
* デフォルトのランク：-1

この規則はいくつかのことを行う。 ルールの重みは10に設定されます。 ランクの値は、0 ～ 1の値である年齢ランク関数の結果です。 ではスペースを使用できませ `search_get_age_rank()`ん。 また、「誕生日」フィールドは中括弧で囲まれています。 最後に、このルールを保存すると、値/ランク定義のコンマが文字で置き換えら `#` れます。この動作は正常です。

**結果の表示**

データ表示機能を使用すると、年齢ランク関数の結果をすばやく確認できます。 適切なメタデータフィールドを追加します。 この例では、とは、 `age_val` デー `myrank` タビューに追加する必要のある2つのメタデータフィールドです。 このフィー `myrank` ルドには、年齢のランクがランク値にどのように影響するかが表示されます。 このフ `age_val` ィールドには、そのドキュメントの指数減衰関数の生の出力が表示されます。

## デフォルト値 {#section_CB109EF78F914E92955D512ACFC3310E}

関数には、次の3つのデフォルト値が含まれま `search_get_age_rank()`す。

* 関数自体に入力できるデフォル `search_get_age_rank()` ト値です。
* ランクルールのデフォルトのランク値。
* メタデータ定義のデフォルト値。

エラーの発生場所に応じて、異なるデフォルト値が取得される場合があります。

例えば、ランキングとフィルターが適切に実装されている場合、メタデータ定義のデフォルト値は発生しません。 このデフォルト値は、そのメタデータフィールドに対して有効なコンテンツまたは既知のコンテンツが存在しない場合の最後のリゾート値です。 が独自の関連タグを参照し、ドキュメント内にタグがな `search_get_age_rank()` い場合、ランキングルールのデフォルト値が表示される場合があります。 この場合、このルールはルールのデフォルト値に直接適用されます。 年齢ランキング関数が別のランキングルールのタグを参照している場合は、参照先のタグがないか無効な場合、その年齢ランキング関数に渡されるデフォルト値が使用される可能性があります。

## ランキングルールの追加 {#task_A132789FD4E5423DAD090DCDA7311E8A}

を追加すると、各Web [!DNL Ranking Rules] ページのコンテンツに基づいて、検索結果内でのWebページの相対的な配置に影響を与えることができます。

ランキングの [設定を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)い。

**ランキングルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. （オプション）ルールグループを作成し、ルールをグループに追加した場合は、ページのドロップダウンリストで、編集するルールを含むルールグループを [!DNL Define Ranking Rules]**[!UICONTROL Select Rule Group]** 選択します。

   ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。
1. ページで、 [!DNL Define Ranking Rules] をクリックし **[!UICONTROL Add Rule]** て新しいランキングルールを追加するか、ルールセットへの参照を追加します。
1. ページで、 [!DNL Add Ranking Rule] 必要なオプションを設定します。 アスタリスク(*)が付いたフィールドは必須です。

   選択したデータソースのタイプは、ドロップダウンリストで選択でき [!DNL Data Source Name] る選択肢に影響します。 例えば、「データソースの種類」 **[!UICONTROL Meta Tag]** として「データソース名」を選択した場合、Webサイトページ上のメタタグの名前がデータソース名として参照されます。 選択した場合、 **[!UICONTROL Adobe Analytics Metric (Number)]**&#x200B;データソース名は、サイト検索/マーチャンダイジングのページにある、レポートスイートで選択したAdobe Analytics指標名の1 **[!UICONTROL Edit Adobe Analytics Metrics]** つを参照します。

   「レポ [ートスイートのAdobe Analytics指標の編集」を参照してください](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)。

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
      <td colname="col2"> <p>このランキングルールへの入力として使用されるデータソースの特性を決定します。 </p> <p>次の中から選択できるデータソースの種類があります。 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> メタタグ </span> <p> このルールは、Webサイトページ上の名前付きのmetaタグ内に格納される数値データまたはテキストデータに基づきます。 </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Adobe Analytics指標（数値） </span> <p>このルールは、サイトページに関連付けられた数値のAdobe Analytics指標に基づきます。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Data Source Name </p> </td> 
      <td colname="col2"> <p>「データソー <span class="uicontrol"> スタイプ」 </span> で「メタタグ」を選択した場合、Webサイトのページ内にあるメタタグの名前です。 ドロップダウンメニューの名前は、設定/メタデータ/定義で設定された定義済みのメタデータ値のリストから得られます。 </p> <p>詳しくは、 <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> 新しいメタタグフィールドの追加を参照してくだ </a>さい。 </p> <p>データソースタイプとして「Adobe Analytics指標（数値）」を選択した場合、これはAdobe Analytics指標の名前です。 ドロップダウンメニューの名前は、設定/Adobe Analytics/指標/編集で設定した、使用可能なAdobe Analytics指標のリストから得られます。 </p> <p>詳しくは、 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> レポートスイートのAdobe Analytics指標の編集を参照してくださ </a>い。 </p> <p>選択したAdobe Analytics指標名が、設定/メタデータ/定義でま <span class="uicontrol"> だ定義さ </span> れていな <span class="uicontrol"> い場 </span><span class="uicontrol"></span>合、テキストフィールドと「追加」ボタンが表示されます。 メタデータフィールド名の名前を入力し（メタデータフィールド名は20文字以下にする必要があります）、「追加」をクリ <span class="uicontrol"> ックしま </span>す。 </p> <p>複数のAdobe Analyticsキーを持つページが見つかった場合、複数の製品を表示する製品ページと同様に、複合スキームは、そのページに関連付けられた複数のAdobe Analytics指標値を処理する方法を指定します。 次のいずれかを選択します。 </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> 合計 </span> <p>指標値の合計を返します。 </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> 平均 </span> <p>値の平均（値の数で割った合計）を返します。 </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> 最大 </span> <p>値の最大値を返します。 </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> 最初 </span> <p>最初のキーに対応する値を返します。 </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> 最後 </span> <p>最後のキーに対応する値を返します。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重み/条件 </p> </td> 
      <td colname="col2"> <p>単純な単一のルール重み付け番号、またはルール重み付け番号とテスト条件のペアのリストが含まれます。 </p> <p>ルールの重み番号は1 ～ 10の値で、ドキュメントの全体的なランクを決定する際に、このランク付けルールが他のランク付けルールに対してどの程度重要かを示します。 ルールの重みが高いほど、重要度が高くなります。 重みがゼロ(0)の場合、ルールは無視されます。 </p> <p>ドロップダ <span class="uicontrol"> ウン </span> リストから「カスタム」を選択し、ルールの重み/テスト条件のペアのリストを定義して、様々なページのルールの重みをカスタマイズします。 テスト条件は、データソース値のテストに使用されるPerlのフラグメント、またはカスタムフィルタースクリプト内で定義されるグローバル変数（例えば、次の例のように、価格、ブランド、季節、ページビュー）です。 テスト条件の評価結果が「true」の場合は、関連するルールの重みの値が適用されます。 テスト条件の評価結果が「false」の場合、リスト内の次の条件が評価されます。 <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>上記のカスタム作成の重み/条件の例では、最初のテスト条件が「true」と評価された場合に、ルールの重み0が適用されます。 つまり、価格に50を超える値が含まれ、ブランドには「Kuhl」が含まれます)。 最初のテスト条件が「false」と評価された場合、次の条件が評価されます。 以前の条件がいずれも満たされない場合、ルールの重み5が割り当てられます。 </p> <p>リストの最後には、条件を指定しないルールの重み付けを常に指定する必要があります。 これを行わない場合、「true」と評価される条件が1つもない場合、ルールの重みは0になります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>値/ランク </p> </td> 
      <td colname="col2"> <p>組み込みのランク付け関数の1つ、または可能なデータソースのコンテンツと目的のランクで構成されます。 </p> <p>データソースタ <span class="uicontrol"> イプとして「Adobe Analytics指標( </span> 数値)」を選択した場合は、次のオプションを含むドロップダウンリストが表示されます。 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> 順序による自動ランク付け（デフォルト） </span> <p>Adobe Analytics指標に従って、ドキュメントの相対的な位置に基づいてランクを計算します。 例えば、ドキュメントの位置が上位のドキュメントに近いほど、ランクが高くなります。 </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> 値による自動ランク付け </span> <p>Adobe Analytics指標に従って、ドキュメントの相対値に基づいてランクを計算します。 例えば、ドキュメントの値が上位のドキュメントの値に近いほど、ランクが高くなります。 </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol">カスタム</span> <p>カスタム設定を指定します。 例えば、「ブランド」という名前のデータソースには、特定の製品のブランド名が含まれている場合があります。 各ブランドの相対的な重要性を指定するには、そのランクと共にブランドをリストします。 </p> </li> 
      </ul> </p> <p>自動ランクの計算から返されるランクの値は、0.0（最低）～ 1.0（最高）の範囲です。 設定/メタデータ/定義の下の「ランク」フィールドに定義された範囲に従って調整されることはありません。 </p> <p>次の例では、特定の検索結果のブランドのデータソースが「DKNY」と完全に一致する場合、その結果に適用されるランクは0.5です。それ以外の場合、ブランドが「レビス」の場合、適用されるランクは0.1です。データソースのコンテンツは、設定値と一致する必要があります。 つまり、データソースのコンテンツが「Levis Corp.」の場合、値「Levis」とは一致しません。 大文字と小文字が区別されないので、「DKNY」は「dkny」と「Dkny」に一致します。 <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>より高度なオプションとして、値を正規表現として指定できます。 例えば、一部のサイトページに「Levis」のブランド値が含まれ、他のサイトページに「Levis jeans」のブランド値が含まれているとします。 キーワードと共に指定した正規表現を使用できます 
      <userinput>
        regexp 
      </userinput>。 </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してくださ </a>い。 </p> <p>次の例では、ブランドコンテンツ「Levis jeans」を含む検索結果ドキュメントに0.1のランクが割り当てられています。標準的な比較と同様、正規表現では大文字と小文字が区別されません。 <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのランク </p> </td> 
      <td colname="col2"> <p> 指定した値のいずれにも一致しない検索結果ドキュメントに適用するランクを指定します。 上の例では、「ギャップ」を含む「ブランド」データソースを持つ検索結果ドキュメントに、デフォルトのランク値が割り当てられています。これは、「ギャップ」が定義された値のいずれにも一致しないためです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メモ </p> </td> 
      <td colname="col2"> <p>作成したランキングルール定義またはルールグループ定義に関連する情報を追加します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   有効なランク値の範囲は、次のように、通常は —1.0 ～ 1.0です。

   * `-1.0` は「最小ランク」（検索結果の下部に表示）です。
   * `0.0` は「中立ランク（検索結果の順序は変更しない）」です。
   * `1.0` は「最大ランク」（検索結果の上位に表示）です。
   定義されたランクは、すべてのルールで同じ範囲内にある必要があります。 また、ランク範囲は、> >の下の「ランク」フィールドに定義されている範囲と一致する **[!UICONTROL Settings]** 必要が **[!UICONTROL Metadata]** ありま **[!UICONTROL Definitions]**&#x200B;す。

   詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。

   ランキングルール [の編集も参照してください](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)。
1. クリック **[!UICONTROL Add]**.
1. ルールの追加の結果をプレビューするには、をクリックして、ステージ **[!UICONTROL regenerate your staged site index]** されたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールの編集 {#task_5EBF55A43D6545FEA46BAE5E586FA275}

既に追加済みの既存のランキングルールを編集できます。

ランキングの [設定を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)い。

**ランキングルールを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. （オプション）ルールグループを作成し、そのグループにルールを追加した場合、ページのドロップダウンリストで、編集するルールを含むルールグループを **[!UICONTROL Define Ranking Rules]****[!UICONTROL Select Rule Group]** 選択します。

   ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。
1. 表の列見出しの下 **[!UICONTROL Actions]** で、変更するデ **[!UICONTROL Edit]** ータソース名をクリックします。
1. ページ [!DNL Edit Ranking Rule] で、必要なオプションを設定します。 アスタリスク(*)が付いたフィールドは必須です。

   ランキングルールの追加のオプションの [表を参照してください](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)。
1. クリック **[!UICONTROL Save Changes]**.
1. ルール編集の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールの削除 {#task_742A3BCC2A6E4164BE84CC7408807EBB}

不要になったランキングルールは削除できます。

ランキングの [設定を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)い。

ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。

**ランキングルールを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. （オプション）ルールグループを作成し、そのグループにルールを追加した場合、ページのドロップダウンリストで、削除するルールを含むルールグループを [!DNL Define Ranking Rules]**[!UICONTROL Select Rule Group]** 選択します。
1. 表の列見出しの下 **[!UICONTROL Actions]** で、変更するデ **[!UICONTROL Delete]** ータソース名をクリックします。
1. ページ上で、 [!DNL Delete Ranking Rule] をクリックしま **[!UICONTROL Delete]**&#x200B;す。

   ページに戻り [!DNL Define Ranking Rules] ます。
1. ルール削除の結果をプレビューするには、ステージングされたWebサイトインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールグループの追加 {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

「rank」タイプの複数のmetaタグを定義した場合は、様々なランクフィールドの計算に使用するルールのコレクションを個別に作成できます。 ランキングルールグループを追加し、定義した「ランク」フィールドの1つに割り当てることができます。

通常、ルールグループには、追加した1つ以上のルールが含まれます。 ただし、ルールグループは他のルールグループを参照することもできます。 例えば、1つ以上のルールグループを作成し、よく使用するルールを各ルールに追加できます。 その後、複数のランクの計算中にこれらのルールが共有されます。

ランキング [ルールグループの編集を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)い。

ランキング [ルールグループの削除を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)い。

ランキングル [ールグループの確認を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E)い。

**ランキングルールグループを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. ページ [!DNL Define Ranking Rules] のドロップダウンリストの右 **[!UICONTROL Select Rule Group]** 側で、をクリックします **[!UICONTROL Add]**。
1. ページの [!DNL Add Ranking Rule Group] フィールドに、 **[!UICONTROL Rule Group Name]** 新しいルールグループの一意の名前を入力します。
1. ドロップダ **[!UICONTROL Rank Field Name]** ウンリストで、新しいルールグループに関連付けるランクメタデータフィールド名を選択します。 ランク **[!UICONTROL None]** を割り当てない場合に選択します。

   ランクフィールド名のリストは、//で追加されたメタデータ定義に基づ **[!UICONTROL Settings]** いて表 **[!UICONTROL Metadata]** 示されま **[!UICONTROL Definitions]**&#x200B;す。

   新しいメタタグフィールドの追加のオ [プションの表を参照してください](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)。
1. クリック **[!UICONTROL Add]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールグループの編集 {#task_D3EC0437E47144BC9E754FEF99C725E5}

既存のランキングルールグループの設定を編集できます。

ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。

**ランキングルールグループを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. ページ [!DNL Define Ranking Rules] のドロップダウンリストの右 **[!UICONTROL Select Rule Group]** 側で、をクリックします **[!UICONTROL Edit]**。
1. ページの [!DNL Edit Ranking Rule Group] フィールドに、ル **[!UICONTROL Rule Group Name]** ールグループの一意の名前を入力します。
1. ドロップダ **[!UICONTROL Rank Field Name]** ウンリストで、ルールグループに関連付けるランクメタデータフィールド名を選択します。 ランク **[!UICONTROL None]** を割り当てない場合に選択します。

   ランクフィールド名のリストは、//で追加されたメタデータ定義に基づ **[!UICONTROL Settings]** いて表 **[!UICONTROL Metadata]** 示されま **[!UICONTROL Definitions]**&#x200B;す。

   新しいメタタグフィールドの追加のオ [プションの表を参照してください](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)。
1. クリック **[!UICONTROL Save Changes]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールグループの削除 {#task_BE5BE01F377843BEA9846E094A07F2EA}

不要になった、または使用しなくなったランキングルールグループを削除できます。 グループを削除すると、そのグループに追加されたルールもすべて削除されます。 デフォルトの「ランキングルール」グループは削除できません。

削除グループに含まれるルールグループの内容は削除されません。これらのグループへの参照のみが削除されます。

Webサイトのインデックスを再作成し、変更が検索結果に正しく反映されるようにしてください。

ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。

**ランキングルールグループを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. ページ [!DNL Define Ranking Rules] のドロップダ **[!UICONTROL Select Rule Group]** ウンリストで、削除するグループを選択します。
1. ドロップダウンリストの右 **[!UICONTROL Select Rule Group]** 側で、をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. ページ上で、 [!DNL Delete Ranking Rule Group] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールグループの確認 {#task_5694459D050C4254A25186038CD66B6E}

ランキングルールグループの概要を使用して、各グループのランクフィールド名、関連するデータソースおよび重み付けを確認できます。

ランキング [ルールグループの追加を参照してくださ](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)い。

**ランキングルールグループを確認するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. ページ [!DNL Define Ranking Rules] のドロップダウンリストの右 **[!UICONTROL Select Rule Group]** 側で、をクリックします **[!UICONTROL Overview]**。
1. ページ上 [!DNL Ranking Rule Groups Overview] のをクリックし **[!UICONTROL Close]** て、ページに戻り [!DNL Define Ranking Rules] ます。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールのテスト {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

設定したランキングルールの定義に適したURLテストを指定できます。 計算で使用される指標と、計算されたランクの値が表示されます。

[ランキングルールについて](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)を参照してください。

**ランキングルールをテストするには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Edit Rules]**。
1. ページ [!DNL Define Ranking Rules] の領域に、Webサ **[!UICONTROL Test URL]** イト上のWebページのURLを入力します。
1. クリック **[!UICONTROL Test]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ランキングルールに関連付けられた重みの調整 {#task_3CB6FC92A66F4D99874A42D55825DB64}

個々のランキングルールの相対的な貢献度と、最終的な検索結果に対するランキングの貢献度を変更できます。

ランキングを定義していない場合、検索結果はページのルールと関連性 **[!UICONTROL Natural Relevance]** スライダバーの横に100%表示され **[!UICONTROL Adjust Ranking Weights]** ます。 このバランスとは、検索結果が検索用語のみに基づいて並べ替えられることを意味します。

ランキングを定義すると、関連するランクメタデータフィールドに1 ～ 10の関連値が割り当てられます。 値が1の場合、計算されたランクが検索結果の順序の10%を占め、残りの90%が自然関連性を占めます。

ルールグループに複数のルールが定義されている場合、各ルールの重み値によって、そのルールの結果が計算されたランクの合計にどの程度影響するかが決まります。 例えば、自然関連性が80%で、関連するランクフィールドの関連性が2であるとします。 また、次の2つのルールを定義しました。重さ3、重さ7。 この場合、最終結果に対する最初のルールの貢献度は6%((3 / (3+7)) * 20%)です。 2番目のルールの最終的な結果への貢献度は14%((7 / (3+7)) * 20%)です。

**ランキングルールに関連付けられた重みを調整するには**

1. 製品メニューで//をクリ **[!UICONTROL Rules]** ックし **[!UICONTROL Ranking Rules]** ます **[!UICONTROL Adjust Weights]**。
1. ページの [!DNL Adjust Ranking Weights] ドロップダウ **[!UICONTROL Select Rule Group]** ンリストで、ランキングの重みを調整するグループを選択します。
1. スライダをドラッグして、対応する貢献度の値を変更します。

   円グラフには、変更内容がグラフで反映されます。
1. クリック **[!UICONTROL Save Changes]**.
1. ルールの追加の結果をプレビューするには、ステージングされたWebサイトのインデックスを再構築します。

   ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。
