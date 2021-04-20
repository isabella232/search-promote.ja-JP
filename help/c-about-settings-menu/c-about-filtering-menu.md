---
description: フィルタリングメニューを使用して、Webドキュメントーのコンテンツを変更してからインデックスを作成するスクリプトを使用します。
solution: Target
subtopic: Filtering
title: フィルタリングメニューについて
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4008'
ht-degree: 1%

---


# フィルタリングメニューについて{#about-the-filtering-menu}

フィルタリングメニューを使用して、Webドキュメントーのコンテンツを変更してからインデックスを作成するスクリプトを使用します。

## フィルタリングスクリプトについて{#concept_E56B73D625854AB2A899EF2D56CFCB47}

[!DNL Filtering Script]を使用すると、Webドキュメントのインデックスを作成する前に、Webコンテンツを変更できます。

ドキュメントのURL、MIMEタイプおよび既存のコンテンツに基づいて、HTMLタグの挿入、無関係なコンテンツの削除、新しいHTMLメタデータの作成を行うこともできます。 フィルタリングスクリプトはPerlスクリプトで、強力な文字列処理と正規式のマッチングの柔軟性を提供します。 フィルタリングスクリプトは、初期化スクリプト、終了スクリプト、URLマスクスクリプト、およびテストURLと共に使用します。

フィルタリングスクリプトは、ドキュメントがWebサイトから読み取られるたびに実行されます。 スクリプトは、標準フィルタとして実行されます。つまり、は、STDINからデータを読み取り、そのデータを何らかの方法で変換し、結果をSTDOUTに書き込みます。 フィルタリングスクリプトを使用すると、フィルタリングスクリプトからインデックスログにステータスメッセージを印刷できます。 メッセージはSTDERRに出力するか、`_search_debug_log()`サブルーチンを使用して出力します。

Staged Filtering Scriptページの&#x200B;**[!UICONTROL Expert (diff)]**&#x200B;モードで使用できるGNU diffオプションの一部は、次のようになります。

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
   <td colname="col2"> <p> 空白の大きさの変更を無視します。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> -C行  </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示する、または行を指定しない場合は3を表示する、コンテキスト出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の違いを無視する大文字と小文字は同じ意味を持ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイル内に表示される順序が変化する出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。<span class="codeph"> -f </span>のように、各コマンドが影響を受ける行の数を指定する点が異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U線  </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行を指定しない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」で始まります。 フィルタリングスクリプトを起動すると、環境に次の標準ファイルハンドルが含まれます。

* STDIN — 何も返さない（読み込み時は直ちにEOFを返す）
* STDOUT - HTMLの置き換え(データがSTDOUTに出力される場合は、元のドキュメントの代わりに使用されます)
* STDERR - STDERRに出力されるデータは、エラーとしてインデックス・ログに出力されます。

また、次の例のように、`_search_debug_log()`サブルーチンを使用して、インデックスログにカスタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文として`DEBUG`という単語で表示され、エラーとして記録されません。

次に、フィルターの例を示します。 Webページ`<title>`のフィールドは、多くの場合、会社名で始まります。 この情報はサイトのナビゲーションの目的に役立ちますが、検索時には関係ありません。 次のように、共通の文字列を含むすべてのMegaCorp Webページ開始のタイトル。

```
<title>MegaCorp -- meaningful title 
here</title>
```

各ドキュメントのタイトルの先頭から「`MegaCorp --`」を削除し、フィルタリングスクリプトで処理された各ドキュメントをカウントする必要があります。 これを行うには、次のスクリプトを使用します。

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

フィルタリングスクリプトでは、次の変数を使用できます。

