---
description: メタデータメニューを使用して、検索定義とインデックスインジェクションをカスタマイズします。
solution: Target
subtopic: Metadata
title: メタデータメニューについて
topic-legacy: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
exl-id: 53d62da9-c5bd-4c4a-bb89-743704f66f7f
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '8028'
ht-degree: 1%

---

# メタデータメニューについて{#about-the-metadata-menu}

メタデータメニューを使用して、検索定義とインデックスインジェクションをカスタマイズします。

## 定義について {#concept_AE48035C210145169BE067D396975620}

[!DNL Definitions]を使用して、顧客が検索クエリを送信する際に考慮されるHTMLフィールドとメタデータフィールドの内容と関連性をカスタマイズできます。

事前定義済みのフィールドを編集できます。 または、メタデータタグのコンテンツに基づいて、新しいユーザー定義フィールドを作成することもできます。 各定義は、[!DNL Staged Definitions]ページの1行に表示されます。

[データビューについて](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)も参照してください。

## 新しいメタタグフィールドの追加 {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

独自のメタデータタグフィールドを定義して追加できます。

新しいメタタグ定義の効果をユーザーに表示する前に、サイトインデックスを再構築する必要があります。

**新しいメタタグフィールドを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページで、「**[!UICONTROL Add New Field]**」をクリックします。
1. [!DNL Add Field]ページで、必要なオプションを設定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p>フィールドの参照に使用する名前を指定します。 </p> <p>フィールド名は、次のルールに従う必要があります。 </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> 名前には英数字のみを使用できます。 </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> ダッシュは名前に含めることができますが、スペースは含まれません。 </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> 名前は20文字以内で入力できます。 </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> 名前は大文字と小文字が区別されませんが、入力したとおりに表示および保存されます。 </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> <span class="wintitle"> Staged Definitions </span>ページのテーブルに表示されるように、事前定義済みフィールドに存在する名前は使用できません。 </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> ユーザー定義のフィールド名の値に「any」という単語を使用することはできません。 </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> 定義済みフィールドの名前は編集できません。 </li> 
      </ul> </p> <p> フィールド名の例： </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> 作成者 </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublishDate </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> 何か異常な </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メタタグ名 </p> </td> 
      <td colname="col2"> <p>定義されたフィールドに関連付けられる内容を決定します。 </p> <p>名前のリストは255文字以内にする必要があります。 また、名前には、HTMLメタタグのname属性に使用できる任意の文字を含めることができます。 </p> <p>1つのフィールド定義に複数のメタタグを指定できます。 </p> <p>複数の値はコンマで区切る必要があり、任意のWebページで見つかる左端のメタタグ名が優先されます。 </p> <p>例えば、「auth」という名前のフィールドを定義したとします。 フィールド名には、関連するメタタグ「author, dc.author」が含まれます。 この場合、両方のメタタグがWebページに表示される場合、「author」メタタグのコンテンツのインデックスが作成され、「dc.author」のコンテンツを検索します。 </p> <p>ユーザー定義フィールドの定義には、メタタグ名が1つ以上必要です。 事前定義済みのフィールドには、メタタグを関連付ける必要はありません。 ただし、1つ以上のメタタグを指定した場合は、各タグの現在のデータソースがメタタグのコンテンツに優先されます。 </p> <p>例えば、メタタグ「dc.title」が事前定義の「title」フィールドに関連付けられている場合、「dc.title」メタタグのコンテンツは、 
      <code>
        &lt;title&gt; 
      </code>タグを使用します。 </p> <p>次に例を示します。 </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> 固有タグ </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>データタイプ </p> </td> 
      <td colname="col2"> <p>すべてのフィールドには、テキスト、数値、日付、バージョン、ランク、場所など、関連するデータタイプがあります。 このデータ型は、フィールドのコンテンツのインデックス付け、検索、およびオプションで並べ替えを行う方法を決定します。 </p> <p>フィールド定義を作成した後でデータ型を変更することはできません。 </p> <p>次の情報を使用して、フィールドに含まれる情報に関連するデータ型を選択します。 </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> テキスト </span> データタイプフィールドは文字列として扱われます。 </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> 数値デ </span> ータ型のフィールドは、整数または浮動小数点の数値として扱われます。 </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> 日付デ </span> ータタイプフィールドは、日付/時間指定子として扱われます。新しいフィールドを追加または編集する際に、使用可能な日付/時間形式をカスタマイズできます。 </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> バージ </span> ョンデータタイプのフィールドは、自由形式の数値データとして扱われます。例えば、1.2.3は1.2.2より前に並べ替えられます。 </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> ラン </span> クデータタイプフィールドは、検索結果のランキング/関連度の計算にさらに影響する点を除いて、「数値」タイプフィールドと同じように扱われます。 <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">ランキングルールについて</a>を参照してください。 </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> 場所デ </span> ータタイプのフィールドは、世界のどこでも物理的な場所として扱われます。使用できる場所の形式は次のとおりです。 <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> 5桁または9桁の郵便番号。DDDDDDまたはDDDDDD-DDDDの形式で表されます。各「D」は0 ～ 9桁の数字です。 </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> 3桁の市外局番。 </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> ±DDD.DDDD±DDDD.DDDDDの形式の緯度と経度のペア。最初の数値は緯度を、2番目の数値は経度を表します。 </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>許可リスト </p> </td> 
      <td colname="col2"> <p>データ型<span class="uicontrol"> Text </span>または<span class="uicontrol"> Number </span>が選択されている場合にのみ使用できます。 </p> <p>このフィールドのメタデータコンテンツで、区切られた値を別々にインデックス化します。 </p> <p>例えば、「許可リスト」が選択されている場合、コンテンツ「Red, Yellow, Green, Blue」は、1つではなく4つの個別の値として扱われます。 この処理は、範囲検索( 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code>または 
      <code>
        sp_q_exact 
      </code>)と 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code>および 
      <code>
        &lt;search-display-field-values&gt; 
      </code>. </p> <p>「バージョン」データ型が選択されている場合は使用できません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 動的ファセット </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>注意：この機能は、デフォルトでは有効になっていません。テクニカルサポートに連絡して、使用する際に有効化してください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたファセットを動的に設定します。 </p> <p>ファセットは、メタタグフィールドの上に構築されます。 メタタグフィールドは、低レベルで中核的なAdobeSearch&amp;Promote層です。 一方、ファセットはGS（ガイド付き検索）の一部で、AdobeSearch&amp;Promoteの上位レベルのプレゼンテーションレイヤーです。 ファセット自体のメタタグフィールドは、ファセットに関して何も知りません。 </p> <p><a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">動的ファセット</a>についてを参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外を許可 </p> </td> 
      <td colname="col2"> <p>このフィールドの重複排除を有効にするには、このオプションをオンにします。 つまり、検索時に、 
        <code>
          sp_dedupe_field 
        </code> CGIパラメータを検索します。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テーブル名 </p> </td> 
      <td colname="col2"> <p>指定されたフィールドを指定されたテーブル名に永続的に関連付けます。 </p> <p>コア検索のCGIパラメータやテンプレートタグ内でこのようなフィールドが言及されると、常にテーブル名が自動的に提供されます。 この機能を使用すると、テーブルの一致による動的ファセットを選択できますが、必要に応じて、動的でないファセットフィールドにも使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>リスト区切り文字 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">許可リスト</span>を選択した場合にのみ使用できます。 </p> <p>個々のリスト値を区切る文字を指定します。 複数の文字を指定でき、それぞれが値の区切り文字として扱われます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトで検索 </p> </td> 
      <td colname="col2"> <p>選択した場合、特定の検索クエリでフィールドが明示的に指定されていない場合でも、フィールドコンテンツが検索されます。 このオプションの選択を解除した場合、フィールドはリクエストがあった場合にのみ検索されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直更新フィールド </p> </td> 
      <td colname="col2"> <p> <p>注意：この機能は、デフォルトでは有効になっていません。テクニカルサポートに連絡して、使用する際に有効化してください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたフィールドを[垂直更新]フィールドに設定します。 </p> <p>「垂直更新」フィールドは、垂直更新プロセス（ <span class="uicontrol">インデックス</span> &gt; <span class="uicontrol">垂直更新</span> ）で更新される候補です。 垂直更新の実施方法により、フリーテキスト検索ではこれらのフィールドのコンテンツを検索できません。 このオプションをオンにすると、どのようなインデックス操作でも、このフィールドのコンテンツが「word」インデックスに追加されません。 また、「垂直更新」の操作中に、このフィールドを更新することもできます。 </p> <p>垂直更新について詳しくは、<a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">垂直更新について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>関連度 </p> </td> 
      <td colname="col2"> <p>事前定義済みフィールドとユーザー定義フィールドの関連度を編集できます。 </p> <p>関連度は1～10の尺度で指定する。 設定が1の場合、最も関連性が低く、10が最も関連性が高いことを意味します。 これらの値は、ソフトウェアが各フィールドでクエリが一致すると見なす場合に考慮されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>並べ替え </p> </td> 
      <td colname="col2"> <p>検索結果を指定されたフィールドで並べ替えるタイミングを、 
        <code>
          sp_s 
        </code> CGIパラメータを検索します。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>言語 </p> </td> 
      <td colname="col2"> <p>データタイプ<span class="uicontrol">ランク</span>、<span class="uicontrol">数値</span>、<span class="uicontrol">日付</span>が選択されている場合にのみ使用できます。 </p> <p>このフィールドの日付、数値、ランクの値をインデックス作成する際に適用される言語とロケールの規則を制御します。 </p> <p>アカウントの言語を適用するように選択できます（言語/単語と言語）。 または、各数値や日付値を含むドキュメントに関連付けられた言語、または特定の言語を適用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>日付の形式 </p> </td> 
      <td colname="col2"> <p>データ型<span class="uicontrol">日付</span>が選択されている場合にのみ使用できます。 </p> <p>このフィールドの日付値のインデックスを作成する際に認識される日付形式を制御します。 </p> <p>各日付フィールドには、日付形式のデフォルトの文字列リストが提供されます。 リストに追加したり、独自のサイトのニーズに合わせてリストを編集したりできます。 </p> <p><a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local">日付の形式</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト日付の形式 </p> </td> 
      <td colname="col2"> <p>データタイプとして「 <span class="uicontrol">日付</span> 」が選択されている場合にのみ使用できます。 </p> <p>指定した日付形式をプレビューして、正しくフォーマットされていることを確認します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムゾーン </p> </td> 
      <td colname="col2"> <p>データタイプとして「 <span class="uicontrol">日付</span> 」が選択されている場合にのみ使用できます。 </p> <p>タイムゾーンを指定していないこのフィールドの日付値のインデックスを作成する際に適用される想定タイムゾーンを制御します。 </p> <p>例えば、アカウントのタイムゾーンを「America/Los Angeles」に設定し、「<span class="uicontrol">アカウントのタイムゾーンを使用</span>」を選択した場合、次のメタ日付値は、指定されたタイムゾーンを持たないが、夏時間を考慮に入れて処理されます。 </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要でないランク値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「 <span class="uicontrol">ランク</span> 」が選択されている場合にのみ使用できます。 </p> <p>ドキュメントの最低ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクが最も低いランクの場合は0から最も高いランクの場合は10に設定します。 </p> <p>ドキュメントのランクが最も高いランクが1から最も低いランクが10の範囲にある場合、この値を10に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのランク値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「 <span class="uicontrol">ランク</span> 」が選択されている場合にのみ使用できます。 </p> <p>ドキュメントにこのランクフィールドに定義されたメタタグが含まれていない場合に使用するランク値を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要なランク値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「 <span class="uicontrol">ランク</span> 」が選択されている場合にのみ使用できます。 </p> <p>ドキュメントの最大ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクが最も低いランクが0から最も高いランクが10の範囲にある場合、この値を10に設定します。 </p> <p>ドキュメントのランクが最も高いランクが1から最も低いランクが10の範囲にある場合、この値を1に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>既定の単位 </p> </td> 
      <td colname="col2"> <p>データタイプ<span class="uicontrol">ロケーション</span>がデータタイプとして選択されている場合にのみ使用できます。 </p> <p>近接検索の距離値の処理を制御します。 </p> <p>既定の単位を<span class="uicontrol">マイル</span>に設定した場合、このフィールドに適用される近接検索の最小距離/最大距離の基準( 
      <code>
        sp_q_min[_#] 
      </code>または 
      <code>
        sp_q_max[_#] 
      </code>検索CGIのパラメータ)は、マイル単位で扱われ、それ以外はキロメートル単位で扱われます。 </p> <p>このオプションは、 
      <code>
        &lt;Search-Display-Field&gt; 
      </code>近接検索出力フィールドに適用した場合の検索結果テンプレートタグ </p> <p><a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local">近接検索</a>についてを参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲の説明を作成しますか？ </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「<span class="uicontrol">数値</span>」が選択されている場合にのみ使用できます。 </p> <p><span class="uicontrol">デザイン</span> / <span class="uicontrol">ナビゲーション</span> / <span class="uicontrol">ファセット</span>で使用する、フィールド範囲の説明の自動作成を制御します。 </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local">ファセット</a>についてを参照してください。 </p> <p> <p>注意： このフィールドで<span class="uicontrol">垂直更新フィールド</span>がオンになっている場合、生成されたフィールド範囲の説明フィールドは、垂直更新時に更新されます。 ただし、「<span class="uicontrol">範囲フィールド</span>」で識別されるフィールドには、「<span class="uicontrol">垂直更新フィールド</span>」もオンにすることをお勧めします。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲フィールド </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> Create Range Description </span>がオンの場合にのみ使用できます。 </p> <p><span class="uicontrol">テキスト</span>フィールドを更新し、現在のフィールドの範囲の説明を表示します。 このリストには、フィールド範囲の生成用に、他のフィールドでまだ使用されていない<span class="uicontrol">テキスト</span>フィールドがすべて含まれています。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲値 </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>フィールド範囲の説明を作成する際に使用するデータポイントの空白区切りリストです。 次に例を示します。 </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>これらの値は任意の順序で入力できます。 値は保存前に並べ替えられ、重複は削除されます。 また、負の値と非整数値を指定することもできます。 </p> <p>このフィールドの各値に対して、次の操作を実行します。 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">値が<span class="uicontrol">範囲の値</span>の最小値より小さい(&lt;)場合は、<span class="uicontrol">「次よりも小さい」形式</span>が使用されます </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">値が<span class="uicontrol">範囲の値</span>の最大値(&gt;=)以上の場合は、<span class="uicontrol"> 「次より大きい」形式</span>が使用されます。 </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">それ以外の場合は、フィールド値が連続する2つの<span class="uicontrol">範囲値</span>(より大きい(&gt;)より小さい(&lt;=)より大きい(&lt;=))値の間にある「範囲」が検出され、<span class="uicontrol">中間形式</span>が使用されます。 </li> 
    </ul> </p> <p>例えば、上記の値のセットの例では、値の説明のセットが定義されます。 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">10未満 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">10以上20未満 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">20以上50未満 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">50以上100未満 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100以上10000未満 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">10000以上 </li> 
      </ul> </p> <p><span class="uicontrol">「次よりも大きい？」を使用したテストを参照してください。 </span> を使用して、これらのテストの実行方法を変更できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>「未満」形式 </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>で見つかった最小値より小さい値の範囲の説明を指定するために使用されるテンプレートです。 最小の値は、数値プレースホルダートークン<span class="uicontrol"> ～N～ </span>を使用して表されます。 次に例を示します。 </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、「5 10 20」の<span class="uicontrol">範囲値</span>定義と1の指定値の場合、生成される範囲の説明は「5未満」のようになります。 代わりに「4.99以下」にする場合は、「<span class="uicontrol">精度</span> 」を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p><span class="uicontrol"> "Less Than"形式</span>では、小文字の<span class="uicontrol"> ～n～ </span>で、値は<span class="uicontrol">精度</span>設定に従って<i>下</i>に丸められます。 </p> <p>注意：範囲の説明に数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けます。例：<span class="uicontrol"> \～N～ </span>または<span class="uicontrol"> \～n～ </span>。 バックスラッシュを含めるには、別のバックスラッシュを使用します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>中間形式 </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>にある最小値と最大値の間にある値の範囲の説明を指定するために使用するテンプレートです。 指定した範囲では、小さい方の値が数値プレースホルダートークン<span class="uicontrol"> ～L～ </span>で表され、大きい方の値はトークン<span class="uicontrol"> ～H～ </span>で表されます。 次に例を示します。 </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>または </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>または </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、「5 10 20」の<span class="uicontrol">範囲値</span>定義と8の指定値の場合、生成される範囲の説明は「5 ～ 10」のようになります。 代わりに、「5 ～ 9.99」の値を大きく設定し、<i>下</i>に<span class="uicontrol">精度</span>を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>同様に、<span class="uicontrol"> ～L～ </span>を<span class="uicontrol"> ～l～ </span>に置き換えて、<span class="uicontrol">精度</span>設定に従って、低い値が<i>上</i>に調整されるようにします。 つまり、次のような定義です。 </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p><span class="uicontrol">精度</span>の値が<span class="uicontrol"> 2 </span>の場合、「5.01 ～ 10」が作成されます。 </p> <p>小文字の<span class="uicontrol"> ～l～ </span>では、<span class="uicontrol">精度</span>設定に従って小文字の値が<i>上</i>に丸められ、小文字の<span class="uicontrol"> ～h～ </span>では、大文字の値が<i>下</i>に丸められます。 </p> <p>注意：範囲の説明に数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けます。例：<span class="uicontrol"> \～L～ </span>または<span class="uicontrol"> \～h～ </span>。 バックスラッシュを含めるには、別のバックスラッシュを使用します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>「次よりも大きい」形式 </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>で見つかった最大値より大きい値の範囲の説明を指定するために使用するテンプレートです。 最大の値は、数値プレースホルダートークン<span class="uicontrol"> ～N～ </span>を使用して表されます。 次に例を示します。 </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、<span class="uicontrol">範囲値</span>の定義が「5 10 20」で、指定された値が30の場合、生成される範囲の説明は単に「20より大きい」のようになります。 代わりに「20.01以降」にする場合は、「<span class="uicontrol">精度</span> 」を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p><span class="uicontrol"> "Greater Than"形式</span>では、小文字の<span class="uicontrol"> ～n～ </span>で、値は<span class="uicontrol">精度</span>設定に従って<i>上</i>に丸められます。 </p> <p>注意：範囲の説明に数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けます。例：<span class="uicontrol"> \～N～ </span>または<span class="uicontrol"> \～n～ </span>。 バックスラッシュを含めるには、別のバックスラッシュを使用します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>精度 </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>小数点の右側の桁数を指定する整数値。 これは丸め操作も制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p>「<span class="uicontrol">範囲の説明を作成</span>」をオンにし、「<span class="uicontrol">範囲フィールド</span>」項目が選択され、ゼロ以外の<span class="uicontrol">精度</span>値が設定されている場合にのみ使用できます。 </p> <p>「0.50」を「。50」として表示する必要がありますか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>末尾のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p>「<span class="uicontrol">範囲の説明を作成</span>」をオンにし、「<span class="uicontrol">範囲フィールド</span>」項目が選択され、ゼロ以外の<span class="uicontrol">精度</span>値が設定されている場合にのみ使用できます。 </p> <p>「10.00」を「10」と表示する必要がありますか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>千単位の区切りを表示しますか？ </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>「10000」を「10,000」と表示する必要がありますか。 ロケール固有の値が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ゼロの値を調整しますか？ </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>ゼロの値を丸めた場合、<span class="uicontrol">精度</span>の設定に従って切り上げまたは切り下げを行う必要がありますか？ 例えば、「0.01」を表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>「次より大きい？」を使用してテストする </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>各値が<span class="uicontrol">範囲値</span>の値と比較され、<i><b>降順</b></i>で処理されるので、デフォルトでは、Greater Than or Equal(&gt;=)演算子を使用して比較され、このテストが成功すると停止します。 つまり、「10 20 50 100 1000」のような<span class="uicontrol">範囲値</span>のセットでは、100は100以上1000以下の範囲に入ります。つまり、100は100以上1000以下になります。 50 ～ 100の範囲に含めたい場合は、このオプションをオンにします。これにより、比較では、代わりに「次より大きい(&gt;)」演算子が使用されます。 </p> <p>例えば、このオプションがオンの場合、このフィールドの各値は次のようになります。 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">値が<span class="uicontrol">範囲の値</span>の最小値(&lt;=)以下の場合は、<span class="uicontrol"> 「次よりも小さい」形式</span>が使用されます </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">値が<span class="uicontrol">範囲の値</span>の最大値より大きい(&gt;)場合は、<span class="uicontrol"> "次より大きい"形式</span>が使用されます </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">それ以外の場合は、フィールド値が連続する2つの<span class="uicontrol">範囲値</span>(小さい値が(&gt;=)以上、大きい値が(&lt;)未満)の範囲に含まれ、 <span class="uicontrol">中間形式</span>が使用されます </li> 
    </ul> </p> <p>およびオフの場合： 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">値が<span class="uicontrol">範囲の値</span>の最小値より小さい(&lt;)場合は、<span class="uicontrol"> "次の値より小さい"形式</span>が使用されます </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">値が<span class="uicontrol">範囲の値</span>の最大値(&gt;=)以上の場合は、<span class="uicontrol"> 「次よりも大きい」形式</span>が使用されます </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">それ以外の場合は、フィールド値が連続する2つの<span class="uicontrol">範囲値</span> (より大きい(&gt;)より小さい(&lt;=)より大きい(&lt;=))値の間にある範囲が見つかり、 <span class="uicontrol">中間形式</span>が使用されます </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p>「 <span class="uicontrol">範囲の説明を作成</span> 」がオンで、「 <span class="uicontrol">範囲フィールド</span> 」項目が選択されている場合にのみ使用できます。 </p> <p>サンプルの数値を指定し、 <span class="uicontrol"> Test </span>ボタンを押して、範囲フィールドの作成方法を確認します。 生成された範囲の説明がウィンドウに表示されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [新しいメタタグフィールド](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)の追加も参照してください。
1. クリック **[!UICONTROL Add]**.
1. （オプション）結果をプレビューする場合は、ステージング済みサイトのインデックスを再構築します。

   [ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 定義済みまたはユーザー定義のメタタグフィールドの編集 {#task_0A7657B63596421BB6DB3ED44F827AB3}

事前定義メタタグ内の特定のフィールドのみを編集したり、ユーザー定義のメタタグ内のすべてのフィールドを編集したりできます。

メタタグの変更の効果をユーザーに表示する前に、サイトのインデックスを再構築する必要があります。

**定義済みまたはユーザー定義のメタタグフィールドを編集するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページのテーブルの[!DNL Actions]列で、変更するメタタグフィールド名の行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Pinned Keyword Results Manager]ページのテーブルで、変更するキーワードの行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Field]ページで、必要なオプションを設定します。

   事前定義済みのメタタグフィールドに変更を加える場合は、すべてのフィールドが編集可能とは限らないことに注意してください。

   [新しいメタタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージング済みサイトのインデックスを再構築します。

   [ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ユーザー定義メタタグフィールドの削除 {#task_9361EF38B5E743038B6672FA6CF70FD3}

不要になった、または使用しなくなったユーザー定義のメタタグフィールドを削除できます。

事前定義済みのメタタグフィールドは削除できません。 ただし、特定のフィールドを編集することはできます。

[定義済みまたはユーザー定義のメタタグフィールドの編集](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)を参照してください。

削除メタタグの効果をユーザーに表示する前に、サイトインデックスを再構築する必要があります。

**ユーザー定義のメタタグフィールドを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページのテーブルの[!DNL User-defined fields]セクションで、削除するメタタグフィールド名の行の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. 確認ダイアログボックスで、「**[!UICONTROL OK]**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージング済みサイトのインデックスを再構築します。

   [ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インジェクションについて {#concept_DA091920671948A0A893A26B3A2FAAE5}

[!DNL Injections]を使用すると、ページ自体を編集する必要なく、Webページにコンテンツを挿入できます。

「target」や「body」などの特定のインデックス付きフィールドにコンテンツを追加したり、インデックス付きのコンテンツを新しい値で置き換えたりできます。 例えば、「ターゲット」メタタグフィールドに新しいコンテンツを挿入した場合、この情報は、ハードコードされたページコンテンツと同じように扱われます。 サイトページに対応するコンテンツが含まれているかどうかに関係なく、事前定義済みのメタタグフィールドのコンテンツを編集できます。 例えば、次の事前定義済みメタタグフィールド名のコンテンツを編集できます。

* ALT
* body
* charset
* date
* desc
* keys
* language
* target
* title
* url

## テストフィールドインジェクションの操作 {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

[!DNL Staged Injections]ページでは、必要に応じて&#x200B;**[!UICONTROL Test]**&#x200B;を使用できます。 テストフィールド名（例：「タイトル」や「本文」）、元のフィールド値（例：「ホームページ」）およびWebサイトのテストURLを入力します。 参照用に、結果の値が表示されます。 現在の値は、テスト中は変更されません。

## フィールドインジェクション定義の操作 {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

インジェクション定義の形式は次のとおりです。

```
append|replace field [regexp] URL value
```

`append|replace`、`field`、`URL`。 と`value`項目は必須です。 ラインごとに1つの射出定義を入力します。 次の例には、6つの異なるインジェクション定義が含まれています。

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>挿入定義 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> append|replace  </span> </p> </td> 
   <td colname="col2"> <p>インジェクション定義の値を追加するには、「append」を選択します(「Adobe:お問い合わせ」または「今すぐ販売中！」 上記の例で)を既存のフィールドの内容に追加する必要があります。 「置換」を選択すると、既存のフィールドの内容が定義済みの値で上書きされます。 フィールドに現在コンテンツが含まれていない場合、どのオプション（追加または置換）が使用されているかに関係なく、定義された値が自動的に追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field  </span> </p> </td> 
   <td colname="col2"> <p>フィールド名は必須です。 次の10個の定義済みフィールド名を使用できます。 </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> keys  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> title </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>各フィールド名は、サイトページの要素に対応します。 例えば、フィールド名<span class="codeph"> desc </span>を指定した場合、サイトページの説明Metaタグに対応するフィールドにインジェクション定義値を追加できます。 </p> <p>説明メタタグがページに存在しない場合は、定義済みのコンテンツによってタグが作成されます。 <span class="codeph"> desc </span>インジェクションで指定されたコンテンツは、ハードコーディングされたメタ説明コンテンツと同じように結果ページに表示されます。 </p> <p>また、同じフィールド名を持つ複数の定義を作成することもできます。 例えば、以下のインジェクションがあるとします。 </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>上記の例のすべてのサイトページに、挿入されたタイトル「Welcome to My Site」が付与されます。 「/company/」フォルダー内のページに、新しいタイトル「My Site:お問い合わせ」を追加しました。 </p> <p>インジェクションは、「<span class="wintitle">フィールドインジェクションの定義</span>」テキストボックスに表示される順序で適用されます。 同じ場所にあるページに対して同じフィールド（この例では「タイトル」）が複数回定義されている場合は、後の定義が優先されます。 </p> <p> <span class="codeph"> [regexp] — オ </span> プション。<span class="codeph">正規表現</span>オプションを使用する場合、定義されたURLは正規表現として扱われます。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規表現</a>を参照してください。 </p> <p>次の定義では、 </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> 正規表現<span class="codeph"> ^と一致するすべてのページの「target」フィールドに、「重要な情報」が挿入されます。*/products/.*\.html$ </span>. </p> <p>そのため、次の操作を実行できます。 </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>次の例では、 </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>このインジェクションは、ファイル名の拡張子が「.pdf」で終わるすべてのページの「タイトル」コンテンツに「Millennium Science」を追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>URLが必要で、挿入するドキュメントを指定します。 </p> <p>URLは、次のいずれかです。 </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> 完全パス( https://www.mydomain.com/products.htmlなど) </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> https://www.mydomain.com/productsのように、部分パス </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> ワイルドカードを使用するURL( https://www.mydomain.com/*.htmlなど) </li> 
     </ul> </p> <p>URL値にはスペース文字を含めないでください。 <span class="codeph">正規表現</span>オプションを使用すると、URLは正規表現のように扱われます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>値は必須で、既存のフィールドコンテンツを置き換えるか、既存のフィールドコンテンツに追加するために使用します。 同じフィールド名に複数の値を指定できます。 次に例を示します。 </p> <p><b>keys</b> https://www.mysite.com/travel/ <b>summer</b>、<b>beach</b>、<b>sand</b>を追加します。 </p> <p><b>keys</b> https://www.mysite.com/travel/fare/*.html <b>格安チケット</b>を追加します。 </p> <p>上記の例では、「/travel/」ディレクトリ内のすべてのページの「keys」フィールドに「summer, beach, sand」という単語が追加されます。 「/travel/fare/」ディレクトリ内のすべてのページの「keys」フィールドにも、「ceaps tickets」という単語が追加されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[クロールするコンテンツタイプとインデックス](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)の選択も参照してください。

## フィールドインジェクション定義の追加 {#task_E86566FA1FF74CF68115C0ADA05172AE}

[!DNL Injections]を使用すると、ページ自体を編集する必要なく、Webページにコンテンツを挿入できます。

[!DNL Injections]ページでは、必要に応じて&#x200B;**[!UICONTROL Test]**&#x200B;を使用できます。 テストフィールド名（例：「タイトル」や「本文」）、元のフィールド値（例：「ホームページ」）およびWebサイトのテストURLを入力します。 参照用に、結果の値が表示されます。 現在の値は、テスト中は変更されません。

**フィールドインジェクション定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;をクリックします。
1. （オプション） [!DNL Injections]ページの[!DNL Test Field Injections]領域で、テストフィールド、テスト元の値およびテストURLを入力し、「**[!UICONTROL Test]**」をクリックします。
1. [!DNL Field Injection Definitions]フィールドに、ラインごとに1つのインジェクション定義を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダーについて {#concept_9EF38E98811B42CDA41996432B9AD209}

[!DNL Attribute Loader]を使用して、Webサイトからクロールされたデータを補強する追加の入力ソースを定義します。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

データフィード入力ソースを使用すると、Webサイトで通常検出される内容とは異なるフォームに保存されたコンテンツにアクセスできます。 これは、使用可能なクロールメソッドの1つを使用して行います。 これらのソースのデータは、クロールされたコンテンツからデータに挿入できます。

[!DNL Staged Attribute Loader Definitions]ページに属性ローダ定義を追加した後、[名前]値と[タイプ]値を除く設定を変更できます

[!DNL Attribute Loader]ページには、次の情報が表示されます。

* 設定して追加した定義済みのAttribute Loader設定の名前。
* 追加した各コネクタに対して、次のいずれかのデータソースタイプを指定します。

   * **テキスト**  — 単純な「フラット」ファイル、コンマ区切り形式、タブ区切り形式、またはその他の一貫した区切り形式。
   * **フィード**  - XMLフィード。

* 次のクロールとインデックスに対して構成が有効かどうか。
* データソースのアドレス。

[テキストとフィードに対する属性の挿入処理の仕組みも参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

[複数のアトリビュートローダの設定について](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)も参照してください。

[属性を追加する際のプレビューの使用について…も参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## 属性ローダーのテキスト設定およびフィード設定に対する属性挿入プロセスの仕組み {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手順 </p> </th> 
   <th colname="col2" class="entry"> <p>手順 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードします。 </p> </td> 
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、単純なファイルダウンロードです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p><span class="uicontrol">テキスト</span>の場合、改行で区切られた各テキスト行は、個々のドキュメントに対応し、コンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p><span class="uicontrol">フィード</span>の場合、各ドキュメントのデータは次の形式の正規表現パターンを使用して抽出されます。 </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle">属性ローダの<span class="uicontrol">マップ</span>を使用して</span>を追加し、キャッシュされたデータのコピーを作成して、クローラのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが設定されます。 </p> <p>解析されたデータはローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラーで必要な単純なHTMLドキュメントを作成します。 例： </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span>要素は、「タイトル」メタデータフィールドへのマッピングが存在する場合にのみ生成されます。 同様に、 <span class="codeph"> &lt;body&gt; </span>要素は、Bodyメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義済みURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについては、元のドキュメント内のデータを持つ各フィールドに対して<span class="codeph"> &lt;meta&gt; </span>タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれるドキュメントごとに、次の例のようにリンクも生成されます。 </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングでは、プライマリキーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取得される際に使用されるキーを形成します。 </p> <p>クローラーは、URL <span class="codeph">インデックスを認識します。</span>スキームプレフィックス。ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p><span class="codeph">インデックス：</span>リンクは、クローラーの保留中リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、そのドキュメントのデータがキャッシュから取得されます。 次に、HTML画像を「アセンブル」し、処理してインデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 複数の属性ローダの設定について {#section_4CC49C74EF294608A184E233F215ADFF}

任意のアカウントに対して複数の属性ローダー設定を定義できます。

属性ローダを追加する場合、オプションで機能&#x200B;**[!UICONTROL Setup Maps]**&#x200B;を使用して、データソースのサンプルをダウンロードできます。 そのデータは適否を調べる。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> 属性ローダーのタイプ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>テキスト </p> </td> 
   <td colname="col2"> <p>最初にタブを試し、次に縦棒( <span class="codeph"> )を試して区切り文字の値を決定します。 | </span>)を挿入し、最後にコンマ( <span class="codeph"> 、 </span>)を挿入します。 「<span class="uicontrol">マップを設定</span>」をクリックする前に区切り文字値を既に指定している場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なTag値とField値の推測値が入力されます。 さらに、解析済みデータのサンプリングが表示されます。 ファイルにヘッダー行が含まれていることがわかっている場合は、「最初の行の<span class="uicontrol">ヘッダー</span>」を必ず選択してください。 設定関数は、この情報を使用して、結果のマップエントリをより適切に識別します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子は、Mapテーブルのタグ行に表示され、同様の値がFieldsに表示されます。 これらの行は、使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータとItemtagを識別するので、これでも役に立ちます。 </p> <p> <p>注意： 「マップを設定」機能は、分析を実行するXMLソース全体をダウンロードします。 ファイルのサイズが大きい場合、この操作はタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は可能なすべてのXPath項目を識別します。この項目の多くは、使用するのが望ましくありません。 必ず、結果のマップ定義を確認し、不要なマップ定義や不要なマップ定義を削除してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サイズの大きいXMLデータセットに対しては、ファイルパーサがファイル全体をメモリに読み込もうとするので、マップ設定機能が動作しない場合があります。 その結果、メモリ不足が発生する場合があります。 ただし、インデックス作成時に同じドキュメントを処理する場合、メモリに読み込まれません。 その代わりに、大きなドキュメントは「外出先で」処理され、最初にメモリに完全に読み込まれるわけではありません。

## アトリビュートローダを追加する際のプレビューの使用について {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

Attribute Loaderデータは、インデックス操作の前に読み込まれます。

アトリビュートローダを追加する際に、オプションで&#x200B;**[!UICONTROL Preview]**&#x200B;機能を使用して、データを保存する場合と同じようにデータを検証できます。 設定に対してテストを実行しますが、設定をアカウントに保存する必要はありません。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラーが使用するメインキャッシュフォルダーとは競合しません。

**Acct:IndexConnector-Preview-Max-Documents**&#x200B;で制御されるデフォルトの5つのドキュメントのみをプレビューで処理します。 プレビューされたドキュメントは、インデックス作成クローラーに表示されるとおりに、ソース形式で表示されます。 この表示は、Webブラウザの「ソースを表示」機能に似ています。 標準のナビゲーションリンクを使用して、プレビューセット内のドキュメントを移動できます。

プレビューでは、XML設定はサポートされていません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## 属性ローダ定義の追加 {#task_A735E5EF763343A9B675E1A3B09AFDBC}

各属性ローダー設定は、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

新しい定義と有効な定義の効果がユーザーに表示される前に、サイトインデックスを再構築します。

**属性ローダー定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Stage Attribute Loader Definitions]ページで、「**[!UICONTROL Add New Attribute Loader]**」をクリックします。
1. [!DNL Attribute Loader Add]ページで、必要な設定オプションを設定します。 使用できるオプションは、選択した&#x200B;**[!UICONTROL Type]**&#x200B;によって異なります。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>名前 </p> </td> 
      <td colname="col2"> <p>属性ローダー設定の一意の名前。 英数字を使用できます。 「_」と「 — 」の文字も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択したデータソースタイプは、「<span class="wintitle">属性ローダー</span>の追加」ページで使用できる結果のオプションに影響します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、コンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行区切りの各テキスト行は、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）は、列番号で参照されるメタデータフィールドに1からマッピングできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むプライマリXMLドキュメントをダウンロードします。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>使用する設定を「オン」にします。 または、設定を「オフ」にして、が使用されないようにすることもできます。 </p> <p> <b>注意</b>:無効な属性ローダーの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドに適したエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、コンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、適切な認証資格情報を入力してHTTPSサーバーにアクセスできます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTPまたはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で指定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、HTTPSの接続の再試行の最大回数を指定します。 この値は、0 ～ 10の範囲で指定する必要があります。 </p> <p>値が0の場合、再試行は行われません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの各フィールドの区切りに使用する文字を指定します。 </p> <p>コンマ文字( <span class="codeph"> 、 </span> )は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るのに役立つフィールド区切り文字として機能します。 </p> <p><span class="uicontrol"> Tab? </span> を使用して、水平タブ文字を区切り文字として使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1行目のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日 </p> </td> 
      <td colname="col2"> <p>Attribute Loaderデータのダウンロード間隔の最小値を設定します。 ダウンロード更新頻度の間隔内で発生するインデックスでトリガーされるダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内にAttribute Loaderデータが2回以上ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1にして列番号を指定します。 各列に新しいマップ行を追加するには、「<span class="wintitle">アクション</span>」で、「<span class="uicontrol"> + </span>」をクリックします。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップするように選択できます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>をドロップダウンリストにし、現在のアカウントに対して定義済みのメタデータフィールドを選択できるようにします。 </p> <p><span class="uicontrol">フィールド</span>の値は、必要に応じて、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、 <span class="wintitle">フィルタリングスクリプト</span>で使用するコンテンツの作成に役立つ場合があります。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプト</a>についてを参照してください。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるフィールドは1つだけです。 このフィールドは、属性ローダーのデータとインデックス内の対応するドキュメントを照合する「外部キー」として使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>マップに行を追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>使用する設定を「オン」にします。 または、設定を「オフ」にして、が使用されないようにすることもできます。 </p> <p> <b>注意</b>:無効な属性ローダーの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、およびオプションで「Username」、「Password」フィールドの適切なエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含むプライマリXMLドキュメントへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、適切な認証資格情報を入力してHTTPSサーバーにアクセスできます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> ファイル </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、次のAdobeXMLドキュメントのFeedフラグメントでは、Itemtag値は<span class="codeph">レコード</span>です。 </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>相互参照フィールド名 </p> </td> 
      <td colname="col2"> <p>メタデータフィールドの値を、アトリビュートローダ設定のデータに対するルックアップ「キー」として使用するよう指定します。 値が選択されていない場合(<b>—None—</b>)、この設定のデータは、ランキングの計算(<b>Rules</b> &gt; <b>Ranking Rules</b> &gt; <b>Edit Rules</b>)では使用できません。 値を選択すると、このフィールドの値を使用して、サイト検索/マーチャンダイジングドキュメントとこの設定のデータを相互参照します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日 </p> </td> 
      <td colname="col2"> <p>Attribute Loaderデータのダウンロード間隔の最小値を設定します。 ダウンロード更新頻度の間隔内で発生するインデックスでトリガーされるダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内にAttribute Loaderデータが2回以上ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobeXMLドキュメントを使用すると、オプションItemtagの下で、次の構文を使用してマッピングできます。 </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、を次のように変換します。 </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>要素の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>にマップされます。 </span></p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">コンテンツ</span>属性（<span class="codeph">タイトル</span>という名前属性を持つ<span class="codeph">レコード</span>要素内に含まれる）は、メタデータフィールド<span class="codeph">タイトル&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">レコードの</span>要素（name属性が<span class="codeph">説明</span>）に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性は、メタデータフィールド<span class="codeph"> &lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">レコードの</span>要素内に含まれる<span class="codeph">メタデータ</span>要素の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本文&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
        </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xml/xpath_intro.asp </a>を参照してください。 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各<span class="codeph"> &lt;meta&gt; </span>タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>をドロップダウンリストにし、現在のアカウントに対して定義済みのメタデータフィールドを選択できるようにします。 </p> <p><span class="uicontrol">フィールド</span>の値は、必要に応じて、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、 <span class="wintitle">フィルタースクリプト</span>で使用するコンテンツを作成する場合に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプト</a>についてを参照してください。 </p> <p>属性ローダーが任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が、結果としてキャッシュされたドキュメントで単一の値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>の値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字の値（定義された最初の区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるフィールドは1つだけです。 このフィールドは、属性ローダーのデータとインデックス内の対応するドキュメントを照合する「外部キー」として使用されます。 </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>マップに行を追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）**[!UICONTROL Setup Maps]**&#x200B;をクリックして、データソースのサンプルをダウンロードします。 そのデータは適否を調べる。
1. **[!UICONTROL Add]**&#x200B;をクリックして、[!DNL Attribute Loader Definitions]ページに設定を追加します。
1. [!DNL Attribute Loader Definitions]ページで、「**[!UICONTROL rebuild your staged site index]**」をクリックします。
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義の編集 {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

定義済みの既存のアトリビュートローダを編集できます。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

[!DNL Type]ドロップダウンリストのAttribute Loader NameやTypeなど、一部のAttribute Loaderオプションを変更できるわけではありません。

**属性ローダ定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を変更する属性ローダ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Edit]ページで、必要なオプションを設定します。

   [属性ローダ定義](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)の追加のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、「**[!UICONTROL rebuild your staged site index]**」をクリックします。
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義のコピー {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

既存のアトリビュートローダ定義をコピーして、作成する新しいアトリビュートローダの基礎として使用できます。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

アトリビュートローダ定義をコピーする場合、コピーされた定義はデフォルトで無効になります。 定義を有効または「オン」にするには、[!DNL Attribute Loader Edit]ページから定義を編集し、**[!UICONTROL Enable]**&#x200B;を選択する必要があります。

[属性ローダ定義の編集](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)を参照してください。

**属性ローダ定義をコピーするには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を複製する属性ローダ定義名の&#x200B;**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Copy]ページで、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義の名前変更 {#task_58D5DFD7EBC04111BCB91118E4440DB4}

既存のアトリビュートローダ定義の名前を変更できます。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

**属性ローダ定義の名前を変更するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、変更する属性ローダ定義名の&#x200B;**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Rename]ページで、[!DNL Name]フィールドに定義の新しい名前を入力します。
1. クリック **[!UICONTROL Rename]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダデータの読み込み {#task_2F3C55189B0A4049AB2113F2291CC181}

設定済みの属性ローダーデータをサイト検索/マーチャンダイジングにダウンロードできます。

[!DNL Data Load]ページには、最後のAttribute Loaderデータ読み込み操作のステータスに関する次の情報が表示されます。

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
   <td colname="col2"> <p>最後のデータ読み込み試行の成功または失敗を示します。 または、既に進行中のデータ読み込み操作のステータスを表示します。 </p> </td> 
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

**属性ローダのデータをロードするには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページで、「**[!UICONTROL Load Attribute Loader Data]**」をクリックします。
1. **[!UICONTROL Attribute Loader Data Load]**&#x200B;ページで、次のいずれかの操作を行います。

   * **[!UICONTROL Start Load]**&#x200B;をクリックして、読み込み操作を開始します。

      データの読み込み操作中は、**Progress**&#x200B;行に進行状況に関する情報が表示されます。

   * **[!UICONTROL Stop Load]**&#x200B;をクリックして、読み込み操作を停止します。

1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL Attribute Loader Definitions]ページに戻ります。

## 属性ローダデータのプレビュー {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

プレビュー(Preview)を使用して、最近ロードしたアトリビュートローダのデータを表示できます。

表の「行」列には、データの各行の番号が表示され、属性ローダの値がロードされた元の順序が示されます。

残りの列には、各エントリに関連付けられた値が表示されます。

テーブルが空の場合は、アトリビュートローダのデータがまだ読み込まれていないことを意味します。 [!DNL Attribute Loader Data Preview]ページを閉じて、アトリビュートローダのデータを読み込むことができます。

[Loading Attribute Loader data](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

**アトリビュートローダのデータをプレビューするには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページの[!DNL Actions]列で、ダウンロードしたデータを表示する設定の&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Data Preview]ページで、ページの上部と下部にあるナビゲーションおよび表示オプションを使用して、データを表示します。

   表の列見出しをクリックして、昇順または降順にデータを並べ替えます。
1. 次のいずれかの操作を行います。

   * **[!UICONTROL Download to Desktop]**&#x200B;をクリックして、表を.xltファイルとしてダウンロードし、保存します。
   * アトリビュートローダのデータのプレビューが終了し、前に表示したページに戻ったら、ページを閉じます。

## 属性ローダ定義の設定の表示 {#task_EA99A9694FE948ADA82C1DBA0667851B}

既存のアトリビュートローダ定義のコンフィギュレーション設定を確認できます。

[!DNL Attribute Loader Definitions]ページに属性ローダ定義を追加した後は、[タイプ]設定を変更できません。 代わりに、定義を削除してから、新しい定義を追加する必要があります。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

**アトリビュートローダ定義の設定を表示するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を確認または編集する属性ローダ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

## 最新の属性ローダーデータ読み込みからのログの表示 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

[!DNL View Log]を使用して、最新のダウンロードプロセスのAttribute Loaderデータログファイルを調べることができます。 また、ログ表示を使用して、実行中のダウンロードを監視することもできます。

[Loading Attribute Loader data](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

**最新のAttribute Loaderデータ読み込みのログを表示するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページで、「**[!UICONTROL View Log]**」をクリックします。 ログページ
1. [!DNL Attribute Loader Data Log]ページで、ページの上部と下部にあるナビゲーションおよび表示オプションを使用して、ログ情報を表示します。
1. 完了したら、ページを閉じて[!DNL Attribute Loader Definitions]ページに戻ります。

## 属性ローダ定義の削除 {#task_E8980F66888B476E98C228C1D307EDF8}

不要になった、または使用しなくなった既存のアトリビュートローダ定義を削除できます。

>[!NOTE]
>
>属性ローダーを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。

**属性ローダ定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページの[!DNL Actions]列見出しの下で、削除する属性ローダ定義名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Delete]ページで、「**[!UICONTROL Delete]**」をクリックします。
