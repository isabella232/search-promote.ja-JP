---
description: フィルタリングメニューを使用して、Webドキュメントのインデックスが作成される前にそのコンテンツを変更するスクリプトを使用します。
seo-description: フィルタリングメニューを使用して、Webドキュメントのインデックスが作成される前にそのコンテンツを変更するスクリプトを使用します。
seo-title: フィルタリングメニューについて
solution: Target
subtopic: Filtering
title: フィルタリングメニューについて
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# フィルタリングメニューについて{#about-the-filtering-menu}

フィルタリングメニューを使用して、Webドキュメントのインデックスが作成される前にそのコンテンツを変更するスクリプトを使用します。

## フィルタリングスクリプトについて {#concept_E56B73D625854AB2A899EF2D56CFCB47}

を使用して、Webドキ [!DNL Filtering Script] ュメントのインデックスが作成される前に、Webドキュメントのコンテンツを変更できます。

HTMLタグの挿入、無関係なコンテンツの削除、ドキュメントのURL、MIMEタイプ、既存のコンテンツに基づく新しいHTMLメタデータの作成を行うこともできます。 フィルタリングスクリプトはPerlスクリプトで、強力な文字列処理と柔軟な正規表現の一致を提供します。 フィルタリングスクリプトは、初期化スクリプト、終了スクリプト、URLマスクスクリプトおよびテストURLと共に使用します。

フィルタリングスクリプトは、Webサイトからドキュメントが読み取られるたびに実行されます。 スクリプトは標準フィルタとして実行されます。つまり、STDINからデータを読み取り、そのデータを何らかの方法で変換し、結果をSTDOUTに書き込みます。 フィルタリングスクリプトを使用して、フィルタリングスクリプトからインデックスログにステータスメッセージを印刷できます。 STDERRにメッセージを出力するか、サブルーチンを使用し `_search_debug_log()` ます。

ステージングされたフィルタリングスクリプトページのモード **[!UICONTROL Expert (diff)]** で使用できるGNU diffオプションの一部は、以下を含みます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diffオプション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> 空白の量の変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C行 </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示するコンテキスト出力形式を使用します。行が指定されていない場合は3行を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の変更を無視する。大文字と小文字を同等にすることを考慮してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイルに表示される順序が変更された出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。-fと同 <span class="codeph"> 様ですが、 </span> 各コマンドは影響を受ける行の数を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 3行のコンテキストを表示し、統合出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U行 </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行が指定されていない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数、またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」の前に置かれます。 フィルタリングスクリプトを起動すると、その環境には次の標準ファイルハンドルが含まれます。

* STDIN — 何も返さない（読み込み時に即座にEOFを返す）
* STDOUT — 置換HTML（データがSTDOUTに出力される場合は、元のドキュメントの代わりに使用されます）
* STDERR - STDERRに出力されるデータは、エラーとしてインデックス・ログに出力される

また、次の例のように、サブルーチンを使用してインデックスログにカ `_search_debug_log()` スタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文とし `DEBUG` て単語と共に表示され、エラーとして記録されません。

次に、フィルターの例を示します。 Webページのフィ `<title>` ールドは、多くの場合、会社名で始まります。 この情報はサイトのナビゲーションの目的で役立ちますが、検索時には関係ありません。 すべてのMegaCorp Webページのタイトルが、次のような共通の文字列で始まる場合：

```
<title>MegaCorp -- meaningful title 
here</title>
```

各ドキュメントタイトルの先 `MegaCorp --`頭から「」を削除し、フィルタリングスクリプトで処理された各ドキュメントをカウントする必要があります。 これを行うには、次のスクリプトを使用します。

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## グローバル変数 {#global-variables}

フィルタースクリプトでは、次の変数を使用できます。

