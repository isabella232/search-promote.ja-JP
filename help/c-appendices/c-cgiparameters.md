---
description: 'null'
seo-description: 'null'
seo-title: CGIパラメーター
solution: Target
title: CGIパラメーター
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '5490'
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

次の表から、バックエンド検索CGIパラメーターを選択できます。
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
   <td colname="col3"> <p> <span class="codeph"> sp_a=文字列 </span> </p> </td> 
   <td colname="col4"> <p>アカウント番号の文字列を指定します。 このパラメーターは必須で、有効なアカウント番号文字列である必要があります。 アカウント番号の文字列は、 <span class="uicontrol"> 設定/アカウントオプション/アカウント </span> 設定で確認でき <span class="uicontrol"></span><span class="uicontrol"></span>ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>sp_advanced=1 <span class="codeph"> がクエリと共に送信さ </span> れた場合、検索フォームでは、 <span class="codeph"> &lt;search-if-advanced&gt; </span> タグと検索テンプレート内の <span class="codeph"> &lt;/search-if-advanced&gt; </span> タグの間のすべてのコードが使用されます。 &lt;search-if-not-advanced&gt;タグと <span class="codeph"> &lt;/search-if-not-advanced&gt; </span><span class="codeph"></span> タグの間のコードはすべて無視されます。 sp_advanced=0 <span class="codeph"></span> （またはその他の値）が送信された場合、&lt;search-if-advanced&gt;テンプレートブロックは無視され、&lt;search-if-not-advanced&gt;テンプレートブロックが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c=数値 </span> </p> </td> 
   <td colname="col4"> <p>表示する結果の合計数を指定します。 デフォルトは 10 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>特定のフィールドのコンテキスト情報を収集します。 収集した情報は、 <span class="codeph"> &lt;search-context&gt; </span> テンプレートタグを介して検索結果に出力されます。 The default value is <span class="codeph"> body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d=タイプ </span> </p> </td> 
   <td colname="col4"> <p>実行する日付範囲検索のタイプを指定します。 日付範囲検索を行わない任意の値を指定する。カスタムは、検索する日付をsp_date_rangeの値を使用して検索する <span class="codeph"> べき値を示し、sp_ </span> 開始のsp_ <span class="codeph"> end_sp_end, sp_endの開始sp_sp_ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> endの開始を示す。年は、日付の範囲を調べます。 <span class="codeph"> sp_d </span> は、検索フォームにカスタム範囲（sp_date_rangeを使用）または特定の開始と終了日の範囲で検索するオプションが含まれている場合にのみ必要 <span class="codeph"></span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#=タイプ </span> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_# </span> クエリに対して実行する日付範囲検索のタイプを指定します。 「#」は1 ～ 16の数字に置き換えられます( <span class="codeph"> sp_d_8など、番号付きクエリ </span>sp_q_8に適用され <span class="codeph"></span>ます)。 </p> <p>typeは任意に設定できます。日付範囲検索は実行しません。 <span class="codeph"> sp_date_range_#の値は検索する日付の決定に使用され、sp_ </span> date_#の値は検索する日付の決定に使用され、sp_min_day_day_#はsp_min_ <span class="codeph"> month_ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> p_max日付の範囲を決定するには、_max_sp_max_month#を使用し、sp_max_year#を使用します。 sp_d_#の使用は、検索フォームにカスタム範囲（sp_date_range_#を使用）または特定の開始と <span class="codeph"> 終了日の範囲で検索するオプションが含まれている場合にのみ必要 </span><span class="codeph"></span>です。 </p> </td> 
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
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_# </span> クエリに適用する、事前定義済みの日付範囲を指定します。 「#」は、1 ～ 16の間の数字に置き換えられます( <span class="codeph"> sp_date_range_8など、番号付きクエリsp_q_8 </span>に適用され <span class="codeph"></span>ます)。 </p> <p>0以上の値は、今日より前に検索する日数を指定します。 例えば、0を指定すると今日が指定されます。値1は今日と昨日を指定します。値を30に設定すると、過去30日以内の期間が指定されます。 </p> <p>0未満の値は、次のようにカスタム範囲を指定します。 </p> <p>-1 = "なし"（日付範囲なしを指定した場合と同じ）。 </p> <p>-2 = "今週"。現在の週の日曜日から土曜日を検索します。 </p> <p>-3 = "先週"。現在の週の前の週の日曜日から土曜日を検索します。 </p> <p>-4 = "今月"（現在の月内の日付を検索） </p> <p>-5 = "先月"。現在の月の前の月内の日付を検索します。 </p> <p>-6 = "今年"（現在の年内の日付を検索） </p> <p>-7 = "昨年"。現在の年の前の年内の日付を検索します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>検索結果を重複除外する単一のフィールドを指定します。 そのフィールドの重複結果はすべて検索結果から削除されます。 例えば、 <span class="codeph"></span>sp_dedupe_field=titleの場合、特定のタイトルに対する最上位の結果のみが検索結果に表示されます（2つの結果が同じタイトルフィールドのコンテンツを持つことはありません）。 複数値(許可リスト)タイプのフィールドの場合は、フィールドの内容全体が比較に使用されます。 1つのフィールドのみを指定できます。 フィールド名に「table-qualifier」は使用できません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e=数値 </span> </p> </td> 
   <td colname="col4"> <p>数字を超える文字を含むクエリ文字列の任意の単語に対して、自動ワイルドカード拡張を行うように指定します。 つまり、 <span class="codeph"> sp_e=5は、「クエリ」や「数値」など5文字以上の単語をワイルドカード文字「*」で展開し、「クエリ*」や「数値*」と同じ検索にすることを </span> 指定します。 文字数の少ない単語は拡張されないので、「word」を検索しても、ワイルドカードによる自動拡張は行われません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= number </span> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"></span> sp_q_#クエリ文字列の任意の単語に対して、数値文字を超える自動ワイルドカード拡張を行うことを指定します。 つまり、 <span class="codeph"> sp_e_2=5は、「クエリ」や「数値」など、sp_q_2 </span> クエリ列に5文字以上含まれる単語をワイルドカード文字「 <span class="codeph"></span><span class="codeph"></span>* 」で展開することを指定し、「クエリ*」や「数値*」の検索と同じ検索結果になります。 文字数の少ない単語は拡張されないので、 <span class="codeph"> sp_q_2で「word」を検索しても、ワイルドカードの自動拡張 </span> は行われません。 </p> </td> 
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
   <td colname="col3"> <p> <span class="codeph"> sp_f=文字列 </span> </p> </td> 
   <td colname="col4"> <p>クエリパラメータ文字列の文字セット( <span class="codeph"> sp_qなど </span>)を指定します。 この文字列は、検索フォームが含まれるページの文字セットと常に一致する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>指定したフィールドから成る論理データテーブルを定義します。 例えば、「color」、「size」、「price」の各フィールドから成る「items」という名前のテーブルは、次のように定義されます。 </p> <p> <span class="codeph"> sp_field_table=items:color,size,price </span> </p> <p>論理テーブルは、「許可リスト」がチェックされているフィールド( <span class="uicontrol"> 設定/ </span> メタデータ <span class="uicontrol"> / </span> 定義 <span class="uicontrol"> の下 </span>)と併用すると最も役立ちます。 フィールド名を値として使用するすべてのCGIパラメーターとテンプレートタグでは、必要に応じてテーブル名の後に「。」を付けて指定できます。 フィールド名の前( <span class="codeph"> sp_x_1=tablename.fieldnameなど </span>)。 </p> <p>例えば、サイズが「large」の1つ以上の「red」ドキュメントを含むアイテム（アイテムがメタデータの平行な行として表される）を検索するには、次を使用します。 </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> 値 </span> </span> </p> </td> 
   <td colname="col4"> <p>レポートを生成する際に検索を無視します。 </p> <p>このクエリを使用して、Did You Meanが生成する検索や、管理者がメンバセンターで生成する検索など、特定のバックエンド検索をマスクします。 エンドユーザはこのような検索タイプを生成しないので、様々なAdobeSearch&amp;Promoteレポートには表示されません。 </p> <p>有効な値は、 <span class="codeph"> sp_i=1 </span> および <span class="codeph"> sp_i=2 </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k=文字列 </span> </p> </td> 
   <td colname="col4"> <p> 検索に使用するコレクションを指定します。 デフォルト値はコレクションなしです。つまり、検索にはサイト全体が含まれる必要があります。 </p> <p>検索フォームでのコレクションの <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> 使用を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l=文字列 </span> </p> </td> 
   <td colname="col4"> <p>クエリパラメータ文字列の言語を指定します( <span class="codeph"> sp_qなど </span>)。 この <i><span class="codeph"></span></i> 文字列は、ISO-639言語コードの後にオプションでISO-3166国コードが続く標準ロケールIDにする必要があります。 例えば、英語は「en」または「en_US」、日本語は「ja」または「ja_JP」です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0または1 </span> </p> </td> 
   <td colname="col4"> <p> sp_literal=1を設定すると、 <span class="codeph"></span> クエリ内の単語を解釈する可能性のあるすべての機能が一時的に無効になります。 このパラメーターを使用すると、同義語、代替単語フォームおよび類似音の一致に関係なく、クエリのリテラル語句のみがドキュメントに一致します。 </p> <p>sp_literal=0は意味を持たないこ <span class="codeph"></span> とに注意してください。この値を使用すると無視されます。 </p> <p>辞書につ <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m=数値 </span> </p> </td> 
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
   <td colname="col4"> <p> 実行する検索のデフォルトの種類を指定します。 「 <span class="codeph"></span> any」を使用すると、クエリ文字列から任意の単語を含むドキュメントを検索できます。 「 <span class="codeph"></span> all」を使用すると、クエリ文字列に含まれるすべての単語を含むドキュメントを検索できます。 phraseを使用すると、 <span class="codeph"></span> クエリ文字列は引用符で囲まれたフレーズとして扱われ、ユーザーが入力した引用符はすべて無視されます。 </p> <p>フレ <span class="codeph"> ーズ </span> とす <span class="codeph"></span>べての場合、検索語の前にある「+」と「 — 」の指定は無効になり、これらの文字は無視されます。 sp_p <span class="codeph"></span> が存在しない場合、または空の文字列または任意の値に設定されている場合は、標準の「+」と「 — 」の単語プリフィックスが許可されます。 </p> <p>検索でプラス(「+」)とマイナス(「 — 」)を使用する方法について詳しくは、検索ヒントの説明を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> <p>sp_pパラメータの使用例については、サンプルのアドバンス検索フォームを参照して <span class="codeph"> く </span> ださい。 </p> <p>詳しくは、「 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> アドバンス検索フォームの例」を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#=任意/すべて/フレーズ </span> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_# </span> クエリで実行する検索のデフォルトのタイプを指定します。 「#」は1 ～ 16の数字に置き換えられます(例えば、 <span class="codeph"> sp_p_8は番号付きクエリ </span> sp_q_8に当てはまり <span class="codeph"></span>ます)。 anyを使用すると、クエリ文字列から任意の単語を含むドキュメントが返され <span class="codeph"></span> ます。 allを使用すると、クエリ文字列内のすべての単語を含むドキュメントが返されます。 <span class="codeph"></span> フレーズを使用すると、 <span class="codeph"></span> クエリ文字列が完全なフレーズとして扱われます（そして、ユーザーが入力した引用符はすべて無視されます）。 </p> <p>す <span class="codeph"> べてまたは </span><span class="codeph"></span>フレーズのいずれかを指定した場合、検索語の前にあるプラス記号とマイナス記号は無視されます。 sp_p_# <span class="codeph"> を省略した場合、または空の文字列または </span><span class="codeph"></span>任意の値に設定した場合は、標準の「+」プリフィックスと「 — 」プリフィックスが許可されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> 適用するターゲットの一致タイプを指定します。 完全一致を使用すると、ターゲットコンテンツ内のドキュメント文字列と完全に一致するクエリ内でのみ、利益ターゲットが一致することを <span class="codeph"></span> 意味します。 等価の使用は、単語の順序が重要でないという点を除いて、完全一致 <span class="codeph"></span> と同様です。 compatibleを使用すると、 <span class="codeph"> sp_pパラメータの値に基づいて、ターゲットの一致タイプが </span> 自動的に設定され <span class="codeph"></span> ます。 sp_pが <span class="codeph"> 全てのフレーズである場合は、 </span> exactを使用し、 <span class="codeph"> sp_pが全てのフレーズである場合は、 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> exactを使用します。 デフォルト値の <span class="codeph"> sp_pt </span> は <span class="codeph"> 互換性があり </span>ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>対応する <span class="codeph"> sp_q_# </span> クエリで適用するターゲットの一致タイプを指定します。 「#」は1 ～ 16の数字に置き換えられます(例えば、 <span class="codeph"> sp_p_8は番号付きクエリ </span> sp_q_8に当てはまり <span class="codeph"></span>ます)。 完全一致を使用すると、ターゲットコンテンツ内のドキュメント文字列と完全に一致するクエリ内でのみ、利益ターゲットが一致することを <span class="codeph"></span> 意味します。 等価な文字の使用は、単語の順序が重要でないという点を除き、 <span class="codeph"> 完全一致と同じで </span><span class="codeph"></span>す。 compatibleを使用すると、対応する <span class="codeph"> sp_p_#パラメータの値に基づいて、ターゲットの一致タイプが </span> 自動的に設定され <span class="codeph"></span> ます。 <span class="codeph"> sp_p_# </span> がすべてまたはフレーズの場合はexactが使用され、それ以外の場合は <span class="codeph"> 等価 </span><span class="codeph"></span> が使用されます。 デフォルト値の <span class="codeph"> sp_pt_# </span> は <span class="codeph"> 互換性があり </span>ます。 </p> </td> 
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
   <td colname="col4"> <p>このパラメーターを使用すると、検索フォームで複数のクエリを作成できます。 sp_q_# <span class="codeph"></span> クエリには、指定した番号付きで使用するクエリ文字列が含まれます。 検索リクエストは、最大16個の異なる番号付きクエリ( <span class="codeph"> sp_q_1 ～ </span> sp_q_16 <span class="codeph"></span>)を参照できます。 </p> <p>例えば、次のフォームを送信すると、「great」と「books」という語を含むすべてのドキュメントが返されます。 </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day、sp_q_month、sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q _day_#、sp_q _month_#、sp_q _year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day=整数値 </span> </p> <p> <span class="codeph"> sp_q_month=整数値 </span> </p> <p> <span class="codeph"> sp_q_year=整数値 </span> </p> <p> <span class="codeph"> sp_q_day_#=整数値 </span> </p> <p> <span class="codeph"> sp_q_month_#=整数値 </span> </p> <p> <span class="codeph"> sp_q_year_#=整数値 </span> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、特定のクエリの正確な日付を指定するために使用されます。 sp_q_day、 <span class="codeph"> sp_q_month、およびsp_q_yearの各 </span>パラメータは、メインクエリ( <span class="codeph"> sp_q_ </span><span class="codeph"></span><span class="codeph"></span>hon)に適用されます。 </p> <p><span class="codeph"> # </span>パラメーターは、1 ～ 16の間の数字に置き換えられます(例えば、番号付きクエリ <span class="codeph"> sp_q_6に該当するsp_q_day_6 </span><span class="codeph"></span>)。 デフォルトでは、すべての日付はグリニッジ標準時を基準に検索されます。 </p> <p>コードの次のセクションでは、「Jan」の日付のドキュメントで「orange」という語を検索できます。 PublishDateという名前のユーザ定義フィールドの「1st, 2000」 <span class="codeph"> は、次のようになり </span>ます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、場所をメインパラメーターまたは番号付きクエリーに関連付けます。 sp_q_locationを使用すると、メイン <span class="codeph"> クエリsp_q_location_# </span> ( <span class="codeph"></span><span class="codeph"></span> #は1 ～ 16の数字で置き換えられます)に影響し、指定した番号付きクエリに影響します。 これらのパラメータは、各サイトページに対してインデックス化された場所データに対して、最小および/または最大距離の近接性検索を実行するために使用されます。 値の形式によって、解釈が決まります。 </p> <p>DDD（3桁の数値）の形式の値は、米国の電話領域と解釈されます。DDDDDDまたはDDDDDD-DDDDDの形式の値は、USのzipcodeとして解釈されます。また、±DDD.DDDD±DDD.DDDDの形式の値は緯度と経度のペアとして解釈されます。 各値に記号が必要です。 例えば、+38.6317+120.5509は緯度38.6317、経度120.5509を指定します。 </p> <p>近接検索 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、近接検索に適用される関連性の計算を制御します。 sp_q_max_relevant_distanceの使用は、メインクエリsp_q_max_relevant_distance_# ( <span class="codeph"> #は1 ～ 16の数字で置き換えられる)に </span> 影響し、指定された番号付きクエリ <span class="codeph"></span><span class="codeph"></span> に影響します。 </p> <p>sp_q_max_relevant_distanceのデフォルト <span class="codeph"> 値 </span> は100です。 </p> <p>近接性コンポーネントの完全な関連性スコアは、0の距離を表します。 近接性コンポーネントの最小関連スコアは、指定した <span class="codeph"> sp_q_max_relevant_distance_# </span> 値のすぐ上の距離を表します。 </p> <p>近接検索 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day、sp_q_min_month、sp_q_min_year </p> <p>sp_q_max_day、sp_q_max_month、sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#、sp_q_min_month_#、sp_q_min_year_# </p> <p> sp_q_max_day_#、sp_q_max_month_#、sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>これらのパラメーターは、特定のクエリの最小および最大の日付範囲を設定するために使用されます。 sp_q_day, sp_q_min_month, sp_q_ <span class="codeph"> min_month, sp_q_q_min_year </span>sp_q_max_ <span class="codeph"> max_q_max_q_max_q_max sp_max sp_max sp_max sp_maxクエリ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><i></i><span class="codeph"></span>sp_min_s </p> <p>パラメーター名 <span class="codeph"> の </span>#は、1 ～ 16の間の数字に置き換えられます(例えば、 <span class="codeph"> sp_q_min_day_6は番号付きクエリ </span> sp_q_6に <span class="codeph"> 適用されます </span>)。 </p> <p>最小の日付のみ、最大の日付のみ、または最小と最大の日付の両方を指定できます。 ただし、最小または最大値を指定する場合は、3つの日付パラメーターをすべて指定する必要があります（日、月、年）。 デフォルトでは、すべての日付はグリニッジ標準時を基準に検索されます。 </p> <p>次のコードのセクションでは、2000年1月1日から2000年12月31日の間の日付を持つドキュメントで、「orange」という語をPublishDateというユーザ定義フィールドで検索でき <span class="codeph"></span>ます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
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
   <td colname="col4"> <p>これらのパラメーターは、メインパラメーターまたは番号付きクエリーに適用する最小（および/または最大）値を指定します。 sp_q_min、 <span class="codeph"> sp_q_max、 </span>sp_q_exactの使用は、メインクエリ( <span class="codeph"> sp_q  ) </span><span class="codeph"></span><span class="codeph"></span>に影響を与えます。 </p> <p>パラメータ名 <span class="codeph"> の# </span>を1 ～ 16の間の数字に置き換えます(例えば、 <span class="codeph"> sp_q_min_8は番号付きクエリ </span> sp_q_8に適用され <span class="codeph"></span>ます)。 </p> <p>sp_q_exact_#は、 <span class="codeph"> sp_q_min_# </span> と <span class="codeph"> sp_q_max_#の両方を同じ値で指定する場合の略記 </span><span class="codeph"></span> 法です。 sp_q_exact_# <span class="codeph"> を指定 </span> した場合、対応する <span class="codeph"> sp_q_min_# </span> または <span class="codeph"> sp_q_max_# </span> パラメータは無視されます。 </p> <p>sp_q_min_# <span class="codeph"> 、sp_q_max_# </span>、および <span class="codeph"> sp_q_exact_#の各 </span><span class="codeph"></span> パラメーターでは、必要に応じて、複数の「|」区切り値を指定できます。 例えば、「color」フィールド内に緑または赤の値を含むドキュメントを検索するには、次のように記述します。 <span class="codeph"> ...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q _nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1または0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1または0 </span> </p> </td> 
   <td colname="col4"> <p>デフォルトのパラメーター値は <span class="codeph"> 0で、共通フレーズ拡張が実行され </span> ることを意味します。 </p> <p>対応する検索クエリに対して1を設定す <span class="codeph"></span> ると、共通フレーズの拡張は実行されません。 </p> <p>sp_q_nocpを使用すると、メ <span class="codeph"> イン検索クエリパラメータ </span> sp_qに <span class="codeph"> 影響が及び </span>ます。 このパラメーターを番号付き検索クエリに適用するには、パラメーター名の <span class="codeph"> # </span> を対応する番号に置き換えます。 例えば、 <span class="codeph"> sp_q_nocp_8は、番号付き検索クエリ </span> sp_q_8に <span class="codeph"> 適用され </span>ます。 </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q _required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1または0または —1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1または0または —1 </span> </p> </td> 
   <td colname="col4"> <p>このパラメーターは、結果ページにドキュメントを返すために、対応するクエリに一致が必要(1)か、5月(0)か、発生しない(-1)かを決定します。 </p> <p>sp_q_requiredの使用は、メ <span class="codeph"> インクエリ( </span> sp_q <span class="codeph"></span>)に影響を与えます。 </p> <p>番号付きクエリに適用するには、パラメーター名 <span class="codeph"> の </span> #を対応する番号に置き換えます(例えば、 <span class="codeph"> sp_q_required_8は番号付きクエリ </span> sp_q_8に <span class="codeph"> 適用され </span>ます)。 パラメーターのデフォルト値は1です（一致する必要があります）。 </p> <p>ユーザー定義の「platform」フィールドで、「calc」という語を含み、「mac」、「win」、「all」を含まないドキュメントを検索する場合、HTML検索フォームに次の行が含まれます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
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
   <td colname="col2"> <p>sp_転送者 </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_転送者= url </span> </p> </td> 
   <td colname="col4"> <p>検索の転送者URLを指定します。 検索結果が検索フォームと同じサイトにリンクして戻る検索書き換えルールに役立ちます。 </p> <p>デフォルト値は、ブラウザーが提供する標準のCGI HTTP_転送者値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> フィールド </span>: <span class="varname"> 関連性 </span> </span> </p> </td> 
   <td colname="col4"> <p>フィールド名ごとの検索時間、関連性の制御（オプション）を許可します。 パラメーター名 <span class="codeph"> のro </span> は、「関連性の上書き」を表します。 このパラメーターは、1つ以上のフィールド名の後にコロンを付け、続いて0 ～ 10の関連値を受け取ります。 </p> <p>例えば、フィールド名「body」の関連性の値を10に設定する場合、顧客が検索を実行する際、このパラメーターは次のように表示されます。 </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>パラメータ文字列で複数のフィールド関連性の上書きを指定する場合は、パイプ区切り文字を使用できます。 例えば、「body」と「title」というフィールド名の関連性の値を9に設定する場合、顧客が検索を実行したときのパラメーターは次のように表示されます。 </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>注意： 関連する検索に関係しないフィールドを指定しても効果はありません。 例えば、 <span class="codeph"> sp_ro=title:10と設定したが、 </span>タイトル <span class="codeph"> フィールド名は検索されない場合、 </span> sp_ro <span class="codeph"></span> パラメータは無効です。 つまり、 <span class="codeph"></span> sp_roパラメーターを使用してフィールド名を指定しても、そのフィールドは自動的には検索されません。代わりに、この値はフィールドの関連する関連設定よりも優先されます。 </p> </p> <p>詳しくは、事前定義またはユーザ定義のmetaタグフィールドの <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> 編集を参照してくだ </a>さい。 </p> <p>「クエリクリーニングルール <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> について」を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= number </span> </p> </td> 
   <td colname="col4"> <p>並べ替え順を指定します。 ゼロ(0)はデフォルトで、関連性スコアで並べ替えることを意味します。 1つは日付順に並べ替えることを意味し、-1は並べ替えを行わないことを意味します。 </p> <p><span class="codeph"> sp_sパラメータの値にフィールド名を指定でき </span> ます。 例えば、 <span class="codeph"></span> sp_s=titleは、タイトルフィールドに含まれる値に従って結果を並べ替えます。 フィールド名を <span class="codeph"> sp_s </span> パラメータの値に使用すると、結果はそのフィールドで並べ替えられ、その後関連性で下位に並べ替えられます。 </p> <p>参照されるフィールドの並べ替えを設定します。または、設定/メタデータ/メタデータの <span class="uicontrol"> 定義を設定して、この </span> 機能を有効に <span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span> します。 </p> <p>検索フォームで <span class="codeph"> sp_sパラメータを複数回設定することで、複数の並べ替えフィールドを1つのクエリに割り当てることもで </span> きます。 次のテンプレート行は、検索結果をアーティスト名、アルバム名、トラック名の順に並べ替えるように設定します。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>また、フィールド名の前にテーブル名修飾子を指定し、例えばitems.priceのように、テーブルと一致するフィールドデータを並べ替えることもできます。 テーブルの一致の詳細については、 <span class="codeph"> sp_field_table </span> パラメータを参照してください。 </p> <p>近接性で検索する場合、「近接性出力フィールド」を指定して、近接性に従って結果を並べ替えることができます。 </p> <p>近接検索 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr=フィールド </span> </p> </td> 
   <td colname="col4"> <p>静的なランクに使用するランクフィールドを指定します。 フィールドは、0より大きい関連性を持つ「ランク」タイプのフィールドである必要があります。 クエリに <span class="codeph"> sp_sr </span> パラメータが指定されていない場合は、Rankタイプのフィールドが自動的に選択されます。 </p> <p>特定のクエリの静的ランキングを無効にするには、 <span class="codeph"> sp_srにNULL値を含め </span> ます(例： <span class="codeph"> &lt;input type="hidden" name="sp_sr" value=""&gt; </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field=文字列 </span> </p> </td> 
   <td colname="col4"> <p>検索テンプレートで <span class="codeph"> &lt;search-field-value-template&gt; </span> タグと組み合わせて使用するフィールドの名前を指定します。 </p> <p>複数の <span class="codeph"> sp_sfvl_field </span> パラメータを指定できます。 </p> </td> 
  </tr> 
  <tr>
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;整数値&gt; </span> </span> </p> </td> 
   <td colname="col4"> <p> この検索に対して、 <span class="codeph"> &lt;integer_value&gt;までの <span class="varname"></span></span> 検索フィールド — 値 —リスト動的ファセット <span class="codeph"></span> フィールドを要求します。 </p> <p>デフォルト値は 0 です。許可される最大値は、特定のインデックスに対して定義されている動的ファセットフィールド、動的ファセットフィールド数の現在の数です。 0未満の整数値は0として扱われます。 dynamic-facet-field-countの上に指定した整数値 <span class="codeph"> は、 </span> dynamic-facet-field-countで大文字になり <span class="codeph"></span>ます。 整数以外の値は無視されます。これらはデフォルト値として扱われます。 </p> <p>特定のスライスの検索には、このスライスのDynamic-Facet-Field-Count <span class="codeph"> 値の </span> 最大許容sp_sfvl_df_count <span class="codeph"></span> 値が上限となります。 スライス結果をマージする場合、 <span class="codeph"> sp_sfvl_df_countの有効最大値 </span> は、すべてのスライスに対して実際に使用する <span class="codeph"> sp_sfvl_df_count </span> の最大値です。 </p> <p>動的ファセットの <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td>
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span></span>&gt;|... </p> </td> 
   <td colname="col4"> <p> この検索の考慮対象から除外する特定の動的ファセットフィールドのリストを指定します。 </p> <p>デフォルトでは、すべての動的ファセットフィールドが考慮されます。 </p> <p>動的ファセットの <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span></span>&gt;|... </p> </td> 
   <td colname="col4"> <p> 検索結果に含める特定の動的ファセットフィールドのリストを指定します。 </p> <p> <p>注意： sp_sfvl_df_count <span class="codeph"></span> パラメータは、返す動的ファセットフィールドの総数を、sp_sfvl_df_includeで指定されたものも含めて指定 <span class="codeph"></span>します。 つまり、 <span class="codeph"> sp_sfvl_df_includeを使用すると、返された動的ファセットフィールドの合計数が </span> sp_sfvl_df_countを超えることを許可され <span class="codeph"></span>ません。 </p> </p> <p>動的ファセットの <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 設定を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>クエリと共に <span class="codeph"> sp_staged=1が送信さ </span> れた場合、実行されるクエリはステージ検索です。 </p> <p>ステージ検索では、インデックスやテンプレートを含む、現在ステージングされているすべてのコンポーネントが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_開始_日、sp_開始_月、sp_開始_年 </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_開始_日=数値 </span> </p> <p> <span class="codeph"> sp_開始_月=数値 </span> </p> <p> <span class="codeph"> sp_開始_年=数値 </span> </p> </td> 
   <td colname="col4"> <p>この3項目の値によって検索の開始日が指定され、セットとして指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_suggest_q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_suggest_q= number </span> </p> </td> 
   <td colname="col4"> <p>sp_suggest_q <span class="codeph"> パラメーターは、Suggestサービスで使用する </span> sp_q[_#] <span class="codeph"></span> パラメーターを決定します。 </p> <p>sp_suggest_qのデフォルト値 <span class="codeph"> は0です。つまり、検索エンジンはsp_qの値を使用して </span> 提案 <span class="codeph"></span> を決定します。 </p> <p>sp_suggest_q=1に設定して、 <span class="codeph"> sp_q_1の値を使用し </span> て提案を決定するなど <span class="codeph"></span> を行います。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t=文字列 </span> </p> </td> 
   <td colname="col4"> <p>使用するトランスポートテンプレートを指定します。 </p> <p>このパラメーターは、検索アカウントの各領域に対して異なる検索トランスポートテンプレートを使用して、Webサイト全体での主要な検索結果の外観を制御する場合に役立ちます。 </p> <p>デフォルトのトランスポートテンプレートは「search」です。 </p> <p>詳しくは、Webサイト用の複数のトランスポートテンプレートの <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> 管理を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0または1 </span> </p> </td> 
   <td colname="col4"> <p>sp_stage=1と設定すると、シミュレーターでコア検索トレース機能 <span class="codeph"></span>が有効になります。 </p> <p>シミュレーター <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> <p> <p>注意： このパラメーターを指定しない場合、コア検索はトレース情報を収集せず、関連するコア検索テンプレートタグは出力されません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w、sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>この特定のクエリで、サウンドに類似したマッチングを有効または無効にすることを指定します。 </p> <p>'Exact'のsp_w_controlは無視されます。 サウンドに似た一致は無効です。 </p><p>'Alike'のsp_w_controlは無視されます。 サウンドに似た一致が有効です</p><p>[その他]のsp_w_controlは1です。 サウンドに似た一致は無効です。 </p><p>[その他]に対するsp_w_controlは、その他の要素です。 サウンドに似た一致は有効です。 </p>sp_w_control <span class="codeph"></span> パラメータを使用すると、サウンドに似た一致をエンドユーザーが制御するための、否定的または肯定的な語のチェックボックスを作成できます。 </p> <p>sp_w_control=0 <span class="codeph"> を使用する </span> と、次の例のように、 <span class="codeph"> sp_w </span> パラメーターを設定するために、否定的な語句のチェックボックスが使用されます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_control=1 <span class="codeph"> を使用 </span> する場合、次のように、肯定的な語のチェックボックスが使用されて <span class="codeph"> sp_w </span> パラメータが設定されます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_controlパラメーターと <span class="codeph"> sp_wパラメーターの使用例については、詳細検索フォームの例を参照し </span><span class="codeph"></span> てください。 </p> <p>詳しくは、「 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> アドバンス検索フォームの例」を参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x=フィールド </span> </p> </td> 
   <td colname="col4"> <p>クエリ文字列を検索するフィールドを指定します。 anyは、すべてのフィールドを検索することを意味します。 titleは、タイトルフィールドのみを検索することを意味します。 descは、ドキュメントの説明フィールドのみを検索することを意味します。 キーは、ドキュメントのキーワードのみを検索することを意味します。 bodyは、本文のみを検索することを意味します。 altは、代替テキストのみを検索することを意味します。 urlは、URL値のみを検索することを意味します。 ターゲットとは、ターゲットのキーワードのみを検索することを意味します。 この場合、対応する <span class="codeph"> sp_qパラメータ内の「text:」、「desc:」、「keys:」、「body:」、「alt:」、「url:」および「ターゲット:」の各フィールドプリフィックスのユーザー指定は無視され </span> ます。 sp_xが存在しない場合、または <span class="codeph"></span> sp_xが空の文字列または任意に設定されている場合は、標準ユーザーフィールドのプリフィックスが許可されます。 フィールドのプリフィックスについて詳しくは、検索のヒントの説明を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">検索について</a>を参照してください。 </p> <p>sp_xパラメータの使用例については、サンプルのアドバンス検索フォームの説明を参照して <span class="codeph"> く </span> ださい。 </p> <p>詳しくは、「 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> アドバンス検索フォームの例」を参照してくだ </a>さい。 </p> <p>Search By Defaultに設定されたすべてのフィールドをOptions &gt; <span class="uicontrol"> Metadata &gt; </span> Defaultで検索するクエリを作成できます。その場合は、Options &gt; <span class="uicontrol"> Metadata setting sp_x </span> any potions <span class="uicontrol"></span><span class="uicontrol"></span><span class="codeph"></span>= any portionsの下に作成できます。 pre-definedフィールドとuser-definedフィールドの両方を、 <span class="codeph"> sp_x </span> パラメータの値として使用できます。 </p> <p>また、 <span class="codeph"> sp_xパラメータを複数回設定することで、1つのクエリに複数のフィールドを割り当てることもで </span> きます。 次のテンプレート行を使用して、「Great Books」の「title」と「author」の両方のフィールドをクエリできます。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#=フィールド名 </span> </p> </td> 
   <td colname="col4"> <p>このパラメーターは、対応する <span class="codeph"> sp_q_# </span> クエリで検索するフィールドを指定します。 <span class="codeph"> #は、1 ～ 16の間の数値に置き換えられます( <span class="codeph"> sp_x_8など </span></span><span class="codeph"></span>)。 field-nameは、事前定義またはユーザー定義のフィールドです。 </p> <p>特定の番号付きクエリに対して <span class="codeph"> sp_x_#パラメータを指定しない場合、Setting Metadata &gt; </span> Defaultの下に設定されたSearch By Defaultとして定義され <span class="uicontrol"> たすべてのフィールドが、そのクエリによって検索され </span><span class="uicontrol"></span><span class="uicontrol"></span><span class="uicontrol"></span> ます。 </p> <p>例えば、次のフォームを送信すると、「great」という単語を含むすべてのドキュメントが返されます。この単語には「author」フィールドに「Fitzgerald」という単語も含まれます。 </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>1回の検索リクエストで同じ <span class="codeph"> sp_xまたはsp_x_#クエリの複数のインスタンスを指定することで、複数のフィールド名を特定のクエリまたは番号付きパラメータに関連付けるこ </span> とが <span class="codeph"></span> できます。 </p> <p>例えば、「body」と「keys」フィールドの両方で「flower」という単語を検索するには、次の情報を含む検索フォームを作成します。 </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

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

