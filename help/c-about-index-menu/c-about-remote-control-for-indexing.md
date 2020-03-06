---
description: Webサイトが変更された場合は、検索ロボットにリモートコントロールを使用してインデックスを実行するように要求するスクリプトまたはプログラムを実行できます。
seo-description: Webサイトが変更された場合は、検索ロボットにリモートコントロールを使用してインデックスを実行するように要求するスクリプトまたはプログラムを実行できます。
seo-title: インデックス作成用のリモートコントロールについて
solution: Target
title: インデックス作成用のリモートコントロールについて
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# インデックス作成用のリモートコントロールについて{#about-remote-control-for-indexing}

Webサイトが変更された場合は、検索ロボットにリモートコントロールを使用してインデックスを実行するように要求するスクリプトまたはプログラムを実行できます。

## インデックス作成にリモートコントロールを使用する {#concept_C79B322190E84106A434E5C6D4A4118F}

リモート制御インデックス作成要求は、通常、サーバー上にあるスクリプトまたはプログラムから送信されます。

ロボットは、メニューから手動で開始した場合と同じインデックス作成手順を実行 [!DNL Index] します。 リモート制御要求を送信するには、必要なパスワードと応答文字列を設定します。

## リモート制御要求の作成方法 {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

リモート制御要求を行うには、データセンターの場所に基づいて次の形式の例を使用します。

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
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999 </span> </p> </td> 
   <td colname="col2"> <p> アカウント番号。 </p> <p>アカウント番号は、設定/アカウント設定/ <span class="uicontrol"> オプ <b>ショ</b> ン設定/アカウント設 </span> 定で確認で <span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span>きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N </span> </p> </td> 
   <td colname="col2"> <p>実行中のインデックスクロールの状態を確認できます。 </p> <p> <span class="codeph">  Nは正 </span> の整数またはすべて <span class="codeph"> です </span>。 これが数値の場合、対応するインデッ <span class="codeph"> クスロ </span> グファイルの最後のN行がJSON応答に含まれます。 </p> <p>値がallの場合、フ <span class="codeph"> ァイ </span>ル全体が返されます。 </p> <p>値が0の場合、ロ <span class="codeph"> グ情 </span>報は返されません。 この値は、実行中のインデックスステータスクエリのデフォルト値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op </span> </p> </td> 
   <td colname="col2"> <p>実行するインデックス作成操作を次の中から1つ指定できます。 </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index </span> <p>検索ロボットは、ウェブサイトの完全なインデックスを実行します。 </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index </span> <p>検索ロボットは、Index <span class="uicontrol"> &gt; <b>Incremental</b> Incremental </span> Incremental <span class="uicontrol"> Index &gt; <b>Configuration Configuration</b></span><span class="uicontrol"><b></b></span>Indexの下に設定された設定を使用して、インクリメンタルインデックスを実行する。 </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index </span> <p>検索ロボットは、 <span class="uicontrol"> Index <b>&gt;</b> Vertical </span> &gt; <span class="uicontrol"> Vertical <b>Update Configuration</b></span><span class="uicontrol"><b></b></span>Configurationの下に設定された設定を用いて更新を実行する。 </p> <p>垂直更新につ <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> いてを参照してください</a>。 </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index </span> <p>検索ロボットは、Index <span class="uicontrol"> &gt; Scripted Index &gt; Configuration <b>Configuration</b> Scripted Index &gt; Scripted Index &gt; Configuration </span><span class="uicontrol"><b></b></span><span class="uicontrol"><b></b></span>Configurationで指定されたテキストファイルを使用して、増分インデックスを実行します。 </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index </span> <p>検索ロボットは、ウェブサイトの完全なステージインデックスを実行します。 </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index </span> <p>検索ロボットは、Index <span class="uicontrol"> &gt; Incremental <b>Index</b> &gt; Incremental </span> Index <span class="uicontrol"> &gt; <b>Configuration Configuration</b></span><span class="uicontrol"><b></b></span>Configuration Indexの下に設定された設定を使用して、増分ステージングインデックスを実行します。 </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index </span> <p>検索ロボットは、Index <span class="uicontrol"> &gt; Vertical Update <b></b> Update </span> Update <span class="uicontrol"> Vertical Update <b>Configuration</b></span><span class="uicontrol"><b></b></span>Configuration Stagedの下に設定された設定を使用して、垂直段階更新を実行します。 </p> </li> 
     </ul> </p> <p>注意： 業務別アップデートを使用するには、お使いのアカウントで、アドビのアカウント担当者またはアドビサポートによって有効にされる必要がある場合があります。 </p> <p>垂直更新につ <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> <p>上記の <span class="codeph"> sp_operation値 </span> のいずれかに_savedを追加して、検索ロボットが保 <span class="codeph"> 存済みコン </span> テンツを使用しようとするように設定できます。 例えば、次のように指定できます。 </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p> または </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>また、上記の <span class="codeph"> sp_operation値のいず </span><span class="codeph"></span> れかに_statusを追加して、現在の操作または最新の操作のステータスレポートを要求することもできます。 例えば、次のように指定できます。 </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p> または </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>結果はJSONオブジェクトとして返されます。 sp_lines=Nを含 <span class="codeph"> めると、関 </span> 連するログファイルのN行が含まれます。 Nが負の場合、最後のN行が含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive </span> </p> </td> 
   <td colname="col2"> <p> ステージングされたインデックスをリモートでプッシュできます。 </p> <p>「Push <span class="codeph"> Live」操作に_saved </span> を追加しようとしても無視されます。 </p> <p>pushlive操作を実行する <span class="codeph"> と、OK、 </span> 優先度、またはエラーの応答テキスト文字列がサーバーに返されます。 これらの応答文字列は、[リモートコントロール]ペ <span class="wintitle"> ージで指定 </span> します。 </p> <p>インデックス <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> 作成のためのリモート制御の設定を参照してくださ</a>い。 </p> <p>ステージングされたインデックスがないときにライブをプッシュした場合、何も起こらず、OK応答文字列が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password=xxxx </span> </p> </td> 
   <td colname="col2"> <p>リモートコントロールのパスワード。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索は、適切なHTTP応答の形式でデータを返します。 完全な応答は、HTTPステータス、HTTP応答ヘッダー、空白行および応答文字列で構成されます。

