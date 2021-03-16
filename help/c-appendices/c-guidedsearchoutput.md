---
description: XMLやJSONなど、テキストベースの任意の形式で出力をカスタマイズする方法を説明します。
solution: Target
title: ガイド付き検索の出力
topic: 付録，サイト検索とマーチャンダイジング
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '6289'
ht-degree: 3%

---


# ガイド付き検索の出力{#guided-search-output}

XMLやJSONなど、テキストベースの任意の形式で出力をカスタマイズできます。

## ガイド付き検索出力の使用{#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

出力形式は、デザインプロセス中に行われるファセット設定、並べ替えおよびその他の実装固有の決定をサポートするようにカスタマイズできます。 必要に応じて、形式自体を適用して、お客様のフロントエンドの開発を簡略化できます。

出力全体は`<result>`タグ内に含まれ、動的データのほとんどは`<![CDATA[ ]]>`タグ内に含まれます。 このような組織では、結果にHTMLおよびその他の非XMLエンティティを含めることができます。

他のページへのリンクが提供される場所には、相対URLの形式で表示されます。 この結果には、目的の結果を生成するために渡されるクエリ文字列パラメーターも含まれます。

## ガイド付き検索の実装について{#section_95483980930C4325BAB50A40BD47245A}

ガイド付き検索の実装を開始する際には、[!DNL Adobe Search&Promote]がビジネス層を担当することを忘れないでください。 つまり、顧客に対して表示される結果とファセットを囲むロジックです。

解析して結果をHTMLとして表示するWeb アプリケーションフロントエンドを実装する場合、機能が表示のみに制限します。 つまり、プレゼンテーションレイヤーの作成に使用するサーバー側のロジックは、必要がない限り、何を顧客に提示するかに関する決定を行いません。 フロントエンドスクリプトが検索結果を変更している場合、ビジネスルールは期待どおりに機能しません。

[!DNL Adobe Search&Promote] URLパラメータを使用して、選択した検索絞り込みオプションのユーザ状態を維持します。すべての`<link>`ノードには、顧客の選択内容に関連するパラメーターが含まれます。 これらのパラメーターには、パンくず、ページネーション、並べ替えおよびファセットの選択を含めることができます。 該当する場合は、`<undolink>`ノードが返され、顧客が選択範囲から「戻る」ことができます。 ファセットとパンくずリストには、この種のリンクがオファーされます。

## 検索サーバの操作{#section_8DBEACDECD714E59BDED6315E6041B8D}

RESTに似たAPIが使用され、これを操作して検索を実行し、結果を受け取ることができます。 結果に使用される最も一般的な形式はXMLまたはJSONです。

ベースURIは、特定のアカウントと、ステージングされた環境またはライブアカウントに関連付けられます。 アカウントマネージャーからベースURIの複数のエイリアスをリクエストできます。 例えば、Megacorpという架空の会社の場合、アカウントに関連付けられた次の2つのベースURLがあります。

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

前者のURIは、そのライブインデックスに対して検索を行い、後者のURIはそのステージングされたインデックスに対して検索を行います。

検索要求は、ベースURIと、ベースURIに関連付けられたアカウントの目的の検索を示すCGIパラメーターのセットまたはキーと値のペアで構成されます。

3つの形式のCGIパラメータがサポートされています。 デフォルトでは、次の例のように、CGIパラメーターをセミコロン(`;`)で区切るようにアカウントが設定されています。

* `https://search.megacorp.com?q=shoes ;page=2`

必要に応じて、アカウントマネージャに、CGIパラメーターを区切るアンパサンド(`&`)を使用するようにアカウントを設定してもらうことができます。次に例を示します。

* `https://search.megacorp.com?q=shoes &page=2`

3つ目の形式（SEO形式）もサポートされています。次の例のように、区切り文字の代わりにスラッシュ(`/`)が使用され、「クリーン」リンクが生成されるのは等号です。

* `https://search.megacorp.com/q/shoes/page/2`

SEO形式を使用してリクエストが送信されると、すべての出力リンクは同じ形式で返されます。

## 検索クエリのパラメーター{#section_7ADA5E130E3040C9BE85D0D68EDD3223}

次の表に、使用できる標準の「そのまま使用できる」検索クエリパラメータを示します。 処理ルールとビジネスルールは、ユーザー定義のクエリパラメーターに基づいて構築し、会社に関連するカスタムのビジネスロジックを実装できます。 コンサルティングチームと協力して、これらのパラメーターに関するドキュメントを入手できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>検索クエリパラメータ </p> </th> 
   <th colname="col2" class="entry"> <p>例 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q=文字列  </span> </p> </td> 
   <td colname="col3"> <p> 検索のクエリ文字列を指定します。 このパラメーターは、<span class="codeph"> sp_q </span>バックエンド検索パラメーターにマップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#=文字列  </span> </p> </td> 
   <td colname="col3"> <p>番号付きの<span class="codeph"> q </span>と<span class="codeph"> x </span>パラメーターは、特定のフィールド内でファセット設定（検索）を行います。 </p> <p><span class="codeph"> q </span>パラメーターは、ファセットで検索する用語を、対応する番号<span class="codeph"> x </span>パラメーターが示すとおりに定義します。 例えば、sizeとcolorという名前のファセットが2つある場合、次のようになります。 </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>このパラメーターは、<span class="codeph"> sp_q_exact_# </span>バックエンド検索パラメーターにマップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#=文字列  </span> </p> </td> 
   <td colname="col3"> <p> 番号付きの<span class="codeph"> q </span>と<span class="codeph"> x </span>パラメーターは、特定のフィールド内でファセット設定（検索）を行います。 </p> <p><span class="codeph"> q </span>パラメーターは、ファセットで検索する用語を、対応する番号<span class="codeph"> x </span>パラメーターが示すとおりに定義します。 例えば、sizeとcolorという名前のファセットが2つある場合、次のようになります。 </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>このパラメーターは、<span class="codeph"> sp_x_# </span>バックエンド検索パラメーターに対応付けられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コレクション </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collection=string  </span> </p> </td> 
   <td colname="col3"> <p> 検索に使用するコレクションを指定します。 このパラメーターは、<span class="codeph"> sp_k </span>バックエンド検索パラメーターにマップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> count </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= number  </span> </p> </td> 
   <td colname="col3"> <p> 表示する結果の合計数を指定します。 デフォルトは、<span class="uicontrol">設定</span> &gt; <span class="uicontrol">検索</span> &gt; <span class="uicontrol">検索</span>で定義されています。 このパラメーターは、<span class="codeph"> sp_c </span>バックエンド検索パラメーターにマップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> page </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= number  </span> </p> </td> 
   <td colname="col3"> <p> 返される結果のページを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ランク  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> rank=フィールド  </span> </p> </td> 
   <td colname="col3"> <p> 静的なランクに使用するランクフィールドを指定します。 フィールドは、0より大きい関連性を持つ「ランク」タイプのフィールドである必要があります。 このパラメーターは、<span class="codeph"> sp_sr </span>バックエンドパラメーターにマップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= string  </span> </p> </td> 
   <td colname="col3"> <p> 検索するストアを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 並べ替え  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= number  </span> </p> </td> 
   <td colname="col3"> <p> 並べ替え順を指定します。 「0」はデフォルトで、関連性スコアで並べ替えられます。「1」は日付で並べ替えます。「 —1」は並べ替えを行いません。 </p> <p>ユーザーは、<span class="codeph"> sp_s </span>パラメーターの値のフィールド名を指定できます。 例えば、<span class="codeph"> sp_s=title </span>は、タイトルフィールドに含まれる値に従って結果を並べ替えます。 <span class="codeph"> sp_s </span>パラメータの値にフィールド名を使用すると、そのフィールドで結果が並べ替えられ、関連性の高い順にサブソートされます。 </p> <p>この機能を有効にするには、次の手順を実行します。 </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">製品メニューで、<span class="uicontrol">設定</span>/<span class="uicontrol">メタデータ</span>/<span class="uicontrol">定義</span>をクリックします。 </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D"><span class="wintitle"> Staged Definitions </span>ページで、次のいずれかを実行します。 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB">「<span class="uicontrol">追加新しいフィールド</span>」をクリックします。 </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">特定のフィールド名に対して「<span class="uicontrol">編集</span>」をクリックします。 </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903"><span class="wintitle">並べ替え</span>ドロップダウンリストで、<span class="uicontrol"> </span>または昇順<span class="uicontrol"> 降順 </span>をクリックします。 <p>このパラメーターは、<span class="codeph"> sp_s </span>バックエンド検索パラメーターにマップされます。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## システムとの統合{#section_91261B19A44A4E579B3FC9FAB9AD3665}