| 変数 | 説明 |
|--- |--- |
| `$main::search_crawl_type` | の値は、進行中の `$main::search_crawl_type` インデックス操作の種類を示します。  廃止されたフォーム：インデッ `$main::ws_crawl_type` クス操作と関連する値には、次のものがあります。 <ul><li>インデックス全体：手動 — `manual`</li><li>インデックス全体：スケジュール済み — `auto`</li><li>インデックス全体：リモートコントロール — `CGI`</li><li>インデックスの増分：手動 — `manual-incremental`</li><li>インデックスの増分：スケジュール済み — `auto-incremental` </li><li>インデックスの増分：リモートコントロール — `CGI-incremental`</li><li>スクリプト化インデックス：手動 — `manual-indexlist.txt` </li><li>スクリプト化インデックス：スケジュール済み — `auto-indexlist.txt`</li><li>スクリプト化インデックス：リモートコントロール — `CGI-indexlist.txt`</li><li>再生成 — `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | この値は、現在のインデックス操作に対して「インデックスキャッシュをクリア」インデックスオプションが要求されたかどうかを示します。 「インデックスキャッシュのクリア」が要求された場合、の値 `$main::search_clear_cache` は「」にな `1`ります。  廃止された形式：`$main::ws_clear_cache` |
| `$main::search_fields` | この値には、アカウントで定義されたメタデータフィールドのタブ区切りリストが含まれます。 デフォルトでは、次の値が設定されます。  非推 `url title desc keys target body alt date charset language` 奨フォーム： `$main::ws_fields` |
| `$main::search_collections` | この値には、アカウントで定義されたコレクションのタブ区切りリストが含まれます。  廃止された形式：`$main::ws_collections` |
| `$main::search_url` | 値はドキュメントの完全修飾URLです。  廃止された形式：`$main::ws_url` |
| `$main::search_content_type` | この値は、http-equivメタタグから取得したドキュメントのコンテンツタイプです。 一般的な値は「text/html;charset=iso-8859-1&quot;  廃止された形式：`$main::ws_content_type` |
| `$main::search_content_class` | 値は、content-typeフィールドから派生する、ドキュメントのコンテンツクラスです。  廃止された形式：`$main::ws_content_class` |
| `$main::search_syntax_check` | この値は、「構文をチェック」ボタンの使用を反映しています。 クリックした場合、値は1(1)です。それ以外の場合、値は0（ゼロ）です。  廃止された形式：`$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Webサーバーによって提供される場合、この値には、ドキュメントの最終変更日のエポック表現（1970年1月1日からの秒数）が含まれます。  この値は、Perlのlocaltime()ライブラリ呼び出しを使用してフォーマットできます。 |

### クイックヒント {#section_89A5C16911744AF98E232DF608C6A1F5}

