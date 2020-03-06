---
description: スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスの作成、更新、維持を行うことができます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。
seo-description: スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスの作成、更新、維持を行うことができます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。
seo-title: スクリプトインデックスについて
solution: Target
subtopic: Scripted Index
title: スクリプトインデックスについて
topic: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# スクリプトインデックスについて{#about-scripted-index}

スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスの作成、更新、維持を行うことができます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。

## スクリプトインデックスの使用 {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## スクリプトの増分インデックスの設定について {#section_161D254065E143F3A39F3FC09C400090}

スクリプト化インデックスを使用するには、スクリプト化インデックスの設定ページを使用して、サーバー上にあるスクリプトファイル（プレーンテキストファイル）のURLを指定します。 例： `https://www.mysite.com/indexlist.txt`サイトが変更されると、手動または自動（ニュースフィード、株価、その他の変更されたファイルからの情報の受信によってトリガーされるスクリプトを使用）でテキストファイルにコマンドブロックを追加できます。

スクリプトの増分インデックスが開始されると、検索ロボットはテキストファイルを読み取り、そのファイル内の新しいコマンドを実行します。 デフォルトでは、検索ロボットは新しいコマンドのみを処理し、ファイルの日付によって決まります。 スクリプト化インデックス **[!UICONTROL Clear Date]** を設定する際にチェックを行わない限り、検索ロボットは最も最近処理されたブロックの日付指定子を「記憶」します。

## スクリプトファイルについて {#section_B312E40539F44C6583B4F9637D428E19}

URLで指定するスクリプトファイルは、サーバー上のプレーンテキストファイルです。 行末シーケンスには、キャリッジリターン、ラインフィードまたはその両方を使用できます。 空白行には、0個以上の空白文字の後に行末シーケンスが続きます。 すべてのコマンドでは、大文字と小文字が区別されません。

テキストファイルは、スクリプト化された増分インデックスを実行する際に検索ロボットが使用する情報を記述したブロックで構成されます。

ブロックは日付順に並べられ、最も古いブロックがテキストファイルの先頭に、最も新しいブロックが下に表示されます。 各ブロックは、1行のdate-commandとdate-specifierコマンドで始まり、次のブロック例のように空白行区切り文字で終わります（間には複数のコマンドがあります）。

