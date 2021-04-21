---
description: テンプレートを使用して、プレゼンテーションテンプレートと転送テンプレートを管理できます。
solution: Target
title: テンプレートについて
topic-legacy: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
exl-id: 846f34b3-9857-494e-9010-3db0b48412d3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '2647'
ht-degree: 1%

---

# テンプレートについて{#about-templates}

**[!UICONTROL Templates]**&#x200B;を使用して、プレゼンテーションテンプレートと転送テンプレートを管理できます。

## テンプレートについて{#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

プレゼンテーションテンプレートとトランスポートテンプレートは、追加、編集、コピー、名前の変更または削除が可能です。 「テンプレート」(Templates)テーブル内の既存のテンプレート名をクリックすると、そのテンプレートがエディタ（またはビューア）ウィンドウに開き、変更を加えることができます。

「テンプレート」(Templates)テーブルのテンプレート名のドロップダウンリストから、「ヒストリー」(History)機能を使用してテンプレートに加えた変更は、すべて元に戻すことができます。

テンプレートテーブル内のテンプレートに対応する&#x200B;**[!UICONTROL Minimize]**&#x200B;チェックボックスをオンにすると、プレゼンテーションテンプレートのページ重み付けを減らすことができます。 テンプレートのページ重み付けを減らすことで、インラインのJavaScriptとCSSを動的に最小化できます。 また、HTML内の重複した空白を削除します。 プレゼンテーションテンプレートのページ重み付けを最小化すると、検索結果をより迅速に配信するのに役立ちます。

ファイル名の横のドロップダウンリストをクリックし、**[!UICONTROL Preview minimized]**&#x200B;をクリックすると、最小化したテンプレートの外観をプレビューできます。 メインのプレゼンテーションテンプレートを最小限に抑える場合は、（`guided-include`タグと共に）含めるテンプレートの最小化を必ず有効にしてください。このオプションは継承できないからです。

プレゼンテーションテンプレートを最小化しても、同じテンプレートの「最小化解除」バージョンを編集できます。

検索前のルール、検索後のルールおよびビジネスルールを使用して、他のプレゼンテーションテンプレートのどちらかを使用するタイミングを決定できます。 「検索ごとに、ターゲットテンプレートをxxxxに設定」などのルールを設定するのは一般的です。 このようなルールを適用した場合、テンプレートテーブルで「デフォルト」テンプレートを変更しても効果がないように見えます。

[Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)についてを参照してください。

[検索後のルールについて](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)を参照してください。

[ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

## プレゼンテーションテンプレートについて{#section_ACDDEA5C499E481C828A517C230D4596}

プレゼンテーションテンプレートは、顧客がWebサイト上で検索結果を表示する際に表示するHTMLテンプレートです。

プレゼンテーションレイヤーには、様々なソースからの複数の検索結果を表示する、単一のプレゼンテーションテンプレートを用意することができます。 プレゼンテーションテンプレートは必要な数だけ定義でき、`include`コマンドを使用して、他のテンプレートが共有するプレゼンテーションテンプレートも定義できます。 プレゼンテーションテンプレートは、ファセット、メニュー、パンくずリストなど、すべてのデザインコンポーネントを組み合わせる場所です。 様々なデザインコンポーネントを表示するには、プレゼンテーションテンプレートタグを使用する必要があります。

[プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)を参照

複数のプレゼンテーションテンプレートがある場合は、使用する各種プレゼンテーションテンプレートを、どの条件で定義します。 受信するCGIパラメーターとCookieに基づいて、使用するプレゼンテーションテンプレートを選択できます。 また、以前の検索の結果に基づいて、使用しているプレゼンテーションテンプレートを切り替えることもできます。

複数のプレゼンテーションテンプレートを使用する場合は、検索結果を最初に表示するテンプレートを指定してください。 これは、Templatesテーブルの&#x200B;**[!UICONTROL Default]**&#x200B;列を使用して行うことができます。

## トランスポートテンプレートについて{#section_35FD3E8AAA4E4695A737DB7E00C3258B}

トランスポートテンプレートは、バックエンド検索からGuided Searchプレゼンテーションレイヤーにデータを渡すXMLまたはJSONテンプレートにすることができます。

デフォルトでは、アカウントはXMLトランスポートテンプレートを使用するように設定されています。 ただし、JSONを使用してガイド付き検索にデータを渡す場合は、Adobeコンサルティングにお問い合わせください。

プレゼンテーションレイヤーには、複数の検索結果を表示する単一のプレゼンテーションテンプレートを用意することができます。 各検索では、同じトランスポートテンプレートまたはカスタムトランスポートテンプレートを使用して、プレゼンテーションレイヤーにデータを渡すことができます。 トランスポートテンプレートはプレゼンテーションレイヤーにデータを渡す目的でのみ使用されるので、検索結果の表示に使用するHTMLを持つことはできません。 テンプレートは、トランスポートテンプレートタグを使用して検索の結果とファセットに入力する結果を渡します。 これらのタグ内では、標準の検索テンプレートタグを使用して実際の値が表示されます。

[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

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
   <td colname="col2"> <p>これらは、プレゼンテーションレイヤーがトランスポートテンプレートから解析する必要のある内容を検出するために使用するルートXMLタグです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、結果セットに基づく概要データを提供する検索テンプレートタグを囲みます。 通常、これらのタグには、結果の合計数、最小の結果、最大の結果の検索タグが含まれます。 <span class="codeph"> general-field </span>タグを使用して、任意の数の追加のグローバルフィールドを定義できます。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは検索結果に含まれるので、ガイド付き検索では検索場所がわかります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは各検索結果に含まれるので、ガイド付き検索は1つの検索結果開始のコンテンツのどこを認識し、その終わりを識別します。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
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
   <td colname="col2"> <p>このタグを使用すると、複数値のリストで各項目をループ処理して1つの結果を得ることができます。 タグは結果内でのみ使用します。 主な目的は、結果フィールドに属する属性を繰り返し実行できるようにすることです。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのセットは、ファセットを設定する結果を渡します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>名前パラメーターがファセット名と一致するファセットには、それぞれ独自のファセットタグが必要です。 検索タグは、ファセット値のファセットタグ内で使用されます。 </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local">ファセットについて</a>を参照してください。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、「Did You Mean」の提案をラップするので、ガイド付き検索では、提案が含まれるXMLノードが認識されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグは、各「Did You Mean」サーチクエリをラップします。 </p> <p> <b>例</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
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

JSONとXMLを検索エンジンから渡す方が、ペイロードが小さく、パーサーが高速なので、処理が高速であることがわかっています。 ただし、JSONを使用して出力内容が厳密なJSONであることを確認する場合は、パーサーが許可しないので注意が必要です。

JSONを初めて使用する場合は、次のリンクと例を使用して作業を開始できます。

* JSONの紹介。 [https://www.json.org/](https://www.json.org/)を参照してください。
* JSONをテストして、有効であることを確認します。 [https://jsonlint.com/](https://jsonlint.com/)を参照してください。

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

**結果属性テーブルを含むJSON結果セクションの例**

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

**関連付けられたフィールドを持つファセットのJSONファセットセクションの例**

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

**スロットファセットのJSONファセットセクションの例**

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

## 新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加{#task_73199757B6E748CAA604902FF913F012}

**[!UICONTROL Add Template]**&#x200B;を使用して、プレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を[!DNL Templates]ページに追加できます。

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**新しいプレゼンテーションまたはトランスポートテンプレートファイルを追加するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページで、**[!UICONTROL Add New Template]**&#x200B;をクリックします。
1. [!DNL Add Template]ダイアログボックスで、必要なオプションを設定します。

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | オプション | 説明 |
   |--- |--- |
   | 新しいファイル名 | 追加するテンプレートの名前を指定します。 選択したテンプレートタイプに基づいて、適切なファイル拡張子がファイル名に自動的に追加されます。  プレゼンテーションテンプレートには.tmplファイル拡張子が付きます。トランスポートテンプレートのファイル拡張子は.tplです。 |
   | 新しいテンプレートタイプ | 追加するプレゼンテーションまたはトランスポートテンプレートを選択できます。  [テンプレートについて](../c-about-design-menu/c-about-templates.md)を参照してください。 |

   「[プレゼンテーションまたはトランスポートテンプレートの編集](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)」も参照してください。
1. クリック **[!UICONTROL Add]**.
1. （オプション）[!DNL Templates]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## プレゼンテーションまたはトランスポートテンプレートの編集{#task_800E0E2265C34C028C92FEB5A1243EC3}

テンプレートエディターを使用して、プレゼンテーションの内容を表示および編集し、テンプレートファイルを転送することができます。

<!-- 

t_editing_a_template.xml

 -->

Webサイトの訪問者が引き続きテンプレートのライブバージョンを使用する間、ステージングされたプレゼンテーションやトランスポートのテンプレートを編集およびテストできます。 ステージングされたテンプレートは、検索ドメインのURLのステージングされたバージョンを使用してテストします。 例えば、ステージングされたクエリ(`sp_staged=1`)を実行し、トランスポートテンプレートの名前に設定された`sp_t`を使用して、ステージングされたトランスポートテンプレートをテストできます。 レイアウトの表示に満足したら、テンプレートエディター内で&#x200B;**[!UICONTROL Push Live]**&#x200B;を使用してテンプレートをライブにします。 テンプレートがライブになると、サイトの訪問者はテンプレートの使用を開始します。

プレゼンテーションテンプレートタグ参照を使用して、ファセット、パンくずリスト、メニューなどのガイド付き検索コンポーネントにプレゼンテーションテンプレートを接続する方法を学習します。

[プレゼンテーションテンプレートタグ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)を参照

トランスポートテンプレートで使用するタグの詳細については、トランスポートテンプレートタグ参照を参照してください。

[トランスポートテンプレートタグ](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)を参照

**[!UICONTROL To edit a presentation or a transport template]**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページで、プレゼンテーションまたはトランスポートテンプレートファイル名をクリックします。
1. [!DNL Template Editor]ページで、タグとコーディングを変更します。

   [!DNL Template Editor]；で行う変更には注意が必要です。元に戻す機能はありません。 意図しない変更を行い、前のバージョンのファイルに戻る場合は、**[!UICONTROL Cancel]**&#x200B;をクリックしてテンプレートの表に戻ります（その時点まで変更を保存していない場合）。 変更を保存済みの場合は、エディターで&#x200B;**[!UICONTROL History]**&#x200B;を使用して、変更を元に戻すことができます。
1. （オプション）**[!UICONTROL Insert Symbol]**&#x200B;をクリックして、米国英語のキーボードに対応するキーを持たない特殊文字や記号を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

1. 終了したら、テンプレートエディタページを閉じます。「テンプレート」ページに戻ります。

## プレゼンテーションまたはトランスポートテンプレートファイルのコピー{#task_B744AB3384C84DD59C33CD25E18C2C90}

**[!UICONTROL Copy Template]**&#x200B;を使用すると、既存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を複製してテンプレートページに追加することで、時間を節約できます。

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

テンプレート名、テンプレートタイプ、またはその両方を変更する必要があります。 変更を行わない場合、テンプレートはコピーされません。

テンプレートをコピーするには、既にテンプレートを追加しておく必要があります。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

**プレゼンテーションまたはトランスポートテンプレートファイルをコピーするには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページの、コピーするテンプレート名の横にあるドロップダウンリストで、**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Copy Template]ダイアログボックスで、必要な1つ以上のオプションを設定します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## プレゼンテーションまたはトランスポートテンプレートファイルの名前の変更{#task_CC30050FC2DE4898BF44379D8378EB31}

[!DNL Rename Template]を使用して、既存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)の名前を変更できます。

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

必要に応じて、テンプレートタイプを変更することもできます。

テンプレート名を変更するには、既にテンプレートを追加しておく必要があります。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

**プレゼンテーションまたはトランスポートテンプレートファイルの名前を変更するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページの、名前を変更するテンプレート名の横にあるドロップダウンリストで、**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Rename Template]ダイアログボックスで、必要な1つ以上のオプションを設定します。
1. クリック **[!UICONTROL Rename]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## プレゼンテーションまたはトランスポートテンプレートファイルの削除{#task_67E532C2B83A449687737E3B06C5AA58}

**[!UICONTROL Delete Template]**&#x200B;を使用して、既存のプレゼンテーションテンプレート(.tmpl)またはトランスポートテンプレート(.tpl)を削除できます。

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

ライブにプッシュされたステージテンプレートに対応するバージョンが既に存在する可能性があります。 テンプレートが存在する場合は、必ず&#x200B;**[!UICONTROL Staging]**&#x200B;を使用して削除済みの環境をライブにプッシュし、ライブテンプレートからも削除されるようにしてください。 または、テンプレートページで&#x200B;**[!UICONTROL Push Live]**&#x200B;を使用できます。

[ステージングについて](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)を参照

[ステージ設定をライブにプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照

テンプレートを削除するには、既にテンプレートを追加しておく必要があります。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

**プレゼンテーションまたはトランスポートテンプレートファイルを削除するには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページの、削除するテンプレート名の横にあるドロップダウンリストで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Delete Template]ダイアログボックスで、**[!UICONTROL Delete.]**&#x200B;をクリックします
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 最小化したプレゼンテーションテンプレートのプレビュー{#task_1757B6207CC74221AE4BFFE5674D320B}

プレゼンテーションテンプレートを最小限に抑える場合、**[!UICONTROL Preview minimized]**&#x200B;を使用して、プレゼンテーションテンプレートの縮小ページ重み付けがどのように表示されるかを確認できます。

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

メインのプレゼンテーションテンプレートを最小限に抑える場合は、（ガイド付きインクルードタグと共に）テンプレートを含める際の最小化を必ず有効にしてください。これは、このオプションは継承できないからです。

[プレゼンテーションテンプレートのページ重み付けを減らすを参照してください…](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

テンプレートは、最小化した状態で、プレビューに既に追加されている必要があります。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

トランスポートテンプレートファイルのXMLコードをプレビューできます。

「[トランスポートテンプレートファイルのXMLのプレビュー](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)」を参照してください。

**プレゼンテーションテンプレートを最小化してプレビューするには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページのプレゼンテーションテンプレート名の横のドロップダウンリストで、**[!UICONTROL Preview minimized]**&#x200B;をクリックします。

   テンプレートテーブルの&#x200B;**[!UICONTROL Type]**&#x200B;列を使用して、プレゼンテーションとトランスポートでテンプレートを並べ替えます。
1. （オプション）[!DNL Preview Minimized Template]ページで、**[!UICONTROL Wrap lines]**&#x200B;をチェックして、定義されたウィンドウ内のタグを読み取ります。
1. クリック **[!UICONTROL Close]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## Webサイト上のプレゼンテーションテンプレートのページ重み付けを減らす{#task_B09BB3CE89714DEAAE8D9A899CF3009E}

テンプレートテーブルの&#x200B;**[!UICONTROL Minimize]**&#x200B;オプションを使用すると、プレゼンテーションテンプレートのページ重み付けを減らすことができます。

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

テンプレートのページ重み付けを減らすことで、インラインのJavaScriptとCSSを動的に最小化できます。 また、HTML内の重複した空白を削除します。 プレゼンテーションテンプレートのページ重み付けを最小化すると、検索結果をより迅速に配信するのに役立ちます。

**[!UICONTROL Preview minimized]**&#x200B;を使用して、最小化したプレゼンテーションテンプレートの外観をプレビューすることもできます。

[最小化したプレゼンテーションテンプレートのプレビュー](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)を参照してください。

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページの[!DNL Minimize]列の下で、Webサイト上で最小限に抑えてプッシュする1つ以上のプレゼンテーションテンプレートファイルのチェックボックスをオンにします。

   [!DNL Templates]テーブルの&#x200B;**[!UICONTROL Type]**&#x200B;列を使用して、テンプレートをプレゼンテーションとトランスポートで並べ替えます。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## Webサイトで使用するデフォルトのプレゼンテーションテンプレートファイルの設定{#task_C1E8CE817E4D43E096167A347C54DD53}

複数のプレゼンテーションテンプレートがある場合、検索結果の表示に最初に使用するテンプレートを指定できます。

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

検索前のルール、検索後のルールおよびビジネスルールを使用して、他のプレゼンテーションテンプレートの1つを使用するタイミングを決定できます。

[Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)についてを参照してください。

[検索後のルールについて](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)を参照してください。

[ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

「検索ごとに、対象のプレゼンテーションテンプレートをxxxxに設定する」などのルールを設定するのは一般的です。 このようなルールを適用した状態で、テンプレートページの「デフォルト」テンプレートを変更しても何も起こりません。

**[!UICONTROL To set the default presentation template file to use on your website]**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページの[!DNL Default]列の下で、デフォルトとして使用する対応するプレゼンテーションテンプレートファイルのラジオボタンをクリックします。

   [!DNL Templates]テーブルの&#x200B;**[!UICONTROL Type]**&#x200B;列を使用して、テンプレートをプレゼンテーションとトランスポートで並べ替えます。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## トランスポートテンプレートファイル{#task_58C6C52078E14AD88D2B2F0B3C439AE8}のXMLのプレビュー

[!DNL Preview]を使用して、追加したトランスポートテンプレートのXMLを確認できます。

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

テンプレートのXMLには、既にプレビューにトランスポートテンプレートを追加しておく必要があります。

「[新しいプレゼンテーションまたはトランスポートテンプレートファイルの追加](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)」を参照してください。

最小化したプレゼンテーションテンプレートファイルをプレビューして、その縮小ページ重み付けを表示できます。

[最小化したプレゼンテーションテンプレートのプレビュー](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)を参照してください。

**トランスポートテンプレートファイルのXMLをプレビューするには**

1. 製品メニューで、**[!UICONTROL Design]**/**[!UICONTROL Templates]**&#x200B;をクリックします。
1. [!DNL Templates]ページのトランスポートテンプレート名の横のドロップダウンリストで、**[!UICONTROL Preview]**&#x200B;をクリックします。

   [!DNL Templates]テーブルの&#x200B;**[!UICONTROL Type]**&#x200B;列を使用して、テンプレートをプレゼンテーションとトランスポートで並べ替えます。
1. 表示ウィンドウを閉じて[!DNL site search/merchandising]に戻ります。
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
