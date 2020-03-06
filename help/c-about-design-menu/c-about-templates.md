---
description: テンプレートを使用して、プレゼンテーションテンプレートと転送テンプレートを管理できます。
seo-description: テンプレートを使用して、プレゼンテーションテンプレートと転送テンプレートを管理できます。
seo-title: テンプレートについて
solution: Target
title: テンプレートについて
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0

---


# テンプレートについて{#about-templates}

を使用して、プレゼンテーシ **[!UICONTROL Templates]** ョンテンプレートと転送テンプレートを管理できます。

## テンプレートについて {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

プレゼンテーションテンプレートとトランスポートテンプレートを追加、編集、コピー、名前の変更または削除できます。 「テンプレート」(Templates)テーブル内の既存のテンプレート名をクリックすると、エディタ（またはビューア）ウィンドウで開き、変更を加えることができます。

テンプレートに対して行った変更は、「テンプレート」(Templates)テーブルのテンプレート名のドロップダウンリストから、「ヒストリー」(History)機能を使用して元に戻すことができます。

テンプレートテーブル内のテンプレートの対応するチェックボックスをオンにすることで、プレゼンテーションテンプレートのペ **[!UICONTROL Minimize]** ージの重みを軽減することができます。 テンプレートのページの重みを減らすことで、インラインのJavaScriptとCSSを動的に最小限に抑えることができます。 また、HTML内の重複した空白を削除します。 プレゼンテーションテンプレートのページの重みを最小限に抑えると、検索結果をより迅速に配信できます。

最小化したテンプレートの外観をプレビューするには、ファイル名の横のドロップダウンリストをクリックし、をクリックしま **[!UICONTROL Preview minimized]**&#x200B;す。 メインのプレゼンテーションテンプレートを最小限に抑える場合は、（タグに付属の）テンプレートを最小限に抑えることを忘れないでください。このオプションは継承でき `guided-include` ないためです。

プレゼンテーションテンプレートを最小化しても、同じテンプレートの「最小化されていない」バージョンを編集できます。

検索前のルール、検索後のルール、ビジネスルールを使用して、他のプレゼンテーションテンプレートの1つを使用するタイミングを決定できます。 「検索ごとに、対象のテンプレートをxxxxに設定する」などのルールを持つのが一般的です。 このようなルールを適用した状態で、「テンプレート」(Templates)テーブルの「デフォルト」(Default)テンプレートを変更しても、何の影響も与えないように見えます。

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## プレゼンテーションテンプレートについて {#section_ACDDEA5C499E481C828A517C230D4596}

プレゼンテーションテンプレートは、顧客がWebサイトで検索結果を表示する際に表示されるHTMLテンプレートです。

プレゼンテーションレイヤーには、さまざまなソースからの複数の検索結果を表示する単一のプレゼンテーションテンプレートを用意できます。 必要な数のプレゼンテーションテンプレートを定義したり、他のテンプレートが共有するプレゼンテーションテンプレートをコマンドを使用して定義することも `include` できます。 プレゼンテーションテンプレートは、ファセット、メニュー、パンくずリストなど、すべてのデザインコンポーネントを組み合わせる場所です。 様々なデザインコンポーネントを表示するには、プレゼンテーションテンプレートタグを使用する必要があります。

