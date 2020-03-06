---
description: ルールの書き換えメニューを使用して、クロールと検索URLとタイトルのルールを設定します。
seo-description: ルールの書き換えメニューを使用して、クロールと検索URLとタイトルのルールを設定します。
seo-title: 書き換えルールメニューについて
solution: Target
subtopic: Rewrite Rules
title: 書き換えルールメニューについて
topic: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# 書き換えルールメニューについて {#about-the-rewrite-rules-menu}

ルールの書き換えメニューを使用して、クロールと検索URLとタイトルのルールを設定します。

## クロールリストのストアURLルールについて {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

クロールURLルールは、Webコンテンツ内で検出されたURLを書き換える方法を指定します。 ルールと条件の数に制限はなく、検出されたURLの任意の部分を操作できます。

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

クロールルールは、Webサイトを訪問する各顧客に対して一意のセッション識別子など、URLの動的な部分を書き換える場合に最も役立ちます。 書き換えルールを使用して、クエリパラメーターなど、URLの一部を検索ロボットから非表示にすることもできます。 デフォルトでは、ルールは指定されず、URLの書き換えも行われません。

Webサイトのクロール時に、埋め込みコンテンツのURLは、クロールする追加のWebページの一時リストに保存されます。 このリストにURLが追加される前に、ストアの書き換えルールが適用されます。 通常、ストアの書き換えルールは、URLからセッションIDを削除したり、特定のセッションIDをクロール用に強制するために使用されます。 検索ロボットがリストからURLを取得すると、Retrieve Rewriteルールを使用して、そのURLの一部を再度操作します。 通常、取得ルールは、時間に依存するデータをURLに挿入するために使用されます。 これは、実際にWebサイトからページを取得するために使用される最終的なURLです。

「クロール [リストのURL取得の規則」を参照してくださ](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)い。

通常は、URLルールの保存のみを使用します。 「URLの取得ルール」は、URLにセッションIDなどの動的データが含まれ、その動的データが有効なままになるように時間の経過とともに変化する場合にのみ必要です。 この場合、「URLルールの保存」を使用して、検出されたURLからデータの最新の状態を取得します。 次に、検索ロボットがページを取得しようとするときに、「URLの取得ルール」を使用して各URLにそのデータを追加します。

各ルールは、書き換え規則(RewriteRule)ディレクティブと、1つ以上のオプションの書き換え条件(RewriteCond)を使用して指定されます。 ルールの順序は重要です。 ルールセットはルールごとにループされます。 ルールが一致すると、対応する書き換え条件をループ処理します。 クロールURLルールは、次の方法で指定します。

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

