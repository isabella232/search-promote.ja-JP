---
description: メタデータメニューを使用して、検索定義とインデックス挿入をカスタマイズします。
solution: Target
subtopic: Metadata
title: メタデータメニューについて
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '8029'
ht-degree: 1%

---


# メタデータメニューについて{#about-the-metadata-menu}

メタデータメニューを使用して、検索定義とインデックス挿入をカスタマイズします。

## 定義について{#concept_AE48035C210145169BE067D396975620}

[!DNL Definitions]を使用すると、顧客が検索クエリを送信したときに考慮されるHTMLフィールドとメタデータフィールドの内容と関連性をカスタマイズできます。

既に定義済みのフィールドは編集できます。 また、メタデータタグのコンテンツに基づいて、新しいユーザ定義フィールドを作成することもできます。 各定義は[!DNL Staged Definitions]ページの1行に表示されます。

[データ表示について](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)も参照してください。

## 新しいメタタグフィールドの追加{#task_6DF188C0FC7F4831A4444CA9AFA615E5}

独自のメタデータタグフィールドを定義して追加できます。

新しいメタタグ定義の効果がユーザーに表示される前に、サイトインデックスを作成し直す必要があります。

**新しいメタタグフィールドを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページで、**[!UICONTROL Add New Field]**&#x200B;をクリックします。
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
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> 名前には、英数字のみを使用する必要があります。 </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> ダッシュは名前の中で使用できますが、スペースは使用できません。 </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> 20文字以内の名前を入力できます。 </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> 名前は大文字と小文字が区別されませんが、入力したとおりに表示および保存されます。 </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> <span class="wintitle"> Staged Definitions </span>ページの表に示すように、事前定義済みのフィールドに存在する名前は使用できません。 </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> ユーザ定義フィールド名の値として「any」という語を使用することはできません。 </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> 事前定義済みのフィールドの名前は編集できません。 </li> 
      </ul> </p> <p> フィールド名の例： </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> 作成者 </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublishDate </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> 何か異常な </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>メタタグ名 </p> </td> 
      <td colname="col2"> <p>定義済みのフィールドに関連付けられている内容を決定します。 </p> <p>名前のリストは255文字までです。 また、nameには、HTMLメタタグのname属性で許可されている任意の文字を含めることができます。 </p> <p>1つのフィールド定義で複数のmetaタグを指定できます。 </p> <p>複数の値はコンマで区切る必要があり、特定のWebページで見つかった左端のメタタグ名が優先されます。 </p> <p>例えば、「auth」という名前のフィールドを定義したとします。 フィールド名には、「author, dc.author」というメタタグが関連付けられています。 この場合、「author」メタタグのコンテンツのインデックスが作成され、両方のメタタグがWebページに表示される場合は、「dc.author」のコンテンツが検索されます。 </p> <p>ユーザ定義フィールドの定義には、メタタグ名が少なくとも1つ必要です。 事前定義済みのフィールドには、メタタグを関連付ける必要はありません。 ただし、1つ以上のmetaタグを指定した場合は、metaタグの内容が各タグの現在のデータソースよりも優先されます。 </p> <p>例えば、メタタグ「dc.title」が事前定義済みの「title」フィールドに関連付けられている場合、「dc.title」メタタグのコンテンツは、 
      <code>
        &lt;title&gt; 
      </code>タグを追加します。 </p> <p>次に例を示します。 </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> 固有タグ </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>データタイプ </p> </td> 
      <td colname="col2"> <p>すべてのフィールドには、テキスト、数値、日付、バージョン、ランク、場所など、関連するデータタイプがあります。 このデータ型は、フィールドのコンテンツのインデックスを作成し、検索する方法、およびオプションで並べ替える方法を決定します。 </p> <p>フィールド定義を作成した後は、データ型を変更できません。 </p> <p>次の情報は、フィールドに含まれる情報に関連するデータ型を選択する際に役立ちます。 </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> テキスト </span> データ型のフィールドは、文字列として扱われます。 </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> 数値 </span> データ型のフィールドは、整数または浮動小数点の数値として扱われます。 </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> 日付 </span> データ型のフィールドは、日付/時間指定子として扱われます。新しいフィールドを追加または編集する際に、許可されている日付/時間形式をカスタマイズできます。 </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> バージョン </span> データ型のフィールドは、自由形式の数値データとして扱われます。例えば、1.2.3では1.2.2より前に並べ替えが行われます。 </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> ランク </span> データ型のフィールドは、検索結果でのランク付け/関連性の計算にさらに影響する点を除いて、「Number」タイプのフィールドと同じように扱われます。 <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">ランキングルールについて</a>を参照してください。 </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> 場所の </span> データ型のフィールドは、世界のどこでも物理的な場所として扱われます。使用できる場所の形式は次のとおりです。 <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> 5桁または9桁の郵便番号。DDDDDDまたはDDDDDD-DDDDの形式で入力します。各「D」は0 ～ 9桁の数字です。 </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> DDD形式の3桁の市外局番。 </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> 緯度/経度の組み合わせ（±DD.DDDD±DDD.DDDDの形式）。最初の数字は緯度を、2番目の数字は経度を表します。 </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>許可リスト </p> </td> 
      <td colname="col2"> <p>データタイプ<span class="uicontrol"> [テキスト</span>]または[<span class="uicontrol">番号</span>]が選択されている場合にのみ使用できます。 </p> <p>このフィールドのメタデータコンテンツ内の区切り値を個別にインデックス化します。 </p> <p>例えば、「許可リスト」が選択されている場合、コンテンツ「Red, Yellow, Green, Blue」は、1つではなく4つの個別の値として扱われます。 この処理は、範囲検索( 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code>または 
      <code>
        sp_q_exact 
      </code>)および 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code>および 
      <code>
        &lt;search-display-field-values&gt; 
      </code>。 </p> <p>「Version」データ型が選択されている場合は使用できません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 動的ファセット </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>注意：この機能は、デフォルトでは有効になっていません。テクニカルサポートに問い合わせて、使用するライセンス認証を行ってください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたファセットを動的に設定します。 </p> <p>ファセットは、メタタグフィールドの上に構築されます。 メタタグフィールドは、AdobeSearch&amp;Promoteの低レベルの中核的な検索層です。 一方、ファセットはGS（ガイド付き検索）の一部で、AdobeSearch&amp;Promoteの高レベルなプレゼンテーション層です。 ファセット自体のメタタグフィールドは、ファセットに関する情報を何も持っていません。 </p> <p><a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">動的ファセットについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>重複除外を許可 </p> </td> 
      <td colname="col2"> <p>このフィールドの重複排除 - 重複を有効にする場合は、このオプションを選択します。 つまり、このフィールドを検索時に 
        <code>
          sp_dedupe_field 
        </code> CGIパラメータを検索します。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テーブル名 </p> </td> 
      <td colname="col2"> <p>指定したフィールドを指定したテーブル名と永続的に関連付けます。 </p> <p>このようなフィールドがコア検索CGIパラメータやテンプレートタグ内で言及されると、自動的にテーブル名が提供されます。 この機能を使用すると、テーブルの一致によって動的ファセットを選択できますが、必要に応じて、動的でないファセットフィールドにも使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>リスト区切り文字 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">許可リスト</span>が選択されている場合にのみ使用できます。 </p> <p>個々のリスト値を区切る文字を指定します。 複数の文字を指定できます。各文字は値の区切り文字として扱われます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトで検索 </p> </td> 
      <td colname="col2"> <p>このオプションを選択すると、所定の検索クエリでフィールドが明示的に指定されていない場合でも、フィールドコンテンツが検索されます。 このオプションの選択を解除すると、フィールドは要求された場合にのみ検索されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直方向の更新フィールド </p> </td> 
      <td colname="col2"> <p> <p>注意：この機能は、デフォルトでは有効になっていません。テクニカルサポートに問い合わせて、使用するライセンス認証を行ってください。 アクティブ化すると、ユーザーインターフェイスに表示されます。 </p> </p> <p>識別されたフィールドを[垂直方向の更新]フィールドに設定します。 </p> <p>縦置き版の更新フィールドは、縦置き版の更新処理（<span class="uicontrol">インデックス</span> &gt; <span class="uicontrol">縦置き版の更新</span>）によって更新される候補です。 垂直方向の更新が行われる方法により、これらのフィールドのコンテンツはフリーテキスト検索では検索できません。 このオプションを選択すると、どのようなインデックス操作でも、このフィールドの内容が「word」インデックスに追加されません。 また、「垂直方向の更新」操作中に、このフィールドを更新できます。 </p> <p>垂直方向の更新について詳しくは、<a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">垂直方向の更新について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>関連度 </p> </td> 
      <td colname="col2"> <p>事前定義済みのフィールドとユーザ定義のフィールドの関連性を編集できます。 </p> <p>関連性は1～10の尺度で特定される。 設定値が1の場合は、最も関連性が低く、10が最も関連性が高いことを意味します。 これらの値は、クエリが各フィールドで一致すると考える場合に考慮されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>並べ替え </p> </td> 
      <td colname="col2"> <p>指定したフィールドで結果を並べ替えるタイミングを、 
        <code>
          sp_s 
        </code> CGIパラメータを検索します。 </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGIパラメーターの検索</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>言語 </p> </td> 
      <td colname="col2"> <p>データタイプ<span class="uicontrol">ランク</span>、<span class="uicontrol">番号</span>、または<span class="uicontrol">日付</span>が選択されている場合にのみ使用できます。 </p> <p>このフィールドの日付、数値およびランクの値のインデックス作成時に適用される言語およびロケールの規則を制御します。 </p> <p>アカウントの言語を適用することを選択できます（言語/単語と言語）。 または、各数字や日付の値を含むドキュメントに関連付けられた言語、または特定の言語を適用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>日付の形式 </p> </td> 
      <td colname="col2"> <p>データタイプ<span class="uicontrol">日付</span>が選択されている場合にのみ使用できます。 </p> <p>このフィールドの日付値のインデックスを作成する際に認識される日付形式を制御します。 </p> <p>各日付フィールドには、日付形式文字列のデフォルトのリストが提供されます。 リストにを追加したり、リストを編集してサイトのニーズに合わせたりできます。 </p> <p><a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local">日付形式</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト用の日付形式 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「<span class="uicontrol">日付</span>」が選択されている場合にのみ使用できます。 </p> <p>指定した日付形式をプレビューして、正しく形式設定されていることを確認できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムゾーン </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「<span class="uicontrol">日付</span>」が選択されている場合にのみ使用できます。 </p> <p>タイムゾーンを指定しないこのフィールドの日付値をインデックス付けする際に適用される想定タイムゾーンを制御します。 </p> <p>例えば、アカウントのタイムゾーンを「米国/ロサンゼルス」に設定し、「<span class="uicontrol">アカウントのタイムゾーンを使用</span>」を選択した場合、次のメタ日付値は、指定したタイムゾーンを持たない太平洋時間として扱われ、夏時間を考慮します。 </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要でないランクの値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「<span class="uicontrol">ランク</span>」が選択されている場合にのみ使用できます。 </p> <p>任意のドキュメントの最小ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクの範囲が0（最低）から10（最高）の場合、この値を0に設定します。 </p> <p>ドキュメントのランクの範囲が1（最上位）から10（最下位）の場合、この値を10に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>デフォルトのランク値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「<span class="uicontrol">ランク</span>」が選択されている場合にのみ使用できます。 </p> <p>ドキュメントに、このランクフィールドに定義されたメタタグが含まれていない場合に使用するランク値を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最も重要なランクの値 </p> </td> 
      <td colname="col2"> <p>データタイプとして「<span class="uicontrol">ランク</span>」が選択されている場合にのみ使用できます。 </p> <p>任意のドキュメントの最大ランクを表すランク値を制御します。 </p> <p>ドキュメントのランクの範囲が0（最低）から10（最高）の場合、この値を10に設定します。 </p> <p>ドキュメントのランクの範囲が1（最上位）から10（最下位）の場合、この値を1に設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>既定の単位 </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「<span class="uicontrol">場所</span>」が選択されている場合にのみ使用できます。 </p> <p>近接検索の距離値の処理を制御します。 </p> <p>デフォルトの単位を<span class="uicontrol">マイル</span>に設定した場合、( 
      <code>
        sp_q_min[_#] 
      </code>または 
      <code>
        sp_q_max[_#] 
      </code>検索CGIパラメーター)はマイルとして扱われ、それ以外はキロメートルとして扱われます。 </p> <p>このオプションは、 
      <code>
        &lt;Search-Display-Field&gt; 
      </code>検索結果テンプレートタグ（近接検索出力フィールドに適用時）。 </p> <p><a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local">近接検索について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲の説明を作成しますか？ </p> </td> 
      <td colname="col2"> <p>「データタイプ」で「<span class="uicontrol">番号</span>」が選択されている場合にのみ使用できます。 </p> <p><span class="uicontrol">デザイン</span> &gt; <span class="uicontrol">ナビゲーション</span> &gt; <span class="uicontrol">ファセット</span>で使用する、フィールド範囲の説明の自動作成を制御します。 </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local">ファセットについて</a>を参照してください。 </p> <p> <p>注意： このフィールドで<span class="uicontrol">垂直更新フィールド</span>がチェックされている場合、生成されるフィールド範囲の説明フィールドは、垂直更新時に更新されます。 ただし、<span class="uicontrol">範囲フィールド</span>で識別されたフィールドにも<span class="uicontrol">垂直更新フィールド</span>をチェックすることをお勧めします。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲フィールド </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> [範囲の説明を作成] </span>がオンの場合にのみ使用できます。 </p> <p>更新する<span class="uicontrol">テキスト</span>フィールド。現在のフィールドの範囲の説明が表示されます。 このリストには、フィールド範囲の生成で他のフィールドと共に使用されていないすべての<span class="uicontrol">テキスト</span>フィールドが含まれています。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>範囲の値 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>フィールド範囲の説明を作成する際に使用するデータポイントの空白区切りのリスト。 次に例を示します。 </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>これらの値は任意の順序で入力できます。 値は並べ替えられ、重複は保存前に削除されます。 負の値や整数以外の値も指定できます。 </p> <p>このフィールドの各値に対して、次の処理が行われます。 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">値が<span class="uicontrol">範囲値</span>内の最小値(&lt;)より小さい(&lt;)の場合、<span class="uicontrol"> "小さい"形式</span>が使用されます </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">値が<span class="uicontrol">範囲値</span>の最大値(&gt;=)以上の場合は、<span class="uicontrol"> "次よりも大きい"形式</span>が使用されます。 </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">それ以外の場合は、フィールド値が2つの連続する<span class="uicontrol">範囲値</span> (より大きい(&gt;)は小さい(&lt;=)大きい値)の間にあり、<span class="uicontrol">中間形式</span>が使用されます。 </li> 
    </ul> </p> <p>例えば、上の値のセットの例では、値の説明のセットが次のように定義されます。 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">10未満 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">10以上20未満 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">20以上50未満 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">50以上100未満 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100以上10000未満 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">10000以上 </li> 
      </ul> </p> <p><span class="uicontrol">次より大きい値を使用したテストを参照してください。 </span> を使用して、これらのテストの実行方法を変更できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"より小さい"形式 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>で見つかった最小値より小さい値の範囲の説明を指定するために使用するテンプレートです。 最小値は、数値のプレースホルダトークン<span class="uicontrol"> ～N～ </span>を使用して表します。 次に例を示します。 </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、<span class="uicontrol">範囲値</span>の定義（「5 10 20」、指定値1）では、生成される範囲の説明は「5未満」のような単純な値になります。 "4.99以下"にしたい場合は、<span class="uicontrol">精度</span>を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p><span class="uicontrol"> "次より小さい"形式</span>では、小文字<span class="uicontrol"> ～n～ </span>の値は、<span class="uicontrol">精度</span>の設定に従って<i>下</i>に丸められます。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例えば、<span class="uicontrol"> \～N～ </span>または<span class="uicontrol"> \～n～ </span> バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>中間形式 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>にある最小値と最大値の間の値の範囲の説明を指定するために使用するテンプレートです。 渡された範囲に対しては、範囲の下限値は数値プレースホルダトークン<span class="uicontrol"> ～L～ </span>を使用して表され、上限値はトークン<span class="uicontrol"> ～H～ </span>を使用して表されます。 次に例を示します。 </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>または </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>または </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、<span class="uicontrol">範囲値</span>の定義（「5 10 20」、指定値8）では、生成される範囲の説明は「5 ～ 10」のような単純な値になります。 "5 ～ 9.99"にしたい場合は、<i>下</i>に高い値を調整し、<span class="uicontrol">精度</span>を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>同様に、<span class="uicontrol"> ～L～ </span>を<span class="uicontrol"> ～l～ </span>に置き換えて、<i>上</i>の精度</span>の設定に従って、下限値を調整することができます。 <span class="uicontrol">これは、次のような定義を意味します。 </span></p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>を<span class="uicontrol">有効桁数</span>の値<span class="uicontrol"> 2 </span>に設定すると、「5.01 ～ 10」が作成されます。 </p> <p>小文字の<span class="uicontrol"> ～l～ </span>は、<span class="uicontrol">精度</span>の設定に従って<i>上</i>を丸め、小文字の<span class="uicontrol"> ～h～ </span>は、大文字の<i>下</i>を丸めます。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例えば、<span class="uicontrol"> \～L～ </span>または<span class="uicontrol"> \～h～ </span> バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>「次よりも大きい」形式 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>これは、<span class="uicontrol">範囲値</span>の最大値より大きい値の範囲の説明を指定するために使用するテンプレートです。 最大値は、数値プレースホルダートークン<span class="uicontrol"> ～N～ </span>を使用して表されます。 次に例を示します。 </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>または </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>通常、値は「そのまま」の形式で設定されます。例えば、<span class="uicontrol">範囲値</span>の定義が"5 10 20"で、指定の値が30の場合、生成される範囲の説明は"20より大きい"のような単純な値になります。 "20.01以上"にしたい場合は、<span class="uicontrol">精度</span>を<span class="uicontrol"> 2 </span>に設定し、次の形式を使用します。 </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p><span class="uicontrol"> "次よりも大きい"形式</span>では、小文字<span class="uicontrol"> ～n～ </span>の値は、<span class="uicontrol">精度</span>の設定に従って<i>上</i>に丸められます。 </p> <p>注意：範囲の説明に任意の数値プレースホルダーを含めるには、バックスラッシュ(\)プレフィックスを付けて指定します。例えば、<span class="uicontrol"> \～N～ </span>または<span class="uicontrol"> \～n～ </span> バックスラッシュ文字を含めるには、別のバックスラッシュを使用して指定します(例：<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>精度 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>小数点の右側の桁数を指定する整数値。 これは丸め処理も制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンになっていて、<span class="uicontrol">範囲フィールド</span>項目が選択され、ゼロ以外の<span class="uicontrol">有効桁数</span>値が設定されている場合にのみ使用できます。 </p> <p>「0.50」を「。50」と表示すべきですか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>末尾のゼロを削除しますか？ </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンになっていて、<span class="uicontrol">範囲フィールド</span>項目が選択され、ゼロ以外の<span class="uicontrol">有効桁数</span>値が設定されている場合にのみ使用できます。 </p> <p>「10.00」を「10」と表示すべきですか。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>千単位区切り文字を表示しますか？ </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>「10000」を「10,000」と表示すべきですか。 ロケール固有の値が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ゼロ値を調整しますか？ </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>ゼロの丸め値を表示する場合、<span class="uicontrol">精度</span>の設定に従って、切り上げまたは切り下げを行う必要がありますか。 （例：「0.01」を表示するか）。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>次よりも大きい値を使用してテストする </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>各値が<span class="uicontrol">範囲値</span>内の値と比較され、<i><b>降順</b></i>で処理されるので、デフォルトでは、次の値より大きいか等しい(&gt;=)演算子を使用して比較され、このテストが成功すると停止します。 つまり、"10 20 50 100 100 1000"のような<span class="uicontrol">範囲値</span>の場合、値100は100以上1000以下の範囲に収まります。実際には100は100以上100以下です。 50 ～ 100の範囲に含めたい場合は、このオプションを選択します。その場合、比較では代わりに「次より大きい」(&gt;)演算子が使用されます。 </p> <p>例えば、このフィールドの各値に対して、このオプションがオンの場合： 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">値が<span class="uicontrol">範囲値</span>の最小値(&lt;=)以下の場合は、<span class="uicontrol"> "次より小さい"形式</span>が使用されます </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">値が<span class="uicontrol">範囲値</span>の最大値(&gt;)より大きい場合は、<span class="uicontrol"> "次よりも大きい"形式</span>が使用されます </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">それ以外の場合は、フィールド値が2つの連続する<span class="uicontrol">範囲値</span> (小さい値以上(&gt;=)、大きい値未満(&lt;))の範囲に含まれる範囲が検出され、<span class="uicontrol">中間形式</span>が使用されます </li> 
    </ul> </p> <p>また、オフの場合は、 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">値が<span class="uicontrol">範囲値</span>内の最小値(&lt;)より小さい場合は、<span class="uicontrol"> "小さい"形式</span>が使用されます </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">値が<span class="uicontrol">範囲値</span>の最大値(&gt;=)以上の場合は、<span class="uicontrol"> "次よりも大きい"形式</span>が使用されます </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">それ以外の場合は、フィールド値が2つの連続する<span class="uicontrol">範囲値</span> (より大きい(&gt;)は小さい(&lt;=)大きい値)の範囲に含まれ、<span class="uicontrol">中間形式</span>が使用されます </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p><span class="uicontrol">範囲の説明を作成</span>がオンで、<span class="uicontrol">範囲フィールド</span>項目が選択されている場合にのみ使用できます。 </p> <p>サンプルの数値を入力し、<span class="uicontrol"> [テスト</span>]ボタンを押して、範囲フィールドの作成方法を確認します。 生成された範囲の説明がウィンドウに表示されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)も参照してください。
1. クリック **[!UICONTROL Add]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 定義済みまたはユーザ定義のmetaタグフィールドの編集{#task_0A7657B63596421BB6DB3ED44F827AB3}

事前定義済みのmetaタグ内の特定のフィールドのみを編集できます。または、ユーザ定義のmetaタグ内のすべてのフィールドを編集できます。

メタタグの変更の効果が顧客に表示される前に、サイトインデックスを作成し直す必要があります。

**定義済みまたはユーザ定義のメタタグフィールドを編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページのテーブルの[!DNL Actions]列で、変更するメタタグフィールド名の行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Pinned Keyword Results Manager]ページの表で、変更するキーワードの行の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Field]ページで、必要なオプションを設定します。

   事前定義済みのmetaタグフィールドに変更を加えることを選択した場合は、編集できないフィールドがあることに注意してください。

   「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ユーザー定義のmetaタグフィールド{#task_9361EF38B5E743038B6672FA6CF70FD3}の削除

不要になった、または使用しなくなったユーザー定義のmetaタグフィールドは削除できます。

事前定義済みのmetaタグフィールドは削除できません。 ただし、特定のフィールドを編集できます。

[定義済みまたはユーザ定義のmetaタグフィールドの編集](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)を参照してください。

削除メタタグの効果が顧客に表示される前に、サイトインデックスを作成し直す必要があります。

**ユーザ定義のメタタグフィールドを削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Definitions]**&#x200B;をクリックします。
1. [!DNL Definitions]ページのテーブルの[!DNL User-defined fields]セクションで、削除するメタタグフィールド名の行の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. 確認ダイアログボックスで、**[!UICONTROL OK]**&#x200B;をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インジェクションについて{#concept_DA091920671948A0A893A26B3A2FAAE5}

[!DNL Injections]を使用すると、ページ自体を編集する必要なく、Webページにコンテンツを挿入できます。

「ターゲット」や「本文」など、インデックスで指定された特定のフィールドにコンテンツを追加したり、インデックスで指定されたコンテンツを新しい値に置き換えたりできます。 例えば、「ターゲット」メタタグフィールドに新しいコンテンツを挿入した場合、この情報は、ページのコンテンツをハードコードした場合と同様に扱われます。 サイトページに対応するコンテンツがあるかどうかに関係なく、あらかじめ定義された任意のmetaタグフィールドのコンテンツを編集できます。 例えば、次の事前定義のメタタグフィールド名のコンテンツを編集できます。

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

## テストフィールドインジェクションの操作{#section_74939EA9E6EA4D2A92E8066B3B11CF92}

[!DNL Staged Injections]ページでは、**[!UICONTROL Test]**&#x200B;をオプションで使用できます。 Webサイトから、テストフィールド名（「タイトル」や「本文」など）、元のフィールド値(「ホームページ」など)、テストURLを入力します。 参照用に結果の値が表示されます。 現在の値は、テスト中に変更されません。

## フィールドインジェクション定義の操作{#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

挿入定義の形式は次のとおりです。

```
append|replace field [regexp] URL value
```

`append|replace`、`field`、`URL`。 および`value`項目は必須です。 1行に1つの射出定義を入力します。 次の例には、6つの異なる挿入定義が含まれています。

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
   <td colname="col2"> <p>「append」を選択して、インジェクション定義(「Adobe:お問い合わせ」または「今すぐ発売！」 上記の例では)を既存のフィールドのコンテンツに追加します。 「置換」を選択して、既存のフィールドの内容を定義された値で上書きします。 フィールドに現在コンテンツが含まれていない場合は、どのオプション（追加または置換）が使用されているかに関係なく、定義された値が自動的に追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field  </span> </p> </td> 
   <td colname="col2"> <p>フィールド名は必須です。 使用できる定義済みのフィールド名は10個です。 </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> キー  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> title </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>各フィールド名は、サイトページの要素に対応しています。 例えば、フィールド名<span class="codeph"> desc </span>を指定した場合、サイトページの説明Metaタグに対応するフィールドに挿入定義値を追加できます。 </p> <p>説明Metaタグがページに存在しない場合、定義済みのコンテンツによってタグが作成されます。 <span class="codeph"> desc </span>インジェクションで指定された内容は、ハードコードされたメタ説明の内容と同じように、結果ページに表示されます。 </p> <p>同じフィールド名を使用して、複数の定義を作成することもできます。 例えば、以下のような注射があるとします。 </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>上記の例のすべてのサイトページに、「Welcome to My Site」という挿入されたタイトルが付きます。 「/会社/」フォルダー内のページに、「My Site:「お問い合わせ」が表示されます。 </p> <p>インジェクションは、「<span class="wintitle">フィールドインジェクション定義</span>」テキストボックスに表示される順に適用されます。 同じ場所にあるページに同じフィールド（この例では「タイトル」）が複数回定義されている場合は、後の定義が優先されます。 </p> <p> <span class="codeph"> [regexp]  </span>  — オプション。<span class="codeph"> regexp </span>オプションを使用する場合、定義されたURLは正規式として扱われます。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>を参照してください。 </p> <p>次の定義では、 </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> 正規式<span class="codeph"> ^に一致するすべてのページの「ターゲット」フィールドに、「重要な情報」が挿入されます。*/products/.*\.html$ </span>. </p> <p>したがって、次のようになります。 </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>次の例では、 </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>挿入により、ファイル名拡張子が「.pdf」で終わるすべてのページの「タイトル」コンテンツに「ミレニアムサイエンス」が追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>URLが必要で、挿入されるドキュメントを指定します。 </p> <p>URLは、次のいずれかです。 </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> フルパス(https://www.mydomain.com/products.htmlなど) </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> 部分パス(https://www.mydomain.com/productsなど) </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> https://www.mydomain.com/*.htmlなど、ワイルドカードを使用するURL </li> 
     </ul> </p> <p>URL値にはスペース文字を含めることはできません。 <span class="codeph"> regexp </span>オプションを使用すると、URLは正規式のように扱われます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>値は必須で、既存のフィールドコンテンツを置き換えたり、既存のフィールドコンテンツに追加したりするために使用します。 同じフィールド名に対して複数の値を指定できます。 次に例を示します。 </p> <p><b>keys</b> https://www.mysite.com/travel/ <b>summer</b>, <b>beach</b>, <b>sand</b>を追加 </p> <p><b>キー</b> https://www.mysite.com/travel/fare/*.html <b>安いチケット</b>を追加 </p> <p>上記の例では、「/travel/」ディレクトリ内のすべてのページの「keys」フィールドに「summer, beach, sand」という語が追加されています。 また、「ceaph tickets」という語は、「/travel/fare/」ディレクトリ内のすべてのページの「keys」フィールドにも追加されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[クロールするコンテンツタイプとインデックスの選択](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)も参照してください。

## フィールドインジェクション定義の追加{#task_E86566FA1FF74CF68115C0ADA05172AE}

[!DNL Injections]を使用すると、ページ自体を編集する必要なく、Webページにコンテンツを挿入できます。

[!DNL Injections]ページでは、**[!UICONTROL Test]**&#x200B;をオプションで使用できます。 Webサイトから、テストフィールド名（「タイトル」や「本文」など）、元のフィールド値(「ホームページ」など)、テストURLを入力します。 参照用に結果の値が表示されます。 現在の値は、テスト中に変更されません。

**フィールドインジェクション定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Injections]**&#x200B;をクリックします。
1. （オプション）[!DNL Injections]ページの[!DNL Test Field Injections]領域で、テストフィールド、テスト元の値、テストURLを入力し、**[!UICONTROL Test]**&#x200B;をクリックします。
1. [!DNL Field Injection Definitions]フィールドに、1行につき1つの射出定義を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダーについて{#concept_9EF38E98811B42CDA41996432B9AD209}

[!DNL Attribute Loader]を使用して、Webサイトからクロールされたデータを拡張する追加の入力ソースを定義します。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

データフィード入力ソースを使用すると、Webサイトで一般的に検出されるものとは異なるフォームに保存されたコンテンツにアクセスできます。 これは、使用可能なクロール方法の1つを使用して行います。 これらのソースのデータは、クロールされたコンテンツからデータに挿入できます。

[!DNL Staged Attribute Loader Definitions]ページに属性ローダー定義を追加した後、Name値とType値以外の設定を変更できます

[!DNL Attribute Loader]ページには次の情報が表示されます。

* 設定および追加した、定義済みのAttribute Loader設定の名前。
* 追加した各コネクタに対して、次のいずれかのデータソースの種類を指定します。

   * **テキスト** ：単純な「フラット」ファイル、カンマ区切り、タブ区切りなどの一貫した区切り形式。
   * **フィード** - XMLフィード

* 構成が次のクロールとインデックスに対して有効かどうか。
* データソースのアドレス。

[テキストとフィードでの属性挿入プロセスの動作も参照してください。](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

[複数の属性ローダの設定について](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)も参照してください。

[属性を追加する際のプレビューの使用についても参照してください…](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## 属性挿入プロセスが属性ローダのテキスト設定とフィード設定に対してどのように機能するか{#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、ファイルのダウンロードは簡単です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p><span class="uicontrol">テキスト</span>の場合、改行で区切られた各テキスト行は、個々のドキュメントに対応し、カンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p><span class="uicontrol">フィード</span>では、各ドキュメントのデータは次の形式の正規式パターンを使用して抽出されます。 </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle"> Attribute Loader </span>ページの<span class="uicontrol"> Map </span>を使用して、データのキャッシュコピーを作成し、クローラのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが入力されます。 </p> <p>解析済みデータがローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラが必要とする単純なHTMLドキュメントが作成されます。 例： </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span>要素は、タイトルメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 同様に、<span class="codeph"> &lt;body&gt; </span>要素は、Bodyメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義されたURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについては、元のドキュメントで見つかったデータを持つ各フィールドに対して、<span class="codeph"> &lt;meta&gt; </span>タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれるドキュメントごとに、次の例のようなリンクも生成されます。 </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングには、プライマリキーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取得される際に使用されるキーを形成します。 </p> <p>クローラはURL <span class="codeph">インデックスを認識します。</span>スキームプレフィックス。これにより、ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p><span class="codeph">インデックス：</span>リンクは、クローラの保留リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、ドキュメントのデータがキャッシュから取得されます。 その後、HTML画像を「アセンブル」し、処理してインデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 複数の属性ローダの設定について{#section_4CC49C74EF294608A184E233F215ADFF}

任意のアカウントに対して、複数のAttribute Loaderの設定を定義できます。

属性ローダを追加する場合、オプションで&#x200B;**[!UICONTROL Setup Maps]**&#x200B;機能を使用して、データソースのサンプルをダウンロードできます。 データの適合性が調べられます。

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
   <td colname="col2"> <p>最初にタブを試し、次に縦棒(<span class="codeph">)を試して区切り値を決定します。 | </span>)を挿入し、最後にカンマ( <span class="codeph"> , </span>)を挿入します。 「<span class="uicontrol">マップの設定</span>」をクリックする前に、既に区切り値を指定している場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なタグとフィールドの値に推測値が入力されます。 さらに、解析済みデータのサンプリングも表示されます。 ファイルにヘッダー行が含まれていることがわかっている場合は、必ず「<span class="uicontrol">先頭行</span>のヘッダー」を選択してください。 この情報は、設定関数で結果のマップエントリを識別しやすくするために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子はMapテーブルのタグ行に表示され、同様の値はFieldsにも表示されます。 これらの行は使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータを説明し、Itemtagを識別するので、この方法が役に立ちます。 </p> <p> <p>注意： セットアップマップ機能は、XMLソース全体をダウンロードして分析を実行します。 ファイルのサイズが大きい場合は、この操作がタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は可能なすべてのXPath項目を識別しますが、その多くは使用が望ましくない項目です。 結果のMap定義を確認し、不要または不要なMap定義を削除してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サイズの大きいXMLデータセットでは、ファイルパーサーがファイル全体をメモリに読み込もうとするので、セットアップマップ機能が動作しない場合があります。 その結果、メモリ不足状態が発生する可能性があります。 ただし、インデックス作成時に同じドキュメントが処理された場合、メモリへの読み込みは行われません。 その代わりに、大きなドキュメントは「外出中」に処理され、最初にメモリに完全に読み込まれるわけではありません。

## 属性ローダ{#section_E9CAB000A94C4D9189786C1EDB1CDB46}を追加する際のプレビューの使用について

Attribute Loaderデータは、Index操作の前に読み込まれます。

属性ローダを追加する際、オプションで&#x200B;**[!UICONTROL Preview]**&#x200B;機能を使用して、データを保存しているかのようにデータを検証できます。 設定をアカウントに保存せずに、設定に対するテストを実行します。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラが使用するメインキャッシュフォルダと競合しません。

プレビューは、**Acct:IndexConnector-プレビュー-Max-ドキュメント**&#x200B;によって制御される5つのドキュメントのデフォルトのみを処理します。 プレビューしたドキュメントは、インデックス作成クローラに表示されるとおり、ソース形式で表示されます。 表示は、Webブラウザーの「表示ソース」機能に似ています。 標準のナビゲーションリンクを使用して、プレビューセット内のドキュメントを移動できます。

プレビューはXML設定をサポートしません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## 属性ローダ定義の追加{#task_A735E5EF763343A9B675E1A3B09AFDBC}

各Attribute Loaderの設定では、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

新しい有効な定義の効果がユーザーに表示される前に、サイトインデックスを作成し直します。

**属性ローダーの定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Stage Attribute Loader Definitions]ページで、**[!UICONTROL Add New Attribute Loader]**&#x200B;をクリックします。
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
      <td colname="col2"> <p>属性ローダー設定の一意の名前。 英数字を使用できます。 「_」と「 — 」も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択するデータソースタイプは、<span class="wintitle">属性ローダー追加</span>ページで使用できる結果のオプションに影響します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行で区切られた各行のテキストは、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）を、1から始まる列番号で参照されるメタデータフィールドにマップできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むプライマリXMLドキュメントをダウンロードします。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>使用する設定を「オン」にします。 または、設定を「オフ」にして、使用しない場合には回避できます。 </p> <p> <b>注意</b>:無効な属性ローダーの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドに対する適切なエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスすることができます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTP、またはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で設定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、またはHTTPS接続の最大再試行数を指定します。 この値は0 ～ 10の範囲で設定する必要があります。 </p> <p>値が0の場合は、再試行を禁止します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの各フィールドの説明文字として使用する文字を指定します。 </p> <p>カンマ文字(<span class="codeph">、</span>)は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るのに役立つフィールド区切り文字として機能します。 </p> <p><span class="uicontrol">タブを選択しますか？ </span> をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭行のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日数 </p> </td> 
      <td colname="col2"> <p>属性ローダーのデータをダウンロードする間隔の最小値を設定します。 ダウンロード更新頻度の間隔で発生するインデックストリガーダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内に属性ローダーのデータが複数回ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1にして、列番号を指定します。 各列に新しいマップ行を追加するには、<span class="wintitle">アクション</span>の下の<span class="uicontrol"> + </span>をクリックします。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップすることもできます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>が、現在のアカウントに対して定義済みのメタデータフィールドを選択できるドロップダウンリストになります。 </p> <p>必要に応じて、<span class="uicontrol">フィールド</span>の値は、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、<span class="wintitle">フィルタースクリプト</span>で使用されるコンテンツの作成に役立つ場合があります。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプトについて</a>を参照してください。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>主キーとして識別されるフィールドは1つだけです。 このフィールドは、Attribute Loaderデータとインデックス内の対応するドキュメントとを一致させる「外部キー」として使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：フィード</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>使用する設定を「オン」にします。 または、設定を「オフ」にして、使用しない場合には回避できます。 </p> <p> <b>注意</b>:無効な属性ローダーの設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p> または </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドに対する適切なエントリに分類されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>複数の「行」情報を含むプライマリXMLドキュメントへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスすることができます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> ファイル </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、AdobeXMLドキュメントの次のフィードフラグメントでは、Itemtagの値は<span class="codeph">レコード</span>です。 </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>メタデータフィールドを指定します。この値は、アトリビュートローダ設定のデータの「キー」として参照されます。 値が選択されない場合(<b>—None—</b>)、この設定のデータは、ランキングの計算（<b>ルール</b> &gt; <b>ランキングルール</b> &gt; <b>ルールの編集</b>）で使用できません。 値を選択すると、このフィールドの値を使用して、サイト検索/マーチャンダイジングドキュメントとこの設定のデータとの相互参照が行われます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>古い日数 </p> </td> 
      <td colname="col2"> <p>属性ローダーのデータをダウンロードする間隔の最小値を設定します。 ダウンロード更新頻度の間隔で発生するインデックストリガーダウンロードは無視されます。 この値をデフォルトの1に設定した場合、24時間以内に属性ローダーのデータが複数回ダウンロードされることはありません。 ダウンロード更新頻度の間隔内に発生するすべての検索インデックスは、最後にダウンロードされたデータセットを使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータとのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析済みXMLデータのXPath表現を指定します。 上記のAdobeXMLドキュメントの例を使用して、Itemtagオプションの下で、次の構文を使用してマッピングできます。 </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>に対応付けられます。 </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内に含まれる）。<span class="codeph">タイトル</span>は、メタデータフィールド<span class="codeph">タイトル&lt;a11に対応します/&gt;。</span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内）（name属性は<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph"> desc1に対応します/&gt;。</span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">レコード</span>要素内の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本体&lt;a11にマッピングされます。/&gt;。<span class="codeph"></span></span> </p> </li> 
        </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a>を参照 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各<span class="codeph"> &lt;meta&gt; </span>タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>が、現在のアカウントに対して定義済みのメタデータフィールドを選択できるドロップダウンリストになります。 </p> <p>必要に応じて、<span class="uicontrol">フィールド</span>の値は、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、<span class="wintitle">フィルタースクリプト</span>で使用されるコンテンツの作成に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプトについて</a>を参照してください。 </p> <p>Attribute Loaderが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結され、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>主キーとして識別されるフィールドは1つだけです。 このフィールドは、Attribute Loaderデータとインデックス内の対応するドキュメントとを一致させる「外部キー」として使用されます。 </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）**[!UICONTROL Setup Maps]**&#x200B;をクリックして、データソースのサンプルをダウンロードします。 データの適合性が調べられます。
1. **[!UICONTROL Add]**&#x200B;をクリックして、設定を[!DNL Attribute Loader Definitions]ページに追加します。
1. [!DNL Attribute Loader Definitions]ページで、**[!UICONTROL rebuild your staged site index]**&#x200B;をクリックします。
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義の編集{#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

定義済みの既存のアトリビュートローダを編集できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

[!DNL Type]ドロップダウンリストのAttribute Loader NameやTypeなど、一部のAttribute Loaderオプションを変更できるわけではありません。

**アトリビュートローダの定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を変更するAttribute Loader定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Edit]ページで、必要なオプションを設定します。

   「[属性ローダー定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、**[!UICONTROL rebuild your staged site index]**&#x200B;をクリックします。
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義のコピー{#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

既存のアトリビュートローダ定義をコピーして、作成する新しいアトリビュートローダの基本として使用できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

アトリビュートローダの定義をコピーする場合、コピーされた定義はデフォルトで無効になります。 定義を有効または「有効にする」には、[!DNL Attribute Loader Edit]ページで定義を編集し、**[!UICONTROL Enable]**&#x200B;を選択する必要があります。

「[属性ローダ定義の編集](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)」を参照してください。

**属性ローダーの定義をコピーするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を重複するAttribute Loaderの定義名&#x200B;**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Copy]ページで、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダ定義の名前の変更{#task_58D5DFD7EBC04111BCB91118E4440DB4}

既存のアトリビュートローダ定義の名前を変更できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

**アトリビュートローダ定義の名前を変更するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、変更する属性ローダ定義名の&#x200B;**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Rename]ページの[!DNL Name]フィールドに、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Rename]**.
1. （オプション）[!DNL Attribute Loader Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 属性ローダーデータの読み込み{#task_2F3C55189B0A4049AB2113F2291CC181}

設定したAttribute Loaderデータをサイトの検索/マーチャンダイジングにダウンロードできます。

[!DNL Data Load]ページには、最後に実行したAttribute Loaderのデータ読み込み操作のステータスに関する次の情報が表示されます。

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
   <td colname="col1"> <p>開始時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ読み込み操作が開始された日時を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>停止時間 </p> </td> 
   <td colname="col2"> <p>最後のデータ・ロード操作の完了日時を表示します。 または、現在のデータ読み込み操作がまだ進行中であることを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**属性ローダのデータを読み込むには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページで、**[!UICONTROL Load Attribute Loader Data]**&#x200B;をクリックします。
1. **[!UICONTROL Attribute Loader Data Load]**&#x200B;ページで、次のいずれかの操作を行います。

   * **[!UICONTROL Start Load]**&#x200B;をクリックして、読み込み操作を開始します。

      データのロード操作中に、**Progress**&#x200B;行に進行状況に関する情報が表示されます。

   * **[!UICONTROL Stop Load]**&#x200B;をクリックして、読み込み操作を停止します。

1. **[!UICONTROL Close]**&#x200B;をクリックして[!DNL Attribute Loader Definitions]ページに戻ります。

## 属性ローダのデータのプレビュー{#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

プレビューを使用して、最も最近ロードされたアトリビュートローダのデータを表示できます。

表の行列には、データの各行の番号が表示され、アトリビュートローダーの値が読み込まれた元の順序が示されます。

残りの列には、各エントリに関連付けられた値が表示されます。

テーブルが空の場合は、アトリビュートローダのデータがまだロードされていないことを意味します。 [!DNL Attribute Loader Data Preview]ページを閉じてから、アトリビュートローダのデータを読み込むことができます。

[属性ローダーデータの読み込み](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

**プレビュー属性ローダーのデータを作成するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページの[!DNL Actions]列の下で、ダウンロードしたデータを表示する設定の&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Data Preview]ページで、ページの上部と下部にあるナビゲーションと表示のオプションを使用して、データを表示します。

   表の列見出しをクリックして、昇順または降順でデータを並べ替えます。
1. 次のいずれかの操作を行います。

   * **[!UICONTROL Download to Desktop]**&#x200B;をクリックして、テーブルを.xltファイルとしてダウンロードし、保存します。
   * アトリビュートローダーデータのプレビューが終了し、前に表示したページに戻ったら、ページを閉じます。

## 属性ローダ定義の設定の表示{#task_EA99A9694FE948ADA82C1DBA0667851B}

既存のアトリビュートローダ定義の設定を確認できます。

[!DNL Attribute Loader Definitions]ページに属性ローダの定義を追加した後は、そのタイプの設定を変更できません。 代わりに、定義を削除してから、新しい定義を追加する必要があります。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

**アトリビュートローダ定義の設定を表示するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader]ページの[!DNL Actions]列見出しの下で、設定を確認または編集するAttribute Loader定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

## 最新の属性ローダー・データ・ロード{#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}からログを表示

[!DNL View Log]を使用して、最新のダウンロードプロセスのAttribute Loaderデータログファイルを調べることができます。 ログ表示を使用して、実行中のダウンロードを監視することもできます。

[属性ローダーデータの読み込み](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)を参照してください。

**最新のアトリビュートローダーのデータ読み込みからログを表示するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページで、**[!UICONTROL View Log]**&#x200B;をクリックします。 ログページ、
1. [!DNL Attribute Loader Data Log]ページで、ページの上部と下部にあるナビゲーションと表示のオプションを使用して、ログ情報を表示します。
1. 終了したら、ページを閉じて[!DNL Attribute Loader Definitions]ページに戻ります。

## 属性ローダ定義の削除{#task_E8980F66888B476E98C228C1D307EDF8}

不要になった、または使用しなくなった既存のアトリビュートローダ定義を削除できます。

>[!NOTE]
>
>Attribute Loaderを使用するには、Adobeアカウント担当者またはAdobeサポートがアカウントでAttribute Loaderを有効にする必要がある場合があります。

**アトリビュートローダ定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Attribute Loader]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Definitions]ページの[!DNL Actions]列見出しの下で、削除するAttribute Loader定義名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Attribute Loader Delete]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