| 変数 | 説明 |
|--- |--- |
| `$main::search_crawl_type` | `$main::search_crawl_type`の値は、進行中のインデックス操作の種類を示します。  非推奨フォーム：`$main::ws_crawl_type`インデックス操作と関連する値には、次のものがあります。 <ul><li>完全なインデックス：手動 — `manual`</li><li>完全なインデックス：スケジュール済み — `auto`</li><li>完全なインデックス：リモートコントロール — `CGI`</li><li>Incremental Index:手動 — `manual-incremental`</li><li>Incremental Index:スケジュール済み — `auto-incremental` </li><li>Incremental Index:リモートコントロール — `CGI-incremental`</li><li>スクリプトインデックス：手動 — `manual-indexlist.txt` </li><li>スクリプトインデックス：スケジュール済み — `auto-indexlist.txt`</li><li>スクリプトインデックス：リモートコントロール — `CGI-indexlist.txt`</li><li>再生成 - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | この値は、現在のインデックス操作に対して「インデックスキャッシュをクリア」インデックスオプションが要求されたかどうかを示します。 &quot;Clear index cache&quot;が要求された場合、`$main::search_clear_cache`の値は&quot; `1`&quot;です。  廃止された形式：`$main::ws_clear_cache` |
| `$main::search_fields` | この値には、アカウントで定義されているメタデータフィールドのタブ区切りリストが含まれます。 デフォルト値は次のとおりです。   `url title desc keys target body alt date charset language`非推奨フォーム：`$main::ws_fields` |
| `$main::search_collections` | 値には、アカウントで定義されているコレクションのタブ区切りリストが含まれます。  廃止された形式：`$main::ws_collections` |
| `$main::search_url` | 値は、ドキュメントの完全修飾URLです。  廃止された形式：`$main::ws_url` |
| `$main::search_content_type` | 値は、http-equivメタタグから取得したドキュメントのコンテンツタイプです。 一般的な値は「text/html;charset=iso-8859-1&quot;.  廃止された形式：`$main::ws_content_type` |
| `$main::search_content_class` | 値は、content-typeフィールドから派生する、ドキュメントのコンテンツクラスです。  廃止された形式：`$main::ws_content_class` |
| `$main::search_syntax_check` | この値は、「構文をチェック」ボタンの使用を反映しています。 クリックした場合、値は1(1)です。それ以外の場合、値は0（ゼロ）です。  廃止された形式：`$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Webサーバーによって提供される場合、この値には、ドキュメントの最終変更日のエポック表現（1970年1月1日からの秒数）が含まれます。  この値は、Perl localtime()ライブラリの呼び出しを使用してフォーマットできます。 |

### クイックヒント{#section_89A5C16911744AF98E232DF608C6A1F5}

* すべてのグローバル変数は、名前空間「main::」で始まります。`$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。`my $i = 0;`
* サブルーチンは、初期化スクリプトで定義します。 明示的な「main::」名前空間は必要ありません。`sub my_sub {` `...`

   `}`

