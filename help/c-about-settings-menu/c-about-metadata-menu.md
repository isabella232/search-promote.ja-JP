---
description: メタデータメニューを使用して、検索定義とインデックスの挿入をカスタマイズします。
seo-description: メタデータメニューを使用して、検索定義とインデックスの挿入をカスタマイズします。
seo-title: メタデータメニューについて
solution: Target
subtopic: Metadata
title: メタデータメニューについて
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: cf2707d124bd3f3a864610bcf41dda5e5670fc90

---


# メタデータメニューについて{#about-the-metadata-menu}

メタデータメニューを使用して、検索定義とインデックスの挿入をカスタマイズします。

## 定義について {#concept_AE48035C210145169BE067D396975620}

を使用して、顧客 [!DNL Definitions] が検索クエリを送信する際に考慮されるHTMLフィールドとメタデータフィールドの内容と関連性をカスタマイズできます。

既に定義済みのフィールドを編集できます。 また、メタデータタグのコンテンツに基づいて新しいユーザ定義フィールドを作成することもできます。 各定義は、ページ上の1行に表示され [!DNL Staged Definitions] ます。

データビューにつ [いても参照してください](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)。

## 新しいメタタグフィールドの追加 {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

独自のメタデータタグフィールドを定義し、追加できます。

新しいメタタグ定義の効果を顧客に表示する前に、サイトインデックスを再構築する必要があります。

