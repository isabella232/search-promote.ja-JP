---
description: Webサイトが変更された場合は常に、リモートコントロールを使用して検索ロボットにインデックスの実行を要求するスクリプトまたはプログラムを実行できます。
solution: Target
title: インデックス作成のためのリモートコントロールについて
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 1%

---


# インデックス作成のリモートコントロールについて{#about-remote-control-for-indexing}

Webサイトが変更された場合は常に、リモートコントロールを使用して検索ロボットにインデックスの実行を要求するスクリプトまたはプログラムを実行できます。

## リモートコントロールを使用したインデックス作成{#concept_C79B322190E84106A434E5C6D4A4118F}

リモートコントロールのインデックス作成要求は、通常、サーバー上にあるスクリプトまたはプログラムから発生します。

ロボットは、[!DNL Index]メニューから手動で開始したのと同じインデックス作成手順を実行します。 リモートコントロール要求を送信するには、必要なパスワードと応答文字列を設定します。

## リモート制御要求の作成方法{#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

リモートコントロール要求を行うには、データセンターの場所に応じて、次の形式の例を使用します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>データセンターの場所 </p> </th> 
   <th colname="col2" class="entry"> <p>例 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ロンドン </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>北アメリカ </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>シンガポール </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

 または

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>文字列と値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999  </span> </p> </td> 
   <td colname="col2"> <p> アカウント番号。 </p> <p>アカウント番号は、<span class="uicontrol"> <b>設定</b> </span> &gt; <span class="uicontrol"> <b>アカウントオプション</b> </span> &gt; <span class="uicontrol"> <b>アカウント設定</span>にあります。</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>実行中のインデックスクロールの状態を確認できます。 </p> <p> <span class="codeph">  N </span> は正の整数または <span class="codeph"> すべて </span>です。これが数値の場合、対応するインデックスログファイルの最後の<span class="codeph"> N </span>行がJSON応答に含まれます。 </p> <p>値が<span class="codeph">の場合、すべての</span>が返されます。 </p> <p>値が<span class="codeph"> 0 </span>の場合、ログ情報は返されません。 この値は、実行中のインデックスステータスクエリのデフォルト値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>実行するインデックス作成操作を次の中から1つ指定できます。 </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>検索ロボットはウェブサイトの完全なインデックスを実行します。 </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index  </span> <p>検索ロボットは、<span class="uicontrol"> <b>インデックス</b> </span> <span class="uicontrol"> <b>増分インデックス</b> </span> <span class="uicontrol"> <b>設定</b></span>に設定された構成を使用して増分インデックスを実行します。 </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>検索ロボットは、<span class="uicontrol"> <b>インデックス</b> </span> &gt; <span class="uicontrol"> <b>垂直更新</b> </span> &gt; <span class="uicontrol"> <b>設定</b></span>に設定された設定を使用して垂直更新を実行します。 </p> <p><a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">垂直更新について</a>を参照してください。 </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>検索ロボットは、<span class="uicontrol"> <b>インデックス</b> </span> <span class="uicontrol"> <b>スクリプトインデックス</b> </span> <span class="uicontrol"> <b>設定</b></span>で指定されたテキストファイルを使用してインクリメンタルインデックスを実行します。 </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>検索ロボットは、ウェブサイトの完全なステージインデックスを実行します。 </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index  </span> <p>検索ロボットは、<span class="uicontrol"> <b>インデックス</b> </span> <span class="uicontrol"> <b>増分インデックス</b> </span> <span class="uicontrol"> <b>設定</b></span>に設定された構成を使用して、増分ステージインデックスを実行します。 </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index  </span> <p>検索ロボットは、<span class="uicontrol"> <b>インデックス</b> </span> <span class="uicontrol"> <b>垂直更新</b> </span> <span class="uicontrol"> <b>設定</b></span>の下に設定された設定を使用して、垂直段階更新を実行します。 </p> </li> 
     </ul> </p> <p>注意： 垂直アップデートを使用するには、Adobeのアカウント担当者またはAdobeサポートがアカウントで有効にする必要がある場合があります。 </p> <p><a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local">縦置き版の更新について</a>を参照してください。 </p> <p>上記の<span class="codeph"> sp_operation </span>値のいずれかに<span class="codeph"> _saved </span>を追加すると、検索ロボットが保存したコンテンツを使用しようとします。 例えば、次のように指定できます。 </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p> または </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>または、上記の<span class="codeph"> sp_operation </span>値のいずれかに<span class="codeph"> _status </span>を追加して、現在または最新の操作に関するステータスレポートを要求できます。 例えば、次のように指定できます。 </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p> または </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>結果はJSONオブジェクトとして返されます。 <span class="codeph"> sp_lines=N </span>を含めて、関連するログファイルのN行を含めます。 Nが負の値の場合は、最後のN行が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive  </span> </p> </td> 
   <td colname="col2"> <p> ステージングされたインデックスをリモートでプッシュして有効にできます。 </p> <p>プッシュライブ操作に<span class="codeph"> _saved </span>を追加しようとしても無視されます。 </p> <p><span class="codeph"> pushlive </span>操作を実行すると、OK、優先度、またはエラーの応答テキスト文字列がサーバーに返されます。 これらの応答文字列は、<span class="wintitle">リモートコントロール</span>ページで指定します。 </p> <p>「<a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local">リモートコントロールのインデックス作成の構成</a>」を参照してください。 </p> <p>ステージングされたインデックスがない場合にライブをプッシュすると、何も起こらず、OK応答文字列が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxx  </span> </p> </td> 
   <td colname="col2"> <p>リモコンパスワードです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索は、適切なHTTP応答の形式でデータを返します。 完全な応答は、HTTPステータス、HTTP応答ヘッダー、空白行および応答文字列で構成されます。