HTTP 1.1スタイルを使用する場合、10番目より前の序数の日付はすべて、先頭に0が必要です。 例えば、11月6日は11月6日ではなく、11月6日です。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コマンド </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>date-command </p> </td> 
   <td colname="col2"> <p>各ブロックの最初の行は、次の2つの日付コマンドのいずれかで始まります。 </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> date </span> <p>「date」コマンドを使用して、日付指定子が日、日、時刻、およびタイムゾーンで構成されることを示します。 </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> 秒 </span> <p>日付指 <span class="codeph"> 定子 </span> がエポック秒の時間で構成されることを示すには、秒を使用します（例：78411777）。 秒を使用す <span class="codeph"> る場合 </span>は、ブロック間の秒数が増加することを確認します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p>通常、 <span class="codeph"> date-specifier </span> コマンドは、ブロック情報がファイルに追加された元の日時（dateコマンド）またはエポック秒（secondsコマンド）の時間を記録します。 次に例を示します。 </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>HTTP 1.1スタイルを使用する場合、10番目より前の序数の日付はすべて、先頭に0が必要です。 例えば、11月6日は11月6日ではなく、11月6日です。 </p> <p>検索ロボットは、最も最近処理されたブロックの日付指定子を「記憶」し、「新しい」と見なされる情報のみをインデックス化します。 (リアルタイムは検索ロボットには関係ありません。 その代わりに、前に処理された他の時間との関係が重要です。) </p> <p>例えば、検索ロボットは、日付指定子が10:00 p.mのブロックを読み取った後、インデックス操作の実行時間にかかわらず、10:00 p.m.より前の時刻を記録するブロックを読み取りません。 最悪の場合は、日付指定子に誤って「2004」ではなく「2040」という年を入力する可能性があります。 この場合、検索ロボットは次のインデックス作成操作中に2040ブロックのインデックスを作成し、その後（2040年以降の1つを除く）他の情報ブロックの読み取りを拒否します。 この問題が発生した場合は、以前に処理されたすべてのブロックをテキストファイルから削除し、「日付をク <span class="uicontrol"> リア」をク </span>リックして、アクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>コメント行 </p> </td> 
   <td colname="col2"> <p>コメント行の先頭は「#」文字にします。 </p> <p>各コメント行は、それぞれ独自の行である必要があります。行末のコメントを入力することはできません。 </p> <p>コメント行は空白行と見なされません。 また、次の例のように、dateまたはsecondsコマンドの前でも、ブロック内の任意の場所に表示できます。 </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-command </p> </td> 
   <td colname="col2"> <p>各テキストブロックには、必要な数のアクションコマンドを含めることができます。 次のアクションコマンドオプションは、標準の増分インデックス作成のオプションに対応しています。 </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <userinput>
         追加 
       </userinput> <p>URLと共に使用します。 検索ロボットは、前回のインデックス作成操作以降に変更された、指定したURLのみインデックスを作成します。 また、検索ロボットは、指定したドキュメント内のリンクに従い、変更されたドキュメントのみをインデックス付けします。 </p> <p>URLは、 
        <userinput>
          nofollow 
        </userinput>  または 
        <userinput>
          noindex 
        </userinput> キーワードを次の例のように指定します。 </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <userinput>
         更新 
       </userinput> <p>URLマスクと共に使用します。 検索ロボットは、指定したURLマスクに一致するすべてのドキュメントを検索し、更新します。 </p> <p>URLは、 
        <userinput>
          nofollow 
        </userinput>  または 
        <userinput>
          noindex 
        </userinput> キーワードを次の例のように指定します。 </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <userinput>
         include 
       </userinput>  または 
       <userinput>
         exclude 
       </userinput> <p>URLマスクと共に使用します。 検索ロボットは、指定されたマスクの種類に基づいて、ドキュメントのインデックス(「include」)を検索するか、ドキュメントを無視します(「exclude」)。 </p> <p>例： </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p> または </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <userinput>
         include-date 
       </userinput>  または 
       <userinput>
         exclude-date 
       </userinput> <p>URLマスクと共に使用します。 検索ロボットは、URLとドキュメントの日付の両方に基づいて、ドキュメントの検索とインデックス付け(「include」)または無視(「exclude」)を行います。 次の種類のマスクを使用できます。 </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <userinput>
            include-days NNN 
          </userinput> <p>検索ロボットは、指定したURLマスクに一致し、NNN日以上前のすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <userinput>
             nofollow 
           </userinput>、 
           <userinput>
             noindex 
           </userinput>，および/または 
           <userinput>
             server-date 
           </userinput>。 </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <userinput>
            include-date YYYY-MM-DD 
          </userinput> <p> 検索ロボットは、指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックスを作成します。「YYYY」は4桁の年、「MM」は1桁または2桁の月(1 ～ 12)、「DD」は1桁または2桁の日(1 ～ 31)です。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <userinput>
             nofollow 
           </userinput>、 
           <userinput>
             noindex 
           </userinput>，および/または 
           <userinput>
             server-date 
           </userinput>。 </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <userinput>
            exclude-days NNN 
          </userinput> <p> 指定したURLマスクに一致し、NNN日以上前のすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <userinput>
             server-date 
           </userinput>。 </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <userinput>
            exclude-date YYYY-MM-DD 
          </userinput> <p>指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <userinput>
             server-date 
           </userinput>。 </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <userinput>
         delete 
       </userinput> <p>URLを指定します。 検索ロボットは、URLで識別されるインデックスからドキュメントを削除します。 </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <userinput>
         deletemask 
       </userinput> <p>検索ロボットは、指定したURLマスクに一致するインデックスからドキュメントを削除します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

URLマスクにつ [いても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)。

## スクリプトファイルの例 {#section_9F580F20E7214751B157A28B392BD64E}

次のスクリプトファイルの例では、検索ロボットは、日付指定子がpost-dateに指定した日付のブロックを、最も最近処理されたブロックの日付指定子で処理します。 その場合、次のインデックス作成操作が実行されます。

* インデックス `y2k-problems.html` から削除します。
* 検索イ `no-y2k-problems.html` ンデックスに追加し、のリンクのどれにも従いませ `no-y2k-problems.html`ん。

* クロール中に、検索インデックスに一致す `housewares.htm` るURLと `lightfixtures.htm`lに一致するURLを除外します。

* その他のすべてのディレクトリとドキュメントをに含めま `www.mydomain.com`す。
* およびディレクトリ内のすべてのドキュメ `products` ントを更新し、 `information` 前回のインデックス作成操作以降に変更されたすべての子リンクをクロールしてインデックスを作成します。

* クロール中に、1999年1月1日以 `archive` 前の日付のURLをWebサイトのセクションから除外します。
* 検索インデックスに一致す `housewares.html` るURLと `lightfixtures.html` 一致するURLを除外します。

* ディレクトリ内のインデックスフ `help` ァイルですが、これらのファイルからのリンクをクロールまたはインデックス付けしないでください。
* に対して検出された他のファイルをクロールし、インデックスを作成しま `www.mydomain.com`す。

