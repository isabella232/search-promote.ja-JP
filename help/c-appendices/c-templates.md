---
description: 'null'
seo-description: 'null'
seo-title: テンプレート一覧
solution: Target
title: テンプレート
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# テンプレート{#templates}

## テンプレート{#concept_A5CFB6BD805D49459A96219AF1B17842}

## プレゼンテーションテンプレートタグ {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

プレゼンテーションテンプレートのサイト検索/マーチャンダイジングタグと属性のリスト。


プレゼンテーションテンプレートは、サイト検索/マーチャンダイジングで定義されるプレゼンテーションテンプレートタグを含むHTMLファイルです。 これらのタグは、顧客に表示される検索結果の形式を示します。

テンプレート [についてを参照してくださ](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)い。

次のプレゼンテーションタググループから選択できます。

* [宣言](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [結果](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [ファセット](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [パンくず](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [メニュー](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [最近の検索](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [どういう意味だ？](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [オートコンプリート](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [ストア](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [ゾーン](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [ループインジケータ](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [その他の言語](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## 宣言 {#section_82C5CA734D2941EB858FEFE3B695D2EC}

宣言は、最上位レベルのプレゼンテーションテンプレートの最上部に設定できる、特別なガイド付き宣言タグです。 含まれるテンプレート内の宣言を含め、以降の宣言は無視されます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>デフォルトでは、プレゼンテーションテンプレートはMIMEタイプtext/htmlで返送されます。 このタグで使用するコンテンツタイプを変更できます。 </p> <p>このタグは、プレゼンテーションテンプレート内で可能な限り高く宣言します。 このタグを使用して、同じ行に他のテキストを追加しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> XMLを返す場合は、このタグを使用してXML宣言を作成できます。 このタグをプレゼンテーションテンプレートの最初の行にします。 このタグを使用すると、最初の行で <span class="codeph"> &lt;guided-content-type-header&gt;を使用して上書きしない限り、content-typeは自動的にtext/xmlに設定 </span> されます。 文字セットを指定しない場合、デフォルトはUTF-8です。 このタグは、XMLドキュメントで次の出力を返します。 </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果 {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results [gsname="searchname"]&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>guided-resultsタグは、結果ループの境界を定義します。 gsname属性を指定すると、任意の結果セットにアクセス <span class="codeph"> でき </span> ます。 gsnameが指定さ <span class="codeph"> れて </span> いない場合は、デフォルトの検索結果が表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link [gsname="fieldname"] [attr="value"]+&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の結果へのリンクを作成するには、 <span class="codeph"> guided-result-linkタグを使用し </span> ます。 gsname属性を定 <span class="codeph"> 義す </span> ると、「search-url」を参照する標準の「loc」タグの代わりに、インデックスのフィールドを使用できます。 クラスやターゲットなど、他の属性も渡すことができ、結果のアンカータグに出力されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname" [attr="value"]+&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-result-img&gt; <span class="codeph"> タグは、生の </span> imgタグ内に変数を埋め込むのではなく、画像タグの作成に役立 <span class="codeph"> ち </span> ます。 </p> <p>画像パスに使用するフィールドをgsname属性で指 <span class="codeph"> 定し </span> ます。 結果は、定義し <span class="codeph"> た標 </span> 準のHTML属性が渡されたimgタグになります。 次に例を示します。 </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname" [escape="html|url|json|ijson|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p> 結果に表示する情報は、 <span class="codeph"> &lt;guided-result-field&gt;タグとして表示されます( </span> &lt;guided-result-img&gt;タグなどの自動生成タグを使用する場合を除く <span class="codeph"></span> )。 </p> <p>「検索インデックス」フィールドの名前を「gsname」に指 <span class="codeph"> 定しま </span>す。 渡された文字列は、テンプレートに出力されます。 </p> <p>このフィールドをトランスポートテンプレートで指定したものとは異なる方法でエスケープする場合は、エスケープオプションを指定できます。 </p> <p>このエンコーディングは、トランスポートテンプレートで指定されたエンコーディングの上に適用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="fieldname&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件タグのセットは、表示する特定のフィールドにコンテンツがある場合にtrueになります。 コンテンツが存在しない場合、条件はfalseです。 タグを使用して、周囲のHTMLを表示するかどうか（値が存在しない場合）、または別の画像を表示するかどうか（その他）を指定できます。 </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>結果を列で表示する場合、このタグを使用して、現在の結果が列の終わりを示すかどうかを識別します。 </p> <p>ブール条件がtrueの場合、HTMLが結果の末尾に追加され、行の最後に追加され、新しい行が開始されます。 最後の行の場合は、新しい行は開始されません。 </p> <p>このタ <span class="codeph"> グの詳細については、&lt;guided-if-not-last&gt; </span> を参照してください。 </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>バックエンド検索要求が結果を返した場合は1を返し、返さなかった場合は0を返します。 gsnameが指定さ <span class="codeph"> れてい </span> ない場合、タグはプライマリ検索と見なされます。 このタグは、JavaScriptルーチンにロジックを渡す場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットの結果の合計数を返します。 gsnameが指定されていない場合に、デフォルトの検 <span class="codeph"> 索を行う </span> と仮定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットに対して、ページ上の下位の結果の結果数を返します。 gsnameが指定されていない場合に、デフォルトの検 <span class="codeph"> 索を行う </span> と仮定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットの、ページ上の上位の結果の結果数を返します。 gsnameが指定されていない場合に、デフォルトの検 <span class="codeph"> 索を行う </span> と仮定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>結果が見つかった場合にコンテンツを表示します。 または、結果が見つからない場合は結果HTMLを表示しません。 </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-result-title&gt; <span class="codeph"> タグは、&lt;title&gt; </span> transportタグで指定されたタイトルトランスポートテンプレートフィールドの <span class="codeph"> 値を </span> 提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-result-description&gt; <span class="codeph"> タグは、&lt;description&gt; </span> transportタグで指定された説明トランスポートテンプレートフィールドの <span class="codeph"> 値を </span> 提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt; <span class="codeph"> guided-result-loc&gt;タグは、 </span> &lt;loc&gt; <span class="codeph"> transportタグで指定されたloc transport templateフィールドの値を </span> 提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Trueを指定すると、特定のフィールドに表示するコンテンツが含まれます。 コンテンツが存在しない場合、条件はfalseです。 タグを使用して、周囲のHTMLを表示するかどうか、値が存在しないか、別の画像を表示するかなどを指定します。 </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、トランスポートテンプレートで定義された属性テーブルを、 <span class="codeph"> &lt;attribute_table&gt;トランスポートタグを使用してルー </span> プ処理します。 属性テー <span class="codeph"> ブルのフィールド値を表示する </span> ための&lt;guided-result-attribute-table-field&gt;タグがあります。 また、ループ内でプレーンなguided-result-field <span class="codeph"> タグを使用して、他の結果 </span> フィールドを表示することもできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートで定義された属性テーブルフィールドを表示します。 </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;
    nbsp;&amp;nbsp;lt;li&amp;gt;gt&amp;nbsp;&amp;nbsp;&amp;;lt;a&amp;nbsp;href=&quot;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&quot;&amp;gt;
    &amp;nbsp;&amp;&amp;nbsp;&amp;nbam;&amp;;;&amp;;sp;amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;
    &amp;nbsp;&amp;&amp;nbsp;&amp;nbsp;&amp;&amp;am;&amp;am;/lt;>;>;nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    
    
    
    
    
    
    &amp;nbsp&amp;lt;li>guided-result&amp;lt;amp;gt;guided-result-amp>lt;lt;lt;
    
    &amp;lt;/guided-results&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の検索用のトランスポートテンプレートによって出力されたJSONデータの一般セクション内のトレースデータ内にあるトレース情報を出力します。 </p> <p>検索名を指定しない場合、デフォル <span class="codeph"> トと見 </span> なされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の検索結果のトランスポートテンプレートによって出力されたJSONデータの結果/トレース情報内のJSONコンテンツを出力します。 </p> <p>このタグは、&lt;guided-results&gt; <span class="codeph"> &lt;/guided-results&gt;ループ内でのみ有効 </span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ファセット {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

ファセットは、検索結果を掘り下げて調べるナビゲーションコンポーネントです。 ファセットタグを使用して、プレゼンテーションテンプレートの様々なファセットを表示できます。 ファセットは名前で参照します。

ファセット [についてを参照してくださ](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)い。

[「Facet Rail」について](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB)を参照してください。

動的ファセ [ットについてを参照してくださ](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>特定の検索に対する任意の動的ファセットのループコンテキスト。 </p> <p>&lt;guided- <span class="codeph"> dynamic-facets&gt; </span> プレゼンテーションテンプレートタグを編集し、gsname属性が&lt;guided-dynamic-facets&gt;ループコンテキストによって自動的に提供されるよう <span class="codeph"></span> にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットの表示ラベルを返します。 </p> <p>ファセットでトランスポ <span class="codeph"> ートテンプレー </span> トの&lt;display-name&gt;タグが使用されている場合、そのタグのコンテンツがラベルになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットパネルの各ファセットの繰り返しパターンとして使用されるプレゼンテーションテンプレートのセクションを定義します。 </p> <p> ファセットパネルに属する各ファセットは、このセクションを使用して出力を評価します。 </p> <p>ファセットパネルの例を次に示します。 </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>次のタグは、 <span class="codeph"> &lt;guided-facet-rail&gt; </span> タグ内の値が検索時に動的に決定され、適切に置き換えられるので、 <span class="codeph"></span> gsname属性は必要ありません。 </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">ガイドファセット </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">guided-facet-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">ガイドファセット動作 </li> 
    </ul> <p>ファセットパネルページの並べ替 <span class="wintitle"> え条件によ </span> って、ファセットの位置が決まります。 「ファセットの並べ替え方法」ドロップダウンリストから並べ替え順を選択できます。 </p> <p> 
     <!--NEW 02/27/2014-->このタグでは、オプションで_dynamic_facetsのgsname属性値を受け入れることができます。これにより、この検索の動的ファセ <span class="codeph"></span>ットに対してループコンテキストが提供されます。 この事前定義されたファセットパネルは、ファセットパネル'_dynamic_facets'のアクションプッシュファセットXをY位置に配置するために、ビジネスルールのユーザーインターフェイスにも表 <span class="codeph"> 示さ </span>れます。 </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">「Facet Rail」について</a>を参照してください。 </p> <p>動的ファセットにつ <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> いても参照してくださ </a>い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>ガイド付きフ <span class="codeph"> ァセットタ </span> グを使用して、すべてのファセットタグが特定のファセットに関連する領域を定義します。 また、このタグはBooleanタグでもあり、ファセットに値が存在しない場合は、すべてのコンテンツを非表示にします。 この場合、ファセット値を出力するポイントはありません)。 </p> <p>高さと幅の属性はオプションで、サイズはピクセル(px)で指定します。 ビジュアルルールビルダー(VRB)では、これら2つの属性を使用し、ファセットが非表示の場合は、インタラクティブなプレースホルダーとして点線のボックスを表示します。 </p> <p> 表示名がファセット内にあり、ファセットが非表示の場合、名前も非表示になります。 ただし、名前がファセットの外にある場合は、ゾーンタグまたはGuided If Facet Visibleタグがその周りに含まれている場合にのみ、名前を非表 <span class="codeph"></span><span class="codeph"></span> 示にすることができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセット値の数が設定で定義された長さのしきい値を超えた場合に適用されます。 リストが長すぎる場合に、切り捨てられたリストやスクロールボックスなど、ファセットを別のUI要素として表示する場合に使用します。 </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>この条件は、gsname属性を使用して特定のファセットを直接参照することで、名前の付いたガ <span class="codeph"> イドファセットブ </span> ロックのコンテキスト外で使用すること <span class="codeph"> もで </span> きます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセットが少なくとも1回クリックされ、現在ファセット値が選択されている場合に有効です。 ファセットがクリックされたかどうかに応じて、HTMLタグまたはgsタグの表示/非表示を切り替えるために使用されます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>この条件は、gsname属性を使用して特定のファセットを直接参照することで、名前の付いたガ <span class="codeph"> イドファセットブ </span> ロックのコンテキスト外で使用すること <span class="codeph"> もで </span> きます。 </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-single [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-single&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセット値が1つだけの場合、この条件付きタグはtrueです。 結果を絞り込むことができない場合は、タグを使用してファセットの表示を変更します。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>この条件は、gsname属性を使用して特定のファセットを直接参照することで、名前の付いたガ <span class="codeph"> イドファセットブ </span> ロックのコンテキスト外で使用すること <span class="codeph"> もで </span> きます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセットが複数選択の場合に適用されます。 タグを使用して、&lt;guided-facet-rail&gt;タグまたは <span class="codeph"> &lt;guided-dynamic-facets&gt;タグ内のファセ </span> ットの表 <span class="codeph"> 示を変更し </span> ます。 </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;...
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values [gsname=" <span class="varname"> facetname </span>"]&gt;&lt;/guided-facet-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>これはファセット値ループイテレータタグです。 名前の付いたガイド付きファセットブロックのコンテキ <span class="codeph"> スト内で定義でき </span> ます。この場合、 <span class="codeph"> gsnameは省略で <span class="varname"> きま </span></span>す。 また、ガイド付きファセットブロックの外部で定義する <span class="codeph"> こともで </span> きますが、 <span class="codeph"> gsname属性を使用して、表示するファセット値のセット <span class="varname"></span></span> を識別する必要があります。 </p> <p>また、このタグを使用して、名前の付いたガイド付きファセットブロックのコンテキスト外にファセット値を表 <span class="codeph"> 示することもで </span> きます。 gsname属性を使用して、特定のファセットを直接 <span class="codeph"> 参 <span class="varname"> 照で </span> きま </span> す。 </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のファセット値の文字列を出力します。 </p> <p>デフォルトでは、この値はHTML escapedです。 値のエスケープ方法を変更するには、エスケープオプションを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のファセット値と一致する結果の数を出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link [attr="value"]+&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>サイト訪問者がクリックするファセット値文字列を囲むリンクを作成します。 パスが自動的に生成され、現在のファセット値で結果が絞り込まれます。 任意の属性をアンカータグに直接渡すことができます。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>ファセット値が現在選択されている場合に、その表示を変更します。 選択済みの場合は、ほとんどの場合、リンクできなくなります。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-value-ghost&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ファセット値がゴースト値の場合に、ファセット値の表示を変更します。 ファセット値がゴースト値の場合、通常、ファセット値は斜体で表示され、その値が存在しない（「ゴースト」されている）ことを示します。 </p> <p>次のコードの抜粋は、ファセットブロックの例です。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定のファセットの元に戻すリンクを表示します。 複数選択ファセットがある場合、このリンクは指定されたファセットの値のすべてを選択解除します。 ファセットに名前を付けます。 ファセットが現在選択されていない場合、リンクは現在のパスになります。 </p> <p>このタグの使用例を次に示します。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセット値の数が設定で定義された長さのしきい値を超えた場合に適用されます。 リストが長すぎる場合に、切り捨てられたリストやスクロールボックスなど、別のユーザーインターフェイス要素としてファセットを表示する場合に使用します。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>この条件は、名前の付いたガイド付きファセットブロックのコンテキスト外で使用するこ <span class="codeph"> ともで </span> きます。その場合は、 <span class="codeph"> gsname属性を使用して、特定のファセットを直接参照 <span class="varname"></span></span> します。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセットが少なくとも1回クリックされ、現在ファセット値が選択されている場合に有効です。 ファセットがクリックされたかどうかに応じて、HTMLタグまたはgsタグの表示/非表示を切り替えるために使用できます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>この条件は、gsname属性を使用して特定のファセットを直接参照することで、名前の付いたガ <span class="codeph"> イドファセットブ </span> ロックのコンテキスト外で使用すること <span class="codeph"> もで </span> きます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>ファセット値が1つだけの場合、この条件付きタグはtrueです。 結果を絞り込む機能がない場合に、ファセットの表示を変更するために使用できます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>この条件は、名前の付いたガイド付きファセットブロックのコンテキスト外で使用するこ <span class="codeph"> ともで </span> きます。その場合は、 <span class="codeph"> gsname属性を使用して、特定のファセットを直接参照 <span class="varname"></span></span> します。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>この条件を使用すると、指定したファセットに値がまったく含まれているかどうかを確認できます。 空のファセットの代わりに別のファセットを表示する場合に使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定のファセット内の結果の合計数を出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname="関連付けら <span class="varname"> れたカスタムファセ </span>ット値" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットに関連付けられている値の文字列を出力します。 ファセットには、0個以上のフィールドを関連付けることができます。 関連付けられたフィールドを持つことは稀で、このようなフィールドをサポートするためにトランスポートテンプレートを設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname="関連付けら <span class="varname"> れたカスタムファセット </span>値"/&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセット値にフィールド値が関連付けられているかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [attr=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>顧客がクリックするファセット値文字列を囲むリンクを作成します。 パスが自動的に生成され、現在のファセット値で結果が絞り込まれます。 任意の属性をアンカータグに直接渡すことができます。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセット値への独自のリンクを作成します。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>デフォルトでは、この値はURLエスケープされています。 ただし、エスケープパラメーターを使用して使用するエスケープモードを指定することで、別のエンコーディングレイヤーを追加できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-facet-values&gt; <span class="codeph"> で各ファセット値 </span> を繰り返し処理すると、このタグはネストされたファセットのすべての子値を繰り返し処理します。 このタグ内で、リンクの作成、元に戻すリンクの作成、ファセット値の表示に、一般的なファセットタグを使用します。 このタグは、ネストされたル <span class="codeph"> ープ処理を行うので、&lt;guided-facet-values&gt; </span> 内に配置する必要があります。 </p> <p>このタグの使用例を次に示します。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在のファセット値に子の値が含まれているかどうかをテストします。 &lt;guided-facet-value-children&gt;タグを使用する前 <span class="codeph"> にを使用することをお勧めし </span> ます。 「else」句はオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-above-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-above-length-threshold&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ファセット値ループ内の現在のファセット値が長さのしきい値を超えているかどうかを判定します。 通常、長いファセットではしきい値を下回る値のみを表示する目的で使用されます（ユーザーが以前にファセットの下に表示される「詳細を表示」リンクを選択した場合を除く）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length-threshold&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ファセット値ループ内の現在のファセット値が長さのしきい値と等しいかどうかを判定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定したファセット値の元に戻すリンクを表示します。 選択したファセット値の横に元に戻すリンクを表示する場合に使用します。 この取り消しリンクは、選択した特定の値を取り消すだけなので、選択したすべての値の選択を解除する <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> とは異なります。 </p> <p> <p>注意： ファセットに複数選択の動作がない場合、2つの元に戻すリンクは同じ動作を持ちます。 つまり、ファセットには1つの選択された値しか含めることができません。 </p> </p> <p>ファセットが現在選択されていない場合、リンクは現在のパスになります。 このタグは、guided-facet-valuesルー <span class="codeph"> プ内でのみ使用し </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のファセット値の元に戻すリンクを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のファセット元に戻すリンクを作成します。 </p> <p> &lt;guided-facet-undo- <span class="codeph"> link&gt;タグと同様ですが、独自の元に戻すリ </span> ンクを作成するための生のパスを提供する点が異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>特定のファセットに選択された値または単一の値「値」がある場合、HTMLを条件付きで表示します。 このタグのセットは、多くの場合、別のファセットで選択した値に基づいてファセットを表示するために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>通常、共通、複数選択など、ファセットの動作を指定します。 XML結果を受け取り、その動作に基づいてファセットの表示方法を動的に変更する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> <varname></varname>

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>このタグで折り返されるコンテンツは、ファセットの表示状態に基づいて、非表示または表示されます。 ビジネスルールでファセットを直接表示または非表示にすると、ファセット内のコンテンツは非表示になります。 これらのタグをファセットの周りに含める必要はありません。 </p> <p> このタグの一般的な使用方法は、名前がファセットの外にある場合に表示名を非表示にすることです。 このタグを表示名の周りに囲むと、ファセットが非表示のときに名前が表示されなくなります。 </p> <p>このタグは、ゾーンを置き換えるものであり、ゾーンを使用する場合と同じパフォーマンス上の利点が多数あります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## パンくず {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

詳しくは、パ [ンくずリストについてを参照してくださ](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb [gsname=" <span class="varname"> breadcrumbname </span>"]&gt;&lt;/guided-breadcrumb&gt; </span> </p> </td> 
   <td colname="col2"> <p>パンくずリストのループタグ。 開始タグと終了タグの間にあるコンテンツは、現在の状態のクエリ番号ごとに反復されます。 </p> <p>gsnameを <span class="codeph"> 省略 <span class="varname"> すると </span></span> 、「default」という名前のパンくずリストが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>階層リンクにリンクを作成します。 デフォルトの動作は「goto」動作です。 リンクの動作が異なる場合は、 <span class="codeph"> gsname <span class="varname"> optional属性を使 </span></span> 用して「remove」または「drop」を指定します。 タグに含まれる属性は、結果のアンカータグに渡されます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>valueタグは、現在の階層リンクイテレーションの変換された値を出力します。 これは、ガイド付き階層リンクブロックのコンテキ <span class="codeph"> ストでのみ使用さ </span> れます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>labelタグは、階層リンク項目を生成するために選択されたファセットの詳細を示す階層リンク値のラベルを出力します。 これは、ガイド付き階層リンクブロックのコンテキ <span class="codeph"> ストでのみ使用さ </span> れます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、現在の階層リンクの値にラベルが含まれている場合に、コンテンツを条件付きで表示するために使用されます。 ラベルが実際に存在する場合にのみ、ラベルを表示し、コンテンツを関連付けるために使用されます。 これは、ガイド付き階層リンクブロックのコンテキ <span class="codeph"> ストでのみ使用さ </span> れます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path [gsname="goto|remove|drop"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自の階層リンクの構築に使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## メニュー {#section_1D489ADF041F4351A66E5D5742125CA8}

メニューにつ [いてを参照してくださ](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>これは、メニュー値のloop iteratorタグです。 gsname属性を使 <span class="codeph"> 用し </span> て、表示するメニュー項目のセットを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link [attr="value"]+&gt;&lt;/guided-menu-item-link </span> </p> </td> 
   <td colname="col2"> <p>メニュー項目の現在の検索を絞り込むためのURLが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option [attr="value"]+ /&gt; </span> </p> </td> 
   <td colname="col2"> <p>通常、テンプレートの選択コントロールにメニューが表示されます。 このタグを使用すると、selectコントロールのオプションを生成するHTMLが生成されるので、selectコントロールの構築が容易になります。 </p> <p>例えば、次のコードブロックがあります。 </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>次のようなHTMLを生成できます。 </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>メニューに関連付けられている値の文字列を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>メニューに関連付けられているラベルの文字列を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>パス文字列を返します。 パスにパラメータを追加し、カスタムリンクを作成する場合は、タグを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在のメニュー項目が選択されているかどうかを示す1または0を返します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

ページナビゲーションタグを使用して、検索結果内を移動できる一連のリンクを作成できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-pages&gt;&lt;/guided-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p>ページナビゲーションのループタグ。 開始タグと終了タグの間のコンテンツは、各ページで反復されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>ページナビゲーションにリンクを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages" [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>最初、前、次または最後のページへのリンクを作成します。 また、1つのページのすべてのページを表示するリンクを作成することもできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> 現在のページ番号を含む文字列を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在繰り返し処理されているページが選択されている場合、この条件付きタグのセットはtrueです。 通常、ページナビゲーションコントロールでページ番号を別々に表示するために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> 現在のページに前のページが含まれる場合、この条件タグのセットはtrueです。 通常、前のリンクをページナビゲーションに表示する際に使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> 現在のページに次のページがある場合、この条件タグのセットはtrueです。 通常、前のリンクをページナビゲーションに表示する際に使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> 検索が大きな結果セットを返す場合は、すべての結果を表示する機能を提供したくない場合があります。 したがって、この一連の条件付きタグを使用して、「すべて表示」リンクを表示するタイミングを決定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件タグのセットを使用して、「ページを表示」リンクを表示するタイミングを決定できます。 通常は、顧客が特定のページを表示できるようにするために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ページナビゲーションに最初のページ、前のページ、次のページが含まれるかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索結果の合計ページ数を示す文字列を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>ページナビゲ <span class="codeph"> ーションの設 </span> 定が少ない場合は、ガイド付きページ番号タグを使用して、すべてのページ番号タグが特定のページ番号設定に関連する領域を定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewwall|viewpages/&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ページナビゲーションに独自のリンクを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>ページナビゲーションの最も高いページが合計ページ数と等しいかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>ページナビゲーション内の最も低いページが同じかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果のページが1つか、結果のページが複数かをテストします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 最近の検索 {#section_8CD907521F584257B475595B01A5964B}

次の例のように、最近の検索タグを使用して、以前の検索をすばやく実行できる一連のリンクを作成できます。

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

詳しくは、最 [近の検索の設定を参照してくださ](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>最近の検索のループタグ。 開始タグと終了タグの間のコンテンツは、各ページで反復されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>最近の検索へのリンクを作成できます。 HTML属性を直接アンカータグに渡すことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>最近の検索の相対URLパスを、ガイド付き最近の検索ループ内 <span class="codeph"> で取得でき </span> ます。 通常は、 <span class="codeph"> guided-recent-search-linkを使用します </span>。 ただし、独自のリンクを作成する場合は、このタグを使用できます。 次に例を示します。 </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>最近の検索に関連付けられたクエリ用語を取得できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link [attr="value"]+&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>顧客に、最近保存した検索をクリアする機能を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のリンクを作 <span class="codeph"> 成できるように、 </span> &lt;guided-recent-searches-clear-link&gt;で使用するパスを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-recent-searches&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>顧客が最近の検索を実行した場合に、最近の検索を表示できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

##  {#section_C1EB3B9D8E1242798A6E04609D1E3543}

検索で結果が返されず、検索語句がアカウントの辞書にない場合は、Did You Meanタグを使用して、提案への一連のリンクを作成できます。 次に、Did You Meanタグの使用例を示します。

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

[「Did You Mean」について](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)を参照してください。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-surgestions&gt;&lt;/guided-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>これは、サーチクエリに対してループするループタグです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-link [attr="value"]+&gt;&lt;/guided-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した提案へのリンクを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>提案があるかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>提案へのパス文字列を返します。 独自のアンカータグを作成する場合に使用します。 通常、代 <span class="codeph"> わりにguided-suggestion-linkが </span> 使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion/&gt; </span> </p> </td> 
   <td colname="col2"> <p>提案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-result-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>提案の結果数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>この機能がオンの場合に備えて、検索結果がゼロのサーチクエリによる自動検索が実行されたかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-query/&gt; </span> </p> </td> 
   <td colname="col2"> <p>自動検索が実行された場合、元のクエリを返します。 </p> <p>使用例： </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>この機能がオンの場合、結果数が少ないことが原因で提案がある場合、この条件はtrueになります。 </p> <p>このタグの使用例を次に示します。 </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## オートコンプリート {#section_897316BEE1454E839A56B565CA4AF018}

次のタグを使用して、検索フォームにオートコンプリートを追加できます。 オートコンプリート機能を正しく動作させるには、head-contentタグとform-contentタグが必要です。 オートコンプリートのJavaScriptとCSSをプレゼンテーションテンプレートにハードコーディングするのではなく、タグを使用することをお勧めします。 この理由は、タグを使用すると、テンプレートを手動で更新しなくても、オートコンプリートの設定を変更するたびに、テンプレートで新しい敗北キャッシュIDを取得できるからです。

オートコ [ンプリートについてを参照](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578)。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>オートコンプリート機能が有効かどうかを検出します。 タグを使用して、オートコンプリートに必要なヘッドおよびフォームコンテンツをオプションで取得できます。 これにより、機能のオン/オフを切り替え、プレゼンテーションテンプレートを変更する必要がなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>プレゼンテーションテンプレートのheadで使用され、オートコンプリート用の適切なCSSスクリプトのインクルードに置き換えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content/&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォーム内のオートコンプリートタグをハードコーディングする代わりに、プレゼンテーションテンプレートの検索フォーム( <span class="codeph"> &lt;form&gt; </span> タグと <span class="codeph"> &lt;/form&gt; </span> タグの間)で使用されます。 タグは、オートコンプリート機能を動作させるために必要な適切なHTMLに置き換えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Autocomplete JavaScriptへのリンクを生成します。 最高のパフォーマンスを得るために、このタグをページの下部付近に配置してから、「body」終了タグの前に配置することをお勧めします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Store {#section_A33E25DB5E67404A823BD9618665B773}

次のタグを使用して、ユーザーが現在所在するストアをテストし、表示します。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のストアを出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがストアにいるかどうかを検出します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがgsnameパラメーターで指定されたストアにいる <span class="codeph"> かどうかを </span> 検出します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ゾーン {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area" [search="associated search"] [facet="associated facet"] [width="xx" height="yy"]&gt; </span> </p> </td> 
   <td colname="col2"> <p>任意のコンテンツをゾーンタグで囲むと、その領域からゾーンを作成できます。 これにより、必要に応じて、ビジネスルールを使用してゾーンを表示できます。 デフォルトでは、ゾーンは常に表示されます。 オプションの検索パラメーターとファセットパラメーターを使用して、ゾーンに関連付けられている検索またはファセットを示すことができます。 この機能を使用すると、ゾーンが非表示の場合に検索やファセットをスキップし、検索時のパフォーマンスを向上できます。 高さと幅の属性はオプションで、ゾーンを削除したときにプレースホルダがVisual Rule Builderでどのように表示されるかを設定するために使用されます。 </p> <p> 可能な場 <span class="codeph"> 合は、ゾーンの代わりにguided-if-facet[-not]-visible </span> タグを使用します。 プレゼンテーションテンプレートが簡単になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグを使用すると、ゾーンが現在表示されているかどうかをテストできます。 この機能は、ページ上の他の場所に、ゾーンが表示されたときにのみ表示したいコンテンツがある場合に役立ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ループインジケータ {#section_387322CA0AA843A2ACF2795C328673E9}

次の各ループインジケーターは、これらのループブロックで使用できます。

* 誘導結果
* guided-facet-values
* ガイドパンくず
* guided-menu-items
* ガイド付きページ

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復がループの最初の反復である場合にtrueになります。 これは、最初の結果または最初のページが表示されるという意味ではなく、最初のページが表示されるという意味です。 サイト訪問者が1ページにつき10件の結果セットの2ページ目にいる場合、最初の反復は11となります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しがループの最後の繰り返しである場合、この条件はtrueです。 これは、最後の結果または最後のページを意味するわけではなく、現在のコンテキスト（ページ）に最後に表示される結果を意味します。 サイト訪問者が200件の結果を含む結果セットの1ページ目にいて、1ページにつき10件の結果しかない場合、最後の繰り返しの結果は200件ではなく10件になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復が（偶数の反復に対して）奇数のループの反復である場合に当てはまります。 これは、行の様々な色を表示する場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復が（奇数の反復に対して）ループの偶数の反復である場合に当てはまります。 これは、行の様々な色を表示する場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の繰り返しがループの偶数の繰り返しである場合に当てはまります。 これは、行の様々な色を表示する場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初と最後のどちらでもない場合、その間のテキストを含めます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初または最後の場合に、その間のテキストを含めます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>ループの各反復で値が増加する（0から始まる）整数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>ループの各反復で値が増加する（1から始まる）整数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## その他の言語 {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

次のタグを使用して、独自のミニファセットの作成など、テンプレートを使用してより高度な操作を行うことができます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path [escape="html|url|json|0"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在使用されているパスが表示されます。 通常、このリンクは、既存の検索に新しいパラメータを追加するリンクを作成するために使用されます。 デフォルトでは、パスはURLエスケープされています。 エスケープパラメータを使用して、使用するエスケープモードを指定できます。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>この例では、検索処理ルールでlangを使用してフランス語版を選択しています。 </p> <p>現在のパスには、常に1つ以上のクエリパラメーターが含まれています。 他のクエリパラメーターが存在しない場合は、 <span class="codeph"> q=*に設定するので、 </span> より多くのパラメーターを追加しやすくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> ベースパス </span> </p> </td> 
   <td colname="col2"> <p> ベースパスを使用してリンクを作成する場合は、 <span class="codeph"> hrefの先頭 </span> で/を使用し、パラ <span class="codeph"> メータ </span> ーを追加します。 </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter" [escape="html|url"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>URL上のクエリパラメーターの既存の値を取得できます。 パラメーターが存在しない場合、このタグは空の文字列を返します。 エスケープオプションを指定しない場合、返される文字列は自動的にHTMLエスケープされ、HTMLエスケープまたはURLエスケープを指定できます。 </p> <p>例： </p> <p> 

    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gz
    &amp;nbsp;nbsp;you&amp;nbsp;nbsp;value&amp;nbsp;lt;guided-query-param
    
    &amp;lt;nbsname=&quot;&amp;lang&quot;&amp;sp;;/;gt;
    gevs&amp;nbsp;you&amp;nbsp;the&amp;nbsp;en
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;gt;gs&amp;you&amp;nbsp;empty&amp;n；文字列
    &amp;アンプ；nbsp;
    
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ガイド付き検索は、階層リンクコントロールで使用されるクエリ番号の概念を持ちます。 <span class="codeph"> guided-query-param-nameを使用すると、 </span> プレゼンテーションテンプレート内のリンクの一部としてパラメータを定義できます。このリンクによって、ガイド付き検索で正しいクエリ番号が見つかります。 gsnameに <span class="codeph"> は「x」 </span> が含まれており、ガイド付き検索では正しい番号に置き換えられます。 オフセット値は0 ～ 15です。0は次に使用可能なクエリ番号が使用されることを示します。 「1」は、1を追加することを示します。 </p> <p>ガイド付き現 <span class="codeph"> 在のパスと組み合わ </span>せて、独自のミニファセットリンクを構築したり、追加のドリルダウンレベルを許可したりできます。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> その他のテンプレートファイルを含めることができます。 この機能により、サブテンプレートをモジュールとして使用して複数のテンプレートを作成できます。 </p> <p>次の例では、パンくずリストとフ <span class="filepath"> ァセットフ </span> ァイル <span class="filepath"> が含ま </span> れています。 </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>動的なインクルードはサポートされていません。 つまり、gsfileを変数にす <span class="codeph"> るこ </span> とはできません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索に要した時間を示します。 返される検索時間の値はミリ秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索結果のページを作成するために使用されるコア検索の数を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>コア検索の数が1より大きいかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復が（奇数の反復に対して）ループの偶数の反復である場合に当てはまります。 これは、行の様々な色を表示する場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復がループの偶数の反復である場合に当てはまります。 これは、行の様々な色を表示する場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初と最後のどちらでもない場合、その間のテキストを含めます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初または最後の場合に、その間のテキストを含めます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>最初の検索で検索中かどうかを確認できます（クエリは検索ボックスからの検索の結果でした）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグをテンプレートで使用すると、検索フォームのアクションをハードコーディングせずに保存できます。 ステージング環境またはライブ環境にいつあるかを検出し、それに応じて変更します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグを使用すると、検索パスで定義されているCGIパラメーターをテストできます。 パラメーターが定義されている場合にのみ、パラメーターの値をテストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number [gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>テンプレートを駆動するガイド付き検索エンジンは、エンジンが生成する新しい各リンクが次に使用可能なクエリ番号を使用するフローティングクエリ番号の概念を持ちます。 このタグを使用すると、次のクエリ番号またはオフセットを取得して、結果セットにドリルインするカスタムリンクを作成できます。 オフセットを使用すると、次のクエリ番号にオフセットできます。 例えば、ファセットを1つ選択した場合、次のクエリー番号は2で、オフセットが1のクエリー番号は3です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>処理ルールで定義されているカスタム変数の既存の値を取得できます。 エスケープオプションを指定しない場合、返される文字列は自動的にHTMLエスケープされ、 <span class="codeph"> html、 </span>url、js、 <span class="codeph"> または </span>0を指定で <span class="codeph"></span><span class="codeph"></span>きます。 処理ルールを使用して受信CGIパラメーターをカスタム変数にコピーし、エスケープセットをnoneまたはjsに設定して、その変数をテンプレートに表示または使用する場合は、検索にXSS脆弱性を作成できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>処理ルール（クエリのクリーニング、検索前の処理、検索後の処理）でカスタム変数が定義されているかどうかをテストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートで定義された一般フィールドの内容を表示できます。 エスケープオプションを指定しない場合、返される文字列は、そのフィールドのトランスポートテンプレートで指定した形式でエンコードされます。 エスケープオプションの指定は、トランスポートテンプレートと同様にフィールドをエンコードしている形式の上に適用されます。 html、js <span class="codeph"> json、 </span>url <span class="codeph"> 、 </span>0のいずれかを指定で <span class="codeph"> きます </span><span class="codeph"></span><span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートで定義された一般フィールドのコンテンツが存在するかどうかをテストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>cookieが使用可能であると仮定して、cookieの値を取得できます。 エスケープオプションを指定しない場合、返される文字列は自動的にHTMLエスケープされ、html、 <span class="codeph"> js、js、json、または0を指 </span>定でき <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cookieが存在するかどうかのテストを有効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area" [escape="html|url|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の領域のバナーを出力します。 オプションの幅と高さの属性は、ユーザーがバナーを選択できるように、意味のあるプレースホルダーを表示できるようにするために、ビジュアルルールビルダーで使用されます。 デフォルトでは、バナーはエスケープされません。 代わりに、プレゼンテーションテンプレートにHTMLを挿入する必要があります。 ただし、JSONテンプレートを作成する場合は、jsエスケープオプションの使用を検討してください。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>バナー領域が設定されているかどうかのテストを有効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>シミュレーターまたはビジュアルルールビルダーで検索を表示していることを検出できます。 通常は、追加のデバッグ情報を表示するために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Adobe Targetキャンペーンを参照するビジネスルールがあるかどうかを <span class="keyword"> 検出で </span> きます。 通常、Targetサーバーが不要な場合にTargetサーバーにアクセスするのを防ぐために、 <span class="keyword"> Adobe Targetとの統合の一部として使用さ </span><span class="keyword"></span> れるツールです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect/&gt; </span> </p> </td> 
   <td colname="col2"> <p>デフォルトでは、リダイレクトは自動的に実行されます。 ただし、WebアプリケーションにXMLまたはJSONの応答を返すようにサイト検索/マーチャンダイジングを設定した場合は、Webアプリケーションで302/301の応答を解析するか、結果セットの一部としてリダイレクトを渡すかを選択できます。 結果セットの一部としてリダイレクトを渡す場合、このタグをテンプレートで使用してリダイレクト場所を出力できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果セットにリダイレクトを返すようにサイト検索/マーチャンダイジングを設定した場合、このタグセットを使用して、出力へのリダイレクトがあるかどうかを判断できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt/&gt; &lt;guided-gt/&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグを使用すると、ガイド付きテンプレートタグをHTML属性内に埋め込むことができます。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 転送テンプレートタグ {#reference_227D199F5A7248049BE1D405C0584751}

トランスポートテンプレートは、バックエンド検索からガイド付き検索プレゼンテーションレイヤーにデータを渡すXMLテンプレートです。

<!-- 

r_transport_template_tags.xml

 -->

プレゼンテーションレイヤーには、複数の検索結果を表示する単一のプレゼンテーションテンプレートを含めることができます。 各検索では、同じトランスポートテンプレートまたはカスタムトランスポートテンプレートを使用して、プレゼンテーションレイヤーにデータを渡すことができます。

トランスポートテンプレートは、プレゼンテーションレイヤーにデータを渡す目的でのみ使用されるので、検索結果の表示に関連するHTMLはありません。 トランスポートテンプレートは、トランスポートテンプレートXMLタグを使用して、ファセット、パンくずリスト、メニューなどのガイド付き検索コンポーネントに入力するための検索結果を渡します。 これらのタグ内では、標準の検索テンプレートタグを使用して実際の値が表示されます。

詳しくは、プ [レゼンテーションまたは転送テンプレートの編集を参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>トランスポートテンプレートタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>プレゼンテーションレイヤーがトランスポートテンプレートから解析される内容を検出するために使用するルートXMLタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは、結果セットに基づいて概要データを提供する検索テンプレートタグを囲みます。 通常、これらのタグには、結果の合計数、結果の低さ、結果の高さに関する検索タグが含まれます。 次の例のように、汎用フィールドタグを使用して任意の数の追加のグ <span class="codeph"> ローバルフ </span> ィールドを定義できます。 </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;結果&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは検索結果の周囲に含まれるので、ガイド付き検索で検索する場所がわかります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;結果&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは各検索結果の周囲に含まれるので、1つの検索結果のコンテンツの開始と終了をガイド付き検索で認識できます。次に例を示します。 </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>複数の値を持つリスト内の各項目をループ処理して、1つの結果を得ることができます。 このタグは、結果内でのみ使用します。 次の例のように、結果フィールドに属する属性を繰り返し処理することが目的です。 </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;ファセット&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットを設定する結果を渡します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットは、動的ファセットとファセットパネルのメンバーの両方として指定できます。 ただし、関連するプレゼンテーションテンプレートタグに対する処理は独立しています。 </p> <p>つまり、動的なファセットのループコンテキスト内でファセットレールのループコンテキストをネストすることはできません。また、その逆も可能です。 </p> <p>動的ファセットと有料ファセットの両方の場合、特定の検索に対して返された動的ファセットのみが、ファセットパネルのループコンテキスト内に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> 各ファセットには独自のファセットタグがあり、nameパラメーターがファセット名と一致します。 検索タグは、次の例のように、ファセット値のファセットタグ内で使用されます。 </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> スロットファセットを使用するアカウントでは、動的タグと表示名タグを使用できます。 これらのタグは、ビジネスルールの作成時に、スロットファセットと実際のファセット間のマッピングを容易にするのに役立ちます。 </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>区切り <span class="codeph"> 文字 </span> 属性を使用すると、リストのsearch-display-fieldデータを出力する際に使用する区切り文字を変更できます。 デフォルトはコンマです。 </p> <p>一般に、使用する区切り文字は、フィールドのコンテンツに簡単に表示されないものにする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;サーチクエリ&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> 「Did You Mean」の提案をタグで囲み、ガイド付き検索でどのXMLノードに提案が含まれているかを認識します。 </p> <p><a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">「Did You Mean」について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;提案&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>次の例のように、各「Did You Mean」提案をタグで囲みます。 </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p><a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">「Did You Mean」について</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 検索テンプレートタグ {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

検索テンプレートは、サイト検索/マーチャンダイジングで定義されるテンプレートタグを含むHTMLファイルです。 これらのタグは、検索結果の形式を示します。 以下の参照に、各検索テンプレートタグとその属性の簡単な説明を示します。

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>トランスポートテンプレートファイル(.tpl)では、検索テンプレートタグのみを使用します。

以下の検索テンプレートタググループと参照マテリアルから選択できます。

結果ループ内でのみ有効なタグには、次のものが含まれます。

* [結果のループタグについて](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [結果のループ文字列タグ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [結果のループ条件タグ](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [結果のループアンカーリンクタグ](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [ループ位置の条件タグ](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

テンプレート全体で有効なタグには、次のものが含まれます。

* [フィールド値のリストタグ](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [フィールド値リストのループタグ](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [タグの提案](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [テンプレート文字列タグ](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [テンプレートアンカーリンクタグ](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [テンプレートの条件タグ](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [テンプレートフォームコントロールタグ](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

検索テンプレートの参照トピック

* [日付形式文字列](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [言語識別子](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [コンテンツタイプのHTTPヘッダーの指定](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [HTMLテンプレートでの文字セットの指定](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [XMLテンプレートでの文字セットの指定](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [検索テンプレートを別の検索テンプレートに含める](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## 結果のループタグについて {#section_D4DC7B4560144663972E8DBC3369C629}

結果のループタグは、テンプレートシステムの最も役に立ちます。 検索中にタグが見つかると、HTMLと、開始結果と終了結果の間にある他のタグがループタグで繰り返され、他のタグは検索結果に置き換えられます。

`<search-results> ... </search-results>`

結果のループタグは、検索結果を表示するHTMLを囲みます。 タグ間のHTMLは、結果ごとに繰り返され、ページに表示されます。

次のタグは、結果ループ内でのみ有効です。

* [結果のループ文字列タグ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [結果のループ条件タグ](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [結果のループアンカーリンクタグ](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [ループ位置の条件タグ](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## 結果のループ文字列タグ {#section_80D68334E8D04A33937A6E58ABAAA320}

次のタグは文字列を返します。

About [Results loop tagsを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果の数値インデックスを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のページタイトルを返します。 オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>ページの先頭から本文を返します。 関連キーワードは太字で表示されます。 オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 encoding属性はオプションで、出力文字をHTMLエンコーディング（デフォルト）、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 現在の結果の説明を返します。 meta descriptionタグが存在し、content属性が空でない場合は、そのテキストが表示されます。 それ以外の場合は、ページの本文の先頭が表示されます。 オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらでエンコードするかを、結果ページの出力用に制御します。 encodingのデフォルト値は <span class="codeph"> html </span> で <span class="codeph"> す </span>。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のスコア（0 ～ 100の数値）を返します。 オプション/メタデータ/定義の下にランクフィール <span class="uicontrol"> ド </span> を定義した場合は、ランク属性( <span class="uicontrol"> &lt;search-score="dynamic" rank </span> )を動的( <span class="uicontrol"></span><span class="codeph"></span>&lt;search-score="dynamic" rank)に設定して、動的ページランクを表示できます。 ランク属性を静的( <span class="codeph"> &lt;search-score rank="static"&gt; </span>)に設定すると、静的ページランクを表示できます。 オプションの精度属性を使用して、表示する小数点以下の桁数を指定できます。 デフォルト値は0（整数スコアを表示）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果の日付を返します。 現在の結果に関連付けられた日付がない場合は、オプションの「なし」テキスト値が表示されます。 オプションの「なし」値を指定しない場合、現在の結果に関連付けられた日付がない場合は、「日付なし」というテキストが表示されます。 </p> <p>「date-format」属性は、「%A, %B %d, %Y」（「Monday, July 25, 2016」の場合）などのUNIXスタイルの日付形式文字列を使用します。 "gmt"のデフォルト値は"yes"で、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 </p> <p>「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は「アカウントの言語を使用」を意味します。 「2」は「Use Document Language」を意味します。 「言語」の値「1」は、将来の使用のために予約されています。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 </p> <p>オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のサイズをバイト単位で返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のURLを返します。 </p> <p>オプションの長さ <span class="codeph"> 属性を </span> 使用して、表示する文字列の長さを制限します。デフォルトの文字数は無制限です。 </p> <p>encoding属性 <span class="codeph"> はオ </span> プションで、出力文字をHTMLエンコーディング、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のURLの疑問符を含む、パスとクエリ部分を返します。 </p> <p>オプションの長さ <span class="codeph"> 属性を </span> 使用して、表示する文字列の長さを制限します。デフォルトの文字数は無制限です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>検索語の次のコンテキスト行を返します。 関連キーワードは太字で表示されます。 このタグを繰り返し呼び出して、現在の結果に対して複数のコンテキスト行を表示します。 </p> <p>オプションの <span class="codeph"> length属 </span> 性を使用して、表示する文字列の長さを制限し、デフォルトの80文字にします。 長さ <span class="codeph"> 属性 </span> を含む&lt; <span class="codeph"> search-if-context&gt;タグまたは&lt; </span> search-if-any-context&gt;タグセットでこのタグが囲まれている場合、長さ属性は無視さ <span class="codeph"></span> れます。 </p> <p>encoding属性 <span class="codeph"> はオ </span> プションで、出力文字をHTMLエンコーディング（デフォルト）、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" comma="moles/kiles" separator="|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>この詳細タグは、現在の結果に対して、name属性で指定されたメタデータフィールド(url、title、desc、keys、target、body、alt、 <span class="uicontrol"> date、charset、language、language)の内容を表示し </span><span class="uicontrol"></span><span class="codeph"></span> ます。 次に例を示します。 </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>検索結果のページのタイトルを出力します。 オプションの <span class="codeph"> none属性 </span> を指定した場合、その値は、フィールドに関連付けられたコンテンツがない場合にのみ結果ページに表示されます。 </p> <p>日付 <span class="codeph"> 形式、 </span>gmt <span class="codeph"> 言語属性は、指定したフ </span> ィールドのコンテンツタイプが <span class="codeph"></span><span class="codeph"></span>dateの場合にのみ関連します。 </p> <p>日付 <span class="codeph"> 形式属 </span> 性は、 <span class="codeph"> %A、%B %d、%YなどのUNIX形式の日付形式文字列(2016年7月25 </span> 日月曜日)を使用します。 <span class="codeph"> gmtはデ </span> フォル <span class="codeph"> トで「はい」 </span> に設定され、日付文字列の時間部分をGMT(はい <span class="codeph"> )で出力するか、アカウントのタイムゾーン（いいえ）で出力するかを制御し </span><span class="codeph"></span>ます。 </p> <p>日付形式文 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 字列を参照してください</a>。 </p> <p>language属性 <span class="codeph"> は、 </span> 出力日付文字列の言語とロケールの規則を制御します。 <span class="codeph"> 0(デフ </span> ォルト)は「アカウントの言語を使用」を意味します。 <span class="codeph"> 2は、「ド </span> キュメントの言語を使用」を意味します。 言語 <span class="codeph"> 値1は、今 </span> 後の使用のた <span class="codeph"></span> めに予約されています)。 その他の言 <span class="codeph"> 語の </span> 値は、特定の言語識別子として解釈されます。例えば、 <span class="codeph"> en_USは「英語（米国） </span> 」を意味します。 </p> <p>言語識別 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 子を参照</a>。 </p> <p>オプション <span class="codeph"> のlength </span> 属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらでエンコードするかを、結果ページの出力用に制御します。 encodingのデフォルト値は <span class="codeph"> html </span> で <span class="codeph"> す </span>。 通常は、encoding属性を指定する必要はありません。 </p> <p>オプション <span class="codeph"> の引用 </span> 符属性は、出力される個々の項目を二重引用符で囲むか（encoding=perlの場合は一重引用符で囲むか） <span class="codeph"> を制御しま </span>す。 引用符のデフォルト値 <span class="codeph"> は「い </span> いえ」 <span class="codeph"> で </span>す。 </p> <p>オプションのコ <span class="codeph"> ンマ属 </span> 性では、個々の項目の出力をコンマで区切るかどうかを制御します。 コンマのデフォルト値 <span class="codeph"> は「は </span> い」 <span class="codeph"> です </span>。 リスト <span class="codeph"> タイプ以 </span> 外のフィールドでは、コンマ属性は無視されます。 </p> <p>オプションの <span class="codeph"> 単位属性は、 </span> 近接検索出力フィールドに適用される距離の単位を制御します。 単位のデフォルト値 <span class="codeph"> は、 </span> 指定した近接検索出力フィールドに関連付けられた位置タイプフィールドの「デフォルトの単位」設定から決定されます。 </p> <p>近接検索に <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> ついてを参照してください</a>。 </p> <p>オプション <span class="codeph"> のseparator </span> 属性は、リストタイプフィールドの出力値の間に挿入される1文字または区切り文字を定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt;...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の結果のメタデータフィールドの値(url、タイトル、説明、キー、target、body、alt、日付、文字セット、言語、またはオプション/メタデータ/定義で定義されたフィールド <span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span>)を列挙するループを作成します。 このタグを別の&lt;search-display-field-values&gt; <span class="codeph"> タグの中にネストしないでく </span> ださい。 name属性 <span class="codeph"> は、 </span> 列挙する値を含むフィールドの名前を指定します。 このタグは、オプション/メタデータ/定義の下にある「リストを許可」属性が <span class="uicontrol"> チェックされているフ </span> ィールド(オ <span class="uicontrol"> プション/メタデ </span> ータ <span class="uicontrol"> の下)で最も役 </span><span class="uicontrol"></span>に立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の <span class="uicontrol"> &lt;search-display-field-values&gt;ループのメタデータ値(url、title、desc、keys、target、body、alt、date、charset、language、language </span> fields <span class="uicontrol"> ( </span> Options/ <span class="uicontrol"> Metadata/ </span>Definitions <span class="codeph"></span> )を出力します。 このタグは、 <span class="codeph"> &lt;search-display-field-values&gt;ループ内でのみ有効 </span> です。 date <span class="codeph"> format, </span>gmt, <span class="codeph"> language属性は、 </span> &lt;search-display-values&gt; <span class="codeph"> nogusencing </span><span class="codeph"></span><span class="codeph"></span>date date <span class="codeph"> -format </span> 属性は、「 <span class="codeph"> %A, </span>%B <span class="codeph"> %B </span> %B <span class="codeph"></span><span class="codeph"></span>Nomday, July 25, 2016」のようなUNIX形式の日付形式文字列を使用します。 デフォルトで <span class="codeph"> は、 </span> 日付文字列の時間部分を「はい」に設定し、出力GMT( <span class="codeph"> yes)とアカウントのタイムゾーン( </span> no <span class="codeph"></span><span class="codeph"></span>no)のどちらにするかを制御します。 </p> <p>language属性 <span class="codeph"> は、 </span> 出力日付文字列の言語とロケールの規則を制御します。 <span class="codeph"> 0(デフ </span> ォルト)は「アカウントの言語を使用」を意味します。 その他の言 <span class="codeph"> 語の </span> 値は、特定の言語識別子として解釈されます。例えば、 <span class="codeph"> en_USは「英語（米国） </span> 」を意味します。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらでエンコードするかを、結果ページの出力用に制御します。 encodingのデフォルト値は <span class="codeph"> html </span> で <span class="codeph"> す </span>。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>name属性で指定されたメタデータフィールド(url、title、desc、keys、target、body、alt、date、charset、言語、または <span class="uicontrol"></span><span class="uicontrol"> Options </span> / <span class="uicontrol"> Metadata </span>&gt; Definitions)の現在の結果の値の合計数を出力します。 このタグは、結果ループの任意の場所に表示できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の <span class="codeph"> &lt;search-display-field-values&gt;ループの繰り返しの序数カウンタ（1、2、3など）を出 </span> 力します。 このタグは、 <span class="codeph"> &lt;search-display-field-values&gt;ループ内でのみ有効 </span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索に対して返される動的ファセットフィールドのループコンテキストを開始します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>このループの繰り返しに対して、現在の動的ファセットフィールドの名前を出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果の配置に関する情報を出力します。例えば、結果の位置に影響を与えた結果ベースのアクションなどです。 </p> <p>このタグの出力形式は、次の例のようにJSONです。 </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>encoding属 <span class="codeph"> 性は </span> オプションです。デフォルト値は <span class="codeph"> htmlで </span>す。 </p> <p> <p>注意： このタグは、コア検索クエ <span class="codeph"> リパラメーターでsp_trace=1 </span> が指定されている場合にのみ出力されます。 </p> </p> <p>バックエンド検索のCGIパラメーターの表の48 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> 行を参照してください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果のループ条件タグ {#section_35C367969E384A06A9865E388F1F9360}

次のタグは、HTMLを条件付きでそれらの間に含めます。

About [Results loop tagsを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt;...&lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt;...&lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、次に <span class="codeph"> &lt;search-title&gt;を呼び出して、ドキュメントタイトルからテキストを返す(または返さ </span> ない)場合、その間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; .../search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt;...&lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> これらのタグは、次に <span class="codeph"> &lt;search-description&gt;を呼び出して、ドキュメントの説明のテキストを返す(または返さ </span> ない)場合、タグ間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt;...&lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt;...&lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、次に <span class="codeph"> &lt;search-bodytext&gt;を呼び出して、ドキュメント本文からテキストを返す(または返さ </span> ない)場合、その間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ...&lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt;...&lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグの間には、次に <span class="codeph"> &lt;search-context&gt;を呼び出したときに空でないコンテキスト文字列が返さ </span> れた場合（または返されなかった場合）、HTMLが含まれます。 length属性は、囲まれた任意の <span class="codeph"> &lt;search-context&gt;タグのlength属性より優先さ </span> れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; .../search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt;...&lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果に関連付けられたコンテキスト文字列が存在する（または存在しない）場合、これらのタグの間にHTMLが含まれます。 length属性は、囲まれた任意の <span class="codeph"> &lt;search-context&gt;タグのlength属性より優先さ </span> れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt; ...&lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX upper=yy rank="dynamic/static"&gt; ...&lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のスコアがXXとYYの間（またはそうでない）の場合、これらのタグの間にHTMLが含まれます。 結果の関連性を示す箇条書きやグラフィックを追加する場合に便利です。 オプション/メタデータ <span class="uicontrol"> / </span> 定義の下にランクタイプフィールドを定義した場合、ランク属性を動的( <span class="uicontrol"> &lt;search-if-score rank="dynamic" lower=XX </span><span class="uicontrol"></span><span class="codeph"></span>YY upper=)に設定して、動的ページランクを確認できます。 ランク属性を静的( <span class="codeph"> &lt;search-if-score rank="static" lower=XX upper=YY&gt; </span>)に設定すると、静的ページランクを確認できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt;...&lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt;...&lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグには、「name」属性で指定したフィールドにコンテンツが含まれているかどうかに基づいて、それらの間にHTMLが含まれます。 オプションの「value」属性を指定した場合、指定した値が現在の結果のフィールドの値と一致する（または一致しない）かどうかに基づいて、タグ間のHTMLが含まれます。 これらのタグは、( <span class="codeph"> &lt;search-results&gt;タグと </span> &lt;/search-results&gt;タグの間の)結果ル <span class="codeph"> ープ内での </span> み機能します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果のループアンカーリンクタグ {#section_C5FAEF520E9E42ADAD1F90651922AA02}

About [Results loop tagsを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt; ...&lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのペアにより、それらの間にHTMLの周りにアンカーリンクが作成されます。 リンクをクリックすると、結果ページが表示されます。 オプションのtarget属性は、フレーム対応ブラウザーが結果ページを表示する名前の付いたウィンドウを指定します。 </p> <p>hbx-enable属性を「yes」に設定すると、HBXを通じて利用できる分析を利用できます。 hbx-linkid-nameを、追跡するメタデータフィールドの名前に設定します。 例えば、SKU番号別に検索結果を追跡するには、hbx-linkid-nameをSKU情報を含むメタデータフィールドの名前に設定します。 </p> <p>日付型フィールドは現在サポートされていません。 hbx-linkid-nameの値は、生成されたアンカーのリンクIDに追加されます。 この名前のメタデータフィールドが空の場合は常に、リンクIDにhbx-linkid-none属性の値が追加されます。 hbx-linkid-lengthの値は、Metaタグから取得および表示される文字数を制限します。 デフォルトの文字数は12です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...&lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのペアは、 <span class="codeph"> &lt;search-link&gt; ...&lt;/search-link&gt;タグを参照してく </span> ださい。 生成されたアンカーリンクをクリックすると、結果ページが表示されますが、結果の前に最も近いアンカータグまでスクロールされたページが表示されます。 PDFリンクの場合、Acrobatビューアに結果を含むページが表示されます。 オプションのtarget属性は、フレーム対応ブラウザーが結果ページを表示する名前の付いたウィンドウを指定します。 </p> <p>hbx-enable属性を「yes」に設定すると、HBXを通じて利用できる分析を利用できます。 hbx-linkid-nameを、追跡するメタデータフィールドの名前に設定します。 例えば、SKU番号別に検索結果を追跡するには、hbx-linkid-nameをSKU情報を含むメタデータフィールドの名前に設定します。 </p> <p>日付型フィールドは現在サポートされていません。 hbx-linkid-nameの値は、生成されたアンカーのリンクIDに追加されます。 この名前のメタデータフィールドが空の場合は常に、リンクIDにhbx-linkid-none属性の値が追加されます。 hbx-linkid-lengthの値は、Metaタグから取得および表示される文字数を制限します。 デフォルトの文字数は12です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt;...&lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt;...&lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果のURLの末尾と一致する拡張子がvalue属性で指定されている場合、これらのタグの間にHTMLが含まれます。 このタグは、リンクの拡張子に基づいて検索結果にグラフィックを含める場合に役立ちます。 value属性は、次のように1つ以上の拡張子（スペース区切り）のリストです。VALUE=".pdf"またはVALUE=".html .htm"。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ループ位置の条件タグ {#section_E0C29DDA09E043C9A396F36334F05EBB}

次のタグは、条件に応じてそれらの間にテキストを含めます。 これらは、「ループ」タグ内でのみ表示できます。&lt;お `search-results>` よび `<search-field-values>`。 結果セット内での現在の結果の位置をテストするために使用されます。

About [Results loop tagsを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt;...&lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt;...&lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果がページ上の最初の結果（またはそれ以外）の場合、または <span class="codeph"> &lt;search-results&gt;内で使用される場合は最初のフィールド値( </span>&lt;search-field-values&gt;内で使用される場合)の場合、これらのタグ間のテキストが含まれます <span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt;...&lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt;...&lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果がページ上の最後の結果（またはそれ以外）の場合、または <span class="codeph"> &lt;search-results&gt;内で使用される場合は最後のフィールド値( </span>&lt;search-field-values&gt;内で使用される場合)の場合、これらのタグ間のテキストが含まれます <span class="codeph"></span>。 このタグを使用して、結果の間に区切り文字を挿入できます。 例えば、次の例では、結果の間に <span class="codeph"> &lt;hr&gt;タグ </span> が挿入されます。 </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt;...&lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt;...&lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果がページ上の最初でも最後の結果でもない場合( <span class="codeph"> &lt;search-results&gt;内で使用される場合)、または最初でも最後のフィールド値でもない場合( </span>&lt;search-field-values&gt;内で使用される場合)、これらのタグ間のテキストが含まれます <span class="codeph"></span>。 タグのnotバージョンは、結果が最初か最後かをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt;...&lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt;...&lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在の結果がページ上の代替結果（または異なる）の場合はそれらの間のテキスト( <span class="codeph"> &lt;search-results&gt;内で使用される場合)、または代替フィールド値( </span>&lt;search-field-values&gt;内で使用される場合)が含まれま <span class="codeph"></span>す。 「代替」の結果は、ページ上の2番目、4番目、6番目などです。 次の使用例は、別のクラスを代替テーブル行に適用します。 &lt;search-lt&gt;と&lt;search-gt&gt;を使用して、 <span class="codeph"> &lt;search-if-alt&gt; </span> タグを&lt; <span class="codeph"> tr&gt;タグの中に"配置"できるよう </span><span class="codeph"></span><span class="codeph"></span> にします。 </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt;...&lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt;...&lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果が偶数の結果（または異なる）の場合、これらのタグの間のテキスト( <span class="codeph"> &lt;search-results&gt;内で使用される場合)、または偶数のフィールド値( </span>&lt;search-field-values&gt;内で使用される場合)が含まれます <span class="codeph"></span>。 検索結果の <span class="codeph"> &lt;search-index&gt;値が偶数の場合、検索結果は偶 </span> 数番号になります。 つまり、結果セット全体内での位置が偶数の場合。 これは、結果セット全体ではなく、ページ上の結果の位置をテ <span class="codeph"> ストする </span> &lt;search-if-alt&gt;とは異なる場合があります。 次の2つの表に違いを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### 最初のページ、sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>索引 </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
   <th colname="col3" class="entry"> <p>でも？ </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>最初の結果 </p> </td> 
   <td colname="col3"> <p>× </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>2番目の結果 </p> </td> 
   <td colname="col3"> <p>○ </p> </td> 
   <td colname="col4"> <p>○ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>3番目の結果 </p> </td> 
   <td colname="col3"> <p>× </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>4番目の結果 </p> </td> 
   <td colname="col3"> <p>○ </p> </td> 
   <td colname="col4"> <p>○ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>5番目の結果 </p> </td> 
   <td colname="col3"> <p>× </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
 </tbody> 
</table>

### 後のページ、sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>索引 </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
   <th colname="col3" class="entry"> <p>でも？ </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>10番目の結果 </p> </td> 
   <td colname="col3"> <p>○ </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>11番目の結果 </p> </td> 
   <td colname="col3"> <p>× </p> </td> 
   <td colname="col4"> <p>○ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>12番目の結果 </p> </td> 
   <td colname="col3"> <p>○ </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>13番目の結果 </p> </td> 
   <td colname="col3"> <p>× </p> </td> 
   <td colname="col4"> <p>○ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>14番目の結果 </p> </td> 
   <td colname="col3"> <p>○ </p> </td> 
   <td colname="col4"> <p>× </p> </td> 
  </tr> 
 </tbody> 
</table>

最後に、これは検索フ `<search-if-even>` ィールドの値と同じ `<search-if-alt>` です。これは、フィールドの値がページングされないためです。

## フィールド値のリストタグ {#section_D3298B5F976447DBA0032B883DCC91B1}

次の高度なタグは、検索結果のセット全体からフィールドの値と関連データを出力します。 これらのタグは、検索クエリの `sp-sfvl-field` CGIパラメータで指定されたフィールドに対してのみ出力されます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" commas="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-format=" gmt="yes/no"language="0/"0/javascript"enco/"enco/"enco/"enco/"e/html/" encoding"json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、結果セット全体の一意のフィールド値、値の数または結果の数のリストを表示します。 </p> <p>このタグは、検索クエリ内の <span class="codeph"> sp_sfvl_field </span> CGIパラメータで指定されたフィールドの出力のみを生成します。 オプションの「引用符」属性は、出力される個々の項目を二重引用符で囲むか（encoding=perlの場合は一重引用符で囲む）を制御します。 「引用符」のデフォルト値は「はい」です。 オプションの「コンマ」属性は、出力される個々の項目をコンマで区切るかどうかを制御します。 「コンマ」のデフォルト値は「はい」です。 オプションの「data」属性は、各一意のフィールド値を出力するか(data="values")、各一意のフィールド値の合計数を出力するか(data="counts")、または各一意の値を含む結果の数(data="results")を出力するかを制御します。 「data」のデフォルト値は「values」です。 リストタイプ以外のフィールドの場合、data="counts"とdata="results"は同等です。 セパレーター属性は、出力の値の間に挿入される1文字または区切り文字を定義します。 オプションの「sortby」属性で、出力の順序を制御します。sortby="none"は特定の順序を意味しません。sortby="values"はフィールド値（フィールドのSortingプロパティに従って昇順または降順）で並べ替え、sortby="counts"はフィールド値の数を降順で並べ替え、sortby="results"は各値を含む結果の数の降順で並べ替えを意味します。 </p> <p>sortby="counts"とsortby="results"は、リストタイプ以外のフィールドと同じです。 オプションの「max-items」属性では、出力する項目数を制限します。 デフォルト値の「max-items」は —1で、「output all items」を意味します。 </p> <p>最大項目数には絶対値100があります。 「date-format」、「gmt」および「language」属性は、指定したフィールドのコンテンツタイプが「date」の場合にのみ関連します。 「date-format」属性は、「%A, %B %d, %Y」（「Monday, July 25, 2016」の場合）などのUNIXスタイルの日付形式文字列を使用します。 "gmt"のデフォルト値は"yes"で、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 </p> <p>日付形式文 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 字列を参照してください</a>。 </p> <p>「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は「アカウントの言語を使用」を意味します。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 オプションの「encoding」属性は、出力文字列文字をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらでエンコードし、結果ページの出力用に出力するかを制御します。 デフォルト値の「encoding」は「html」です。 </p> <p>言語識別 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 子を参照</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、特定のsearch-field-value-listのカウント情報を表示します。 このタグの用途は3つあります。 「name」属性のみを指定した場合、このタグは、結果セット全体の名前付きフィールドの一意の値の数を出力します。 「name」と「value」の両方の属性を指定した場合、このタグは、結果セット全体（results="no"の場合）で指定された値の合計数か、結果セット全体（results="yes"の場合）で指定された値を含む結果の合計数を出力します。 デフォルト値の「results」は「no」です。 注意：リストタイプ以外のフィールドの場合、results="yes"とresults="no"は同等です。 「value」属性が指定されていない場合、「results」の値は無視されます。 このタグは、検索クエリ内のsp-sfvl-field <span class="codeph"> CGIパラメータで指定されたフィー </span> ルドの出力のみを生成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt;...&lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt;...&lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt;を指定された属性で同等に呼び出した場合（または呼び出した場合）、その間に </span> HTMLを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt;...&lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、指定された属性で <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt;を呼び出した場合（または呼び出さなかった場合）、それらのタグ間のコンテンツを表示します </span> 。 これは、通常、アカウントがファセットスロットを使用する場合に使用されます。 ファセットスロットでは、通常、値スロットは、関連付けられた名前スロットに単一の項目がある場合にのみ表示します。 トランスポートテンプレートでこのチェックを行う方が、プレゼンテーションレイヤーで行うよりも効率的です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## フィールド値リストのループタグ {#section_0717FA09F0FC449CB916883B0500A60E}

次の高度なタグは、ループ構文を使用して、検索結果のセット全体からフィールドの値と関連データを列挙し、出力します。 これらのタグは、検索クエリの `sp-sfvl-field` CGIパラメータで指定されたフィールドに対してのみ出力されます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ...&lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、結果セット全体内の特定のフィールドのフィールド値および関連データを列挙するループを作成します。 このタグを別の&lt;search-field-values&gt; <span class="codeph"> タグの中にネストしないでく </span> ださい。 "name"属性は、列挙する値を含むフィールドの名前を指定します。 オプションの「sortby」属性で、列挙順序を制御します。「なし」は特定の順序がないことを意味し、「値」はフィールド値（フィールドのSortingプロパティに従って昇順または降順）で並べ替え、「sortby="counts"はフィールド値カウントの降順で並べ替え、「sortby="results"」は各値を含む結果の数の降順で並べ替えます。 </p> <p>sortby="counts"とsortby="results"は、リストタイプ以外のフィールドと同じです。. オプションの「max-items」属性では、繰り返し回数を指定した値に制限します。 「max-items」のデフォルト値は —1で、「すべての値を列挙」を意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の&lt;search-field-values&gt;ループの繰り返しのフィールド値を出力します。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効 </span> です。 「date-format」、「gmt」および「language」属性は、含まれる&lt;search-field-values&gt;タグで指定されたフィールド名のコンテンツタイプが「date」の場合にのみ関連します。 「date-format」属性は、「%A, %B %d, %Y」（「Monday, July 25, 2020」の場合）などのUNIXスタイルの日付形式文字列を使用します。 </p> <p>日付形式文 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 字列を参照してください</a>。 </p> <p>オプションの「encoding」属性は、出力文字列文字をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらでエンコードし、結果ページの出力用に出力するかを制御します。 デフォルト値の「encoding」は「none」です。 通常は、encoding属性を指定する必要はありません。 "gmt"のデフォルト値は"yes"で、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は「アカウントの言語を使用」を意味します。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 </p> <p>言語識別 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 子を参照</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の&lt;search-field-values&gt;ループ <span class="codeph"> の繰り返しに関連付けられているカウントを </span> 出力します。 出力数は、フィールド値(results="yes")を含む結果セット全体の結果数か、結果セット全体のフィールド値の合計数です。 デフォルト値の「results」は「no」です。 </p> <p>リストタイプ以外のフィールドの場合、results="yes"とresults="no"は同等です。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効 </span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の&lt;search-field-values&gt;ループ <span class="codeph"> 反復の序数カウンタを出 </span> 力します。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効 </span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## タグの提案 {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

「Did you mean?」という意味で、ユーザーにわかりやすい内容の提案が表示されます。 別の検索用語を提案するサービス。 例えば、検索語のスペルを間違えた場合、「提案」は、正しいスペルを提案することで、検索結果を見つけるのに役立ちます。 また、ユーザが結果を見つけるのに役立つ関連キーワードを提案することもできます。 提案を生成する際、Suggestサービスは次の2つの辞書を使用します。1つはアカウントの言語(> >で設定 **[!UICONTROL Indexing]** )に基づ **[!UICONTROL Words and Languages]****[!UICONTROL Language]**&#x200B;き、もう1つはアカウントのインデックス内のキーワードから一意に構築されます。

>[!NOTE]
>
>Suggestサービスは、中国語、日本語、韓国語では機能しません。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-surgestions&gt;...&lt;/search-if-surgestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"> &lt;search-suggestion&gt;、&lt;search-suggestion-link&gt;などの「提案」テンプレートタグで囲み </span><span class="codeph"></span>ます。 検索で提案が生成されると、開始タグと終了タグの間のすべての情報が出力され、処理されます。 検索でサーチクエリが生成されない場合、ネストされたコンテンツは出力されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-surgestions&gt;...&lt;/search-surgestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、「提案」ループを生成します。このループには、提案された検索語句のリストが含まれます（例えば、「意図」、「意図」、「意図」など）。元々「意図」として入力されたクエリーに対して使用します。 キーワードのリストを生成する際、検索エンジンはネストされたHTMLタグやテンプレートタグを最大5回まで繰り返します。これは、サーチクエリの最大数です。 生成される提案の数(0 ～ 5)を指定するには、count属性を使用します。 </p> <p>&lt; <span class="codeph"> search-surgestions&gt;タグをペ </span> ージに複数回表示して、提案のリストを繰り返すことができます。 複数のサーチクエリは、各イールドの結果数に従って並べ替えられます。 </p> <p>&lt;search-surgestions&gt; <span class="codeph"> タグを開 </span> くタグと閉じる&lt;search-if-suggestions&gt;タグの間にネストし <span class="codeph"></span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt;...&lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、元のキーワードではなく、選択した推奨検索キーワードを使用して、元の検索クエリへのリンクを生成します。 このタグは、クラス、ターゲット、スタイルなどのHTML属性を受け取って、単純に出力します。 タグはURL属性も受け取ることができます。この値は、生成されたリンクのベースURLとして使用されます。 タグは、 <span class="codeph"> &lt;search-surgestions&gt;ループ内でのみ表示でき </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text/&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在提案されているクエリー用語を出力します（例えば、最初に「意図」として入力されたクエリーの「意図」）。 タグには属性がなく、 <span class="codeph"> &lt;search-surgestions&gt;ループ内でのみ使用でき </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-surgestions&gt;...&lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索で提案が生成されない場合、検索エンジンは開始タグと終了タグの間のすべての情報を出力し、処理します。 検索で提案が生成される場合、ネストされたコンテンツは出力されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-suggestion&gt;...&lt;/search-if[-not]-first-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの条件付きタグには、候補ループの最初のキーワードが推奨キーワードかどうかに基づいて、それらの間のHTMLが含まれます。 タグは、&lt;search-suggestion&gt;タグの開始タグと終了タグの間に <span class="codeph"> 表示する必要があ </span> ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-suggestion&gt;...&lt;/search-if[-not]-last-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの条件付きタグには、候補ループの最後のキーワードが推奨キーワードかどうかに基づいて、それらの間のHTMLが含まれます。 タグは、&lt;search-suggestion&gt;タグの開始タグと終了タグの間に <span class="codeph"> 表示する必要があ </span> ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在推奨されている検索語句の数値インデックスを返します。 タグは、&lt;search-suggestion&gt;タグの開始タグと終了タグの間に <span class="codeph"> 配置する必要があ </span> ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、生成された推奨検索用語の合計数を返します。 タグは、&lt;search-suggestion&gt;タグの開始タグと終了タグの間に <span class="codeph"> 配置する必要があ </span> ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、推奨検索用語の結果の合計数を返します。 タグは、&lt;search-suggestion&gt;タグの開始タグと終了タグの間に <span class="codeph"> 配置する必要があ </span> ります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレート文字列タグ {#section_67E3D529661F4F03A1FF469D9D658CAF}

次のタグは、テンプレート内のその時点でHTMLに文字列を出力します。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;検索本文&gt; </span> </p> </td> 
   <td colname="col2"> <p>「基本の外観」セクションで「テンプレート」リンクの下に設定される「検索リンクの色」設定を含むHTML bodyタグ。 結果ページに背景画像を表示するには、このタグにbackground属性を追加します。 このタグに追加されるカラー属性は、「基本外観」セクションで設定される「検索リンクの色」の設定よりも優先されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>「テンプレート」リンクの下の「基本的な外観」セクションで設定された、検索結果ヘッダーのHTML。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt;...&lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>search-cdataタグは、XMLタグと同等のXMLタグに置き換えられます。 <span class="codeph"> &lt;search-cdata&gt;は、 </span><span class="codeph"> &lt;![CDATA["と&lt;/search-cdata&gt;タグは" </span> ]&gt; <span class="codeph"></span>"に置き換えられます。 XMLパーサーは、openタグとcloseタグの間の情報を解析しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>訪問者が入力したクエリ。 詳細なオプションの「query-number」属性は、このタグによって出力される番号付きのクエリ文字列を制御します。 例えば、 <span class="codeph"> &lt;search-query query-number=1&gt;は、 </span> sp_q_1 <span class="codeph"> cgiパラメータの内容を出力し </span> ます。 「query-number」が指定されていない場合、またはquery-numberが「0」の場合は、メインのクエリ( <span class="codeph"> sp_q </span>)が出力されます。 オプションの「encoding」属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにするかを制御します。 デフォルト値の「encoding」は「html」です。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索の結果の合計数です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>このページでレポートされた結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>このページでレポートされた最初の結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>このページで最後にレポートされた結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>前のページでレポートされた結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>次のページに対してレポートされた結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;検索時刻&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索の時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>アカウント用に設定された検索ロゴのHTML（存在する場合）。 このロゴは、サイト検索/マーチャンダイジングにクレジットを与える画像です。 </p> <p>現時点では、ほとんどのアカウントに検索ロゴが関連付けられていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索の結果のコレクションです。 オプションの「all」属性を使用して、Webサイト全体を表すコレクションの名前を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt;...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォームの開始タグと終了タグを挿入します。 開始フォームタグにメソッドとアクションの属性を挿入します。 言語にdir="RTL"属性を含む追加の属性と、JavaScript関連の"name"属性と"onSubmit"属性を受け入れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>アカウント番号を指定するフォーム入力タグを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>ギャラリー番号を指定するフォームのinputタグを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>クエリ文字列を指定するフォーム入力タグを挿入します。 詳細なオプションの「query-number」属性は、フォームのinputタグに使用する番号付きのクエリを制御します。 例えば、 <span class="codeph"> &lt;search-input-query-number=1&gt;は、 </span> sp_q_1 <span class="codeph"> クエリのフォーム入力タグを出力し </span> ます。 「query-number」が指定されていない場合、または「query-number」が「0」の場合は、メインの <span class="codeph"> sp_qクエリの入力タグが挿入 </span> されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォームのselectタグと関連するHTMLを挿入し、コレクションの選択メニューを表示します。 オプションの「all」属性を使用して、Webサイト全体を表すコレクションの名前を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索テンプレートタグの1つを、他のHTMLまたはテンプレートタグ内の結果ページに挿入します。 <span class="codeph"> &lt;search-lt&gt;は、より小さ </span> い文字を挿入します。 &lt;search-lt&gt;と <span class="codeph"> &lt;search-gt&gt;を使用すると、タグの定義をエスケープ </span><span class="codeph"></span> して、検索テンプレートタグを属性値として使用できます。 検索に応答してテンプレートがレンダリングされると、&lt;search-lt&gt;タグが小なり記号(&lt;)に置き換え <span class="codeph"> られ </span> ます。 例えば、 <span class="codeph"> &lt;search-link&gt; </span> は <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt;と同じです </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索テンプレートタグの1つを、他のHTMLまたはテンプレートタグ内の結果ページに挿入します。 <span class="codeph"> &lt;search-gt&gt;は、より大き </span> い文字を挿入します。 &lt;search-lt&gt;と <span class="codeph"> &lt;search-gt&gt;を使用すると、タグの定義をエスケープ </span><span class="codeph"></span> し、他のテンプレートタグを属性値として使用できます。 検索に応答してテンプレートがレンダリングされると、 <span class="codeph"> &lt;search-gt&gt;タグが大なり記号(&gt;)に置き換えら </span> れます。 例えば、 <span class="codeph"> &lt;search-link&gt; </span> は <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt;と同じです </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の検索要求から「param-name」という名前のcgiパラメータの値を返します。 オプションの「encoding」属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにするかを制御します。 デフォルト値の「encoding」は「html」です。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>encoding属 <span class="codeph"> 性は </span> オプションです。デフォルト値は <span class="codeph"> jsonです </span>。 </p> <p> <p>注意： このタグは、コア検索クエ <span class="codeph"> リパラメーターでsp_trace=1 </span> が指定されている場合にのみ出力されます。 </p> </p> <p>バックエンド検索のCGIパラメーターの表の48 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> 行を参照してください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートアンカーリンクタグ {#section_3A51D27616C541E2B818CC52B2B856BA}

以下は、間のHTMLをアンカーリンクで囲むタグです。 アンカーリンクをクリックすると、別のページの結果が表示されます。 オプションの属性「count」は、表示するページ上で多くの結果が出るリクエストを数えます。 指定しなかった場合は、現在のページで要求された数が使用されます。 詳細なオプションの「URL」属性は、関連するリンクの転送先ドメインを制御します。 デフォルトではドメインは `https://search.atomz.com/search/`ですが、URL属性を使用して変更できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果の次または前のページを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果を日付順または関連性順に並べ替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>概要の表示/非表示を切り替えます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートの条件タグ {#section_18D9BC66DE484881932FD2F7EA9D170D}

HTMLを条件付きで含めることができるタグ。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt;...&lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt;...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページに検索結果が含まれている（または含まれていない）場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt;.../search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt;.../search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt;...&lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt;...&lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>前のページまたは次のページに結果が関連付けられている（または何も関連付けられていない）場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt;...&lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt;...&lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt;...&lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt;...&lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在のページが関連性または日付で並べ替えられた場合、またはそれ以外の場合にHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt;...&lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt;...&lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページで概要の表示/非表示を切り替えている場合、これらのタグにはHTMLが含まれます。 これらのタグを使用して、検索結果の一部を含めたり除外したりできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt;...&lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt;...&lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページの検索結果の生成でコレクションが指定されている場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt;...&lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt;...&lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索クエリにsp_advanced=1 <span class="codeph"> CGIパラメータが指定され </span> ている場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt;...&lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt;...&lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、指定したパラメーターが無効な場合、または無効でない場合、その間にHTMLを含めるか除外します。 </p> <p>現在、 <span class="codeph"> sp_q_location[_#]パラメータのみがサポ </span> ートされています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt;...&lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt;...&lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグには、「name」属性で指定されたCGIパラメーターが「value」属性で指定された値を持つかどうかに基づいて、それらの間のHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt;...&lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt;...&lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグは、現在のページが指定のフィールド名で並べ替えられている場合、またはそれ以外の場合、その間のHTMLを含みます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートフォームコントロールタグ {#section_45AFC414ACA74825B72FEAA8456F8DD2}

検索テンプレート上のチェックボックス、ラジオボタン、リストボックスのデフォルトの選択状態を制御す `<form>` るタグです。

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>タグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;input&gt;タグの代わりにテンプレートで <span class="codeph"> 使用さ </span> れます。 タグがブラウザに書き込まれると、「 <span class="codeph"> input」という単語が検索入力に置き換えら </span><span class="codeph"></span> れ、タグ内の他のすべての情報がそのまま出力されます。 また、タグで指定さ <span class="codeph"> れ </span> た名前がCGIパラメータとしてリストされ、タグで指定された値がそのCGIパラメータの値である場合は、 <span class="codeph"> checkedという語がタグの末尾に追加さ </span><span class="codeph"></span> れます。 このようにして、検索結果のデフォルトのラジオボタンまたはチェックボックスの状態を、現在のクエリと同じにすることができます。 </p> <p>例えば、チェックボックスのHTMLコードは次のようになります。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;サウンドに一致しません </span> </p> <p>このチェックボックスに対応するテンプレートコードは、次のとおりです。 </p> <p> <span class="codeph"> &lt;search-input type=checkbox name="sp_w" value="exact"&gt;一致するサウンドがありません </span> </p> <p>クエリのCGIパラメータ文字列に <span class="codeph"> sp_w=exactが含まれる場合、検索結果と共にブラウザに書き込まれるタグは次のようになります(チェックされた単語はタ </span><span class="codeph"></span> グの末尾に挿入されます)。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact" checked&gt;類似音の一致なし </span> </p> <p>クエリのCGIパラメータ文字列に <span class="codeph"> sp_w=exactが含まれていない場合、検索結果と共にブラウザに書き込まれるタグは次のようになります(チェックされた単語はタ </span><span class="codeph"></span> グに表示されません)。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;サウンドに一致しません </span> </p> <p>&lt;search- <span class="codeph"> input&gt;タグは、検 </span> 索テンプレートにチェックボックスやラジオボタンを配置する場合に便利です。 検索テンプレートの <span class="codeph"> &lt;form&gt;に追加するチェックボックスやラジオボタンが </span> ある場合は、 <span class="codeph"> &lt;input...&gt;の代わりに </span> &lt;search-input..&gt;を使用します <span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt;...&lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt;...&lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;form&gt;タグのコンボボックスは、 <span class="codeph"> &lt;select&gt; </span> タグで始まり、 <span class="codeph"> &lt;/select&gt; </span> タグで終 <span class="codeph"> わりま </span> す。 関連 <span class="codeph"> するCGI </span> パラメータの名前は、 <span class="codeph"> &lt;select&gt;タグ内に表示さ </span> れます。 &lt;select&gt;タ <span class="codeph"> グの後に </span> は、リストボックス内に表示する値を指 <span class="codeph"> 定 </span> する&lt;option&gt;タグのリストが表示されます。 </p> <p>&lt; <span class="codeph"> search-select&gt; </span>、 <span class="codeph"> &lt;/search-select&gt; 、 </span>&lt;search-option&gt; 、 <span class="codeph"> &lt;/search-option&gt;タグは、 </span><span class="codeph"></span><span class="codeph"></span> &lt;search-input-tag&gt;と同じ機能を提供します。 つまり、選択した単語は、ブラウザに対して自動的に&lt;option&gt;の末尾に追加されます。 <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> &lt;option&gt;の名前が、CGI&lt;select&gt;のタグが、CGIのタグが、CGIのタグが、CGIのパラメータが、CGIの値が、CGIのパラメータが、CGIの値が、検索 このようにして、検索結果内のデフォルトのリストボックス選択を、現在のクエリと同じにすることができます。 </p> <p>例えば、次のようなリストボックスが一般的です。 </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>このリストボックスの対応するテンプレートコードは、次のとおりです。 </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>検索テンプレートの&lt; <span class="codeph"> form&gt;に追加する場合は、 </span> &lt;select&gt; <span class="codeph"> &lt;select&gt; </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>&lt;select&gt;&lt;select&gt;&gt;&lt;select&gt;&lt;select&gt;&lt;select&gt;&lt;select&gt;&lt;select&gt;&lt;select&gt;検索オプション&lt;select&gt;検索&lt;select&gt;検索場所探索オプション&lt;./option&gt;を参照。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ...&lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグは、HTMLの周囲にアンカーリンクを作成します。 このアンカーをクリックすると、特定のフィールドで並べ替えられた結果のページが表示されます。 オプションの <span class="codeph"> count属 </span> 性では、結果ページに表示する結果の数を指定します。 countを省 <span class="codeph"> 略す </span> ると、現在のページで使用されている数が使用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 日付形式文字列 {#section_4BBDBBEF2B96414497617CD4B52D96E4}

次の変換指定を日付形式文字列で使用できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>日付形式文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p> 完全な曜日の名前を国内表現（例：「Monday」）に一致させます。 言語/単語と言 <span class="uicontrol"> 語/言 </span> 語の設 <span class="uicontrol"> 定によって、国 </span> 民の表現が決ま <span class="uicontrol"></span> ります。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> 曜日の略号を国単位で表したものに一致します。省略名は最初の3文字で、例えば「Mon」となります。 言語/単語と言 <span class="uicontrol"> 語/言 </span> 語の設 <span class="uicontrol"> 定によって、国 </span> 民の表現が決ま <span class="uicontrol"></span> ります。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> 完全な月名の国名表現に一致します（例：「June」）。 言語/単語と言 <span class="uicontrol"> 語/言 </span> 語の設 <span class="uicontrol"> 定によって、国 </span> 民の表現が決ま <span class="uicontrol"></span> ります。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> 月の略式名の国単位の表現に一致します。省略形は最初の3文字で、例えば「Jun」となります。 言語/単語と言 <span class="uicontrol"> 語/言 </span> 語の設 <span class="uicontrol"> 定によって、国 </span> 民の表現が決ま <span class="uicontrol"></span> ります。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>"%m/%d/%y"と同じです（例："07/25/13"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> 月の日付を10進数(01 ～ 31)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> 月の日付を10進数(1 ～ 31)で表します。 空白は1桁の前に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> 10進数(00 ～ 23)で24時間の時計に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> 月の略式名の国単位の表現に一致します。省略形は最初の3文字で、例えば「Jun」（%bと同じ）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> 10進数(01 ～ 12)で12時間の時計に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> 年の何日目かを10進数(001 ～ 366)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> （24時間形式の時計）を10進数(0 ～ 23)で表します。 空白は1桁の前に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> 10進数(1 ～ 12)で12時間の時計に一致します。 空白は1桁の前に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> 分を10進数(00 ～ 59)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> 月を10進数(01 ～ 12)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> 必要に応じて、「ante meridiem」または「post meridiem」の国別表現に一致します（例：「PM」）。 言語/単語と言 <span class="uicontrol"> 語/言 </span> 語の設 <span class="uicontrol"> 定によって、国 </span> 民の表現が決ま <span class="uicontrol"></span> ります。 </p> <p>単語と言 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 語についてを参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>"%H:%M"と同じです（例："13:23"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>"%I:%M:%S %p"と同じです（例："01:23:45 PM"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> 10進数(00 ～ 60)で2番目の値に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>"%H:%M:%S"と同じです（例："13:26:47"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> 年の週番号（日曜日を週の最初の日として）を10進数(00 ～ 53)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>"%e-%b-%Y"と同じです（例："2013年7月25日"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%はい </p> </td> 
   <td colname="col2"> <p> 世紀を10進数で表した年に一致します（例："2013"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> 世紀を含まない年を10進数(00 ～ 99)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> タイムゾーン名と一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> 一致する "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## 言語識別子 {#section_0490DECC00E34691ADE5A9ED90A6D911}

次の表に、サポートされている各言語の言語識別子を示します。 これらの識別子は、次のテンプレートタグでオプションの「言語」属性の値として使用できます。

* `search-date` および `search-display-field`.

   結果のル [ープ文字列タグを参照してくださ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)い。

* `search-field-value-list` フィールド [値のリストタグを参照してくださ](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)い。

* `search-field-value` フィールド [値リストのループタグを参照してくださ](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)い。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>言語 </p> </th> 
   <th colname="col2" class="entry"> <p>言語識別子 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ブルガリア語（ブルガリア） </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語（中国） </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語（香港） </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語（シンガポール） </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語（台湾） </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>チェコ語（チェコ共和国） </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>デンマーク語（デンマーク） </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>オランダ語 (ベルギー) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>オランダ語 (オランダ) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>英語（オーストラリア） </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>英語（カナダ） </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>英語（英国） </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>英語 (米国) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フランス語 (ベルギー) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フランス語（カナダ） </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> フィンランド語（フィンランド） </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フランス語 (フランス) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フランス語（スイス） </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ドイツ語（オーストリア） </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ドイツ語（ドイツ） </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ドイツ語（スイス） </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ギリシャ語（ギリシャ） </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アイルランドゲール語（アイルランド） </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>イタリア語 (イタリア) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本語（日本） </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>韓国語（韓国） </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ノルウェー語 (ノルウェー) </p> </td> 
   <td colname="col2"> <p> no_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ポーランド語（ポーランド） </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ポルトガル語（ブラジル） </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ポルトガル語（ポルトガル） </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ロシア語（旧ソ連） </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>スロバキア語（スロバキア） </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>スロバキア語（スロベニア） </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>スペイン語（メキシコ） </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>スペイン語（スペイン） </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>スウェーデン語 (スウェーデン) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## コンテンツタイプのHTTPヘッダーの指定 {#section_AEED823E9938448A9EDB2F286D9CFD90}

次のタグを使用して、Content-Type HTTP応答ヘッダーを指定できます。

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

属性と属 `content` 性はオ `charset` プションです。 このタグは、可能な限り早くテンプレートに表示されます。 また、またはの前に表示することもお勧めし `<search-html-meta-charset>` ます。こ `<search-xml-decl>`れらのタグの動作に影響するからです。

属性を指定しない場 `content` 合、の値は、 > `MIME-type` >で設定された値にデフォル **[!UICONTROL Settings]** ト設定さ **[!UICONTROL Crawling]** れます **[!UICONTROL Content Types]**。 属性を指定した場 `content` 合、その属性がタグのデフォル `content` ト属性として使用され `<search-html-meta-charset>` ます。

属性を指定しない場合、 `charset` ヘッダーに値 `charset` が書き込まれなくなり `content-type` ます。

を指定した場 `charset="1"` 合、の実際の値は `charset-name` CGIパ `sp_f` ラメータの値になります。 検索で `sp_f` CGIパラメーターが送信されない場合、の実際の値はアカウントの設 `charset-name` 定から読み取られます。 アカウントに関連付けられている文字セットは、 > > >で表 **[!UICONTROL Settings]** 示または **[!UICONTROL My Profile]** 変更で **[!UICONTROL Personal Information]** きます **[!UICONTROL Character Encoding]**。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

またはのように、特定の文字セット名を値としてリストするこ `charset` とで選択で `charset="iso-8859-1"` きます `charset="Shift-JIS"`。

属性を指定す `charset` ると、タグとタグのデフォル `charset` ト属性と `<search-html-meta-charset>` し `<search-xml-decl>` て使用され、ヘッダに出力され `content-type` ます。

## HTMLテンプレートでの文字セットの指定 {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

デフォルトのHTML検索結果テンプレートでは、次のタグを使用して、現在のアカウントに関連付けられた文字セットを指定します。

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

content属性とcharset属性はオプションです。 このタグは、テンプレートの「HTML」セクション `<head>` に表示する必要があります。 このタグは、テンプレートから生成されたHTMLページで次のタグになります。

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

content属性を指定しない場合、の実際の値は2つの値のいず `MIME-type` れかに設定されます。 タグで属 `<search-content-type-header>` 性が指定さ `content` れている場合は、その値が使用されます。 それ以外の場合、「>/」タブの値が使 **[!UICONTROL Templates]** 用さ **[!UICONTROL Settings]** れ **[!UICONTROL Content Type]** ます。

属性を指定しない場合、 `charset` の実際の値は2つの値のいず `charset-name` れかに設定されます。 タグで属 `<search-content-type-header>` 性が指定さ `charset` れている場合は、その値が使用されます。 それ以外の場合は、の実際の値がア `charset-name` カウントの設定から読み取られます。 アカウントに関連付けられている文字セットは、 > > >で表 **[!UICONTROL Settings]** 示または **[!UICONTROL My Profile]** 変更で **[!UICONTROL Personal Information]** きます **[!UICONTROL Character Encoding]**。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

を指定した場 `charset="1"` 合、の実際の値は `charset-name` CGIパ `sp_f` ラメータの値になります。 検索で `sp_f` CGIパラメータが送信されない場合、の実際の値は、タグで設定された値（指定された場合）またはアカウント設定で設定された値( `charset-name``<search-content-type-header>` その場合)になります。

に示すように、特定の文字セット名を指定できま `charset="charset-name"`す。 For example, `charset="iso-8859-1"` or `charset="Shift-JIS"`.

タグは `<search-html-meta-charset>` オプションです。 削除した場合、ブラウザーはのデフォルト値を `content-type`想定します。次に示します。 `content="text/html; charset=ISO-8859-1"`. また、タグを独自のタグに置き換え `<search-html-meta-charset>` ることもでき `http-equiv` ます。

## XMLテンプレートでの文字セットの指定 {#section_17DC31CDCC104F5F8081466B41A96E9D}

デフォルトのXML検索結果テンプレートでは、次のタグを使用して、現在のアカウントに関連付けられた文字セットを指定します。

`<search-xml-decl [charset="charset-name"]>`

属性は `charset` オプションです。 このタグは、テンプレートの上部で、タグの後に配置する必要があ `<search-content-type-header>` ります。 このタグは、テンプレートから生成されたXMLドキュメントで次のタグになります。

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

を指定しない場合、の実 `charset`際の値は2つの値のいず `charset-name` れかに設定されます。 属性を `<search-content-type-header>` 指定し `charset` た場合は、その値が使用されます。 それ以外の場合は、の実際の値がア `charset-name` カウントの設定から読み取られます。 アカウントに関連付けられている文字セットは、 > > >で表 **[!UICONTROL Settings]** 示または **[!UICONTROL My Profile]** 変更で **[!UICONTROL Personal Information]** きます **[!UICONTROL Character Encoding]**。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

を指定した場 `charset="1"` 合、の実際の値は `charset-name` CGIパ `sp_f` ラメータの値になります。 検索で `sp_f` CGIパラメータが送信されない場合、の実際の値は、タグで設定された値（指定された場合）またはアカウント設定で設定された値( `charset-name``<search-content-type-header>` その場合)になります。

必要に応じて、特定の文字セット名を指 `charset="charset-name"`定することができます。 例： `charset="iso-8859-1" or charset="Shift-JIS"`

タグを独自のタグに置き換え `<search-xml-decl>` ることもでき `?xml` ます。

## 検索テンプレートを別の検索テンプレートに含める {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

ある検索テンプレートを別の検索テンプレートに含めるには、 `<search-include>` タグを使用し、file属性を次の例のように、含めるテンプレートファイルの名前に設定します。

`<search-include file="seo/seo_search_title.tpl" />`

SEO検索テンプレートセグメントはサブフォル `seo/` ダーに、通常の検索テンプレートはサブフォルダーに含ま `templates/` れます。 このコンテキストに含めることができるのは.tplファイルだけです。

## Webサイト用の複数のトランスポートテンプレートの管理 {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

各領域に異なる検索トランスポートテンプレートを使用して、Webサイト全体での検索結果の外観を制御できます。

<!-- 

r_managing_multiple_templates.xml

 -->

この種の検索機能を実現するには、サイト検索/マーチャンダイジングでトランスポートテンプレートを管理します。 または、「公開」でトランスポートテンプレートを管理できます。 サイト検索/マーチャンダイジングと同様に、「公開」を使用すると、複数の検索トランスポートテンプレートを編集、プレビューおよび公開できます。

（デフォルト以外の）特定のトランスポートテンプレートを使用するように検索フォームを設定するには、クエリパラメータを使 `sp_t` 用します。 例えば、Webサイトのマークダウン販売エリアに「クリアランス」という検索テンプレートがあるとします。 標準のHTML検索フォームを使用し、次の追加のフォームコードを使用します。

`<input type=hidden name="sp_t" value="clearance">`

顧客がこのコード行を含む標準フォームをクリックすると、検索結果と共に「クリアランス」検索トランスポートテンプレートが表示されます。

「検索フォ [ームでのコレクションの使用」を参照してくださ](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)い。

詳しくは、フ [ォームでのフレームの使用を参照してくださ](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)い。

詳しくは、 [アドバンス検索フォームの例を参照してくださ](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)い。