* すべてのグローバル変数は、名前空間「main::」で始まります。 `$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。 `my $i = 0;`
* サブルーチンは、初期化スクリプトで定義されます。 明示的な「main::」名前空間は必要ありません。 `sub my_sub {`  `...`

   `}`

* ファイルを変 `$main::search_content_type` 更する前に、をテストします。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* は、サ `$main::search_content_type` ーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプに続けて、ドキュメントの文字セットエンコーディング(「text/html;charset=iso-8859-1&quot;
* HTML以外のドキュメントのタイプごとに、様々な値 `$main::search_content_type` を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプ値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、は次の `$main::search_content_class` 値を取ることができます。

   * html
   * pdf
   * 単語
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」 `$main::search_content_class` のテストは、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の手順を実行します。 `print "<html></html>";`

## フィルタリングスクリプトの追加 {#task_0AB84FD1133F47F9AA069A79BEA13A22}

フィルタリングスクリプトは、Webサイトからダウンロードされた各ドキュメントに対して実行されるPerlスクリプトです。

フィルタリングスクリプトは、初期化スクリプト、終了スクリプト、URLマスクスクリプトと組み合わせて使用します。

フィルタリングスクリプトの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**フィルタリングスクリプトを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Filtering]** ます **[!UICONTROL Filtering Script]**。
1. （オプション）ページの [!DNL Filtering Script] フィールドに、Webサ [!DNL Test URL] イト上のドキュメントのURLを入力します。

   生のHTMLテキストの変更を表示するには、テストオプションをクリックします。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>テストURLフィールド </p> </td> 
      <td colname="col2"> <p>Webサイト上のドキュメントのURLを入力できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テスト </p> </td> 
      <td colname="col2"> <p>URLをフィルタリングスクリプトおよびURLマスクと比較してテストします。 </p> <p>テストURLドキュメントがダウンロードされ、フィルタリングスクリプトへのSTDIN入力として使用されます。 その後、初期化、フィルタリング、および終了スクリプトが実行されます。 フィルタリングスクリプトからのSTDOUT出力がある場合、その出力は新しいブラウザウィンドウに表示されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>テストのみ </p> </td> 
      <td colname="col2"> <p>スクリプトの操作のみをテストします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プレビュー </p> </td> 
      <td colname="col2"> <p>ページを表示できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フルビジュアル </p> </td> 
      <td colname="col2"> <p>ドキュメントの前後の完全なテーブルビューを生成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ショートビジュアル </p> </td> 
      <td colname="col2"> <p>前後のビューの違いのみを表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エキスパート（相違） </p> </td> 
      <td colname="col2"> <p>提供されたコマンドラインオプションを使用して、ファイルの比較に使用されるGNU diffコマンドの生の出力を表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィルタリングスクリプト </p> </td> 
      <td colname="col2"> <p>提供されたフィールドにフィルタリングスクリプトを貼り付けます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>変更の保存 </p> </td> 
      <td colname="col2"> <p>フィルタリングスクリプトを保存します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>構文の確認 </p> </td> 
      <td colname="col2"> <p>初期化、フィルタリング、終了の各スクリプトを実行して、スクリプトの構文を簡単に確認できます。 スクリプトは更新されず、保存されません。 </p> <p>Perlコンパイラのエラーや警告、STDERRの出力がすべて印刷されます。 </p> <p>スクリプトの効果が顧客に表示される前に、サイトインデックスを再構築する必要があります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **GNU diffコマンドラインオプション**

   ステージングされたフィルタリングスクリプトページのモード **[!UICONTROL Expert (diff)]** で使用できるGNU diffオプションの一部は、以下を含みます。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>GNU diffコマンドラインオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
      <td colname="col2"> <p> 空白の量の変更を無視します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
      <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
      <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C行 </span> </p> </td> 
      <td colname="col2"> <p> コンテキストの行（整数）を表示するコンテキスト出力形式を使用します。行が指定されていない場合は3行を表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
      <td colname="col2"> <p> 大文字と小文字の変更を無視する。大文字と小文字を同等にすることを考慮してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
      <td colname="col2"> <p> edスクリプトに似ているが、ファイルに表示される順序が変更された出力を作成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
      <td colname="col2"> <p> RCS形式のdiffを出力します。-fと同 <span class="codeph"> 様ですが、 </span> 各コマンドは影響を受ける行の数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> 3行のコンテキストを表示し、統合出力形式を使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U行 </span> </p> </td> 
      <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行が指定されていない場合は3を表示します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. をクリック **[!UICONTROL Test]** して、フィルタリングスクリプトとURLマスクに対するテストを行います。

   をクリック **[!UICONTROL Test]** しても、フィルタリングスクリプトは更新および保存されません。
1. フィールドにス [!DNL Filtering Script] クリプトを貼り付けます。
1. （オプション）をクリッ **[!UICONTROL Check Syntax]** クして、フィルタリング、初期化、終了の各スクリプトを実行し、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** が更新されず、スクリプトが保存されません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Filtering Script] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 初期化スクリプトについて {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

を使用して、Webドキ [!DNL Initialization Script] ュメントのインデックスが作成される前に、Webドキュメントのコンテンツを変更できます。

HTMLタグの挿入、無関係なコンテンツの削除、ドキュメントのURL、MIMEタイプ、既存のコンテンツに基づく新しいHTMLメタデータの作成を行うこともできます。 初期化スクリプトはPerlスクリプトで、強力な文字列処理と柔軟な正規表現のマッチングを提供します。 初期化スクリプトは、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプト、およびテストURLと共に使用します。

初期化スクリプトは、インデックス作成を開始する前に1回実行されます。 このスクリプトを使用して、フィルタリングスクリプトで使用するグローバル変数とサブルーチンを初期化します。 初期化スクリプトを使用して、フィルタリングスクリプトからインデックスログにステータスメッセージを出力できます。 メッセージをSTDERRに出力するか、サブルーチンを使用して出力し `_search_debug_log()` ます。

Staged Initialization Scriptページのモードで使用できるGNU **[!UICONTROL Expert (diff)]** diffオプションの一部は、次のようになります。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diffオプション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> 空白の量の変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C行 </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示するコンテキスト出力形式を使用します。行が指定されていない場合は3行を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の変更を無視する。大文字と小文字を同等にすることを考慮してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイルに表示される順序が変更された出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。-fと同 <span class="codeph"> 様ですが、 </span> 各コマンドは影響を受ける行の数を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 3行のコンテキストを表示し、統合出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U行 </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行が指定されていない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数、またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」の前に置かれます。 初期化スクリプトを起動すると、その環境には次の標準ファイル・ハンドルが含まれます。

* STDIN — 何も返さない（読み込み時に即座にEOFを返す）
* STDOUT — 何も出力されません（データがSTDOUTに出力される場合、破棄されます）
* STDERR - STDERRに出力されるデータは、エラーとしてインデックス・ログに出力される

また、次の例のように、サブルーチンを使用してインデックスログにカ `_search_debug_log()` スタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文とし `DEBUG` て単語と共に表示され、エラーとして記録されません。

初期化スクリプトの例を次に示します。

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

「グローバル [変数」を参照](#global-variables)

### クイックヒント {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* すべてのグローバル変数は、名前空間「main::」で始まります。 `$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。 `my $i = 0;`
* サブルーチンは、初期化スクリプトで定義されます。 明示的な「main::」名前空間は必要ありません。 `sub my_sub {`  `...`

   `}`

