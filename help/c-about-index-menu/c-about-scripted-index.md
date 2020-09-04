---
description: スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスオプションを書き込み、更新、維持できます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。
seo-description: スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスオプションを書き込み、更新、維持できます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。
seo-title: スクリプトインデックスについて
solution: Target
subtopic: Scripted Index
title: スクリプトインデックスについて
topic: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 1%

---


# スクリプトインデックスについて{#about-scripted-index}

スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスオプションを書き込み、更新、維持できます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。

## スクリプトインデックスの使用 {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## スクリプトの増分インデックスの設定について {#section_161D254065E143F3A39F3FC09C400090}

スクリプトインデックスを使用するには、スクリプトインクリメンタルインデックス設定ページを使用して、サーバー上にあるスクリプトファイル（プレーンテキストファイル）のURLを指定します。 例： `https://www.mysite.com/indexlist.txt`サイトが変更されると、手動または自動（ニュースフィード、株価、その他の変更されたファイルからの情報の受信によってトリガーされるスクリプトを使用）でテキストファイルにコマンドブロックを追加できます。

スクリプトの増分インデックスが開始されると、検索ロボットはテキストファイルを読み取り、そのファイル内の新しいコマンドを実行します。 デフォルトでは、検索ロボットは新しいコマンドのみを処理し、これはファイルの日付によって決まります。 スクリプトインデックス **[!UICONTROL Clear Date]** を設定する際にチェックを入れない限り、検索ロボットは最近処理されたブロックの日付指定子を「記憶」します。

## スクリプトファイルについて {#section_B312E40539F44C6583B4F9637D428E19}

URLで指定するスクリプトファイルは、サーバー上のプレーンテキストファイルです。 行末シーケンスには、キャリッジリターン、ラインフィード、またはその両方を使用できます。 空白行には、0個以上の空白文字の後に行末のシーケンスが続きます。 すべてのコマンドでは、大文字と小文字が区別されません。

テキストファイルは、スクリプト化された増分インデックスを実行する際に検索ロボットが使用する情報を記述するブロックで構成されます。

ブロックは日付順に並べられ、最も古いブロックがテキストファイルの先頭に、最も新しいブロックが下に表示されます。 各ブロックは、1行のdate-commandとdate-specifierコマンドで始まり、次のブロック例のように空白行区切りで終わります（間に複数のコマンドがあります）。

