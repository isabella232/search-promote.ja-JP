---
description: ルールの書き換えメニューを使用して、クロールおよび検索URLとタイトルルールを設定します。
solution: Target
subtopic: Rewrite Rules
title: 書き換えルールメニューについて
topic: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '10202'
ht-degree: 0%

---


# [書き換え規則]メニューについて{#about-the-rewrite-rules-menu}

ルールの書き換えメニューを使用して、クロールおよび検索URLとタイトルルールを設定します。

## クロールリストストアのURLルールについて{#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

クロールURLルールは、Webコンテンツ内で遭遇するURLを書き換える方法を指定します。 ルールと条件の数に制限はありません。また、検出されたURLの任意の部分を操作できます。

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

クロールルールは、Webサイトの訪問者ごとに一意のセッション識別子など、URLの動的な部分を書き換えるのに最も役立ちます。 再書き込みルールを使用して、クエリパラメーターなど、URLの一部を検索ロボットから非表示にすることもできます。 デフォルトでは、ルールは指定されておらず、URLの書き換えは実行されません。

Webサイトがクロールされると、埋め込みコンテンツのURLは、クロールする追加のWebページの一時リストに保存されます。 URLがこのリストに追加される前に、ストア書き換えルールが適用されます。 通常、ストア書き換えルールは、URLからセッションIDを削除したり、特定のセッションIDをクロール用に強制するために使用します。 検索ロボットがリストからURLを取得すると、Retrieve書き換えルールを使用して、そのURLの一部を再度操作します。 通常、取得ルールは、時間に依存するデータをURLに挿入する際に使用します。 これは、Webサイトから実際にページを取得するために使用される最終URLです。

[クロールリストの取得URLルールについて](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)を参照してください。

通常は、「URLルールを保存」のみを使用します。 「URLの取得ルール」は、セッションIDなどの動的データがURLに含まれている場合、およびその動的データが時間の経過と共に変化し、有効なままになる場合にのみ必要です。 この場合、「URLルールの保存」を使用して、検出されたURLからデータの最新の状態を取得します。 次に、検索ロボットがページを取得しようとする際に、「URLルールの取得」を使用して各URLにデータを追加します。

各ルールは、書き換え規則(RewriteRule)ディレクティブと、1つ以上のオプションの書き換え条件(RewriteCond)を使用して指定されます。 ルールの順序は重要です。 ルールセットは、ルールごとにループされます。 ルールが一致する場合、対応する書き換え条件をループ処理します。 クロールURLルールは次の方法で指定します。

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

埋め込みURLが見つかると、検索ロボットはURLと各クロールルールのパターンとの一致を試みます。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構成される新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示された順に処理されます。 再書き込みエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)とを照合しようとします。 2つの一致が見つかった場合は、それ以上条件がなくなるまで、次の条件が処理されます。 すべての条件が一致する場合、URLはルールで指定されている置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて{#section_162122340BB34F12BB9A36DC9349092B}

RewriteRuleディレクティブは次の形式を持ちます。

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` はPOSIXの正規式で、現在のURLに適用されます。以前のルールでは既にURLと一致し変更されている場合があるので、「現在のURL」は、リクエストされた元のURLと異なる場合があります。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「not」文字(&#39;!&#39;)は使用できません。 を追加します。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のURLがこのパターンと一致しない場合にのみtrueになります。 「not」文字は、除外パターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。

>[!NOTE]
>
>パターンでは、「not」文字とグループ化されたワイルドカードの両方を使用できません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用してパターン内に逆参照を作成できます。逆参照は、SubstitutionとCondPatternで参照できます。

**** 置換URLは置換文字列に置換され、次の文字列が含まれます。

テキスト：変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例：`RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RewriteCond** Backreferencesこれらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0)  &lt;>

変数：これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設定について詳しくは、`*[E]*`フラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escape URLは、*key*&#x200B;内のすべての文字をエンコードします。
* 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、&#39;_&#39;は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」を空白に戻し、すべての%xx個のURLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次に、特殊な置換文字列を示します。`'-'`は、&quot;NO substitution&quot;を意味します。 `'-'`文字列はC（チェーン）フラグと共に使用されることが多く、置換が発生する前にURLを複数のパターンに一致させます。

**フラグ**

（オプション）フラグは角括弧`[]`で囲みます。 複数のフラグはコンマで区切られます。

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
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のURLではなく）最後の書き換えルールのURLを使用して（最初の書き換えルールから再び始める）書き換え処理を再実行します。 デッドループの作成には注意が必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールに連結します（次のルールに連結することもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行します。 ルールが一致しない場合は、それ以降のチェーン付きルールはすべてスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> パターンが現在のURLと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の間に違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは、書き換えエンジンにルールセット内の次の数値ルールをスキップさせます。 このフラグを使用して、疑似if-then-else構文を作成します。 then節の最後の規則はskip=Nになります。Nはelse節の規則の数です。 </p> <p> <p>注意： このフラグは'chain|C'フラグとは異なります。) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p>値VALに設定された環境変数"VAR"を作成します。VALには、正規式のバックリファレンス（$Nと%N）を含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで再参照できます。 </p> <p>このフラグを使用して、URLから情報を取り除き、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Store Rewrite RulesとRetrieve Rewrite Rulesは変数の値を共有します。 この動作のため、埋め込みURLを検出して保存する際に、変数に時間の影響を受けるsessionid値を設定できます。 一時ストレージリストから次のURLを取得する場合、そのページを取得する前に、最新のsessionid値をそのURLに追加できます。

**関数を持つRewriteRuleの例**

大文字と小文字が区別されるサーバーがあり、`"www.mydomain.com"`と`"www.MyDomain.com"`の処理方法が異なるとします。 サーバーが正しく動作するようにするには、`"www.MyDomain.com."`を参照するリンクが一部のドキュメントーに含まれていても、ドメインが常に`"www.mydomain.com"`であることを確認します。これを行うには、次のルールを使用します。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

この書き換えルールは、関数`tolower`を使用してURLのドメイン部分を書き換え、次のように常に小文字に変換します。

1. パターン`(^https://([^/]*)(.*)$)`には、URL内の`https://`と最初の`/`の間のすべての文字と一致する後方参照`([^/]*)`が含まれています。 このパターンには、URL内の残りのすべての文字と一致する2つ目の後方参照`(.*)`も含まれます。

1. 置換`(https://${tolower:$1}$2)`は、最初のバックリファレンス`(https:// ${tolower:$1}$2)`で`tolower`関数を使用し、残りのURLを`(https://${tolower:$1} $2)`に残してURLを書き換えるよう検索エンジンに指示します。

これにより、`https://www.MyDomain.com/INTRO/index.Html`形式のURLが`https://www.mydomain.com/INTRO/index.Html`に書き換えられる。