* ファイルを変 `$main::search_content_type` 更する前に、をテストします。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* は、サ `$main::search_content_type` ーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプに続けて、ドキュメントの文字セットエンコーディング(「text/html;charset=iso-8859-1&quot;
* HTML以外のドキュメントのタイプごとに、様々な値 `$main::search_content_type` を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプ値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、は次の `$main::search_content_class` 値を取ることができます。

   * html
   * pdf
   * 単語
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」 `$main::search_content_class` のテストは、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の手順を実行します。 `print "<html></html>";`

## 初期化スクリプトの追加 {#task_5A03B8D0C46E4674B7CE88203515803B}

初期化スクリプトは、ドキュメントのインデックスが作成される前に1回だけ実行されるPerlスクリプトです。

初期化スクリプトは、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプトと組み合わせて使用します。

初期化スクリプトの結果が顧客に表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**初期化スクリプトを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Filtering]** ます **[!UICONTROL Initialization Script]**。
1. （オプション）ページの [!DNL Initialization Script] フィールドに、Webサ [!DNL Test URL] イト上のドキュメントのURLを入力します。

   生のHTMLテキストの変更を表示するには、テストオプションをクリックします。

   「フィルタリングスクリプトの追加」のフィルタリ **ングオプションの表を参照してくださ**&#x200B;い。

   をクリック **[!UICONTROL Test]** して、フィルタリングスクリプトとURLマスクに対するテストを行います。

   をクリック **[!UICONTROL Test]** しても、初期化スクリプトは更新されず、保存されません。
