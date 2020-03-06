---
description: 正規表現の構成の構文と規則に関するリフレッシャ。
seo-description: 正規表現の構成の構文と規則に関するリフレッシャ。
seo-title: 正規表現
solution: Target
title: 正規表現
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 正規表現{#regular-expressions}

正規表現の構成の構文と規則に関するリフレッシャ。

ステージングされ [たWebサイトの増分インデックスの設定も参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**正規表現の構文**

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
   <td colname="col3"> <p> 代替の境界を設定するため、または$Nを使用してRewriteRuleのRHSでN番目のグループが使用される参照を作成するための、テキストのグループ化) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>アンカー</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> ラインアンカーの始点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> 行アンカーの終わり。 </p> </td> 
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

**正規表現に関するルール**

* 通常の文字（以下に示す特殊文字の1つではない）は、それ自体に一致する1文字の正規表現です。
* バックスラッシュ(¥)の後に任意の特殊文字が続く場合は、その特殊文字自体に一致する1文字の正規表現を指定します。 特殊文字には、次のものがあります。

   * `.` （ピリオド）、 `*` （アスタリスク）、 `?` （疑問符）、 `+` （プラス記号）、 `[` （左角括弧）、 `|` （縦線）および `\` （バックスラッシュ）は、角括弧内に表示される場合を除き、常に特殊文字です。
   * `^` （キャレットまたはサーカムフレックス）は、正規表現の先頭、または角括弧の組み合わせの直後の特殊な文字です。
   * `$` （ドル記号）は、正規表現の末尾で特別な値です。
   * `.` （ピリオド）は、任意の文字に一致する1文字の正規表現です。新しい行以外の補助コードセット文字も含まれます。
   * （左角括弧と右角括弧で囲まれた）空でない文字列は、その文字列内の1文字（補助コードセット文字を含む）と一致する1文字の正規表現です。 `[ ]`

      ただし、文字列の最初の文字が `^` （サーカムフレックス）の場合、1文字の正規表現は、補助コードセット文字を含む任意の文字と一致します。ただし、改行文字と文字列内の残りの文字は例外です。

      は、文 `^` 字列内で最初に出現する場合にのみ、この特別な意味を持ちます。 補助コードセ `-` ット文字を含む連続する文字の範囲を示すには、マイナス記号を使用します。 例えば、 [0-9は] 0123456789と同じ [です]。

      範囲を指定する文字は、同じコードセットの文字である必要があります。 異なるコードセットの文字を使用する場合、範囲を指定する文字の1つが一致します。 文字列 `-` 内で最初（最初の文字の後）または最後（存在する場合） `^`に発生する場合、はこの特別な意味を失います。 文字 `]` 列（右角括弧）内の最初の文字の場合、その文字列が最初の文字の後（存在する場合）で終わ `^`ることはありません。 例えば、 []a-f]は、a `]` （右角括弧）またはASCII文字a ～ fのいずれかに一致します。 上記の特殊文字としてリストされた4文字は、このような文字列内の文字を表します。

**1文字の正規表現から正規表現を作成するルール**

次のルールを使用して、1文字の正規表現から正規表現を作成できます。

* 1文字の正規表現は、1文字の正規表現で一致するものに一致する正規表現です。
* 1文字の正規表現の後に（アスタリスク）が続く正規表現は、1文字の正規表現の0回以上の繰り返しに一致する正規表現です。これは、補助コードセット文字の場合があります。 `*` 選択肢がある場合は、一致を許可する最も左に長い文字列が選択されます。
* 1文字の正規表現の後に（疑問符）が続く正規表現は、0回または1回の1文字の正規表現に一致する正規表現で、補助コードセット文字の場合もあります。 `?` 選択肢がある場合は、一致を許可する最も左に長い文字列が選択されます。
* 1文字の正規表現の後にプラス記号（+記号）が続く正規表現は、1文字の正規表現の1つ以上のオカレンスと一致する正規表現で、補助コードセット文字の場合もあります。 `+` 選択肢がある場合は、一致を許可する最も左に長い文字列が選択されます。
* 1文字の正規表現の後に、、、ま `{m}`たは `{m,}`が続く正規 `{m,n}` 表現は、1文字の正規表現の出現範囲に一致する正規表現です。 mとnの値は、256未満の負でない整数である必要があります。完全 `{m}` にm個の繰り返しに一致します。少なく `{m,}` ともm個の繰り返しに一致します。m ～ nの `{m,n}` 任意の数のオカレンスと一致します。 選択肢が存在する場合は常に、可能な限り多くの値と一致します。
* 正規表現を連結したものは、正規表現の各構成要素に一致する文字列を連結したものと一致します。
* 文字シーケンス（および）で囲まれた正規表現は、装飾のない正規表現が一致するものに一致する正規表現です。
* 正規表現の後に(垂直パイプ `|` )を続けて正規表現とは、最初の正規表現（垂直パイプの前）または2番目の正規表現（垂直パイプの後）に一致する正規表現です。

また、線の最初のセグメント、最後のセグメント、またはその両方に一致するように正規表現を制約することもできます。

* 正規 `^` 表現の先頭に（サーカムフレックス）がある場合、その正規表現が線の最初のセグメントに一致するように制限されます。
* 正規 `$` 表現全体の末尾に（ドル記号）を付けると、その正規表現が行の最後のセグメントに一致するように制限されます。
* 構造^regular expression$は、行全体に一致するように正規表現を制限します。

複雑な括弧で囲まれた正規表現の代わりに使用できる、定義済みの文字クラス名がいくつかあります。 例えば、1文字の正規表現 [0 ～ 9や、文字クラスの1文字の正規表現] [[:digit:]]で表すことができます。

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
   <td colname="col2"> <p> 制御コード印刷しない文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:digit:]] </p> </td> 
   <td colname="col2"> <p>数字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:graph:]] </p> </td> 
   <td colname="col2"> <p> スペースを除く任意の印刷文字。 </p> </td> 
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

2つの特殊文字クラス名は、単語の先頭と末尾のヌルスペースに一致します。 つまり、実際の文字とは一致しません。 単語は、英字、数字またはアンダースコア(_)の任意のシーケンスと見なされます。

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
   <td colname="col2"> <p> 単語の先頭 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>語末 </p> </td> 
  </tr> 
 </tbody> 
</table>