HTTP 1.1スタイルを使用する場合、序数が10より小さいすべての日付に対して、先頭にゼロを付ける必要があります。 例えば、11月6日は11月6日ではなく、11月6日です。

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
   <td colname="col2"> <p>各ブロック開始の最初の行に、次の2つの日付コマンドのいずれかが含まれます。 </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> date </span> <p>「date」コマンドを使用して、日付指定子が日、日、時刻、およびタイムゾーンで構成されることを示します。 </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> 秒 </span> <p>日付指定子がエポック秒の時間で構成されることを示す <span class="codeph"></span> には、「秒」を使用します（例：78411777）。 秒数を使用する場合は、 <span class="codeph"></span>ブロック間の秒数が増えることを確認してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p>date-specifierコマンドは、通常、 <span class="codeph"></span> ブロック情報がファイルに追加された日付と時刻（dateコマンド）、またはエポック秒（secondsコマンド）の時刻を記録します。 次に例を示します。 </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>HTTP 1.1スタイルを使用する場合、序数が10より小さいすべての日付に対して、先頭にゼロを付ける必要があります。 例えば、11月6日は11月6日ではなく、11月6日です。 </p> <p>検索ロボットは、最も最近処理されたブロックの日付指定子を「記憶」し、「新しい」と見なされる情報のみをインデックス化します。 (リアルタイムは検索ロボットには関係ありません。 その代わりに、前に処理された他の時間との関係が重要です。) </p> <p>例えば、検索ロボットが日付指定子が10:00 p.mのブロックを読み取った後、インデックス操作の実行時間に関係なく、午後10:00以前の時刻を記録するブロックは読み取りません。 ワーストケースシナリオでは、日付指定子に誤って「2004」ではなく「2040」と入力する場合があります。 この場合、検索ロボットは次のインデックス作成操作中に2040ブロックのインデックスを作成し、その後（2040年の日付が1つ以外の場合）他の情報ブロックの読み取りを拒否します。 この問題が発生する場合は、前に処理されたすべてのブロックをテキストファイルから削除し、「 <span class="uicontrol"> 日付をクリア」をクリックし </span>てから、アクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>コメント行 </p> </td> 
   <td colname="col2"> <p>コメント行の先頭には「#」文字を付けます。 </p> <p>各コメント行は、それぞれ独自の行でなければなりません。行末コメントを入力することはできません。 </p> <p>コメント行は、空白行と見なされません。 また、次の例のように、日付や秒コマンドの前でも、ブロック内の任意の場所に表示できます。 </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-command </p> </td> 
   <td colname="col2"> <p>各テキストブロックには、必要な数のアクションコマンドを含めることができます。 次のアクションコマンドオプションは、標準の増分インデックスのオプションに対応します。 </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <code>
         add 
       </code> <p>URLと共に使用します。 検索ロボットは、前回のインデックス作成操作以降に変更された、指定したURLのみをインデックス化します。 また、検索ロボットは、指定したドキュメント内に含まれるリンクに従い、変更されたドキュメントのみをインデックス化します。 </p> <p>次の例のように、URLの後に <code>
          nofollow 
        </code> または <code>
          noindex 
        </code> キーワードを付けることができます。 </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>URLマスクと共に使用します。 検索ロボットは、指定したURLマスクに一致するすべてのドキュメントを検索し、更新します。 </p> <p>次の例のように、URLの後に <code>
          nofollow 
        </code> または <code>
          noindex 
        </code> キーワードを付けることができます。 </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <code>
         include 
       </code> または 
       <code>
         exclude 
       </code> <p>URLマスクと共に使用します。 検索ロボットは、指定されたマスクの種類に基づいて、ドキュメントのインデックス(「include」)を作成するか、無視(「exclude」)を作成します。 </p> <p>例： </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p> または </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <code>
         include-date 
       </code> または 
       <code>
         exclude-date 
       </code> <p>URLマスクと共に使用します。 検索ロボットは、URLとドキュメントの日付の両方に基づいて、ドキュメントのインデックス(「include」)を作成するか、無視(「exclude」)を作成します。 次の種類のマスクを使用できます。 </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <code>
            include-days NNN 
          </code> <p>検索ロボットは、指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後にキーワード <code>
             nofollow 
           </code>、 <code>
             noindex 
           </code>またはその両方を付けることができ <code>
             server-date 
           </code>ます。 </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> 検索ロボットは、指定したURLマスクに一致し、YYYY-MM-DD（日付YYYY）より古いすべてのドキュメントのインデックスを作成します。「YYYY」は4桁の年、「MM」は1桁または2桁の月(1 ～ 12)、「DD」は1桁または2桁の日(1 ～ 31)です。 </p> <p>URLマスクの後にキーワード <code>
             nofollow 
           </code>、 <code>
             noindex 
           </code>またはその両方を付けることができ <code>
             server-date 
           </code>ます。 </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> 指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができ <code>
             server-date 
           </code>ます。 </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができ <code>
             server-date 
           </code>ます。 </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <code>
         delete 
       </code> <p>URLを指定します。 検索ロボットは、URLで識別されるインデックスからドキュメントを削除します。 </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <code>
         deletemask 
       </code> <p>検索ロボットは、指定されたURLマスクに一致するインデックスからドキュメントを削除します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

URLマスクにつ [いても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)。

## スクリプトファイルの例 {#section_9F580F20E7214751B157A28B392BD64E}

次のスクリプトファイルの例では、検索ロボットは日付指定子が日付後に指定したブロックを処理します。日付指定子は、最近処理されたブロックの日付指定子です。 その場合、次のインデックス作成操作が実行されます。

* インデックス `y2k-problems.html` から削除します。
* 検索イ `no-y2k-problems.html` ンデックスに追加し、のリンクのどれにも従いません `no-y2k-problems.html`。

* クロール中に、検索インデックスから `housewares.htm` lと一致するURLを除外 `lightfixtures.htm`します。

* の下に他のすべてのディレクトリとドキュメントを含め `www.mydomain.com`ます。
* およびディレクトリ内のすべてのドキュメント `products``information` を更新し、最後のインデックス作成操作以降に変更されたすべての子リンクをクロールしてインデックスを作成します。