「プレゼンテーシ [ョンテンプレートタグ」を参照してください。](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

複数のプレゼンテーションテンプレートがある場合は、使用する各種プレゼンテーションテンプレートを、どの条件で定義します。 受信するCGIパラメーターとcookieに基づいて、使用するプレゼンテーションテンプレートを選択できます。 また、以前の検索の結果に基づいて、使用しているプレゼンテーションテンプレートを切り替えることもできます。

複数のプレゼンテーションテンプレートを使用する場合は、検索結果を最初に表示するテンプレートを必ず指定してください。 これは、テンプレートテーブルの **[!UICONTROL Default]** 列を使用して行います。

## 転送テンプレートについて {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

トランスポートテンプレートは、バックエンド検索からガイド付き検索プレゼンテーションレイヤーにデータを渡すXMLまたはJSONテンプレートのいずれかです。

デフォルトでは、アカウントはXMLトランスポートテンプレートを使用するように設定されています。 ただし、JSONを使用してガイド付き検索にデータを渡す場合は、アドビのコンサルティング担当者にお問い合わせください。

プレゼンテーションレイヤーには、複数の検索結果を表示する単一のプレゼンテーションテンプレートを含めることができます。 各検索では、同じトランスポートテンプレートまたはカスタムトランスポートテンプレートを使用して、プレゼンテーションレイヤーにデータを渡すことができます。 トランスポートテンプレートは、プレゼンテーションレイヤーにデータを渡す目的でのみ使用されるので、検索結果の表示に使用するHTMLを持つことはできません。 テンプレートは、トランスポートテンプレートタグを使用して、検索の結果とファセットの入力の結果を渡します。 これらのタグ内では、標準の検索テンプレートタグを使用して実際の値が表示されます。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

**XML Transport Template固有のタグ**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>XMLトランスポートテンプレートタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらは、プレゼンテーションレイヤーがトランスポートテンプレートから何を解析する必要があるかを検出するために使用するルートXMLタグです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、結果セットに基づいて概要データを提供する検索テンプレートタグを囲みます。 通常、これらのタグには、結果の合計数、最小結果、最大結果を示す検索タグが含まれます。 汎用フィールドタグを使用して、任意の数の追加のグローバルフィール <span class="codeph"> ドを定義で </span> きます。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;結果&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは検索結果に含まれるので、ガイド付き検索では検索場所がわかります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;結果&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは各検索結果に含まれるので、1つの検索結果のコンテンツの開始と終了をガイド付き検索で認識できます。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグを使用すると、複数値のリストにある各項目をループ処理して1つの結果を得ることができます。 結果内でのみタグを使用します。 その主な目的は、結果フィールドに属する属性を繰り返し処理できるようにすることです。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;ファセット&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのセットは、ファセットを設定する結果を渡します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>各ファセットには、nameパラメーターがファセット名と一致する独自のファセットタグが必要です。 検索タグは、ファセット値のファセットタグ内で使用されます。 </p> <p>ファセットにつ <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;サーチクエリ&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、ガイド付き検索でどのXMLノードに提案が含まれているかを認識できるように、「Did You Mean」の提案をラップします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;提案&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、「Did You Mean」の提案ごとに含まれます。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**JSONトランスポートテンプレート固有のタグ**

JSONとXMLを検索エンジンから渡す方が、ペイロードが小さく、パーサーが高速なので、より高速に処理できます。 ただし、JSONを使用して出力内容が厳密なJSONであることを確認する場合は、パーサーが許可しないので注意が必要です。

JSONを初めて使用する場合は、次のリンクと例を使用して作業を開始できます。

* JSONの紹介。 https://www.json.org/を参照し [てください](https://www.json.org/)。
* JSONをテストして、有効であることを確認します。 https://jsonlint.com/を参照し [てください](https://jsonlint.com/)。

**JSONテンプレートの例**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**結果の属性テーブルを含むJSON結果セクションの例**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**関連するフィールドを含むファセットのJSONファセットセクションの例**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**スロットファセット用のJSONファセットセクションの例**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## 新しいプレゼンテーションまたは転送テンプレートファイルの追加 {#task_73199757B6E748CAA604902FF913F012}

を使用して、ペ **[!UICONTROL Add Template]** ージにプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を追加で [!DNL Templates] きます。

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**新しいプレゼンテーションまたは転送テンプレートファイルを追加するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ上で、 [!DNL Templates] をクリックしま **[!UICONTROL Add New Template]**&#x200B;す。
1. ダイアログ [!DNL Add Template] ボックスで、必要なオプションを設定します。

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | オプション | 説明 |
   |--- |--- |
   | 新しいファイル名 | 追加するテンプレートの名前を指定します。 選択したテンプレートタイプに基づいて、ファイル名に適切なファイル拡張子が自動的に追加されます。  プレゼンテーションテンプレートには.tmplファイル拡張子が付きます。トランスポートテンプレートには.tplファイル拡張子が付いています。 |
   | 新しいテンプレートタイプ | 追加するプレゼンテーションまたは転送テンプレートを選択できます。  テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md)い。 |

   プレゼンテーショ [ンまたは転送テンプレートの編集も参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。
1. クリック **[!UICONTROL Add]**.
1. （オプション）ページ [!DNL Templates] で、次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## プレゼンテーションまたは転送テンプレートの編集 {#task_800E0E2265C34C028C92FEB5A1243EC3}

テンプレートエディターを使用して、プレゼンテーションの内容を表示および編集し、テンプレートファイルを転送することができます。

<!-- 

t_editing_a_template.xml

 -->

Webサイトの訪問者が引き続きテンプレートのライブバージョンを使用している間、ステージングされたプレゼンテーションやトランスポートテンプレートを編集およびテストできます。 ステージングされたテンプレートは、検索ドメインのURLのステージバージョンを使用してテストします。 例えば、ステージングされたトランスポートテンプレートをテストするには、トランスポートテンプレートの名前に設定されたステ `sp_staged=1``sp_t` ージングされたクエリ()を実行します。 レイアウトの表示方法に満足したら、テンプレートエディター内からテ **[!UICONTROL Push Live]** ンプレートを使用してライブにすることができます。 テンプレートがライブになると、サイトの訪問者はテンプレートを使用し始めます。

プレゼンテーションテンプレートタグ参照を使用して、ファセット、パンくずリスト、メニューなどのガイド付き検索コンポーネントにプレゼンテーションテンプレートを接続する方法を学びます。

「プレゼンテーシ [ョンテンプレートタグ」を参照してください。](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

トランスポートテンプレートで使用するタグの詳細については、トランスポートテンプレートタグ参照を参照してください。

トランスポートテ [ンプレートタグを参照してください。](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ上で、プ [!DNL Templates] レゼンテーションまたはトランスポートテンプレートのファイル名をクリックします。
1. ページ [!DNL Template Editor] で、タグとコーディングを変更します。

   で行う変更には注意が必要です [!DNL Template Editor]。元に戻す機能はありません。 不要な変更を行い、前のバージョンのファイルに戻る場合は、をクリックしてテンプレートの表に戻ります（その時点まで変更を保存しなかった場合）。 **[!UICONTROL Cancel]** 変更を保存済みの場合は、エディターを使用し **[!UICONTROL History]** て変更を元に戻すことができます。
1. （オプション）をクリ **[!UICONTROL Insert Symbol]** ックして、米国英語キーボードに対応するキーを持たない特殊文字や記号を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

1. 完了したら、テンプレートエディターページを閉じます。テンプレートページに戻ります。

## プレゼンテーションまたは転送テンプレートファイルのコピー {#task_B744AB3384C84DD59C33CD25E18C2C90}

を使用すると、既 **[!UICONTROL Copy Template]** 存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を複製して、テンプレートページに追加することで、時間を節約できます。

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

テンプレート名、テンプレートタイプ、またはその両方を変更する必要があります。 変更を行わない場合、テンプレートはコピーされません。

テンプレートをコピーするには、既にテンプレートを追加しておく必要があります。

詳しくは、新 [しいプレゼンテーションまたは転送テンプレートファイルの追加を参照してくださ](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)い。

**プレゼンテーションまたは転送テンプレートファイルをコピーするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ [!DNL Templates] 上で、コピーするテンプレート名の横のドロップダウンリストで、をクリックしま **[!UICONTROL Copy]**&#x200B;す。
1. ダイアログ [!DNL Copy Template] ボックスで、必要な1つ以上のオプションを設定します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## プレゼンテーションまたは転送テンプレートファイルの名前の変更 {#task_CC30050FC2DE4898BF44379D8378EB31}

を使用して、既 [!DNL Rename Template] 存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)の名前を変更できます。

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

また、必要に応じて、テンプレートのタイプを変更することもできます。

テンプレートの名前を変更するには、既にテンプレートを追加しておく必要があります。

詳しくは、新 [しいプレゼンテーションまたは転送テンプレートファイルの追加を参照してくださ](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)い。

**プレゼンテーションまたは転送テンプレートファイルの名前を変更するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ [!DNL Templates] の、名前を変更するテンプレート名の横のドロップダウンリストで、をクリックしま **[!UICONTROL Rename]**&#x200B;す。
1. ダイアログ [!DNL Rename Template] ボックスで、必要な1つ以上のオプションを設定します。
1. クリック **[!UICONTROL Rename]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## プレゼンテーションまたは転送テンプレートファイルの削除 {#task_67E532C2B83A449687737E3B06C5AA58}

を使用して、既 **[!UICONTROL Delete Template]** 存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を削除できます。

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

ライブにプッシュされたステージテンプレートの対応するバージョンが既に存在する場合があります。 削除したテンプレートが存在する場合は、を使用して削除したテンプレートをライブ **[!UICONTROL Staging]** にプッシュし、ライブ環境からも削除されるようにしてください。 または、テンプレートペ **[!UICONTROL Push Live]** ージでを使用できます。

ステージングに [ついてを参照してください](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

詳しくは、ステ [ージ設定のライブプッシュを参照してください。](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

テンプレートを削除するには、既にテンプレートを追加しておく必要があります。

詳しくは、新し [いプレゼンテーションまたは転送テンプレートファイルの追加を参照してください。](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**プレゼンテーションまたは転送テンプレートファイルを削除するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ [!DNL Templates] 上で、削除するテンプレート名の横のドロップダウンリストで、をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. ダイアログボッ [!DNL Delete Template] クスで、「 **[!UICONTROL Delete.]**
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 最小化したプレゼンテーションテンプレートのプレビュー {#task_1757B6207CC74221AE4BFFE5674D320B}

を使用して、最 **[!UICONTROL Preview minimized]** 小限に抑えることを選択した場合に、プレゼンテーションテンプレートのページの重さがどのように減少するかを確認できます。

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

メインのプレゼンテーションテンプレートを最小限に抑える場合は、（ガイド付きのタグ付きで）テンプレートを含める場合は、このオプションは継承できないので、テンプレートの最小化を必ず有効にしてください。

詳しく [は、プレゼンテーションテンプレートのページ重みを減らすを参照してください。](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

テンプレートを最小化してプレビューするには、既にテンプレートを追加しておく必要があります。

詳しくは、新し [いプレゼンテーションまたは転送テンプレートファイルの追加を参照してください。](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

トランスポートテンプレートファイルのXMLコードをプレビューできます。

詳しくは、ト [ランスポートテンプレートファイルのXMLのプレビューを参照してください。](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**最小化したプレゼンテーションテンプレートをプレビューするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページの [!DNL Templates] プレゼンテーションテンプレート名の横のドロップダウンリストで、をクリックしま **[!UICONTROL Preview minimized]**&#x200B;す。

   テンプレートテ **[!UICONTROL Type]** ーブルの列を使用して、テンプレートをプレゼンテーションとトランスポートで並べ替えます。
1. （オプション）ページ上で、 [!DNL Preview Minimized Template] 定義されたウ **[!UICONTROL Wrap lines]** ィンドウ内のタグを読み取ります。
1. クリック **[!UICONTROL Close]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Webサイト上のプレゼンテーションテンプレートのページ重みの軽減 {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

テンプレートテーブルのオプションを使用すると、プレゼンテーションテンプレートのペ **[!UICONTROL Minimize]** ージの重みを軽減できます。

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

テンプレートのページの重みを減らすことで、インラインのJavaScriptとCSSを動的に最小限に抑えることができます。 また、HTML内の重複した空白を削除します。 プレゼンテーションテンプレートのページの重みを最小限に抑えると、検索結果をより迅速に配信できます。

また、を使用して、最小化したプレゼンテーションテンプレートの外観をプレビューすることもできま **[!UICONTROL Preview minimized]**&#x200B;す。

詳しくは、最 [小化したプレゼンテーションテンプレートのプレビューを参照してくだ](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)さい。

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページの [!DNL Templates] 列の下で、Webサイ [!DNL Minimize] ト上で最小限に抑えて表示する1つ以上のプレゼンテーションテンプレートファイルのチェックボックスをオンにします。

   表の列を使 **[!UICONTROL Type]** 用して、テ [!DNL Templates] ンプレートをプレゼンテーションと転送で並べ替えます。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Webサイトで使用するデフォルトのプレゼンテーションテンプレートファイルの設定 {#task_C1E8CE817E4D43E096167A347C54DD53}

複数のプレゼンテーションテンプレートがある場合、検索結果の表示に最初に使用するテンプレートを指定できます。

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

検索前のルール、検索後のルールおよびビジネスルールを使用して、他のプレゼンテーションテンプレートの1つを使用するタイミングを決定できます。

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

「検索ごとに、対象のプレゼンテーションテンプレートをxxxxに設定する」などのルールを設定するのは一般的です。 このようなルールを適用した状態で、テンプレートページの「デフォルト」テンプレートを変更しても効果がないように見えます。

**[!UICONTROL To set the default presentation template file to use on your website]**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページの [!DNL Templates] 列の下で、デフ [!DNL Default] ォルトとして使用する対応するプレゼンテーションテンプレートファイルのラジオボタンをクリックします。

   表の列を使 **[!UICONTROL Type]** 用して、テ [!DNL Templates] ンプレートをプレゼンテーションと転送で並べ替えます。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## トランスポートテンプレートファイルのXMLのプレビュー {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

を使用して、追 [!DNL Preview] 加したトランスポートテンプレートのXMLを確認できます。

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

テンプレートのXMLをプレビューするには、既にトランスポートテンプレートを追加しておく必要があります。

詳しくは、新 [しいプレゼンテーションまたは転送テンプレートファイルの追加を参照してくださ](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)い。

最小化したプレゼンテーションテンプレートファイルをプレビューして、ページの重さを軽減できます。

詳しくは、最 [小化したプレゼンテーションテンプレートのプレビューを参照してくだ](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)さい。

**トランスポートテンプレートファイルのXMLをプレビューするには**

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページで、 [!DNL Templates] トランスポートテンプレート名の横のドロップダウンリストで、をクリックしま **[!UICONTROL Preview]**&#x200B;す。

   表の列を使 **[!UICONTROL Type]** 用して、テ [!DNL Templates] ンプレートをプレゼンテーションと転送で並べ替えます。
1. 表示ウィンドウを閉じ、に戻りま [!DNL site search/merchandising]す。
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

