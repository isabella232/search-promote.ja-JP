---
description: スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスオプションを書き込み、更新、維持できます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。
solution: Target
subtopic: Scripted Index
title: スクリプトインデックスについて
topic: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1730'
ht-degree: 1%

---


# スクリプトインデックスについて{#about-scripted-index}

スクリプトインデックスを使用すると、ログインしなくても、インクリメンタルインデックスオプションを書き込み、更新、維持できます。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取ります。

## スクリプトインデックスの使用{#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## スクリプトの増分インデックスの設定について{#section_161D254065E143F3A39F3FC09C400090}

スクリプトインデックスを使用するには、スクリプトインクリメンタルインデックス設定ページを使用して、サーバー上にあるスクリプトファイル（プレーンテキストファイル）のURLを指定します。 例： `https://www.mysite.com/indexlist.txt`サイトが変更されると、手動または自動（ニュースフィード、株価、その他の変更されたファイルからの情報の受信によってトリガーされるスクリプトを使用）でテキストファイルにコマンドブロックを追加できます。

スクリプトの増分インデックスが開始されると、検索ロボットはテキストファイルを読み取り、そのファイル内の新しいコマンドを実行します。 デフォルトでは、検索ロボットは新しいコマンドのみを処理し、これはファイルの日付によって決まります。 スクリプトインデックスの設定時に&#x200B;**[!UICONTROL Clear Date]**&#x200B;をチェックしない限り、検索ロボットは最近処理されたブロックの日付指定子を「記憶」します。

## スクリプトファイルについて{#section_B312E40539F44C6583B4F9637D428E19}

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
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> 秒 </span> <p><span class="codeph">秒</span>を使用して、日付指定子がエポック秒の時間で構成されることを示します（例：78411777）。 <span class="codeph">秒</span>を使用する場合は、ブロック間の秒数が増えることを確認します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p><span class="codeph"> date-specifier </span>コマンドは、通常、ブロック情報がファイルに追加された元の日時（dateコマンド）、またはエポック秒（secondsコマンド）の時間を記録します。 次に例を示します。 </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>HTTP 1.1スタイルを使用する場合、序数が10より小さいすべての日付に対して、先頭にゼロを付ける必要があります。 例えば、11月6日は11月6日ではなく、11月6日です。 </p> <p>検索ロボットは、最も最近処理されたブロックの日付指定子を「記憶」し、「新しい」と見なされる情報のみをインデックス化します。 (リアルタイムは検索ロボットには関係ありません。 その代わりに、前に処理された他の時間との関係が重要です。) </p> <p>例えば、検索ロボットが日付指定子が10:00 p.mのブロックを読み取った後、インデックス操作の実行時間に関係なく、午後10:00以前の時刻を記録するブロックは読み取りません。 ワーストケースシナリオでは、日付指定子に誤って「2004」ではなく「2040」と入力する場合があります。 この場合、検索ロボットは次のインデックス作成操作中に2040ブロックのインデックスを作成し、その後（2040年の日付が1つ以外の場合）他の情報ブロックの読み取りを拒否します。 この問題が発生した場合は、以前に処理されたすべてのブロックをテキストファイルから削除し、「<span class="uicontrol">日付をクリア</span>」をクリックしてから、有効にします。 </p> </td> 
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
       </code> <p>URLと共に使用します。 検索ロボットは、前回のインデックス作成操作以降に変更された、指定したURLのみをインデックス化します。 また、検索ロボットは、指定したドキュメント内に含まれるリンクに従い、変更されたドキュメントのみをインデックス化します。 </p> <p>URLは、 
        <code>
          nofollow 
        </code>または 
        <code>
          noindex 
        </code>キーワードを次の例のように指定します。 </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>URLマスクと共に使用します。 検索ロボットは、指定したURLマスクに一致するすべてのドキュメントを検索し、更新します。 </p> <p>URLは、 
        <code>
          nofollow 
        </code>または 
        <code>
          noindex 
        </code>キーワードを次の例のように指定します。 </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
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
          </code> <p>検索ロボットは、指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>および/または 
           <code>
             server-date 
           </code>。 </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> 検索ロボットは、指定したURLマスクに一致し、YYYY-MM-DD（日付YYYY）より古いすべてのドキュメントのインデックスを作成します。「YYYY」は4桁の年、「MM」は1桁または2桁の月(1 ～ 12)、「DD」は1桁または2桁の日(1 ～ 31)です。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>および/または 
           <code>
             server-date 
           </code>。 </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> 指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックス作成を無効にします。 </p> <p>URLマスクの後にキーワードを付けることができます 
           <code>
             server-date 
           </code>. </p> </li> 
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

[URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)も参照してください。

## スクリプトファイルの例{#section_9F580F20E7214751B157A28B392BD64E}

次のスクリプトファイルの例では、検索ロボットは日付指定子が日付後に指定したブロックを処理します。日付指定子は、最近処理されたブロックの日付指定子です。 その場合、次のインデックス作成操作が実行されます。

* インデックスから`y2k-problems.html`を削除します。
* 検索インデックスに`no-y2k-problems.html`を追加します。`no-y2k-problems.html`のリンクはどれも追いません。

