---
description: 増分インデックスを使用すると、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。
solution: Target
subtopic: Incremental Index
title: 増分インデックスについて
topic-legacy: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
exl-id: 41943f84-23f0-434c-8eef-a9075dd5c03d
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 0%

---

# 増分インデックスについて{#about-incremental-index}

増分インデックスを使用すると、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。

## 増分インデックスの使用{#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

増分インデックスの実行に要する時間は数秒で、完全なインデックス作成までに数時間かかる大容量Webサイトで役立ちます。

増分インデックスを生成すると、インデックス作成プロセス中の開始時間、経過時間、エラーなどのステータス情報が表示されます。 最後のインデックスの状態に関する情報も表示されます。

増分インデックス作成プロセスは、いつでも停止または再開できます。

新しい増分インデックスが本番用Webサイトに作成される間、ユーザーは最後の増分インデックスを使用してサイトを検索し続けることができます。

## ステージングされたWebサイトの増分インデックスの設定{#task_46A367B0786C4C90BFFA5D3F95FD86C0}

WebサイトのURLとURLマスクを指定することで、インクリメンタルインデックスに含めるWebサイトページを設定できます。

**ステージングされたWebサイトの増分インデックスを構成するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Configuration]**&#x200B;をクリックします。
1. **[!UICONTROL Incremental Index Configuration]**&#x200B;ページで、様々なフィールドを使用して、インデックスを作成するページを指定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>フィールド </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>または追加URLの更新 </p> </td> 
      <td colname="col2"> <p>URLを指定します。 </p> <p>検索ロボットは、最後にインデックスを作成した後に変更された、指定したドキュメントのみをインデックス化します。 </p> <p>また、検索ロボットは、指定したドキュメント内のリンクに従い、変更されたドキュメントのみをインデックス化します。 </p> <p>次の例のように、このフィールドにはドキュメントURLのみを含め、マスクは含めません。 </p> <p> 
        <code>
          https://www.mydomain.com/products/new.html 
        </code> </p> <p>URLで使用できるキーワードは次のとおりです。 </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <code>
            noindex 
          </code> <p>指定したURLと一致するページ上のテキストのインデックスを作成せず、そのページのリンクに従う場合は、 
            次の例のように、URLの後に<code>
              noindex 
            </code>が続きます。 </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html noindex 
            </code> </p> <p>必ず別の 
            <code>
              noindex 
            </code>をURLからスペースで囲み、コンマは有効な区切り文字ではありません。 </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <code>
            nofollow 
          </code> <p>指定したURLと一致するが、ページのリンクに従わないページ上のテキストのインデックスを作成する場合は、 
            次の例のように、URLの後に<code>
              nofollow 
            </code>が続きます。 </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html nofollow 
            </code> </p> <p> 必ず別の 
            <code>
              nofollow 
            </code>をURLからスペースで囲み、コンマは有効な区切り文字ではありません。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクの検索と更新 </p> </td> 
      <td colname="col2"> <p>単純なURLマスク(フルパス、部分パス、ワイルドカードまたは正規式を使用するパス)を指定します。 </p> <p>検索ロボットは、一致するすべてのドキュメントを検索し、最後にインデックスを作成した後に変更されたドキュメントのみをインデックス化します。 </p> <p>また、検索ロボットは、一致するドキュメント内のリンクに従い、変更されたページのみをインデックス化します。 次に例を示します。 </p> <p> 
      <code>
        https://www.mydomain.com/products/household/*.html 
      </code> </p> <p>次の例のように、正規式も使用できます。 </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </code> </p> <p>「<a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>」を参照してください。 </p> <p>また、 
      <code>
        nofollow 
      </code>と 
      <code>
        noindex 
      </code>を参照してくだ追加さい。<span class="uicontrol"></span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクを含める/除外する </p> </td> 
      <td colname="col2"> <p>単純なURLマスクを含めるまたは除外する、フルパス、部分パス、ワイルドカードまたは正規式を使用するパスを指定します。 </p> <p>検索ロボットは、指定されたマスクの種類に基づいて、ドキュメントのインデックス(「include」)を作成するか、無視(「exclude」)を作成します。 </p> <p> サイトのインデックス付けを行う場合は、表示順に指示に従います。 例えば、次のリストのマスクを使用できます。 </p> <p> 
      <code>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </code> </p> <p> 
      <code>
        exclude https://www.mydomain.com/products/ 
      </code> </p> <p>ページのインデックス 
      <code>
        lightbulbs1.html 
      </code>と 
      <code>
        lightbulbs2.html 
      </code>. ただし、productsディレクトリにリストされている他のページのインデックスは作成されません。 </p> <p>最初に表示されるURLマスクは、リストの後ろに表示されるURLマスクよりも常に優先されます。 また、検索ロボットが「含むマスク」と「除外するマスク」の両方に一致するドキュメントを検出すると、最初に表示されるマスクが優先されます。 </p> <p>また、 
      <code>
        nofollow 
      </code>と 
      <code>
        noindex 
      </code>を参照してくだ追加さい。<span class="uicontrol"></span> </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URLマスクについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>日付マスクを含める/除外する </p> </td> 
      <td colname="col2"> <p>単純な日付マスクを含めるまたは除外する、フルパス、部分パス、ワイルドカードまたは正規式を使用するパスを指定します。 </p> <p>検索ロボットは、URLとドキュメント日の両方に基づいて、ドキュメントの検索とインデックス(「include」)または無視(「exclude」)を行います。 </p> <p>次の種類の日付マスクを使用できます。 </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <code>
        include-days NNN 
      </code> <p>検索ロボットは、指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後には、次のキーワードを1つ以上追加できます。 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">server-date </li> 
        </ul> </p> <p>例えば、次のマスクは、/archive/supportフォルダー内の0日以上前のドキュメントをすべて含めます。 </p> <p> 
        <code>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </code> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <code>
        include-date YYYY-MM-DD 
      </code> <p>検索ロボットは、指定したURLマスクに一致し、YYYY-MM-DD日付より古い、または古いすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後には、次のキーワードを1つ以上追加できます。 </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> server-date </li> 
        </ul> </p> <p>次のマスクの例には、2011年7月25日以前の/archive/フォルダー内のすべてのドキュメントが含まれています。 </p> <p> 
        <code>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <code>
        exclude-days NNN 
      </code> <p>指定したURLマスクに一致し、NNN日以上経過しているすべてのドキュメントのインデックス作成を無効にします。 </p> <p>オプションで、URLマスクをキーワードでフォローできます 
        <code>
          server-date 
        </code>. </p> <p>次のマスクの例では、90日前以前のPDFファイルをすべてインデックスから除外します。 </p> <p> 
        <code>
          exclude-days 90 *.pdf 
        </code> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <code>
        exclude-date YYYY-MM-DD 
      </code> <p>指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックス作成を無効にします。 </p> <p>オプションで、URLマスクをキーワードでフォローできます 
        <code>
          server-date 
        </code>. </p> <p>次のマスクの例では、2004年4月23日以前の/archive/フォルダー内のすべてのドキュメントーが除外されます。 </p> <p> 
        <code>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      </ul> </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local">日付マスクについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLの削除 </p> </td> 
      <td colname="col2"> <p>URLを指定します。 </p> <p>検索ロボットは、検索インデックスから指定されたドキュメントを検索し削除します。 指定したページが既に検索インデックスに含まれている場合、ロボットはそのページを削除してから、他のページを追加または更新します。 </p> <p>このフィールドには、ドキュメントURLのみを含め、マスクは含めないでください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクの検索と削除 </p> </td> 
      <td colname="col2"> <p>単純なURLマスク(フルパス、部分パス、ワイルドカードまたは正規式を使用するURLマスク)を指定します。 </p> <p>指定したURLマスクが検索インデックス内のページと一致する場合、検索ロボットはページを削除してから、他のページを追加または更新します。 次に例を示します。 </p> <p> 
      <code>
        https://www.mydomain.com/products/1998/household/* 
      </code> </p> <p>次の例のように、正規式も使用できます。 </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </code> </p> <p>「<a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>」を参照してください。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## ライブWebサイト{#task_2A46BA189ECC4317A9D5C6E99A336F33}の増分インデックススケジュールの設定