例えば、次のリモートコントロール要求を実行したとします。

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

次に、サーバーからの応答を示します。

```
Status: 200 OK 
Content-type: text/plain 
OK
```

または、次のリモートコントロールステータス要求を実行したとします。

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

サーバーからの応答は次のようになります。

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

このインデックス操作に関連付けられたログ一覧の最初の10行とそのステータスを取得するには、次のクエリを使用します。

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

サーバーからの応答：

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

`offset`の値をメモしておきます。 この値は、読み取りが行われたログファイル内のファイルオフセットの位置を示します。 ファイル内の&#x200B;*next* 10行を読み取るには、この例では、サーバーに送信される要求に`&sp_offset=672`を含めます。

`sp_offset`を使用すると、ログファイルを効果的に閲覧できます。

ログの&#x200B;*最後の* 10行とステータスを取得するには、カウントを負の数に指定します。 例えば、次のように`sp_lines=`を`-10`の値で指定します。

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

サーバーからの応答：

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

この処理はファイルの最後で終了し、読み込む行がなくなるので、ここに`offset`値が返されません。

## {#task_57C296258404448DA7A5ADC9B7232391}のインデックス作成のためのリモートコントロールの構成

Webサイトが変更された場合は常に、リモートコントロールを使用して、検索ロボットにインデックスの実行を要求して、サーバーからスクリプトまたはプログラムを実行できます。

**インデックス作成用のリモートコントロールを構成するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Remote Control]**&#x200B;をクリックします。
1. [!DNL Remote Control]ページで、各設定フィールドのオプションを設定し、自動的にサーバーからインデックス作成要求を送信してWebサイトのインデックスを作成できるようにします。

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>オプション </p> </th> 
    <th colname="col2" class="entry"> <p>説明 </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>リモートコントロールパスワード </p> </td> 
    <td colname="col2"> <p>リモートコントロールのパスワードを指定します。 </p> <p> パスワードは大文字と小文字が区別され、長さが6文字以上で、1文字以上にする必要があります。 少なくとも1つの数字も含めることをお勧めします。 </p> <p>サイト検索/マーチャンダイジングのログインパスワードは使用しないでください。 </p> <p>パスワードは、各リモートコントロール要求で使用されます。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>OK応答文字列 </p> </td> 
    <td colname="col2"> <p>要求されたインデックス操作が正常に開始した場合に、OK応答のテキスト文字列を指定できます。 この場合、検索ロボットはOK応答文字列をサーバに返します。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>優先度応答文字列 </p> </td> 
    <td colname="col2"> <p>リモート要求が行われた際に、別のインデックス作成操作が進行中の場合、検索ロボットは要求されたインデックスを実行できません。 このような場合、Priority応答テキスト文字列がサーバーに返されます。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>エラー応答文字列 </p> </td> 
    <td colname="col2"> <p>エラー応答のテキスト文字列を指定できます。パスワードが正しくない場合や、別のエラーが発生した場合。 このような場合、検索ロボットはエラー応答文字列をサーバに返します。 </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