1. フィールドにス [!DNL Initialization Script] クリプトを貼り付けます。
1. （オプション）をクリッ **[!UICONTROL Check Syntax]** クして、フィルタリング、初期化、終了の各スクリプトを実行し、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** が更新されず、スクリプトが保存されません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Initialization Script] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 終了スクリプトについて {#concept_AAD6B3B0E7124874AD0947096FC42F47}

を使用して、Webドキ [!DNL Termination Script] ュメントのインデックスが作成される前に、Webドキュメントのコンテンツを変更できます。

HTMLタグの挿入、無関係なコンテンツの削除、ドキュメントのURL、MIMEタイプ、既存のコンテンツに基づく新しいHTMLメタデータの作成を行うこともできます。 初期化スクリプトはPerlスクリプトで、強力な文字列処理と柔軟な正規表現のマッチングを提供します。 終了スクリプトは、初期化スクリプト、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプト、およびテストURLで使用します。

終了スクリプトは、すべてのドキュメントのインデックスが作成された後に1回実行されます。 終了スクリプトを使用して、フィルタリングスクリプトからインデックスログにステータスメッセージを印刷できます。 メッセージをSTDERRに出力するか、サブルーチンを使用して出力し `_search_debug_log()` ます。

Staged Termination Scriptページのモード中に使用できるGNU **[!UICONTROL Expert (diff)]** diffコマンドラインオプションの一部は、以下を含みます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diffコマンドラインオプション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> 空白の量の変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C行 </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示するコンテキスト出力形式を使用します。行が指定されていない場合は3行を表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の変更を無視する。大文字と小文字を同等にすることを考慮してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイルに表示される順序が変更された出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。-fと同 <span class="codeph"> 様ですが、 </span> 各コマンドは影響を受ける行の数を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 3行のコンテキストを表示し、統合出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U行 </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行が指定されていない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数、またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」の前に置かれます。 終了スクリプトを起動すると、その環境には次の標準ファイルハンドルが含まれます。

* STDIN — 何も返さない（読み込み時に即座にEOFを返す）
* STDOUT — 何も出力されません（データがSTDOUTに出力される場合、破棄されます）
* STDERR - STDERRに出力されたデータは、エラーとしてインデックス・ログに出力されます。

また、次の例のように、サブルーチンを使用してインデックスログにカ `_search_debug_log()` スタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文とし `DEBUG` て単語と共に表示され、エラーとして記録されません。

フィルタリングスクリプトによって処理されたドキュメントの数をインデックスログのエラー行として表示するには、次の終了スクリプトを使用します。

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

「グローバル [変数」を参照](#global-variables)

### クイックヒント {#section_5790EA7ACAC046CBA01F759F88E2460F}

* すべてのグローバル変数は、名前空間「main::」で始まります。 `$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。 `my $i = 0;`
* サブルーチンは、初期化スクリプトで定義されます。 明示的な「main::」名前空間は必要ありません。 `sub my_sub {`  `...`

   `}`

* ファイルを変 `$main::search_content_type` 更する前に、をテストします。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* は、サ `$main::search_content_type` ーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプに続けて、ドキュメントの文字セットエンコーディング(「text/html;charset=iso-8859-1&quot;
* HTML以外のドキュメントのタイプごとに、様々な値 `$main::search_content_type` を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプ値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、は次の `$main::search_content_class` 値を取ることができます。

   * html
   * pdf
   * 単語
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」 `$main::search_content_class` のテストは、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の手順を実行します。 `print "<html></html>";`

## 終了スクリプトの追加 {#task_F0CFB412871642CFBC88132889C5B6F9}

終了スクリプトは、すべてのドキュメントのインデックスが作成された後に1回実行されるPerlスクリプトです。

終了スクリプトは、フィルタリングスクリプト、終了スクリプト、およびURLマスクスクリプトと組み合わせて使用します。

初期化スクリプトの結果が顧客に表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**終了スクリプトを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Filtering]** ます **[!UICONTROL Termination Script]**。
1. （オプション）ページの [!DNL Termination Script] フィールドに、Webサ [!DNL Test URL] イト上のドキュメントのURLを入力します。

   生のHTMLテキストの変更を表示するには、テストオプションをクリックします。

   フィルタリングスクリプトの追加のフィルタリングオプ **ションの表を参照してくださ**&#x200B;い。

   をクリック **[!UICONTROL Test]** して、フィルタリングスクリプトとURLマスクに対するテストを行います。

   をクリック **[!UICONTROL Test]** しても、終了スクリプトは更新されず、保存されません。
1. フィールドにス [!DNL Termination Script] クリプトを貼り付けます。
1. （オプション）をクリッ **[!UICONTROL Check Syntax]** クし、初期化、フィルタリング、終了の各スクリプトを実行して、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** が更新されず、スクリプトが保存されません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Termination Script] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## URLマスクスクリプトについて {#concept_384F32EA18F84853A7BA99A04009330B}

フィルタリングを使用すると、Webドキュメントのインデックスが作成される前に、Webドキュメントのコンテンツを変更できます。 HTMLタグの挿入、無関係なコンテンツの削除、ドキュメントのURL、MIMEタイプ、既存のコンテンツに基づく新しいHTMLメタデータの作成を行うこともできます。 URLマスクスクリプトは、強力な文字列処理と柔軟な正規表現の一致を提供するPerlスクリプトです。

Webサイトの特定の部分にのみ存在するドキュメントのコンテンツを変更するには、URLマスクを含めるか、URLマスクを除外するか、またはその両方を指定して、適切なページを定義します。

のドキュメントのみを変更する場合は、 `"https://www.mysite.com/faqs/"`次のマスクのセットを使用できます。

```
include https://www.mysite.com/faqs/ 
exclude *
```

次の例のように、URLマスクスクリプトで正規表現を使用することもできます。

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

スクリプト化されたURLマスクは、フィールドに入力した順に考慮さ [!DNL URL Masks] れます。 ドキュメントURLがマスクと一致する場合、そのドキュメントはマスクの種類に基づいて含められるか、除外されます。 ドキュメントのURLがURLマスクと一致しない場合、ドキュメントのMIMEタイプが「text/html」の場合にのみドキュメントが含まれます。 その他のMIMEタイプはすべて除外されます。

## URLマスクスクリプトの追加 {#task_D18F2A496C1C45C997B5DA650AAF5D59}

URLにマスクを含めるおよびマスクを除外を指定して、Webサイトの特定の部分にのみ存在するドキュメントのコンテンツを変更します。

URLマスク設定の効果が訪問者に表示される前に、サイトのインデックスを再構築します。

**URLマスクスクリプトを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Filtering]** ます **[!UICONTROL URL Masks]**。
1. （オプション）ページの [!DNL URL Masks] フィールド [!DNL Test URL] に、Webサイト上のドキュメントのURLを入力し、をクリックして、URLをフィルタリングスクリプト **[!UICONTROL Test]** とマスクに対してテストします。

   テストURLドキュメントがダウンロードされ、フィルタリングスクリプトへのSTDIN入力として使用されます。 次に、フィルタリング、初期化、終了の各スクリプトが実行されます。 フィルタリングスクリプトからのSTDOUT出力がある場合、その出力は新しいブラウザウィンドウに表示されます。

   をクリック **[!UICONTROL Test]** しても、スクリプトは更新されず、保存されません。
1. フィールド [!DNL URL Masks] に、1行に1つのURLマスクを入力します。
1. （オプション）をクリ **[!UICONTROL Check Syntax]** ックして、フィルタリング、初期化、終了の各スクリプトを実行して、URLマスクの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** が更新されず、スクリプトが保存されません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL URL Masks] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## フィルタリングのコンテンツタイプについて {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

このアカウントに対してフィルターを適用するコンテンツタイプを選択できます。

選択したコンテンツタイプ内のテキストはHTMLに変換され、「フィルタリングスクリプト」で指定したスクリプトを使用して処理されます。

詳しくは、スク [リプトのフィルタリングについてを参照し](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)。

次のコンテンツタイプから選択できます。

* PDFドキュメント
* テキストドキュメント
* Adobe Flashムービー
* Microsoft Wordファイル
* Microsoft Officeファイル(OpenXML)
* Microsoft Excelファイル
* Microsoft Powerpointファイル
* MP3音楽ファイル内のテキスト

コンテンツタイプの設定や設定の変更がユーザーに表示される前に、サイトインデックスを再構築する必要があります。

## フィルタリングするコンテンツタイプの選択 {#task_C46081FA425A43EC8FDE6EA4A52A170A}

「スクリプトのフィルタリング」で指定したスクリプトに渡すコンテンツタイプを選択します。

詳しくは、スク [リプトのフィルタリングについてを参照し](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)。

**フィルタリングするコンテンツタイプを選択するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Filtering]** ます **[!UICONTROL Content Types]**。
1. ページで、 [!DNL Content Types] フィルタースクリプトに渡すコンテンツタイプを確認します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。
1. （オプション）ページで、 [!DNL Content Types] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。