```
# Start of file. 
# Added by John Smith 
date Sat, 01 Jan 2004 16:05:53 PST 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/ 
delete https://www.mydomain.com/y2k-problems.html 
add https://www.mydomain.com/no-y2k-problems.html nofollow 
 
date Sun, 02 Jan 2004 20:19:08 PST 
# Added by the wire service updater 
exclude-date 1999-01-01 https://www.mydomain.com/archive server-date 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/help/ nofollow 
include https://www.mydomain.com/ 
# no add files, just update existing files 
# update all files in the "products" directory 
update https://www.mydomain.com/products/ 
# update all files in the "information" directory 
update regexp ^https://www\.mydomain\.com/information/.*$ 
# End of file.
```

## スクリプト化された増分インデックスの設定 {#task_05AE040FE75E40FFAA5E10B6B6D4D255}

作成したスクリプトを指定して、インクリメンタルインデックスの書き込み、更新、維持を行うことができます。ログインする必要はありません。 検索ロボットは、増分インデックスを実行するために、サーバー上でホストされているテキストファイルから指示を読み取ります。

**スクリプト化された増分インデックスを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Scripted Index]** ます **[!UICONTROL Configuration]**。
1. ページ **[!UICONTROL Scripted Incremental Index Configuration]** ので、サーバ **[!UICONTROL Script File URL]**&#x200B;ー上にあるテキストファイルスクリプトのURLを入力します。

   スクリプト化イ [ンデックスについてを参照してくださ](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)い。
1. （オプション）検 **[!UICONTROL Clear Date]** 索ロボットに、最も最近処理されたブロックの日付指定子を「記憶」させないかどうかを確認します。

   デフォルトでは、検索ロボットはテキストファイル内の新しいコマンドブロック（ファイルの日付によって決まる）のみを処理します。 デフォルトを使用しない場合は、をオンにしま **[!UICONTROL Clear Date]**&#x200B;す。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ライブWebサイト用のスクリプト化された増分インデックススケジュールの設定 {#task_B3A87AC4AC784507859C23B9062BA11C}

1日を通じて、定期的にスクリプト化された増分インデックスを作成するようにスケジュールできます。

選択する基本時刻は、[アカウントの設定]で設定したタイムゾーンに従ってローカルになります。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

多くの場合、深夜には、メンテナンスのためにウェブサーバがダウンする予定です。 スケジュールされたインデックス時間中にサーバーがダウンした場合、インデックス作成処理は失敗します。 Webサーバーが利用可能な時間帯を選択していることを確認してください。

インデックススケジュールは、ライブインデックスにのみ適用されます。ステージングされた増分インデックスはスケジュールできません。

**ライブWebサイトのスクリプト化された増分インデックススケジュールを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Scripted Index]** ます **[!UICONTROL Live Schedule]**。
1. ページ **[!UICONTROL Scripted Incremental Index Schedule]** のドロップダ **[!UICONTROL Read the Scripted Incrementally Indexing File]** ウンリストで、スクリプトの増分インデックステキストファイルを実行する頻度を、時間単位または分単位で選択します。
1. ドロップダ **[!UICONTROL Base Time]** ウンリストで、新しいスクリプト化された増分インデックスを再生成する開始時刻を選択します。
1. クリック **[!UICONTROL Save Changes]**.

## ライブWebサイトまたはステージWebサイトのスクリプト化された増分インデックスの実行 {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

スクリプト化された増分インデックスを使用すると、頻繁に変更されるページのコレクションなど、ライブまたはステージングされたWebサイトの「断片」のインデックスを作成でき、ログインする必要はありません。

この機能を使用するには、スクリプト化された増分インデックステキストファイルを設定済みであることを確認してください。

詳しくは、ス [クリプト化された増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255)い。

**ライブWebサイトまたはステージWebサイトのスクリプト化された増分インデックスを実行するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. クリック **[!UICONTROL Scripted Index Now]**.
1. （オプション）インデックスエラーが発生した場合は、をクリックし **[!UICONTROL View Errors]** て関連付けられたログを表示します。

## ライブWebサイトまたはステージングされたWebサイトのスクリプト化された増分インデックスログの表示 {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

ライブのフルスクリプトインデックスまたはステージングされたフルスクリプトインデックスが完了すると、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き表示できます。

**ライブWebサイトまたはステージWebサイトの増分インデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * ナビゲーションオプシ **[!UICONTROL First]**&#x200B;ョン、、、、 **[!UICONTROL Prev]**&#x200B;また **[!UICONTROL Next]**&#x200B;はを使 **[!UICONTROL Last]**&#x200B;用して **[!UICONTROL Go to line]** ログ内を移動します。

   * 表示オプション、または **[!UICONTROL Errors only]**&#x200B;を使用 **[!UICONTROL Wrap line]**&#x200B;して、 **[!UICONTROL Show]** 表示内容を調整します。

