---
description: ファセットを使用して、プレゼンテーションレイヤーをカスタマイズし、ユーザーに対して、検索結果をドリルダウンできるガイド付き検索を提供できます。
seo-description: ファセットを使用して、プレゼンテーションレイヤーをカスタマイズし、ユーザーに対して、検索結果をドリルダウンできるガイド付き検索を提供できます。
seo-title: ファセットについて
solution: Target
subtopic: Navigation
title: ファセットについて
topic: Design,Site search and merchandising
uuid: 28bc4d4d-a84c-4a77-befb-b0fb3bbdb966
translation-type: tm+mt
source-git-commit: 52c8d7985e7cb0aa35be1deabeb7cb92a55f07c2

---


# ファセットについて{#about-facets}

ファセットを使用して、プレゼンテーションレイヤーをカスタマイズし、ユーザーに対して、検索結果をドリルダウンできるガイド付き検索を提供できます。

## ファセットの使用 {#concept_FA912B3B41EE493DB2F492D188457FF5}

例えば、ツールを販売するWebサイトの訪問者がレンチを検索したとします。 会社は次の2つのファセットを使用できます。1つは検出されたすべてのレンチのブランドを指定し、もう1つはレンチのサイズを指定します。 顧客は、適切なファセット内のブランドやサイズをクリックして、結果を絞り込み、必要なレンチをすばやく見つけることができます。

既存のメタデータ定義を基にファセットを作成できます。 メタデータで日付タイプとして定義されたファセットは、日付範囲ファセットとして表示されます。

ページの表には、追 [!DNL Staged Facets] 加された各ファセットを構成する設定の一般的な概要が表示されます。 新しいファセットを追加したり、既存のファセットを編集または削除したりできます。 ページの右上隅近くにあるを使用して、ファセットに対して行っ **[!UICONTROL History]** た変更を元に戻すことができます。

ファセット設定は、デフォルトでステージングされ、変更をテストしてからライブにプッシュできます。

ステージング [についてを参照してくださ](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)い。

を使用して、ステ **[!UICONTROL View Live Settings]** ージ設定を現在のライブ設定と比較できます。 ステージ **[!UICONTROL View Staged Settings]** ング領域に戻る場合に使用します。 ステージングされたアイテムの場合、設定のライブバージョンは読み取り専用です。 したがって、ステージ設定をライブにプッシュすることで操作できます。 ステージされたファセットに対して行った変更に満足したら、をクリックして変更を **[!UICONTROL Push Live]** ライブにプッシュします。

## 日付範囲ファセット {#section_FEFFF6B5B6534456913189FEF559BA58}

メタデータのDate型として定義されたファセットは、他のファセットとは異なる方法で処理されます。 値のセットとして扱われるのではなく、開始日、終了日、またはその両方を含む日付範囲として扱われます。

日付範囲ファセットには、開始日の後に「BTW」（「次の範囲内」の場合）が続き、終了日が続きます。 日付の形式は次の2つです。

mm-dd-yyyy

年 / 月 / 日

4桁の年が必要です。 開始日または終了日の少なくとも1つが必要ですが、両方が必須ではありません。 例えば、「12/1/2007BTW1/4/2009」は、2007年12月1日から2009年1月4日までのすべての日付を意味します。 ただし、「1-1-2005BTW」は、2005年1月1日からのすべての日付を意味します。

通常のファセットと同様、プレゼンテーシ `<guided-facet-value/>` ョンテンプレートタグを使用して、日付範囲ファセットの値を取得できます。 現在、検索する日付範囲の入力をユーザーに許可するにはJavaScriptが必要です。 例えば、開始日と終了日の2つの入力フィールドから入力を受け取ることができます。 次に、入力を検証し、（2つの入力フィールドから作成された）新しいファセットの値とファセット名を既存のURLに追加します。

プレゼンテーシ [ョンテンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)い。

次のコード例は、ページに日付範囲を表示する方法の例です。 既存の日付範囲が選択されている場合は、その日付範囲が表示されます。それ以外の場合は、単純な入力フォームが表示されます。 フォームが送信されると、単純な検証が実行されます。 次に、2つの新しいパラメーターを含む新しいURLにブラウザーを送信します。

* `q#` - 2つの入力フィールドからアセンブリされた、選択した日付範囲を表します。
* `x#`  — ファセットの名前を指定します。 この例では、日付範囲ファセットの名前は「変更済み」です。

Apacheはセ `replace(/%2F/ig, '~2F')``%2F` キュリティ上の理由でURLパスを許可しておらず、SEO URLを使用する場合はURLパスにクエリが含まれるので、コードの各部分が必要です。 したがって、 `/` は通常URL内にあ `~2F` るので、 `%2F`の代わりに、のようにエンコードされます。