## RewriteCondディレクティブについて{#section_CD5A19B2D3204F73B645411931FC34A1}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleの前にある場合、そのルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。 書き換え条件は、次の形式を取ります。

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` は、次の構文を含む文字列です。

テキスト：変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例： `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`

* **RewriteCond** Backreferencesこれらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0)&lt;>

変数：これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を示す文字列にすることができます。 変数の設定について詳しくは、RewriteRule *`[E]`*&#x200B;フラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escapeキー内のすべての文字をURLエンコードします。 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、&#39;_&#39;は変更されません。スペースは&#39;+&#39;に変換され、その他のすべての文字は`%xx` URLエンコードされた等価な文字に変換されます。
* unescapeは&#39;+&#39;をスペースに戻し、すべての`%xx` URLをエンコードして文字を1文字に戻します。

**CondPatternは標準の拡張正規式で、いくつか追加されています。** パターン文字列の先頭には`!`文字（感嘆符）を付け、一致しないパターンを指定できます。 実際の正規式文字列の代わりに、次の特別な変数の1つを使用できます。

>[!NOTE]
>
>また、これらすべてのテストの前に感嘆符(&#39;!&#39;)を付けることもできます 彼らの意味を打ち消す

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
   <td colname="col2"> <p>辞書的に少ない。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式的にCondPatternより小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に大きい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式順でCondPatternより大きい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式上CondPatternと等しい場合、つまり、2つの文字列が完全に等しい（文字単位で）場合はtrueです。 CondPatternが"" （2つの引用符）の場合、TestStringと空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ**
（オプション）フラグは角括弧で囲み `[]`ます。複数のフラグはコンマで区切られます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p>このフラグは、テストで大文字と小文字が区別されないようにします。つまり、拡張されたTestStringとCondPatternの両方で、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

一部のWebページでは、訪問者が初めてサイトに到達したときに「sessionid」CGI変数が割り当てられます。 この変数は訪問者を識別するために使用され、訪問者がサイトを閲覧する際に変数が渡されます。 検索ロボットはサイトの訪問者のように見えるので、「sessionid」番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値を割り当てようとしても、この「sessionid」値を1つ維持します。 これを確実に行うには、2つの書き換えルールが必要です。

最初のルールは、sessionid変数を識別して保存するために使用します。

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRuleはEフラグ`([E=sessionid:$1])`を使用して、sessionid CGIパラメータの現在の値を変数`sessionid`に割り当てます。 `$1`は最初の逆参照を参照します。この逆参照は、RewriteRuleのPattern `([^&#]+)`内の最初の括弧の間に含まれます。

正規式`^&#]+`は、URLの一部を`sessionid`と次の`**&**or**#**`文字の間に一致させます。 このRewriteRuleは、sessionid変数の初期値を作成する目的でのみ使用されるので、書き換えは行われません。 ルールの「Substitution」フィールドは`-`に設定され、書き換えの必要がないことを示します。

RewriteCondは変数`sessionid` ( `%{sessionid}`)を調べます。 1文字も含まない場合は(!.+)の場合、RewriteRuleは一致と見なされます。

このルールを使用すると、URLは`https://www.domain.com/home/?sessionid=1234&function=start`として読み取られ、値`1234`を変数`sessionid`に割り当てます。

2つ目のルールは、次のRewriteRuleパターンに一致するすべてのURLを書き換えるために使用されます。

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule Patternには、2つのバックリファレンスが含まれています。`(.+)`と`(.*)`。 最初の後方参照は、`sessionid`より前のすべての文字と一致します。 2番目の後方参照は、末尾`&`または`#`の後のすべての文字と一致します。

置換パターンは、最初のバックリファレンスを使用してURLを書き換え、文字列「sessionid=」が続き、最初のルール`%{sessionid}`で定義されたセッションID変数の値が続き、2番目のバックリファレンスが続きます。`($1sessionid=%{sessionid} $2)`

このRewriteRuleにRewriteCondが含まれていないことに注意してください。 したがって、RewriteRule *Pattern*&#x200B;に一致するすべてのURLが書き換えられます。 したがって、sessionid変数(`%{sessionid}`)の値が`1234`の場合、`https://www.domain.com/products/?sessionid=5678&function=buy`形式のURLは`https://www.domain.com/products/?sessionid=1234&function=buy`に書き換えられます

## 確認{#section_B17088EF38244496BC1DDD4ECF75EB5B}

再書き込みエンジンソフトウェアは、元々Apache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようになりました。

## クロールリストストアのURL規則{#task_22DD40DF95584B12BE8E6ECFBF579BCD}を追加する

クロールリストストアURLルールを追加して、Webコンテンツ内で検出されたURLの書き換え方法を指定できます。 ルールと条件の数に制限はありません。また、検出されたURLの任意の部分を操作できます。

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**クロールリストストアのURLルールを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Rewrite Rules]**/**[!UICONTROL Crawl List Store URL Rules]**&#x200B;をクリックします。
1. [!DNL Crawl List Store URL Rules]フィールドに、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。
1. （オプション）[!DNL Crawl List Store URL Rules]ページの[!DNL Test Crawl List Store URL Rules]フィールドに、クロールルールをテストするテストURLを入力し、**「テスト**」をクリックします。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Crawl List Store URL Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## クロールリスト取得URLルールについて{#concept_EC8E2E48B99A458D8567B526C9827CBA}

クロールURLのルールでは、Webコンテンツ内で検出されたURLを書き換える方法を指定します。 ルールと条件の数に制限はありません。また、検出されたURLの任意の部分を操作できます。

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

ルールの効果がユーザーに表示される前に、サイトインデックスを必ず作成し直してください。

クロールルールは、Webサイトの訪問者ごとに一意のセッション識別子など、URLの動的な部分を書き換えるのに最も役立ちます。 再書き込みルールを使用して、クエリパラメーターなど、URLの一部を検索ロボットから非表示にすることもできます。 デフォルトでは、ルールは指定されておらず、URLの書き換えは実行されません。

Webサイトがクロールされると、埋め込みコンテンツのURLは、クロールする追加のWebページの一時リストに保存されます。 検索ロボットがリストからURLを取得すると、「Retrieve Rewrite Rules」を使用して、そのURLの一部が操作されます。 通常、取得ルールは、時間に依存するデータをURLに挿入するために使用します。 これは、Webサイトから実際にページを取得するために使用される最終URLです。

「Retrieve Rewrite Rules」は、セッションIDなどの動的データがURLに含まれ、その動的データが時間の経過とともに変化して有効なままになる場合にのみ必要です。 この場合、ストア書き換えルールを使用して、遭遇したURLからデータの最新の状態を取得します。 次に、検索ロボットがページを取得したときに、「Retrieve Rewrite Rules」を使用して各URLにそのデータを追加します。

各ルールは、書き換え規則(RewriteRule)ディレクティブと、1つ以上のオプションの書き換え条件(RewriteCond)を使用して指定されます。 ルールの順序は重要です。 ルールセットは、ルールごとにループされます。 ルールが一致する場合、対応する書き換え条件をループ処理します。 クロールURLルールは次の方法で指定します。

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

埋め込みURLが見つかると、検索ロボットはURLと各クロールルールのパターンとの一致を試みます。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構成される新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示された順に処理されます。 再書き込みエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)とを照合しようとします。 2つの一致が見つかった場合は、それ以上条件がなくなるまで、次の条件が処理されます。 すべての条件が一致する場合、URLはルールで指定されている置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて{#section_32B24B29627946398AFBC5F869A610CB}

RewriteRuleディレクティブは次の形式を持ちます。

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` はPOSIXの正規式で、現在のURLに適用されます。以前のルールでは既にURLと一致し変更されている場合があるので、「現在のURL」は、リクエストされた元のURLと異なる場合があります。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「not」文字(&#39;!&#39;)は使用できません。 を追加します。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のURLがこのパターンと一致しない場合にのみtrueになります。 「not」文字は、除外パターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。

>[!NOTE]
>
>パターンでは、「not」文字とグループ化されたワイルドカードの両方を使用できません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用してパターン内に逆参照を作成できます。逆参照は、SubstitutionとCondPatternで参照できます。

**** 置換URLは置換文字列に置換され、次の文字列が含まれます。

テキスト：変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例：`RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** RewriteCond Backreferences**一致する最後に一致したRewriteCondPattern内のバックリファレンスに一致し、%Nの形式をとります(0 &lt;= N &lt;= 9)。

変数：これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列です。 環境変数の設定について詳しくは、*[E]*&#x200B;フラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escape URLは、*key*&#x200B;内のすべての文字をエンコードします。
* 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、&#39;_&#39;は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」を空白に戻し、すべての%xx個のURLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次に、特殊な置換文字列を示します。「 — 」は「NO置換」を意味します。 「 — 」文字列はC（チェーン）フラグと共に使用されることが多く、置換が発生する前にURLを複数のパターンに一致させることができます。

**フラグ**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
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
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のURLではなく）最後の書き換えルールのURLを使用して（最初の書き換えルールから再び始める）書き換え処理を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールに連結します（次のルールに連結することもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行します。 ルールが一致しない場合は、それ以降のチェーン付きルールはすべてスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> パターンが現在のURLと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の間に違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは、書き換えエンジンにルールセット内の次の数値ルールをスキップさせます。 このフラグを使用して、疑似if-then-else構文を作成します。 then節の最後の規則はskip=Nになります。Nはelse節の規則の数です。 </p> <p> <p>注意： このフラグは'chain|C'フラグとは異なります。) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p>値VALに設定された環境変数"VAR"を作成します。VALには、正規式のバックリファレンス（$Nと%N）を含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで再参照できます。 </p> <p>このフラグを使用して、URLから情報を取り除き、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Store Rewrite RulesとRetrieve Rewrite Rulesは変数の値を共有します。 この動作のため、埋め込みURLを検出して保存する際に、変数に時間の影響を受けるsessionid値を設定できます。 一時ストレージリストから次のURLを取得する場合、そのページを取得する前に、最新のsessionid値をそのURLに追加できます。

**関数を持つRewriteRuleの例**

大文字と小文字が区別されるサーバーがあるとします。このサーバーでは、「www.mydomain.com」と「www.MyDomain.com」の文字列の処理方法が異なります。 サーバーが正しく動作するようにするには、「www.MyDomain.com」を参照するリンクが一部のドキュメントーに含まれていても、ドメインが常に「www.mydomain.com」であることを確認してください。 これを行うには、次のルールを使用します。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

この書き換えルールは、関数`tolower`を使用してURLのドメイン部分を書き換え、次のように常に小文字に変換します。

1. パターン`(^https://([^/]*)(.*)$)`には、URL内の`https://`と最初の`/`の間のすべての文字に一致する後方参照** `([^/]*)`**が含まれています。 このパターンには、URL内の残りのすべての文字と一致する2つ目の後方参照`(.*)`も含まれます。
1. 置換`(https://${tolower:$1}$2)`は、最初のバックリファレンス`(https:// ${tolower:$1}$2)`で`tolower`関数を使用し、残りのURLを`(https://${tolower:$1} $2)`に残してURLを書き換えるよう検索エンジンに指示します。

これにより、`https://www.MyDomain.com/INTRO/index.Html`形式のURLが`https://www.mydomain.com/INTRO/index.Html`に書き換えられる。

## RewriteCondディレクティブについて{#section_ADD642A24B68452CB98294A0BD687EC3}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleの前にある場合、そのルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。 書き換え条件は、次の形式を取ります。

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` は、次の構文を含む文字列です。

テキスト：変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例： `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`

* **RewriteCond** Backreferencesこれらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0)&lt;>

変数：これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を示す文字列にすることができます。 変数の設定について詳しくは、RewriteRule *`[E]`*&#x200B;フラグを参照してください。

関数：これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escapeキー内のすべての文字をURLエンコードします。 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、「*」、「 — 」、「。」、「/」、「@」、「_」は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」をスペースに戻し、すべての%xx URLをエンコードして文字を1文字に戻します。

**CondPatternは標準の拡張正規式で、いくつか追加されています。** パターン文字列の先頭には「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規式文字列の代わりに、次の特別な変数の1つを使用できます。

>[!NOTE]
>
>また、これらすべてのテストの前に感嘆符(&#39;!&#39;)を付けることもできます 彼らの意味を打ち消す

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
   <td colname="col2"> <p>辞書的に少ない。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式的にCondPatternより小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に大きい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式順でCondPatternより大きい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> CondPatternをプレーン文字列として扱い、辞書式順にTestStringと比較します。 TestStringが辞書式上CondPatternと等しい場合、つまり、2つの文字列が完全に等しい（文字単位で）場合はtrueです。 CondPatternが"" （2つの引用符）の場合、TestStringと空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ**
（オプション）フラグは角括弧で囲み `[]`ます。複数のフラグはコンマで区切られます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p>このフラグは、テストで大文字と小文字が区別されないようにします。つまり、拡張されたTestStringとCondPatternの両方で、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

一部のWebページでは、訪問者が初めてサイトに到達したときに「sessionid」CGI変数が割り当てられます。 この変数は訪問者を識別するために使用され、訪問者がサイトを閲覧する際に変数が渡されます。 検索ロボットはサイトの訪問者のように見えるので、「sessionid」番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値を割り当てようとしても、この「sessionid」値を1つ維持します。 これを確実に行うには、2つの書き換えルールが必要です。

最初のルールは、sessionid変数を識別して保存するために使用します。

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRuleはEフラグ`([E=sessionid:$1])`を使用して、sessionid CGIパラメータの現在の値を変数`sessionid`に割り当てます。 `$1`は最初の逆参照を参照します。この逆参照は、RewriteRuleのPattern `([^&#]+)`内の最初の括弧の間に含まれます。

正規式`^&#]+`は、URLの一部を`sessionid`と次の**&amp;**または**#**文字の間で一致させます。 このRewriteRuleは、sessionid変数の初期値を作成する目的でのみ使用されるので、書き換えは行われません。 ルールの「Substitution」フィールドは`-`に設定され、書き換えの必要がないことを示します。

RewriteCondは変数`sessionid` ( `%{sessionid}`)を調べます。 1文字も含まない場合は(!.+)の場合、RewriteRuleは一致と見なされます。

このルールを使用すると、URLは`https://www.domain.com/home/?sessionid=1234&function=start`として読み取られ、値`1234`を変数`sessionid`に割り当てます。

2つ目のルールは、次のRewriteRuleパターンに一致するすべてのURLを書き換えるために使用されます。

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule Patternには、2つのバックリファレンスが含まれています。`(.+)`と`(.*)`。 最初の後方参照は、`sessionid`より前のすべての文字と一致します。 2番目の後方参照は、末尾`&`または`#`の後のすべての文字と一致します。

置換パターンは、最初のバックリファレンスを使用してURLを書き換え、文字列「sessionid=」が続き、最初のルール`%{sessionid}`で定義されたセッションID変数の値が続き、2番目のバックリファレンスが続きます。`($1sessionid=%{sessionid} $2)`

このRewriteRuleにRewriteCondが含まれていないことに注意してください。 したがって、RewriteRule *Pattern*&#x200B;に一致するすべてのURLが書き換えられます。 したがって、sessionid変数(`%{sessionid}`)の値が`1234`の場合、`https://www.domain.com/products/?sessionid=5678&function=buy`形式のURLは`https://www.domain.com/products/?sessionid=1234&function=buy`に書き換えられます

## 確認{#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

再書き込みエンジンソフトウェアは、元々Apache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようになりました。

## クロールリスト取得URLルール{#task_94A28ED7DC404BFF9767DBB5ADEE6B7A}を追加しています

クロールリスト取得URLルールを追加して、Webコンテンツ内で遭遇したURLを書き換える方法を指定できます。 「Retrieve Rewrite Rules」は、セッションIDなどの動的データがURLに含まれている場合、およびその動的データが有効なままになるように時間の経過と共に変化する場合にのみ必要です。

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**クロールリスト取得URLルールを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Rewrite Rules]**/**[!UICONTROL Crawl List Retrieve URL Rules]**&#x200B;をクリックします。
1. [!DNL Crawl List Retrieve URL Rules]フィールドに、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。
1. （オプション）[!DNL Crawl List Retrieve URL Rules]ページの[!DNL Test Crawl List Retrieve URL Rules]フィールドに、クロールルールをテストするテストURLを入力し、**「テスト**」をクリックします。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Crawl List Retrieve URL Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## クロールタイトルールについて{#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

クロールタイトルルールでは、Webコンテンツ内で遭遇したタイトルを、検索インデックスに保存する前に書き換える方法を指定します。

<!-- 

c_about_crawl_title_rules.xml

 -->

例えば、再書き込みルールを使用して、組織名など、タイトルの一部を削除できます。 Webサイトがクロールされると、遭遇したタイトルは一時バッファーに格納されます。 ただし、このバッファーにタイトルを追加する前に、タイトルルールが適用されます。 デフォルトでは、サイト検索/マーチャンダイジングにはクロールタイトルルールがなく、タイトルの変更も行われません。

ルールの効果がユーザーに表示される前に、サイトインデックスを作成し直します。

履歴機能を使用して、クロールタイトルルールに対して行った変更をすばやく元に戻すことができます。

ルールは、2つの主要な要素で構成できます。rewriteRuleおよびオプションのRewriteCond。 ルールと条件の数に制限はありません。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールが一致する場合、（オプションの）対応する書き換え条件をループ処理します。 クロールURLルールは、次の方法で指定します。

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

タイトルが見つかると、検索ロボットはタイトルと各クロールルールのパターンとの一致を試みます。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、URLは置換文字列から構成される新しい値で置換され、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示された順に処理されます。 再書き込みエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)とを照合しようとします。 2つの一致が見つかった場合は、それ以上条件がなくなるまで、次の条件が処理されます。 すべての条件が一致する場合、URLはルールで指定されている置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