埋め込みURLが見つかると、検索ロボットはURLを各クロールルールのパターンと一致させようとします。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構築された新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示される順に処理されます。 書き換えエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)との照合を試みます。 2つの一致が見つかった場合、次の条件が処理され、それ以上の条件が使用できなくなります。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて {#section_162122340BB34F12BB9A36DC9349092B}

RewriteRuleディレクティブの形式は次のとおりです。

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` は、現在のURLに適用されるPOSIX正規表現です。 「現在のURL」は、以前のルールでURLが既に一致し、変更されている可能性があるので、元のリクエストされたURLと異なる場合があります。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「not」文字(&#39;!&#39;)は使用できません。をクリックします。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のURLがこのパターンと一致しない場合にのみ真となります。 「not」文字は、負のパターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。

>[!NOTE]
>
>パターン内で「not」文字とグループ化されたワイルドカードの両方を使用することはできません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して、パターン内にバックリファレンスを作成できます。このバックリファレンスは、SubstitutionおよびCondPatternで参照できます。

**置換** URLは置換文字列に置換され、次の文字列が含まれます。

テキスト：変更されずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RewriteCond Backreferences** これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数：これらは%{NAME_OF_VARIABLE}という形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設 `*[E]*` 定について詳しくは、フラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコード *します*。
* a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、および&#39;_&#39;は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx個のURLエンコードされた等価な文字に変換されます。
* unescapeは、「+」をスペースに戻し、すべての%xx URLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次の特殊な置換文字列があります。つま `'-'` り「代替なし」です。 この文 `'-'` 字列はC（チェーン）フラグと共に使用され、置換が発生する前にURLを複数のパターンに一致させることができます。

**フラグ**

（オプション）フラグは角括弧で囲みま `[]`す。 複数のフラグはコンマで区切られます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>最後のルール。 </p> <p>書き換え処理を停止し、追加の書き換え規則を適用しません。 このフラグを使用して、現在のURLが処理されないようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のURLではなく）最後の書き換えルールのURLを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールにチェーン（次のルールにチェーンすることもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行されます。 ルールが一致しない場合は、後続のすべてのチェーンルールがスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> パターンが現在のURLと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の間に違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは書き換えエンジンに対して、ルールセット内の次のnumルールをスキップさせます。 このフラグを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nとなり、Nはelse節内の規則の数を表します。 </p> <p> <p>注意： このフラグは'chain|C'フラグとは異なります。) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p>値VALに設定された環境変数「VAR」を作成します。VALには、正規表現のバックリファレンス$Nと%Nを含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照解除できます。 </p> <p>このフラグを使用して、URLからの情報を削除し、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Store Rewrite RulesとRetrieve Rewrite Rulesは変数値を共有します。 この動作のため、埋め込みURLを検出して保存する際に、変数を時間に依存するsessionid値に設定できます。 次のURLが一時ストレージリストから取得されると、そのページが取得される前に、最新のsessionid値がそのURLに追加されます。

**関数を持つRewriteRuleの例**

文字列の処理方法と処理方法が異なる、大文字と小文字が区別されるサーバーがあ `"www.mydomain.com"` るとし `"www.MyDomain.com"` ます。 サーバーが正しく機能するために、ドメインが常にドメインであることを確認します。これを行うには、次のルールを使用します。これは、ドキュメ `"www.mydomain.com"``"www.MyDomain.com."` ントに参照するリンクが含まれている場合でも可能です。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

この書き換えルールでは、関数を使 `tolower` 用してURLのドメイン部分を書き換え、次のように常に小文字になるようにします。

1. パターンに `(^https://([^/]*)(.*)$)` は、URL内の最 `([^/]*)` 初との間のすべての文字と一致 `https://` する後方参照が含 `/` まれています。 このパターンには、URL内の残りのすべての文字 `(.*)` と一致する2番目の後方参照も含まれます。

1. 置換は、 `(https://${tolower:$1}$2)` 検索エンジンに対して、最初の後方参照の関数を使用してURL `tolower` を書き換え、残りのURL `(https:// ${tolower:$1}$2)` はそのまま残りのままにするよう指示しま `(https://${tolower:$1} $2)`す。

これにより、フォームのURLがに書き `https://www.MyDomain.com/INTRO/index.Html` 換えられま `https://www.mydomain.com/INTRO/index.Html`す。

## RewriteCondディレクティブについて {#section_CD5A19B2D3204F73B645411931FC34A1}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleより前にある場合、ルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。 書き換え条件は、次の形式をとります。

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` は、次の構成要素を含む文字列です。

テキスト：変更されずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例： `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`

* **RewriteCond Backreferences** これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%N (0&lt;= N &lt;= 9)の形式をとります。

変数：これらは%{NAME_OF_VARIABLE}という形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 変数の設定について詳し *`[E]`* くは、RewriteRuleフラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコードします。 a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9、「*」、「 — 」、「。」、「/」、「@」および「_」は変更されず、スペースは「+」に変換され、その他のすべての文字は `%xx` URLエンコードされた等価な文字に変換されます。
* unescapeは「+」を空白に戻し、すべての `%xx` URLが文字を1文字にエンコードし直します。

**CondPatternは** 、標準の拡張正規表現で、いくつか追加されています。 パターン文字列の先頭に文字（感嘆符）を `!` 付けて、一致しないパターンを指定できます。 実際の正規表現文字列の代わりに、次の特別なバリアントのいずれかを使用できます。

>[!NOTE]
>
>また、これらのすべてのテストの前に感嘆符(&#39;!&#39;)を付けることもできます彼らの意味を打ち消す

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的には少ない。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternより小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に大きい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternより大きい場合は、Trueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternと等しい場合、つまり、2つの文字列が完全に等しい（文字単位で）場合はtrueです。 CondPatternが""（2つの引用符）の場合、TestStringと空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ**（オプション）フラグは角括弧で囲みま `[]`す。 複数のフラグはコンマで区切られます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p>このフラグは、テストで大文字と小文字を区別しないようにします。つまり、拡張されたTestStringとCondPatternの両方で、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

一部のWebページでは、訪問者が初めてサイトに到達したときに「sessionid」CGI変数を割り当てます。 この変数は、訪問者を識別するために使用され、訪問者がサイトを閲覧する際に、変数が渡されます。 検索ロボットはサイトの訪問者のように見えるので、「sessionid」の番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値の割り当てを試みても、この単一の「sessionid」値を維持します。 これを確実に行うには、2つの書き換えルールが必要です。

最初のルールは、sessionid変数を識別して保存するために使用されます。

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRuleはEフラグを使用して、 `([E=sessionid:$1])` sessionid CGIパラメータの現在の値を変数に割り当てま `sessionid`す。 は、 `$1` RewriteRuleのPattern内の最初の括弧の間に含まれる最初の後方参照を参照します `([^&#]+)`。

正規表現は、URL `^&#]+` の単語と次の文字の間の部分と `sessionid` 一致させます `**&**or**#**` 。 このRewriteRuleは、sessionid変数の初期値を作成する目的でのみ使用されるので、書き換えは行われません。 ルールの「置換」フィールドは、書き換えの必要がない `-` ことを示すように設定されています。

RewriteCondは変数 `sessionid` ()を調べ `%{sessionid}`ます。 1文字も含まない場合(!.+)の場合、RewriteRuleが一致します。

このルールを使用して、URLを読み取り、 `https://www.domain.com/home/?sessionid=1234&function=start` 変数に値を割り `1234` 当てます `sessionid`。

2つ目のルールは、次のRewriteRuleパターンに一致するすべてのURLを書き換えるために使用されます。

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule Patternには2つのバックリファレンスが含まれています。 `(.+)` と `(.*)`最初の後方参照は、前のすべての文字と一致しま `sessionid`す。 2番目の後方参照は、終了文字またはの後のすべての文字と一致 `&` しま `#`す。

置換パターンは、最初のバックリファレンスを使用してURLを書き換え、次に文字列「sessionid=」を使用し、次に最初のルールで定義されたセッションID変数の値を続け、次に2番目のバックリファレ `%{sessionid}`ンスを使用して書き換えます。 `($1sessionid=%{sessionid} $2)`

このRewriteRuleにRewriteCondが含まれていないことに注意してください。 したがって、RewriteRule *Patternに一致するすべてのURLが書き換えられ*&#x200B;ます。 したがって、sessionid変数( `%{sessionid}`)の値がで `1234``https://www.domain.com/products/?sessionid=5678&function=buy` ある場合、フォームのURLは、 `https://www.domain.com/products/?sessionid=1234&function=buy`

## 通知 {#section_B17088EF38244496BC1DDD4ECF75EB5B}

書き換えエンジンソフトウェアは、もともとApache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようにしました。

## クロールリストのストアURLルールの追加 {#task_22DD40DF95584B12BE8E6ECFBF579BCD}

クロールリストのストアURLルールを追加して、Webコンテンツ内で検出されたURLの書き換え方法を指定できます。 ルールと条件の数に制限はなく、検出されたURLの任意の部分を操作できます。

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**クロールリストのストアURLルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Rewrite Rules]** ます **[!UICONTROL Crawl List Store URL Rules]**。
1. フィールド [!DNL Crawl List Store URL Rules] に、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。
1. （オプション）ページ [!DNL Crawl List Store URL Rules] のフィールドに、 [!DNL Test Crawl List Store URL Rules] クロールルールをテストするテストURLを入力し、「テスト」をクリック **します**。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Crawl List Store URL Rules] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## クロールリストの取得URLルールについて {#concept_EC8E2E48B99A458D8567B526C9827CBA}

「クロールURLルール」では、Webコンテンツ内で検出されたURLの書き換え方法を指定します。 ルールと条件の数に制限はなく、検出されたURLの任意の部分を操作できます。

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

ルールの効果が顧客に表示される前に、サイトインデックスを必ず再構築してください。

クロールルールは、Webサイトを訪問する各顧客に対して一意のセッション識別子など、URLの動的な部分を書き換える場合に最も役立ちます。 書き換えルールを使用して、クエリパラメーターなど、URLの一部を検索ロボットから非表示にすることもできます。 デフォルトでは、ルールは指定されず、URLの書き換えも行われません。

Webサイトのクロール時に、埋め込みコンテンツのURLは、クロールする追加のWebページの一時リストに保存されます。 検索ロボットがリストからURLを取得すると、Retrieve Rewrite Rulesを使用して、そのURLの一部が操作されます。 通常、取得ルールは、時間に依存するデータをURLに挿入するために使用されます。 これは、実際にWebサイトからページを取得するために使用される最終的なURLです。

「Retrieve Rewrite Rules」は、URLにセッションIDなどの動的データが含まれ、その動的データが有効なままになるように時間の経過とともに変化する場合にのみ必要です。 この場合、ストア書き換えルールを使用して、検出されたURLからデータの最新の状態を取得します。 次に、検索ロボットがページを取得したときに、「Retrieve Rewrite Rules」を使用して各URLにそのデータを追加します。

各ルールは、書き換え規則(RewriteRule)ディレクティブと、1つ以上のオプションの書き換え条件(RewriteCond)を使用して指定されます。 ルールの順序は重要です。 ルールセットはルールごとにループされます。 ルールが一致すると、対応する書き換え条件をループ処理します。 クロールURLルールは、次の方法で指定します。

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

埋め込みURLが見つかると、検索ロボットはURLを各クロールルールのパターンと一致させようとします。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構築された新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示される順に処理されます。 書き換えエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)との照合を試みます。 2つの一致が見つかった場合、次の条件が処理され、それ以上の条件が使用できなくなります。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて {#section_32B24B29627946398AFBC5F869A610CB}

RewriteRuleディレクティブの形式は次のとおりです。

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` は、現在のURLに適用されるPOSIX正規表現です。 「現在のURL」は、以前のルールでURLが既に一致し、変更されている可能性があるので、元のリクエストされたURLと異なる場合があります。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「not」文字(&#39;!&#39;)は使用できません。をクリックします。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のURLがこのパターンと一致しない場合にのみ真となります。 「not」文字は、負のパターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。

>[!NOTE]
>
>パターン内で「not」文字とグループ化されたワイルドカードの両方を使用することはできません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して、パターン内にバックリファレンスを作成できます。このバックリファレンスは、SubstitutionおよびCondPatternで参照できます。

**置換** URLは置換文字列に置換され、次の文字列が含まれます。

テキスト：変更されずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** RewriteCond Backreferences**これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%Nの形式をとります(0 &lt;= N &lt;= 9)。

変数：これらは%{NAME_OF_VARIABLE}という形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設 *[定について詳しくは]* 、Eフラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコード *します*。
* a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、および&#39;_&#39;は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx個のURLエンコードされた等価な文字に変換されます。
* unescapeは、「+」をスペースに戻し、すべての%xx URLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次の特殊な置換文字列があります。「 — 」は「置換なし」を意味します。 「 — 」文字列はC（チェーン）フラグと共に使用され、置換が発生する前にURLを複数のパターンに一致させることができます。

**フラグ**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>最後のルール。 </p> <p>書き換え処理を停止し、追加の書き換え規則を適用しません。 このフラグを使用して、現在のURLが処理されないようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のURLではなく）最後の書き換えルールのURLを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールにチェーン（次のルールにチェーンすることもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行されます。 ルールが一致しない場合は、後続のすべてのチェーンルールがスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> パターンが現在のURLと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の間に違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは書き換えエンジンに対して、ルールセット内の次のnumルールをスキップさせます。 このフラグを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nとなり、Nはelse節内の規則の数を表します。 </p> <p> <p>注意： このフラグは'chain|C'フラグとは異なります。) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p>値VALに設定された環境変数「VAR」を作成します。VALには、正規表現のバックリファレンス$Nと%Nを含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照解除できます。 </p> <p>このフラグを使用して、URLからの情報を削除し、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Store Rewrite RulesとRetrieve Rewrite Rulesは変数値を共有します。 この動作のため、埋め込みURLを検出して保存する際に、変数を時間に依存するsessionid値に設定できます。 次のURLが一時ストレージリストから取得されると、そのページが取得される前に、最新のsessionid値がそのURLに追加されます。

**関数を持つRewriteRuleの例**

大文字と小文字が区別されるサーバーがあり、「www.mydomain.com」と「www.MyDomain.com」の処理方法が異なるとします。 サーバーが正しく動作するようにするには、「www.MyDomain.com」を参照するリンクが一部のドキュメントに含まれている場合でも、ドメインが常に「www.mydomain.com」であることを確認します。 これを行うには、次のルールを使用します。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

この書き換えルールでは、関数を使 `tolower` 用してURLのドメイン部分を書き換え、次のように常に小文字になるようにします。

1. パターン `(^https://([^/]*)(.*)$)` には、URL内の最初との間のすべての文字に一致する後方参照*** `([^/]*)`が含ま `https://``/` れています。 このパターンには、URL内の残りのすべての文字 `(.*)` と一致する2番目の後方参照も含まれます。
1. 置換は、 `(https://${tolower:$1}$2)` 検索エンジンに対して、最初の後方参照の関数を使用してURL `tolower` を書き換え、残りのURL `(https:// ${tolower:$1}$2)` はそのまま残りのままにするよう指示しま `(https://${tolower:$1} $2)`す。

これにより、フォームのURLがに書き `https://www.MyDomain.com/INTRO/index.Html` 換えられま `https://www.mydomain.com/INTRO/index.Html`す。

## RewriteCondディレクティブについて {#section_ADD642A24B68452CB98294A0BD687EC3}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleより前にある場合、ルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。 書き換え条件は、次の形式をとります。

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` は、次の構成要素を含む文字列です。

テキスト：変更されずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例： `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`

* **RewriteCond Backreferences** これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%N (0&lt;= N &lt;= 9)の形式をとります。

変数：これらは%{NAME_OF_VARIABLE}という形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 変数の設定について詳し *`[E]`* くは、RewriteRuleフラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコードします。 a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9、「*」、「 — 」、「。」、「/」、「@」および「_」は変更されず、スペースは「+」に変換され、その他のすべての文字は%xx URLエンコードされた等価な文字に変換されます。
* unescapeは「+」を空白に戻し、すべての%xx URLが文字を1文字にエンコードし直します。

**CondPatternは** 、標準の拡張正規表現で、いくつか追加されています。 パターン文字列の先頭に「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規表現文字列の代わりに、次の特別なバリアントのいずれかを使用できます。

>[!NOTE]
>
>また、これらのすべてのテストの前に感嘆符(&#39;!&#39;)を付けることもできます彼らの意味を打ち消す

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的には少ない。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternより小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に大きい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternより大きい場合は、Trueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式的にTestStringと比較します。 TestStringが辞書式的にCondPatternと等しい場合、つまり、2つの文字列が完全に等しい（文字単位で）場合はtrueです。 CondPatternが""（2つの引用符）の場合、TestStringと空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ**（オプション）フラグは角括弧で囲みま `[]`す。 複数のフラグはコンマで区切られます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p>このフラグは、テストで大文字と小文字を区別しないようにします。つまり、拡張されたTestStringとCondPatternの両方で、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

一部のWebページでは、訪問者が初めてサイトに到達したときに「sessionid」CGI変数を割り当てます。 この変数は、訪問者を識別するために使用され、訪問者がサイトを閲覧する際に、変数が渡されます。 検索ロボットはサイトの訪問者のように見えるので、「sessionid」の番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値の割り当てを試みても、この単一の「sessionid」値を維持します。 これを確実に行うには、2つの書き換えルールが必要です。

最初のルールは、sessionid変数を識別して保存するために使用されます。

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRuleはEフラグを使用して、 `([E=sessionid:$1])` sessionid CGIパラメータの現在の値を変数に割り当てま `sessionid`す。 は、 `$1` RewriteRuleのPattern内の最初の括弧の間に含まれる最初の後方参照を参照します `([^&#]+)`。

正規表現は、URL `^&#]+` の単語と次の**&amp;or `sessionid`****#**文字の間の部分と一致します。 このRewriteRuleは、sessionid変数の初期値を作成する目的でのみ使用されるので、書き換えは行われません。 ルールの「置換」フィールドは、書き換えの必要がない `-` ことを示すように設定されています。

RewriteCondは変数 `sessionid` ()を調べ `%{sessionid}`ます。 1文字も含まない場合(!.+)の場合、RewriteRuleが一致します。

このルールを使用して、URLを読み取り、 `https://www.domain.com/home/?sessionid=1234&function=start` 変数に値を割り `1234` 当てます `sessionid`。

2つ目のルールは、次のRewriteRuleパターンに一致するすべてのURLを書き換えるために使用されます。

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule Patternには2つのバックリファレンスが含まれています。 `(.+)` と `(.*)`最初の後方参照は、前のすべての文字と一致しま `sessionid`す。 2番目の後方参照は、終了文字またはの後のすべての文字と一致 `&` しま `#`す。

置換パターンは、最初のバックリファレンスを使用してURLを書き換え、次に文字列「sessionid=」を使用し、次に最初のルールで定義されたセッションID変数の値を続け、次に2番目のバックリファレ `%{sessionid}`ンスを使用して書き換えます。 `($1sessionid=%{sessionid} $2)`

このRewriteRuleにRewriteCondが含まれていないことに注意してください。 したがって、RewriteRule *Patternに一致するすべてのURLが書き換えられ*&#x200B;ます。 したがって、sessionid変数( `%{sessionid}`)の値がで `1234``https://www.domain.com/products/?sessionid=5678&function=buy` ある場合、フォームのURLは、 `https://www.domain.com/products/?sessionid=1234&function=buy`

## 通知 {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

書き換えエンジンソフトウェアは、もともとApache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようにしました。

## クロールリスト取得URLルールの追加 {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A}

クロールリスト取得URLルールを追加して、Webコンテンツ内で遭遇したURLを書き換える方法を指定できます。 「Retrieve Rewrite Rules」は、URLにセッションIDなどの動的データが含まれ、その動的データが有効なままになるように時間の経過とともに変化する場合にのみ必要です。

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**クロールリスト取得URLルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Rewrite Rules]** ます **[!UICONTROL Crawl List Retrieve URL Rules]**。
1. フィールド [!DNL Crawl List Retrieve URL Rules] に、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。
1. （オプション）ページ [!DNL Crawl List Retrieve URL Rules] のフィールドに、 [!DNL Test Crawl List Retrieve URL Rules] クロールルールをテストするテストURLを入力し、「テスト」をクリック **します**。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Crawl List Retrieve URL Rules] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## クロールタイトルルールについて {#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

クロールタイトルルールは、Webコンテンツ内で検出されたタイトルが検索インデックスに保存される前に書き換えられる方法を指定します。

<!-- 

c_about_crawl_title_rules.xml

 -->

例えば、書き換えルールを使用して、組織名などのタイトルの一部を削除できます。 Webサイトがクロールされると、検出されたタイトルは一時バッファーに保存されます。 ただし、タイトルがこのバッファに追加される前に、タイトルルールが適用されます。 デフォルトでは、サイト検索/マーチャンダイジングにはクロールタイトルルールがなく、タイトルの変更も行われません。

ルールの効果が顧客に表示される前に、サイトインデックスを再構築します。

履歴機能を使用して、クロールタイトルルールに対して行った変更をすばやく元に戻すことができます。

ルールは、次の2つの主要な要素で構成できます。rewriteruleとオプションのRewriteCond。 ルールと条件の数に制限はありません。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールが一致すると、対応する（オプションの）書き換え条件をループ処理します。 クロールURLルールは、次の方法で指定します。

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

タイトルが見つかると、検索ロボットはタイトルを各クロールルールのパターンと一致させようとします。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構築された新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示される順に処理されます。 書き換えエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)との照合を試みます。 2つの一致が見つかった場合、次の条件が処理され、それ以上の条件が使用できなくなります。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

テキストボックスに「クロールURLルール」を入力し、「変更の保存」をクリックします。 空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。 検索ルールをテストするには、「テスト書き換えルール」テキストボックスにテストURLを入力し、「テスト」をクリックします。

## RewriteRuleディレクティブ {#section_669445C505754E838E14029D6583D9B6}

各RewriteRuleディレクティブは、1つの書き換え規則を定義します。 ルールは、リストに表示される順序で適用されます。 書き換えルールは、次の形式をとります。

```
RewriteRule Pattern Substitution [Flags]
```

**Patternは** 、現在のタイトルに適用されるPOSIX正規表現です。 「現在のタイトル」は、以前のルールが既に一致し、変更されているので、元のタイトルとは異なります。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「not」文字(&#39;!&#39;)を使用できます。をクリックします。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のタイトルがパターンと一致しない場合にのみ真となります。 「not」文字は、負のパターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。 注意：パターン内で「not」文字とグループ化されたワイルドカードの両方を使用することはできません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して後方参照を作成し、SubstitutionとCondPatternで参照できます。

**置換** ：タイトルは置換文字列に置換されます。 この文字列には、次の値を含めることができます。

プレーンテキスト — 変更なしで渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* RewriteRule Backreferences

   対応するRewriteRule Patternのバックリファレンスに一致し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RewriteCondバックリファレンス

   これらの一致後のRewriteCondPattern内のバックリファレンスは、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数これらは%{NAME_OF_VARIABLE}という形式の変数で、NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設 `[E]` 定について詳しくは、フラグを参照してください。

関数${NAME_OF_FUNCTION:key} NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。

>[!NOTE]
>
>次の特殊な置換文字列があります。「 — 」は「置換なし」を意味します。 文字列「 — 」はC（チェーン）フラグと共に使用すると、置換前にタイトルを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧で囲み、複 `[]`数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>最後のルール。 </p> <p> 書き換えプロセスを停止し、追加の書き換え規則を適用しません。 このフラグを使用すると、現在のタイトルが処理されなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> 元のタイトルではなく、最後の書き換えルールのタイトルを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行する。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールにチェーン（次のルールにチェーンすることもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行されます。 ルールが一致しない場合は、後続のすべてのチェーンルールがスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p>パターンが現在のタイトルと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の間に違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは書き換えエンジンに対して、ルールセット内の次のnumルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nとなり、Nはelse節内の規則の数を表します。 (注意：これは'chain|C'フラグとは異なります。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> 値VALに設定された環境変数「VAR」を作成します。VALには、正規表現のバックリファレンス$Nと%Nを含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照できます。 タイトルの情報を削除し、記憶するには、このフラグを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCondディレクティブ（オプション） {#section_D664B71DE3884E0790531804C49A3222}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleより前にある場合、ルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

書き換え条件ディレクティブは次の形式をとります。

```
RewriteCond TestString CondPattern [Flags] 
```

**TestStringは** 、次の構成要素を含む文字列です。

プレーンテキスト — 変更なしで渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* RewriteRuleバックリファレンス対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RewriteCondバックリファレンス最後に一致したRewriteCondCondPattern内のこれらの一致バックリファレンスを参照し、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数これらは%{NAME_OF_VARIABLE}という形式の変数で、NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設 `[E]` 定について詳しくは、フラグを参照してください。

関数${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコードします。
* a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9、「*」、「 — 」、「。」、「/」、「@」および「_」は変更されず、スペースは「+」に変換され、その他のすべての文字は%xx URLエンコードされた等価な文字に変換されます。
* unescapeは、「+」をスペースに戻し、すべての%xx URLエンコードされた文字を1文字に戻します。

**CondPatternは** 、標準の拡張正規表現で、いくつか追加されています。 パターン文字列の先頭に「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規表現文字列の代わりに、次の特別なバリアントの1つを使用できます。

>[!NOTE]
>
>これらのすべてのテストの前に感嘆符(&#39;!&#39;)を付けることができます彼らの意味を打ち消す

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に少ない。 </p> <p>CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書式的に <i></i> CondPatternより小さい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に大きい。 </p> <p>CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書 <i>式的に</i> CondPatternより大きい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> 辞書式的に等しい。 </p> <p>CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 Trueを指定す <i>ると</i> 、TestStringが辞書的に <i>CondPattern</i>と等しく、つまり、2つの文字列が完全に等しい（文字単位で）。 CondPattern <i>が</i> ""（2つの引用符）だけの場合、TestStringと空の文字列が <i>比較されます</i> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧で囲み、複 `[]`数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> テストを無感度にします。 つまり、拡張された <i>TestStringとCondPatternの両方で「A-Z」と「a-z」の間に違いはありま</i><i>せん。</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

標準的なタイトル形式を持つ会社のウェブサイトがあるとします。「My Company」の後にハイフンが続き、次にページ固有の説明（「My Company - Welcome」や「My Company - News」など）が続きます。 タイトルから「マイカンパニー — 」を削除し、サイトのインデックスを作成する際にタイトル全体を大文字に変換する場合。

次の書き換えルールは、関数toupperを使用して、タイトルの説明部分のみを大文字に書き換えます。

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

ルールのパターンには、「 `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` My Company — 」に続くタ `(.*)` イトルコンテンツに一致する後方参照が含まれています。 パターンの一部を括弧( )で囲むと、代替(Substitution)で参照できる後方参照が作成されることに注意してください。 この例では、置換(${toupper:**$1**})は、toupper関数を使用してバックリファレンス(**$1**)を書き換えます。

したがって、「My Company - Welcome」という形式のタイトルは「WELCOME」に書き換えられます。

**通知**

書き換えエンジンソフトウェアは、もともとApache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようにしました。

## クロールタイトルルールの追加 {#task_272BB4C603BA4C9ABDBEEB398798B101}

クロールタイトルルールを追加して、Webコンテンツ内で検出されたタイトルが検索インデックスに保存される前に書き換えられる方法を指定できます。

<!-- 

t_adding_crawl_title_rules.xml

 -->

**クロールタイトルルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Rewrite Rules]** ます **[!UICONTROL Crawl Title Rules]**。
1. フィールド [!DNL Crawl Title Rules] に、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。
1. （オプション）ページ [!DNL Crawl Title Rules] のフィールドに、 [!DNL Test Crawl Title Rules] 検索ルールをテストするテストURLを入力し、「テスト」をクリックし **ます**。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Crawl Title Rules] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索URLルールについて {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

検索URLルールは、Webサイトの検索結果のURLの表示方法を指定します。 ルールは完全なURLに対して実行されます。 セッションID情報が頻繁に保持されるクエリ引数など、URLの任意の部分を操作できます。

<!-- 

c_about_search_url_rules.xml

 -->

通常、検索URLルールは、セッションIDをURLに挿入するために使用されます。 ただし、検索URLルールを使用して、結果と共に表示されるドメイン名を変更することもできます。 デフォルトでは、ルールは指定されず、URLの変更も行われません。

検索URLルールは、次の2つの主要な要素で構成できます。rewriteruleとオプションのRewriteCond。 URLが検索結果の一部として含まれる場合、ルールを使用してURLを操作します。 検索URLのルールと条件の数に制限はありません。 ルールセットはルールごとにループされるので、ルールの順序は重要です。 ルールが一致すると、ソフトウェアは対応する（オプションの）書き換え条件をループ処理します。 クロールURLルールは、次の方法で指定します。

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

URLを処理する際、サイト検索/マーチャンダイジングは、URLを各検索ルールのパターンに一致させようとします。 一致が失敗した場合、書き換えエンジンは即座にルールの処理を停止し、セット内の次のルールを続行します。 パターンが一致する場合、書き換えエンジンは対応するRewriteCond命令を探します。 条件が存在しない場合、URLは新しい値で置き換えられます。 この値は置換文字列から構築され、ルールセット内の次のルールに続きます。 条件が存在する場合、リストに表示される順序は、処理方法です。 書き換えエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)との照合を試みます。 2つの一致が見つかった場合、次の条件が処理され、それ以上の条件が使用できなくなります。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて {#section_A3473B5B90B74DA1970213113A90591E}

書き換えルールは、次の形式をとります。

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**Patternは** 、現在のURLに適用されるPOSIX正規表現になります。 「現在のURL」は、以前のルールが既に一致し変更されている場合があるので、元のURLと異なる場合があります。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「not」文字(&#39;!&#39;)を使用できます。をクリックします。 「not」文字を使用すると、パターンを無効にできます。 つまり、現在のURLがパターンと一致しない場合にのみ当てはまります。 「not」文字は、負のパターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。 パターン内で「NOT」文字とグループ化ワイルドカードの両方を使用することはできません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して後方参照を作成し、SubstitutionとCondPatternで参照できます。

**置換** URLは、次の文字列を含む置換文字列に完全に置換されます。

プレーンテキスト — 変更なしで渡されるテキスト。

[バックリファレンス] [パターン]または[CondPattern]のグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

RewriteRuleバックリファレンス対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RewriteCond Backreferences — 最後に一致したRewriteCondPatternのバックリファレンスに一致し、%N (0 &lt;= N &lt;= 9)の形式をとります。

関数：次に、${NAME_OF_FUNCTION:key}という形式の関数を示します。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコード *します*。
* a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、および&#39;_&#39;は変更されません。スペースは「+」に変換されます。その他のすべての文字は、%xx個のURLエンコードされた等価な文字に変換されます。
* unescapeは、「+」をスペースに戻し、すべての%xx URLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次の特殊な置換文字列があります。「 — 」は「置換なし」を意味します。 「 — 」文字列は、多くの場合、C（チェーン）フラグと組み合わせて使用します。 置換が発生する前に、URLを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧で囲み、複 `[]`数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>最後のルール。 </p> <p> 書き換え処理を停止し、追加の書き換え規則を適用しない。 このフラグを使用して、現在のURLが処理されないようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p> 次のラウンド。 </p> <p>（元のURLではなく）最後の書き換えルールのURLを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行する。 デッドループを作らないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> 次のルールと連結。 </p> <p>このフラグは、現在のルールを次のルールにチェーン化し、次のルールにチェーン化することもできます。 ルールが一致する場合、置換プロセスは通常どおり続行されます。 ルールが一致しない場合は、後続のすべてのチェーンルールがスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p>このフラグは、Patternで大文字と小文字を区別しません。 つまり、パターンが現在のURLと一致する場合、「A-Z」と「a-z」の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは書き換えエンジンに対して、ルールセット内の次のnumルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nとなり、Nはelse節内の規則の数を表します。 (注意：これは'chain|C'フラグとは異なります。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> このフラグは、値VALに設定された環境変数「VAR」を作成します。 VALには、正規表現のバックリファレンス$Nと%Nを含めることができます。これらのバックリファレンスは展開されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照解除できます。 このフラグを使用して、URLからの情報を削除し、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

Store Rewrite RulesとRetrieve Rewrite Rulesは変数値を共有します。 このため、埋め込みURLを検出して保存する際に、変数を時間に依存するsessionid値に設定できます。 次のURLが一時ストレージリストから取得されると、そのページが取得される前に、最新のsessionid値がそのURLに追加されます。

**例**

大文字と小文字が区別されるサーバーがあるとします。 文字列「www.mydomain.com」と「www.MyDomain.com」の処理方法が異なります。 サーバーが正しく動作するようにするには、「www.MyDomain.com」を参照するリンクが一部のドキュメントに含まれている場合でも、ドメインが常に「www.mydomain.com」であることを確認する必要があります。 これを行うには、次のルールを使用します。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

この書き換えルールでは、関数「tolower」を使用してURLのドメイン部分を書き換え、常に小文字になるようにします。

1. パターンに `(^https://([^/]*)(.*)$)` は、URL内の「https://」 **`([^/]*)`** と最初の「/」の間のすべての文字に一致する後方参照が含まれています。 パターンには、2番目の後方参照 **(.*)** 。URL内の残りのすべての文字と一致します。

1. 置換は、 `(https://${tolower:$1}$2)` 最初のバックリファレンスでtolower **関数を使用し、残りのURLを変更せずにURL** を書き換えるよう検索エンジンに指示します `(https://**${tolower:$1**}$2)``(https://${tolower:$1}*$2*)`。

したがって、フォームのURLは、次のように書き `https://www.MyDomain.com/INTRO/index.Html` 換えられます。 `https://www.mydomain.com/INTRO/index.Html`

**RewriteCondディレクティブ** （オプション）

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleより前にある場合、ルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

書き換え条件ディレクティブは次の形式をとります。

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

*TestStringは* 、次の構成要素を含む文字列です。

テキスト：変更されずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* ** RewriteRule Backreferences**対応するRewriteRule Patternのバックリファレンスと一致し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond Backreferences** これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数これらは%{NAME_OF_VARIABLE}という形式の変数で、NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 変数の設定について詳し *`[E]`* くは、RewriteRuleフラグを参照してください。

>[!NOTE]
>
>書き換えルールは、通常、変数を使用します。 現在のURLのすべてのCGIパラメーターは、自動的に変数になります。 例えば、検索URLは自動的に4 `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"` つの変数を提供し、この変数は書き換えルールで参照できます。 この例では、1つの変数を「session」、その値を「1234」、別の変数を「id」、その値を「5678」と呼びます。 (他の2つの変数は、 `sp_a` および `sp_q`です)。必要な変数はすべて、ウェブページ上の検索フォームから非表示フィールドとして渡す必要があります。 この例では、検索を実行するウェブサイトユーザを識別する「session」と「id」の値を渡す必要があります。 検索フォームで非表示のフィールドを渡すには、のようなタグを使用しま `<input type=hidden name="session" value="1234">`す。

関数${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコード *します*。 a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9、「*」、「 — 」、「。」、「/」、「@」および「_」は変更されず、スペースは「+」に変換され、その他のすべての文字は%xx URLエンコードされた等価な文字に変換されます。
* unescapeは「+」を空白に戻し、すべての%xx URLが文字を1文字にエンコードし直します。

**CondPatternは** 、標準の拡張正規表現で、いくつか追加されています。 パターン文字列の先頭に「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規表現文字列の代わりに、次の特別なバリアントの1つを使用できます。

感嘆符(&#39;!&#39;)を使用して、これらのテストのすべてのプレフィックスを付けることができます彼らの意味を打ち消す

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に少ない。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書式的に <i></i> CondPatternより小さい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に大きい。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書 <i>式的に</i> CondPatternより大きい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書 <i>的に</i> CondPatternと等しい場合はTrue <i>です</i>。 つまり、2つの文字列は完全に等しい（文字単位で）。 CondPattern <i>が</i> ""（2つの引用符）だけの場合、TestStringと空の文字列が <i>比較されます</i> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧で囲み、複 `[]`数のフラグはコンマで区切ります。

&#39;nocase|NC&#39; （大文字と小文字の区別なし）:これにより、テストでは大文字と小文字が区別されません。 つまり、拡張された *TestStringとCondPatternの両方で「A-Z」と「a-z」の間に違いはありま* せん **。

&#39;ornext|OR&#39; （または次の条件）:ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせるには、これを使用します。 このフラグがないと、条件/規則を複数回書き込む必要があります。

**例**

一部のWebページでは、顧客が初めてサイトに来訪したときに「sessionid」CGI変数を割り当てます。 この変数は、顧客を識別するために使用され、顧客がサイトを閲覧する際に、変数が渡されます。 検索ロボットはサイトの顧客のように見えるので、「sessionid」番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値の割り当てを試みても、この単一の「sessionid」値を維持します。 これを確実に行うには、次の書き換えルールが必要です。

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

RewriteRule Patternには2つのバックリファレンスが含まれています。(.+) および (.*) となります。最初の後方参照は、&quot;sessionid=&quot;より前のすべての文字と一致します。 2番目のバックリファレンスは、セッションIDの末尾にある「&amp;」または「#」の後のすべての文字と一致します。

Substitutionパターンは、最初のバックリファレンスを使用してURLを書き換え、次に文字列「sessionid=」を使用し、続いてURL内のCGIパラメーターとして渡されたセッションID変数の値を書き換え、次に2番目のバックリファレンスを書き換えます。 `($1sessionid=%{sessionid}$2)`.

RewriteCondは **変数** sessionidを調べます `(%{sessionid})`。 少なくとも1文字(.+)の場合、RewriteRuleが一致します。

したがって、検索クエリが含まれている場合は、検索ロボットがサイトをクロールしてリンクを保存した際に検出した「sessionid」値ではなく、「sessionid」値が「5678」になるように、すべての検索結果URLが書き換えられます。 `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`

**通知**

書き換えエンジンソフトウェアは、もともとApache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようにしました。

## 検索URLルールの追加 {#task_50C77D1B53804AEEB20896F74265BD6F}

検索URLルールを追加して、Webサイトの検索結果のURLの表示方法を指定できます。 ルールは完全なURLに対して実行されます。 セッションID情報が頻繁に保持されるクエリ引数を含め、URLの任意の部分を操作できます。

<!-- 

t_adding_search_url_rules.xml

 -->

**検索URLルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Rewrite Rules]** ます **[!UICONTROL Search URL Rules]**。
1. フィールド [!DNL Search URL Rules] に、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。
1. （オプション）ページ [!DNL Search URL Rules] のフィールドに、 [!DNL Test Search URL Rules] クロールルールをテストするテストURLを入力し、「テスト」をクリック **します**。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Search URL Rules] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 検索タイトルのルールについて {#concept_C72D20F8DFF64EDE809AF4B72797E858}

検索タイトルルールは、Webサイトの検索結果のタイトルの表示方法を指定します。 タイトルの任意の部分を操作できます。

<!-- 

c_about_search_title_rules.xml

 -->

書き換えルールは、例えば組織名など、タイトルの一部を削除する場合に使用します。 デフォルトでは、サイト検索/マーチャンダイジングにはタイトルルールがなく、タイトルの変更も行われません。

タイトルルールは、次の2つの主要な要素で構成できます。rewriteruleおよびオプションのRewriteCond。 指定できるルールと条件の数に制限はありません。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールが一致すると、ソフトウェアは対応する（オプションの）書き換え条件をループ処理します。 検索タイトルルールは次の方法で指定します。

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

タイトルが見つかると、サイト検索/マーチャンダイジングは、それを各クロールルールのパターンと一致させようとします。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、タイトルは置換文字列から構築された新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示される順に処理されます。 書き換えエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)との照合を試みます。 2つの一致が見つかった場合、次の条件が処理され、それ以上の条件が使用できなくなります。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブ {#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

各RewriteRuleディレクティブは、1つの書き換え規則を定義します。 ルールは、リストに表示される順序で適用されます。 書き換えルールは、次の形式をとります。

```
RewriteRule Pattern Substitution [Flags]
```

**Pattern** ：現在のタイトルに適用されるPOSIX正規表現。 「現在のタイトル」は、以前のルールが既に一致し変更されている場合があるので、元のタイトルと異なる場合があります。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

「not」文字(&#39;!&#39;)を使用できます。をクリックします。 「not」文字を使用すると、パターンを無効にできます。 つまり、現在のタイトルがパターンと一致しない場合にのみ真となります。 「not」文字は、負のパターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。 注意：パターン内で「not」文字とグループ化されたワイルドカードの両方を使用することはできません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して後方参照を作成し、SubstitutionとCondPatternで参照できます。

**置換** ：タイトルは、次を含む置換文字列に完全に置換されます。

プレーンテキスト — 変更なしで渡されるテキスト。

**[バックリファレンス** ] [パターン]または[CondPattern]のグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** RewriteCond Backreferences**これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%Nの形式をとります(0 &lt;= N &lt;= 9)。

**変数** ：これらは%{NAME_OF_VARIABLE}という形式の変数で、NAME_OF_VARIABLEは定義済みの変数の名前を表す文字列です。 環境変数の設 [定について詳しくは] 、Eフラグを参照してください。 変数は、検索結果を生成した検索フォームでも定義できます。

**関数** : ${NAME_OF_FUNCTIONの形式の関数です。key} NAME_OF_FUNCTIONは次のとおりです。

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。

次の特殊な置換文字列があります。「 — 」は「置換なし」を意味します。 「 — 」文字列は、C（チェーン）フラグと組み合わせて使用すると、置換前にタイトルを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧で囲み、複 `[]`数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> 最後のルール。 </p> <p> 書き換え処理を停止し、追加の書き換え規則を適用しない。 このフラグを使用すると、現在のタイトルが処理されなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のタイトルではなく）最後の書き換えルールのタイトルを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p> このフラグは、現在のルールを次のルール（次のルールにチェーンすることもできます）にチェーン付けします。 ルールが一致する場合、置換プロセスは通常どおり続行されます。 ルールが一致しない場合は、後続のすべてのチェーンルールがスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p> このフラグは、Patternで大文字と小文字を区別しません。 つまり、パターンが現在のタイトルと一致する場合、「A-Z」と「a-z」の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p> 次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは書き換えエンジンに対して、ルールセット内の次のnumルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nとなり、Nはelse節内の規則の数を表します。 （これは'chain|C'フラグとは異なります。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> このフラグは、値VALに設定された環境変数「VAR」を作成します。VALには、正規表現のバックリファレンス$Nと%Nを含めることができ、これは拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照できます。 タイトルの情報を削除し、記憶するには、このフラグを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCondディレクティブ（オプション） {#section_9D72B2AB454849A7B681BC39C506AAA3}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleより前にある場合、ルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

書き換え条件ディレクティブは次の形式をとります。

```
RewriteCond TestString CondPattern [Flags]
```

**TestStringは** 、次の構成要素を含む文字列です。

プレーンテキスト — 変更なしで渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* **RewriteRule Backreferences** これらの一致するバックリファレンスは、対応するRewriteRuleパターン内で$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond Backreferences** これらの一致するバックリファレンスは、最後に一致したRewriteCond CondPattern内にあり、%N (0 &lt;= N &lt;= 9)の形式をとります。

**変数** ：これらは%{NAME_OF_VARIABLE}という形式の変数で、NAME_OF_VARIABLEは定義済みの変数の名前を表す文字列です。 環境変数の設 `[E]` 定について詳しくは、フラグを参照してください。 変数は、検索結果を生成した検索フォームでも定義できます。

**Functions** THESE are functions of the form ${NAME_OF_FUNCTION:key} NAME_OF_FUNCTION is:

* 「lower」を指定すると、すべての文字がキ *ーで* 小文字になります。
* toupperはすべての文字を大文字 *で入力* します。
* escapeキー内のすべての文字をURLエンコード *します*。
* a..z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9、「*」、「 — 」、「。」、「/」、「@」および「_」は変更されず、スペースは「+」に変換され、その他のすべての文字は%xx URLエンコードされた等価な文字に変換されます。
* unescapeは、「+」をスペースに戻し、すべての%xx URLエンコードされた文字を1文字に戻します。

次の特殊な置換文字列があります。「 — 」は「置換なし」を意味します。 「 — 」文字列は、C（チェーン）フラグと組み合わせて使用すると、置換が発生する前にURLを複数のパターンに一致させることができます。

**CondPattern** 標準の拡張正規表現で、いくつか追加されました。 パターン文字列の先頭に「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規表現文字列の代わりに、次の特別なバリアントの1つを使用できます。

これらのテストのすべてに、感嘆符(&#39;!&#39;)の前に付けることもできます彼らの意味を打ち消す

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern文字列 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書的に少ない。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書式的に <i></i> CondPatternより小さい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> 辞書的に大きい。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書 <i>式的に</i> CondPatternより大きい場合はTrue <i>です</i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレ <i>ーン文字列として扱い</i> 、辞書式的にTestStringと比較 <i>します</i>。 TestStringが辞書 <i>的に</i> CondPatternと等しい場合はTrue <i>です</i>。 つまり、2つの文字列は完全に等しい（文字単位で）。 CondPattern <i>が</i> ""（2つの引用符）だけの場合、TestStringと空の文字列が <i>比較されます</i> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧で囲み`[]`、複数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Flag </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' （大文字と小文字を区別しない） </p> </td> 
   <td colname="col2"> <p>テストを無感度にします。 つまり、拡張された <i>TestStringとCondPatternの両方で「A-Z」と「a-z」の間に違いはありま</i> せん <i></i>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' （または次の条件） </p> </td> 
   <td colname="col2"> <p> ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせるには、これを使用します。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section_E7454FFE169E459AABD9D033651939CB}

標準的なタイトル形式を持つ会社のウェブサイトがあるとします。「My Company」の後にハイフンが続き、次にページ固有の説明（「My Company - Welcome」や「My Company - News」など）が続きます。 タイトルから「マイカンパニー — 」を削除し、サイトのインデックスを作成する際にタイトル全体を大文字に変換する場合。

次の書き換えルールは、関数toupperを使用して、タイトルの説明部分のみを大文字に書き換えます。

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

ルールのパターンには、「 `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` My Company — 」に続くタ **`(.*)`** イトルコンテンツに一致する後方参照が含まれています。 パターンの一部を括弧( )で囲むと、代替(Substitution)で参照できる後方参照が作成されることに注意してください。 この例では、置換(${toupper:**$1**})は、toupper関数を使用してバックリファレンス(**$1**)を書き換えます。

したがって、「My Company - Welcome」という形式のタイトルは「WELCOME」に書き換えられます。

**通知**

書き換えエンジンソフトウェアは、もともとApache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようにしました。

## 検索タイトルルールの追加 {#task_155CECB74BE3444384EDBBD04F41515E}

検索タイトルルールを追加して、Webサイトの検索結果に表示するタイトルの表示方法を指定できます。 タイトルの任意の部分を操作できます。

<!-- 

t_adding_search_title_rules.xml

 -->

**検索タイトルールを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Rewrite Rules]** ます **[!UICONTROL Search Title Rules]**。
1. フィールド [!DNL Search Title Rules] に、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が許可されます。
1. （オプション）ページの [!DNL Search Title Rules] フィールドにテ [!DNL Test Search Title Rules] ストのタイトルを入力し、「テスト」をクリック **します**。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Search Title Rules] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