```
<div class="date_range"> 
 <p>Date Range</p> 
 <guided-if-facet-selected gsname="modified"> 
  <guided-facet-values gsname="modified"> 
   <script> 
   var modified_daterange= '<guided-facet-value />'.split(/BTW/) ; 
   if (modified_daterange[0]=='') modified_daterange[0]= '--/--/----' ; 
   if (modified_daterange[1]=='') modified_daterange[1]= '--/--/----' ; 
   document.write('From: ' + modified_daterange[0]) ; 
   document.write('<br>To: ' + modified_daterange[1]) ; 
   </script> 
  </guided-facet-values> 
 
 <guided-else-facet-selected> 
  <form action="#"> 
   From: <input name="dateFrom" size=10> 
   <br>To: <input name="dateTo" size=10> 
   <br><input type="button" value="Go" onclick="goClick(this.form)"> 
  </form> 
  <script> 
  function goClick(f) { 
   if (f.dateFrom.value=='' && f.dateTo.value=='') { 
    alert('You must enter either a From: date or a To: date.') ; 
    return ; 
   } 
   if ( f.dateFrom.value!='' && !f.dateFrom.value.match(/^\d+[\/\-]\d+[\/\-]\d\d\d\d$/) ) { 
    alert('From: date must be in "mm/dd/yyyy" or "mm-dd-yyyy" format.') ; 
    return ; 
   } 
   if ( f.dateTo.value!='' && !f.dateTo.value.match(/^\d+[\/\-]\d+[\/\-]\d\d\d\d$/) ) { 
    alert('To: date must be in "mm/dd/yyyy" or "mm-dd-yyyy" format.') ; 
    return ; 
   } 
   // Note that "/" is encoded as "~2F" instead of "%2F" to avoid Apache 404 error. 
   var new_url= '<guided-current-path />&<guided-query-param-name gsname="q#" offset="0" />=' 
    + encodeURIComponent(f.dateFrom.value).replace(/%2F/ig, '~2F') + 'BTW' 
    + encodeURIComponent(f.dateTo  .value).replace(/%2F/ig, '~2F') 
    + '&<guided-query-param-name gsname="x#" offset="0" />=modified' ; 
   location.href= new_url ; 
  } 
  </script> 
 </guided-if-facet-selected> 
</div>
```

## ネストされたファセットについて {#section_6BC77F38DE9F43D5B6911F8CECB15DFC}

ネストされたファセットは、次のように複数レベルのカテゴリを表示するファセットです。

![](assets/nestedfacets.png)

「女性」カテゴリと「男性」カテゴリは、上位または親ファセットにあります。 「アクセサリ」や「靴」などのサブカテゴリは、下部ファセットまたは子ファセットにあります。

現在サポートされているネストされたファセットの深さは2ですが、ドリルダウンリストの任意の場所に置くことができます。

次に、様々なタイプのネストされたファセットの動作を示します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ネストされたファセットタイプの動作 </p> </th> 
   <th colname="col2" class="entry"> <p>動作 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>標準 </p> </td> 
   <td colname="col2"> <p>通常のネストされたファセットの動作は、他のファセットが検索を絞り込むと縮小するという点です。 </p> <p>ネストされたファセットを選択すると、選択範囲に向かって縮小されます。 親ファセットが選択されている場合は、その親のみが残りの子ファセットと共に表示されます。 子ファセットを選択した場合は、選択した親ファセットと選択した子ファセットのみが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>固定 </p> </td> 
   <td colname="col2"> <p>共通ネストされたファセットの動作は、他のファセットまたは検索条件の状態に基づいて、できる限りファセットを開いたままにしようとすることです。 子ファセットが選択されている場合、共通の深さにカウントされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>複数選択 </p> </td> 
   <td colname="col2"> <p>複数選択ファセットの動作は、ファセットを開いたままにすることです。 新しい選択では、そのファセットがカテゴリの「親」でない限り、他のすべてのファセット選択が消去されます。 この場合、「親」とは、ネストされたファセットの最上位のカテゴリではなく、カテゴリファセットを指します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>カテゴリの複数選択 </p> </td> 
   <td colname="col2"> <p>「複数選択」に類似したネストされたファセットタイプですが、次の例外があります。 </p> 
    <ul id="ul_D5AB6AF3169A483E8F3FC6D2A2EA3A28"> 
     <li id="li_9308156EF2FF43CE9DFB933F13786C58">このファセットが初めて選択された場合、以前に選択したその他のファセットは選択解除されます。 </li> 
     <li id="li_DD96D6802A9C479283212A0FD68C6F85">親ファセットをクリックせずに、または別の親ファセットの兄弟を選択せずに、顧客が直接子ファセットにドリルダウンする場合は、以前に選択した他のファセットも選択解除されます。 </li> 
     <li id="li_8BF58F10969B4743986D5D0E0086AD6C">カテゴリーファセットには親が含まれているという意味で、親を持つことができます。 この動作と、すべてのネストされたファセットで見つかった親子関係とを混同しないでください。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