* クロール中に、Webサイトの `archive` セクションにあるURLを除外します（URLが1999年1月1日以前の日付の場合）。
* 検索インデックスと一致 `housewares.html` するURLと検索インデックス `lightfixtures.html` からURLを除外します。

* ディレクトリ内のインデックスファイルですが、これらのファイルからのリンクをクロールまたはインデックス付けしないでください。 `help`
* に対して発生した他のファイルをクロールしてインデックスを作成し `www.mydomain.com`ます。

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

作成したスクリプトを指定して、インクリメンタルインデックスの書き込み、更新、維持を行うことができます。ログインは不要です。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取り、増分インデックスを実行します。

**スクリプト化された増分インデックスを設定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Index]** ま **[!UICONTROL Scripted Index]** す **[!UICONTROL Configuration]**。
1. ページの **[!UICONTROL Scripted Incremental Index Configuration]** で、サーバー上にあるテキストファイルスクリプトのURLを **[!UICONTROL Script File URL]**&#x200B;入力します。

   「Scripted Index [について](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)」を参照してください。
1. （オプション）検索ロボット **[!UICONTROL Clear Date]** に、最近処理されたブロックの日付指定子を「記憶」させないかどうかをチェックします。

   デフォルトでは、検索ロボットはテキストファイル内の新しいコマンドブロック（ファイルの日付によって決まる）のみを処理します。 デフォルトを使用しない場合は、チェックをオンにし **[!UICONTROL Clear Date]**&#x200B;ます。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## ライブWebサイト用のスクリプト化された増分インデックススケジュールの設定 {#task_B3A87AC4AC784507859C23B9062BA11C}

1日を通して定期的にスクリプトの増分インデックスが行われるように、スケジュールを設定できます。

選択する基本時刻は、「アカウントの設定」で設定したタイムゾーンに応じてローカルになります。

「アカウント設定の [指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

多くの場合、Webサーバーは、深夜にメンテナンスのためにダウンする予定です。 スケジュールされたインデックス時間中にサーバーがダウンした場合、インデックス作成プロセスは失敗します。 Webサーバーが利用可能な時間帯を選択していることを確認してください。

インデックススケジュールは、ライブインデックスにのみ適用されます。ステージインクリメンタルインデックスはスケジュールできません。

**ライブWebサイト用のスクリプト化された増分インデックススケジュールを設定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Index]** ま **[!UICONTROL Scripted Index]** す **[!UICONTROL Live Schedule]**。
1. ページのドロップダウン **[!UICONTROL Scripted Incremental Index Schedule]****[!UICONTROL Read the Scripted Incrementally Indexing File]** リストで、スクリプト増分インデックステキストファイルを実行する頻度を、時間単位または分単位で選択します。
1. ドロップダウンリストで、新しいスクリプト付き増分インデックスを再生成する開始時間を選択します。 **[!UICONTROL Base Time]**
1. クリック **[!UICONTROL Save Changes]**.

## ライブWebサイトまたはステージングされたWebサイトのスクリプト化された増分インデックスの実行 {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

スクリプト付き増分インデックスを使用すると、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成でき、ログインする必要がありません。

この機能を使用するには、スクリプト化されたインクリメンタルインデックステキストファイルを必ず設定してください。

詳しくは、スクリプト増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255)。

**ライブWebサイトまたはステージングされたWebサイトのスクリプト化された増分インデックスを実行するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. クリック **[!UICONTROL Scripted Index Now]**.
1. （オプション）インデックス作成エラーが発生した場合は、をクリックして関連するログ **[!UICONTROL View Errors]** を表示します。

## ライブWebサイトまたはステージングされたWebサイトのスクリプト化された増分インデックスログの表示 {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

ライブフルスクリプトインデックスまたはステージフルスクリプトインデックスが完了した場合、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き閲覧可能です。

**ライブWebサイトまたはステージングされたWebサイトの増分インデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * ナビゲーションオプション **[!UICONTROL First]**、、、、 **[!UICONTROL Prev]**&#x200B;またはを使用して、ログ内 **[!UICONTROL Next]****[!UICONTROL Last]****[!UICONTROL Go to line]** を移動します。

   * 表示オプション **[!UICONTROL Errors only]**、 **[!UICONTROL Wrap line]**&#x200B;または **[!UICONTROL Show]** を使用して、表示内容を調整します。