* クロール中に、`housewares.htm`と`lightfixtures.htm`lに一致するURLを検索インデックスから除外します。

* `www.mydomain.com`の下の他のディレクトリとドキュメントをすべて含めます。
* `products`ディレクトリと`information`ディレクトリ内のすべてのドキュメントを更新し、前回のインデックス作成操作以降に変更されたすべての子リンクをクロールしてインデックスを作成します。

* クロール中に、Webサイトの`archive`セクションのURLが1999年1月1日以前の日付の場合は除外します。
* `housewares.html`と`lightfixtures.html`に一致するURLを検索インデックスから除外します。

* `help`ディレクトリ内のインデックスファイルですが、これらのファイルからのリンクをクロールまたはインデックス付けしないでください。
* `www.mydomain.com`に対して検出された他のファイルをクロールしてインデックスを作成します。

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

## スクリプト化された増分インデックスの設定{#task_05AE040FE75E40FFAA5E10B6B6D4D255}

作成したスクリプトを指定して、インクリメンタルインデックスの書き込み、更新、維持を行うことができます。ログインは不要です。 検索ロボットは、サーバー上でホストされているテキストファイルから指示を読み取り、増分インデックスを実行します。

**スクリプト化された増分インデックスを設定するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Configuration]**&#x200B;をクリックします。
1. **[!UICONTROL Scripted Incremental Index Configuration]**&#x200B;ページの&#x200B;**[!UICONTROL Script File URL]**&#x200B;に、サーバー上のテキストファイルスクリプトのURLを入力します。

   「[スクリプトインデックスについて](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)」を参照してください。
1. （オプション）検索ロボットに最近処理されたブロックの日付指定子を「記憶」させない場合は、**[!UICONTROL Clear Date]**&#x200B;をチェックします。

   デフォルトでは、検索ロボットはテキストファイル内の新しいコマンドブロック（ファイルの日付によって決まる）のみを処理します。 デフォルトを使用しない場合は、**[!UICONTROL Clear Date]**&#x200B;をチェックします。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ライブWebサイト用のスクリプト化された増分インデックススケジュールの設定{#task_B3A87AC4AC784507859C23B9062BA11C}

1日を通して定期的にスクリプトの増分インデックスが行われるように、スケジュールを設定できます。

選択する基本時刻は、「アカウントの設定」で設定したタイムゾーンに応じてローカルになります。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

多くの場合、Webサーバーは、深夜にメンテナンスのためにダウンする予定です。 スケジュールされたインデックス時間中にサーバーがダウンした場合、インデックス作成プロセスは失敗します。 Webサーバーが利用可能な時間帯を選択していることを確認してください。

インデックススケジュールは、ライブインデックスにのみ適用されます。ステージインクリメンタルインデックスはスケジュールできません。

**ライブWebサイト用のスクリプト化された増分インデックススケジュールを設定するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Live Schedule]**&#x200B;をクリックします。
1. **[!UICONTROL Scripted Incremental Index Schedule]**&#x200B;ページの&#x200B;**[!UICONTROL Read the Scripted Incrementally Indexing File]**&#x200B;ドロップダウンリストで、スクリプト付き増分インデックステキストファイルを実行する頻度を、時間単位または分単位で選択します。
1. **[!UICONTROL Base Time]**&#x200B;ドロップダウンリストで、新しいスクリプト付き増分インデックスを再生成する開始時間を選択します。
1. クリック **[!UICONTROL Save Changes]**.

## ライブWebサイトまたはステージWebサイトのスクリプト化された増分インデックスの実行{#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

スクリプト付き増分インデックスを使用すると、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成でき、ログインする必要がありません。

この機能を使用するには、スクリプト化されたインクリメンタルインデックステキストファイルを必ず設定してください。

「[スクリプト増分インデックスの設定](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255)」を参照してください。

**ライブWebサイトまたはステージングされたWebサイトのスクリプト化された増分インデックスを実行するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Live Index]**&#x200B;をクリックします。
   * **[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Staged Index]**&#x200B;をクリックします。

1. クリック **[!UICONTROL Scripted Index Now]**.
1. （オプション）インデックス作成エラーが発生した場合は、**[!UICONTROL View Errors]**&#x200B;をクリックして関連するログを表示します。

## ライブWebサイトまたはステージWebサイトのスクリプト化された増分インデックスログの表示{#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

ライブフルスクリプトインデックスまたはステージフルスクリプトインデックスが完了した場合、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。

ログをエクスポートしたり、保存したりすることはできません。 ただし、新しいインデックスが発生するまで、ログは引き続き閲覧可能です。

**ライブWebサイトまたはステージングされたWebサイトの増分インデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Live Log]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Scripted Index]**/**[!UICONTROL Staged Log]**&#x200B;をクリックします。

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * **[!UICONTROL First]**、**[!UICONTROL Prev]**、**[!UICONTROL Next]**、**[!UICONTROL Last]**、または&#x200B;**[!UICONTROL Go to line]**&#x200B;のナビゲーションオプションを使用してログ内を移動します。

   * 表示オプション&#x200B;**[!UICONTROL Errors only]**、**[!UICONTROL Wrap line]**、または&#x200B;**[!UICONTROL Show]**&#x200B;を使用して、表示内容を絞り込みます。