See also [About Facet Rail](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

## Adding a new facet {#task_FC07BFFA62CA4B718D6CBF4F2855C89B}

ファセットを追加して、プレゼンテーションレイヤーをカスタマイズし、顧客に対してガイド付き検索を提供して、検索結果を掘り下げることができます。

<!-- 

t_adding_a_new_facet.xml

 -->

ページのファセット表に [!DNL Facets] は、単一のファセットを構成する設定の抜粋が表示されます。 新しいファセットを追加したり、既存のファセットを編集または削除したりできます。 ファセットに対して行った変更は、履歴機能を使用して元に戻すことができます。

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートでファセットを参照していることを確認してください。

See also [About Facet Rail](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

**新しいファセットを追加するには**

1. 新しいファセットを追加する前に、次の手順に進む前に、既に次の操作を完了していることを確認します。

   * いくつかのメタタグフィールドを既に定義しておきます。

      詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。
   * インデックスにメタデータを挿入します。
フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

1. 製品メニューで、//をクリ **[!UICONTROL Design]** ックしま **[!UICONTROL Navigation]** す **[!UICONTROL Facets.]**
1. ページ上で、 [!DNL Facets] をクリックしま **[!UICONTROL Add New Facet]**&#x200B;す。
1. ページ [!DNL Add Facet] で、必要なオプションを設定します。

   これらの設定は、ファセットの動作とデフォルト表示の両方に影響します。 これらの設定の一部は、プレゼンテーションテンプレートの設定を使用して上書きできます。

   メタデータで日付タイプとして定義されたファセットは、日付範囲として表示されます。

   日付範囲 [ファセットを参照](../c-about-design-menu/c-about-facets.md#section_FEFFF6B5B6534456913189FEF559BA58)。

   選択したファセットオプションに応じて、すべてのオプションが使用できるわけではありません。

   <!-- 
   r_add_facet_options.xml
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>ファセット名 </p> </td> 
      <td colname="col2"> <p>特定のファセットの名前を識別します。 </p> <p> <p>注意： 既存のユーザ定義メタデータに基づくファセットのみを持つことができます。 ドロップダウンリストで使用できるファセットがない場合は、まずいくつかのメタデータを定義する必要があります。 </p> </p> <p>詳しくは、 <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita" scope="local"> 新しいメタタグフィールドの追加を参照してくだ </a>さい。 </p> <p>フィールドテーブルに基づいてファセットを作成するには、カスタムファセット名を使用し、フィールドテーブル名を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ラベルを表示 </p> </td> 
      <td colname="col2"> <p>メタデータのfieldname( <span class="codeph"> &lt;guided- </span> breadcrumb-label&gt;タグ付き)やスタンドアロンの値( <span class="codeph"> &lt;guided-facet-display-name&gt;タグ付き)の代わりに、パンくずリストで使用できるファセットのラベルを設定し </span> ます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>動作 </p> </td> 
      <td colname="col2"> <p>3つのファセット動作のいずれかを設定します。 </p> <p> 
      <ul id="ul_67C19E1C16224B9990F04A0D05BD3D05"> 
      <li id="li_6B232C11A61840B68CA59E1F593405A0"> <span class="uicontrol"> 標準 </span> <p>動作が「標準」に設定されているファセットを顧客がク <span class="uicontrol"> リック </span>すると、その品目の検索結果がドリルで表示されます。 このページから、検索結果の数をさらに絞り込み、さらに絞り込むことができます。 </p> </li> 
      <li id="li_7D7C43A7F7AB4B84A9B0FEF34627605A"> <span class="uicontrol"> カテゴリ </span> <p>カテゴリファセットは、ナビゲーション要素のように機能します。 これらのファセットは、顧客が通常、属性オプションを使用してファセットを表示する前にドリルスルーする最上位のファセットです。 他のファセットが選択され、開いたままの場合、カテゴリファセットは狭くなりません。 カテゴリファセット内の別の値をクリックすると、そのカテゴリファセットの親を除く、ページ上の他のすべてのファセットの選択が解除されます。 </p> </li> 
      <li id="li_01255993D71F40DBA8870AA3FEA7D304"> <span class="uicontrol"> カテゴリの複数選択 </span> <p>ファセットは、項目が「OR」されるファセットからの複数の項目の選択をサポートするカテゴリファセットです。 </p> </li> 
      </ul> 
      <ul id="ul_683F6D3FC8524E65AF303453ADDB6001"> 
        <li id="li_81F504D1D1294666BBBC5EA43B34B712"> <span class="uicontrol"> 固定 </span> <p>動作が「固定」に設定されているファセットを顧客がクリッ <span class="uicontrol"> クす </span>ると、ドリルダウン中に、選択したオプションを持つファセットが開いたままになります。 このオプションは、顧客が以前の選択を変更できるようにする場合に便利です。 </p> </li> 
      </ul> 
      <ul id="ul_8E871D63B09445268C600C8ABC20F6A4"> 
        <li id="li_F88AC5528B0C4751BC4CFE7FA9525857"> <span class="uicontrol"> 複数選択 </span> <p>ファセット内の項目を「OR」で結合する、ファセットから複数の項目を選択できます。 このオプションは、色などの小さな属性を表示するファセットで、顧客が「赤または黒の靴をサイズで表示」するクエリーを作成できるようにする場合に便利です。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>常に表示 </p> </td> 
      <td colname="col2"> <p>通常のファセットまたは共通のファセットの場合、常に顧客に表示されたままにするようにファセットを設定します。 </p> <p>このオプションは、[標準]、[カテゴリ]、または[定 <span class="uicontrol"> 着]ドロップダウンリ </span>ストから[標準]、[カテ <span class="uicontrol"> ゴリ]、または[ </span>定着]を選択した場合にの <span class="uicontrol"></span><span class="uicontrol"></span> み使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットの親 </p> </td> 
      <td colname="col2"> <p>このオプションは、「動作」ドロップダウンリ <span class="uicontrol"> ストで「カ </span> テゴリ」また <span class="uicontrol"> は「カテゴリの複数選択」を選択し </span> た場合にのみ <span class="uicontrol"></span> 使用できます。 </p> <p>カテゴリファセットの親を示します。 現在のカテゴリファセット内で使用可能な選択肢を絞り込むために、親ファセット内で選択した項目が使用されます。 顧客がカテゴリファセットを操作する場合、親ファセットの選択は解除されません。 複数の親をコンマで区切って指定できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>定着深度 </p> </td> 
      <td colname="col2"> <p>このオプションは、動作ドロップダウンリストから「 <span class="uicontrol"> 固定」 </span> を選択した <span class="uicontrol"> 場合に </span> のみ使用できます。 </p> <p>ドリルダウン中に開いたままにするオプションの数を設定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>長さのしきい値 </p> </td> 
      <td colname="col2"> <p>項目数で定義されるファセットの垂直方向の長さ(1 ～ 9999)を設定します。 </p> <p>プレゼンテーションテンプレートが適切に設定されている場合は、この設定を使用して「表示を増やす」を設定できます。 リンクを追加したり、ファセットをスクロール可能なdivにスローするタイミングを指定したりします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>長さの切り捨てしきい値 </p> </td> 
      <td colname="col2"> <p>指定したしきい値の後にファセット内の項目数を切り捨てます。 </p> <p>実装によっては、何千もの項目が含まれたファセットを持つ場合もあります。 全てのデータを送るのは高くつく。 この設定を使用して、ファセットを管理可能なレベルにトリムできます。 並べ替え後にファセットが切り捨てられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大値の幅 </p> </td> 
      <td colname="col2"> <p>ファセット値の文字列の長さの制限を指定します(1 ～ 999)。 </p> <p>このオプションは、固定幅レイアウトにファセットを配置し、文字列の折り返しを防ぐ場合に便利です。 デフォルトでは、文字列はしきい値より3文字短く設定され、省略記号を追加できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>値の拡張子 </p> </td> 
      <td colname="col2"> <p>ファセット値の切り捨てを示す文字列を指定します。 デフォルトでは、「。..」という文字列が が使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>ファセットに適用される区切り区切り値リストに使用する区切り文字を指定します。 </p> <p>使用される区切り文字は、ファセットの基となるメタデータで定義されている区切り文字と同じです。 デフォルトの区切り文字はコンマです。 ただし、XML準拠の任意の値を使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>並べ替え </p> </td> 
      <td colname="col2"> <p>Webサイト上のファセットの並べ替え方法を指定します。 次の順でファセットを並べ替えることができます。 必要に応じて、最大5種類の並べ替えを組み合わせることができます。 </p> 
      <ul id="ul_12987F4DC7B34C63ABC906B59688A174"> 
      <li id="li_3206C96013DF431D90119F594D93D85D"> <span class="uicontrol"> alpha </span> <p>値を(0 ～ 9、A ～ Z)アルファベット順に並べ替えます。句読点も含まれます。 </p> </li> 
      <li id="li_304E4A518FBE48D18D9E9EA7339A3481"> <span class="uicontrol"> alpha（英数字のみ） </span> <p>値をアルファベット(0 ～ 9、A ～ Z)順に並べ替え、句読点の文字は無視します。 </p> </li> 
      <li id="li_CADB888CC514455F9CA379C8EEE490AA"> <span class="uicontrol"> alpha（大文字と小文字は区別されません） </span> <p>値をアルファベット順(0 ～ 9、A ～ Z)に並べ替えます。大文字と小文字は区別されず、句読点も含まれます。 </p> </li> 
      <li id="li_F61122E79AB5413792DA31F8AB1414BD"> <span class="uicontrol"> alpha（大文字と小文字は区別されない、英数字のみ） </span> <p>値をアルファベット順(0 ～ 9、A ～ Z)に並べ替えます。大文字と小文字は区別されず、句読点も無視されます。 </p> </li> 
      <li id="li_F50CC298ABF046D0A39D5AE5B1261823"> <span class="uicontrol"> count </span> <p>各ファセット値に一致する結果の数を最大から最小に並べ替えます。 </p> </li> 
      <li id="li_32B6AF39E9534762B39B15181DC5AD01"> <span class="uicontrol"> numeric </span> <p>数値を並べ替えます。 数値を並べ替える場合は、アルファ並べ替えよりもこのオプションの方が優れています。アルファ並べ替えを使用すると、2の前に10が表示されるからです。 </p> </li> 
      <li id="li_CF8E76A7B1184E0C8DCC11B53E31A1DC"> <span class="uicontrol"> split </span> <p>カウントしきい値でリストを2つの異なるリストに分割します。 しきい値を超えるファセット値は上に移動されます。 数がしきい値を下回るファセット値は下に移動されます。 特定の範囲の値を常に最上位に固定する場合は、分割しきい値が必要です。 </p> </li> 
      <li id="li_4AB8276577384B1099CBA895898205AD"> <span class="uicontrol"> break </span> <p>特定の値を強制的にリストの上または下に配置します。 例えば、「その他」という用語を常にリストの一番下に表示するとします。 分割ソートを使用して、並べ替えの先頭または末尾に配置する必要のある明示的な値を識別する場合は、上位の値または下位の値が必要です。 </p> </li> 
      <li id="li_227E96CFED2044FCA2F10B6913B03CFB"> <span class="uicontrol"> 注文 </span> <p>ファセット値は常に固定順(後述の「順序」オプションで定義される区切り値リ <span class="uicontrol"> スト </span> )である必要があります。 </p> </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットのエイリアス </p> </td> 
      <td colname="col2"> <p>既存の検索URLをサポートするには、ファセットエイリアスを使用して、以前のパラメーター名を変更対象にマップするか、単に別の名前のファセットを作成します。 エイリアスは、受信する要求にのみ適用され、ファセットリンクの作成には使用されません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファセットパネル名 </p> </td> 
      <td colname="col2"> <p>ファセットをアルファベット順、カウント別、またはカスタムメソッド別に並べ替える場合のファセットパネルの名前。 </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">「Facet Rail」について</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Order </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 並べ替え」 <span class="uicontrol"> を選択し </span> た場合にのみ使用できます。 </p> <p>使用する順序を指定する値の区切りリストを定義できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>追加 </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 並べ替え」 <span class="uicontrol"> を選択し </span> た場合にのみ使用できます。 </p> <p>順序付けられたリストに値が存在しない場合、値は末尾に追加されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ゴーストを表示 </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 並べ替え」 <span class="uicontrol"> を選択し </span> た場合にのみ使用できます。 </p> <p>順序付けられたリストで指定された値がない場合、このオプションは、ファセット内の欠落した各項目に「ゴースト」というフラグを付け、項目の表示を変えます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ネストされたファセット </p> </td> 
      <td colname="col2"> <p>ネストされたファセットには、そのカテゴリとその子のカテゴリが表示されます。 2つのカテゴリの深さのみを表示できますが、ドリルダウンに沿って任意の場所に表示できます。 </p> <p>このファセットのデータは、2つのカテゴリのレベルを記述する際の規則に従う必要があります。 例えば、ファセット値は「靴：ブーツ」で、親カテゴリが「靴」、子カテゴリが「ブーツ」の場合があります。 区切り文字として「:」が使用されます。 </p> <p>区切り文字の変更について詳しくは、後述の「入れ子区切り文字」を参照してください。 </p> <p>この形式でデータを生成するには、フィルタースクリプトを使用して、2つの既存のカテゴリを組み合わせます。 「標準」、「カテゴリ」、「共通」の各動作をネストされたファセットと組み合わせることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ネストされた親名 </p> </td> 
      <td colname="col2"> <p>このドロップダウンリストは、「ネストされたファセット」を選択した場合にの <span class="uicontrol"> み使用できま </span>す。 </p> <p>親カテゴリを表すフィールドを選択できます。 このフィールドは、親カテゴリと一致する検索時に使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>子名の入れ子 </p> </td> 
      <td colname="col2"> <p>このドロップダウンリストは、「ネストされたファセット」を選択した場合にの <span class="uicontrol"> み使用できま </span>す。 </p> <p>子カテゴリを表すフィールドを選択できます。 このフィールドは、子カテゴリと一致する検索時に使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ネストされたファセット区切り </p> </td> 
      <td colname="col2"> <p>このオプションは、「ネストされたファセット」を選択した場合に <span class="uicontrol"> のみ使用できま </span>す。 </p> <p>ここに入力した文字は、親カテゴリと子カテゴリをデータから解析するために使用されます。 </p> <p>例えば、「:」が区切り文字として使用され、親が「靴」で、子が「boots」の場合、データは「shoes:boots」としてフォーマットされる必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>分割しきい値 </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 分割」を選 <span class="uicontrol"> 択した場 </span> 合にのみ使用できます。 </p> <p>分割の並べ替えを使用する場合、分割のしきい値は、ファセットを2つの異なるリストに分割するカウントを定義します。 しきい値以上のカウントを持つ値は上に維持され、しきい値未満の値は下に移動されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最高値 </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 分類」を選 <span class="uicontrol"> 択した場 </span> 合にのみ使用できます。 </p> <p>改ページの並べ替えを使用する場合、この値の区切りリストは常にリストの先頭に配置されます。 正規表現は使用できますが、中括弧または中括弧で囲む必要があります。例：{^New .*?},{^Very New .*} </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最低値 </p> </td> 
      <td colname="col2"> <p>このオプションは、「並べ替え」ドロップダウンリ <span class="uicontrol"> ストで「 </span> 分類」を選 <span class="uicontrol"> 択した場 </span> 合にのみ使用できます。 </p> <p>改ページの並べ替えを使用する場合、この区切り形式の値のリストは常にリストの一番下に配置されます。 正規表現は使用できますが、次の例のように中括弧または中括弧で囲む必要があります。{^Old .*?},{^とても古い。*} </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）ページ [!DNL Facets] で、次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ネストされたファセットの追加 {#task_A132FA7EB7494A6B88E443F2C3FABBBA}

ネストされたファセットを追加して、複数のレベルのカテゴリを表示できます。

<!-- 

t_adding_a_nested_facet.xml

 -->

ネストされたファセットを作成する場合は、次の点に注意してください。

* ネストされた各ファセットには、1つのユーザー定義のメタタグフィールドが必要です。
* ネストされたファセットは、親ファセットと子ファセットの2つの他のファセットで構成されます。 単一値ファセットまたは複数値ファセットを使用できます。 単一値ファセットと複数値ファセットの混在は許可されません。
* このファセットを検索フィールドテーブルで使用するかどうかを決定する必要があります。 フィールドテーブルには、ネストされたファセット自体と、その合成ファセットが必要です。
* JSONを使用してネストされたファセットを実装することを検討します。それは簡単です。

* [タスク1 — メタタグの追加](../c-about-design-menu/c-about-facets.md#task_6944558325204E749C725DCFEF17EF3D)
* [タスク2 — 事前に形式設定されたデータを生成するフィルタリングスクリプトの追加](../c-about-design-menu/c-about-facets.md#task_2DFED8BCB87B4067A6CE280945D7CAF4)
* [タスク3 — 新しいファセットの追加](../c-about-design-menu/c-about-facets.md#task_3C11A4159FC44B9494D48594941AF8CF)
* [タスク4 — ガイド付き検索の編集](../c-about-design-menu/c-about-facets.md#task_E50EFD7BBD0F45729C15759EA4F548D8)
* [タスク5 — トランスポートテンプレートの作成](../c-about-design-menu/c-about-facets.md#task_C1FEDEF11D2549DEB1A9C09BFBA64381)
* [タスク6 — プレゼンテーションテンプレートの作成](../c-about-design-menu/c-about-facets.md#task_4B2ABB37B9CD4F3F8AF8E6874227A995)
* [タスク7 — 階層リンクの編集](../c-about-design-menu/c-about-facets.md#task_5E22409528EC4DA284821F82FDCE3438)

>[!NOTE]
>
>このトピックでは、ネストされたファセットをfacet n1と呼びます。

## タスク1 — メタタグの追加 {#task_6944558325204E749C725DCFEF17EF3D}

ネストされたファセットの保持日専用の新しいメタタグフィールドを追加します。 複数値のフィールドまたは1つの値のフィールドを指定できます。

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Metadata]** ます **[!UICONTROL Definitions]**。
1. ページ上で、 [!DNL Definitions] をクリックしま **[!UICONTROL Add New Field]**&#x200B;す。
1. ページ [!DNL Add Field] で、必要なオプションを設定します。

   詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。
1. クリック **[!UICONTROL Add]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

   残りのタスクは、このメタタグフィールドを **n1と呼びます**。

## タスク2 — 事前に形式設定されたデータを生成するフィルタリングスクリプトの追加 {#task_2DFED8BCB87B4067A6CE280945D7CAF4}

1. 元のファセットを次の形式に結合するフィルタリングスクリプトを追加します。 `<parent_value><nested_delimiter><child_value>`.

   詳しくは、フ [ィルタリングスクリプトの追加を参照してくださ](../c-about-settings-menu/c-about-filtering-menu.md#task_0AB84FD1133F47F9AA069A79BEA13A22)い。

   メタタグフィールドn1の値の例を次に示します。上記の形式を使用します。

   `Womens:Handbags`

   `Womens:Dresses`

   `Mens:Accessories`

   `Mens:Footwear`
1. フィルタリングスクリプトを作成または編集した後、スクリプトをテストします。 正しく表示される場合は、必要に応じてアカウントのインデックスを再作成します。 インデックスは、を使用して確認できま [!DNL Index Overview]す。

   次の例は、フィルタリングスクリプトの初期化に標準のコンサルティングライブラリが含まれていることを前提としています。 各アカウントは異なるので、フィルタリングスクリプトには、自分のアカウントに必要な要件が反映されている必要があります。

   **複数値のフィルタリングスクリプトの例**

   ```
   my $doc; 
   { 
   # Slurp all the data into $doc 
   local $/; 
   undef $/; 
   $doc = <>; 
   } 
    # Create n1 field 
    if ( $doc =~ m{<meta\s+name="t1"\s+content="([^\"]*)"}is ) 
    { 
     my @t1arr = split(/\|/, $1); 
     if (scalar @t1arr > 0) 
     { 
      if ( $doc =~ m{<meta\s+name="t2"\s+content="([^\"]*)"}is ) 
      { 
       my @t2arr = split(/\|/, $1); 
   
       if ( scalar @t2arr > 0 ) 
       { 
        my $max = ((scalar @t1arr) < (scalar @t2arr)) ? (scalar @t1arr) : (scalar @t2arr); 
        for (my $i = 0; $i < $max; $i++) 
        { 
         $t1arr[$i] .= ":" . $t2arr[$i]; 
        } 
       } 
      } 
      my $output = join( '|', @t1arr ); 
      $doc =~ s{</head>}{<meta name="n1" content="$output" />\b</head>}is; 
     } 
    } 
    # END: n1 field
   ```

   **単一の値のフィルタリングスクリプトの例**

   ```
   # This is a complete example. 
   # This script is designed for index connector where each record 
   # in the XML file is converted into a fake HTML page filled with 
   # meta data tags.  
   my $doc; 
   { 
   # Slurp all the data 
   local $/; 
   undef $/; 
   $doc = <>; 
   } 
   # All legitimate index connector data has key in its URL. 
   # Process the page if and only if it is coming from index connector and 
   # it is not the first entry point page.  Entry point pages don't have key 
   # in the URL. 
   if ($main::search_url =~ /\?key=/) { 
    my $meta = {}; 
    # Mine and scrape the meta fields from the page 
    my @lines = split(/\n/,$doc); 
    foreach my $line (@lines) 
    { 
     if ($line =~ m{<meta name="(.*?)" content="(.*?)" />}) 
     { 
      $meta->{lc($1)} = $2; 
     } 
    } 
    # Combined t1,t2 and t2,t3, and t3,t4 together. 
    # Assign them respectively to n1, n2, and n3. 
    my ($t1, $t2, $t3, $t4); 
    my %meta2; 
    $t1 = $meta->{'t1'}; 
    $t2 = $meta->{'t2'}; 
    $t3 = $meta->{'t3'}; 
    $t4 = $meta->{'t4'}; 
    if (defined $t1 && $t1) { 
     $meta2{'n1'} = $t1; 
     if (defined $t2 && $t2) { 
      $meta2{'n1'} .= ":" . $t2; 
      $meta2{'n2'} = $t2; 
      if (defined $t3 && $t3) { 
      $meta2{'n2'} .= ":" . $t3; 
       $meta2{'n3'} = $t3; 
       if (defined $t4 && $t4) { 
        $meta2{'n3'} .= ":" . $t4; 
       } 
      } 
     } 
    } 
    foreach my $stuff ( keys %meta2 ) 
    { 
     my $v = $meta2{$stuff}; 
     $doc =~ s{</head>}{<meta name="$stuff" content="$v" />\n</head>}; 
    } 
   } 
   
   # Do some ranking stuff here 
   ws_insert_static_rank_meta_tag(\$doc, "RANK"); 
   
   # Prints the entire page back out. 
   print $doc;
   ```

## タスク3 — 新しいファセットの追加 {#task_3C11A4159FC44B9494D48594941AF8CF}

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Facets]**。
1. ページ上で、 [!DNL Facets] をクリックしま **[!UICONTROL Add New Facet]**&#x200B;す。
1. ページで、 [!DNL Add Facet] 次のオプションを設定します。

   * ドロップダ [!DNL Facet Name] ウンリストで、タスク1で定義したメタタグフィールドを選択します。 検索フィールドテーブルを使用している場合は、ド **[!UICONTROL custom]** ロップダウンリストでを選択し、ファセットのカスタム名を入力します。

   * ネストさ **[!UICONTROL Nested Facet]** れたファセットを「オン」にする場合に選択します。
   * およびドロ [!DNL Nested Parent Name] ップダ [!DNL Nested Child Name] ウンリストで、使用できるメタタグフィールドを選択します。 検索フィールドテーブルを使用している場合は、ファセ **[!UICONTROL custom]** ットのカスタム名を選択して入力します。

   * フィー [!DNL Nested Facet Delimiter] ルドで、使用する区切り文字(「:」（コロン）など)を指定します。 複数値の区切り文字と混同しないでください。 両方の区切り文字は互いに異なる必要があります。
   * ファセットの動作を設定する場合は、ファセ **[!UICONTROL Category]**&#x200B;ットの親を指定できます（親をネストされたファセットの親と混同しないでください）。 一般に、別のネストされたファセットの名前をカテゴリの親として使用しないでください。 その代わりに、ネストされたファセットを構成する個々のファセットを使用します。
   * 必要なその他のファセットオプションを設定します。
   「新しいフ [ァセットの追加」を参照してくださ](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)い。
1. クリック **[!UICONTROL Add]**.

## タスク4 — ガイド付き検索の編集 {#task_E50EFD7BBD0F45729C15759EA4F548D8}

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Searching]** ます **[!UICONTROL Searches]**。
1. ページ [!DNL Searches] 上で、更新 **[!UICONTROL Edit]** する検索タイプ名をクリックします。
1. フィールド `sp_field_table` n1、t1、t2が必要です。

   フィールドテーブルを使用する場合は、パラメータを編集する必要が `sp_field_table` あります。 または、クエリ消去ルールや検索前のルールを使用して、他の場所でこれを行うこともできます。

   「クエリク [リーニングルールの追加」を参照してくださ](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)い。

   「新し [い検索前ルールの追加」を参照してください](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11)。
1. クリック **[!UICONTROL Save Changes]**.

## タスク5 — トランスポートテンプレートの作成 {#task_C1FEDEF11D2549DEB1A9C09BFBA64381}

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ上で、 [!DNL Templates] をクリックしま **[!UICONTROL Add New Template]**&#x200B;す。
1. ダイアログ [!DNL Add Template] ボックスで、トランスポートテンプレートファイルの名前を指定します。
1. ドロップダ [!DNL New Template Type] ウンリストで、を選択しま **[!UICONTROL Transport]**&#x200B;す。
1. クリック **[!UICONTROL Add]**.
1. ページで、 [!DNL Templates] 追加したトランスポートテンプレートファイル名の名前をクリックします。
1. トランスポ [!DNL Template Editor] ートテンプレートのページで、フィールドn1のデータを含めます。 次の例を参照してください。

   **ネストされたファセットデータを返すXMLの例** XMLの例では、ファセット値の区切り文字として使用する文字を指定する必要があります。 この場合、パイプ(|)です。

   ```
   <facet name="n1"> 
     <values delimiter="|"><search-field-value-list name="n1" quotes="no" separator="|" sortby="values" data="values" /></values> 
     <counts><search-field-value-list name="n1" quotes="no" sortby="values" data="results" /></counts> 
   </facet>
   ```

   **ネストされたファセットデータを返すJSONの例**

   ```
   { 
      "name" : "n1", 
      "values" : [ <search-field-value-list name="n1" quotes="yes" sortby="values" data="values" encoding="json"/>], 
      "counts" : [<search-field-value-list name="n1" quotes="no" sortby="values" data="results" />] 
   },
   ```

## タスク6 — プレゼンテーションテンプレートの作成 {#task_4B2ABB37B9CD4F3F8AF8E6874227A995}

1. 製品メニューで、/をクリッ **[!UICONTROL Design]** クしま **[!UICONTROL Templates]**&#x200B;す。
1. ページ上で、 [!DNL Templates] をクリックしま **[!UICONTROL Add New Template]**&#x200B;す。
1. ダイアログボ [!DNL Add Template] ックスで、プレゼンテーションテンプレートファイルの名前を指定します。
1. ドロップダ [!DNL New Template Type] ウンリストで、を選択しま **[!UICONTROL Presentation]**&#x200B;す。
1. クリック **[!UICONTROL Add]**.
1. ページ上で、 [!DNL Templates] 追加したプレゼンテーションテンプレートファイル名の名前をクリックします。
1. プレゼンテー [!DNL Template Editor] ションテンプレートのページで、必要な出力と統合するHTMLマークアップを追加します。

   次のタグを使用して、子タグを表示できます。

* **If Child Existタグ**`<guided-if-facet-value-has-children><guided-else-facet-value-selected></guided-if-facet-value-has-children>`

* **子の値タグ**`<guided-facet-value-children></guided-facet-value-children>`

   子の値タグは、通常のガイド付きファセット値タグとは異なります。 は、親ファセット値ではなく子ファセッ `<guided-facet-value>` ト値を繰り返し処理するすべての包括タグを含むラッパータグです。 同様に、取り消しタグなど、他のガイド付きファセットタグも同じ内容に従います。 タグ内での使用に最適 `<guided-if-facet-value-has-children>` です。

   次に、HTMLマークアップを含むプレゼンテーションテンプレートの例を示します。

   ```
   <guided-facet gsname="n1"> 
   <guided-if-facet-selected> 
    <guided-facet-values> 
    <guided-if-facet-value-selected> 
     <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
      <guided-if-facet-value-selected> 
       <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
      <guided-else-facet-value-selected> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-if-facet-value-selected> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    <guided-else-facet-value-selected> 
     <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    </guided-if-facet-value-selected> 
    </guided-facet-values> 
   <guided-else-facet-selected>  
    <guided-facet-values> 
    <guided-if-facet-value-selected> 
     <li><span class="selected"><guided-facet-value /></span><guided-facet-value-undo-link gsname="n1">X</guided-facet-value-undo-link></li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    <guided-else-facet-value-selected> 
     <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
     <guided-if-facet-value-has-children> 
      <ul> 
      <guided-facet-value-children> 
       <li><guided-facet-link title='<guided-facet-value />'><guided-facet-value /> (<guided-facet-count />)</guided-facet-link> </li> 
      </guided-facet-value-children> 
      </ul> 
     </guided-if-facet-value-has-children> 
    </guided-if-facet-value-selected> 
    </guided-facet-values> 
   </guided-if-facet-selected> 
   </guided-facet>
   ```

## タスク7 — 階層リンクの編集 {#task_5E22409528EC4DA284821F82FDCE3438}

検索にパンくずリストを使用している場合は、「移動先」に動作を設定する必要が **あります**。

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Breadcrumbs]**。
1. ページ上 [!DNL Breadcrumbs] で、動作を更 **[!UICONTROL Edit]** 新する階層リンク名をクリックします。
1. ページ [!DNL Edit Breadcrumb] のドロップダウ [!DNL Behavior] ンリストで、「移動先」を **選択します**。
1. クリック **[!UICONTROL Save Changes]**.

## ファセットの編集 {#task_457EDC49983F4F7781873703AF574DA5}

追加した任意のファセットの設定を編集できます。

<!-- 

t_editing_a_facet.xml

 -->

>[!NOTE]
>
>Webサイトに表示されるように、プレゼンテーションテンプレートでファセットを参照してください。

**ファセットを編集するには**

1. 製品メニューで、//をクリ **[!UICONTROL Design]** ックしま **[!UICONTROL Navigation]** す **[!UICONTROL Facets.]**
1. ページ [!DNL Facets] で、ファセッ **[!UICONTROL Edit]** ト名の一番右をクリックします。
1. ページ [!DNL Edit Facet] で、必要なオプションを設定します。

   「新しいファセットの追加」のオ [プションの表を参照してください](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ペ [!DNL Facets] ージで、

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ファセットの削除 {#task_17756FD66BCC49629325B2217F821BDD}

追加したファセットは削除できます。

<!-- 

t_deleting_a_facet.xml

 -->

**ファセットを削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Navigation]** ます **[!UICONTROL Facets]**。
1. ページ [!DNL Facets] で、ファセッ **[!UICONTROL Delete]** ト名の一番右をクリックします。
1. ダイアログボッ [!DNL Confirmation] クスで、をクリックしま **[!UICONTROL OK]**&#x200B;す。
1. 次のいずれかを実行します。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

