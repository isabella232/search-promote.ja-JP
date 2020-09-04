---
description: 'null'
seo-description: 'null'
seo-title: テンプレート一覧
solution: Target
title: テンプレート
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: ca4156f80d7dbb85d2d56b6caf7c0f560299d86e
workflow-type: tm+mt
source-wordcount: '15139'
ht-degree: 2%

---


# テンプレート{#templates}

## テンプレート{#concept_A5CFB6BD805D49459A96219AF1B17842}

## プレゼンテーションテンプレートタグ {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

プレゼンテーションテンプレート用のサイト検索/マーチャンダイジングタグと属性のリスト。


プレゼンテーションテンプレートは、サイト検索/マーチャンダイジングで定義されるプレゼンテーションテンプレートタグを含むHTMLファイルです。 これらのタグは、顧客に表示される検索結果の形式設定を示します。

テンプレート [についてを参照してください](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)。

次のプレゼンテーションタググループから選択できます。

* [宣言](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [結果](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [ファセット](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [パンくず](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [メニュー](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [パジェナブ](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [最近実行した検索](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [本気か？](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [オートコンプリート](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [格納](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [ゾーン](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [ループインジケータ](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [その他の言語](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## 宣言 {#section_82C5CA734D2941EB858FEFE3B695D2EC}

宣言は、トップレベルのプレゼンテーションテンプレートの最上部に設定できる特別なガイド付き宣言タグです。 これ以降の宣言（含まれるテンプレート内の宣言を含む）は無視されます。

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
   <td colname="col2"> <p>デフォルトでは、プレゼンテーションテンプレートはMIMEタイプがtext/htmlの状態で戻されます。 このタグで使用するcontent-typeは変更できます。 </p> <p>プレゼンテーションテンプレートで、このタグをできるだけ高く宣言します。 このタグを使用して、同じ行に他のテキストを追加しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> XMLを返す場合は、このタグを使用してXML宣言を作成できます。 このタグをプレゼンテーションテンプレートの最初の行にします。 このタグを使用する場合、最初の行で <span class="codeph"> &lt;guided-content-type-header&gt;を使用して上書きしない限り、content-typeは自動的にtext/xml </span> に設定されます。 文字セットを指定しない場合、デフォルトはUTF-8です。 このタグは、XMLドキュメントで次のように出力されます。 </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
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
   <td colname="col2"> <p>guided-resultsタグは、結果ループの境界を定義します。 gsname <span class="codeph"></span> 属性を指定すると、任意の結果セットにアクセスできます。 gsnameを指定しない場合 <span class="codeph"></span> は、デフォルトの検索結果が表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link [gsname="fieldname"] [attr="value"]+&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の結果へのリンクを作成するには、 <span class="codeph"> guided-result-link </span> タグを使用します。 gsname <span class="codeph"></span> 属性を定義すると、「search-url」を参照する標準の「loc」タグの代わりに、インデックスのフィールドを使用できます。 クラスやターゲットなど、他の属性も渡すことができ、結果のアンカータグに出力されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname" [attr="value"]+&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-result-img&gt; <span class="codeph"> タグは、生の </span><span class="codeph"></span> imgタグ内に変数を埋め込む代わりに、イメージタグを作成するのに役立ちます。 </p> <p>画像パスに使用するフィールドを <span class="codeph"> gsname </span> 属性で指定します。 結果は、 <span class="codeph"> img </span> タグと定義済みの標準HTML属性が渡されます。 次の例を見てみましょう。 </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname" [escape="html|url|json|ijson|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p> 結果に表示する情報は、 <span class="codeph"> &lt;guided-result-field&gt; </span> タグとして表示されます(&lt;guided-result-img&gt;タグなどの自動生成タグを使用する場合を除く <span class="codeph"></span> )。 </p> <p>「検索インデックス」フィールドの名前を「 <span class="codeph"> gsname」に指定し </span>ます。 渡された文字列と完全に一致するものがテンプレートに出力されます。 </p> <p>このフィールドをトランスポートテンプレートで指定したものとは異なる方法でエスケープする場合は、エスケープオプションを指定できます。 </p> <p>このエンコーディングは、トランスポートテンプレートで指定されたエンコーディングの上に適用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="fieldname&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件タグのセットは、表示する特定のフィールドにコンテンツがある場合にtrueになります。 コンテンツが存在しない場合、条件はfalseです。 タグを使用して、周囲のHTMLを表示するかどうか（値が存在しない場合）、または別の画像を表示するかどうか（その他）を決定できます。 </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
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
   <td colname="col2"> <p>列に結果を表示する場合、このタグは、現在の結果が列の終わりを示すかどうかを識別するために使用されます。 </p> <p>ブール条件がtrueの場合、HTMLが結果の末尾に追加され、行の最後に追加され、新しい行が開始されます。 最後の行の場合は、新しい行は開始されません。 </p> <p>そのタグの詳細につ <span class="codeph"> いては、&lt;guided-if-not-last&gt; </span> を参照してください。 </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
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
   <td colname="col2"> <p>バックエンド検索リクエストが結果を返した場合は1を返し、返さなかった場合は0を返します。 gsnameが指定されていない場合 <span class="codeph"></span> 、タグはプライマリ検索を指定するものと見なします。 このタグは、JavaScriptルーチンにロジックを渡す場合に役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットの結果の合計数を返します。 gsnameが指定されていない場合に、デフォルトの検索 <span class="codeph"> を行う </span> と想定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットに対して、ページ上で下位の結果の結果数を返します。 gsnameが指定されていない場合に、デフォルトの検索 <span class="codeph"> を行う </span> と想定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>指定した結果セットに対して、ページ上の上位の結果の結果数を返します。 gsnameが指定されていない場合に、デフォルトの検索 <span class="codeph"> を行う </span> と想定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not-results-found&amp;gt;&lt;/code> &lt;/p> &lt;/td>
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
   <td colname="col2"> <p>&lt; <span class="codeph"> guided-result-title&gt; </span><span class="codeph"></span> タグは、&lt;title&gt;トランスポートタグで指定されたタイトルトランスポートテンプレートフィールドの値を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt; <span class="codeph"> guided-result-description&gt; </span><span class="codeph"></span> タグは、&lt;description&gt;トランスポートタグで指定された説明トランスポートテンプレートフィールドの値を提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt; <span class="codeph"> guided-result-loc&gt; </span> タグは、 <span class="codeph"> &lt;loc&gt; </span> transportタグで指定されたloc transport templateフィールドの値を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Trueを指定すると、特定のフィールドに表示するコンテンツが含まれます。 コンテンツが存在しない場合、条件はfalseです。 タグを使用して、周囲のHTMLを表示するかどうか、値が存在しないか、別の画像を表示するかなどを決定します。 </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、トランスポートテンプレートで定義されているループスルー属性テーブルに <span class="codeph"> &lt;attribute_table&gt;トランスポートタグを </span> 付けます。 属性テーブルのフィールド値を表示する <span class="codeph"> ための&lt;guided-result-attribute-table-field&gt; </span> タグがあります。 ループ内で、プレーンな <span class="codeph"> guided-result-field </span> タグを使用して、他の結果フィールドを表示することもできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートでの定義に従って、属性テーブルのフィールドを表示します。 </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;
    gt;nbsp;&amp;lt;li&amp;&amp;nbsp;amp;&amp;sp;&amp;sp;;lt;a&amp;nbsp;href=&quot;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;
    &amp;&amp;nbmp;&amp;nbsp;&amp;nbsp;&amp;sp;;sp;amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;gt;nbsp;&amp;nbsp;&amp;nbsp;&amp;&lt;amp;>nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/>)&amp;nbsp;&amp;nbsp;lt;lt;li&amp;guided/result-amp&amp;
    
    
    
    
    
    
    
    amp;gt;lt&amp;lt;lt}
    
    &amp;lt;/guided-results&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の検索用のトランスポートテンプレートによって出力されるJSONデータの一般セクション内のトレースデータ内にあるトレース情報を出力します。 </p> <p>検索名を指定しない場合、 <span class="codeph"> デフォルト </span> と見なされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の検索結果のトランスポートテンプレートによって出力されたJSONデータの結果/トレース情報内のJSONコンテンツを出力します。 </p> <p>このタグは、 <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt;ループ内でのみ有効で </span> す。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ファセット {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

ファセットは、検索結果を詳細に調べるためのナビゲーションコンポーネントです。 ファセットタグを使用すると、プレゼンテーションテンプレートに様々なファセットを表示できます。 ファセットは名前で参照します。

ファセット [についてを参照してください](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)。

[「Facet Rail」について](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB)を参照してください。

動的ファセット [についてを参照してください](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)。

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
    <!--NEW 2/2/2014--> <p>任意の検索に対する動的ファセットのループコンテキスト。 </p> <p>&lt;guided-facet&gt; <span class="codeph"></span> プレゼンテーションテンプレートタグを編集し、gsname属性が <span class="codeph"></span> &lt;guided-dynamic-facets&gt;ループコンテキストによって自動的に提供されるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットの表示ラベルを返します。 </p> <p>ファセットでトランスポートテンプレートの <span class="codeph"> &lt;display-name&gt; </span> タグが使用されている場合、そのタグのコンテンツがラベルになります。 </p> </td> 
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
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>次のタグは、 <span class="codeph"> &lt;guided-facet-rail&gt; </span> タグ内の値が検索時に動的に決定され、適切に置き換えられる場合、gsname <span class="codeph"></span> 属性は必要ありません。 </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">ガイド・ファセット </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">guided-facet-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">ガイド付きファセット動作 </li> 
    </ul> <p>「 <span class="wintitle"> Facet Rail」 </span> ページの並べ替え条件によって、ファセットの位置が決まります。 並べ替え順は、「ファセットの並べ替えリスト」ドロップダウンメニューから選択できます。 </p> <p> 
     <!--NEW 02/27/2014-->このタグでは、 <span class="codeph"></span>_dynamic_facetsのgsname属性値をオプションで受け入れることができます。これにより、任意の動的ファセットに対してループコンテキストが提供され、検索に使用できます。 この事前定義されたファセットパネルは、Business Rulesユーザーインターフェイスにも表示され、ファセットパネル'_dynamic_facets'のアクション <span class="codeph"> プッシュファセットXをY </span>に配置できます。 </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">「Facet Rail」について</a>を参照してください。 </p> <p>動的ファセットにつ <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> いても参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" 60px <span class="varname"> " width=" 120px </span><span class="varname"></span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>ガイド付きファセット <span class="codeph"></span> タグを使用して、すべてのファセットタグが特定のファセットに関連付けられる領域を定義します。 また、このタグはブール型タグでもあり、ファセットに値が存在しない場合は、すべてのコンテンツを非表示にします。 この場合、ファセット値を出力するポイントはありません)。 </p> <p>高さと幅の属性はオプションで、サイズはピクセル単位(px)で指定します。 Visual Rule Builder(VRB)ではこれら2つの属性を使用し、ファセットが非表示の場合に、インタラクティブなプレースホルダーとして点線のボックスを表示します。 </p> <p> 表示名がファセット内にあり、ファセットが非表示の場合、その名前も非表示になります。 ただし、名前がファセットの外にある場合、 <span class="codeph"> ゾーンタグまたはGuided If Facet Visible </span><span class="codeph"></span> タグがファセットの周りに含まれている場合にのみ、名前を非表示にできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセット値の数が設定で定義されている長さのしきい値を超えている場合にtrueになります。 リストが長すぎる場合にファセットを別のUI要素(切り捨てられたリストやスクロールボックスなど)として表示するには、この関数を使用します。 </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
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
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"></span> ブロックのコンテキスト外でこの条件を使用することもできます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; </span> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセットが少なくとも1回クリックされ、現在ファセット値が選択されている場合にtrueになります。 ファセットがクリックされたかどうかに応じて、HTMLタグまたはgsタグの表示/非表示を切り替えるために使用されます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"></span> ブロックのコンテキスト外でこの条件を使用することもできます。 </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
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
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"></span> ブロックのコンテキスト外でこの条件を使用することもできます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットが複数選択の場合、この条件タグはtrueです。 タグを使用して、 <span class="codeph"> &lt;guided-facet-rail&gt;タグ </span> または&lt;guided-dynamic-facets&gt; <span class="codeph"></span> タグ内のファセットの表示を変更します。 </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;..
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values [gsname=" <span class="varname"> facetname </span>"]&gt;&lt;/guided-facet-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>これは、ファセット値ループイテレータタグです。 名前の付いた <span class="codeph"> ガイド付きファセット </span> ブロックのコンテキスト内で定義できます。この場合、 <span class="codeph"> gsnameは省略でき <span class="varname"></span></span>ます。 また、ガイド付きファセットブロックの外部で定義するこ <span class="codeph"> ともできますが、表示するファセット値のセットを指定するには、 </span> gsname <span class="codeph"><span class="varname"></span></span> 属性が必要になります。 </p> <p>また、このタグを使用して、名前付きの <span class="codeph"> ガイド付きファセット </span> ブロックのコンテキスト外にファセット値を表示することもできます。 gsname <span class="codeph"><span class="varname"> 属性を使用して、特定のファセットを直接参照し </span></span> ます。 </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のファセット値の文字列を出力します。 </p> <p>デフォルトでは、値はHTMLエスケープです。 値のエスケープ方法は、エスケープオプションを使用して変更できます。 </p> </td> 
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
   <td colname="col2"> <p>サイト訪問者がクリックするファセット値文字列を囲むリンクを作成します。 パスが自動的に生成され、現在のファセット値で結果が絞り込まれます。 アンカータグへの属性の直接渡しをサポートします。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>ファセット値が現在選択されている場合に、ファセット値の表示を変更します。 選択済みの場合は、ほとんどの場合、リンクできなくなります。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
<td colname="col2"> <p>ファセット値がゴースト値の場合に、ファセット値の表示を変更します。 ファセット値がゴースト値の場合、通常、ファセット値は斜体で表示され、その値が欠落しているか「ホスト化」されていることを示します。 </p> <p>次のコードの抜粋は、ファセットブロックの例です。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>特定のファセットに対して「元に戻す」リンクを表示します。 複数選択ファセットがある場合、このリンクは指定されたファセットの値のすべてを選択解除します。 ファセットに名前を付けます。 ファセットが現在選択されていない場合、リンクは現在のパスになります。 </p> <p>以下は、このタグの使用例です。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-long [gsname="facetname"]&gt; 
      &lt;guided-else-facet-long&gt;&lt;/guided-if-facet-long&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセット値の数が設定で定義されている長さのしきい値を超えている場合にtrueになります。 リストが長すぎる場合に、切り捨てられたリストやスクロールボックスなど、ファセットを別のユーザーインターフェイス要素として表示する場合に使用します。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
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
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"> ブロックのコンテキスト外でこの条件を使用することもで <span class="varname"></span></span> きます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件付きタグは、ファセットが少なくとも1回クリックされ、現在ファセット値が選択されている場合にtrueになります。 ファセットがクリックされたかどうかに応じて、HTMLタグまたはgsタグの表示/非表示を切り替えるために使用できます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"></span> ブロックのコンテキスト外でこの条件を使用することもできます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-single [gsname="facetname"]&gt; 
      &lt;guided-else-facet-single&gt;&lt;/guided-if-facet-single&gt; </code> </p> </td> 
   <td colname="col2"> <p>ファセット値が1つだけの場合、この条件付きタグはtrueです。 結果を絞り込む機能がない場合は、この関数を使用してファセットの表示を変更できます。 </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 属性を使用して特定のファセットを直接参照することで、名前付きの </span> ガイドファセット <span class="codeph"> ブロックのコンテキスト外でこの条件を使用することもで <span class="varname"></span></span> きます。 </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-has-values [gsname="facetname"]&gt; 
      &lt;guided-else-facet-has-values&gt;&lt;/guided-if-facet-has-values&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件を使用すると、指定したファセットに値がまったくないかどうかを確認できます。 空のファセットの代わりに別のファセットを表示する場合に使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定のファセット内の結果の合計数を出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> associated custom facet value </span>" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットに関連付けられている値の文字列を出力します。 ファセットには、0個以上のフィールドを関連付けることができます。 フィールドが関連付けられることはまれです。このような場合には、トランスポートテンプレートを設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> associated custom facet value </span>"/&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセット値に関連するフィールド値があるかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [attr=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>顧客がクリックできるファセット値文字列を囲むリンクを作成します。 パスが自動的に生成され、現在のファセット値で結果が絞り込まれます。 アンカータグへの属性の直接渡しをサポートします。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>&lt;guided-facet-values&gt; <span class="codeph"></span> で各ファセット値を繰り返し実行すると、このタグはネストされたファセットのすべての子値を繰り返し実行します。 このタグ内で、リンクの作成、元に戻すリンクの作成、ファセット値の表示に一般的なファセットタグを使用します。 入れ子にされたループが行われるので、このタグは <span class="codeph"> &lt;guided-facet-values&gt;内にある必要があ </span> ります。 </p> <p>このタグの使用例を次に示します。 </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
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
   <td colname="col2"> <p>現在のファセット値に子の値があるかどうかをテストします。 &lt;guided-facet-value-children&gt; <span class="codeph"></span> タグを使用する前にを使用することをお勧めします。 「else」句はオプションです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-above-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-above-length-threshold&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ファセット値ループ内の現在のファセット値が長さのしきい値を超えているかどうかを判定します。 通常は、長いファセットにしきい値を下回る値のみを表示する目的で使用されます（ユーザーが以前にファセットの下に表示される「詳細」リンクを選択した場合を除く）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length-threshold&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ファセット値ループ内の現在のファセット値が長さのしきい値と等しいかどうかを判定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の選択されたファセット値に対する元に戻すリンクを表示します。 これを使用して、選択したファセット値の横に「元に戻す」リンクを表示します。 この元に戻すリンクは、選択した特定の値を元に戻すだけなので、選択したすべての値の選択を解除する <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> とは異なります。 </p> <p> <p>注意： ファセットに複数選択の動作がない場合、2つの元に戻すリンクの動作は同じです。 つまり、ファセットには1つの選択された値しか含めることができません。 </p> </p> <p>ファセットが現在選択されていない場合、リンクは現在のパスになります。 このタグは、 <span class="codeph"> ガイド付きファセット値のループ内でのみ使用 </span> します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のファセット値の元に戻すリンクを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のファセットの元に戻すリンクを作成します。 </p> <p> &lt;guided-facet-undo-link&gt; <span class="codeph"></span> タグと同様ですが、独自の元に戻すリンクを作成するための生のパスを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-matches facetname="facetname" value="value"&gt;&lt;guided-else-facet-value-matches&gt; 
      &lt;/guided-if-facet-value-matches&gt; </code> </p> </td> 
   <td colname="col2"> <p>特定のファセットに選択された値または単一の値「値」が含まれる場合、条件に応じてHTMLを表示します。 このタグのセットは、多くの場合、別のファセットで選択した値に基づいてファセットを表示するのに使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>通常、共通、複数選択などのファセットの動作を決定します。 XML結果を受け取り、その動作に基づいてファセットの表示方法を動的に変更する必要がある顧客にとって役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>このタグで折り返されるコンテンツは、ファセットの表示状態に基づいて非表示または表示されます。 ビジネスルールでファセットを直接表示または非表示にした場合、ファセット内のコンテンツはすべて非表示になり、表示されます。 これらのタグをファセットで囲む必要はありません。 </p> <p> このタグの一般的な使用法は、表示名がファセットの外にある場合に表示名を非表示にすることです。 表示名の周りにこのタグを含めると、ファセットが非表示の場合に名前が表示されなくなります。 </p> <p>このタグは、ゾーンを置き換えるものであり、ゾーンを使用する場合と同じパフォーマンス上の利点を多数持ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## パンくず {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

パンくずリスト [についてを参照してください](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03)。

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
   <td colname="col2"> <p>パンくずリストのループタグ。 開始タグと終了タグの間のコンテンツは、現在の状態のクエリ番号ごとに反復されます。 </p> <p><span class="codeph"> gsnameを省略 <span class="varname"></span></span> した場合は、「default」という名前のパンくずリストが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>階層リンク内にリンクを作成します。 デフォルトの動作は「goto」動作です。 リンクの動作が異なる場合は、 <span class="codeph"> gsname <span class="varname"></span></span> optional属性を使用して「remove」または「drop」を指定します。 タグに含まれる属性は、結果のアンカータグに渡されます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>valueタグは、現在の階層リンクイテレーションの変換された値を出力します。 これは、 <span class="codeph"> ガイド付き階層リンク </span> ブロックのコンテキストでのみ使用されます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>labelタグは、階層リストの値のラベルを出力します。階層リストの値の詳細は、どのファセットが選択されたかによって示されます。 これは、 <span class="codeph"> ガイド付き階層リンク </span> ブロックのコンテキストでのみ使用されます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
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
   <td colname="col2"> <p>この条件付きタグは、現在の階層リンクの値にラベルが含まれている場合に、コンテンツを条件付きで表示するために使用されます。 ラベルが実際に存在する場合にのみ、ラベルを表示し、コンテンツを関連付けるために使用します。 これは、 <span class="codeph"> ガイド付き階層リンク </span> ブロックのコンテキストでのみ使用されます。 </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
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

メニュー [についてを参照してください](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32)。

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
   <td colname="col2"> <p>これは、メニュー値のループ反復子タグです。 gsname <span class="codeph"></span> 属性を使用して、表示するメニュー項目のセットを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link [attr="value"]+&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
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

## パジェナブ {#section_2EE397635C514BBC8D668278EA314F35}

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
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewwall|viewpages" [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>最初、前、次または最後のページへのリンクを作成します。 また、1つのページのすべてのページを表示するためのリンクを作成することもできます。 </p> </td> 
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
   <td colname="col2"> <p>現在繰り返し処理されているページが選択されている場合、この条件タグのセットはtrueです。 通常、ページナビゲーションコントロールにページ番号を別の形式で表示するために使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> 現在のページに前のページがある場合、この条件タグのセットはtrueです。 通常、前のリンクをページナビゲーションで表示する場合に使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> 現在のページに次のページがある場合、この条件タグのセットはtrueです。 通常、前のリンクをページナビゲーションで表示する場合に使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> 検索が大きな結果セットを返す場合、すべての結果を表示する機能をオファーしたくない場合があります。 したがって、この条件タグのセットを使用して、「すべての表示」リンクを表示するタイミングを決定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件タグのセットを使用して、表示ページのリンクを表示するタイミングを決定できます。 通常、これは顧客が特定のページを表示できるようにするために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>ページナビゲーションに最初のページ、前のページ、次のページなどがあるかどうかをテストします。 </p> </td> 
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
   <td colname="col2"> <p>ページナビゲーション設定が少ない場合は、 <span class="codeph"> ガイド付きページ編集 </span> タグを使用して、すべてのページネーションタグが特定のページネーション設定に関連付けられる領域を定義します。 </p> </td> 
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
   <td colname="col2"> <p>ページナビゲーションの最も低いページが同じかどうかをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果のページが1ページだけか、結果のページが複数かをテストします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 最近実行した検索 {#section_8CD907521F584257B475595B01A5964B}

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

「最近の検索の [設定](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562)」を参照してください。

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
   <td colname="col2"> <p>最近の検索に関する相対URLパスを、ガイド付きで最近検索したループ内で取得 <span class="codeph"> でき </span> ます。 通常は、 <span class="codeph"> guided-recent-search-linkを使用 </span>します。 ただし、独自のリンクを作成する場合は、このタグを使用できます。 次に例を示します。 </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>最近の検索に関連付けられたクエリ用語を取得できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link [attr="value"]+&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>顧客が最近保存した検索をクリアする機能をオファーできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>独自のリンクを作成できるように、 <span class="codeph"> &lt;guided-recent-searches-clear-link&gt; </span> で使用されるパスを返します。 </p> </td> 
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

検索で結果が返されず、検索語句がアカウントの辞書にない場合は、「あなたの平均」タグを使用して、提案への一連のリンクを作成できます。 次に、Did You Meanタグの使用例を示します。

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
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestions&gt;&lt;/guided-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>これは、サーチクエリに対してループを行うためのループタグです。 </p> </td> 
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
   <td colname="col2"> <p>サーチクエリへのパス文字列を返します。 独自のアンカータグを作成する場合に使用できます。 通常、代わりに <span class="codeph"> guided-suggestion-link </span> が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggetion/&gt; </span> </p> </td> 
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
   <td colname="col2"> <p>検索結果がゼロの場合にサーチクエリによる自動検索が実行されたかどうかをテストできます（この機能がオンの場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-クエリ/&gt; </span> </p> </td> 
   <td colname="col2"> <p>自動検索が実行された場合に、元のクエリを返します。 </p> <p>使用例： </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>結果の数が少ないことが原因で提案がある場合、この条件はtrueです。この機能がオンの場合に限ります。 </p> <p>次に、このタグの使用例を示します。 </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
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

次のタグを使用して、検索フォームにオートコンプリートを追加できます。 オートコンプリート機能を正しく行うには、head-contentタグとform-contentタグが必要です。 オートコンプリートのJavaScriptとCSSをプレゼンテーションテンプレートにハードコーディングするのではなく、タグを使用することをお勧めします。 これは、タグを使用すると、テンプレートを手動で更新することなく、オートコンプリート設定を変更した場合に、テンプレートで新しい敗北キャッシュIDをすべて取得できるからです。

オートコンプリート [についてを参照してください](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578)。

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
   <td colname="col2"> <p>オートコンプリート機能が有効かどうかを検出します。 タグを使用して、オートコンプリートに必要なヘッドおよびフォームコンテンツをオプションで取得できます。 これにより、この機能のオン/オフを切り替え、プレゼンテーションテンプレートを変更する必要がなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>プレゼンテーションテンプレートのheadで使用され、オートコンプリート用の適切なCSSスクリプトインクルードに置き換えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content/&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォーム内のオートコンプリートタグをハードコーディングする代わりに、プレゼンテーションテンプレートの検索フォーム( <span class="codeph"> &lt;form&gt; </span> タグと <span class="codeph"></span> &lt;/form&gt;タグの間)で使用されます。 タグは、オートコンプリート機能を動作させるために必要な適切なHTMLに置き換えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Autocomplete JavaScriptへのリンクを生成します。 最良のパフォーマンスを得るために、このタグをページの下部付近に配置してから、終了タグ「body」を付けることをお勧めします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 格納 {#section_A33E25DB5E67404A823BD9618665B773}

次のタグを使用して、ユーザーが現在入っているストアをテストし、表示します。

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
   <td colname="col2"> <p>ユーザーが <span class="codeph"> gsname </span> パラメーターで指定されたストアにいるかどうかを検出します。 </p> </td> 
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
   <td colname="col2"> <p>任意のコンテンツをゾーンタグで囲むと、その領域からゾーンを作成できます。 これにより、必要に応じて、ビジネスルールを使用してゾーンを表示できます。 既定では、ゾーンは常に表示されます。 オプションの検索パラメーターとファセットパラメーターを使用して、ゾーンに関連付けられている検索またはファセットを示すことができます。 この機能により、ゾーンが非表示の場合に検索またはファセットをスキップし、検索時間のパフォーマンスを向上させることができます。 高さと幅の属性はオプションです。ゾーンを削除した場合のVisual Rule Builderでのプレースホルダの表示方法を設定する際に使用します。 </p> <p> 可能な場合は、ゾーンの代わりに <span class="codeph"> guided-if-facet[-not]-visible </span> タグを使用します。 プレゼンテーションテンプレートが簡単になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグを使用すると、ゾーンが現在表示されている場合のテストが可能になります。 ゾーンを表示する場合にのみ表示したいコンテンツがページ上にある場合に便利です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ループインジケータ {#section_387322CA0AA843A2ACF2795C328673E9}

これらのループブロックでは、次の各ループインジケーターを使用できます。

* 誘導結果
* guided-facet-values
* 誘導パンくず
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
   <td colname="col2"> <p>この条件は、現在の繰り返しがループの最初の繰り返しである場合にtrueになります。 これは、最初の結果または最初のページを意味するわけではありませんが、最初のページが表示されます。 サイト訪問者が1ページにつき10回の結果セットの2ページ目にある場合、最初の反復は結果11になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の繰り返しがループの最後の繰り返しである場合にtrueになります。 これは、最後の結果または最後のページを意味するわけではなく、現在のコンテキスト（ページ）で最後に表示される結果を意味します。 サイト訪問者が、200件の結果を含み、1ページにつき10件の結果しかない結果セットの1ページ目にある場合、最後の反復は結果200ではなく結果10になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復がループの奇数の反復（偶数の反復に対する）の場合にtrueになります。 これは、行の様々な色を表示する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の繰り返しがループの偶数の繰り返し（奇数の繰り返しに対する）の場合にtrueになります。 これは、行の様々な色を表示する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復がループの偶数反復である場合にtrueになります。 これは、行の様々な色を表示する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初と最後のどちらでない場合に、その間のテキストを含めます。 </p> </td> 
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
   <td colname="col2"> <p>ループの繰り返しごとに値が増加する整数（0から始まる）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>ループの繰り返しごとに値が増加する整数（1から始まる）。 </p> </td> 
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
   <td colname="col2"> <p>現在使用されているパスが表示されます。 通常は、既存の検索に新しいパラメーターを追加するリンクを作成する際に使用します。 デフォルトでは、パスはURLエスケープされています。 使用するエスケープモードは、escapeパラメーターを使用して指定できます。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>この例では、検索処理ルールでlangを使用してフランス語のバージョンを選択しています。 </p> <p>現在のパスには、常に1つ以上のクエリパラメーターが含まれています。 他のクエリパラメーターが存在しない場合は、 <span class="codeph"> q=*に設定され </span> るので、より多くのパラメーターを追加しやすくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> 基本パス </span> </p> </td> 
   <td colname="col2"> <p> ベースパスを使用してリンクを作成する場合は、 <span class="codeph"> hrefの開始で「/」を使用し、パラメーター </span> を追加 <span class="codeph"></span> します。 </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-クエリ-param gsname="クエリパラメーター" [escape="html|url"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>URL上にあるクエリパラメーターの既存の値を取得できます。 パラメーターが存在しない場合、このタグは空の文字列を返します。 エスケープオプションを指定しない場合、返される文字列は自動的にHTMLエスケープされます。HTMLエスケープまたはURLエスケープのどちらかを指定できます。 </p> <p>例： </p> <p> 

    &amp;lt;guided-クエリ-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    gams&amp;nbsp;the&amp;nbsp;bants&amp;lt;guided-クエリ
    
    -param&amp;nbsname=&quot;lang&quot;&amp;sp/;&amp;gt;
    gevs&amp;nbsp;you&amp;nbsp;the&amp;nbsp;en
    
    &amp;lt;guided-クエリ-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/>
    gt;gevs&amp;nbamp;an&amp;sp;empt;nbsp;string
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-クエリ-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>ガイド付き検索には、階層リンクコントロールで使用されるクエリ番号の概念があります。 <span class="codeph"> guided-クエリ-param-name </span> を使用すると、プレゼンテーションテンプレート内のリンクの一部としてパラメーターを定義できます。この場合、ガイド付き検索で正しいクエリ番号が自動的に見つかります。 gsnameには「x」が含ま <span class="codeph"></span> れており、これがガイド付き検索で正しい番号に置き換えられます。 オフセット値は0 ～ 15の範囲で指定できます。0は次に使用可能なクエリ番号が使用されることを示します。 「1」は、1を追加することを示します。 </p> <p>ガイド付き <span class="codeph"> 現在のパスと組み合わせ </span>て、独自のミニファセットリンクを構築したり、追加のドリルダウンレベルを許可したりできます。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
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
   <td colname="col2"> <p> その他のテンプレートファイルを含めることができます。 つまり、サブテンプレートをモジュールとして使用して複数のテンプレートを作成できます。 </p> <p>次の例では、 <span class="filepath"> パンくずリスト </span> と <span class="filepath"> ファセット </span> ファイルが含まれています。 </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>動的なインクルードはサポートされていません。 つまり、gsfileを変数にすること <span class="codeph"></span> はできません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索に要した時間を示します。 返される検索時間の値はミリ秒単位で指定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索結果のページを作成するのに使用されるコア検索の数を返します。 </p> </td> 
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
   <td colname="col2"> <p>この条件は、現在の繰り返しがループの偶数の繰り返し（奇数の繰り返しに対する）の場合にtrueになります。 これは、行の様々な色を表示する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>この条件は、現在の反復がループの偶数反復である場合にtrueになります。 これは、行の様々な色を表示する場合に便利です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>現在の繰り返しが最初と最後のどちらでない場合に、その間のテキストを含めます。 </p> </td> 
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
   <td colname="col2"> <p>最初の検索を行っているかどうかを確認できます(クエリは、検索ボックスからの検索の結果でした)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグをテンプレートで使用すると、検索フォームのアクションをハードコーディングせずに保存できます。 ステージング済みまたはライブ環境にいる場合を検出し、それに応じて変更を行います。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-クエリ-param-defined gsname="クエリパラメーター"&gt; &lt;guided-else-クエリ-param-defined&gt; &lt;/guided-if-クエリ-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>この一連のタグを使用すると、検索パスで定義されているCGIパラメーターをテストできます。 パラメーターの値が定義されている場合にのみ、テストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-クエリ番号[gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>テンプレートを駆動するガイド付き検索エンジンは、エンジンが生成する新しいリンクごとに次に使用可能なクエリ番号を使用する「浮動クエリ番号」の概念を持ちます。 このタグを使用すると、次のクエリ番号またはオフセットを取得して、結果セットにドリルダウンするカスタムリンクを作成できます。 オフセットを使用すると、次のクエリ番号にオフセットできます。 例えば、1つのファセットを選択した場合、次のクエリ番号は2で、オフセットが1のクエリ番号は3になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>処理ルールで定義されているカスタム変数の既存の値を取得できます。 エスケープオプションを指定しない場合、返される文字列が自動的にHTMLエスケープされます。 <span class="codeph"> html、 </span>url、jsま <span class="codeph"> たは </span>0を指定できます <span class="codeph"></span><span class="codeph"></span>。 処理ルールを使用して受信CGIパラメーターをカスタム変数にコピーし、その変数をテンプレートに表示または使用する場合、エスケープ設定をnoneまたはjsに設定して、検索にXSS脆弱性を作成できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>処理ルール(クエリクリーニング、検索前処理、検索後処理)でカスタム変数が定義されているかどうかをテストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートで定義された一般的なフィールドの内容を表示できます。 エスケープオプションを指定しない場合、返される文字列は、そのフィールドのトランスポートテンプレートで指定した形式でエンコードされます。 エスケープオプションの指定は、トランスポートテンプレートと同様に、フィールドをエンコードしている形式の上に適用されます。 html、 <span class="codeph"> url js、js </span>、json <span class="codeph"> 、 </span>json、、または <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>0を指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>トランスポートテンプレートで定義された一般フィールドの内容が存在するかどうかをテストできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>cookieが使用可能であると仮定して、cookieの値を取得できます。 エスケープオプションを指定しない場合、返される文字列が自動的にHTMLエスケープされるように、html、url、js、json <span class="codeph"> 、jsonのいずれかを指定できます。これには、html、url escaped、json </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>、jsonのいずれかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cookieが存在するかどうかのテストを有効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area" [escape="html|url|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>特定の領域のバナーを出力します。 オプションのwidthとheightの属性は、ビジュアルルールビルダーで使用できます。これにより、意味のあるプレースホルダーを表示して、ユーザーがバナーを選択できるようになります。 デフォルトでは、バナーはエスケープされません。 代わりに、プレゼンテーションテンプレートにHTMLを挿入する必要があります。 ただし、JSONテンプレートを作成する場合は、jsエスケープオプションを使用することを検討してください。 </p> <p>例： </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
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
   <td colname="col2"> <p>シミュレーターまたはビジュアルルールビルダーで検索を表示している場合を検出できます。 通常は、追加のデバッグ情報を表示するために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p><span class="keyword"> Adobe Target </span> キャンペーンを参照するビジネスルールがあるかどうかを検出できます。 通常は、 <span class="keyword"> Adobe Targetとの統合の一環として使用され、不要な </span> ターゲット <span class="keyword"></span> サーバーに到達しないようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect/&gt; </span> </p> </td> 
   <td colname="col2"> <p>デフォルトでは、リダイレクトは自動的に実行されます。 ただし、WebアプリケーションにXMLまたはJSON応答を返すようにSite Search/Merchandisingを設定した場合は、Webアプリケーションで302/301応答を解析するか、結果セットの一部としてリダイレクトを渡すかを選択できます。 リダイレクトを結果セットの一部として渡す場合は、このタグをテンプレートで使用してリダイレクト場所を出力できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果セットにリダイレクトを返すようにSite Search/Merchandisingを設定した場合、このタグセットを使用して、出力へのリダイレクトがあるかどうかを判断できます。 </p> </td> 
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

## トランスポートテンプレートタグ {#reference_227D199F5A7248049BE1D405C0584751}

トランスポートテンプレートは、バックエンド検索からGuided Searchプレゼンテーションレイヤーにデータを渡すXMLテンプレートです。

<!-- 

r_transport_template_tags.xml

 -->

プレゼンテーションレイヤーには、複数の検索結果を表示する単一のプレゼンテーションテンプレートを用意することができます。 各検索では、同じトランスポートテンプレートまたはカスタムトランスポートテンプレートを使用して、プレゼンテーションレイヤーにデータを渡すことができます。

トランスポートテンプレートは、プレゼンテーションレイヤーにデータを渡す目的でのみ使用されるので、検索結果の表示に関連するHTMLはありません。 トランスポートテンプレートは、トランスポートテンプレートXMLタグを使用して、ファセット、パンくずリスト、メニューなどのガイド付き検索コンポーネントに入力するための検索結果を渡します。 これらのタグ内では、標準の検索テンプレートタグを使用して実際の値が表示されます。

「プレゼンテーションまたはトランスポートテンプレートの [編集](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)」を参照してください。

詳しくは、 [検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

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
   <td colname="col2"> <p>プレゼンテーションレイヤーがトランスポートテンプレートから解析される内容を検出するために使用するルートXMLタグです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは、結果セットに基づいて概要データを提供する検索テンプレートタグを囲みます。 通常、これらのタグには、検索結果の総数、低い結果、高い結果を得るための検索タグが含まれます。 次の例のように、 <span class="codeph"> 汎用フィールド </span> タグを使用して、任意の数の追加のグローバルフィールドを定義できます。 </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;結果&gt;&lt;/結果&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは検索結果に含まれるので、ガイド付き検索では検索場所がわかります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>タグは各検索結果に含まれるので、ガイド付き検索では、次の例のように、1つの検索結果開始のコンテンツのどこで終わるかが認識されます。 </p> <code class="syntax html"> &lt;results&gt; 
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
   <td colname="col2"> <p>複数値のリストで各項目をループ処理して1つの結果を得ることができます。 このタグは結果内でのみ使用します。 次の例のように、結果フィールドに属する属性を繰り返し処理できます。 </p> <code class="syntax html"> &lt;results&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;ファセット&gt;&lt;/ファセット&gt; </span> </p> </td> 
   <td colname="col2"> <p>ファセットを設定する結果を渡します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットを動的ファセットとして指定することも、ファセットパネルのメンバーとして指定することもできます。 ただし、関連するプレゼンテーションテンプレートタグに対する処理は独立しています。 </p> <p>つまり、動的なファセットループコンテキスト内でファセットパネルのループコンテキストをネストすることはできません。また、その逆もできません。 </p> <p>動的なファセットと有料のファセットの両方で、特定の検索に対して返された動的ファセットのみが、ファセットパネルのループコンテキスト内に表示されます。 </p> </td> 
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
     &lt;/facets&gt; </code> <p> スロットファセットを使用するアカウントでは、Dynamicタグと表示名タグを使用できます。 これらのタグはどちらも、ビジネスルールを作成する際に、スロット化されたファセットと実際のファセットのマッピングを容易にします。 </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>区切り文字 <span class="codeph"></span> 属性を使用すると、リスト用のsearch-display-fieldデータを出力する際に使用する区切り文字を変更できます。 デフォルトはコンマです。 </p> <p>通常、使用する区切り文字は、フィールドコンテンツに簡単に表示されないものにする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;サーチクエリ&gt;&lt;/surgestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> 「Did You Mean」の提案をタグで囲み、ガイド付き検索で、提案が含まれるXMLノードを認識できるようにします。 </p> <p><a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">「Did You Mean」について</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;サーチクエリ&gt;&lt;/サーチクエリ&gt; </span> </p> </td> 
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

検索テンプレートは、サイト検索/マーチャンダイジングで定義されるテンプレートタグを含むHTMLファイルです。 これらのタグは、検索結果の形式設定を示します。 次のリファレンスには、各検索テンプレートタグとその属性に関する簡単な説明が含まれています。

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>トランスポートテンプレートファイル(.tpl)では、検索テンプレートタグのみを使用します。

以下の検索テンプレートタググループと参照マテリアルから選択できます。

結果のループ内でのみ有効なタグには、次のものが含まれます。

* [結果のループタグについて](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [結果のループ文字列タグ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [結果のループの条件タグ](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [結果ループのアンカーリンクタグ](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [ループ位置の条件タグ](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

テンプレート全体で有効なタグには、次のものがあります。

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
* [検索テンプレートを別の](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## 結果のループタグについて {#section_D4DC7B4560144663972E8DBC3369C629}

結果のループタグは、テンプレートシステムの最も役立ちます。 検索中にタグが見つかると、HTMLが繰り返され、検索結果の開始タグと終了タグの間に他のタグが続きます。他のタグは検索結果に置き換えられます。

`<search-results> ... </search-results>`

結果のループタグは、検索結果を表示するHTMLを囲みます。 タグ間のHTMLが結果ごとに繰り返され、ページに表示されます。

次のタグは、結果ループ内でのみ有効です。

* [結果のループ文字列タグ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [結果のループの条件タグ](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [結果ループのアンカーリンクタグ](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [ループ位置の条件タグ](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## 結果のループ文字列タグ {#section_80D68334E8D04A33937A6E58ABAAA320}

次のタグは文字列を返します。

結果のループタグ [についてを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

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
   <td colname="col2"> <p>ページの先頭から始まる本文を返します。 関連する用語は太字で表示されます。 オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 encoding属性はオプションです。出力文字は、HTMLエンコーディング（デフォルト）、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 現在の結果の説明を返します。 meta descriptionタグが存在し、content属性が空でない場合は、そのテキストが表示されます。 それ以外の場合は、ページの本文の先頭が表示されます。 オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにエンコードするかを制御します。 エンコーディングのデフォルト値 <span class="codeph"> は </span> htmlで <span class="codeph"></span>す。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のスコア（0 ～ 100の数値）を返します。 オプション/ <span class="uicontrol"> メタデータ/ </span> 定義の下にランクフィールドを定義した場合 <span class="uicontrol"> 、ランク属性を動的( </span><span class="uicontrol"></span><span class="codeph"></span>&lt;search-score="dynamic" rank&gt; )に設定すると、動的ページランクを表示できます。 ランク属性を静的( <span class="codeph"> &lt;search-score rank="static"&gt; </span>)に設定すると、静的ページランクを表示できます。 オプションの精度属性を使用して、表示する小数点以下の桁数を指定できます。 デフォルトは0で、整数スコアが表示されます)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果の日付を返します。 現在の結果に日付が関連付けられていない場合は、オプションの「なし」テキスト値が表示されます。 オプションの「none」値を指定しない場合、現在の結果に日付が関連付けられていない場合は、テキスト「No Date」が表示されます。 </p> <p>「date-format」属性には、「%A, %B %d, %Y」などのUNIXスタイルの日付形式文字列（「2016年7月25日月曜日」の場合）を指定します。 "gmt"はデフォルトで"yes"に設定され、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 </p> <p>「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は、「アカウントの言語を使用」を意味します。 「2」は、「ドキュメント言語を使用」を意味します。 「言語」値「1」は、将来的に使用するために予約されています。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 </p> <p>オプションのlength属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のサイズをバイト単位で返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のURLを返します。 </p> <p>オプションの <span class="codeph"> 長さの </span> 属性を使用して、表示する文字列の長さを制限します。デフォルトの文字数は無制限です。 </p> <p>encoding <span class="codeph"></span> 属性はオプションです。出力文字は、HTMLエンコーディング、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-クエリの長さ="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のURLの疑問符を含むパスとクエリの部分を返します。 </p> <p>オプションの <span class="codeph"> 長さの </span> 属性を使用して、表示する文字列の長さを制限します。デフォルトの文字数は無制限です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>検索語句のコンテキストの次の行を返します。 関連する用語は太字で表示されます。 このタグを繰り返し呼び出して、現在の結果に対して複数のコンテキスト行を表示します。 </p> <p>オプションの <span class="codeph"> 長さの </span> 属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 このタグが、長さ属性を含む <span class="codeph"> &lt;search-if-context&gt; </span> または <span class="codeph"> &lt;search-if-any-context&gt; </span><span class="codeph"></span> タグセットで囲まれている場合、length属性は無視されます。 </p> <p>encoding <span class="codeph"></span> 属性はオプションです。出力文字をHTMLエンコーディング（デフォルト）、Javascriptエンコーディング、Perlエンコーディングまたはなしでエンコードできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" comma="miles/kiles" sepator="|"|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>この高度なタグは、現在の結果に対して、name <span class="uicontrol"> 属性に指定されたメタデータフィールド(url、タイトル、説明、キー、ターゲット、本文、alt、日付、文字セット、言語、またはフィールド)の内容を表示し </span><span class="uicontrol"></span><span class="codeph"></span> ます。 次に例を示します。 </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>検索結果のページのタイトルを出力します。 オプションで <span class="codeph"></span> none属性を指定した場合、その値は、フィールドに関連付けられたコンテンツがない場合にのみ結果ページに表示されます。 </p> <p><span class="codeph"> 日付形式、 </span>gmt、言語 <span class="codeph"> の属性は、指定したフィールドのコンテンツタイプが </span><span class="codeph"></span><span class="codeph"></span>dateである場合にのみ関連します。 </p> <p>日付形式 <span class="codeph"> の </span> 属性では、 <span class="codeph"> %A、%B %d、%YなどのUNIX形式の日付形式文字列(2016年7月25日（月） </span> が使用されます。 <span class="codeph"> gmt </span> はデフォルトで「 <span class="codeph"> yes」 </span> に設定され、日付文字列の時間部分をGMT( <span class="codeph"> yes)で出力するか(yes </span>)、アカウントのタイムゾーン(no <span class="codeph"></span>)で出力するかを制御します。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 日付形式文字列</a>を参照してください。 </p> <p>language <span class="codeph"></span> 属性は、出力日付文字列の言語とロケールの規則を制御します。 <span class="codeph"> 0 </span> （デフォルト）は、「アカウントの言語を使用」を意味します。 <span class="codeph"> 2は、「ドキュメント言語を使用」を </span> 意味します。 言 <span class="codeph"> 語 </span> 値 <span class="codeph"></span> 1は、将来的に使用するために予約されています)。 その他の <span class="codeph"> 言語の </span> 値は、特定の言語識別子として解釈されます。例えば、en_USは「英語（米国）」 <span class="codeph"></span> を意味します。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 言語識別子を参照してください</a>。 </p> <p>オプションの <span class="codeph"> length </span> 属性を使用して、表示する文字列の長さを制限します。デフォルトは80文字です。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにエンコードするかを制御します。 エンコーディングのデフォルト値 <span class="codeph"> は </span> htmlで <span class="codeph"></span>す。 通常は、encoding属性を指定する必要はありません。 </p> <p>オプションの <span class="codeph"> 引用符 </span> 属性は、出力される個々の項目を重複引用符で囲むかどうかを制御します( <span class="codeph"> encoding=perlの場合は一重引用符 </span>)。 引用符のデフォルト値 <span class="codeph"> は </span> noで <span class="codeph"></span>す。 </p> <p>オプションの <span class="codeph"> コンマ </span> 属性は、個々の項目の出力をコンマで区切るかどうかを制御します。 コンマのデフォルト値 <span class="codeph"> は </span> yesで <span class="codeph"></span>す。 カンマ <span class="codeph"></span> 属性は、リストタイプ以外のフィールドでは無視されます。 </p> <p>オプションの <span class="codeph"> 単位 </span> 属性は、近接検索出力フィールドに適用する距離の単位を制御します。 ユニットのデフォルト値 <span class="codeph"></span> は、指定した近接検索出力フィールドに関連付けられた位置タイプフィールドの「デフォルトのユニット」設定から決定されます。 </p> <p>近接検索 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> についてを参照してください</a>。 </p> <p>オプションの <span class="codeph"> separator </span> 属性は、リスト型フィールドの出力値の間に挿入される1文字（区切り文字）を定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt;...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の結果のメタデータフィールドの値(url、タイトル、説明、キー、ターゲット、本文、alt、日付、文字セット、言語、または <span class="uicontrol"> オプション </span> / <span class="uicontrol"> メタデータ </span> / <span class="uicontrol"> 定義 </span>で定義されたフィールド)を列挙するループを作成します。 このタグを別の <span class="codeph"> &lt;search-display-field-values&gt;タグの中にネストしないでくだ </span> さい。 name <span class="codeph"></span> 属性では、列挙する値が格納されているフィールドの名前を指定します。 このタグは、 <span class="uicontrol"> 許可リスト属性がチェックされているフィールド( </span> オプション/メタデータ/ <span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span>定義の下)で最も役立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の <span class="uicontrol"> &lt;search display-field-values&gt;ループのメタデータフィールドの値(url、タイトル、説明、キー、ターゲット、本文、alt、日付、文字セット、言語、または </span> オプション/ <span class="uicontrol"> メタデータ/ </span> 定義で定義されたフィールド <span class="uicontrol"></span><span class="codeph"></span> )を出力します。 このタグは、 <span class="codeph"> &lt;search-display-field-values&gt;ループ内でのみ有効 </span> です。 date-format、 <span class="codeph"> gmt、 </span>言語 <span class="codeph"> の各属性は、含まれる&lt;search display-field values&gt;タグに指定されているフィールド名の内容タイプがdateである場合にのみ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>有効です。 date-format <span class="codeph"> 属性は、 </span> "%A, <span class="codeph"> %B </span>%d, <span class="codeph"> %d </span><span class="codeph"></span><span class="codeph"></span>notday, 7月25, 2016"などのUNIXスタイルの日付形式文字列を取ります。 デフォルトの <span class="codeph"> gmt </span> 属性は <span class="codeph"> yesで、日付文字列の時間部分をGMT（はい）とアカウントのタイムゾーン( </span> no no in)のどちらに出力するかを制御 <span class="codeph"></span><span class="codeph"></span>します。 </p> <p>language <span class="codeph"></span> 属性は、出力日付文字列の言語とロケールの規則を制御します。 <span class="codeph"> 0 </span> （デフォルト）は、「アカウントの言語を使用」を意味します。 その他の <span class="codeph"> 言語の </span> 値は、特定の言語識別子として解釈されます。例えば、en_USは「英語（米国）」 <span class="codeph"></span> を意味します。 </p> <p>オプションの <span class="codeph"> encoding </span> 属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにエンコードするかを制御します。 エンコーディングのデフォルト値 <span class="codeph"> は </span> htmlで <span class="codeph"></span>す。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>name属性で指定したメタデータフィールド(url、タイトル、説明、キー、ターゲット、本文、alt、日付、文字セット、言語、または <span class="uicontrol"> オプション </span> / <span class="uicontrol"> メタデータ </span> / <span class="uicontrol"> 定義で定義されたフィールド </span>)の現在の結果の値の合計数を出力します。 このタグは、結果のループ内の任意の場所に含めることができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の <span class="codeph"> &lt;search-display-field-values&gt;ループ反復の序数カウンタ（1、2、3など）を出力し </span> ます。 このタグは、 <span class="codeph"> &lt;search-display-field-values&gt;ループ内でのみ有効 </span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索に対して返される動的ファセットフィールドのループコンテキストを開始します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>ループの反復で使用する、現在の動的ファセットフィールドの名前を出力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果の配置に関連する情報を出力します。例えば、結果の位置に影響を与えた結果ベースのアクションなどです。 </p> <p>このタグの出力形式は、次の例のようなJSONです。 </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>エン <span class="codeph"> コーディング </span> 属性はオプションです。デフォルト値は <span class="codeph"> htmlで </span>す。 </p> <p> <p>注意： このタグは、コア検索クエリのパラメーターで <span class="codeph"> sp_trace=1が指定さ </span> れている場合にのみ出力されます。 </p> </p> <p>バックエンド検索CGIパラメーターにある表の48行を参照して <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> ください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果のループの条件タグ {#section_35C367969E384A06A9865E388F1F9360}

以下のタグは、HTMLを条件付きでそれらの間に含めます。

結果のループタグ [についてを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ... &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ... &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、次に <span class="codeph"></span> &lt;search-title&gt;を呼び出すと、ドキュメントタイトルからテキストが返される（または返されない）場合、それらの間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ... &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> これらのタグは、次に <span class="codeph"></span> &lt;search-description&gt;を呼び出すと、ドキュメントの説明のテキストが返される（または返されない）場合、それらの間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt; ... &lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt; ... &lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、次に <span class="codeph"></span> &lt;search-bodytext&gt;を呼び出すと、ドキュメントの本文からテキストが返される（または返されない）場合、間のHTMLを含みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ... &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ... &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"></span> &lt;search-context&gt;を次に呼び出すと空でないコンテキスト文字列が返される（または返されない）場合、それらの間のHTMLを含みます。 length属性は、囲まれた <span class="codeph"> &lt;search-context&gt; </span> タグのlength属性よりも優先されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ... &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果に関連付けられたコンテキスト文字列が存在する（または存在しない）場合、これらのタグ間にHTMLが含まれます。 length属性は、囲まれた <span class="codeph"> &lt;search-context&gt; </span> タグのlength属性よりも優先されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt; ... &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX upper=yy rank="dynamic/static"&gt; ... &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果のスコアがXXとYYの間にある（またはない）場合、これらのタグには、それらの間のHTMLが含まれます。 結果の関連性を示す箇条書きやグラフィックを追加する場合に便利です。 オプション <span class="uicontrol"> / </span> メタデータ/ <span class="uicontrol"> 定義の下にランクタイプフィールドを定義した場合、ランク属性を動的( </span><span class="uicontrol"></span><span class="codeph"></span>&lt;search-if-score rank="dynamic" lower=XX=YY upper)に設定して、動的ページランクを確認できます。 ランク属性を静的( <span class="codeph"> &lt;search-if-score rank="static" lower=XX upper=YY&gt; </span>)に設定すると、静的ページランクを確認できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ... &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ... &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグには、「name」属性で指定したフィールドにコンテンツが含まれているかどうかに基づいて、間にHTMLが含まれます。 オプションの「value」属性を指定した場合、渡された値が現在の結果のフィールドの値と一致する（または一致しない）かどうかに基づいて、タグ間にHTMLが含まれます。 これらのタグは、結果のループ内( <span class="codeph"> &lt;search-results&gt; </span> タグと <span class="codeph"> &lt;/search-results&gt; </span> タグの間)でのみ機能します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果ループのアンカーリンクタグ {#section_C5FAEF520E9E42ADAD1F90651922AA02}

結果のループタグ [についてを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-linkターゲット="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt;.. &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのペアによって、タグ間のHTMLの周囲にアンカーリンクが作成されます。 リンクをクリックすると、結果ページが表示されます。 オプションのターゲット属性は、フレーム対応ブラウザが結果ページを表示する名前付きウィンドウを指定します。 </p> <p>hbx-enable属性を「yes」に設定すると、HBXで利用できる分析を利用できます。 hbx-linkid-nameを、追跡するメタデータフィールドの名前に設定します。 例えば、SKU番号で検索結果を追跡するには、hbx-linkid-nameを、SKU情報を含むメタデータフィールドの名前に設定します。 </p> <p>日付型フィールドは現在サポートされていません。 hbx-linkid-nameの値は、生成されたアンカー内のリンクIDに追加されます。 名前の付いたメタデータフィールドが空の場合は常に、リンクIDにhbx-linkid-none属性の値が追加されます。 hbx-linkid-lengthの値は、Metaタグから取得して表示する文字の数を制限します。 デフォルトの文字数は12です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-linkターゲット="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ... &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグのペアは、 <span class="codeph"> &lt;search-link&gt; ... &lt;/search-link&gt; </span> タグに似ています。 生成されたアンカーリンクをクリックすると、結果ページが表示されますが、結果の前に最も近いアンカータグまでスクロールされたページが表示されます。 PDFリンクの場合、Acrobatビューアに結果を含むページが表示されます。 オプションのターゲット属性は、フレーム対応ブラウザが結果ページを表示する名前付きウィンドウを指定します。 </p> <p>hbx-enable属性を「yes」に設定すると、HBXで利用できる分析を利用できます。 hbx-linkid-nameを、追跡するメタデータフィールドの名前に設定します。 例えば、SKU番号で検索結果を追跡するには、hbx-linkid-nameを、SKU情報を含むメタデータフィールドの名前に設定します。 </p> <p>日付型フィールドは現在サポートされていません。 hbx-linkid-nameの値は、生成されたアンカー内のリンクIDに追加されます。 名前の付いたメタデータフィールドが空の場合は常に、リンクIDにhbx-linkid-none属性の値が追加されます。 hbx-linkid-lengthの値は、Metaタグから取得して表示する文字の数を制限します。 デフォルトの文字数は12です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ... &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ... &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>value属性で結果のURLの末尾と一致する拡張子が指定されている場合、これらのタグには、それらの間のHTMLが含まれます。 このタグは、リンクの拡張に基づいて検索結果にグラフィックを含める場合に役立ちます。 value属性は、次のように1つ以上の拡張子（スペース区切り）のリストです。VALUE=".pdf"またはVALUE=".html .htm" </p> </td> 
  </tr> 
 </tbody> 
</table>

## ループ位置の条件タグ {#section_E0C29DDA09E043C9A396F36334F05EBB}

以下のタグは、条件に応じてそれらの間にテキストを含めます。 これらは、「ループ」タグ内でのみ表示できます。&lt; `search-results>` と `<search-field-values>`。 結果セット内の現在の結果の位置をテストするために使用されます。

結果のループタグ [についてを参照してください](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ... &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ... &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在の結果がページ上の最初の結果（またはそれ以外）の場合はそれらの間のテキストが含まれます( <span class="codeph"> &lt;search-results&gt;内で使用される場合 </span>)。または、最初のフィールド値( <span class="codeph"> &lt;search-field-values&gt;内で使用される場合) </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ... &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ... &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在の結果がページ上の最後の結果（またはそれ以外）の場合はそれらの間のテキストが含まれます( <span class="codeph"> &lt;search-results&gt;内で使用される場合 </span>)。または、最後のフィールド値( <span class="codeph"> &lt;search-field-values&gt;内で使用される場合) </span>。 このタグは、結果の間に区切りを挿入するのに使用できます。 例えば、次の例では、結果の間に <span class="codeph"> &lt;hr&gt; </span> タグが挿入されます。 </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ... &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ... &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の結果がページの最初でも最後の結果でもない場合( <span class="codeph"> &lt;search-results&gt;内で使用される場合)、または最初と最後のフィールド値でもない場合( </span>&lt;search-field-values&gt;内で使用される場合)、これらのタグ間のテキストが含まれ <span class="codeph"></span>ます。 タグのnotバージョンは、結果が最初か最後かをテストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ... &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ... &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在の結果がページ上の代替結果（またはそれ以外）の場合はそれらの間のテキストが含まれます( <span class="codeph"> &lt;search-results&gt;内で使用される場合 </span>)。または、代替フィールド値( <span class="codeph"> &lt;search-field-values&gt;内で使用される場合) </span>。 「代替」の結果は、ページ上の2番目、4番目、6番目などです。 次の使用例は、代替テーブル行に別のクラスを適用します。 &lt;search-lt&gt;と <span class="codeph"> &lt;search-gt&gt;を使用して、&lt;search-if-alt&gt; </span> タグを&lt;tr&gt;タグ内に"配置することを許可することに注意してくだ <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> さい。 </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ... &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ... &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在の結果が偶数の結果（またはそれ以外の結果）の場合はそれらの間のテキストが含まれます( <span class="codeph"> &lt;search-results&gt;内で使用される場合 </span>)。または、偶数のフィールド値( <span class="codeph"> &lt;search-field-values&gt;内で使用される場合) </span>。 検索結果の <span class="codeph"> &lt;search-index&gt; </span> 値が偶数の場合、検索結果は偶数になります。 つまり、結果セット全体内での位置が偶数の場合です。 これは、結果セット全体ではなく、ページ上の結果の位置をテストする <span class="codeph"> &lt;search-if-alt&gt; </span> とは異なる場合があります。 次の2つの表にその違いを示します。 </p> </td> 
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

最後に、フィールドの値 `<search-if-even>` はページ送信されないので、検索フィールド `<search-if-alt>` の値と常に同じ値になります。

## フィールド値のリストタグ {#section_D3298B5F976447DBA0032B883DCC91B1}

次の高度なタグは、フィールドの値と関連するデータを検索結果のセット全体から出力します。 これらのタグは、検索クエリの `sp-sfvl-field` CGIパラメーターで指定されたフィールドに対してのみ出力されます。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-language name="field-name" quotes="yes/no" commas="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format-string=" yes/no" language=" javascript=" enco/html/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、結果セット全体に含まれる一意のフィールド値、値の数または結果の数のリストを表示します。 </p> <p>このタグは、検索クエリの <span class="codeph"> sp_sfvl_field </span> CGIパラメータで指定されたフィールドの出力のみを生成します。 オプションの「引用符」属性は、出力される個々の項目を重複引用符で囲むかどうかを制御します（encoding=perlの場合は一重引用符）。 「quotes」のデフォルト値は「yes」です。 オプションの「コンマ」属性は、個々の項目の出力をコンマで区切るかどうかを制御します。 「コンマ」のデフォルト値は「yes」です。 オプションの「data」属性は、各固有フィールドの値を出力するか(data="values")、各固有フィールドの値の合計数を出力するか(data="counts")、各固有値を含む結果の数を出力するか(data="results")を制御します。 デフォルト値の「data」は「values」です。 リストタイプ以外のフィールドの場合、data="counts"とdata="results"は等価です。 separator属性は、出力の値の間に挿入される1文字または区切り文字を定義します。 オプションの「sortby」属性で、出力の順序を制御します。sortby="none"は特定の順序を意味しません。sortby="values"はフィールド値（フィールドのSortingプロパティに従って昇順または降順）で並べ替え、sortby="counts"はフィールド値のカウント順で並べ替え、sortby="results"は各値を含む結果の数の降順で並べ替えます。 </p> <p>sortby="counts"とsortby="results"は、リストタイプ以外のフィールドと同じです。 オプションの「max-items」属性では、出力する項目数を制限します。 デフォルト値の「max-items」は —1で、「output all items」を意味します。 </p> <p>最大アイテム数は100までに絶対制限されます。 「date-format」、「gmt」および「language」属性は、指定したフィールドのコンテンツタイプが「date」の場合にのみ有効です。 「date-format」属性には、「%A, %B %d, %Y」などのUNIXスタイルの日付形式文字列（「2016年7月25日月曜日」の場合）を指定します。 "gmt"はデフォルトで"yes"に設定され、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 日付形式文字列</a>を参照してください。 </p> <p>「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は、「アカウントの言語を使用」を意味します。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 オプションの「encoding」属性は、出力文字列文字をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらにエンコードするかを制御し、結果ページの出力に使用します。 デフォルト値の「encoding」は「html」です。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 言語識別子を参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-リストカウント名="フィールド名" value="フィールド値" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、特定のsearch-field-value-リストのカウント情報を表示します。 このタグには3つの用途があります。 「name」属性のみを指定した場合、このタグは、結果セット全体に含まれる名前付きフィールドの固有値の数を出力します。 「name」と「value」の両方の属性を指定した場合、このタグは、結果セット全体内の指定された値の合計数（results="no"の場合）または結果セット全体に指定された値を含む結果の合計数（results="yes"の場合）を出力します。 デフォルト値の「results」は「no」です。 注意：リストタイプ以外のフィールドの場合、results="yes"とresults="no"は等価です。 「value」属性を指定しない場合、「results」の値は無視されます。 このタグは、検索クエリの <span class="codeph"> sp-sfvl-field </span> CGIパラメータで指定されたフィールドの出力のみを生成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-field-リスト-count name="field-name" value="field-value"&gt; ... &lt;/search-if-field-value-リスト-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-field-value-count name="field-name" value="field-value"&gt; ... &lt;/search-if-not-field-value-リスト-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"></span> &lt;search-field-value-field-count name="field-name" value="field-value"&gt;を呼び出すと、指定された属性で0より大きい値が返される（または返されない）場合、その間のHTMLを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-field-count name="field-name"&gt; ... &lt;/search-if-single-field-value-リスト-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"></span> &lt;search-field-value-field-count name="field-name" value="field-value"&gt;を呼び出した場合に、指定された属性で1つの値が返される（または返されない）場合に、その間のコンテンツを表示します。 これは、通常、アカウントがファセットスロットを使用する場合に使用されます。 ファセットスロットの場合、通常は、関連付けられた名前スロットに単一の項目がある場合にのみ値スロットを表示します。 トランスポートテンプレートでこのチェックを行う方が、プレゼンテーションレイヤーで行うよりも効率的です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## フィールド値リストのループタグ {#section_0717FA09F0FC449CB916883B0500A60E}

次の高度なタグは、ループ構文を使用して、検索結果のセット全体からフィールドの値と関連するデータを列挙し、出力します。 これらのタグは、検索クエリの `sp-sfvl-field` CGIパラメーターで指定されたフィールドに対してのみ出力されます。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ... &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、結果セット全体に含まれる特定のフィールドのフィールド値と関連データを列挙するループを作成します。 このタグを別の <span class="codeph"> &lt;search-field-values&gt;タグの中にネストしないでくだ </span> さい。 "name"属性は、列挙する値が格納されているフィールドの名前を指定します。 オプションの「sortby」属性で、定義済みリストの順序を制御します。「なし」は特定の順序を持たないことを意味し、「値」はフィールドの値（Sortingプロパティに従って昇順または降順）で並べ替え、sortby="counts"はフィールドの値のカウント順で並べ替え、sortby="results"は各値を含む結果の数の降順で並べ替えます。 </p> <p>sortby="counts"とsortby="results"は、リストタイプ以外のフィールドと同じです。. オプションの「max-items」属性は、繰り返し回数を指定した値に制限します。 「max-items」のデフォルト値は —1です。これは、「すべての値を列挙」を意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の&lt;search-field-values&gt;ループ反復のフィールド値を出力します。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効で </span> す。 「date-format」、「gmt」および「language」属性は、含まれる&lt;search-field-values&gt;タグで指定されたフィールド名のコンテンツタイプが「date」の場合にのみ有効です。 「date-format」属性には、「%A, %B %d, %Y」などのUNIXスタイルの日付形式文字列（「Monday, July 25, 2020」の場合）を指定します。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 日付形式文字列</a>を参照してください。 </p> <p>オプションの「encoding」属性は、出力文字列文字をHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのどちらにエンコードするかを制御し、結果ページの出力に使用します。 デフォルト値の「encoding」は「none」です。 通常は、encoding属性を指定する必要はありません。 "gmt"はデフォルトで"yes"に設定され、日付文字列の時間部分をGMT("yes")で出力するか、アカウントのタイムゾーン("no")で出力するかを制御します。 「language」属性は、出力日付文字列の言語とロケールの規則を制御します。 「0」（デフォルト）は、「アカウントの言語を使用」を意味します。 その他の「言語」値は、特定の言語識別子として解釈されます。例えば、「en_US」は「英語（米国）」を意味します。 </p> <p>詳しくは、 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 言語識別子を参照してください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の <span class="codeph"> &lt;search-field-values&gt;ループの反復に関連付けられているカウントを出力し </span> ます。 出力数は、フィールド値を含む結果セット全体の結果数(results="yes")か、結果セット全体のフィールド値の合計数です。 デフォルト値の「results」は「no」です。 </p> <p>リストタイプ以外のフィールドの場合、results="yes"とresults="no"は等価です。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効で </span> す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在の <span class="codeph"> &lt;search-field-values&gt;ループ反復の序数カウンターを出力し </span> ます。 このタグは、 <span class="codeph"> &lt;search-field-values&gt;ループ内でのみ有効で </span> す。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## タグの提案 {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

「ご意味は？」というメッセージが表示され、ユーザーにわかりやすく表示されます。 別の検索用語を提案するサービスです。 例えば、検索語のスペルを間違えた場合、「修正候補」は、正しいスペルを提案して結果を探すのに役立ちます。 システムは、ユーザが結果を見つけるのに役立つ関連キーワードを提案することもできます。 サーチクエリを生成する際、Suggestサービスでは次の2つの辞書が使用されます。1つはアカウントの言語( **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]****[!UICONTROL Language]**>で設定)に基づいており、もう1つはアカウントインデックスのキーワードから一意に作成されたものです。

>[!NOTE]
>
>Suggestサービスは、中国語、日本語または韓国語では機能しません。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-surgessions&gt; ... &lt;/search-if-surgessions&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、 <span class="codeph"> &lt;search-suggestion&gt; </span>、&lt;search-suggestion-link&gt;などの「提案」テンプレートタグで囲み <span class="codeph"></span>ます。 サーチクエリが生成された場合、検索エンジンはopenタグとcloseタグの間のすべてを出力して処理します。 検索でサーチクエリが生成されない場合、ネストされたコンテンツは1つも出力されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-surgessions&gt; ... &lt;/search-surgestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、「提案」ループを生成します。このループには、推奨検索用語(「意図」、「意図」、「意図」など、元々「意図」として入力されたクエリ用)のリストが含まれます。 キーワードのリストを生成する際、検索エンジンはネストされたHTMLタグやテンプレートタグを最大5回まで繰り返します。これはサーチクエリの最大数です。 生成される提案の数(0 ～ 5)を指定するには、count属性を使用します。 </p> <p>ページに <span class="codeph"> &lt;search-surgessions&gt; </span> タグを複数回表示して、サーチクエリのリストを繰り返すことができます。 複数の提案は、各結果の結果数に従って並べ替えられます。 </p> <p>&lt;search-suggestions&gt; <span class="codeph"> タグを開いたタグと閉じた </span> &lt;search-if-suggestions&gt; <span class="codeph"></span> タグの間にネストします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt; ... &lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、元の検索語ではなく、選択した推奨検索語句を使用して、元の検索クエリへのリンクを生成します。 このタグは、クラス、ターゲット、スタイルなどのHTML属性を受け取って、単純に出力します。 タグにはURL属性も指定できます。この値は、生成されたリンクのベースURLとして使用されます。 タグは、 <span class="codeph"> &lt;search-suggestions&gt;ループ内でのみ使用でき </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text/&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在提案されているクエリ用語(例えば、クエリの「意図」が元々「意図」として入力された場合)を出力します。 タグには属性がなく、 <span class="codeph"> &lt;search-suggestions&gt;ループ内でのみ使用でき </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggessions&gt; ... &lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>サーチクエリが生成されない場合、検索エンジンは開始タグと終了タグの間のすべてを出力して処理します。 サーチクエリが生成された場合、ネストされたコンテンツは1つも出力されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-suggestion&gt; ... &lt;/search-if[-not]-first-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの条件タグには、候補ループの最初のキーワードが推奨キーワードであるかどうかに基づいて、それらのキーワード間にHTMLが含まれます。 タグは、開いたタグと閉じた <span class="codeph"> &lt;search-suggestion&gt;タグの間に表示する必要があり </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-suggestion&gt; ... &lt;/search-if[-not]-last-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの条件タグには、候補ループの最後のキーワードが候補と見なされるかどうかに基づいて、それらの間にHTMLが含まれます。 タグは、開いたタグと閉じた <span class="codeph"> &lt;search-suggestion&gt;タグの間に表示する必要があり </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、現在推奨されている検索用語の数値インデックスを返します。 タグは、&lt;search-suggestion&gt;タグを開くタグと閉じるタグの間に含める必要があり <span class="codeph"> ま </span> す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、生成された推奨検索用語の総数を返します。 タグは、&lt;search-suggestion&gt;タグを開くタグと閉じるタグの間に含める必要があり <span class="codeph"> ま </span> す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>このタグは、推奨された検索用語の検索結果の合計数を返します。 タグは、&lt;search-suggestion&gt;タグを開くタグと閉じるタグの間に含める必要があり <span class="codeph"> ま </span> す。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>「基本外観」セクションで「テンプレート」リンクの下に設定される、検索リンクの色の設定を含むHTMLのbodyタグ。 結果ページに追加背景画像を表示するための、このタグのbackground属性。 このタグに追加される色属性は、基本ルックセクションで設定される検索リンクの色設定よりも優先されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>テンプレートリンクの下の基本的な外観セクションに設定された、検索結果ヘッダーのHTML。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt; ... &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>search-cdataタグは、XMLタグに置き換えられます。 <span class="codeph"> &lt;search-cdata&gt; </span><span class="codeph"> は、&lt;![CDATA["と&lt;/search-cdata&gt; </span> タグは" <span class="codeph"> ]&gt; </span>"に置き換えます。 XMLパーサーは、openタグとcloseタグの間の情報を解析しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-クエリクエリ番号="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>訪問者が入力したクエリ。 高度でオプションの「クエリ番号」属性は、このタグで出力される番号付きクエリ文字列を制御します。 例えば、 <span class="codeph"> &lt;search-クエリクエリ番号=1&gt;は、 </span> sp_q_1の <span class="codeph"></span> cgiパラメータの内容を出力します。 「クエリ番号」を指定しない場合、またはクエリ番号が「0」の場合は、メインクエリ( <span class="codeph"> sp_q </span>)が出力されます。 オプションの「encoding」属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにエンコードするかを制御します。 デフォルト値の「encoding」は「html」です。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索の結果の合計数です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>このページでレポートされる結果の数。 </p> </td> 
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
   <td colname="col2"> <p>次のページに対してレポートされる結果の数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;検索時間&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索にかかる時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>アカウント用に設定されている検索ロゴのHTML（存在する場合）。 このロゴは、サイトの検索/マーチャンダイジングにクレジットを与える画像です。 </p> <p>現時点では、ほとんどのアカウントに検索ロゴが関連付けられていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>この検索の結果のコレクション。 オプションの「all」属性を使用して、Webサイト全体を表すコレクションの名前を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt;...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォームの開始タグと終了タグを挿入します。 開始フォームタグにメソッドおよびアクション属性を挿入します。 言語にdir="RTL"属性を含む追加の属性と、JavaScript関連の"name"属性と"onSubmit"属性を受け入れます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>アカウント番号を指定するフォーム入力タグを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>ギャラリー番号を指定するフォーム入力タグを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-クエリクエリ番号="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>クエリ文字列を指定するフォーム入力タグを挿入します。 高度なオプションの「クエリ番号」属性は、フォーム入力タグに使用する番号付きクエリを制御します。 例えば、 <span class="codeph"> &lt;search-input-クエリクエリ番号=1&gt;は、 </span> sp_q_1 <span class="codeph"></span> クエリのフォーム入力タグを出力します。 "クエリ番号"を指定しない場合、または"クエリ番号"が"0"の場合は、メインの <span class="codeph"> sp_q </span> クエリの入力タグが挿入されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>フォーム選択タグと関連HTMLを挿入し、コレクション選択メニューを表示します。 オプションの「all」属性を使用して、Webサイト全体を表すコレクションの名前を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索テンプレートタグの1つから出力を、結果ページの他のHTMLタグまたはテンプレートタグ内に挿入します。 <span class="codeph"> &lt;search-lt&gt;は、より小さい文字を </span> 挿入します。 &lt;search-lt&gt; <span class="codeph"> と </span><span class="codeph"></span> &lt;search-gt&gt;を使用すると、タグの定義をエスケープして、検索テンプレートタグを属性値として使用できます。 検索に応じてテンプレートがレンダリングされると、 <span class="codeph"> &lt;search-lt&gt; </span> タグが小なり記号(&lt;)に置き換えられます。 例えば、 <span class="codeph"> &lt;search-link&gt; </span> は、 <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt;と同じ </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索テンプレートタグの1つから出力を、結果ページの他のHTMLタグまたはテンプレートタグ内に挿入します。 <span class="codeph"> &lt;search-gt&gt;は、次の文字より大きい文字を </span> 挿入します。 &lt;search-lt&gt; <span class="codeph"> と </span><span class="codeph"></span> &lt;search-gt&gt;を使用すると、タグの定義をエスケープして、他のテンプレートタグを属性値として使用できます。 検索に応じてテンプレートがレンダリングされると、 <span class="codeph"> &lt;search-gt&gt; </span> タグが大なり記号(&gt;)に置き換えられます。 例えば、 <span class="codeph"> &lt;search-link&gt; </span> は、 <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt;と同じ </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在の検索要求から、"param-name"という名前のcgiパラメーターの値を返します。 オプションの「encoding」属性は、出力を結果ページの出力用にHTMLエンコード、JavaScriptエンコード、Perlエンコード、URLエンコードのいずれにエンコードするかを制御します。 デフォルト値の「encoding」は「html」です。 通常は、encoding属性を指定する必要はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>エン <span class="codeph"> コーディング </span> 属性はオプションです。デフォルト値は <span class="codeph"> jsonで </span>す。 </p> <p> <p>注意： このタグは、コア検索クエリのパラメーターで <span class="codeph"> sp_trace=1が指定さ </span> れている場合にのみ出力されます。 </p> </p> <p>バックエンド検索CGIパラメーターにある表の48行を参照して <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> ください</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートアンカーリンクタグ {#section_3A51D27616C541E2B818CC52B2B856BA}

次に示すのは、タグの間にアンカーリンクを設定してHTMLを囲む原因となるタグです。 アンカーリンクをクリックすると、別のページの結果を表示するように求められます。 オプションの属性「count」リクエストで、表示するページ上の結果の数が多くなります。 指定しなかった場合は、現在のページで要求された数が使用されます。 詳細なオプションの「URL」属性は、関連リンクの転送先ドメインを制御します。 デフォルトではドメインはですが、URL属性を使用し `https://search.atomz.com/search/`てこれを変更できます。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果の次のページまたは前のページを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>結果を日付順または関連性順に並べ替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>サマリの表示/非表示を切り替えます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートの条件タグ {#section_18D9BC66DE484881932FD2F7EA9D170D}

間にHTMLを条件付きで含めることができるタグ。

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
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ... &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt;...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページに検索結果が含まれる（または含まれない）場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ... &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ... &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ... &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ... &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>前のページまたは次のページに結果が関連付けられている（または何も結果がない）場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ... &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ... &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ... &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ... &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグには、現在のページが関連性または日付で並べ替えられた場合、またはそれ以外の場合に、HTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt; ... &lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt; ... &lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページで概要を表示または非表示にしている場合、これらのタグにはHTMLが含まれます。 これらのタグを使用して、検索結果の一部を含めたり除外したりできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt; ... &lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt; ... &lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>現在のページの検索結果の生成でコレクションが指定されている場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt; ... &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ... &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>検索クエリに <span class="codeph"> sp_advanced=1 </span> CGIパラメーターが指定されている場合、これらのタグにはHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ... &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ... &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらのタグは、指定されたパラメーターが無効な場合、または無効でない場合、それらの間にHTMLを含めたり除外したりします。 </p> <p>現在、 <span class="codeph"> sp_q_location[_#]パラメータのみがサポートされ </span> ています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ... &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt; ... &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグには、「name」属性で指定されたCGIパラメーターが「value」属性で指定された値を持つかどうかに基づいて、それらの間にHTMLが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ... &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ... &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグは、現在のページがある場合、またはない場合、その間にHTMLを含みます。このHTMLは、指定されたfield-nameで並べ替えられます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレートフォームコントロールタグ {#section_45AFC414ACA74825B72FEAA8456F8DD2}

検索テンプレート内のチェックボックス、ラジオボタン、リストボックスのデフォルトの選択状態を制御す `<form>` るためのタグ。

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
   <td colname="col2"> <p>&lt; <span class="codeph"> input&gt; </span> タグの代わりにテンプレートで使用されます。 タグがブラウザに書き込まれると、単語 <span class="codeph"> inputが </span> search-inputに置き換わり、タグ内の他のすべての情報 <span class="codeph"></span> がそのまま出力されます。 また、タグで <span class="codeph"> 指定された名前がCGIパラメータとしてリストされ、タグで指定された </span> 値がそのCGIパラメータの値 <span class="codeph"> である場合は、タグの末尾に </span><span class="codeph"></span> checkedという単語が追加されます。 このようにして、検索結果内のデフォルトのラジオボタンまたはチェックボックスの状態を、現在のクエリと同じ状態に自動的にすることができます。 </p> <p>例えば、チェックボックスのHTMLコードは次のようになります。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;サウンドに類似した一致はありません </span> </p> <p>このチェックボックスの対応するテンプレートコードは次のとおりです。 </p> <p> <span class="codeph"> &lt;search-input type=checkbox name="sp_w" value="exact"&gt;サウンドに類似した一致はありません </span> </p> <p>クエリのCGIパラメータ文字列に <span class="codeph"> sp_w=exactが含まれている場合、検索結果と共にブラウザに書き込まれるタグは次のようになります(この場合、 </span><span class="codeph"></span> checkedという単語がタグの末尾に挿入されます)。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact" checked&gt;サウンドに類似した一致はありません </span> </p> <p>クエリのCGIパラメータ文字列に <span class="codeph"> sp_w=exactが含まれていない場合、検索結果と共にブラウザに書き込まれるタグは次のようになります( </span>checkedという単語はタグに含ま <span class="codeph"></span> れません)。 </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;サウンドに類似した一致はありません </span> </p> <p>&lt;search-input&gt; <span class="codeph"></span> タグは、チェックボックスやラジオボタンを検索テンプレートに挿入する場合に便利です。 検索テンプレートの <span class="codeph"> &lt;フォーム&gt;に追加するチェックボックスやラジオボタンがある場合は、 </span> &lt;入力…&gt; <span class="codeph"> の代わりに </span> &lt;検索入力…&gt;を使用 <span class="codeph"></span>します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;検索 — 選択&gt; ... &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt; ... &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;form&gt;タグ内のドロップダウンリストボックスは、 <span class="codeph"> &lt;select&gt; </span> タグで始まり、 <span class="codeph"> &lt;/select&gt; </span><span class="codeph"></span> タグで終わります。 関連するCGIパラメーター <span class="codeph"> の </span> 名前は、 <span class="codeph"> &lt;select&gt; </span> タグ内に一覧表示されます。 &lt; <span class="codeph"> select&gt; </span> タグの後には、 <span class="codeph"></span> &lt;option&gt;タグのリストが続き、リストボックス内に表示する値を指定します。 </p> <p>&lt;search-select&gt; 、 <span class="codeph"> &lt;/search-select&gt; 、 </span>&lt;search-option&gt; 、 <span class="codeph"> &lt;search-option&gt; 、 </span>&lt;/search-option&gt;タグは、 <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> &lt;search-input&gt;タグと同様の機能を&lt;search-input&gt;タグに提供します。 つまり、ブラウザに&lt;option&gt;タグの末尾に、&lt;option&gt;タグ名をCGIとして&lt;select&gt;タグ名をCGIとして&lt;search- <span class="codeph"> select&gt;タグ名をCGIとして&lt;search- </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> select&gt;タグ名をCGIとして列挙した値をCGIとして自動的に追加する。 このようにして、検索結果内のデフォルトのリストボックスを、現在のクエリと同じように自動的に選択できます。 </p> <p>例えば、一般的なリストボックスは次のようになります。 </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>そのテンプレートボックスの対応するリストコードは次のとおりです。 </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>リストを検索テンプレートに <span class="codeph"> &lt;form&gt;に追加する場合は、を&lt;select&gt;に&lt;search-select.&gt;&lt;select&gt;に&lt;search-select.&gt;を使用します。 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>&lt;select&gt;検索を&lt;select&gt;に、検索を&lt;select.&gt;に使用します。&lt;/option&gt; . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ... &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>これらの高度なタグによって、それらの間にアンカーリンクがHTMLの周囲に作成されます。 このアンカーをクリックすると、特定のフィールドで並べ替えられた結果のページが表示されます。 オプションの <span class="codeph"> count </span> 属性では、結果ページに表示する結果の数を指定します。 countを省略すると、現在のページで使用されている数が使用されます。 <span class="codeph"></span> </p> </td> 
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
   <td colname="col2"> <p> 曜日を表す全体的な曜日名に一致します（例：「Monday」）。 言語/ <span class="uicontrol"> 単語と言語/言語の設定で、 </span> 各国語の表現 <span class="uicontrol"></span><span class="uicontrol"></span> を決定します。 </p> <p>「単語と言語 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> について</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> 曜日の略称を国内表現したものに一致します。略語は最初の3文字を表します（例：「月」）。 言語/ <span class="uicontrol"> 単語と言語/言語の設定で、 </span> 各国語の表現 <span class="uicontrol"></span><span class="uicontrol"></span> を決定します。 </p> <p>「単語と言語 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> について</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> 月名の全体表現に一致します（「June」など）。 言語/ <span class="uicontrol"> 単語と言語/言語の設定で、 </span> 各国語の表現 <span class="uicontrol"></span><span class="uicontrol"></span> を決定します。 </p> <p>「単語と言語 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> について</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> 月の略称を国内表現で表します。省略形は最初の3文字で、例えば「Jun」などです。 言語/ <span class="uicontrol"> 単語と言語/言語の設定で、 </span> 各国語の表現 <span class="uicontrol"></span><span class="uicontrol"></span> を決定します。 </p> <p>「単語と言語 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> について</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>"%m/%d/%y"と同じです（例："07/25/13"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> 月の何日かを10進数(01 ～ 31)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> 日付を10進数(1 ～ 31)で表します。 空白は1桁の桁数の前に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> 10進数(00 ～ 23)で24時間の時計に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> 月の略称を国単位で表したものに一致します。省略形は最初の3文字で、例えば「Jun」（%bと同じ）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> 12時間の時計を10進数(01 ～ 12)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> 年の何日目かを10進数で表します(001-366)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> (24時間制の時計を10進数(0 ～ 23)で表します。 空白は1桁の桁数の前に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> 12時間制の時刻を10進数(1 ～ 12)で表します。 空白は1桁の桁数の前に表示されます。 </p> </td> 
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
   <td colname="col2"> <p> 必要に応じて、「ante meridiem」または「post meridiem」の国別表現に一致します（例：「PM」）。 言語/ <span class="uicontrol"> 単語と言語/言語の設定で、 </span> 各国語の表現 <span class="uicontrol"></span><span class="uicontrol"></span> を決定します。 </p> <p>「単語と言語 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> について</a>」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>"%H:%M"と同じです（例： "13:23"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>"%I:%M:%S %p"と同じです（例："01:23:45 PM"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> 2番目の値に10進数(00 ～ 60)で対応します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>"%H:%M:%S"と同じです（例："13:26:47"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> 年の何週目か（日曜日を週の最初の曜日として）を10進数(00 ～ 53)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>"%e-%b-%Y"と同じです（例："25-Jul-2013"）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%はい </p> </td> 
   <td colname="col2"> <p> 世紀を10進数で表した年に一致します（例：「2013」）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> 世紀を含まない年を10進数(00 ～ 99)で表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> タイムゾーン名に一致します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> 一致する "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## 言語識別子 {#section_0490DECC00E34691ADE5A9ED90A6D911}

次の表に、サポートされている各言語の言語識別子を示します。 次のテンプレートタグで、これらの識別子をオプションの「言語」属性の値として使用できます。

* `search-date` および `search-display-field`.

   「 [結果のループ文字列タグ](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)」を参照してください。

* `search-field-value-list` 詳しくは、 [フィールド値のリストタグ](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)を参照してください。

* `search-field-value` フィールド値の [リストループタグを参照してください](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)。

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
   <td colname="col1"> <p>アイルランド語（アイルランド） </p> </td> 
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
   <td colname="col1"> <p>ロシア語(旧ソ連和集合) </p> </td> 
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

Content-Type HTTP応答ヘッダーは、次のタグを使用して指定できます。

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

属性 `content` と `charset` 属性はオプションです。 このタグは、可能な限り早くテンプレートに表示されます。 また、またはの前に記述することもお勧めし `<search-html-meta-charset>` ます。これらのタグの動作に影響を与えるから `<search-xml-decl>`です。

属性を指定しない場合、 `content` の値は、 `MIME-type` > **[!UICONTROL Settings]** >で設定された値にデフォルト値が設定され **[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;ます。 属性を指定した場合は、その `content` 属性が `content` タグのデフォルト `<search-html-meta-charset>` 属性として使用されます。

属性を指定しない場合、 `charset` ヘッダーに `charset` 値が書き込まれません `content-type` 。

を指定した場合、 `charset="1"` の実際の値 `charset-name` は `sp_f` CGIパラメーターの値になります。 検索で `sp_f` CGIパラメーターが送信されない場合、の実際の値はアカウント設定から読み取 `charset-name` られます。 アカウントに関連付けられている文字セットは、 > > >で表示したり変更し **[!UICONTROL Settings]** たりでき **[!UICONTROL My Profile]****[!UICONTROL Personal Information]****[!UICONTROL Character Encoding]**&#x200B;ます。

詳しくは、個人ユーザ情報の [設定を参照してください](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)。

またはのように、特定の文字セット名を `charset` 値としてリストすることで選択でき `charset="iso-8859-1"` ま `charset="Shift-JIS"`す。

属性を指定する場合、その属性が `charset` タグと `charset` タグのデフォルト `<search-html-meta-charset>` 属性として使用され、 `<search-xml-decl>``content-type` ヘッダーに出力されます。

## HTMLテンプレートでの文字セットの指定 {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

デフォルトのHTML検索結果テンプレートでは、次のタグを使用して、現在のアカウントに関連付けられた文字セットを指定します。

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

content属性とcharset属性はオプションです。 このタグは、テンプレートのHTML `<head>` セクションに表示する必要があります。 このタグは、テンプレートから生成されたHTMLページに次のタグを返します。

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

content属性を指定しない場合、実際の値は2つの値のいずれかに `MIME-type` なります。 タグで `<search-content-type-header>``content` 属性が指定されている場合は、その値が使用されます。 それ以外の場合は、「>/」 **[!UICONTROL Templates]** タブの値セットが使用され **[!UICONTROL Settings]****[!UICONTROL Content Type]** ます。

属性を指定しない場合、 `charset` 実際の値は2つの値のいずれか `charset-name` になります。 タグで `<search-content-type-header>``charset` 属性が指定されている場合は、その値が使用されます。 それ以外の場合は、の実際の値 `charset-name` がアカウント設定から読み込まれます。 アカウントに関連付けられている文字セットは、 > > >で表示したり変更し **[!UICONTROL Settings]** たりでき **[!UICONTROL My Profile]****[!UICONTROL Personal Information]****[!UICONTROL Character Encoding]**&#x200B;ます。

詳しくは、個人ユーザ情報の [設定を参照してください](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)。

を指定した場合、 `charset="1"` の実際の値 `charset-name` は `sp_f` CGIパラメーターの値になります。 検索で `sp_f` CGIパラメーターが送信されない場合、の実際の値は、タグで設定された値(指定さ `charset-name``<search-content-type-header>` れた場合)またはアカウント設定で設定された値（アカウント設定）になります。

に示すように、特定の文字セット名を指定でき `charset="charset-name"`ます。 For example, `charset="iso-8859-1"` or `charset="Shift-JIS"`.

タ `<search-html-meta-charset>` グはオプションです。 削除した場合、ブラウザーはのデフォルト値を想定します。 `content-type`次の値が使用されます。 `content="text/html; charset=ISO-8859-1"`. また、タグを独自のタグに置き換えることもで `<search-html-meta-charset>` き `http-equiv` ます。

## XMLテンプレートでの文字セットの指定 {#section_17DC31CDCC104F5F8081466B41A96E9D}

デフォルトのXML検索結果テンプレートでは、次のタグを使用して、現在のアカウントに関連付けられた文字セットを指定します。

`<search-xml-decl [charset="charset-name"]>`

この `charset` 属性はオプションです。 このタグは、テンプレートの上部で、任意のタグの後に表示する必要があり `<search-content-type-header>` ます。 このタグにより、テンプレートから生成されるXMLドキュメントに次のタグが追加されます。

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

を指定しない場合 `charset`、実際の値は2つの値のいずれか `charset-name` になります。 属性を `<search-content-type-header>``charset` 指定した場合は、その値が使用されます。 それ以外の場合は、の実際の値 `charset-name` がアカウント設定から読み込まれます。 アカウントに関連付けられている文字セットは、 > > >で表示したり変更し **[!UICONTROL Settings]** たりでき **[!UICONTROL My Profile]****[!UICONTROL Personal Information]****[!UICONTROL Character Encoding]**&#x200B;ます。

詳しくは、個人ユーザ情報の [設定を参照してください](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)。

を指定した場合、 `charset="1"` の実際の値 `charset-name` は `sp_f` CGIパラメーターの値になります。 検索で `sp_f` CGIパラメーターが送信されない場合、の実際の値は、タグで設定された値(指定さ `charset-name``<search-content-type-header>` れた場合)またはアカウント設定で設定された値（アカウント設定）になります。

必要に応じて、のように特定の文字セット名を指定 `charset="charset-name"`できます。 例： `charset="iso-8859-1" or charset="Shift-JIS"`

タグを独自のタグに置き換えることがで `<search-xml-decl>` き `?xml` ます。

## 検索テンプレートを別の {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

ある検索テンプレートを別の検索テンプレートに含めるには、 `<search-include>` タグを使用し、file属性に含めるテンプレートファイルの名前を設定します。次に例を示します。

`<search-include file="seo/seo_search_title.tpl" />`

SEO検索テンプレートセグメントはサブフォルダーに含まれ、通常の検索テンプレートはサブ `seo/``templates/` フォルダーに含まれます。 このコンテキストに含めると意味のあるのは.tplファイルのみです。

## Webサイト用の複数のトランスポートテンプレートの管理 {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

各領域に異なる検索トランスポートテンプレートを使用して、Webサイト全体での検索結果の外観を制御できます。

<!-- 

r_managing_multiple_templates.xml

 -->

この種の検索機能を実現するには、サイト検索/マーチャンダイジングでトランスポートテンプレートを管理します。 または、「公開」でトランスポートテンプレートを管理できます。 サイト検索/マーチャンダイジングと同様に、「発行」では、複数の検索トランスポートテンプレートを編集、プレビュー、および発行できます。

（デフォルト以外の）特定のトランスポートテンプレートを使用するように検索フォームを設定するには、 `sp_t` クエリパラメータを使用します。 例えば、Webサイトのマークダウン販売エリアに「クリアランス」という名前の検索テンプレートがあるとします。 標準のHTML検索フォームを使用し、次の追加のフォームコードを使用します。

`<input type=hidden name="sp_t" value="clearance">`

顧客がこのコード行を含む標準フォームをクリックすると、検索結果と共に「クリアランス」検索トランスポートテンプレートが表示されます。

「検索フォームでのコレクションの [使用](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)」を参照してください。

フォーム [でのフレームの使用を参照してください](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)。

詳しくは、「アドバンス検索フォーム [の例](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)」を参照してください。