**新しいメタタグフィールドを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Definitions]**。
1. ページ上で、 [!DNL Definitions] をクリックしま **[!UICONTROL Add New Field]**&#x200B;す。
1. ページ [!DNL Add Field] で、必要なオプションを設定します。

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
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> 名前には、英数字のみを使用する必要があります。 </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> 名前にはダッシュを使用できますが、スペースは使用できません。 </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> 20文字までの名前を入力できます。 </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> 名前の大文字と小文字は区別されませんが、入力したとおりに表示および保存されます。 </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> 「ステージングされた定義」ページの表に示すように、事前定義済みのフィールドに存在する名前は使用 <span class="wintitle"> でき </span> ません。 </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> 「any」という語をユーザ定義フィールド名の値として使用することはできません。 </li> 
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
      <td colname="col2"> <p>定義済みのフィールドに関連付けられているコンテンツを決定します。 </p> <p>名前のリストは255文字まで入力できます。 また、nameには、HTMLメタタグのname属性で許可されている任意の文字を含めることができます。 </p> <p>単一のフィールド定義で複数のmetaタグを指定できます。 </p> <p>複数の値はコンマで区切る必要があり、任意のWebページで見つかった左端のメタタグ名が優先されます。 </p> <p>例えば、「auth」という名前のフィールドを定義したとします。 フィールド名には、関連するmetaタグ「author, dc.author」が含まれます。 この場合、両方のメタタグがWebページに表示される場合、「author」メタタグのコンテンツのインデックスが作成され、「dc.author」のコンテンツが検索されます。 </p> <p>ユーザ定義フィールドの定義には、メタタグ名が少なくとも1つ必要です。 事前定義済みのフィールドには、メタタグを関連付ける必要はありません。 ただし、1つ以上のmetaタグが指定されている場合は、metaタグの内容が各タグの現在のデータソースより優先されます。 </p> <p>例えば、メタタグ「dc.title」が事前定義の「title」フィールドに関連付けられている場合、「dc.title」メタタグのコンテンツは、 
      <userinput>
        &lt;title&gt; 
      </userinput> タグを使用します。 </p> <p>次に例を示します。 </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> 固有タグ </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>データタイプ </p> </td> 
      <td colname="col2"> <p>各フィールドには、テキスト、数値、日付、バージョン、ランク、場所などのデータタイプが関連付けられています。 このデータ型は、フィールドのコンテンツのインデックス化、検索、およびオプションでの並べ替えの方法を決定します。 </p> <p>フィールド定義の作成後は、データ型を変更できません。 </p> <p>次の情報を使用して、フィールドに含まれる情報に関連するデータ型を選択します。 </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> テキスト </span> データ型フィールドは、文字列として扱われます。 </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> 数値デ </span> ータ型のフィールドは、整数または浮動小数点の数値として扱われます。 </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> 日付デ </span> ータ型フィールドは、日付/時間指定子として扱われます。 新しいフィールドを追加または編集する際に、許可される日付/時間形式をカスタマイズできます。 </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> バージョン </span> データ型フィールドは、自由形式の数値データとして扱われます。 例えば、1.2.3は1.2.2より前に並べ替えられます。 </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> ランク </span> データ型フィールドは、検索結果のランクや関連性の計算に追加的に影響する点を除き、「Number」タイプフィールドと同じように扱われます。 <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">ランキングルールについて</a>を参照してください。 </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> 場所のデ </span> ータ型のフィールドは、世界のどこでも物理的な場所として扱われます。 使用できる場所の形式は次のとおりです。 <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> 5桁または9桁の郵便番号。DDDDDDまたはDDDDDD-DDDDDの形式で表します。各「D」は0 ～ 9桁です。 </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> DDD形式の3桁の市外局番。 </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> 緯度/経度の組み合わせは、±DD.DDDD±DDD.DDDDDの形式です。最初の数値は緯度を、2番目の数値は経度を表します。 </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>リストを許可 </p> </td> 
      <td colname="col2"> <p>データタイプが「テキスト」または「 <span class="uicontrol"> 数値」 </span>の場合にの <span class="uicontrol"> み使用 </span> できます。 </p> <p>このフィールドのメタデータコンテンツ内の区切られた値を別々にインデックス化します。 </p> <p>例えば、「Allow Lists」が選択されている場合、コンテンツ「Red, Yellow, Green, Blue」は4つの個別の値として扱われ、1つではなく処理されます。 この処理は、範囲検索( 
      <userinput>
        sp_q_min 
      </userinput>、 
      <userinput>
        sp_q_max 
      </userinput> または  
      <userinput>
        sp_q_exact 
      </userinput>)と 
      <userinput>
        &lt;search-field-value-list&gt; 
      </userinput>、 
      <userinput>
        &lt;search-field-values&gt; 
      </userinput>, および 
      <userinput>
        &lt;search-display-field-values&gt; 
      </userinput>。 </p> <p>「Version」データタイプが選択されている場合は使用できません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 動的ファセット </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>注意：この機能は、デフォルトでは有効になっていません。お使いの製品のライセンス認証を行うには、テクニカルサポートにお問い合わせください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたファセットを動的に設定します。 </p> <p>ファセットは、メタタグフィールドの上に構築されます。 メタタグフィールドは、Adobe Search&amp;Promoteの低レベルのコア検索レイヤーです。 一方、ファセットはGS（ガイド付き検索）の一部で、Adobe Search&amp;Promoteの高度なプレゼンテーションレイヤーです。 ファセットには独自のメタタグフィールドがありますが、メタタグフィールドはファセットに関する情報を何も知りません。 </p> <p>動的ファセ <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> ットについてを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複排除を許可 </p> </td> 
      <td colname="col2"> <p>このフィールドの重複除外を有効にするには、このオプションを選択します。 つまり、検索時にこのフィールドを 
        <userinput>
          sp_dedupe_field 
        </userinput> CGIパラメータを検索します。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テーブル名 </p> </td> 
      <td colname="col2"> <p>指定したフィールドを指定したテーブル名に永続的に関連付けます。 </p> <p>このようなフィールドがコア検索CGIパラメータやテンプレートタグ内で言及されると、常にテーブル名が自動的に提供されます。 この機能を使用すると、テーブルの一致による動的ファセットの選択が可能になりますが、必要に応じて、非動的ファセットフィールドにも使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り文字のリストを表示 </p> </td> 
      <td colname="col2"> <p>「リストを許可」が選択さ <span class="uicontrol"> れている場合に </span> のみ使用できます。 </p> <p>個々のリスト値を区切る文字を指定します。 複数の文字を指定できます。各文字は値の区切り文字として扱われます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトで検索 </p> </td> 
      <td colname="col2"> <p>このオプションを選択すると、特定の検索クエリでフィールドが明示的に指定されていない場合でも、フィールドのコンテンツが検索されます。 このオプションの選択を解除すると、フィールドは要求時にのみ検索されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直方向の更新フィールド </p> </td> 
      <td colname="col2"> <p> <p>注意：この機能は、デフォルトでは有効になっていません。お使いの製品のライセンス認証を行うには、テクニカルサポートにお問い合わせください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたフィールドを垂直方向の更新フィールドに設定します。 </p> <p>垂直更新フィールドは、垂直更新プロセス(索引/垂直 <span class="uicontrol"> 更 </span> 新)を介し <span class="uicontrol"> て更新され </span>ます。縦置き版の更新方法により、これらのフィールドのコンテンツはフリーテキスト検索では検索できません。 このオプションを選択すると、どのようなインデックス操作でも、このフィールドのコンテンツが「word」インデックスに追加されません。 また、垂直更新操作中にこのフィールドを更新できるようにします。 </p> <p>垂直方向の更新について詳しくは、「垂直方向の更新につ <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> いて」を参照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>関連度 </p> </td> 
      <td colname="col2"> <p>事前定義フィールドとユーザ定義フィールドの関連性を編集できます。 </p> <p>関連性は1 ～ 10の尺度で指定されます。 設定値が1の場合、最も関連性が低く、10が最も関連性が高いことを意味します。 これらの値は、各フィールドでクエリが一致すると考えられる場合に考慮されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>並べ替え </p> </td> 
      <td colname="col2"> <p>検索結果を名前の付いたフィールドで並べ替えるタイミングを、 
        <userinput>
          sp_s 
        </userinput> CGIパラメータを検索します。 </p> <p>CGIパラメータ <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> ーの検索を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>言語 </p> </td> 
      <td colname="col2"> <p>データタイプ「ランク」、「番号」また <span class="uicontrol"> は「日付」が選 </span>択され <span class="uicontrol"> ている場 </span>合にの <span class="uicontrol"> み使用 </span> できます。 </p> <p>このフィールドの日付、数値およびランク値のインデックス作成時に適用される言語とロケールの規則を制御します。 </p> <p>アカウントの言語を適用することを選択できます（言語/単語と言語）。 また、各数値や日付値を含むドキュメントに関連付けられた言語、または特定の言語を適用することもできます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>日付の形式 </p> </td> 
      <td colname="col2"> <p>「日付」(Date)データタイプが選択されてい <span class="uicontrol"> る場合にの </span> み使用できます。 </p> <p>このフィールドの日付値のインデックスを作成する際に認識される日付形式を制御します。 </p> <p>各日付フィールドには、日付形式文字列のデフォルトのリストが提供されます。 リストに追加したり、サイトのニーズに合わせてリストを編集したりできます。 </p> <p>日付形式を <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> 参照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト日付形式 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「日付」(Date)デ <span class="uicontrol"> ータタ </span> イプが選択されている場合にのみ使用できます。 </p> <p>指定した日付形式をプレビューして、正しく形式設定されていることを確認できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムゾーン </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「日付」(Date)デ <span class="uicontrol"> ータタ </span> イプが選択されている場合にのみ使用できます。 </p> <p>タイムゾーンを指定しないこのフィールドの日付値のインデックス作成時に適用される想定タイムゾーンを制御します。 </p> <p>例えば、アカウントのタイムゾーンが「America/Los Angeles」に設定されていて、「アカウントのタイムゾーンを使用」を選択した場合、次のメタ日付値は、指定されたタイムゾーンを持たない太平洋時間として扱われ、夏時間を考慮します。 <span class="uicontrol"></span> </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要でないランクの値 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「ランク」が選 <span class="uicontrol"> 択さ </span> れている場合にのみ使用できます。 </p> <p>任意のドキュメントの最低ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクの範囲が0（最低）から10（最高）の場合、この値を0に設定します。 </p> <p>ドキュメントのランクの範囲が1（最上位）から10（最下位）の場合、この値を10に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのランク値 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「ランク」が選 <span class="uicontrol"> 択さ </span> れている場合にのみ使用できます。 </p> <p>ドキュメントにこのランクフィールドに定義されたメタタグが含まれていない場合に使用するランク値を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要なランク値 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「ランク」が選 <span class="uicontrol"> 択さ </span> れている場合にのみ使用できます。 </p> <p>ドキュメントの最大ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクの範囲が0（最低）から10（最高）の場合、この値を10に設定します。 </p> <p>ドキュメントのランクの範囲が1（最上位）から10（最下位）の場合、この値を1に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>既定の単位 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「場所」が選択さ <span class="uicontrol"> れて </span> いる場合にのみ使用できます。 </p> <p>近接検索の距離値の処理を制御します。 </p> <p>デフォルトの単位をマイル( <span class="uicontrol"> Miles) </span>に設定した場合、このフィールドに適用される近接検索の最小/最大距離基準( 
      <userinput>
        sp_q_min[_#] 
      </userinput>  または  
      <userinput>
        sp_q_max[_#] 
      </userinput> 検索CGIパラメーター)は、マイルとして扱われます。それ以外の場合は、キロメートルとして扱われます。 </p> <p>このオプションは、 
      <userinput>
        &lt;Search-Display-Field&gt; 
      </userinput> 近接検索出力フィールドに適用された場合の検索結果テンプレートタグ。 </p> <p>近接検索につ <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲の説明を作成しますか？ </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「 <span class="uicontrol"> Number」が選 </span> 択されている場合にのみ使用できます。 </p> <p>デザイン/ナビゲーション/ファセットで使用する、フィールド範囲の説明の <span class="uicontrol"> 自動作 </span> 成を <span class="uicontrol"> 制 </span> 御し <span class="uicontrol"> ます </span>。 </p> <p>ファセットにつ <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> <p> <p>注意： このフィールドで「垂直方向の更新 <span class="uicontrol"> フィールド」がオ </span> ンになっている場合、生成されたフィールド範囲の説明フィールドは、垂直方向の更新時に更新されます。 ただし、「範囲フィールド」で指定したフィールドで「垂直方向の更新フ <span class="uicontrol"> ィールド」もチ </span> ェックされている <span class="uicontrol"> ことをお勧め </span> します。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲フィールド </p> </td> 
      <td colname="col2"> <p>[範囲の説明を作成]がオ <span class="uicontrol"> ンになっている場合に </span> のみ使用できます。 </p> <p>更新する <span class="uicontrol"> テキ </span> ストフィールドで、現在のフィールドの範囲の説明が表示されます。 このリストには、フィールド範 <span class="uicontrol"> 囲の生 </span> 成用に他のフィールドと共に使用されていないすべてのテキストフィールドが含まれます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲の値 </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>フィールド範囲の説明を作成する際に使用するデータポイントの空白区切りのリストです。 次に例を示します。 </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>これらの値は任意の順序で入力できます。 値は、保存前に並べ替えられ、重複が削除されます。 また、負の値や整数以外の値を指定することもできます。 </p> <p>このフィールドの各値に対して、次の操作を行います。 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">値が範囲値の最小値(&lt;)より小さい場合、「小さい」 <span class="uicontrol"> 形 </span>式が <span class="uicontrol"> 使用され </span> ます </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">値が範囲値の最大値(&gt;=)以上の場合、「次の値より大きい」 <span class="uicontrol"> の形 </span>式 <span class="uicontrol"> が使用さ </span> れます。 </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">それ以外の場合は、フィールド値が2つの連続する範囲値 <span class="uicontrol"> (より大きい(&gt;)から小さい値(&lt;=)までの範囲内にある「範囲」が見つかり、「中間形式」が使用され </span><span class="uicontrol"></span> ます。 </li> 
    </ul> </p> <p>例えば、上の値のセットの例では、値の説明のセットが定義されます。 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">10未満 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">10以上20未満 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">20以上50未満 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">50以上100未満 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100以上10000未満 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">10000以上 </li> 
      </ul> </p> <p>「次よりも大き <span class="uicontrol"> い」を使用したテストを参照する </span> を使用して、これらのテストの実行方法を変更します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"より小さい"形式 </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>これは、「範囲の値」で見つかった最小値より小さい値の範囲の説明を指定するために使用するテ <span class="uicontrol"> ンプレートで </span>す。 最小値は、数値プレースホルダトークン～N～を使用し <span class="uicontrol"> て表されま </span>す。 次に例を示します。 </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>通常、値は「そのまま」( <span class="uicontrol"> 5 10 20)の形式で表されます。つまり、範囲値の定義が「5 </span> 10 20」で、指定した値が1の場合、生成される範囲の説明は「5未満」のように単純になります。 「4.99以下」にする場合は、「精度」を2に設定し <span class="uicontrol"> て </span> 次の <span class="uicontrol"> 形 </span> 式を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>「次よ <span class="uicontrol"> り小さい」形式 </span>では、小文字の～n～が、精度の設定に従って値 <span class="uicontrol"> を切り </span><i></i><span class="uicontrol"></span> 捨てます。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーをそのまま含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例： <span class="uicontrol"> \～N～ま </span> たは <span class="uicontrol"> \～n～ </span>。 バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例： <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>中間形式 </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>これは、範囲の値の範囲の説明を指定するために使用するテンプレートで、範囲の値の中で最も小さい値と最も大きい値の間にあ <span class="uicontrol"> る値を指定しま </span>す。 渡された範囲の場合、範囲の値は数値プレースホルダトークン～ <span class="uicontrol"> L～を使用して、範囲の値は </span>トークン～H～を使用して <span class="uicontrol"> 表されます </span>。 次に例を示します。 </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>または </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>または </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>通常、値は「そのまま」( <span class="uicontrol"> 5 10 20)の形式で表されます。つまり、範囲値の定義が「5 10 </span> 20」で、指定された値が8の場合、生成される範囲の説明は「5 ～ 10」のように単純になります。 代わりに「5 ～ 9.99」にし、大きい値を下に調整したい場合は、 <i></i>「精度」を「 <span class="uicontrol"> 2」に設定し </span> 、次の形 <span class="uicontrol"></span> 式を使用します。 </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>同様に、 <span class="uicontrol"> ～L～を </span> ～l <span class="uicontrol"> ～に置き換え </span> て、精度の設定に従って低い値を上に調整 <i>できます</i><span class="uicontrol"></span> 。 これは、次のような定義を意味します。 </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>の精度 <span class="uicontrol"> を2 </span> に設定す <span class="uicontrol"> ると、「5.01 </span> ～ 10」が作成されます。 </p> <p>小文字～l～は精度の設定に従って小文字 <span class="uicontrol"> ～l～を丸め、小文字～h～は小文字 </span> ～ <i>h～を丸めて小文字</i><span class="uicontrol"></span><span class="uicontrol"></span><i></i>～lを丸めます。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーをそのまま含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例： <span class="uicontrol"> \～L～ま </span> たは <span class="uicontrol"> \～h～ </span>。 バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例： <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>「次よりも大きい」形式 </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>これは、範囲の値の最大値より大きい値の範囲の説明を指定するために使用するテンプレ <span class="uicontrol"> ートで </span>す。 最大値は、数値プレースホルダトークン～N～を使 <span class="uicontrol"> 用して表されま </span>す。 次に例を示します。 </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>通常、値は「そのまま」( <span class="uicontrol"> 5 10 20)の範囲値定義と30の範囲値定義の場合、生成される範囲の説明は「 </span> 20より大きい」のような単純な形式になります。 代わりに「20.01以上」にする場合は、「精度」を2に設定 <span class="uicontrol"> し、 </span> 次の <span class="uicontrol"> 形式 </span> を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>「次よ <span class="uicontrol"> り大きい」形式 </span>では、小文字の～n～が、精度の設定に従って値 <span class="uicontrol"> を丸め </span><i></i><span class="uicontrol"></span> るようにします。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーをそのまま含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例： <span class="uicontrol"> \～N～ま </span> たは <span class="uicontrol"> \～n～ </span>。 バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例： <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>精度 </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>小数点以下の桁数を指定する整数値。 丸め処理も制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> る場合にのみ使用できます。「範囲フィールド」( <span class="uicontrol"> Range Field) </span> 項目が選択され、ゼロ以外の精 <span class="uicontrol"></span> 度値が設定されている場合にのみ使用できます。 </p> <p>「0.50」を「。50」と表示しますか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>末尾のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> る場合にのみ使用できます。「範囲フィールド」( <span class="uicontrol"> Range Field) </span> 項目が選択され、ゼロ以外の精 <span class="uicontrol"></span> 度値が設定されている場合にのみ使用できます。 </p> <p>「10.00」を「10」と表示しますか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>千単位区切り文字を表示しますか？ </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>「10,000」を「10,000」と表示しますか。 ロケール固有の値が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ゼロ値を調整する </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>ゼロの丸め値を表示する場合、精度の設定に従って切り上げまたは切り下げを行う必 <span class="uicontrol"> 要があ </span> るか。 例：表示「0.01」? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>次よりも大きい値を使用してテストする </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>各値が <span class="uicontrol"> Range Values </span>の値と比較され、降順で処理されるので <i><b></b></i> 、デフォルトではGreater Than or Equal(&gt;=)演算子を使用して比較され、このテストが成功すると停止します。 つまり、「10 20 50 100 1000」などの範囲値のセットでは、100は実際には100より大きい100から1000までの範囲に含まれます。 <span class="uicontrol"></span> 50 ～ 100の範囲に含める場合は、このオプションを選択します。これにより、比較で代わりに大なり(&gt;)演算子が使用されます。 </p> <p>例えば、このフィールドの各値に対して、このオプションがオンの場合： 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">値が範囲値の最小値(&lt;=)以下の場合、「次より小さい」 <span class="uicontrol"> 形 </span>式 <span class="uicontrol"> が使用さ </span> れます。 </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">値が範囲値の最大値(&gt;)より大きい場合、「次の値よ <span class="uicontrol"> り大きい」 </span>の形 <span class="uicontrol"> 式が使用さ </span> れます。 </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">それ以外の場合は、フィールド値が2つの連続する範囲値 <span class="uicontrol"> (&gt;=より小さい値（&gt;=より大きい値）と小さい値(&lt;)の間にある範囲が見つかり、中間形式が使用され </span><span class="uicontrol"></span> ます </li> 
    </ul> </p> <p>チェックを外すと、 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">値が範囲値の最小値(&lt;)より小さい場合、「 <span class="uicontrol"> 小さい」 </span>形 <span class="uicontrol"> 式が使用さ </span> れます。 </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">値が範囲値の最大値(&gt;=)以上の場合、「次より大きい」 <span class="uicontrol"> の形 </span>式 <span class="uicontrol"> が使用さ </span> れます。 </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">それ以外の場合は、フィールド値が2つの連続する範囲値 <span class="uicontrol"> （&gt;より大きい値）と小さい値（&lt;=より大きい値）の間にある範囲が見つかり、中間形式が使用され </span><span class="uicontrol"></span> ます </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p>「範囲の説明を作成」がオ <span class="uicontrol"> ンになってい </span> て、「範囲フィールド」項目が選 <span class="uicontrol"> 択されている場 </span> 合にのみ使用できます。 </p> <p>サンプルの数値を入力し、「テスト」ボタ <span class="uicontrol"> ンを </span> 押して、範囲フィールドの作成方法を確認します。 生成された範囲の説明がウィンドウに表示されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   新しいメタタグフ [ィールドの追加も参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。
1. クリック **[!UICONTROL Add]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 事前定義済みまたはユーザ定義のメタタグフィールドの編集 {#task_0A7657B63596421BB6DB3ED44F827AB3}

編集できるのは、事前定義のmetaタグ内の特定のフィールドだけです。または、metaタグ内のユーザー定義のすべてのフィールドを編集できます。

メタタグの変更の効果を顧客に表示する前に、サイトインデックスを再構築する必要があります。

**事前定義またはユーザ定義のメタタグフィールドを編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Definitions]**。
1. ページ [!DNL Definitions] のテーブル [!DNL Actions] の列で、変更するメ **[!UICONTROL Edit]** タタグフィールド名の行をクリックします。
1. ページ [!DNL Pinned Keyword Results Manager] の表で、変更するキーワ **[!UICONTROL Edit]** ードの行をクリックします。
1. ページ [!DNL Edit Field] で、必要なオプションを設定します。

   事前定義のmetaタグフィールドに変更を加える場合は、編集できないフィールドがあることに注意してください。

   新しいメタタグフィールドの追加のオ [プションの表を参照してください](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ユーザー定義のメタタグフィールドの削除 {#task_9361EF38B5E743038B6672FA6CF70FD3}

不要になった、または使用しなくなったユーザー定義のメタタグフィールドを削除できます。

事前定義のメタタグフィールドは削除できません。 ただし、特定のフィールドを編集できます。

詳しくは、 [事前定義またはユーザ定義のメタタグフィールドの編集を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)い。

削除メタタグの効果を顧客に表示する前に、サイトインデックスを再構築する必要があります。

**ユーザー定義のメタタグフィールドを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Definitions]**。
1. ページ [!DNL Definitions] のテーブルのセ [!DNL User-defined fields] クションで、削 **[!UICONTROL Delete]** 除するメタタグフィールド名の行をクリックします。
1. 確認ダイアログボックスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 注射について {#concept_DA091920671948A0A893A26B3A2FAAE5}

を使用すると、ペ [!DNL Injections] ージ自体を編集する必要なく、Webページにコンテンツを挿入できます。

「target」や「body」など、特定のインデックス付きフィールドにコンテンツを追加したり、インデックス付きコンテンツを新しい値で置き換えたりできます。 例えば、「target」メタタグフィールドに新しいコンテンツを挿入した場合、この情報は、ページのコンテンツをハードコードする場合と同様に扱われます。 サイトページに対応するコンテンツがあるかどうかに関係なく、あらかじめ定義されたメタタグフィールドのコンテンツを編集できます。 例えば、次の事前定義のメタタグフィールド名の内容を編集できます。

* ALT
* body
* charset
* date
* desc
* キー
* language
* target
* title
* url

## テストフィールドインジェクションの操作 {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

オプションで、ページ **[!UICONTROL Test]** で使用で [!DNL Staged Injections] きます。 Webサイトのテストフィールド名（「タイトル」や「本文」など）、元のフィールド値（「ホームページ」など）、テストURLを入力します。 参照用に結果の値が表示されます。 現在の値は、テスト中は変更されません。

## フィールド挿入定義の操作 {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

インジェクション定義の形式は次のとおりです。

```
append|replace field [regexp] URL value
```

The `append|replace`, `field`, `URL`. および `value` 項目は必須です。 1行につき1つの射出定義を入力します。 次の例には、6つの異なる挿入定義が含まれています。

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
   <th colname="col1" class="entry"> <p>挿入の定義 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> append|replace </span> </p> </td> 
   <td colname="col2"> <p>「append」を選択して、挿入定義(「Adobe:お問い合わせ、または「今すぐ販売中！」 上の例で)を既存のフィールドの内容に置き換えます。 「置換」を選択すると、既存のフィールドの内容が定義された値で上書きされます。 フィールドにコンテンツがない場合は、どのオプション（追加または置換）が使用されているかに関係なく、定義された値が自動的に追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field </span> </p> </td> 
   <td colname="col2"> <p>フィールド名は必須です。 次の10個の定義済みフィールド名を使用できます。 </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> キー </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> title </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>各フィールド名は、サイトページの要素に対応します。 例えば、フィールド名 <span class="codeph"> descを指 </span> 定した場合、サイトページの説明Metaタグに対応するフィールドにインジェクション定義値を追加できます。 </p> <p>説明Metaタグがページに存在しない場合、定義済みのコンテンツによってタグが作成されます。 注釈挿入で指定されたコンテ <span class="codeph"> ンツは、 </span> ハードコードされたメタ説明のコンテンツと同じように、結果ページに表示されます。 </p> <p>同じフィールド名を使用して複数の定義を作成することもできます。 例えば、以下のような注射があるとします。 </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>上記の例のすべてのサイトページに、「Welcome to My Site」というタイトルが挿入されます。 「/company/」フォルダ内のページに、「My Site:「お問い合わせ」をクリックします。 </p> <p>インジェクションは、「フィールドインジェクション定義」( <span class="wintitle"> Field Injection Definitions)テキストボックスに表示される順に適用さ </span> れます。 同じ場所にあるページに対して同じフィールド（この例では「title」）が複数回定義されている場合、後の定義が優先されます。 </p> <p> <span class="codeph"> [regexp] </span> — オプション。 regexpオプションを使用する <span class="codeph"> と、 </span> 定義されたURLが正規表現として扱われます。 </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してくださ </a>い。 </p> <p>次の定義では、 </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> 「重要な情報」は、正規表現^に一致するすべてのページの「target」フィールドに挿入され <span class="codeph"> ます。*/products/.*\.html$ </span>. </p> <p>したがって、次のようになります。 </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>次の例では、 </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>このインジェクションは、ファイル名拡張子が「.pdf」で終わるすべてのページの「タイトル」コンテンツに「Millennium Science」を追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>URLは必須で、挿入するドキュメントを指定します。 </p> <p>URLは、次のいずれかです。 </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> フルパス(https://www.mydomain.com/products.htmlなど) </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> 部分パス(https://www.mydomain.com/productsなど) </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> ワイルドカードを使用するURL(https://www.mydomain.com/*.htmlなど) </li> 
     </ul> </p> <p>URL値にはスペース文字を含めることはできません。 regexpオプション <span class="codeph"> を </span> 使用すると、URLは正規表現のように扱われます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>値は必須で、既存のフィールドの内容を置き換えるか、既存のフィールドの内容に追加するために使用します。 同じフィールド名に対して複数の値を指定できます。 次に例を示します。 </p> <p>キーを <b>追加</b> https://www.mysite.com/travel/ summer <b>、</b>beach <b>、</b><b>sand</b> </p> <p>キーを追加 <b>する</b> https://www.mysite.com/travel/fare/*.html割安 <b>チケット</b> </p> <p>上記の例では、「/travel/」ディレクトリ内のすべてのページの「keys」フィールドに「summer, beach, sand」という語が追加されています。 また、「cheap tickets」という単語は、「/travel/fare/」ディレクトリ内のすべてのページの「keys」フィールドにも追加されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

クロールおよびイ [ンデックスを作成するコンテンツタイプの選択も参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)い。

## フィールド挿入定義の追加 {#task_E86566FA1FF74CF68115C0ADA05172AE}

を使用すると、ペ [!DNL Injections] ージ自体を編集する必要なく、Webページにコンテンツを挿入できます。

オプションで、ページ **[!UICONTROL Test]** で使用で [!DNL Injections] きます。 Webサイトのテストフィールド名（「タイトル」や「本文」など）、元のフィールド値（「ホームページ」など）、テストURLを入力します。 参照用に結果の値が表示されます。 現在の値は、テスト中は変更されません。

**フィールド挿入定義を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Injections]**。
1. （オプション）ペー [!DNL Injections] ジの領域で、テ [!DNL Test Field Injections] ストフィールド、テスト元の値、テストURLを入力し、をクリックします **[!UICONTROL Test]**。
1. フィールド [!DNL Field Injection Definitions] に、1行に1つの射出定義を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 属性ローダーについて {#concept_9EF38E98811B42CDA41996432B9AD209}

Webサイトか [!DNL Attribute Loader] らクロールされたデータを拡張する追加の入力ソースを定義する場合に使用します。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

データフィード入力ソースを使用して、Webサイトで一般に見つかるものとは異なるフォームに保存されたコンテンツにアクセスできます。 これは、使用可能なクロール方法の1つを使用して行います。 これらのソースのデータは、クロールされたコンテンツのデータに挿入できます。

ページに属性ローダ定義を追加した後、「名 [!DNL Staged Attribute Loader Definitions] 前」の値と「タイプ」の値を除く任意の設定を変更できます

このペ [!DNL Attribute Loader] ージには、次の情報が表示されます。

* 設定および追加した定義済みの属性ローダー設定の名前。
* 追加した各コネクタに対して、次のいずれかのデータソースタイプを指定します。

   * **テキスト** — 単純な「フラット」ファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。
   * **フィード** - XMLフィード

* 構成が次のクロールとインデックスに対して有効かどうか。
* データソースのアドレス。

詳しくは、テ [キストとフィードでの属性挿入プロセスの仕組みも参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

複数の属性ローダ [ーの設定についても参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

属性を追加 [する際のプレビューの使用についても参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## 属性ローダーのテキスト設定とフィード設定での属性挿入プロセスの動作 {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、単純なファイルのダウンロードです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p>テキ <span class="uicontrol"> スト </span>の場合、改行で区切られた各行のテキストは個々のドキュメントに対応し、コンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p>フィー <span class="uicontrol"> ド </span>の場合、各ドキュメントのデータは次の形式の正規表現パターンを使用して抽出されます。 </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>[属性ロ <span class="uicontrol"> ーダ </span> の追加]ペ <span class="wintitle"> ージの[マップ]を使用し </span> て、データのキャッシュされたコピーを作成し、クローラのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが入力されます。 </p> <p>解析されたデータがローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは、後で読み取られ、クローラーが必要とする単純なHTMLドキュメントを作成します。 例： </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>&lt;title&gt; <span class="codeph"> 要素は、タ </span> イトルメタデータフィールドにマッピングが存在する場合にのみ生成されます。 同様に、 <span class="codeph"> &lt;body&gt;要素は、Body </span> メタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義されたURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについて <span class="codeph"> は、元のドキ </span> ュメント内のデータを含む各フィールドに対して&lt;meta&gt;タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれる各ドキュメントに対して、次の例のようにリンクも生成されます。 </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングには、主キーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取り込まれる際に使用されるキーを形成します。 </p> <p>クローラはURLインデックスを認 <span class="codeph"> 識します。スキーム </span> のプレフィックス。ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p>インデッ <span class="codeph"> クス：リン </span> クは、クローラーの保留リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、そのドキュメントのデータがキャッシュから取得されます。 次に、HTML画像を「アセンブル」して処理し、インデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 複数の属性ローダの設定について {#section_4CC49C74EF294608A184E233F215ADFF}

任意のアカウントに対して複数のAttribute Loader設定を定義できます。

属性ローダを追加する場合、オプションでこの機能を使用して、デ **[!UICONTROL Setup Maps]** ータソースのサンプルをダウンロードできます。 データが適合性を調べられる。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Attribute Loader type </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>テキスト </p> </td> 
   <td colname="col2"> <p>最初にタブを試し、次に縦棒( <span class="codeph"> | </span>)と最後のコンマ( <span class="codeph"> , </span>)。 「マップの設定」をクリックする前に区切り値を既に指 <span class="uicontrol"> 定してい </span>る場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なタグとフィールドの値に推測が入力されます。 さらに、解析されたデータのサンプリングが表示されます。 ファイルにヘッダー行が含ま <span class="uicontrol"> れていることがわか </span> っている場合は、必ず「最初の行のヘッダー」を選択してください。 この情報を使用して、結果のマップエントリをより適切に識別します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子は、Mapテーブルのタグ行に表示され、同様の値がFieldsに表示されます。 これらの行は使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータを説明し、Itemtagを識別するので、この機能は役に立ちます。 </p> <p> <p>注意： マップの設定機能は、分析を実行するためにXMLソース全体をダウンロードします。 ファイルのサイズが大きい場合は、この操作がタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は、使用が望ましくないXPath項目をすべて識別します。 必ず、結果のMap定義を確認し、不要または不要なMap定義を削除してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>ファイルパーサーがファイル全体をメモリに読み込もうとするので、マップの設定機能は大きなXMLデータセットに対しては動作しない場合があります。 その結果、メモリ不足状態が発生する可能性があります。 ただし、インデックス作成時に同じドキュメントが処理された場合、そのドキュメントはメモリに読み込まれません。 その代わり、大きなドキュメントは「外出先で」処理され、最初にメモリに読み込まれることはありません。

## アトリビュートローダを追加する際のプレビューの使用について {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

属性ローダのデータは、インデックス操作の前に読み込まれます。

アトリビュートローダを追加する際、オプションでデータを検証す **[!UICONTROL Preview]** る機能を使用できます。保存したかのように使用できます。 設定に対するテストを実行しますが、設定をアカウントに保存しません。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラが使用するメインキャッシュフォルダと競合しません。

「プレビュー」は、 **Acct:IndexConnector-Preview-Max-Documentsで制御される5つのドキュメントのデフォルトのみを処理します**。 プレビューされたドキュメントは、インデックス作成クローラに表示されるとおり、ソース形式で表示されます。 この表示は、Webブラウザの「ソースの表示」機能に似ています。 プレビューセット内のドキュメントは、標準のナビゲーションリンクを使用して移動できます。

プレビューはXML設定をサポートしません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## 属性ローダ定義の追加 {#task_A735E5EF763343A9B675E1A3B09AFDBC}

各Attribute Loaderの設定では、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

新しい有効な定義の効果が顧客に表示される前に、サイトインデックスを再構築します。

**アトリビュートローダ定義を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページ上で、 [!DNL Stage Attribute Loader Definitions] をクリックしま **[!UICONTROL Add New Attribute Loader]**&#x200B;す。
1. ページ [!DNL Attribute Loader Add] で、必要な設定オプションを設定します。 使用できるオプションは、選択したオプションに **[!UICONTROL Type]** よって異なります。

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
      <td colname="col2"> <p>属性ローダー設定の一意の名前。 英数字を使用できます。 「_」と「 — 」も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択したデータソースタイプは、[属性ローダの追加]ページで使用できる結果のオプシ <span class="wintitle"> ョンに影響を与 </span> えます。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行で区切られた各テキスト行は、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）を、1から始まる列番号で参照されるメタデータフィールドにマップできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むマスターXMLドキュメントをダウンロードします。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>設定を「オン」にして使用します。 または、設定を「オフ」にして、使用しない場合は防ぐことができます。 </p> <p> <b>注意</b>:無効な属性ローダの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>このURIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドの適切なエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、HTTPサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTP、またはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で指定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、またはHTTPS接続の再試行の最大回数を指定します。 この値は0 ～ 10の範囲で指定する必要があります。 </p> <p>値が0の場合、再試行は行われません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の各フィールドの区切り文字を指定します。 </p> <p>コンマ文字( <span class="codeph"> , </span>)は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るフィールド区切り文字として機能します。 </p> <p>タブを選 <span class="uicontrol"> 択しますか？ </span> をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭行のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日 </p> </td> 
      <td colname="col2"> <p>属性ローダのデータのダウンロード間隔の最小値を設定します。 ダウンロード更新頻度の間隔内で発生するインデックスによってトリガーされるダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内にAttribute Loaderデータが複数回ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1(1)にして、列番号を指定します。 各列に新しいマップ行を追加するには、「アクション」の「 <span class="wintitle"> +」 </span>をクリック <span class="uicontrol"> しま </span>す。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップするように選択できます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p>フィールド <span class="uicontrol"> が </span> コンボボックスになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応 <span class="uicontrol"> じて、 </span> Field値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、フィルタリングスクリプトで使用するコンテンツの作成に役立 <span class="wintitle"> つ場合がありま </span>す。 </p> <p>スクリプトのフ <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> ィルタリングについてを参照してく </a>ださい。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>主キーとして識別されるフィールドは1つだけです。 このフィールドは、属性ローダのデータとインデックス内の対応するドキュメントとを一致させる「外部キー」として使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグが削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：フィード</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>設定を「オン」にして使用します。 または、設定を「オフ」にして、使用されない場合は防ぐことができます。 </p> <p> <b>注意</b>:無効な属性ローダの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>このURIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドの適切なエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含むマスターXMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、HTTPサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、次のAdobe XMLドキュメントのフィードフラグメントでは、Itemタグの値はレコード <span class="codeph"> です </span>。 </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>値がアトリビュートローダ設定のデータの「キー」の参照として使用されるメタデータフィールドを指定します。 値が選択されていない場合(<b>—None—</b>)、この設定のデータは、ランキングの計算で使用できません(<b>Rules</b> / <b>Ranking Rules</b> / <b>Edit Rules</b>Rules/Edit Rules Edit Rules)。 値を選択すると、このフィールドの値を使用して、この設定のデータを含むサイト検索/マーチャンダイジングドキュメントを相互参照します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日 </p> </td> 
      <td colname="col2"> <p>属性ローダのデータのダウンロード間隔の最小値を設定します。 ダウンロード更新頻度の間隔内で発生するインデックスによってトリガーされるダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内にAttribute Loaderデータが複数回ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobe XMLドキュメントを使用して、オプションItemtagの下で、次の構文を使用してマッピングできます。 </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>レコード <span class="codeph"> 要素のdisplayurl属 </span> 性は、メタデ <span class="codeph"> ータ </span> フィールドのpage-url <span class="codeph"> にマップされま </span>す。 </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素のコンテンツ、 </span><span class="codeph"> メタ要素内に含まれるレコード要素、名前メタデータ要素内に含まれるメタ要素、メタデータ要素内に含まれるメタデータ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素、メタデータ要素内にマップされるレコード要素。 </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素の内容、レコード要素内に含まれるレコード要素、名前メタデータ </span> 属性内に含まれるレコード要素、メタデータフィールド <span class="codeph"> 内にマップされるメタ要素 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>の内容。 </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素 </span> の内容、レコード要素内に含まれる <span class="codeph"></span> メタ要素内の内容、メタデータ要素内のメタデータ要素内のメタデータ <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素内のメタデータ要素とメタデータ要素本体との対応付けを行う。 </p> </li> 
        </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p>https://www.w3schools.com/xpath/を参照して <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> ください </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性 <span class="codeph"> 値を定義し </span> ます。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p>フィールド <span class="uicontrol"> が </span> コンボボックスになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応 <span class="uicontrol"> じて、 </span> Field値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、フィルタリングスクリプトで使用するコンテンツの作成に役立 <span class="wintitle"> つ場合があり </span>ます。 </p> <p>スクリプトのフ <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> ィルタリングについてを参照してく </a>ださい。 </p> <p>属性ローダーで、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、結果のキャッシュされたドキュメントで、複数の値が1つの値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field値が定義済み </span> のメタデータフィールドであるとします。 また、このフィールドには「リストを許可」属 <span class="wintitle"> 性が設定さ </span> れています。 この場合、フィールドのList Delimiters値（最初に定義された区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>主キーとして識別されるフィールドは1つだけです。 このフィールドは、属性ローダのデータとインデックス内の対応するドキュメントとを一致させる「外部キー」として使用されます。 </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグが削除されます。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）をクリック **[!UICONTROL Setup Maps]** して、データソースのサンプルをダウンロードします。 データが適合性を調べられる。
1. をクリック **[!UICONTROL Add]** して、ページに設定を追加 [!DNL Attribute Loader Definitions] します。
1. ページ上で、 [!DNL Attribute Loader Definitions] をクリックしま **[!UICONTROL rebuild your staged site index]**&#x200B;す。
1. （オプション）ページで、 [!DNL Attribute Loader Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 属性ローダ定義の編集 {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

定義済みの既存のアトリビュートローダを編集できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

ドロップダウンリストから「属性ローダ名」や「タイプ」など、属性ローダのオプションを変更できな [!DNL Type] い場合があります。

**アトリビュートローダの定義を編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader] 列見出しの下 [!DNL Actions] で、設定を変 **[!UICONTROL Edit]** 更するAttribute Loader定義名をクリックします。
1. ページで、 [!DNL Attribute Loader Edit] 必要なオプションを設定します。

   「属性ローダ定義の追加」のオ [プションの表を参照してください](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ページで、 [!DNL Attribute Loader Definitions] をクリックしま **[!UICONTROL rebuild your staged site index]**&#x200B;す。
1. （オプション）ページで、 [!DNL Attribute Loader Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 属性ローダ定義のコピー {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

既存のアトリビュートローダ定義をコピーして、作成する新しいアトリビュートローダの基本として使用できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

アトリビュートローダ定義をコピーする場合、コピーされた定義はデフォルトで無効になっています。 定義を有効または「有効にする」には、ページから編集し、を選択 [!DNL Attribute Loader Edit] する必要がありま **[!UICONTROL Enable]**&#x200B;す。

「属性ロ [ーダ定義の編集」を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)い。

**属性ローダ定義をコピーするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader] 列見出しの下 [!DNL Actions] で、設定を複製 **[!UICONTROL Copy]** するアトリビュートローダ定義名をクリックします。
1. ページ [!DNL Attribute Loader Copy] で、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）ページで、 [!DNL Attribute Loader Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 属性ローダ定義の名前の変更 {#task_58D5DFD7EBC04111BCB91118E4440DB4}

既存のアトリビュートローダ定義の名前を変更できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

**アトリビュートローダ定義の名前を変更するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader] 列見出しの下 [!DNL Actions] で、変更する属 **[!UICONTROL Rename]** 性ローダ定義名をクリックします。
1. ページ [!DNL Attribute Loader Rename] で、フィールドに定義の新しい名前を入力し [!DNL Name] ます。
1. クリック **[!UICONTROL Rename]**.
1. （オプション）ページで、 [!DNL Attribute Loader Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 属性ローダデータの読み込み {#task_2F3C55189B0A4049AB2113F2291CC181}

設定したAttribute Loaderデータをサイト検索/マーチャンダイジングにダウンロードできます。

このペ [!DNL Data Load] ージには、最後に実行した属性ローダのデータ読み込み操作のステータスに関する次の情報が表示されます。

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
   <td colname="col1"> <p>開始時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ読み込み操作が開始された日時を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>停止時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ・ロード操作の完了日時が表示されます。 または、現在のデータ読み込み操作がまだ進行中であることを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**アトリビュートローダデータを読み込むには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページ上で、 [!DNL Attribute Loader Definitions] をクリックしま **[!UICONTROL Load Attribute Loader Data]**&#x200B;す。
1. ページで、 **[!UICONTROL Attribute Loader Data Load]** 次のいずれかの操作を行います。

   * をクリック **[!UICONTROL Start Load]** して、読み込み操作を開始します。

      データの読み込み操作中に、**Progress** 行に進行状況に関する情報が表示されます。

   * をクリック **[!UICONTROL Stop Load]** して、読み込み操作を停止します。

1. をクリッ **[!UICONTROL Close]** クして、ページに戻 [!DNL Attribute Loader Definitions] ります。

## 属性ローダデータのプレビュー {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

プレビュー(Preview)を使用して、最も最近ロードされたアトリビュートローダのデータを表示できます。

表の「行」列には、各データ行の数が表示され、属性ローダの値が読み込まれた元の順序が示されます。

残りの列には、各エントリに関連付けられている値が表示されます。

テーブルが空の場合は、まだ属性ローダのデータがロードされていないことを意味します。 ページを閉じてから、 [!DNL Attribute Loader Data Preview] アトリビュートローダのデータを読み込むことができます。

詳しくは、属 [性ローダデータの読み込みを参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)い。

**アトリビュートローダのデータをプレビューするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader Definitions] 列の下で、ダウ [!DNL Actions] ンロードしたデ **[!UICONTROL Preview]** ータを表示する設定のをクリックします。
1. ページ上 [!DNL Attribute Loader Data Preview] 部および下部のナビゲーションと表示オプションを使用して、データを表示します。

   データを昇順または降順で並べ替えるには、テーブルの列見出しをクリックします。
1. 次のいずれかの操作を行います。

   * をクリ **[!UICONTROL Download to Desktop]** ックして、テーブルを.xltファイルとしてダウンロードし、保存します。
   * アトリビュートローダのデータのプレビューが終了したら、ページを閉じ、前に表示したページに戻ります。

## アトリビュートローダ定義の設定の表示 {#task_EA99A9694FE948ADA82C1DBA0667851B}

既存のアトリビュートローダ定義の設定を確認できます。

属性ローダの定義をページに追加した後 [!DNL Attribute Loader Definitions] は、そのタイプの設定を変更できません。 代わりに、定義を削除し、新しい定義を追加する必要があります。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

**アトリビュートローダ定義の設定を表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader] 列見出しの下 [!DNL Actions] で、設定を確認また **[!UICONTROL Edit]** は編集するAttribute Loader定義名をクリックします。

## 最新の属性ローダのデータ・ロードからのログの表示 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

を使用して、最新 [!DNL View Log] のダウンロードプロセスのAttribute Loaderデータログファイルを調べることができます。 また、ログビューを使用して、実行中のダウンロードを監視することもできます。

詳しくは、属 [性ローダデータの読み込みを参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)い。

**最新のアトリビュートローダのデータ読み込みのログを表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページ上で、 [!DNL Attribute Loader Definitions] をクリックしま **[!UICONTROL View Log]**&#x200B;す。 ログページ、
1. ページ上 [!DNL Attribute Loader Data Log] 部および下部のナビゲーションと表示オプションを使用して、ログ情報を表示します。
1. 完了したら、ページを閉じてページに戻り [!DNL Attribute Loader Definitions] ます。

## 属性ローダ定義の削除 {#task_E8980F66888B476E98C228C1D307EDF8}

不要になった既存のアトリビュートローダ定義を削除したり、使用しなくなったりできます。

>[!NOTE]
>
>Attribute Loaderを使用するには、アドビのアカウント担当者またはアドビサポートによって、アカウントで有効にする必要がある場合があります。

**アトリビュートローダ定義を削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Attribute Loader]**。
1. ページの [!DNL Attribute Loader Definitions] 列見出しの下 [!DNL Actions] で、削除する属 **[!UICONTROL Delete]** 性ローダ定義名をクリックします。
1. ページ上で、 [!DNL Attribute Loader Delete] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