テキストボックスに「クロールURLルール」を入力し、「変更の保存」をクリックします。 空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。 検索ルールをテストするには、「テスト書き換えルール」テキストボックスにテストURLを入力し、「テスト」をクリックします。

## RewriteRuleディレクティブ{#section_669445C505754E838E14029D6583D9B6}

各RewriteRuleディレクティブは、1つの書き換え規則を定義します。 ルールは、リストに表示されている順序で適用されます。 書き換えルールは次の形式を取ります。

```
RewriteRule Pattern Substitution [Flags]
```

**PatternはPOSIXの正規式で、現在のタイトルに適用されます。** 「現在のタイトル」は、以前のルールで既に一致し変更されているので、元のタイトルとは異なります。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「not」文字(&#39;!&#39;)は、 を追加します。 「not」文字を使用すると、パターンを無効にできます。つまり、現在のタイトルがパターンと一致しない場合にのみ真になります。 「not」文字は、除外パターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。 注意：パターンでは、「not」文字とグループ化されたワイルドカードの両方を使用できません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して逆参照を作成できます。逆参照はSubstitutionとCondPatternで参照できます。

**** 置換タイトルは置換文字列に置換されます。文字列には次の値を含めることができます。

プレーンテキスト — 変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 次に、2種類のバックリファレンスを示します。

* RewriteRuleバックリファレンス

   対応するRewriteRuleパターン内のこれらの一致後参照は、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RewriteCond Backreferences

   最後に一致したRewriteCondPattern内のこれらの一致後参照は、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を示す文字列にすることができます。 環境変数の設定について詳しくは、`[E]`フラグを参照してください。

関数これらは${NAME_OF_FUNCTIONの形式の関数です。key} NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。

>[!NOTE]
>
>次に、特殊な置換文字列を示します。「 — 」は「NO置換」を意味します。 「 — 」文字列はC（チェーン）フラグと共に使用すると便利で、置換が発生する前にタイトルを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>最後のルール。 </p> <p> 書き換えプロセスを停止し、追加の書き換え規則を適用しません。 このフラグを使用すると、現在のタイトルがそれ以上処理されなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> 元のタイトルではなく、最後の書き換えルールのタイトルを使用して、書き換え処理（最初の書き換えルールから再び開始）を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p>現在のルールを次のルールに連結します（次のルールに連結することもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行します。 ルールが一致しない場合は、それ以降のチェーン付きルールはすべてスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p>パターンが現在のタイトルと一致する場合に、パターンで大文字と小文字が区別されないようにします（つまり、「A-Z」と「a-z」の違いはありません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは、書き換えエンジンにルールセット内の次の数値ルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nになります。Nはelse節の規則の数です。 (注意：これは'chain|C'フラグとは異なります。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> 値VALに設定された環境変数"VAR"を作成します。VALには、正規式のバックリファレンス（$Nと%N）を含めることができ、拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照できます。 タイトルの情報を削除して記憶するには、このフラグを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCondディレクティブ（オプション） {#section_D664B71DE3884E0790531804C49A3222}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleの前にある場合、そのルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

再書き込み条件ディレクティブは、次の形式を取ります。

```
RewriteCond TestString CondPattern [Flags] 
```

**TestStringは次の** 構成要素を含む文字列です。

プレーンテキスト — 変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* RewriteRuleバックリファレンス対応するRewriteRuleパターン内のこれらの一致するバックリファレンスを返し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RewriteCond Backreferences最後に一致したRewriteCondPatternのバックリファレンスと一致し、%N (0 &lt;= N &lt;= 9)の形式をとります。

変数これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を示す文字列にすることができます。 環境変数の設定について詳しくは、`[E]`フラグを参照してください。

関数これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escapeキー内のすべての文字をURLエンコードします。
* 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、「*」、「 — 」、「。」、「/」、「@」、「_」は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」を空白に戻し、すべての%xx個のURLエンコードされた文字を1文字に戻します。

**CondPatternは標準の拡張正規式で、いくつか追加されています。** パターン文字列の先頭には「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規式文字列の代わりに、次の特別な変数の1つを使用できます。

>[!NOTE]
>
>これらのテストの前に感嘆符(&#39;!&#39;)を付けることができます 彼らの意味を打ち消す

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
   <td colname="col2"> <p>辞書式的に少ない。 </p> <p><i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>より小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書形式的に大きい。 </p> <p><i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式順で<i>CondPattern</i>より大きい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> 辞書式的に等しい。 </p> <p><i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>と等しい場合、つまり、2つの文字列が完全に等しい（文字単位）場合はtrueです。 <i>CondPattern</i>が単なる""（2つの引用符）の場合、<i>TestString</i>と空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p> テストを無感度にします。 つまり、拡張された<i>TestString</i>内と<i>CondPattern.</i>内の両方で、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> または次の条件。 </p> <p>このフラグを使用して、ルール条件を暗黙的なANDの代わりにローカルのORと組み合わせます。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

標準的なタイトル形式を持つ会社のウェブサイトがあるとします。「マイ会社」の後にハイフンが続き、ページ固有の説明(例：「マイ会社 — ようこそ」、「マイ会社 — ニュース」)が続きます。 タイトルから「マイ会社 — 」を除去し、サイトのインデックスを作成する際に、タイトル全体を大文字に変換する必要がある。

次の再書き込みルールは、関数toupperを使用して、タイトルの説明部分のみを大文字に書き換えます。

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

ルールのパターン`(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))`には、「My会社 — 」に続くタイトルコンテンツに一致する後方参照`(.*)`が含まれています。 パターンの一部を括弧( )で囲むと、代替(Substitution)で参照可能な逆参照が作成されることに注意してください。 この例では、置換(${toupper:**$1**})は、toupper関数を使用してバックリファレンス(**$1**)を書き換えます。

したがって、「マイ会社 — ようこそ」という形式のタイトルは、「ようこそ」と書き換えられます。

**確認**

再書き込みエンジンソフトウェアは、元々Apache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようになりました。

## クロールタイトルルールの追加{#task_272BB4C603BA4C9ABDBEEB398798B101}

クロールタイトルルールを追加して、Webコンテンツ内で遭遇したタイトルを、検索インデックスに保存する前に書き直す方法を指定できます。

<!-- 

t_adding_crawl_title_rules.xml

 -->

**クロールタイトルルールを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Rewrite Rules]**/**[!UICONTROL Crawl Title Rules]**&#x200B;をクリックします。
1. [!DNL Crawl Title Rules]フィールドに、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。
1. （オプション）[!DNL Crawl Title Rules]ページの[!DNL Test Crawl Title Rules]フィールドに、テストする検索ルールを持つテストURLを入力し、**「テスト**」をクリックします。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Crawl Title Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 検索URLルールについて{#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

検索URLルールは、Webサイト検索結果内のURLの表示方法を指定します。 ルールは、完全なURLに対して機能します。 セッションID情報が頻繁に保持されるクエリ引数など、URLの任意の部分を操作できます。

<!-- 

c_about_search_url_rules.xml

 -->

通常、検索URLルールは、セッションIDをURLに挿入するために使用されます。 ただし、検索URLルールを使用して、結果と共に表示されるドメイン名を変更することもできます。 デフォルトでは、ルールは指定されておらず、URLの変更は行われません。

検索URLルールは、次の2つの主要要素で構成できます。rewriteRuleおよびオプションのRewriteCond。 URLが検索結果の一部として含まれる場合、ルールを使用してURLが操作されます。 検索URLのルールおよび条件の数に制限はありません。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールが一致すると、ソフトウェアは対応する書き換え条件をループ処理します（オプション）。 クロールURLルールは、次の方法で指定します。

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

URLを処理する際、サイト検索/マーチャンダイジングは、URLを各検索ルールのパターンに一致させようとします。 一致が見つからなかった場合、書き換えエンジンは直ちにルールの処理を停止し、セット内の次のルールに進みます。 パターンが一致する場合、書き換えエンジンは対応するRewriteCond命令を探します。 条件が存在しない場合、URLは新しい値で置き換えられます。 この値は置換文字列から構成され、ルールセット内の次のルールに続きます。 条件が存在する場合、それらの条件が表示される順序は、処理方法です。 再書き込みエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)とを照合しようとします。 2つの一致が見つかった場合は、それ以上条件がなくなるまで、次の条件が処理されます。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブについて{#section_A3473B5B90B74DA1970213113A90591E}

書き換えルールは次の形式を取ります。

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**パ** ターンはPOSIXの正規式で、現在のURLに適用されます。「現在のURL」は、以前のルールで既に一致し変更されている場合があるので、元のURLと異なる場合があります。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「not」文字(&#39;!&#39;)は、 を追加します。 「not」文字を使用すると、パターンを無効にできます。 つまり、現在のURLがパターンと一致しない場合にのみtrueになります。 除外パターンに一致した方がよい場合や、最終的なデフォルトのルールとして、「not」文字を使用できます。 パターンでは、「not」文字とグループ化ワイルドカードの両方を使用できません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

括弧を使用して逆参照を作成できます。逆参照はSubstitutionとCondPatternで参照できます。

**** 置換URLは、次の文字列を含む置換文字列に完全に置換されます。

プレーンテキスト — 変更せずに渡されるテキスト。

[バックリファレンス] PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

RewriteRuleバックリファレンス対応するRewriteRuleパターン内のこれらの一致するバックリファレンスを返し、$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RewriteCond Backreferences — これらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0 &lt;= N &lt;= 9)。

関数：次に、${NAME_OF_FUNCTION:key}の形式の関数を示します。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escape URLは、*key*&#x200B;内のすべての文字をエンコードします。
* 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、&#39;*&#39;、&#39;-&#39;、&#39;.&#39;、&#39;/&#39;、&#39;@&#39;、&#39;_&#39;は変更されません。スペースは「+」に変換されます。その他のすべての文字は、%xx個のURLエンコードされた等価な文字に変換されます。
* 「+」を空白に戻し、すべての%xx個のURLエンコードされた文字を1文字に戻します。

>[!NOTE]
>
>次に、特殊な置換文字列を示します。「 — 」は「NO置換」を意味します。 「 — 」文字列は、多くの場合、C（チェーン）フラグと組み合わせて使用すると便利です。 置換が発生する前に、URLを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
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
   <td colname="col2"> <p> 次のラウンド。 </p> <p>（元のURLではなく）最後の書き換えルールのURLを使用して、（最初の書き換えルールから再び始める）書き換え処理を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> 次のルールと連結。 </p> <p>このフラグは、現在のルールを次のルールに連結します。次のルールに連結することもできます。 ルールが一致する場合、置換プロセスは通常どおり続行します。 ルールが一致しない場合は、それ以降のチェーン付きルールはすべてスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>大文字と小文字は区別されません。 </p> <p>このフラグは、Patternで大文字と小文字を区別しません。 つまり、パターンが現在のURLと一致する場合、「A-Z」と「a-z」の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは、書き換えエンジンにルールセット内の次の数値ルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nになります。Nはelse節の規則の数です。 (注意：これは'chain|C'フラグとは異なります。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> このフラグは、値VALに設定された環境変数「VAR」を作成します。 VALには、正規式のバックリファレンス（$Nと%N）を含めることができ、これらは展開されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで再参照できます。 このフラグを使用して、URLから情報を取り除き、記憶します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

Store Rewrite RulesとRetrieve Rewrite Rulesは変数の値を共有します。 このため、埋め込みURLを検出して保存する際に、変数に時間の影響を受けるsessionid値を設定できます。 一時ストレージリストから次のURLを取得する場合、そのページを取得する前に、最新のsessionid値をそのURLに追加できます。

**例**

大文字と小文字が区別されるサーバーがあるとします。 文字列「www.mydomain.com」と「www.MyDomain.com」の処理方法が異なります。 サーバーが正しく動作するようにするには、「www.MyDomain.com」を参照するリンクが一部のドキュメントに含まれていても、ドメインが常に「www.mydomain.com」であることを確認する必要があります。 これを行うには、次のルールを使用します。

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

この書き換えルールでは、関数「tolower」を使用してURLのドメイン部分を書き換え、常に小文字になるようにします。

1. パターン`(^https://([^/]*)(.*)$)`には、URLの「https://」と最初の「/」の間のすべての文字と一致する後方参照&#x200B;**`([^/]*)`**&#x200B;が含まれています。 パターンには、2番目の後方参照&#x200B;**(も含まれます。*)**&#x200B;は、URLの残りのすべての文字と一致します。

1. 置換`(https://${tolower:$1}$2)`は、最初のバックリファレンス`(https://**${tolower:$1**}$2)`で&#x200B;**tolower**&#x200B;関数を使用し、残りのURLを`(https://${tolower:$1}*$2*)`に残してURLを書き換えるよう検索エンジンに指示します。

したがって、`https://www.MyDomain.com/INTRO/index.Html`形式のURLは`https://www.mydomain.com/INTRO/index.Html`に書き換えられます

**RewriteCondディレクティブ** （オプション）

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleの前にある場合、そのルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

再書き込み条件ディレクティブは、次の形式を取ります。

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

** TestStringは次の構成要素を含む文字列です。

テキスト：変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* ** RewriteRule Backreferences**対応するRewriteRuleパターン内のこれらの一致するバックリファレンスは$N (0 &lt;= N &lt;= 9)の形式をとります。 例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** Backreferencesこれらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0)  &lt;>

変数これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を示す文字列にすることができます。 変数の設定について詳しくは、RewriteRule *`[E]`*&#x200B;フラグを参照してください。

>[!NOTE]
>
>書き換えルールは、通常、変数を使用します。 現在のURLのすべてのCGIパラメーターは、自動的に変数に変換されます。 例えば、検索URL `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"`は自動的に4つの変数を提供し、これを書き換えルールで参照できます。 この例では、1つの変数を「session」、その値を「1234」、別の変数を「id」、値を「5678」と呼びます。 （他の2つの変数は`sp_a`と`sp_q`です）。 必要な変数はすべて、Webページの検索フォームから非表示フィールドとして渡す必要があります。 この例では、検索を実行するウェブサイトユーザを識別する「session」値と「id」値を渡す必要があります。 検索フォームで非表示のフィールドを渡すには、`<input type=hidden name="session" value="1234">`のようなタグを使用します。

関数これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escape URLは、*key*&#x200B;内のすべての文字をエンコードします。 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、「*」、「 — 」、「。」、「/」、「@」、「_」は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」をスペースに戻し、すべての%xx URLをエンコードして文字を1文字に戻します。

**CondPatternは標準の拡張正規式で、いくつか追加されています。** パターン文字列の先頭には「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規式文字列の代わりに、次の特別な変数の1つを使用できます。

感嘆符(&#39;!&#39;)を使用すると、これらのテストのすべてのプレフィックスを付けることができます 彼らの意味を打ち消す

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
   <td colname="col2"> <p>辞書式的に少ない。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>より小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書形式的に大きい。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式順で<i>CondPattern</i>より大きい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>と等しい場合はtrueです。 つまり、2つの文字列は完全に等しい（文字単位）です。 <i>CondPattern</i>が単なる""（2つの引用符）の場合、<i>TestString</i>と空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切ります。

&#39;nocase|NC&#39; （大文字と小文字を区別しない）:これにより、テストでは大文字と小文字が区別されなくなります。 つまり、拡張された&#x200B;*TestString*&#x200B;内と&#x200B;*CondPattern*&#x200B;内の両方において、&#39;A-Z&#39;と&#39;a-z&#39;の間に違いはありません。

&#39;ornext|OR&#39;（または次の条件）:これは、ルール条件を、暗黙的なANDの代わりに、ローカルのORと組み合わせる場合に使用します。 このフラグがないと、条件/規則を複数回書き込む必要があります。

**例**

一部のWebページでは、顧客が初めてサイトに来訪したときに「sessionid」CGI変数が割り当てられます。 この変数は、顧客を識別するために使用され、顧客がサイトを閲覧する際に変数が渡されます。 検索ロボットはサイトの顧客のように見えるので、「sessionid」番号が割り当てられます。 検索ロボットは、2番目のサイトページが新しい値を割り当てようとしても、この「sessionid」値を1つ維持します。 これを確実に行うには、次の書き換えルールが必要です。

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

RewriteRule Patternには、2つのバックリファレンスが含まれています。(.+) および (.*) となります。最初の逆参照は、&quot;sessionid=&quot;より前のすべての文字と一致します。 2番目のバックリファレンスは、セッションIDの終了文字である「&amp;」または「#」以降のすべての文字と一致します。

置換パターンは、最初のバックリファレンスを使用してURLを書き換え、次に文字列「sessionid=」を記述し、続いてURLのCGIパラメーターとして渡されたセッションID変数の値を記述し、続いて2番目のバックリファレンスを記述します。`($1sessionid=%{sessionid}$2)`.

**RewriteCond**&#x200B;は、変数のセッションID `(%{sessionid})`を調べます。 文字(.+)の場合、RewriteRuleは一致と見なされます。

したがって、検索クエリが`"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`の場合、検索結果URLはすべて書き換えられ、検索ロボットがサイトをクロールしてリンクを保存した際に検出した「sessionid」値ではなく、「sessionid」値が「5678」になります。

**確認**

再書き込みエンジンソフトウェアは、元々Apache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようになりました。

## 検索URLルールの追加{#task_50C77D1B53804AEEB20896F74265BD6F}

検索URLルールを追加して、Webサイト検索結果内のURLの表示方法を指定できます。 ルールは、完全なURLに対して機能します。 セッションID情報が頻繁に保持されるクエリ引数など、URLの任意の部分を操作できます。

<!-- 

t_adding_search_url_rules.xml

 -->

**検索URLルールを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Rewrite Rules]**/**[!UICONTROL Search URL Rules]**&#x200B;をクリックします。
1. [!DNL Search URL Rules]フィールドに、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。
1. （オプション）[!DNL Search URL Rules]ページの[!DNL Test Search URL Rules]フィールドに、クロールルールをテストするテストURLを入力し、**「テスト**」をクリックします。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Search URL Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 検索タイトルルールについて{#concept_C72D20F8DFF64EDE809AF4B72797E858}

検索タイトルルールは、Webサイト検索結果内のタイトルの表示方法を指定します。 タイトルの任意の部分を操作できます。

<!-- 

c_about_search_title_rules.xml

 -->

再書き込みルールは、組織名など、タイトルの一部を削除する場合に使用します。 デフォルトでは、サイト検索/マーチャンダイジングにはタイトルルールがなく、タイトルを変更する必要はありません。

タイトルルールは、次の2つの主要な要素で構成できます。rewriteRuleおよびオプションのRewriteCond。 ルールと条件は無制限に指定できます。 ルールセットはルールごとにループされるので、これらのルールの順序は重要です。 ルールが一致すると、ソフトウェアは対応する書き換え条件をループ処理します（オプション）。 検索タイトルルールは、次の方法で指定します。

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

タイトルが見つかると、サイト検索/マーチャンダイジングは、それを各クロールルールのパターンと一致させようとします。 パターンが一致する場合、書き換えエンジンは対応するRewriteCondディレクティブを探します。 条件が存在しない場合、タイトルは置換文字列から構成される新しい値で置き換えられ、ルールセット内の次のルールに続きます。 条件が存在する場合は、リストに表示された順に処理されます。 再書き込みエンジンは、条件パターン(CondPattern)とテスト文字列(TestString)とを照合しようとします。 2つの一致が見つかった場合は、それ以上条件がなくなるまで、次の条件が処理されます。 すべての条件が一致する場合、URLはルールで指定された置換に置き換えられます。 条件が満たされない場合、条件の完全なセットと対応するルールは失敗します。

## RewriteRuleディレクティブ{#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

各RewriteRuleディレクティブは、1つの書き換え規則を定義します。 ルールは、リストに表示されている順序で適用されます。 書き換えルールは次の形式を取ります。

```
RewriteRule Pattern Substitution [Flags]
```

**** Pattern現在のタイトルに適用されるPOSIX正規式。「現在のタイトル」は、以前のルールで既に一致し変更されている場合があるので、元のタイトルと異なる場合があります。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

「not」文字(&#39;!&#39;)を使用できます。 を追加します。 「not」文字を使用すると、パターンを無効にできます。 つまり、現在のタイトルがパターンと一致しない場合にのみtrueに設定します。 「not」文字は、除外パターンに一致した方がよい場合や、最終的なデフォルトのルールとして使用できます。 注意：パターンでは、「not」文字とグループ化されたワイルドカードの両方を使用できません。 また、置換文字列に$Nが含まれる場合は、無効なパターンを使用することはできません。

逆参照は、SubstitutionやCondPatternで参照できる逆参照を作成する場合に使用できます。

**** 置換タイトルは、次の文字列を含む置換文字列に完全に置換されます。

プレーンテキスト — 変更せずに渡されるテキスト。

**バ** ックリファレンスパターンまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。次に、2種類のバックリファレンスを示します。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** RewriteCond Backreferences**一致する最後に一致したRewriteCondPattern内のバックリファレンスに一致し、%Nの形式をとります(0 &lt;= N &lt;= 9)。

**** 変数これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列にすることができます。環境変数の設定について詳しくは、[E]フラグを参照してください。 変数は、検索結果を生成した検索フォームでも定義できます。

**関** 数次に、${NAME_OF_FUNCTIONの形式の関数を示します。key} NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。

次に、特殊な置換文字列を示します。「 — 」は「NO置換」を意味します。 「 — 」文字列は、C（チェーン）フラグと組み合わせて使用すると便利で、置換が発生する前にタイトルを複数のパターンに一致させることができます。

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切ります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> 最後のルール。 </p> <p> 書き換え処理を停止し、追加の書き換え規則を適用しない。 このフラグを使用すると、現在のタイトルがそれ以上処理されなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>次のラウンド。 </p> <p> （元のタイトルではなく）最後の書き換えルールのタイトルを使用して（最初の書き換えルールから再び開始）、書き換え処理を再実行します。 デッドループを作成しないように注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>次のルールと連結。 </p> <p> このフラグは、現在のルールを次のルールに連結します（次のルールに連結することもできます）。 ルールが一致する場合、置換プロセスは通常どおり続行します。 ルールが一致しない場合は、それ以降のチェーン付きルールはすべてスキップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> 大文字と小文字は区別されません。 </p> <p> このフラグは、Patternで大文字と小文字を区別しません。 つまり、パターンが現在のタイトルと一致する場合、「A-Z」と「a-z」の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p> 次のルールをスキップします。 </p> <p> 現在のルールが一致する場合、このフラグは、書き換えエンジンにルールセット内の次の数値ルールをスキップさせます。 これを使用して、擬似if-then-else構成を作成します。 then節の最後の規則はskip=Nになります。Nはelse節の規則の数です。 （これは'chain|C'フラグとは異なります。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>環境変数を設定します。 </p> <p> このフラグは、値VALに設定された環境変数"VAR"を作成します。VALには、正規式のバックリファレンス（$Nと%N）を含めることができ、これは拡張されます。 このフラグを複数回使用して、複数の変数を設定できます。 変数は、後で%{VAR}を介して次のRewriteCondパターンで参照できます。 タイトルの情報を削除して記憶するには、このフラグを使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCondディレクティブ（オプション） {#section_9D72B2AB454849A7B681BC39C506AAA3}

RewriteCondディレクティブは、ルール条件を定義します。 RewriteCondがRewriteRuleの前にある場合、そのルールは、そのパターンが現在のタイトルと一致し、追加の条件が適用された場合にのみ使用されます。

再書き込み条件ディレクティブは、次の形式を取ります。

```
RewriteCond TestString CondPattern [Flags]
```

**TestStringは次の** 構成要素を含む文字列です。

プレーンテキスト — 変更せずに渡されるテキスト。

バックリファレンスは、PatternまたはCondPatternのグループ化されたパーツ（括弧内）にアクセスできます。 バックリファレンスには次の2種類があります。

* **RewriteRule** Backreferences対応するRewriteRuleパターンのバックリファレンスと一致し、$N (0  &lt;>例：`RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** Backreferencesこれらの一致するバックリファレンスは、最後に一致したRewriteCondPattern内にあり、%Nの形式をとります(0)  &lt;>

**** 変数これらは%{NAME_OF_VARIABLE}の形式の変数です。NAME_OF_VARIABLEは、定義された変数の名前を表す文字列にすることができます。環境変数の設定について詳しくは、`[E]`フラグを参照してください。 変数は、検索結果を生成した検索フォームでも定義できます。

**関** 数これらは${NAME_OF_FUNCTION:key}の形式の関数です。NAME_OF_FUNCTIONは次のとおりです。

* tolowerは、*key*&#x200B;内のすべての文字を小文字にします。
* toupperは、*key*&#x200B;の文字をすべて大文字にします。
* escape URLは、*key*&#x200B;内のすべての文字をエンコードします。
* 「a」。.z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;...&#39;9&#39;、「*」、「 — 」、「。」、「/」、「@」、「_」は変更されません。スペースは「+」に変換され、その他のすべての文字は、%xx URLエンコードされた等価な文字に変換されます。
* 「+」を空白に戻し、すべての%xx個のURLエンコードされた文字を1文字に戻します。

次に、特殊な置換文字列を示します。「 — 」は「NO置換」を意味します。 「 — 」文字列はC（チェーン）フラグと組み合わせて使用すると便利で、置換が発生する前にURLを複数のパターンに一致させることができます。

**CondPattern標準の拡張正規式で、いくつか追加されています。** パターン文字列の先頭には「!」を付けることができます。 文字（感嘆符）を使用して、一致しないパターンを指定します。 実際の正規式文字列の代わりに、次の特別な変数の1つを使用できます。

これらのテストのすべてには、感嘆符(&#39;!&#39;)の前に付けることもできます 彼らの意味を打ち消す

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
   <td colname="col2"> <p>辞書式的に少ない。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>より小さい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> 辞書形式的に大きい。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式順で<i>CondPattern</i>より大きい場合はtrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>辞書式的に等しい。 </p> <p> <i>CondPattern</i>をプレーン文字列として扱い、辞書式順に<i>TestString</i>と比較します。 <i>TestString</i>が辞書式的に<i>CondPattern</i>と等しい場合はtrueです。 つまり、2つの文字列は完全に等しい（文字単位）です。 <i>CondPattern</i>が単なる""（2つの引用符）の場合、<i>TestString</i>と空の文字列が比較されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**フラグ** （オプション）

フラグは角括弧`[]`で囲み、複数のフラグはコンマで区切って指定します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>フラグ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' （大文字と小文字を区別しない） </p> </td> 
   <td colname="col2"> <p>テストを無感度にします。 つまり、拡張された<i>TestString</i>内と<i>CondPattern</i>内の両方において、'A-Z'と'a-z'の間に違いはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR'（または次の条件） </p> </td> 
   <td colname="col2"> <p> これは、ルール条件を、暗黙的なANDの代わりに、ローカルのORと組み合わせる場合に使用します。 このフラグがないと、条件/規則を複数回書き込む必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section_E7454FFE169E459AABD9D033651939CB}

標準的なタイトル形式を持つ会社のウェブサイトがあるとします。「マイ会社」の後にハイフンが続き、ページ固有の説明(例：「マイ会社 — ようこそ」、「マイ会社 — ニュース」)が続きます。 タイトルから「マイ会社 — 」を除去し、サイトのインデックスを作成する際に、タイトル全体を大文字に変換する必要がある。

次の再書き込みルールは、関数toupperを使用して、タイトルの説明部分のみを大文字に書き換えます。

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

ルールのパターン`(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))`には、「My会社 — 」に続くタイトルコンテンツに一致する後方参照&#x200B;**`(.*)`**&#x200B;が含まれています。 パターンの一部を括弧( )で囲むと、代替(Substitution)で参照可能な逆参照が作成されることに注意してください。 この例では、置換(${toupper:**$1**})は、toupper関数を使用してバックリファレンス(**$1**)を書き換えます。

したがって、「マイ会社 — ようこそ」という形式のタイトルは、「ようこそ」と書き換えられます。

**確認**

再書き込みエンジンソフトウェアは、元々Apache Groupが開発し、Apache HTTPサーバープロジェクト(https://www.apache.org/)で使用するようになりました。

## 検索タイトルルールの追加{#task_155CECB74BE3444384EDBBD04F41515E}

検索タイトルルールを追加して、Webサイトの検索結果に表示するタイトルを指定できます。 タイトルの任意の部分を操作できます。

<!-- 

t_adding_search_title_rules.xml

 -->

**検索タイトルルールを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Rewrite Rules]**/**[!UICONTROL Search Title Rules]**&#x200B;をクリックします。
1. [!DNL Search Title Rules]フィールドに、必要なルールを入力します。

   空白行と、「#」（ハッシュ）文字で始まるコメント行が使用できます。
1. （オプション）[!DNL Search Title Rules]ページの[!DNL Test Search Title Rules]フィールドにテストタイトルを入力し、「**テスト**」をクリックします。
1. 「**変更を保存**」をクリックします。
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Search Title Rules]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

