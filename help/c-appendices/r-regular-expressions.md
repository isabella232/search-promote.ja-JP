---
description: 正規式を作成する構文とルールに関するリフレッシャー。
seo-description: 正規式を作成する構文とルールに関するリフレッシャー。
seo-title: 正規表現
solution: Target
title: 正規表現
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 1%

---


# 正規表現{#regular-expressions}

正規式を作成する構文とルールに関するリフレッシャー。

ステージングされたWebサイトの増分インデックスの [設定も参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**正規式の構文**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>テキスト</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>1 文字 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [文字] </p> </td> 
   <td colname="col3"> <p> 文字クラス：1文字 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^chars] </p> </td> 
   <td colname="col3"> <p>文字クラス：文字なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> 代替：text1またはtext2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>量指定子</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 前のテキストの0または1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 前のテキストの0またはN(N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>前のテキストの1またはN(N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>グループ</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (text) </p> </td> 
   <td colname="col3"> <p> 代替の境界を設定するため、またはN番目のグループがRewriteRuleのRHSで使用される逆参照を作成するための、テキストのグループ化($N) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>アンカー</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> ラインアンカーの開始。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> 行アンカーの終了。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>エスケープ</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>特定の文字をエスケープします。 例えば、「。[]()など。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**正規式に関するルール**

* 通常の式は、以下に示す特殊文字の1つではなく、それ自体に一致する1文字の正規文字です。
* バックスラッシュ(¥)の後に任意の特殊文字が続く場合は、その特殊文字自体に一致する1文字の正規式を指定します。 特殊文字には次のものがあります。

   * `.` （ピリオド）、 `*` （アスタリスク）、 `?` （疑問符）、 `+` （プラス記号）、 `[` （左角括弧）、 `|``\` （縦線）、（バックスラッシュ）は、角括弧内に表示される場合を除き、常に特殊文字です。
   * `^` （キャレットまたはサーカムフレックス）は、正規式の先頭、または角括弧の組み合わせの左にすぐ後にある場合に特殊です。
   * `$` （ドル記号）は、正規式の終わりに特別な値です。
   * `.` （ピリオド）は、改行以外の補助コードセット文字を含め、任意の文字と一致する1文字の正規式です。
   * （左右の角括弧で囲まれた）空でない文字列 `[ ]` は、その文字列内の1文字（補助コードセット文字を含む）と一致する1文字の正規式です。

      ただし、文字列の最初の文字が `^` （サーカムフレックス）の場合、1文字の正規式は、補助コードセット文字を含む任意の文字と一致します。ただし、文字列内の改行文字と残りの文字は例外です。

      は、文字列内で最初に出現する場合にのみ、この特別な意味を持ちます。 `^` 補助コードセット文字 `-` を含め、連続する文字の範囲を示すのにマイナス記号を使用できます。 例えば、 [0-9] は0123456789と同じ [です]。

      範囲を指定する文字は、同じコードセットに含まれている必要があります。 異なるコードセットの文字が使用されている場合、その範囲を指定する文字の1つが一致します。 文字列内で最初（最初の文字の後、最初の文字列が存在する場合）または最後に出現する場合、 `-``^`はこの特別な意味を失います。 文字列 `]` （右角括弧）は、文字列内の最初の文字の場合、その文字列の最初の文字の後（最初の文字がある場合）に終了し `^`ません。 例えば、 `[]a-f]` は、a `]` （右角括弧）またはASCII文字a ～ fのいずれかと一致します。 上記の特殊文字として一覧に示した4文字は、このような文字列の中でその文字自体を表します。

**1文字の正規式から正規式を作成する際のルール**

次のルールを使用して、1文字の正規式から正規式を作成できます。

* 1文字の正規式とは、1文字の正規式が一致する任意の正規式に一致する正規です。
* 1文字の正規式の後に `*` （アスタリスク）が続く正規式は、1文字の正規式の0回以上の繰り返しと一致する正規です。これは、補助コードセット文字の場合があります。 選択肢がある場合、一致を許可する左端の最も長い文字列が選択されます。
* 1文字の正規式の後に `?` （疑問符）が続く正規式は、0回または1文字の正規式の1回の繰り返しと一致する正規です。これは、補助コードセット文字の場合があります。 選択肢がある場合、一致を許可する左端の最も長い文字列が選択されます。
* 1文字の正規式の後にプラス記号が続く正規式 `+` は、1文字の正規式の1回以上の繰り返しと一致する正規です。これは、補助コードセット文字の場合があります。 選択肢がある場合、一致を許可する左端の最も長い文字列が選択されます。
* 1文字の正規式の後に、 `{m}`、、 `{m,}`またはが続く正規式 `{m,n}` は、1文字の正規式の出現範囲と一致します。 mとnの値は、256以下の負の整数でなければなりません。 `{m}` は、ちょうどm回と一致します。 `{m,}` は最低m回の繰り返しと一致します。 `{m,n}` はm ～ nの任意の数の値と一致します。 選択肢が存在する場合は常に、正規式は可能な限り多く一致します。
* 正規式を連結するのは、正規式の各コンポーネントに一致する文字列を連結する正規式です。
* 文字シーケンス（および）の間に囲まれた正規式は、無装飾の正規式が一致するものに一致する正規式です。
* 正規式の後に `|` （垂直パイプ）が続く正規式は、最初の正規式（垂直パイプの前）または2番目の正規式（垂直パイプの後）に一致する正規式です。

また、線の最初のセグメント、最後のセグメント、またはその両方に一致するように正規式を制限することもできます。

* 正規式の最初にある `^` （サーカムフレックス）は、その正規式を、線の最初のセグメントに一致するように制約します。
* 正規式全体の最後に `$` （ドル記号）があると、その正規式が線の最後のセグメントに一致するように制限されます。
* 構築^regular式$により、正規式が線全体に一致するように制限されます。

複雑でかっこで囲まれた正規式の代わりに使用できる、定義済みの文字クラス名がいくつかあります。 例えば、1文字の正規式 [0 ～ 9で表される数字や、1文字の正規式（文字クラス）] [[:digit:]]で表される数字を使用できます。

定義済みの文字クラスとその意味は次のとおりです。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>文字クラス </p> </th> 
   <th colname="col2" class="entry"> <p>意味 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> 英字または数字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>英字文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:空白:]] </p> </td> 
   <td colname="col2"> <p>スペースまたはタブ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> 制御コード；印刷しない文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:digit:]] </p> </td> 
   <td colname="col2"> <p>数字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:graph:]] </p> </td> 
   <td colname="col2"> <p> スペース以外の任意の印刷文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lower:]] </p> </td> 
   <td colname="col2"> <p>小文字の英字文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:print:]] </p> </td> 
   <td colname="col2"> <p> スペースを含む任意の印刷文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> 句読点 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:スペース:]] </p> </td> 
   <td colname="col2"> <p> スペース、タブ、行末などの空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:upper:]] </p> </td> 
   <td colname="col2"> <p> 大文字の英字文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xdigit:]] </p> </td> 
   <td colname="col2"> <p> 大文字または小文字の16進数値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

2つの特殊文字クラス名は、開始のヌルスペースと単語の末尾に一致します。 つまり、実際の文字とは一致しません。 1つの単語は、英字、数字またはアンダースコア(_)の任意のシーケンスと見なされます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>文字クラス </p> </th> 
   <th colname="col2" class="entry"> <p>意味 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> 単語の開始 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>語末 </p> </td> 
  </tr> 
 </tbody> 
</table>