増分インデックスの頻度と、増分インデックスのクロールと更新に使用する基準時間を選択できます。

選択する時刻は、「アカウントの設定」で設定したタイムゾーンに応じてローカルに設定されます。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

多くの場合、Webサーバーは、深夜にメンテナンスのためにダウンする予定です。 スケジュールされたインデックス時間中にサーバーがダウンした場合、インデックス作成プロセスは失敗します。 Webサーバーが利用可能な時間帯を選択していることを確認してください。

インデックススケジュールは、ライブインデックスにのみ適用されます。ステージングされたインデックスはスケジュールできません。

**ライブWebサイトのインクリメンタルインデックススケジュールを設定するには**

1. 製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Live Schedule]**&#x200B;をクリックします。
1. **[!UICONTROL Incremental Index Schedule]**&#x200B;ページの&#x200B;**[!UICONTROL Incrementally Index]**&#x200B;ドロップダウンリストで、インデックス作成頻度を時間単位または分単位で選択します。
1. **[!UICONTROL Base Time]**&#x200B;ドロップダウンリストで、新しい増分インデックスを再生成する開始時間を選択します。
1. クリック **[!UICONTROL Save Changes]**.

## ライブWebサイトまたはステージWebサイトの増分インデックスの実行{#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

増分インデックスを使用すると、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。

**ライブWebサイトまたはステージングされたWebサイトの増分インデックスを実行するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Live Index]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Staged Index]**&#x200B;をクリックします。

1. クリック **[!UICONTROL Incremental Index Now]**.
1. （オプション）インデックス作成エラーが発生した場合は、**[!UICONTROL View Errors]**&#x200B;をクリックして関連するログを表示します。

## ライブWebサイトまたはステージWebサイトの増分インデックスログの表示{#task_E668E1F1240C476DAA1CA783DC728232}

ライブ増分インデックスまたはステージ増分インデックスが完了した場合、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。


ログをエクスポートしたり、保存したりすることはできません。 ログは、新しいインデックスが発生するまで表示可能です。

**ライブWebサイトまたはステージングされたWebサイトの増分インデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * **[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Live Log]**&#x200B;をクリックします。

   * **[!UICONTROL Index]**/**[!UICONTROL Incremental Index]**/**[!UICONTROL Staged Log]**&#x200B;をクリックします。

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * **[!UICONTROL First]**、**[!UICONTROL Prev]**、**[!UICONTROL Next]**、**[!UICONTROL Last]**、または&#x200B;**[!UICONTROL Go to line]**&#x200B;のナビゲーションオプションを使用してログ内を移動します。

   * 表示オプション&#x200B;**[!UICONTROL Errors only]**、**[!UICONTROL Wrap line]**、または&#x200B;**[!UICONTROL Show]**&#x200B;を使用して、表示内容を絞り込みます。
