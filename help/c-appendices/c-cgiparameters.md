---
description: 'null'
seo-description: 'null'
seo-title: CGIパラメーター
solution: Target
title: CGIパラメーター
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 9271dce5ed49a2d5d629011c29b60cc33e715c5d
workflow-type: tm+mt
source-wordcount: '1934'
ht-degree: 1%

---


# CGIパラメーター{#cgi-parameters}

## CGIパラメーター {#concept_F395999090FE4926B38BC73D5E612800}

## CGIパラメーターの検索 {#reference_DA27A8B0728246DA94994885E1353890}

サイトのHTMLにコピー&amp;ペーストできる検索フォームコードが用意されています( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**)。

「検索フォームのHTMLコードを…に [コピーする」を参照してください。](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

検索フォーム自体またはスクリプトから、リストに含まれるパラメーターを設定することもできます。 以下に示すパラメーターに加えて、バックエンド検索パラメーターを使用して検索を制御することもできます。

「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。

検索リクエストはベースURLで構成されます。 ベースURLは、顧客が検索しているアカウントを示し、関連するアカウントに対して目的の検索結果を返す方法を示すCGIパラメーターのセット（キーと値のペア）が示されます。

ベースURLは、特定のアカウントと、ステージングされた環境またはライブアカウントに関連付けられます。 アカウントマネージャーから、ベースURLの複数のエイリアスをリクエストできます。 例えば、Megacorpという会社のアカウントに2つのベースURLが関連付けられているとします。 `https://search.megacorp.com` と `https://stage.megacorp.com`。 前者のURLはライブインデックスを検索し、後者のURLはステージングされたインデックスを検索します。

3つの形式のCGIパラメーターがサポートされています。 デフォルトでは、次の例のように、CGIパラメーターをセミコロンで区切るようにアカウントが設定されています。

`https://search.megacorp.com?q=shoes;page=2`

必要に応じて、アカウントマネージャーに、CGIパラメーターを区切るアンパサンドを使用するようにアカウントを設定してもらうことができます。次に例を示します。

`https://search.megacorp.com?q=shoes&page=2`

3つ目の形式（SEO形式）もサポートされています。この形式では、次の例のように、区切り文字の代わりにスラッシュ `/` を使用し、等号を使用します。

`https://search.megacorp.com/q/shoes/page/2`

SEO形式を使用してリクエストが送信されると、すべての出力リンクは同じ形式で返されます。

| ガイド付き検索パラメーター | 例 | 説明 |
|--- |--- |--- |
| q | `q=string` | 検索のクエリ文字列を指定します。 このパラメーターはバックエンド検索パラメーターにマップ `sp_q` されます。  「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| q# | `q#=string` | ファセット設定（特定のフィールド内での検索）は、番号付きのqとxのパラメータを使って行います。  qパラメーターは、対応する番号付きxパラメーターで示されるように、ファセットで検索する用語を定義します。<br>例えば、sizeとcolorという名前の2つのファセットがある場合、q1=small;x1=size;q2=red;x2=colorのように指定できます。  このパラメーターはバックエンド検索パラメーターにマップ `sp_q_exact_#` されます。  <br>「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| x# | `q#=string` | ファセット設定（特定のフィールド内での検索）は、番号付きのqとxのパラメータを使って行います。  qパラメーターは、対応する番号付きxパラメーターで示されるように、ファセットで検索する用語を定義します。 <br>例えば、sizeとcolorという名前の2つのファセットがある場合、q1=small;x1=size;q2=red;x2=colorのように指定できます。  このパラメーターはバックエンド検索パラメーターにマップ `sp_x_#` されます。  <br>「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| コレクション | `collection=string` | 検索に使用するコレクションを指定します。  このパラメーターはバックエンド検索パラメーターにマップ `sp_k` されます。  「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| count | `count=number` | 表示する結果の合計数を指定します。  デフォルトは、 [!UICONTROL Settings ] > [!UICONTROL Searching ] >で定義されてい [!UICONTROL Searches ]ます。.  このパラメーターはバックエンド検索パラメーターにマップ `sp_c` されます。  「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| page | `page=number` | 返される結果のページを指定します。 |
| ランク | `rank=field` | 静的なランクに使用するランクフィールドを指定します。  フィールドは、0より大きい関連性を持つ「ランク」タイプのフィールドである必要があります。  このパラメーターはバックエン `sp_sr` ドパラメーターにマッピングされます。  「 [バックエンド検索CGIパラメーター](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)」を参照してください。 |
| 並べ替え | `sort=number` | 並べ替え順を指定します。<br>「0」はデフォルトで、関連性スコアで並べ替えられます。「1」は日付で並べ替えます。「 —1」は並べ替えを行いません。  ユーザーは、パラメーターの値のフィールド名を指定でき `sp_s` ます。  例えば、タイトルフィールドに含まれる値に従って結果を `sp_s=title` 並べ替えます。 フィールド名をパラメーターの値に使用すると、結果はそのフィールドで並べ替えられ、その後関連性で下位並べ替えられます。 ` sp_s `  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. 定義ページで、をクリックするか、特定のフィールド名 [!UICONTROL Add New Field ][!UICONTROL Edit ] をクリックします。 ドロップダウン [!UICONTROL Sorting ] リストで、またはのいずれかを選択し [!UICONTROL Ascending ] ま [!UICONTROL Descending ]す。 このパラメーターはバックエンド検索パラメーターにマップ `sp_s` されます。 <br>「 [バックエンド検索CGIパラメーター]」を参照してください。(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)。 |

## バックエンド検索CGIパラメーター {#reference_582E85C3886740C98FE88CA9DF7918E8}

通常、お客様はガイド付き検索と呼ばれるプレゼンテーションレイヤーとやり取りします。 ただし、理論的には、Guided Searchレイヤーをスキップし、このページで説明するCGIパラメーターを使用してバックエンドのコア検索と直接やり取りすることは可能です。

次の表から、バックエンド検索のCGIパラメーターを選択できます。
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>単一クエリのサポート </p> </th> 
   <th colname="col03" class="entry"> <p>複数クエリのサポート </p> </th> 
   <th colname="col3" class="entry"> <p>例 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>アカウント番号の文字列を指定します。 このパラメーターは必須で、有効なアカウント番号文字列である必要があります。 アカウント番号の文字列は、 <span class="uicontrol"> 設定/アカウントオプション/アカウント </span> 設定で確認でき <span class="uicontrol"></span><span class="uicontrol"></span>ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p>がクエリ <code>sp_advanced=1 </code> と共に送信された場合、タグと検索テンプレート内の <code>&lt;search-if-advanced&gt; </code><code>&lt;/search-if-advanced&gt; </code> タグとの間のすべてのコードが検索フォームに使用されます。 タグとタグの間のコ <code>&lt;search-if-not-advanced&gt; </code> ードはすべて無視 <code>&lt;/search-if-not-advanced&gt; </code> されます。 送信された場合 <code>sp_advanced=0 </code> （またはその他の値）、&lt;search-if-advanced&gt;テンプレートブロックは無視され、&lt;search-if-not-advanced&gt;テンプレートブロックが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>表示する結果の合計数を指定します。 デフォルトは 10 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>特定のフィールドのコンテキスト情報を収集します。 収集した情報は、テンプレートタグを介して検索結果に出力され <code>&lt;search-context&gt; </code> ます。 デフォルト値は <code>body </code> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>実行する日付範囲検索のタイプを指定します。 指定可能な値は「any」（日付範囲検索を実行しない）、「custom」(の値を検索する日付の決定に使用する <code>sp_date_range </code> 必要がある)、「 <code>sp_start_day </code>, <code>sp_start_month </code><code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code>」、「」の値を使用して検索する日付範囲の決定に使用する <code>sp_end_year </code> )です。 <code>sp_d </code> は、検索フォームに、カスタム範囲(経由 <code>sp_date_range </code>)、または特定の開始と終了日の範囲で検索するオプションが含まれる場合にのみ必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>対応する <code>sp_q_# </code> クエリに対して実行する日付範囲検索のタイプを指定します。 「#」は1 ～ 16の間の数字に置き換えられます(例えば、番号付きクエリ <code>sp_d_8 </code>に適用され <code>sp_q_8 </code>ます)。 </p> <p>日付範囲検索を実行しないことを意味し、の値を検索する日付の決定に使用する <code>type </code> ことを示す値、特定の値を <code>sp_date_range_# </code> 示す値、 <code>sp_q_min_day_# </code>、 <code>sp_q_min_month_# </code>、、 <code>sp_q_min_year_# </code>、、 <code>sp_q_max_day_# </code>カスタム、およびカスタムの値を使用して日付範囲を決定することを示す値を設定でき <code>sp_q_max_month_# </code><code>sp_q_max_year_# </code> ます。 の使用は、検索フォーム <code>sp_d_# </code> に、カスタム範囲（経由）または特定の開始と終了日の範囲で検索するオプションが含まれている場合にのみ必要で <code>sp_date_range_# </code>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>検索に適用する事前定義の日付範囲を指定します。 0以上の値は、今日より前に検索する日数を指定します。例えば、「0」の値は「today」を、「1」の値は「today and yesterday」を、「30」の値は「within thast 30 days」を示します。 </p> <p>0未満の値は、次のようにカスタム範囲を指定します。 </p> <p>-1 = "なし"（日付範囲なしを指定した場合と同じ）。 </p> <p>-2 = "今週"。現在の週の日曜日から土曜日を検索します。 </p> <p>-3 = "先週"。現在の週の前の週の日曜日から土曜日を検索します。 </p> <p>-4 = "今月"（現在の月内の日付を検索） </p> <p>-5 = "先月"。現在の月の前の月内の日付を検索します。 </p> <p>-6 = "今年"（現在の年内の日付を検索） </p> <p>-7 = "昨年"。現在の年の前の年内の日付を検索します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>対応する <code>sp_q_# </code> クエリに適用する、事前定義済みの日付範囲を指定します。 「#」は1 ～ 16の間の数字に置き換えられます(例えば、番号付きクエリ <code>sp_date_range_8 </code>に適用され <code>sp_q_8 </code>ます)。 </p> <p>0以上の値は、今日より前に検索する日数を指定します。 例えば、0を指定すると今日が指定されます。値1は今日と昨日を指定します。値を30に設定すると、過去30日以内の期間が指定されます。 </p> <p>0未満の値は、次のようにカスタム範囲を指定します。 </p> <p>-1 = "なし"（日付範囲なしを指定した場合と同じ）。 </p> <p>-2 = "今週"。現在の週の日曜日から土曜日を検索します。 </p> <p>-3 = "先週"。現在の週の前の週の日曜日から土曜日を検索します。 </p> <p>-4 = "今月"（現在の月内の日付を検索） </p> <p>-5 = "先月"。現在の月の前の月内の日付を検索します。 </p> <p>-6 = "今年"（現在の年内の日付を検索） </p> <p>-7 = "昨年"。現在の年の前の年内の日付を検索します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>検索結果を重複除外する単一のフィールドを指定します。 そのフィールドの重複結果はすべて検索結果から削除されます。 例えば、特定のタイトルに対する上位の結果のみ <code>sp_dedupe_field=title </code>が検索結果に表示されます（2つの結果が同じタイトルフィールドのコンテンツを持つことはありません）。 複数値(許可リスト)タイプのフィールドの場合は、フィールドの内容全体が比較に使用されます。 1つのフィールドのみを指定できます。 フィールド名に「table-qualifier」は使用できません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>数字を超える文字を含むクエリ文字列の任意の単語に対して、自動ワイルドカード拡張を行うように指定します。 つまり、「クエリ」や「数値」など5文字以上の単語をワイルドカード文字「*」で展開するように <code>sp_e=5 </code> 指定すると、検索は「クエリ*」や「数値*」と同じになります。 文字数の少ない単語は拡張されないので、「word」を検索しても、ワイルドカードによる自動拡張は行われません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>数字を超える文字を含む対応する <code>sp_q_# </code> クエリ文字列の任意の単語に対して、自動ワイルドカード拡張を行うように指定します。 つまり、「クエリ」や「数値」のように、 <code>sp_e_2=5 </code> クエリ列に5文字以上含まれる単語をワイルドカード文字「 <code>sp_q_2 </code><code>* </code>」で展開し、「クエリ*」や「数値*」と同じ検索結果にすることを指定します。 文字数の少ない単語は拡張されないので、での「単語」の検索では、ワイルドカードの自動拡張 <code>sp_q_2 </code> は行われません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day、sp_end_month、sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>この3項目の値は、検索の終了日の範囲を指定し、セットとして指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>クエリパラメーター文字列(など <code>sp_q </code>)の文字セットを指定します。 この文字列は、検索フォームが含まれるページの文字セットと常に一致する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>指定したフィールドから成る論理データテーブルを定義します。 例えば、「color」、「size」、「price」の各フィールドから成る「items」という名前のテーブルは、次のように定義されます。 </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>論理テーブルは、「許可リスト」がチェックされているフィールド( <span class="uicontrol"> 設定/ </span> メタデータ <span class="uicontrol"> / </span> 定義 <span class="uicontrol"> の下 </span>)と併用すると最も役立ちます。 フィールド名を値として使用するすべてのCGIパラメーターとテンプレートタグでは、必要に応じてテーブル名の後に「。」を付けて指定できます。 」をフィールド名の前に置きます(例： <code>sp_x_1=tablename.fieldname </code>)。 </p> <p>例えば、サイズが「large」の1つ以上の「red」ドキュメントを含むアイテム（アイテムがメタデータの平行な行として表される）を検索するには、次を使用します。 </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>&lt;search-field-value-list&gt; </code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

## バックエンド検索CGIパラメーターの一般的な使用例 {#section_260012BBC2514CC9A8E02E53DE8B41EE}

次のリンククエリは、検索クエリとして「Music」を使用して検索を開始し、すべてのデフォルトパラメータを使用します。 URLは読みやすくするために2行に分割されます。 HTMLでは、このリンクはすべて1行に記述する必要があります。

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

同じ機能は、フォームにより一般的に定義されます。

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

通常、検索を開始する際は、デフォルトのパラメーターを使用する必要があります。 これにより、最初のページが関連性順に表示され、顧客が他のページや他のオプションを選択できるようになります。 サイトの検索フォームにコレクションのオプションが含まれる場合は、コレクション名をパラメーターとして渡します。

## バックエンド検索CGIパラメーターの詳しい使用例 {#section_5FA3C620D5124FB2AB28857F8D8473F6}

次のフォームクエリには、結果から開始する `25` 結果が表示され `10`ます。 概要が表示されず、並べ替え順が日付順になり、という名前のコレクション `support` が使用されます。 過去30日以内の日付のドキュメントのみが返されます。

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