* ファイルに変更を加える前に、`$main::search_content_type`をテストしてください。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`は、サーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプとその後にドキュメントの文字セットエンコーディングなどの他の情報を含めることもできます(「text/html;charset=iso-8859-1&quot;.
* HTML以外のドキュメントのタイプごとに、`$main::search_content_type`は様々な値を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプの値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、`$main::search_content_class`は次の値を取ることができます。

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」に対して`$main::search_content_class`をテストすると、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合は、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の操作を行います。`print "<html></html>";`

## フィルタリングスクリプト{#task_0AB84FD1133F47F9AA069A79BEA13A22}の追加

フィルタリングスクリプトは、Webサイトからダウンロードされた各ドキュメントに対して実行されるPerlスクリプトです。

フィルタリングスクリプトは、初期化スクリプト、終了スクリプト、URLマスクスクリプトと組み合わせて使用します。

フィルタリングスクリプトの結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**フィルタリングスクリプトを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Filtering]**/**[!UICONTROL Filtering Script]**&#x200B;をクリックします。
1. （オプション）[!DNL Filtering Script]ページの[!DNL Test URL]フィールドに、WebサイトのドキュメントのURLを入力します。

   テストオプションをクリックして、生のHTMLテキストの変更を表示します。

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
      <td colname="col2"> <p>URLをフィルタリングスクリプトおよびURLマスクと比較してテストします。 </p> <p>テストURLドキュメントがダウンロードされ、フィルタリングスクリプトへのSTDIN入力として使用されます。 その後、初期化、フィルタリング、終了スクリプトが実行されます。 フィルタリングスクリプトからのSTDOUT出力がある場合、その出力は新しいブラウザウィンドウに表示されます。 </p> </td> 
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
      <td colname="col2"> <p>ドキュメントの前後の完全なテーブル表示を生成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>短いビジュアル </p> </td> 
      <td colname="col2"> <p>前後の表示の違いのみを表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エキスパート（相違） </p> </td> 
      <td colname="col2"> <p>提供されたコマンドラインオプションを使用して、ファイルの比較に使用されるGNU diffコマンドの生の出力を表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィルタリングスクリプト </p> </td> 
      <td colname="col2"> <p>指定されたフィールドにフィルタースクリプトを貼り付けることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>変更の保存 </p> </td> 
      <td colname="col2"> <p>フィルタリングスクリプトを保存します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>構文をチェック </p> </td> 
      <td colname="col2"> <p>初期化、フィルタリング、終了の各スクリプトを実行して、スクリプトの構文を簡単に確認できます。 スクリプトは更新および保存されません。 </p> <p>すべてのPerlコンパイラのエラーと警告、およびすべてのSTDERR出力が出力されます。 </p> <p>スクリプトの効果がユーザーに表示される前に、サイトインデックスを再構築する必要があります。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **GNU diffコマンドラインオプション**

   Staged Filtering Scriptページの&#x200B;**[!UICONTROL Expert (diff)]**&#x200B;モードで使用できるGNU diffオプションの一部は、次のようになります。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>GNU diffコマンドラインオプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> 空白の大きさの変更を無視します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C行  </span> </p> </td> 
      <td colname="col2"> <p> コンテキストの行（整数）を表示する、または行を指定しない場合は3を表示する、コンテキスト出力形式を使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> 大文字と小文字の違いを無視する大文字と小文字は同じ意味を持ちます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> edスクリプトに似ているが、ファイル内に表示される順序が変化する出力を作成します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> RCS形式のdiffを出力します。<span class="codeph"> -f </span>のように、各コマンドが影響を受ける行の数を指定する点が異なります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> 統合出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U線  </span> </p> </td> 
      <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行を指定しない場合は3を表示します。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. フィルタースクリプトとURLマスクに対してテストを行うには、**[!UICONTROL Test]**&#x200B;をクリックします。

   **[!UICONTROL Test]**&#x200B;をクリックしても、フィルタリングスクリプトは更新および保存されません。
1. [!DNL Filtering Script]フィールドにスクリプトを貼り付けます。
1. （オプション）**[!UICONTROL Check Syntax]**&#x200B;をクリックして、フィルタリング、初期化、終了の各スクリプトを実行し、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** は、スクリプトを更新および保存しません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Filtering Script]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 初期化スクリプトについて{#concept_048B4C8BC9F74BE8BB6162C490C201A3}

[!DNL Initialization Script]を使用すると、Webドキュメントのインデックスを作成する前に、Webコンテンツを変更できます。

ドキュメントのURL、MIMEタイプおよび既存のコンテンツに基づいて、HTMLタグの挿入、無関係なコンテンツの削除、新しいHTMLメタデータの作成を行うこともできます。 初期化スクリプトはPerlスクリプトで、強力な文字列処理と正規式のマッチングの柔軟性を提供します。 初期化スクリプトは、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプト、およびテストURLと共に使用します。

初期化スクリプトは、インデックス作成を開始する前に1回だけ実行されます。 次のスクリプトを使用して、フィルタリングスクリプトで使用するすべてのグローバル変数とサブルーチンを初期化します。 初期化スクリプトを使用して、フィルタリング・スクリプトからインデックス・ログにステータス・メッセージを印刷できます。 メッセージは、STDERRに出力するか、`_search_debug_log()`サブルーチンを介して出力します。

Staged Initialization Scriptページの&#x200B;**[!UICONTROL Expert (diff)]**&#x200B;モードで使用できるGNU diffオプションの一部は、以下のとおりです。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diffオプション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> 空白の大きさの変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C行  </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示する、または行を指定しない場合は3を表示する、コンテキスト出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の違いを無視する大文字と小文字は同じ意味を持ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイル内に表示される順序が変化する出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。<span class="codeph"> -f </span>のように、各コマンドが影響を受ける行の数を指定する点が異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U線  </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行を指定しない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」で始まります。 初期化スクリプトを起動すると、その環境には次の標準ファイル・ハンドルが含まれます。

* STDIN — 何も返さない（読み込み時は直ちにEOFを返す）
* STDOUT — 何も返しません（データがSTDOUTに出力される場合は、破棄されます）
* STDERR - STDERRに出力されるデータは、エラーとしてインデックス・ログに出力されます。

また、次の例のように、`_search_debug_log()`サブルーチンを使用して、インデックスログにカスタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文として`DEBUG`という単語で表示され、エラーとして記録されません。

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

[グローバル変数](#global-variables)を参照

### クイックヒント{#section_A2CC0302CAF14135BF8EF6171FB184F1}

* すべてのグローバル変数は、名前空間「main::」で始まります。`$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。`my $i = 0;`
* サブルーチンは、初期化スクリプトで定義します。 明示的な「main::」名前空間は必要ありません。`sub my_sub {` `...`

   `}`