お使いのシステムとの統合に関する推奨事項を以下に示します。

* 検索サーバーとの通信。

   httpGETリクエストを使用して[!DNL Adobe Search&Promote] Webサーバーと通信できます。 これらのリクエストは、サーバーで生成されるか、クライアント側でAjaxリクエストを実行します。
* 検索履歴の保存

[!DNL Adobe Search&Promote] はstatelessで、httpリクエストで状態全体が渡されます。
* 返された結果を解析しています。

   XML応答の解析には、SAXベースのXMLパーサーを使用することをお勧めします。 Ajaxリクエストを生成する場合、[!DNL Adobe Search&Promote]を設定して、それらのリクエストに対するJSON応答を返すようにし、応答の解析を容易にします。

## ガイド付き検索JSON出力{#reference_EB8182A564DE4374BB84158F2AABEF74}

標準JSON応答出力を説明する表。

[ガイド付き検索JSONの出力](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74)も参照してください。

次のJSON応答を確認できます。

* [バナー](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [パンくず](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [ファセット](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
* [ヘッダーとクエリ](../c-appendices/c-guidedsearchoutput.md#section_1D57062259CA46E0B4F598FA4EB37065)
* [ページ編集](../c-appendices/c-guidedsearchoutput.md#section_504E7AB570BD49AF9839530DC438EE96)
* [最近実行した検索](../c-appendices/c-guidedsearchoutput.md#section_525816A0355C48F8970D89B8FC3F1FFF)
* [結果](../c-appendices/c-guidedsearchoutput.md#section_41AC56BB0A084BF59379B06C8BEF2157)
* [検索フォーム](../c-appendices/c-guidedsearchoutput.md#section_434DA13EA295474C99FFE9F14801CD0E)
* [並べ替え](../c-appendices/c-guidedsearchoutput.md#section_558853CD376F4D71BACF211D53085D55)
* [提案](../c-appendices/c-guidedsearchoutput.md#section_6EC104E1DDD94AC799B65E6E61A2FB3C)
* [ゾーン](../c-appendices/c-guidedsearchoutput.md#section_AE53A498B440465EAF2286F2AE87D548)

## バナー {#section_88519CAAD25F4BD49D5E517077745B0E}

例：

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>バナーのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々のバナーノード。 複数のバナーノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Webページ上でバナーが表示される領域です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> バナー領域のHTMLコンテンツです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## パンくず{#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

次の例では、顧客がファセットを下に絞り込むたびに、ファセット内の階層リンクに選択が追加されます。 各項目は`<breadcrumb-item>`として表されます。

例：

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>パンくずリストのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 目的の表示を示す検索結果への相対リンク。 階層リンクをクリックすると、後続のすべての絞り込みが削除された表示が表示されます。 その他のオプションも使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> パンくずリスト項目の顧客表示テキスト。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ファセット{#section_65932C95931743A1BFAF1DF16D7E6D92}

ファセットは、結果をフィルタリングする機能を提供する細分オプションです。 ファセットは、一般に、分類、価格範囲、色の選択、その他の属性の細分化に使用されます。 インデックス内のメタデータは、ファセットを駆動します。

顧客がカテゴリー内を下に移動すると、「カテゴリーファセット」を表示または非表示にするのが一般的です。 最も高いレベルの分類(カテゴリ)を階層1と呼びます。 お客様が階層1のオプションをクリックすると、階層2（サブカテゴリ）の細分オプションが表示され、階層1のオプションは表示されなくなります。 お客様が階層2のオプションをクリックすると、階層3（サブサブカテゴリ）細分オプションが表示され、階層2のオプションが消えます。 上記のように、これらのオプションは非表示になり、Webアプリケーションに表示されますが、これらのオプションの影響は受けません。

各ファセットは`<facet-item>`タグ内に含まれます。 次の例では、顧客が「休日」で検索結果を絞り込むことのできるファセットを1つ示しています。

例：

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item> 
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ファセットのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットに対する顧客対応のタイトル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットオプションの顧客対応ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプションを絞り込む結果への相対リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> 絞り込まれた結果セットの結果数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセット値を選択すると、ノードから「元に戻すリンク」が返され、顧客は結果を取り消すことができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ヘッダーとクエリ{#section_1D57062259CA46E0B4F598FA4EB37065}

例：

```xml
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

これらのタグを一緒に使用すると、次のようなメッセージが表示されます。「年明けに621件中1-16件の結果を示しています」

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ヘッダーとクエリのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> リクエストと共に送信されるキーワードクエリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの最初の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの最後の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> ユーザークエリと一致する結果の合計数です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索結果にグローバルに適用されるオプションのフィールドです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ページ番号{#section_504E7AB570BD49AF9839530DC438EE96}

例：

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ページネーションのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> 結果の合計ページ数を、結果の数をページあたりの結果の数で割った値に基づきます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が既に1ページ目を表示している場合を除き、結果セットの最初のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が最後のページを表示していない場合に、結果セットの最後のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が1ページ目を表示していない限り、結果セットの前のページへの相対リンクが含まれます。この場合、空白になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が最後のページを表示していない場合に、結果セットの最後のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> 特定のページ番号への相対リンクが含まれます。 10個の連続したページ番号が表示されます。 1ページ目は、1 ～ 10ページになります。 結果セット（この場合は39）の最後に、30 ～ 39ページになります。 例えば、結果セットの中央の15ページには、11 ～ 20ページが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> 現在選択されているページの属性として適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 最近実行した検索 {#section_525816A0355C48F8970D89B8FC3F1FFF}

最近の検索はcookieベースの機能で、cookieの情報をサーバーにリレーする場合にのみ機能します。

例：

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>最近の検索でのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々の最近の検索ノード。 最近使用した検索ノードは複数持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が以前に検索した用語。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 前の検索へのリンク。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果 {#section_41AC56BB0A084BF59379B06C8BEF2157}

結果セットは、JSON応答のカスタマイズ可能な領域です。 各インデックスは、メタデータのフィールド命名メカニズムで一意です。 タイトル、説明、URLなど、各結果に対して返される共通フィールドがあります。 ただし、インデックス内のページに対して定義されたメタデータは、各結果ノードで使用できるようになります。 分類、価格、色、サムネールは、検索結果をより説得力のあるものにするために、結果に適用できるオプションの一部にすぎません。

結果の形式は、実装に固有のメタデータに基づいてカスタマイズされます。 サムネール画像のURLを含む、結果に表示する結果ごとのデータがここに含まれます。

さらに、「特集結果」などの複数の結果ゾーンをページ内に設定したり、「製品」と「コンテンツ」の結果セクションを個別に設定したりできます。 この場合、ファセットは主な結果セットにのみ関連付けられますが、複数の結果ゾーンがHTML内に提供されます。

例：

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>結果のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> この結果セット内の結果のシリアル番号。 この例では、1ページに10件の結果が表示され、2ページ目の結果には最初の項目のインデックスが11になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの顧客対応のタイトル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページのURL。 顧客が結果をクリックスルーできるハイパーリンクを作成するために使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 検索フォーム{#section_434DA13EA295474C99FFE9F14801CD0E}

例：

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>検索フォームのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプション. JSON内に存在する場合、値が1の場合は、アカウントが<span class="keyword"> Test&amp;ターゲット</span>にリンクされ、A:Bテスト内に少なくとも1つのビジネスルールがあることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプション. オートコンプリートを使用する場合、このノードは、CSSとJavaScriptがフォーム内のコンテンツと共にページに存在することを示します。 オートコンプリートの設定が変更されていない場合、通常、これらのフィールドは変更されません。 このような場合、xxx_cache_verフィールドが増分され、キャッシュされたコンテンツがユーザーのブラウザー上で強制的に無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートに関連付けられているCSS。 ページのレンダリングを改善するために、ページ内でこのタグの高さを高くすることをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートユーティリティが正しいコントロールにフックアップするために、search-from内で必要なコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートに必要なカスタムJavaScript。 ページのレンダリングを改善するために、ページの下部にこのタグを配置することをお勧めします。 YUI JavaScriptは、オートコンプリートにも必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索フォームに含める非表示のパラメーター（名前と値）がすべて含まれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 並べ替え {#section_558853CD376F4D71BACF211D53085D55}

次の例は、3つのオプションから成る並べ替えメニューのデータを示しています。 このメニューを使用すると、顧客は関連性、タイトルまたは評価で並べ替えることができます。 現在選択されているアイテムには、「selected=true」属性が含まれています。 &quot;. 常に関連性のあるオプションをオファーし、顧客が最初に表示されたデフォルトの検索結果に戻れるようにします。

例：

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>並べ替えメニューのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプションの顧客向けテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> このオプションの「sort」クエリ文字列パラメーターの値を表します。 <span class="codeph"> &lt;link&gt; </span>値を使用する場合は、このタグは不要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 選択されていないオプションの場合、<span class="codeph"> &lt;link&gt; </span>パラメーターには、同じ結果セットを返す相対リンクが含まれ、新しい並べ替えパラメーターで並べ替えられます。 現在選択されている並べ替えオプションでは、このフィールドは空白です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 提案{#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

サーチクエリは、結果が少ない場合、または結果がない場合に返されます。 このノードには、成功したクエリを生み出す用語が含まれており、「結果なし」ページに表示できます。 また、顧客が新しいクエリにジャンプできるように、リンクが返されます。

例：

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>提案のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>サーチクエリ用語の検索結果へのハイパーリンクを作成するために使用する相対リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>推奨される用語。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ゾーン{#section_AE53A498B440465EAF2286F2AE87D548}

例：

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ゾーン内のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々のゾーンノード。 複数のゾーンノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> ゾーンの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1または0を指定して、ゾーンが表示されているか、表示されていないかを示します。 実際のゾーンのコンテンツは、Webページ上や検索結果（ベストセラーや関連商品など）の静的な領域にすることができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ガイド付き検索XML出力{#reference_D93E859A277643068B10AE7A61C973EA}

標準XML応答出力を説明する表。

XML応答は次の項目で確認できます。

* [バナー](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [パンくず](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [ファセット](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
* [ヘッダーとクエリ](../c-appendices/c-guidedsearchoutput.md#section_802835E19BCB48239C6770A1B72DFFF8)
* [ページ編集](../c-appendices/c-guidedsearchoutput.md#section_72DB86DDE1284B1EA295CFFBC16A3150)
* [最近実行した検索](../c-appendices/c-guidedsearchoutput.md#section_BCA2DDD17F264CF6BA11634E1A514E28)
* [結果](../c-appendices/c-guidedsearchoutput.md#section_EC496F5CA2634158891455E2F6DF6833)
* [検索フォーム](../c-appendices/c-guidedsearchoutput.md#section_F92D8C3D37174A10A4E26CAFF3F3DF89)
* [並べ替え](../c-appendices/c-guidedsearchoutput.md#section_32DC50A103BF491BA3665A5CADCCAADE)
* [提案](../c-appendices/c-guidedsearchoutput.md#section_D81BCE46F0AF443695DF9C4BA084B716)
* [ゾーン](../c-appendices/c-guidedsearchoutput.md#section_15D8AA585F3246799968BA88EE2C9FC2)

## バナー {#section_6A19EC26DD3B494194AAA788151B78B5}

例：

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>バナーのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々のバナーノード。 複数のバナーノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Webページ上でバナーが表示される領域です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> バナー領域のHTMLコンテンツです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## パンくず{#section_E48A71B0EBDB4EDDA7587009AD865488}

次の例では、顧客がファセットを下に絞り込むたびに、ファセット内の階層リンクに選択が追加されます。 各項目は`<breadcrumb-item>`として表されます。

例：

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>パンくずリストのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 目的の表示を示す検索結果への相対リンク。 階層リンクをクリックすると、後続のすべての絞り込みが削除された表示が表示されます。 その他のオプションも使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> パンくずリスト項目の顧客表示テキスト。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ファセット{#section_5CEB1F966C004FFEA3CF675638966E25}

ファセットは、結果をフィルタリングする機能を提供する細分オプションです。 ファセットは、一般に、分類、価格範囲、色の選択、その他の属性の細分化に使用されます。 インデックス内のメタデータは、ファセットを駆動します。

顧客がカテゴリー内を下に移動すると、「カテゴリーファセット」を表示または非表示にするのが一般的です。 最も高いレベルの分類(カテゴリ)を階層1と呼びます。 お客様が階層1のオプションをクリックすると、階層2（サブカテゴリ）の細分オプションが表示され、階層1のオプションは表示されなくなります。 お客様が階層2のオプションをクリックすると、階層3（サブサブカテゴリ）細分オプションが表示され、階層2のオプションが消えます。 上記のように、これらのオプションは非表示になり、Webアプリケーションに表示されますが、これらのオプションの影響は受けません。

各ファセットは`<facet-item>`タグ内に含まれます。 次の例では、顧客が「休日」で検索結果を絞り込むことのできるファセットを1つ示しています。

例：

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item>  
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ファセットのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットに対する顧客対応のタイトル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセットオプションの顧客対応ラベル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプションを絞り込む結果への相対リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> 絞り込まれた結果セットの結果数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> ファセット値を選択すると、ノードから「元に戻すリンク」が返され、顧客は結果を取り消すことができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ヘッダーとクエリ{#section_802835E19BCB48239C6770A1B72DFFF8}

例：

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

これらのタグを一緒に使用すると、次のようなメッセージが表示されます。「年明けに621件中1-16件の結果を示しています」

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ヘッダーとクエリのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> リクエストと共に送信されるキーワードクエリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの最初の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの最後の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> ユーザークエリと一致する結果の合計数です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索結果にグローバルに適用されるオプションのフィールドです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ページ番号{#section_72DB86DDE1284B1EA295CFFBC16A3150}

例：

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ページネーションのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> 結果の合計ページ数を、結果の数をページあたりの結果の数で割った値に基づきます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が既に1ページ目を表示している場合を除き、結果セットの最初のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が最後のページを表示していない場合に、結果セットの最後のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が1ページ目を表示していない限り、結果セットの前のページへの相対リンクが含まれます。この場合、空白になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が最後のページを表示していない場合に、結果セットの最後のページへの相対リンクが含まれます。 この場合、空白です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> 特定のページ番号への相対リンクが含まれます。 10個の連続したページ番号が表示されます。 1ページ目は、1 ～ 10ページになります。 結果セット（この場合は39）の最後に、30 ～ 39ページになります。 例えば、結果セットの中央の15ページには、11 ～ 20ページが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> 現在選択されているページの属性として適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 最近実行した検索 {#section_BCA2DDD17F264CF6BA11634E1A514E28}

最近の検索はcookieベースの機能で、cookieの情報をサーバーにリレーする場合にのみ機能します。

例：

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>最近の検索でのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々の最近の検索ノード。 最近使用した検索ノードは複数持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> 顧客が以前に検索した用語。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 前の検索へのリンク。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果 {#section_EC496F5CA2634158891455E2F6DF6833}

結果セットは、XML応答のカスタマイズ可能な領域です。 各インデックスは、メタデータのフィールド命名メカニズムで一意です。 タイトル、説明、URLなど、各結果に対して返される共通フィールドがあります。 ただし、インデックス内のページに対して定義されたメタデータは、各結果ノードで使用できるようになります。 分類、価格、色、サムネールは、検索結果をより説得力のあるものにするために、結果に適用できるオプションの一部にすぎません。

結果の形式は、実装に固有のメタデータに基づいてカスタマイズされます。 サムネール画像のURLを含む、結果に表示する結果ごとのデータがここに含まれます。

さらに、「特集結果」などの複数の結果ゾーンをページ内に設定したり、「製品」と「コンテンツ」の結果セクションを個別に設定したりできます。 この場合、ファセットは主な結果セットにのみ関連付けられますが、複数の結果ゾーンがHTML内に提供されます。

例：

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>結果のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> この結果セット内の結果のシリアル番号。 この例では、1ページに10件の結果が表示され、2ページ目の結果には最初の項目のインデックスが11になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページの顧客対応のタイトル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> このページのURL。 顧客が結果をクリックスルーできるハイパーリンクを作成するために使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 検索フォーム{#section_F92D8C3D37174A10A4E26CAFF3F3DF89}

例：

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>検索フォームのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプション. XML内に存在する場合、値が1の場合は、アカウントが<span class="keyword"> Test&amp;ターゲット</span>にリンクされ、A:Bテスト内に少なくとも1つのビジネスルールがあることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプション. オートコンプリートを使用する場合、このノードは、CSSとJavaScriptがフォーム内のコンテンツと共にページに存在することを示します。 オートコンプリートの設定が変更されていない場合、通常、これらのフィールドは変更されません。 このような場合、xxx_cache_verフィールドが増分され、キャッシュされたコンテンツがユーザーのブラウザー上で強制的に無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートに関連付けられているCSS。 ページのレンダリングを改善するために、ページ内でこのタグの高さを高くすることをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートユーティリティが正しいコントロールにフックアップするために、search-from内で必要なコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> オートコンプリートに必要なカスタムJavaScript。 ページのレンダリングを改善するために、ページの下部にこのタグを配置することをお勧めします。 YUI JavaScriptは、オートコンプリートにも必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> 検索フォームに含める非表示のパラメーター（名前と値）がすべて含まれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 並べ替え {#section_32DC50A103BF491BA3665A5CADCCAADE}

次の例は、3つのオプションから成る並べ替えメニューのデータを示しています。 このメニューを使用すると、顧客は関連性、タイトルまたは評価で並べ替えることができます。 現在選択されているアイテムには、「selected=true」属性が含まれています。 &quot;. 常に関連性のあるオプションをオファーし、顧客が最初に表示されたデフォルトの検索結果に戻れるようにします。

例：

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>並べ替えメニューのタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> オプションの顧客向けテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> このオプションの「sort」クエリ文字列パラメーターの値を表します。 <span class="codeph"> &lt;link&gt; </span>値を使用する場合は、このタグは不要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> 選択されていないオプションの場合、<span class="codeph"> &lt;link&gt; </span>パラメーターには、同じ結果セットを返す相対リンクが含まれ、新しい並べ替えパラメーターで並べ替えられます。 現在選択されている並べ替えオプションでは、このフィールドは空白です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 提案{#section_D81BCE46F0AF443695DF9C4BA084B716}

サーチクエリは、結果が少ない場合、または結果がない場合に返されます。 このノードには、成功したクエリを生み出す用語が含まれており、「結果なし」ページに表示できます。 また、顧客が新しいクエリにジャンプできるように、リンクが返されます。

例：

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>提案のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>サーチクエリ用語の検索結果へのハイパーリンクを作成するために使用する相対リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>推奨される用語。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ゾーン{#section_15D8AA585F3246799968BA88EE2C9FC2}

例：

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ゾーン内のタグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> 個々のゾーンノード。 複数のゾーンノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> ゾーンの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1または0を指定して、ゾーンが表示されているか、表示されていないかを示します。 実際のゾーンのコンテンツは、Webページ上や検索結果（ベストセラーや関連商品など）の静的な領域にすることができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Experience Manager{#reference_DBE13C606C3A4BB185DE53F88D0D3048}のガイド付き検索XML出力

AEM(Adobe Experience Manager)の標準XML応答出力を示す表。

も参照してください。 [ガイド付き検索XML出力](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

XML応答は次の項目で確認できます。

* [バナー](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [パンくずリスト](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [カスタムフィールド](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [ファセット](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [ヘッダー](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [メニューと並べ替え](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [ページ編集](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [クエリ](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [最近実行した検索](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [結果](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [検索フォーム](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [提案](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [テンプレート](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [ゾーン](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## バナー {#section_B16EDC5533FA4494AC9983AA7357CBE3}

サイト検索/マーチャンダイジングは、顧客のバナーを管理し、Webページの様々な部分にバナーを接続できます。

バナーの例：

次の例は、「top」と呼ばれるページの領域に配置されるバナーの例です。

```xml
   <banners> 
       <banner> 
           <area><![CDATA[top]]></area> 
           <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
       </banner> 
    </banners> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>バナー </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>各バナー領域と、その領域にプラグインされるコンテンツを示す0-n個のバナーノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バナー </p> </td> 
   <td colname="col2"> <p>バナー </p> </td> 
   <td colname="col3"> <p>個々のバナーノード。 複数のバナーノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>area </p> </td> 
   <td colname="col2"> <p>バナー </p> </td> 
   <td colname="col3"> <p>Webページ上でバナーが表示される領域です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>content </p> </td> 
   <td colname="col2"> <p>バナー </p> </td> 
   <td colname="col3"> <p>バナーのコンテンツ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## パンくずリスト {#section_49EA7043FBE44315A79A4E738BE30114}

複数のパンくずリストがサポートされます。 パンくずリストとそれに対応する動作は、**[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**&#x200B;で定義できます。 また、定義したパンくずリストごとに一意の名前を割り当てる必要があります。 パンくずリストXMLノードは、定義されたパンくずリストのすべてに対して反復処理を行います。 検索結果に階層リンクを1つだけ表示することをお勧めします。

次の例では、顧客がファセットを下に絞り込むたびに、ファセット内の階層リンクに選択が追加されます。 各項目は`<breadcrumb-item>`として表されます。

パンくずノードの例：

```xml
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;sp_cs=UTF-8;view=xml]]></link> 
   <value><![CDATA[mens]]></value> 
                <label><![CDATA[]]></label> 
      </breadcrumb-item> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;q1=Channel;sp_cs=UTF-8;view=xml;x1=brand]]></link> 
   <value><![CDATA[Channel]]></value> 
                <label><![CDATA[brand]]></label> 
      </breadcrumb-item> 
   </breadcrumb> 
    </breadcrumbs> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>パンくず </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p> 各パンくずリストを定義する0-n個のパンくずノードが含まれます。 ほとんどの顧客はパンくずリストを1つだけ持っています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>パンくず </p> </td> 
   <td colname="col2"> <p>パンくず </p> </td> 
   <td colname="col3"> <p> 階層リンクの定義を定義する子ノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>パンくず </p> </td> 
   <td colname="col3"> <p> 階層リンクの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>階層リンク </p> </td> 
   <td colname="col2"> <p>階層リンク内の個々の項目。 各項目は、結果セットを絞り込むたびに、トレールのステップを示します。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>階層リンク </p> </td> 
   <td colname="col3"> <p> 目的の表示を示す検索結果への相対リンク。 階層リンクをクリックすると、後続のすべての絞り込みが削除された表示が表示されます。 ドロップや削除など、他のオプションも使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>階層リンク </p> </td> 
   <td colname="col3"> <p> パンくずリスト項目の顧客表示テキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>階層リンク </p> </td> 
   <td colname="col3"> <p> labelタグは、階層リストの値のラベルを出力します。階層リストの値の詳細は、どのファセットが選択されたかによって示されます。 これは、ガイド付き階層リンクブロックのコンテキストでのみ使用されます。 クエリ用語の手順の場合、これは空白です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カスタムフィールド{#section_38DD31AFE5DD4263A63644AFF484E0F4}

カスタムフィールドは、グローバルコンテキストを持つ各種変数のコレクションです。 通常、この変数は、検索結果ページのメタデータに設定されたSEOの目的で変数を渡すために使用されます。

カスタムフィールドノードの例：

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>カスタムフィールド </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p> カスタムフィールドを定義する0 ～ n個の子ノードを含めることができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>custom-field </p> </td> 
   <td colname="col2"> <p>カスタムフィールド </p> </td> 
   <td colname="col3"> <p> オプション. name属性で示される、特定のカスタムフィールドの値が含まれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ファセット{#section_BE98990E3DD748A1BD4E0CA322314B79}

ファセットは、結果をフィルタリングする機能を提供する細分オプションです。 ファセットは、一般に、分類、価格範囲、色の選択、その他の属性の細分化に使用されます。 ファセットは、インデックス内のメタデータの上に構築されます。

顧客がカテゴリー内を下に移動すると、「カテゴリーファセット」を表示または非表示にするのが一般的です。 最も高いレベルの分類(カテゴリ)を階層1と呼びます。 お客様が階層1のオプションをクリックすると、階層2（サブカテゴリ）の細分オプションが表示され、階層1のオプションは表示されなくなります。 お客様が階層2のオプションをクリックすると、階層3（サブサブサブサブカテゴリ）の細分オプションが表示され、階層2のオプションが消えます。 上記のように、これらのオプションは非表示になり、表示されます。webアプリケーションは影響を与えません。

各ファセットは`<facet-item>`タグ内に含まれます。 次の例では、顧客が「休日」で検索結果を絞り込むことのできるファセットを1つ示しています。

ファセットブロックの例：

```xml
<facets>          
     <facet> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undo-link> 
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;q2=Mens;sp_staged=1;view=xml;x1=brand;x2=leveli]]></link> 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undolink> 
      </facet-value> 
      </facet> 
     <facet> 
         <facet-title><![CDATA[Sub-Category]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>0</selected> 
      <facet-value>           
              <label><![CDATA[Apparel]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans;q3=Apparel;sp_staged=1;view=xml;x1=leveli;x2=brand;x3=levelii]]></link> 
       <count><![CDATA[3]]></count>                         
      </facet-value>   
      </facet>         
     <facet> 
         <facet-title><![CDATA[Brand]]></facet-title> 
                <behavior><![CDATA[multi-select]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undo-link> 
      <facet-value>        
              <label><![CDATA[Amoura]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Amoura;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[9]]></count>                         
      </facet-value>   
      <facet-value>         
              <label><![CDATA[Armora]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[12]]></count>                        
      </facet-value>   
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Armora Jeans]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora+Jeans;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undolink> 
      </facet-value>   
      <facet-value>           
              <label><![CDATA[Art of Grooming]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Art+of+Grooming;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count>                         
      </facet-value>   
      <facet-value>          
              <label><![CDATA[Bear Co.]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Bear+Co.;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[1]]></count> 
      </facet-value> 
      <facet-value>      
              <label><![CDATA[Citizens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Citizens;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[D&amp;B]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|D%26B;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[17]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[David Yuri]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|David+Yuri;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[2]]></count>    
      </facet-value>   
      </facet> 
    </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ファセット </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>各ファセットを表す0-n個の子ノードを持つコンテナファセットノード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ファセット </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p> 単一のファセットインスタンス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet-title </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p>ファセットに対する顧客対応のタイトル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>行動 </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p>ファセットの動作。 例えば、normal、sticky、multi-selectなどです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selected </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p>ファセットに選択された値がある場合は1、それ以外の場合は0。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>元に戻すリンク </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p> ファセットが選択された場合にのみ表示されます。 「リンクを元に戻す」は、ファセット全体を元に戻します。 例えば、複数選択ファセットの場合、ファセットに対して選択されたすべてのオプションの選択が解除されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ファセット値 </p> </td> 
   <td colname="col2"> <p>ファセット </p> </td> 
   <td colname="col3"> <p>ファセットに属する個々のファセット項目がすべて含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selected </p> </td> 
   <td colname="col2"> <p>ファセット値 </p> </td> 
   <td colname="col3"> <p>ファセットを含む現在の項目が選択されている場合、このノードが存在し、「true」に設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>ファセット値 </p> </td> 
   <td colname="col3"> <p>ファセットオプションの顧客対応ラベル。 デフォルトでは、既にHTMLエスケープが使用されているはずです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>ファセット値 </p> </td> 
   <td colname="col3"> <p> オプションをさらに絞り込む結果への相対リンク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>count </p> </td> 
   <td colname="col2"> <p>ファセット値 </p> </td> 
   <td colname="col3"> <p>絞り込まれた結果セットの結果数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>元に戻すリンク </p> </td> 
   <td colname="col2"> <p>ファセット値 </p> </td> 
   <td colname="col3"> <p>ファセット値を選択すると、ノードは「元に戻すリンク」を返します。このリンクを使用すると、顧客は個々のファセット選択を選択し直すことができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ヘッダー {#section_5305B1DC5774439485CA0665DB683F9C}

例：

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## メニューと並べ替え{#section_A34CBB645DBF4C70A12A5B7E81211295}

結果を並べ替えるためのメニューがサポートされており、1ページに返す結果の数を変更できます。 また、「ナビゲーションとして検索」を使用するのに便利なナビゲーションメニューもサポートしています。 アカウントでは、同じ種類の複数のメニューを定義し、任意のメニューを使用して表示できます。

メニューノードの例：

次の例は、3つのオプションから成る並べ替えメニューとナビゲーションメニューのデータを示しています。 並べ替えメニューを使用すると、顧客は関連性、タイトルまたは評価で並べ替えることができます。 現在選択されているアイテムには、「selected=true」属性が含まれています。 &quot;. 常に関連性のあるオプションをオファーし、顧客が最初に表示されたデフォルトの検索結果に戻れるようにします。

```xml
<menus> 
        <menu> 
           <name><![CDATA[sort]]></name>         
             <item selected="true"> 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>   
                    <item> 
                        <label><![CDATA[WOMEN'S]]></label> 
          <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[MEN'S]]></label> 
          <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
          <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
          <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
          <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
          <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[GIFTS & HOME]]></label> 
          <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[CHILDREN & TOYS]]></label> 
          <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[ELECTRONICS]]></label> 
          <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link> 
                    </item> 
        </menu> 
    </menus> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>メニュー </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>各メニューを定義する0-n個の子ノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>メニュー </p> </td> 
   <td colname="col2"> <p>メニュー </p> </td> 
   <td colname="col3"> <p>メニューの単一のインスタンス（<span class="uicontrol">デザイン</span> &gt; <span class="uicontrol">ナビゲーション</span> &gt; <span class="uicontrol">メニュー</span>で定義されているメニューに対応）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>メニュー </p> </td> 
   <td colname="col3"> <p>メニューの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>item </p> </td> 
   <td colname="col2"> <p>メニュー </p> </td> 
   <td colname="col3"> <p>メニューの各項目を定義します。 選択したオプションの属性は、指定したメニュー項目が現在選択されている場合はtrueに設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>メニュー項目の顧客向けテキスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>メニュー項目の値(メニューが設定されるクエリパラメーターの値)を表します。 &lt;link&gt;値を使用する場合、このタグは不要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>選択されていないオプションの場合、&lt;link&gt;パラメーターには、同じ結果セットを返す相対リンクが含まれますが、メニューオプションが適用されます。 現在選択されている並べ替えオプションでは、このフィールドは空白です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ページ番号{#section_E52F81C6A6EB4B8F996157B657EC540F}

結果セットは複数のページに分割されます。 通常、1つのページに10 ～ 20件の結果が表示されます。 以降の結果は次のページに表示されます。 ページネーションXMLを使用すると、結果セットをページ単位で閲覧できるように、一連のナビゲーションリンクを作成できます。 次の4つのナビゲーションリンクを使用できます。first、last、nextおよびprevious。 各リンクタイプを使用すると、顧客はページ間をすばやく移動できるので、探しているものを簡単に確認し、絞り込むことができます。

次の例は、5ページへのリンクを表示するようにページ番号が設定された最初のページの検索のページ番号を示しています。

ページネーションの例：

```xml
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
        </pages> 
    </pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ページ </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p> 結果の合計ページ数を、結果の数をページあたりの結果の数で割った値に基づきます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>合計ページ数 </p> </td> 
   <td colname="col2"> <p>ページ </p> </td> 
   <td colname="col3"> <p>検索結果が見開きになるページの合計数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ページ </p> </td> 
   <td colname="col2"> <p>ページ </p> </td> 
   <td colname="col3"> <p>ページネーションの各ページを定義する0-nページのノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>page </p> </td> 
   <td colname="col2"> <p>ページ </p> </td> 
   <td colname="col3"> <p>次の4つの特別なページノードが存在します。first、last、previous、nextの3つの値を指定します。 これらの4つのページはオプションで、意味がある場合にのみ結果セットに表示されます。 例えば、1ページ目の場合は、「前の」リンクはありません。 他のすべてのページは、位置を示しています。 表示されるページ数は、ページネーションユーザーインターフェイスで設定される「ページへのリンク数」によって異なります。 「selected」属性は、顧客が現在閲覧しているページを示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## クエリ {#section_3DAA1013F09742869B80F6A361816E6C}

クエリノードの例：

```xml
    <query> 
        <user-query><![CDATA[mens]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[265]]></total-results> 
    </query> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p> クエリの概要を提供するグローバルノード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ユーザークエリ </p> </td> 
   <td colname="col2"> <p>クエリ </p> </td> 
   <td colname="col3"> <p> 検索されたキーワード。 <span class="uicontrol"> 「お客様の意味</span>」が、結果を得られない元の用語が原因で自動的に推奨キーワードを検索した場合、検索された新しいキーワードに反映されます（元のキーワードを取得するには、提案ノードを参照してください）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>低い結果 </p> </td> 
   <td colname="col2"> <p>クエリ </p> </td> 
   <td colname="col3"> <p> このページの最初の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>上位の結果 </p> </td> 
   <td colname="col2"> <p>クエリ </p> </td> 
   <td colname="col3"> <p> このページの最後の結果のアイテム番号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>合計結果数 </p> </td> 
   <td colname="col2"> <p>クエリ </p> </td> 
   <td colname="col3"> <p> ユーザークエリと一致する結果の合計数です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 最近実行した検索 {#section_17F942F6EC07456DABED7A483AC08446}

最近の検索はcookieベースの機能で、cookieの情報をサイトの検索/マーチャンダイジングサーバーにリレーした場合にのみ機能します。

最近の検索の例：

```xml
    <recent-searches> 
        <clear-link><![?q=womens&gscr=clear]]></clear-link> 
        <recent-search> 
            <link><![?q=mens]]></link> 
            <label><![CDATA[mens]]></label> 
        <recent-search> 
    </recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>最近の検索 </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>ノードは、検索に最近の検索がある場合にのみ存在します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clear-link </p> </td> 
   <td colname="col2"> <p>最近の検索 </p> </td> 
   <td colname="col3"> <p>顧客の最近の検索をすべてクリアする相対パス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>最近の検索 </p> </td> 
   <td colname="col2"> <p>最近の検索 </p> </td> 
   <td colname="col3"> <p>最近の検索を定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>最近の検索 </p> </td> 
   <td colname="col3"> <p>ユーザーが最近実行した検索を実行するリンクを作成するパスです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>最近の検索 </p> </td> 
   <td colname="col3"> <p>最近の検索で顧客に表示する表示ラベル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 結果 {#section_155A80B8C4F641678DD9C8F257108412}

結果セットは、XML応答のカスタマイズ可能な領域です。 各インデックスは、メタデータのフィールド命名メカニズムで一意です。 タイトル、説明、URLなど、各結果に対して返される共通フィールドがあります。 ただし、インデックス内のページに対して定義されたメタデータは、各結果ノードで使用できるようになります。 分類、価格、色、サムネールは、検索結果をより説得力のあるものにするために、結果に適用できるオプションの一部にすぎません。

結果の形式は、実装に固有のメタデータに基づいてカスタマイズされます。 サムネール画像のURLを含む、結果に表示する結果ごとのデータがここに含まれます。

さらに、「特集結果」などの複数の結果ゾーンをページ内に設定したり、「製品」と「コンテンツ」の結果セクションを個別に設定したりできます。 この場合、ファセットは主な結果セットにのみ関連付けられますが、複数の結果ゾーンがHTML内に提供されます。

結果ノードの例：

```xml
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
                    <field name="sku"><![CDATA[200190]]></field> 
                    <field name="pagename"><![CDATA[Relaxed Paint Splattered]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>   
         <result> 
                    <field name="index"><![CDATA[2]]></field> 
                    <field name="sku"><![CDATA[200195]]></field> 
                    <field name="pagename"><![CDATA[Tumbled Jeans]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[235]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>    
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
                    <field name="sku"><![CDATA[200196]]></field> 
                    <field name="pagename"><![CDATA[Montana Relaxed]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[220]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>         
        </result-set>   
    </results> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>結果の表示 </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>0-n個の結果セットのコンテナノード。 結果セットがゼロの場合、特別な結果なしランディングページになっていることを意味します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>result-set </p> </td> 
   <td colname="col2"> <p>結果の表示 </p> </td> 
   <td colname="col3"> <p>入力検索では、複数の検索を実行できます。 各結果セットには、実行された特定の名前付き検索の結果が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>result-set </p> </td> 
   <td colname="col3"> <p>結果セットが属する検索の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>result </p> </td> 
   <td colname="col2"> <p>result-set </p> </td> 
   <td colname="col3"> <p>結果セットの個々の結果に関連付けられているすべてのフィールドが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>field </p> </td> 
   <td colname="col2"> <p>result </p> </td> 
   <td colname="col3"> <p>name属性は、表示されるインデックス内のフィールドの名前を定義します。 値は、そのフィールドの実際の値です。 結果によっては、個々の結果に関連のないフィールドが見つからない場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 検索フォーム{#section_9E4B99D4FEDC49629F6C7E866F3A7493}

検索フォームは、顧客が動的に検索フォームを作成できるように、結果セットに含まれています。 この手順はオプションです。 ほとんどの顧客は固定検索フォームを持っています。 ただし、A:Bテストを実行するビジネスルールが1つ以上あることに基づいて、検索フォームにTest&amp;Bターゲットmboxが必要かどうかを判断することはできます。 同様に、最新のオートコンプリートCSSとJavaScriptを自動的に取得できます。

検索フォームXMLの例：

```xml
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>search-form </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>検索フォームを駆動するためのデータが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>include-tnt-mbox </p> </td> 
   <td colname="col2"> <p> search-form </p> </td> 
   <td colname="col3"> <p>技術的には、Test&amp;Bテストを実行するビジネスルールが1つ以上ある場合、検索フォームでmboxのみが必要となります。 このノードは、Test&amp;Testターゲットサーバーでのヒット数を減らすためにmboxが必要かどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>autocomplete </p> </td> 
   <td colname="col2"> <p>search-form </p> </td> 
   <td colname="col3"> <p>オートコンプリートに関連する子ノードを格納します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有効 </p> </td> 
   <td colname="col2"> <p>autocomplete </p> </td> 
   <td colname="col3"> <p>検索アカウントでオートコンプリートを使用する場合は1に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> autocomplete </p> </td> 
   <td colname="col3"> <p> オートコンプリート用のCSS。 このノードをページのできるだけ上に配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> form-content </p> </td> 
   <td colname="col2"> <p>autocomplete </p> </td> 
   <td colname="col3"> <p>検索フォームに挿入されるコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>autocomplete </p> </td> 
   <td colname="col3"> <p>オートコンプリート用のJavaScript。 このノードをページ上でできる限り低い位置に配置します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 提案{#section_2899FACB9AD84F60B3687C1B4EF09E15}

**[!UICONTROL Did You Mean]**&#x200B;機能の設定は、次の3つの方法で行うことができます。結果がないので提案を行う、結果がない場合は最初の提案を自動的に検索する、結果が少ない場合は結果が少ない場合は結果が少ない場合は結果数が多い場合は提案を行う。 すべての提案が結果を生み出します。

この提案ノードには、成功したクエリをもたらす用語が含まれています。 また、顧客が新しいクエリにジャンプできるように、リンクが返されます。

検索結果が0件の場合の提案の出力例：

```xml
    <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>0</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=arcade;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[arcade]]></word> 
 </suggestion-item>    
    </suggestions>
```

サーチクエリに対する自動検索の出力例：

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

結果が低いための提案の出力例：

```xml
   <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>1</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=coffee;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[coffee]]></word> 
 </suggestion-item>  
    </suggestions> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>提案 </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p> 提案が存在する場合は、その提案を定義する子ノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>自動検索 </p> </td> 
   <td colname="col2"> <p>提案 </p> </td> 
   <td colname="col3"> <p> 存在する場合は、結果がないために新しい用語に対してサイト検索/マーチャンダイジングが自動的に検索されるかどうかを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>オリグクエリ </p> </td> 
   <td colname="col2"> <p>提案 </p> </td> 
   <td colname="col3"> <p> サイト検索/マーチャンダイジングが最初の提案に対して自動的に検索を行う場合、クエリノードのユーザクエリは、検索対象のキーワードを示します。 このノードは、元のクエリ用語を表示します。 この2つを組み合わせることで、「アーケースではなくアーケードの検索」などの構造を作成できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>提案件数が少ない </p> </td> 
   <td colname="col2"> <p>提案 </p> </td> 
   <td colname="col3"> <p>このキーワードがある場合は、現在の検索用語が検索結果を少なくしているためにサイト検索/マーチャンダイジングが提案を行っているか、および提案が非常に高い結果を生み出しているかを示します。 2つのしきい値は、<span class="uicontrol"> 「お使いの意味</span>」で設定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>提案項目 </p> </td> 
   <td colname="col2"> <p>提案 </p> </td> 
   <td colname="col3"> <p>様々な提案を示す0 ～ nのノードが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>提案項目 </p> </td> 
   <td colname="col3"> <p>推奨された用語へのリンクを作成するためのパスが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>word </p> </td> 
   <td colname="col2"> <p>提案項目 </p> </td> 
   <td colname="col3"> <p> 推奨される単語が含まれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## テンプレート{#section_1E2BB2F274B04F5491A4CCCC38F507BD}

結果に基づいて顧客の検索エクスペリエンスを切り替える機能がサポートされます。 その一部として、検索結果のレイアウトを変えて、異なるテンプレートを切り替えることがあります。 例えば、多数の製品がある場合に、グリッド表示の製品を含むテンプレートがあるとします。 また、より詳細な単一の結果を表示する場合に、「スポットライト」テンプレートを使用することもできます。 検索結果が得られない場合は、「検索結果なし」のテンプレートを使用することもできます。 テンプレートノードは、検索結果の表示に使用されるテンプレートを示します。

サンプルテンプレート：

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>template </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>検索結果の表示に使用されるテンプレートの名前を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ゾーン{#section_26C4A947E7B1474A8E37D86D9579B93E}

ゾーンとは、ビジネスルールによってオンまたはオフにできるページのセクションです。 ゾーンには、ファセット、検索、パンくずリスト、静的コンテンツなど、任意のコンテンツを含めることができますが、これらに限定されません。 顧客のWebページのゾーンは、サイト検索/マーチャンダイジングと同じ領域にマップする必要があります。

ゾーンノードの例：

```xml
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ノード </p> </th> 
   <th colname="col2" class="entry"> <p>親ノード </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ゾーン </p> </td> 
   <td colname="col2"> <p>顧客の結果 </p> </td> 
   <td colname="col3"> <p>0 ～ n個のゾーンが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ゾーン </p> </td> 
   <td colname="col2"> <p>ゾーン </p> </td> 
   <td colname="col3"> <p> 個々のゾーンノード。 複数のゾーンノードを持つことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>ゾーン </p> </td> 
   <td colname="col3"> <p>ゾーンの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>display </p> </td> 
   <td colname="col2"> <p>1または0。ゾーン名に対応するゾーンを表示するか、非表示にするかを示します。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

Geometrixxと呼ばれる架空のWebサイト上の*検索用の出力例と、サンプル出力の作成に使用されるサンプルプレゼンテーションテンプレートです。

* [出力例](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [プレゼンテーションテンプレートの例](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## 出力例{#section_515C000A18B847D59097D0A9CCC02636}

Geometrixxと呼ばれる架空のWebサイト上の*検索の出力例です。

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[*]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[1337]]></total-results> 
    </query> 
 
    <custom-fields> 
 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name>

             <item selected="true"> 
 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item>

             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=*;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>

                    <label><![CDATA[WOMEN'S]]></label> 
      <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link>

                    <label><![CDATA[MEN'S]]></label> 
      <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
      <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link>

                    <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
      <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
      <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link>

                    <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
      <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link>

                    <label><![CDATA[GIFTS & HOME]]></label> 
      <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link>

                    <label><![CDATA[CHILDREN & TOYS]]></label> 
      <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link>

                    <label><![CDATA[ELECTRONICS]]></label> 
      <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link>

        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
       
  <breadcrumb-item> 
    <link><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></link> 
    <value><![CDATA[*]]></value> 
                        <label><![CDATA[]]></label> 
   </breadcrumb-item> 
          
   </breadcrumb> 
 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched>0</auto-searched> 
         
        <suggestions-low-results>0</suggestions-low-results> 
         
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
      
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

        </pages> 
    </pagination> 
 
    <facets>  
         
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected>0</selected>

      <facet-value> 
           
              <label><![CDATA[Womens]]></label> 
 
       <link><![CDATA[?i=1;q=*;q1=Womens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[219]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Mens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[202]]></count> 
                         
      </facet-value> 
   
      <facet-value>

              <label><![CDATA[Beauty &amp; Fragrance]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Beauty+%26+Fragrance;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[169]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Children &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Children+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[209]]></count> 
                         
      </facet-value>

      <facet-value> 
           
              <label><![CDATA[Electronics &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Electronics+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[200]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Gifts &amp; Home]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Gifts+%26+Home;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[156]]></count>

      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Jewelry &amp; Accessories]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Jewelry+%26+Accessories;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[182]]></count> 
                         
      </facet-value> 
   
      </facet-item> 
  
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
               
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[2]]></field> 
      <field name="brand"><![CDATA[One For All]]></field> 
      <field name="price"><![CDATA[145]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[208]]></field> 
 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[4]]></field> 
      <field name="brand"><![CDATA[Vera Watson]]></field> 
      <field name="price"><![CDATA[850]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Dresses,  
          Day]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[5]]></field> 
 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[6]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[80]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[7]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[85]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[8]]></field> 
      <field name="brand"><![CDATA[Woolberry]]></field> 
 
      <field name="price"><![CDATA[280]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[9]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[10]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[55]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[11]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[45]]></field> 
 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[12]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[47]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
      
        </result-set>   
    </results>

    <banners> 
         
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
            </banner>

    </banners> 
 
    <zones> 
        <zone> 
 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

## プレゼンテーションテンプレートの例{#section_AD42571DFB88491AA7F0FDF0929EBE97}

上記の出力例の作成に使用するプレゼンテーションテンプレートの例を次に示します。

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[<guided-query-param gsname="q" />]]></user-query> 
 <lower-results><![CDATA[<guided-results-lower>]]></lower-results> 
 <upper-results><![CDATA[<guided-results-upper>]]></upper-results> 
 <total-results><![CDATA[<guided-results-total>]]></total-results> 
    </query> 
 
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[<guided-general-field gsname="default" field="seo_search_keywords"/>]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name> 
     <guided-menu gsname="sort"> 
         <guided-if-menu-item-selected> 
             <item selected="true"> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
        <guided-else-menu-item-selected> 
             <item> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[<guided-menu-item-path />]]></link>     
             </item> 
        </guided-if-menu-item-selected> 
    </guided-menu> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name> 
            <guided-menu gsname="ss_head_nav"> 
                <guided-if-menu-item-selected> 
                    <item selected="true"> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                <guided-else-menu-item-selected> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                </guided-if-menu-item-selected> 
            </guided-menu>  
        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
      <guided-breadcrumb gsname="default"> 
  <breadcrumb-item> 
    <link><![CDATA[<guided-breadcrumb-path gsname="goto">]]></link> 
    <value><![CDATA[<guided-breadcrumb-value />]]></value> 
                        <label><![CDATA[<guided-breadcrumb-label>]]></label> 
   </breadcrumb-item> 
         </guided-breadcrumb> 
   </breadcrumb> 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched><guided-if-suggestion-autosearch>1<guided-else-suggestion-autosearch>0</guided-if-suggestion-autosearch></auto-searched> 
        <guided-if-suggestion-autosearch><orig-query><![CDATA[<guided-suggestion-original-query/>]]></orig-query></guided-if-suggestion-autosearch> 
        <suggestions-low-results><guided-if-suggestion-low-results>1<guided-else-suggestion-low-results>0</guided-if-suggestion-low-results></suggestions-low-results> 
        <guided-suggestions> 
     <suggestion-item> 
         <link><![CDATA[<guided-suggestion-path />]]></link> 
  <word><![CDATA[<guided-suggestion />]]></word> 
     </suggestion-item> 
 </guided-suggestions> 
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[<guided-page-total />]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[<guided-page-path gsname="first" />]]></page> 
     <page position="last"><![CDATA[<guided-page-path gsname="last" />]]></page> 
     <guided-if-page-prev><page position="prev"><![CDATA[<guided-page-path gsname="prev" />]]></page></guided-if-page-prev> 
     <guided-if-page-next><page position="next"><![CDATA[<guided-page-path gsname="next" />]]></page></guided-if-page-next> 
     <guided-if-page-viewall><page position="viewall"><![CDATA[<guided-page-path gsname="viewall" />]]></page></guided-if-page-viewall> 
     <guided-if-page-viewpages><page position="viewall"><![CDATA[<guided-page-path gsname="viewpages" />]]></page></guided-if-page-viewpages> 
 
     <guided-pages> 
                <guided-if-page-selected><page position="<guided-page-number />" selected="true"><![CDATA[<guided-page-path />]]></page> 
  <guided-else-page-selected><page position="<guided-page-number />"><![CDATA[<guided-page-path />]]></page> 
  </guided-if-page-selected> 
     </guided-pages> 
        </pages> 
    </pagination> 
 
    <facets>  
        <guided-facet gsname="leveli"> 
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected><guided-if-facet-selected>1<guided-else-facet-selected>0</guided-if-facet-selected></selected> 
                <guided-if-facet-selected><undo-link><![CDATA[<guided-facet-undo-path gsname="leveli">]]></undo-link></guided-if-facet-selected> 
  <guided-facet-values> 
      <facet-value> 
          <guided-if-facet-value-selected><selected><![CDATA[true]]></selected></guided-if-facet-value-selected> 
              <label><![CDATA[<guided-facet-value>]]></label> 
       <link><![CDATA[<guided-facet-value-path />]]></link> 
       <count><![CDATA[<guided-facet-count>]]></count> 
                        <guided-if-facet-value-selected><undolink><![CDATA[<guided-facet-value-undo-path />]]></undolink></guided-if-facet-value-selected> 
      </facet-value> 
  </guided-facet-values> 
      </facet-item> 
 </guided-facet> 
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
            <guided-results gsname="default">   
         <result> 
                    <field name="index"><![CDATA[<guided-result-index />]]></field> 
      <field name="brand"><![CDATA[<guided-result-field gsname="brand" />]]></field> 
      <field name="price"><![CDATA[<guided-result-field gsname="price" />]]></field> 
      <field name="foundIn"><![CDATA[<guided-if-result-field gsname="leveli"><!--tmpl_var name='leveli'-->, </guided-if-result-field> 
            <guided-if-result-field gsname="levelii"><!--tmpl_var name='levelii'-->, </guided-if-result-field> 
          <guided-if-result-field gsname="leveliii"><!--tmpl_var name='leveliii'--></guided-if-result-field>]]></field> 
         </result>   
     </guided-results> 
        </result-set>   
    </results> 
 
    <guided-if-recent-searches> 
    <recent-searches> 
        <clear-link><guided-recent-searches-clear-path/></clear-link> 
        <guided-recent-searches> 
            <recent-search> 
                <link><guided-recent-searches-path></link> 
                <label><guided-recent-searches-value></label> 
            <recent-search> 
        </guided-recent-searches> 
    </recent-searches> 
    </guided-if-recent-searches> 
 
    <banners> 
        <guided-if-banner-set gsname="top"> 
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<guided-banner gsname="top">]]></content> 
            </banner> 
        </guided-if-banner-set> 
        <guided-if-banner-set gsname="bottom"> 
            <banner> 
                <area><![CDATA[bottom]]></area> 
                <content><![CDATA[<guided-banner gsname="bottom">]]></content> 
            </banner> 
        </guided-if-banner-set> 
    </banners> 
 
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display><guided-if-zone gsname="brand-facet">1<guided-else-zone>0</guided-if-zone></display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox><guided-if-tnt-business-rules>1<guided-else-tnt-business-rules>0</guided-if-tnt-business-rules></include-tnt-mbox> 
        <autocomplete> 
            <enabled><guided-if-autocomplete>1<guided-else-autocomplete>0</guided-if-autocomplete></enabled> 
            <css><![CDATA[<guided-ac-css/>]]></css> 
            <form-content><![CDATA[<guided-ac-form-content/>]]></form-content> 
            <javascript><![CDATA[<guided-ac-javascript/>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