例えば、次のリモート制御要求を実行したとします。

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

このインデックス操作に関連付けられたログリストの最初の10行と、そのステータスを取得するには、次のクエリが使用されます。

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

Note the `offset` value. この値は、読み取りが中止されたログファイル内のファイルオフセット位置を示します。 ファイル内の *次の* 10行を読み取るには、この例では、サーバーに送信され `&sp_offset=672` るリクエストに含めます。

を使用す `sp_offset`ると、ログファイルを効果的にページスルーできます。

ログの最後の ** 10行とステータスを取得するには、カウントを負の数で指定します。 例えば、次のよ `sp_lines=` うに値を `-10` 指定します。

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

この操作はファイルの最 `offset` 後で終了し、読み込む行がなくなったので、ここに値が返されません。

## インデックス作成用のリモートコントロールの構成 {#task_57C296258404448DA7A5ADC9B7232391}

Webサイトが変更された場合は、リモートコントロールを使用して、検索ロボットにインデックスの実行を要求するスクリプトまたはプログラムをサーバーから実行できます。

**インデックス作成用のリモートコントロールを構成するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Index]** クしま **[!UICONTROL Remote Control]**&#x200B;す。
1. ページで、 [!DNL Remote Control] 各設定フィールドのオプションを設定し、Webサイトのインデックスを作成するインデックス作成要求をサーバーから自動的に送信できるようにします。

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
    <td colname="col2"> <p>リモートコントロールのパスワードを指定します。 </p> <p> パスワードは大文字と小文字が区別され、長さが6文字以上で、少なくとも1文字を含める必要があります。 少なくとも1つの数字も含めることをお勧めします。 </p> <p>サイト検索/マーチャンダイジングのログインパスワードは使用しないでください。 </p> <p>パスワードは、各リモートコントロール要求で使用されます。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>OK応答文字列 </p> </td> 
    <td colname="col2"> <p>要求されたインデックス操作が正常に開始した場合に、OK応答のテキスト文字列を指定できます。 この場合、検索ロボットはOK応答文字列をサーバに返します。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>優先度応答文字列 </p> </td> 
    <td colname="col2"> <p>リモート要求が行われたときに別のインデックス作成操作が進行中の場合、検索ロボットは要求されたインデックスを実行できません。 このような場合、Priority応答のテキスト文字列がサーバーに返されます。 </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>エラー応答文字列 </p> </td> 
    <td colname="col2"> <p>エラー応答のテキスト文字列を指定できます。パスワードが正しくない場合や、別のエラーが発生した場合。 このような場合、検索ロボットはエラー応答文字列をサーバに返します。 </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