* ファイルに変更を加える前に、`$main::search_content_type`をテストしてください。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`は、サーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプとその後にドキュメントの文字セットエンコーディングなどの他の情報を含めることもできます(「text/html;charset=iso-8859-1&quot;.
* HTML以外のドキュメントのタイプごとに、`$main::search_content_type`は様々な値を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプの値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、`$main::search_content_class`は次の値を取ることができます。

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」に対して`$main::search_content_class`をテストすると、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合は、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の操作を行います。`print "<html></html>";`

## 初期化スクリプト{#task_5A03B8D0C46E4674B7CE88203515803B}の追加

初期化スクリプトは、ドキュメントのインデックスが作成される前に1回実行されるPerlスクリプトです。

初期化スクリプトは、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプトと組み合わせて使用します。

初期化スクリプトの結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**初期化スクリプトを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Filtering]**/**[!UICONTROL Initialization Script]**&#x200B;をクリックします。
1. （オプション）[!DNL Initialization Script]ページの[!DNL Test URL]フィールドに、WebサイトのドキュメントのURLを入力します。

   テストオプションをクリックして、生のHTMLテキストの変更を表示します。

   「**フィルタリングスクリプトの追加**」のフィルタリングオプションの表を参照してください。

   フィルタースクリプトとURLマスクに対してテストを行うには、**[!UICONTROL Test]**&#x200B;をクリックします。

   **[!UICONTROL Test]**&#x200B;をクリックしても、初期化スクリプトは更新および保存されません。
1. [!DNL Initialization Script]フィールドにスクリプトを貼り付けます。
1. （オプション）**[!UICONTROL Check Syntax]**&#x200B;をクリックして、フィルタリング、初期化、終了の各スクリプトを実行し、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** は、スクリプトを更新および保存しません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Initialization Script]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 終了スクリプトについて{#concept_AAD6B3B0E7124874AD0947096FC42F47}

[!DNL Termination Script]を使用すると、Webドキュメントのインデックスを作成する前に、Webコンテンツを変更できます。

ドキュメントのURL、MIMEタイプおよび既存のコンテンツに基づいて、HTMLタグの挿入、無関係なコンテンツの削除、新しいHTMLメタデータの作成を行うこともできます。 初期化スクリプトはPerlスクリプトで、強力な文字列処理と正規式のマッチングの柔軟性を提供します。 初期化スクリプト、フィルタリングスクリプト、終了スクリプト、URLマスクスクリプト、およびテストURLで、終了スクリプトを使用します。

終了スクリプトは、すべてのドキュメントのインデックスが作成された後に1回実行されます。 終了スクリプトを使用すると、フィルタリングスクリプトからインデックスログにステータスメッセージを印刷できます。 メッセージは、STDERRに出力するか、`_search_debug_log()`サブルーチンを介して出力します。

GNU diffコマンドラインオプションの一部は、Staged Termination Scriptページの&#x200B;**[!UICONTROL Expert (diff)]**&#x200B;モードで使用できますが、以下を含みます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diffコマンドラインオプション </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> 空白の大きさの変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> 空白行を挿入または削除した変更を無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> コンテキスト出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C行  </span> </p> </td> 
   <td colname="col2"> <p> コンテキストの行（整数）を表示する、または行を指定しない場合は3を表示する、コンテキスト出力形式を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> 大文字と小文字の違いを無視する大文字と小文字は同じ意味を持ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> edスクリプトに似ているが、ファイル内に表示される順序が変化する出力を作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> RCS形式のdiffを出力します。<span class="codeph"> -f </span>のように、各コマンドが影響を受ける行の数を指定する点が異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用し、3行のコンテキストを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U線  </span> </p> </td> 
   <td colname="col2"> <p> 統合出力形式を使用して、コンテキストの行（整数）を表示します。行を指定しない場合は3を表示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらのスクリプトでは、ローカル変数、グローバル変数またはその両方を使用できます。 すべてのグローバル変数は、名前空間「main::」で始まります。 終了スクリプトを起動すると、環境に次の標準ファイルハンドルが含まれます。

* STDIN — 何も返さない（読み込み時は直ちにEOFを返す）
* STDOUT — 何も返しません（データがSTDOUTに出力される場合は、破棄されます）
* STDERR - STDERRに出力されるデータは、エラーとしてインデックス・ログに出力されます。

また、次の例のように、`_search_debug_log()`サブルーチンを使用して、インデックスログにカスタムメッセージを書き込むこともできます。

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

これらのメッセージは、序文として`DEBUG`という単語で表示され、エラーとして記録されません。

フィルタリングスクリプトによって処理されたドキュメントの数をインデックスログのエラー行として表示するには、次の終了スクリプトを使用します。

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

[グローバル変数](#global-variables)を参照

### クイックヒント{#section_5790EA7ACAC046CBA01F759F88E2460F}

* すべてのグローバル変数は、名前空間「main::」で始まります。`$main::doc_count = 0;`
* すべてのローカル変数は「my」で宣言されます。`my $i = 0;`
* サブルーチンは、初期化スクリプトで定義します。 明示的な「main::」名前空間は必要ありません。`sub my_sub {` `...`

   `}`

* ファイルに変更を加える前に、`$main::search_content_type`をテストしてください。 テストを行うと、SWFファイルやPDFファイルなどのバイナリファイルに不注意な変更を加えないようにできます。

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`は、サーバーから配信される完全なContent-Typeヘッダーです。 「text/html」など、単純なMIMEタイプを含めることができます。 または、MIMEタイプとその後にドキュメントの文字セットエンコーディングなどの他の情報を含めることもできます(「text/html;charset=iso-8859-1&quot;.
* HTML以外のドキュメントのタイプごとに、`$main::search_content_type`は様々な値を取ることができます。 スクリプト内の各値のテストは面倒になります。 例えば、一部のWordドキュメントのコンテンツタイプの値は、「application/msword」、「application/vnd.ms-word」、「application/x-msword」です。 このような場合、`$main::search_content_class`は次の値を取ることができます。

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* この例では、「word」に対して`$main::search_content_class`をテストすると、3つのcontent-type値のいずれかと一致します。
* フィルタリングスクリプトからSTDOUTに何も出力されない場合は、ドキュメントはダウンロードされたとおりに使用されます。 つまり、ドキュメント内の変更が不要な場合は、そのドキュメントのSTDOUTにSTDINをコピーする必要はありません。
* ドキュメントからすべてのテキストを削除する場合は、有効なファイルSTDOUTを印刷します。 例えば、HTMLドキュメントからすべてのテキストを完全に削除するには、次の操作を行います。`print "<html></html>";`

## 終了スクリプトの追加{#task_F0CFB412871642CFBC88132889C5B6F9}

終了スクリプトは、すべてのドキュメントのインデックスが作成された後に1回実行されるPerlスクリプトです。

終了スクリプトは、フィルタリングスクリプト、終了スクリプト、およびURLマスクスクリプトと組み合わせて使用します。

初期化スクリプトの結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**終了スクリプトを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Filtering]**/**[!UICONTROL Termination Script]**&#x200B;をクリックします。
1. （オプション）[!DNL Termination Script]ページの[!DNL Test URL]フィールドに、WebサイトのドキュメントのURLを入力します。

   テストオプションをクリックして、生のHTMLテキストの変更を表示します。

   「**フィルタリングスクリプトの追加**」のフィルタリングオプションの表を参照してください。

   フィルタースクリプトとURLマスクに対してテストを行うには、**[!UICONTROL Test]**&#x200B;をクリックします。

   **[!UICONTROL Test]**&#x200B;をクリックしても、終了スクリプトは更新および保存されません。
1. [!DNL Termination Script]フィールドにスクリプトを貼り付けます。
1. （オプション）**[!UICONTROL Check Syntax]**&#x200B;をクリックして、初期化、フィルタリング、終了スクリプトを実行し、スクリプトの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** は、スクリプトを更新および保存しません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Termination Script]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## URLマスクスクリプトについて{#concept_384F32EA18F84853A7BA99A04009330B}

フィルタリングを使用すると、Webドキュメントーのコンテンツを変更してからインデックスを作成できます。 ドキュメントのURL、MIMEタイプおよび既存のコンテンツに基づいて、HTMLタグの挿入、無関係なコンテンツの削除、新しいHTMLメタデータの作成を行うこともできます。 URLマスクスクリプトは、強力な文字列処理と正規式のマッチングの柔軟性を提供するPerlスクリプトです。

Webサイトの特定の部分にのみ存在するドキュメントのコンテンツを変更するには、URLマスクを含める、URLマスクを除外する、またはその両方を指定して、適切なページを定義します。

`"https://www.mysite.com/faqs/"`の下のドキュメントのみを変更する場合は、次のマスクを使用できます。

```
include https://www.mysite.com/faqs/ 
exclude *
```

次の例のように、URLマスクスクリプトで正規式を使用することもできます。

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

スクリプト化されたURLマスクは、[!DNL URL Masks]フィールドに入力した順に考慮されます。 ドキュメントURLがマスクに一致する場合、そのドキュメントはマスクの種類に基づいて含められるか、除外されます。 ドキュメントのURLがURLマスクと一致しない場合、ドキュメントは、そのMIMEタイプが「text/html」の場合にのみ含まれます。 その他のMIMEタイプはすべて除外されます。

## URLマスクスクリプト{#task_D18F2A496C1C45C997B5DA650AAF5D59}の追加

マスクを含むURLとマスクを除外を指定して、Webサイトの特定の部分にのみ存在するドキュメントのコンテンツを変更します。

URLマスク設定の効果が訪問者に表示される前に、サイトのインデックスを作成し直してください。

**URLマスクスクリプトを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Filtering]**/**[!UICONTROL URL Masks]**&#x200B;をクリックします。
1. （オプション）[!DNL URL Masks]ページの[!DNL Test URL]フィールドに、Webサイト上のドキュメントのURLを入力し、**[!UICONTROL Test]**&#x200B;をクリックして、URLをフィルタリングスクリプトおよびマスクと比較してテストします。

   テストURLドキュメントがダウンロードされ、フィルタリングスクリプトへのSTDIN入力として使用されます。 次に、フィルタリング、初期化、終了スクリプトが実行されます。 フィルタリングスクリプトからのSTDOUT出力がある場合、その出力は新しいブラウザウィンドウに表示されます。

   **[!UICONTROL Test]**&#x200B;をクリックしても、スクリプトは更新および保存されません。
