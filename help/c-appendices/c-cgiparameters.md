---
description: 'null'
seo-description: 'null'
seo-title: CGIパラメータ
solution: Target
title: CGIパラメータ
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# CGIパラメータ{#cgi-parameters}

## CGIパラメータ {#concept_F395999090FE4926B38BC73D5E612800}

## CGIパラメータの検索 {#reference_DA27A8B0728246DA94994885E1353890}

サイトのHTMLにコピー&amp;ペーストできる検索フォームコードが提供され **[!UICONTROL Design]** てい **[!UICONTROL Auto-Complete]** ます(> **[!UICONTROL Form Source]**>)。

「検 [索フォームのHTMLコードを](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

検索フォーム自体またはスクリプトから、リストに表示されるパラメーターを設定することもできます。 以下に示すパラメーターに加えて、バックエンド検索パラメーターを使用して検索を制御することもできます。

バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。

検索リクエストはベースURLで構成されます。 ベースURLは、顧客が検索しているアカウントと、関連するアカウントに対して目的の検索結果を返す方法を示すCGIパラメーターのセット（キーと値のペア）を示します。

ベースURLは、特定のアカウントと、ステージングされた環境またはライブ環境に関連付けられます。 アカウントマネージャーからベースURLの複数のエイリアスをリクエストできます。 例えば、Megacorpという会社のアカウントには、次の2つのベースURLが関連付けられている場合があります。 `https://search.megacorp.com` と `https://stage.megacorp.com`前者のURLはライブインデックスを検索し、後者のURLはステージングインデックスを検索します。

CGIパラメーターの3つの形式がサポートされています。 デフォルトでは、次の例のように、CGIパラメーターをセミコロンで区切るようにアカウントが設定されています。

`https://search.megacorp.com?q=shoes;page=2`

必要に応じて、アカウントマネージャーにアカウントを設定し、アンパサンドを使用してCGIパラメーターを区切るように設定することもできます。次に例を示します。

`https://search.megacorp.com?q=shoes&page=2`

SEO形式と呼ばれる3つ目の形式もサポートされています。この場合、区切り文字の代わりにスラッシュを使用し、 `/` 次の例のように等号を付けます。

`https://search.megacorp.com/q/shoes/page/2`

SEO形式を使用してリクエストが送信されるたびに、すべての出力リンクは同じ形式で返されます。

| ガイド付き検索パラメーター | 例 | 説明 |
|--- |--- |--- |
| q | `q=string` | 検索のクエリ文字列を指定します。 このパラメーターはバックエンド検索パラメ `sp_q` ーターにマップされます。  バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| q# | `q#=string` | ファセット化（特定のフィールド内での検索）は、番号付きのqおよびxパラメータを使用して行われます。  qパラメーターは、対応する番号付きのxパラメーターで示されるように、ファセット内で検索する用語を定義します。<br>例えば、sizeとcolorという名前の2つのファセットがある場合、q1=small;x1=size;q2=red;x2=colorのように指定できます。  このパラメーターはバックエンド検索パラメ `sp_q_exact_#` ーターにマッピングされます。  <br>バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| x# | `q#=string` | ファセット化（特定のフィールド内での検索）は、番号付きのqおよびxパラメータを使用して行われます。  qパラメーターは、対応する番号付きのxパラメーターで示されるように、ファセット内で検索する用語を定義します。 <br>例えば、sizeとcolorという名前の2つのファセットがある場合、q1=small;x1=size;q2=red;x2=colorのように指定できます。  このパラメーターはバックエンド検索パラメ `sp_x_#` ーターにマッピングされます。  <br>バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| コレクション | `collection=string` | 検索に使用するコレクションを指定します。  このパラメーターはバックエンド検索パラメ `sp_k` ーターにマップされます。  バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| count | `count=number` | 表示される結果の合計数を指定します。  デフォルトは、 > >で定 [!UICONTROL Settings ] 義さ [!UICONTROL Searching ] れます [!UICONTROL Searches ]。.  このパラメーターはバックエンド検索パラメ `sp_c` ーターにマップされます。  バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| page | `page=number` | 返される結果のページを指定します。 |
| ランク | `rank=field` | 静的なランクに使用するランクフィールドを指定します。  このフィールドは、関連性が0より大きいRank型のフィールドである必要があります。  このパラメーターはバックエンドパラメーター `sp_sr` にマップされます。  バックエンド [検索のCGIパラメーターを参照してくださ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)い。 |
| 並べ替え | `sort=number` | 並べ替え順を指定します。<br>「0」はデフォルトで、関連度スコアで並べ替えられます。「1」は日付順に並べ替えます。「 —1」は並べ替えを行いません。  ユーザーは、パラメーターの値のフィールド名を指定で `sp_s` きます。  例えば、タイトル `sp_s=title` フィールドに含まれる値に従って結果を並べ替えます。 パラメーターの値にフィールド名を使用すると、結果 ` sp_s ` はそのフィールドで並べ替えられ、その後関連性で下位に並べ替えられます。  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. 定義ページで、をクリックするか、特定 [!UICONTROL Add New Field ] のフィールド [!UICONTROL Edit ] 名をクリックします。 ドロップダ [!UICONTROL Sorting ] ウンリストで、またはのいずれかを選 [!UICONTROL Ascending ] 択しま [!UICONTROL Descending ]す。 このパラメーターはバックエンド検索パラメ `sp_s` ーターにマップされます。 <br>バックエンド [検索のCGIパラメーターを参照してくださ]い。(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)。 |

## バックエンド検索CGIパラメータ {#reference_582E85C3886740C98FE88CA9DF7918E8}

通常、お客様はガイド付き検索と呼ばれるプレゼンテーションレイヤーを操作します。 ただし、理論的には、Guided Searchレイヤーをスキップし、このページで説明するCGIパラメーターを使用してバックエンドのコア検索と直接やり取りすることが可能です。

次の表から、バックエンド検索CGIパラメータを選択できます。
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>単一のクエリのサポート </p> </th> 
   <th colname="col03" class="entry"> <p>複数のクエリのサポート </p> </th> 
   <th colname="col3" class="entry"> <p>例 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_a=文字列 </span> </p> </td> 
   <td colname="col4"> <p>アカウント番号の文字列を指定します。 このパラメーターは必須で、有効なアカウント番号文字列である必要があります。 アカウント番号の文字列は、設定/アカウントオ <span class="uicontrol"> プショ </span> ン/アカ <span class="uicontrol"> ウント </span> 設定 <span class="uicontrol"> にありま </span>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>sp_ <span class="codeph"> advanced=1 </span> がクエリで送信された場合、検索テンプレート内の <span class="codeph"> &lt;search-if-advanced&gt;タグと </span><span class="codeph"></span> &lt;/search-if-advanced&gt;タグの間のすべてのコードが検索フォームに使用されます。 &lt;search-if-not-advanced&gt; <span class="codeph"> タグと&lt;/search-if-not-advanced&gt; </span> タグの間のコードはすべて無 <span class="codeph"></span> 視されます。 sp_advanced=0 <span class="codeph"></span> （または他の値）が送信された場合、&lt;search-if-advanced&gt;テンプレートブロックは無視され、&lt;search-if-not-advanced&gt;テンプレートブロックが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= number </span> </p> </td> 
   <td colname="col4"> <p>表示する結果の合計数を指定します。 デフォルトは 10 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>特定のフィールドのコンテキスト情報を収集します。 収集された情報は、 <span class="codeph"> &lt;search-context&gt;テンプレートタグを使用して検索結果に出力 </span> されます。 The default value is <span class="codeph"> body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d=タイプ </span> </p> </td> 
   <td colname="col4"> <p>実行する日付範囲検索のタイプを指定します。 指定可能な値は、日付範囲検索を行わないことを意味する。 <span class="codeph"> sp_date_の値を用いて検索対象の日付を決定することを示す。 </span> sp_date_の値を用いて検索対象の日付を決定し、 <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> sp_start_day、 sp_sp_st_start_sp_end、 sp_sp_en検索する日付範囲を決定するために使用します。 <span class="codeph"> sp_dは、 </span> 検索フォームにカスタム範囲（sp_date_rangeを使用）または特定の開始日と終了日の範囲で検索するオプションが含まれている場合にのみ必 <span class="codeph"></span>要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#=タイプ </span> </p> </td> 
   <td colname="col4"> <p>対応するsp_q_#クエリで実行する日付範囲 <span class="codeph"> の検索のタイプを指定し </span> ます。 「#」は1 ～ 16の数値に置き換えられます(例： <span class="codeph"> sp_d_8、番号付きクエ </span>リ <span class="codeph"> sp_q_8に適用されます </span>)。 </p> <p>typeは、 <span class="codeph"> sp_date_range_#の値を使用して検索日を決定し、sp_ </span> q_min_ <span class="codeph"> day_#、sp_min_ </span> min_sp_min_ <span class="codeph"> min_#、sp_q_min_min_ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> max_max日付の範囲を調べるには、_max_month_q_q#とsp_max_year#を使う。 sp_ <span class="codeph"> d_#の使用は、検索フォームにカスタム範囲( </span><span class="codeph"></span>sp_date_range_#を使用)または特定の開始日と終了日の範囲で検索するオプションが含まれている場合にのみ必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>検索に適用する事前定義の日付範囲を指定します。 0以上の値は、今日より前に検索する日数を指定します — 例えば、「0」の値は「today」を、「1」の値は「today and yesterday」を、「30」の値は「直近の30日以内」を示します。 </p> <p>0未満の値は、次のようにカスタム範囲を指定します。 </p> <p>-1 = "なし"。日付範囲を指定しない場合と同じ。 </p> <p>-2 = "今週"。現在の週の日曜日から土曜日まで検索します。 </p> <p>-3 = "先週"。現在の週の前の週の日曜日から土曜日までを検索します。 </p> <p>-4 = "今月"。現在の月内の日付を検索します。 </p> <p>-5 = "先月"。現在の月の前の月の日付を検索します。 </p> <p>-6 = "今年"。現在の年内の日付を検索します。 </p> <p>-7 = "昨年"。現在の年の前の年の日付を検索します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>対応するsp_q_#クエリに適用する、事前定義さ <span class="codeph"> れた日付範囲を指定し </span> ます。 「#」は1 ～ 16の数値に置き換えられます(例： <span class="codeph"> sp_date_range_8、番号付きクエリ </span>sp_q_8に適用されま <span class="codeph"></span>す)。 </p> <p>0以上の値は、今日より前に検索する日数を指定します。 例えば、値0は今日を表します。値1は今日と昨日を指定します。値30は、過去30日間以内などを指定します。 </p> <p>0未満の値は、次のようにカスタム範囲を指定します。 </p> <p>-1 = "なし"。日付範囲を指定しない場合と同じ。 </p> <p>-2 = "今週"。現在の週の日曜日から土曜日まで検索します。 </p> <p>-3 = "先週"。現在の週の前の週の日曜日から土曜日までを検索します。 </p> <p>-4 = "今月"。現在の月内の日付を検索します。 </p> <p>-5 = "先月"。現在の月の前の月の日付を検索します。 </p> <p>-6 = "今年"。現在の年内の日付を検索します。 </p> <p>-7 = "昨年"。現在の年の前の年の日付を検索します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>検索結果を重複除外する単一のフィールドを指定します。 そのフィールドの重複した結果はすべて検索結果から削除されます。 例えば、 <span class="codeph"></span>sp_dedupe_field=titleの場合、特定のタイトルの最上位の結果のみが検索結果に表示されます（2つの結果が同じタイトルフィールドのコンテンツを持つことはありません）。 複数値（許可リスト）タイプのフィールドの場合、フィールドの内容全体が比較に使用されます。 1つのフィールドのみ指定できます。 フィールド名に「table-qualifier」は使用できません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= number </span> </p> </td> 
   <td colname="col4"> <p>数字を超える文字を含むクエリ文字列の任意の単語に対して、自動ワイルドカード拡張を行うことを指定します。 つまり、 <span class="codeph"> sp_e=5は、「 </span> query」や「number」など5文字以上の単語をワイルドカード文字「*」で展開し、「query*」や「number*」の検索と同等にすることを指定します。 文字数の少ない単語は展開されないので、「word」を検索しても、自動的にワイルドカードが展開されることはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= number </span> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_#クエリ文字列の任意の単語に対して、数字を超える文字を使用して、自動ワ </span> イルドカード拡張を行うことを指定します。 つまり、 <span class="codeph"> sp_e_2=5は、 </span><span class="codeph"></span><span class="codeph"></span>sp_q_2クエリ文字列内の5文字以上の単語（「query」や「number」など）をワイルドカード文字「*」で展開し、「query*」や「number*」の検索と同等にすることを指定します。 文字数の少ない単語は展開されないので、 <span class="codeph"> sp_q_2で「word」を検索しても、自動的にワイルドカ </span> ードが拡張されることはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day、sp_end_month、sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>この3つの値は、検索の終了日の範囲を指定し、セットとして指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f=文字列 </span> </p> </td> 
   <td colname="col4"> <p>クエリパラメータ文字列の文字セット( <span class="codeph"> sp_qなど </span>)を指定します。 この文字列は、検索フォームを含むページの文字セットと常に一致する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>指定したフィールドから成る論理データテーブルを定義します。 例えば、「color」、「size」、「price」の各フィールドから成る「items」というテーブルは、次のように定義されます。 </p> <p> <span class="codeph"> sp_field_table=items:color,size,price </span> </p> <p>論理テーブルは、（設定/メタデータ/定義の下の）「リストを許可」がオンになってい <span class="uicontrol"> るフ </span> ィールド <span class="uicontrol"> と組み </span> 合わ <span class="uicontrol"> せて最 </span>も役立ちます。 フィールド名を値として使用するすべてのCGIパラメーターとテンプレートタグでは、オプションでテーブル名の後に「。」を付けて指定できます。 フィールド名の前(例： <span class="codeph"> sp_x_1=tablename.fieldname </span>)。 </p> <p>例えば、サイズが「大」（項目がメタデータの平行な行として表される）の1つ以上の「赤」項目を含むドキュメントを検索するには、次を使用します。 </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> 値 </span></span> </p> </td> 
   <td colname="col4"> <p>レポートを生成する際に検索を無視します。 </p> <p>このクエリを使用して、Did You Meanが生成する検索や、管理者がメンバセンターで生成する検索など、特定のバックエンド検索をマスクします。 エンドユーザーはこのような検索タイプを生成しないので、Adobe Search&amp;Promoteの様々なレポートには表示されません。 </p> <p>有効な値 <span class="codeph"> は、sp_i=1 </span> と <span class="codeph"> sp_i=2です </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k=文字列 </span> </p> </td> 
   <td colname="col4"> <p> 検索に使用するコレクションを指定します。 デフォルト値はコレクションなしです。つまり、検索にはサイト全体が含まれます。 </p> <p>「検索フォ <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> ームでのコレクションの使用」を参照してくださ </a>い。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l=文字列 </span> </p> </td> 
   <td colname="col4"> <p>クエリパラメータ文字列の言語( <span class="codeph"> sp_qなど </span>)を指定します。 文字列 <i> は、ISO-639 <span class="codeph"></span></i> 言語コードの後にISO-3166国コードが続くオプションの文字列を含む標準ロケールIDにする必要があります。 例えば、英語の場合は「en」または「en_US」、日本語の場合は「ja」または「ja_JP」です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0または1 </span> </p> </td> 
   <td colname="col4"> <p> sp_literal=1 <span class="codeph"> を設定すると、ク </span> エリ内の単語を解釈するすべての機能が一時的に無効になります。 このパラメーターを使用すると、同義語、代替単語フォーム、類似音の一致に関係なく、クエリのリテラル語のみがドキュメントと一致します。 </p> <p>sp_literal=0 <span class="codeph"> は意味を持た </span> ず、使用した場合は無視されます。 </p> <p>辞書につ <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m=番号 </span> </p> </td> 
   <td colname="col4"> <p> 概要を表示するかどうかを指定します。 1ははい、0はいいえ。 デフォルトは 1 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n=数値 </span> </p> </td> 
   <td colname="col4"> <p> 検索結果を開始する結果の数を指定します。 デフォルトは 1 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> 検索結果がない場合に、指定したURLにリダイレクトするかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p> 実行する検索のデフォルトのタイプを指定します。 anyを使用すると、ク <span class="codeph"> エリ文 </span> 字列から任意の単語を含むドキュメントを検索できます。 allを使用すると、 <span class="codeph"> ク </span> エリ文字列内のすべての単語を含むドキュメントを検索できます。 phraseを使用すると、 <span class="codeph"> ク </span> エリ文字列が引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>フレーズ <span class="codeph"> とす </span> べての <span class="codeph"></span>場合、検索語の前に「+」と「 — 」を指定すると、指定は無効になり、これらの文字は無視されます。 sp_pが <span class="codeph"> 存在しな </span> い場合、または空の文字列または任意の値に設定されている場合は、標準の「+」と「 — 」の単語プリフィックスが許可されます。 </p> <p>検索でプラス(「+」)とマイナス(「 — 」)を使用する方法について詳しくは、検索のヒントの説明を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> <p>sp_pパラメータの使用例については、サンプルのアドバンス検索フォ <span class="codeph"> ームを参照してく </span> ださい。 </p> <p>詳しくは、アドバ <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> ンス検索フォームの例を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#=任意/すべて/フレーズ </span> </p> </td> 
   <td colname="col4"> <p>対応するsp_q_#クエリで実行するデフォルトの <span class="codeph"> 検索タイプを指定し </span> ます。 「#」は1 ～ 16の数値に置き換えられます(例えば、 <span class="codeph"> sp_p_8は番号付きク </span> エリ <span class="codeph"> sp_q_8に適用されま </span>す)。 anyを使用すると、ク <span class="codeph"> エリ文 </span> 字列から任意の単語を含むドキュメントが返されます。 allを使用すると、 <span class="codeph"> クエ </span> リ文字列内のすべての単語を含むドキュメントが返されます。 フレーズを使用す <span class="codeph"> ると </span> は、クエリ文字列が完全なフレーズであるかのように処理されることを意味します（ユーザが入力した引用符はすべて無視されます）。 </p> <p>allまたはphraseのいずれかを指 <span class="codeph"> 定した場 </span> 合、検 <span class="codeph"> 索語の前のプラス記 </span>号とマイナス記号は無視されます。 sp_ <span class="codeph"> p_#を省略し </span> た場合、または空の文字列または任意の値に設定した場合は、標準の「+」と「 — 」のプリフィッ <span class="codeph"> クス </span>が許可されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> 適用するターゲットの一致のタイプを指定します。 完全一致を使用すると、 <span class="codeph"> ターゲ </span> ットコンテンツ内のクエリ文字列と完全に一致するドキュメント内でのみ、ターゲットが一致することになります。 等価の使用は <span class="codeph"> 完全に </span> 似ていますが、単語の順序は重要ではありません。 互換性を使用す <span class="codeph"> ると、 </span> sp_pパラメータの値に基づいて、ターゲットの一致タイプが自動的に設定さ <span class="codeph"></span> れます。 sp_pが全てのフレーズである場合は <span class="codeph"> exactを使用し、それ以外の場合は </span> requictを使用する <span class="codeph"> か、あるいは等価を使用する </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> 場合はexactを使用します。 デフォルト値の <span class="codeph"> sp_ptは互 </span> 換性があ <span class="codeph"> ります </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_#クエリで適用するターゲットの一致のタイプを指定し </span> ます。 「#」は1 ～ 16の数値に置き換えられます(例えば、 <span class="codeph"> sp_p_8は番号付きク </span> エリ <span class="codeph"> sp_q_8に適用されま </span>す)。 完全一致を使用すると、 <span class="codeph"> ターゲ </span> ットコンテンツ内のクエリ文字列と完全に一致するドキュメント内でのみ、ターゲットが一致することになります。 等価の使用は、単 <span class="codeph"> 語の順 </span> 序が重 <span class="codeph"> 要でない点 </span>を除いて、完全一致と似ています。 互換性を使用す <span class="codeph"> ると、対 </span> 応するsp_p_#パラメータの値に基づいて、ターゲットの一致タイプが自動的に <span class="codeph"> 設定され </span> ます。 <span class="codeph"> sp_p_#がすべ </span> てまたはフレーズの場合は、完全一致が使用されます。それ以外の場合は、 <span class="codeph"> 同等の値が使 </span><span class="codeph"></span> 用されます。 デフォルト値の <span class="codeph"> sp_pt_#は互 </span> 換性があ <span class="codeph"> ります </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q=文字列 </span> </p> </td> 
   <td colname="col4"> <p> 検索のクエリ文字列を指定します。 空の文字列は、結果が表示されないことを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= text </span> </p> </td> 
   <td colname="col4"> <p>このパラメーターを使用すると、検索フォームに対して複数のクエリを作成できます。 sp_q_# <span class="codeph"> パラメータには、 </span> 指定した番号付きクエリで使用するクエリ文字列が含まれます。 検索要求は、最大16個の異なる番号付きクエリ( <span class="codeph"> sp_q_1 </span> ～ <span class="codeph"> sp_q_16 </span>)を参照できます。 </p> <p>例えば、次のフォームを送信すると、「great」と「books」という語を含むすべてのドキュメントが返されます。 </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day、sp_q_month、sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q_day_#、sp_q_month_#、sp_q_year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day=整数値 </span> </p> <p> <span class="codeph"> sp_q_month=整数値 </span> </p> <p> <span class="codeph"> sp_q_year=整数値 </span> </p> <p> <span class="codeph"> sp_q_day_#=整数値 </span> </p> <p> <span class="codeph"> sp_q_month_#=整数値 </span> </p> <p> <span class="codeph"> sp_q_year_#=整数値 </span> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、特定のクエリーの正確な日付を指定するために使用されます。 sp_ <span class="codeph"> q_day、 </span>sp_q_month、お <span class="codeph"> よびsp_q_y_yearの各パラメータは、メインクエリ </span>(sp_q_ <span class="codeph"></span><span class="codeph"></span>q)に適用されます。 </p> <p># <span class="codeph"> パ </span>ラメータは、1 ～ 16の数値に置き換えられます(例： <span class="codeph"> sp_q_day_6、番号付きクエリ </span>sp_q_6に適用され <span class="codeph"></span>ます)。 デフォルトでは、すべての日付がグリニッジ標準時を基準に検索されます。 </p> <p>コードの次のセクションでは、「Jan」の日付のドキュメントで「orange」という語を検索できます。 PublishDateという名前のユーザ定義フィールドの「2000年1月」 <span class="codeph"> の値 </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、場所をメインクエリーまたは番号付きクエリーに関連付けます。 sp_q_locationを使用すると、 <span class="codeph"> sp_q_location_# </span> ( <span class="codeph"> #は1 ～ 16の数字で置き換えられます </span><span class="codeph"></span> )のメインクエリーに影響し、指定した番号付きクエリーに影響します。 これらのパラメータは、各サイトページに対してインデックス化された場所データに対して、最小および/または最大距離の近接性検索を実行するために使用されます。 値の形式によって解釈が決まります。 </p> <p>DDD（3桁）の形式の値は、米国の電話番号と解釈されます。DDDDDDまたはDDDDDD-DDDDDの形式の値は、USのzipcodeとして解釈されます。また、±DDD.DDDD±DDD.DDDDDの形式の値は緯度と経度のペアと解釈されます。 各値に記号が必要です。 例えば、+38.6317+120.5509は緯度38.6317、経度120.5509を指定します。 </p> <p>近接検索につ <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメータは、近接検索に適用される関連性の計算を制御します。 sp_q_max_relevant_distanceを使用すると、メインクエリ <span class="codeph"> sp_q_max_relevant_distance_# </span> ( <span class="codeph"></span><span class="codeph"></span> #は1 ～ 16の数字で置き換えられます)に影響し、指定した番号付きクエリに影響します。 </p> <p>sp_q_max_relevant_ <span class="codeph"> distanceのデフォルト値は100 </span> です。 </p> <p>近接コンポーネントの完全な関連性スコアは、距離0を表します。 近接コンポーネントの最小関連スコアは、指定した <span class="codeph"> sp_q_max_relevant_distance_#値の直上の距離を表し </span> ます。 </p> <p>近接検索につ <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day、sp_q_min_month、sp_q_min_year </p> <p>sp_q_max_day、sp_q_max_month、sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#、sp_q_min_month_#、sp_q_min_year_# </p> <p> sp_q_max_day_#、sp_q_max_month_#、sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、特定のクエリーの最小および最大の日付範囲を設定するために使用されます。 <span class="codeph"> sp_q_min_day, sp_q_min_month, sp_q_q_ </span>y_year, sp_max_max_day_q_max_ <span class="codeph"> q_max_daysp_max_q_max_max_ </span>max_q_max_q_max_q_max_q_max_min <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><i></i><span class="codeph"></span>. </p> <p>パラメ <span class="codeph"> ー </span>タ名の#は、1 ～ 16の数字で置き換えられます(例： <span class="codeph"> sp_q_min_day_6は、番号付きのクエリ </span> sp_q_6に適用されます <span class="codeph"></span>)。 </p> <p>最小日のみ、最大日のみ、または最小日と最大日の両方を指定することができます。 ただし、指定した最小値または最大値のセットに対して、3つの日付パラメーター（日、月、年）をすべて指定する必要があります。 デフォルトでは、すべての日付がグリニッジ標準時を基準に検索されます。 </p> <p>次のコードのセクションでは、PublishDateというユーザ定義フィールドで、2000年1月1日から2000年12月31日の間の日付を持つドキュメント内の「orange」という語を検索でき <span class="codeph"> ます </span>。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min、sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q _min_#、sp_q _max_#、sp_q _exact_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min=値 </span> </p> <p> <span class="codeph"> sp_q_max=値 </span> </p> <p> <span class="codeph"> sp_q_min_#=値 </span> </p> <p> <span class="codeph"> sp_q_max_#=値 </span> </p> <p> <span class="codeph"> sp_q_exact_#=value </span> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、メインクエリーまたは番号付きクエリーに適用する最小（または最大）値を指定します。 sp_q_min、 <span class="codeph"> sp_q_max、 </span>sp_q_qの使用は、メインクエリ <span class="codeph"> (sp_q </span><span class="codeph"></span><span class="codeph"></span>)に正確に影響します。 </p> <p>パラメ <span class="codeph"> ー </span>タ名の#を1 ～ 16の数値で置き換えます(例： <span class="codeph"> sp_q_min_8 </span> は番号付きクエリ <span class="codeph"> sp_q_8に適用されます </span>)。 </p> <p>sp_q_exact_# <span class="codeph"> は、同じ値で </span> sp_q_min_# <span class="codeph"> と </span> sp_q_max_#の両方を指定する場合の略 <span class="codeph"></span> 語です。 sp_q_exact_# <span class="codeph"> を指定した場合、対応する </span> sp_q_min_# <span class="codeph"> また </span> はsp_q_max_#パラメータは無 <span class="codeph"></span> 視されます。 </p> <p>sp_q_min_#、 <span class="codeph"> sp_q_max_# </span>、 <span class="codeph"> sp_q_exact_#の各パラメーターでは、必要に応じて複数の「|」区切り値 </span><span class="codeph"></span> を指定できます。 例えば、「color」フィールド内に緑または赤の値を含むドキュメントを検索するには、次のように記述します。 <span class="codeph"> ...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q_nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1または0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1または0 </span> </p> </td> 
   <td colname="col4"> <p>デフォルトのパラメータ値は0 <span class="codeph"> で、共 </span> 通フレーズの拡張が実行されます。 </p> <p>対応する検索クエ <span class="codeph"> リに対し </span> て1を設定した場合、共通フレーズの拡張は実行されません。 </p> <p>sp_q_nocpを使 <span class="codeph"> 用すると、メ </span> イン検索クエリパラメータ <span class="codeph"> sp_qに影響しま </span>す。 このパラメータを番号付き検索クエリに適用するには、パラメ <span class="codeph"> ー </span> タ名の#を対応する番号に置き換えます。 例えば、 <span class="codeph"> sp_q_nocp_8は、番号付き検 </span> 索クエリ <span class="codeph"> sp_q_8に適用されます </span>。 </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q_required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1または0または —1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1または0または —1 </span> </p> </td> 
   <td colname="col4"> <p>このパラメーターは、結果ページにドキュメントを返すために、対応するクエリで一致が必要(1)か、5月(0)か、または必要(-1)でないかを決定します。 </p> <p>sp_q_requiredを使 <span class="codeph"> 用すると、メ </span> インクエリ( <span class="codeph"> sp_q </span>)に影響します。 </p> <p>番号付きクエリーに適用するには、パラメーター名の <span class="codeph"> #を対応する番号に置き換えます(例： </span> sp_q_required_8 <span class="codeph"> は番号付きクエリ </span> ーsp_q_8に適用されます <span class="codeph"></span>)。 パラメーターのデフォルト値は1です（一致する必要があります）。 </p> <p>「calc」という語を含み、「mac」、「win」または「all」を含まないドキュメントをユーザー定義の「platform」フィールドで検索する場合、HTML検索フォームに次の行が含まれます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>検索結果が1つだけの場合に、検索結果URLにリダイレクトするかどうかを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_referrer </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_referrer= url </span> </p> </td> 
   <td colname="col4"> <p>検索のリファラーURLを指定します。 検索結果が検索フォームと同じサイトにリンクする検索書き換えルールに役立ちます。 </p> <p>デフォルト値は、ブラウザが提供する標準のCGI HTTP_REFERRER値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro=フィー <span class="varname"> ルド </span>: <span class="varname"> 関連 </span> 性 </span> </p> </td> 
   <td colname="col4"> <p>フィールド名ごとの検索時間、関連性の制御（オプション）を許可します。 パラメ <span class="codeph"> ータ名 </span> のroは、「関連性の上書き」を表します。 このパラメーターは、1つ以上のフィールド名の後にコロンを付け、続いて0 ～ 10の関連値を受け取ります。 </p> <p>例えば、フィールド名「body」の関連値を10に設定する場合、顧客が検索を実行すると、パラメータは次のように表示されます。 </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>また、パラメータ文字列で複数のフィールド関連性の上書きを指定する場合は、パイプ区切り文字を使用できます。 例えば、「body」と「title」というフィールド名の関連性の値を9に設定する場合、顧客が検索を実行すると、次のようにパラメータが表示されます。 </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>注意： 関連する検索に含まれないフィールドを指定しても効果はありません。 例えば、 <span class="codeph"> sp_ro=title:10と設定したが、タイト </span>ルフィールド名 <span class="codeph"> が検索さ </span> れない場合、 <span class="codeph"> sp_roパラメー </span> タは無効です。 つまり、 <span class="codeph"> sp_roパラメータを使用してフィールド名を指定しても、そのフ </span> ィールドは自動的には検索されません。代わりに、そのフィールドに関連付けられている関連性の設定が上書きされます。 </p> </p> <p>詳しくは、 <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> 事前定義またはユーザ定義のメタタグフィールドの編集を参照してくださ </a>い。 </p> <p>「クエリクリ <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> ーニングルールについて」を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= number </span> </p> </td> 
   <td colname="col4"> <p>並べ替え順を指定します。 ゼロ(0)がデフォルトで、関連度スコアで並べ替えを行います。 1つは日付順に並べ替えることを意味し、-1は並べ替えを行わないことを意味します。 </p> <p>sp_sパラメータの値のフィールド名を指 <span class="codeph"> 定でき </span> ます。 例えば、 <span class="codeph"> sp_s=titleは、タイト </span> ルフィールドに含まれる値に従って結果を並べ替えます。 sp_sパラメータの値にフィールド名を使用すると、結果はそのフィール <span class="codeph"></span> ドで並べ替えられ、その後関連性で下位に並べ替えられます。 </p> <p>参照先のフィールドの並べ替えをAscendingまたはDescendingに設定するには、 Settings &gt; <span class="uicontrol"> Metadata &gt; </span> Descending <span class="uicontrol"> DefinitionsをDescendingに設定し、この機能を有効 </span><span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span> にするには、Secendingを設定します。 </p> <p>また、検索フォームで <span class="codeph"> sp_sパラメータを複数回設定することで、複数の並べ替えフィールドを1つのク </span> エリに割り当てることもできます。 次のテンプレート行は、検索結果をアーティスト名、アルバム名、トラック名の順に並べ替えるように設定します。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>また、フィールド名の前にテーブル名修飾子を指定することで、テーブルと一致するフィールドデータを並べ替えることもできます（例：items.price）。 テーブルの一 <span class="codeph"> 致の詳細については、 </span> sp_field_tableパラメータを参照してください。 </p> <p>近接性で検索する場合は、「近接性出力フィールド」を指定して、近接性に従って結果を並べ替えることができます。 </p> <p>近接検索につ <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr=フィールド </span> </p> </td> 
   <td colname="col4"> <p>静的なランクに使用するランクフィールドを指定します。 このフィールドは、関連性が0より大きいRank型のフィールドである必要があります。 クエリーに <span class="codeph"> sp_srパラメ </span> ータが指定されていない場合は、「Rank」タイプのフィールドが自動的に選択されます。 </p> <p>特定のクエリーの静的ランクを無効にするには、 <span class="codeph"> sp_srにNULL値を含めます </span> (例： <span class="codeph"> &lt;input type="hidden" name="sp_sr" value=""&gt; </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= string </span> </p> </td> 
   <td colname="col4"> <p>検索テンプレートの <span class="codeph"> &lt;search-field-value-list&gt;タグと組み合わせて使用するフィー </span> ルドの名前を指定します。 </p> <p>複数の <span class="codeph"> sp_sfvl_fieldパラメータを指定で </span> きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;整数値&gt; </span></span> </p> </td> 
   <td colname="col4"> <p> 
     <!--NEW 2/2/2014-->この検索に対し <span class="codeph"> て、 <span class="varname"> </span> &lt;integer_value&gt; </span> <span class="codeph"> search-field-value-list動的ファセッ </span> トフィールドまでをリクエストします。 </p> <p>デフォルト値は 0 です。許可される最大値は、指定したインデックスに対して定義された、動的ファセットフィールド、動的ファセットフィールドの現在の数です。 0未満の整数値は0として扱われます。 dynamic-facet-field-countの上に指定 <span class="codeph"> した整数値は、動的 —facet-field-count </span> で <span class="codeph"> 大文字として扱われます </span>。 整数以外の値は無視されます。これらはデフォルト値として扱われます。 </p> <p>特定のスライスの検索は、このスライスの <span class="codeph"> dynamic-facet-field-count値の </span> sp_sfvl_df_count <span class="codeph"> の最大許容値で </span> 上限が設定されています。 スライスの結果をマージする場合、 <span class="codeph"> sp_sfvl_df_countの有効最大値は、すべてのスライスに対して実際に </span> 実行される <span class="codeph"> sp_sfvl_df_count </span> の最大値です。 </p> <p>動的ファセ <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> ットの設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span></span>&gt;|... </p> </td> 
   <td colname="col4"> <p> この検索の考慮対象から除外する特定の動的ファセットフィールドのリストを指定します。 </p> <p>デフォルトでは、すべての動的ファセットフィールドが考慮されます。 </p> <p>動的ファセ <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> ットの設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span></span>&gt;|.. </p> </td> 
   <td colname="col4"> <p> 検索結果に含める特定の動的ファセットフィールドのリストを指定します。 </p> <p> <p>注意： sp_ <span class="codeph"> sfvl_df_countパラメー </span> タは、返す動的ファセットフィールドの合計数を決定します。この数には、 <span class="codeph"> sp_sfvl_df_includeで指定したものも含まれます </span>。 つまり、 <span class="codeph"> sp_sfvl_df_includeを使用すると、返された動的ファセットフィールドの合計数が </span> sp_sfvl_df_countを超えることは許可されません <span class="codeph"></span>。 </p> </p> <p>動的ファセ <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> ットの設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>sp_staged=1 <span class="codeph"> がクエリ </span> ーと共に送信された場合、実行されるクエリーはステージ検索です。 </p> <p>ステージ検索では、インデックスやテンプレートを含む、現在ステージングされているすべてのコンポーネントが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day、sp_start_month、sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= number </span> </p> <p> <span class="codeph"> sp_start_month= number </span> </p> <p> <span class="codeph"> sp_start_year= number </span> </p> </td> 
   <td colname="col4"> <p>この3つの値によって、検索の開始日の範囲が指定され、セットとして指定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_suggest_q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_suggest_q= number </span> </p> </td> 
   <td colname="col4"> <p>sp_suggest_qパ <span class="codeph"> ラメー </span> ターは、Suggestサービスで使用するsp_q[_#] <span class="codeph"></span> パラメーターを決定します。 </p> <p>sp_suggest_qのデフォ <span class="codeph"> ルト値は0 </span> です。つまり、検索エンジンはsp_qの値を使用して提案を <span class="codeph"></span> 決定します。 </p> <p>sp_suggest_q=1 <span class="codeph"> を設定 </span> し、 <span class="codeph"> sp_q_1の値を使用し </span> て候補を決定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t=文字列 </span> </p> </td> 
   <td colname="col4"> <p>使用するトランスポートテンプレートを指定します。 </p> <p>このパラメーターは、検索アカウントの各領域に対して異なる検索トランスポートテンプレートを使用して、Webサイト全体での主要な検索結果の外観を制御する場合に役立ちます。 </p> <p>デフォルトのトランスポートテンプレートは「検索」です。 </p> <p>詳しくは、Webサ <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> イト用の複数のトランスポートテンプレートの管理を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>sp_stage=1と設定 <span class="codeph"> した場合、シミュレ </span>ーターでコア検索トレース機能を有効にします。 </p> <p>シミュレーターに <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> ついてを参照してくだ </a>さい。 </p> <p> <p>注意： このパラメーターを指定しない場合、コア検索ではトレース情報が収集されず、関連するコア検索テンプレートタグは出力されません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w、sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>この特定のクエリに対して、類似したサウンドの一致を有効または無効にすることを指定します。 </p> <p>'Exact'のsp_w_controlは無視されます。 サウンドに似た一致は無効です。 </p><p>'Alike'のsp_w_controlは無視されます。 サウンドに似た一致が有効</p><p>[その他]のsp_w_controlは1です。 サウンドに似た一致は無効です。 </p><p>[その他]に対するsp_w_controlは、他の何でも使用できます。 サウンドに似た一致は有効です。 </p>sp_w_controlパ <span class="codeph"> ラメータを使 </span> 用すると、エンドユーザがサウンドに似たマッチングを制御するための、否定的または肯定的な語句のチェックボックスを作成できます。 </p> <p>sp_w_control=0 <span class="codeph"> を使用す </span> ると、次の例のように、否定的な語句のチェックボックスが使用され <span class="codeph"> てsp_w </span> パラメータが設定されます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_control=1 <span class="codeph"> を使用す </span> ると、正の単語のチェックボックスが使用され、次のように <span class="codeph"> sp_wパラ </span> メータが設定されます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_controlおよびsp_wパラメータの使用例については、サンプルのアドバンス <span class="codeph"> 検索フォームを </span> 参照し <span class="codeph"> てくだ </span> さい。 </p> <p>詳しくは、アドバ <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> ンス検索フォームの例を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x=フィールド </span> </p> </td> 
   <td colname="col4"> <p>クエリ文字列を検索するフィールドを指定します。 anyは、すべてのフィールドを検索することを意味します。 タイトルとは、タイトルフィールドのみを検索することを意味します。 descは、ドキュメントの説明フィールドのみを検索することを意味します。 キーは、ドキュメントのキーワードのみを検索することを意味します。 bodyは、本文のみを検索することを意味します。 altは、代替テキストのみを検索することを意味します。 urlは、URL値のみを検索することを意味します。 targetは、ターゲットキーワードのみを検索することを意味します。 この場合、対応する <span class="codeph"> sp_qパラメーター内の「text:」、「desc:」、「keys:」、「body:」、「alt:」、「url:」および「target:」フィールドのプリフィックスのユーザー指定は無視さ </span> れます。 sp_xが <span class="codeph"> 存在しな </span> い場合、または空の文字列またはいずれかに設定されている場合は、標準のユーザーフィールドプレフィックスが許可されます。 フィールドの接頭辞について詳しくは、検索のヒントの説明を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> <p>sp_xパラメータの使用例については、サンプルのアドバンス検索フォームの説明を <span class="codeph"> 参照してく </span> ださい。 </p> <p>詳しくは、アドバ <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> ンス検索フォームの例を参照してくだ </a>さい。 </p> <p>オプション/メタデータ/デフォルトのメタデータ/sp_x <span class="uicontrol"> neveryを設定するクエリを、 </span> sp_x <span class="uicontrol"> neveryを設定するクエリを、 Search By </span><span class="uicontrol"></span><span class="uicontrol"></span><span class="codeph"></span>Defaultに設定されたすべてのフィールドを検索するクエリを作成できます。 sp_xパラメータの値として、事前定義フィールドとユーザ定義フィールドの両方を使 <span class="codeph"> 用でき </span> ます。 </p> <p>また、 <span class="codeph"> sp_xパラメータを複数回設定することで、1つのクエリーに複数のフィールドを割り当てる </span> こともできます。 次のテンプレート行を使用すると、「Great Books」の「タイトル」と「作成者」フィールドの両方を照会できます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#=フィールド名 </span> </p> </td> 
   <td colname="col4"> <p>このパラメーターは、対応する <span class="codeph"> sp_q_#クエリで検索するフィールドを指定し </span> ます。 # <span class="codeph"> は1 <span class="codeph"> ～ 16 </span> の数字( </span> sp_x_8など <span class="codeph"> )に置き換えられます </span>。 field-nameは、事前定義またはユーザ定義のフィールドです。 </p> <p>特定の番号付きクエリに対してSearch <span class="codeph"> By_#パラメータが指定されていない場合、Search By Defaultとして定義されるすべてのフィールドは、Metadata </span> &gt; <span class="uicontrol"> Sp </span><span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span> Default設定&gt; Queryによって検索されます。 </p> <p>例えば、次のフォームを送信すると、「author」フィールドに「Fitzgerald」という語を含む「great」という語を含むすべてのドキュメントが返されます。 </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>1回の検索リクエストで同じ <span class="codeph"> sp_xまたは </span> sp_x_#パラメータの複数のインスタンスを指定することで、複数のフィールド名を特定のクエリまたは番号付きクエリ <span class="codeph"></span> に関連付けることができます。 </p> <p>例えば、「body」と「keys」の両方のフィールドで「flower」という単語を検索するには、次の情報を含む検索フォームを作成します。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## バックエンド検索CGIパラメータの一般的な使用例 {#section_260012BBC2514CC9A8E02E53DE8B41EE}

次のリンククエリは、検索クエリとして「音楽」を使用して検索を開始し、すべてのデフォルトパラメータを使用します。 URLは読みやすくするために2行に分割されます。 HTMLでは、このリンクはすべて1行で記述する必要があります。

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

通常、フォームでは同じ機能が定義されます。

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

通常、検索を開始する際にはデフォルトのパラメータを使用する必要があります。 これにより、最初のページが関連性順に表示され、顧客は他のページや他のオプションを選択できます。 サイト上の検索フォームにコレクションのオプションが含まれる場合は、コレクション名をパラメーターとして渡します。

## バックエンド検索CGIパラメータの詳しい使用例 {#section_5FA3C620D5124FB2AB28857F8D8473F6}

次のフォームクエリは、結果から `25` 始まる結果を表示しま `10`す。 概要は表示されず、並べ替え順は日付順で、という名前のコレクションが使 `support` 用されます。 過去30日以内の日付のドキュメントのみが返されます。

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```