1. [!DNL URL Masks]フィールドに、1行につき1つのURLマスクを入力します。
1. （オプション）**[!UICONTROL Check Syntax]**&#x200B;をクリックして、フィルタリング、初期化、終了の各スクリプトを実行し、URLマスクの簡単な構文チェックを実行します。

   **[!UICONTROL Check Syntax]** は、スクリプトを更新および保存しません。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL URL Masks]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フィルタリングのコンテンツタイプについて{#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

このアカウント用にフィルターを適用するコンテンツタイプを選択できます。

選択したコンテンツタイプ内のテキストはHTMLに変換され、フィルタリングスクリプトで指定したスクリプトを使用して処理されます。

[フィルタリングスクリプトについて](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)を参照してください。

次のコンテンツタイプから選択できます。

* PDFドキュメント
* テキストドキュメント
* AdobeFlashムービー
* Microsoft Wordファイル
* Microsoft Officeファイル(OpenXML)
* Microsoft Excelファイル
* Microsoft Powerpointファイル
* MP3ミュージックファイル内のテキスト

ユーザーがコンテンツタイプ設定や設定の変更を表示できるようにするには、サイトインデックスを作成し直す必要があります。

## フィルターを適用するコンテンツタイプの選択{#task_C46081FA425A43EC8FDE6EA4A52A170A}

フィルタースクリプトで指定したスクリプトに渡すコンテンツタイプを選択します。

[フィルタリングスクリプトについて](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)を参照してください。

**フィルタリングするコンテンツタイプを選択するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Filtering]**/**[!UICONTROL Content Types]**&#x200B;をクリックします。
1. [!DNL Content Types]ページで、フィルタースクリプトに渡すコンテンツタイプを確認します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）結果をプレビューする場合は、ステージングされたサイトインデックスを再構築します。

   「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。
1. （オプション）[!DNL Content Types]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。
