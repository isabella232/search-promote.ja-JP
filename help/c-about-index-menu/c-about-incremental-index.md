---
description: 増分インデックスを使用して、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。
seo-description: 増分インデックスを使用して、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。
seo-title: 増分インデックスについて
solution: Target
subtopic: Incremental Index
title: 増分インデックスについて
topic: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# 増分インデックスについて{#about-incremental-index}

増分インデックスを使用して、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。

## 増分インデックスの使用 {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

増分インデックスは、実行に数秒かかるだけで、完全なインデックス作成までに長時間かかる大容量Webサイトで役立ちます。

増分インデックスを生成すると、インデックス作成プロセス中の開始時間、経過時間、エラーなどのステータス情報が表示されます。 最後のインデックスのステータスに関する情報も表示されます。

増分インデックス作成プロセスは、いつでも停止または再開できます。

ライブWebサイト用に新しい増分インデックスを作成する間、顧客は最後の増分インデックスを使用してサイトを検索し続けることができます。

## ステージングされたWebサイトの増分インデックスの設定 {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

WebサイトのURLとURLマスクを指定することで、増分インデックスに含めるWebサイトページを設定できます。

**ステージングされたWebサイトの増分インデックスを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Incremental Index]** ます **[!UICONTROL Configuration]**。
1. ページ上 **[!UICONTROL Incremental Index Configuration]** で、様々なフィールドを使用して、インデックスを作成するページを指定します。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>フィールド </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URLの追加または更新 </p> </td> 
      <td colname="col2"> <p>URLを指定します。 </p> <p>検索ロボットは、前回インデックスを作成した後に変更された、指定したドキュメントのインデックスのみを作成します。 </p> <p>また、検索ロボットは、指定したドキュメント内のリンクに従い、変更されたドキュメントのみのインデックスを作成します。 </p> <p>次の例のように、このフィールドにはドキュメントURLのみを含め、マスクは含めないでください。 </p> <p> 
        <userinput>
          https://www.mydomain.com/products/new.html 
        </userinput> </p> <p>URLでは、次のキーワードを使用できます。 </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <userinput>
            noindex 
          </userinput> <p>指定したURLと一致するページ上のテキストのインデックスを作成せず、そのページのリンク先に移動する場合は、 
            <userinput>
              noindex 
            </userinput> をURLの後に追加します。 </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html noindex 
            </userinput> </p> <p>必ず別の 
            <userinput>
              noindex 
            </userinput> をスペース付きのURLから取得します。コンマは有効な区切り文字ではありません。 </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <userinput>
            nofollow 
          </userinput> <p>指定したURLと一致するが、ページのリンクをたどる必要がないページ上のテキストのインデックスを作成する場合は、 
            <userinput>
              nofollow 
            </userinput> をURLの後に追加します。 </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html nofollow 
            </userinput> </p> <p> 必ず別の 
            <userinput>
              nofollow 
            </userinput> をスペース付きのURLから取得します。コンマは有効な区切り文字ではありません。 </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクの検索と更新 </p> </td> 
      <td colname="col2"> <p>単純なURLマスク（フルパス、部分パス、ワイルドカードまたは正規表現を使用するパス）を指定します。 </p> <p>検索ロボットは、一致するすべてのドキュメントを検索し、前回インデックスを作成した後に変更されたドキュメントのみをインデックス化します。 </p> <p>また、検索ロボットは、一致するドキュメント内のリンクに従い、変更されたページのみをインデックス化します。 次に例を示します。 </p> <p> 
      <userinput>
        https://www.mydomain.com/products/household/*.html 
      </userinput> </p> <p>次の例のように、正規表現を使用することもできます。 </p> <p> 
      <userinput>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </userinput> </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してください</a>。 </p> <p>また、 
      <userinput>
        nofollow 
      </userinput> および 
      <userinput>
        noindex 
      </userinput> 上記の「URLの追加ま <span class="uicontrol"> たは更新」で説明されて </span> いるとおり。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクを含む/除外する </p> </td> 
      <td colname="col2"> <p>単純なURLマスク（フルパス、部分パス、ワイルドカードまたは正規表現を使用するパス）を含めるか除外するかを指定します。 </p> <p>検索ロボットは、指定されたマスクの種類に基づいて、ドキュメントのインデックス(「include」)を検索するか、ドキュメントを無視します(「exclude」)。 </p> <p> サイトのインデックスを作成する際には、表示順に指示に従います。 例えば、次のマスクのリストが表示されます。 </p> <p> 
      <userinput>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </userinput> </p> <p> 
      <userinput>
        除外https://www.mydomain.com/products/ 
      </userinput> </p> <p>ページのインデックス 
      <userinput>
        lightbulbs1.html 
      </userinput> および 
      <userinput>
        lightbulbs2.html 
      </userinput> ただし、productsディレクトリの下に表示される他のページのインデックスは作成されません。 </p> <p>最初に表示されるURLマスクは、常にリストの後ろに表示されるURLマスクより優先されます。 また、検索ロボットが「含むマスク」と「除外するマスク」の両方に一致するドキュメントを検出した場合は、最初に表示されるマスクが優先されます。 </p> <p>また、 
      <userinput>
        nofollow 
      </userinput> および 
      <userinput>
        noindex 
      </userinput> 上記の「URLの追加ま <span class="uicontrol"> たは更新」で説明されて </span> いるとおり。 </p> <p>URLマスクにつ <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> いてを参照してください</a>。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>日付マスクを含む/除外する </p> </td> 
      <td colname="col2"> <p>単純な日付マスクを含めるか除外するかを指定します。つまり、フルパス、部分パス、ワイルドカードや正規表現を使用するパスを指定します。 </p> <p>検索ロボットは、URLとドキュメントの日付の両方に基づいて、ドキュメントのインデックス(「include」)を検索するか、ドキュメントを無視します(「exclude」)。 </p> <p>次のタイプの日付マスクを使用できます。 </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <userinput>
        include-days NNN 
      </userinput> <p>検索ロボットは、指定したURLマスクに一致し、NNN日以上前のすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後に、次のキーワードを1つ以上指定できます。 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">server-date </li> 
        </ul> </p> <p>例えば、次のマスクは、/archive/supportフォルダー内の0日以上前のすべてのドキュメントを含みます。 </p> <p> 
        <userinput>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </userinput> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <userinput>
        include-date YYYY-MM-DD 
      </userinput> <p>検索ロボットは、指定したURLマスクに一致し、YYYY-MM-DD日付より古い、または古いすべてのドキュメントのインデックスを作成します。 </p> <p>URLマスクの後に、次のキーワードを1つ以上指定できます。 </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> server-date </li> 
        </ul> </p> <p>次のマスクの例では、2011年7月25日以前の日付の/archive/フォルダー内のすべてのドキュメントが含まれています。 </p> <p> 
        <userinput>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <userinput>
        exclude-days NNN 
      </userinput> <p>指定したURLマスクと一致し、NNN日以上前のドキュメントのインデックス作成を無効にします。 </p> <p>オプションで、URLマスクの後にキーワードを付けることもできます 
        <userinput>
          server-date 
        </userinput>。 </p> <p>次のマスクの例では、90日前またはそれより古いPDFファイルをインデックスから除外します。 </p> <p> 
        <userinput>
          exclude-days 90 *.pdf 
        </userinput> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <userinput>
        exclude-date YYYY-MM-DD 
      </userinput> <p>指定したURLマスクに一致し、YYYY-MM-DDより古い、または古いすべてのドキュメントのインデックス作成を無効にします。 </p> <p>オプションで、URLマスクの後にキーワードを付けることもできます 
        <userinput>
          server-date 
        </userinput>。 </p> <p>次のマスクの例では、2004年4月23日以前の日付の/archive/フォルダー内のすべてのドキュメントを除外します。 </p> <p> 
        <userinput>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      </ul> </p> <p>日付マスク <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> についてを参照してくださ</a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLの削除 </p> </td> 
      <td colname="col2"> <p>URLを指定します。 </p> <p>検索ロボットは、指定されたドキュメントを検索インデックスから検索および削除します。 指定したページが既に検索インデックスに含まれている場合は、他のページを追加または更新する前に削除されます。 </p> <p>このフィールドには、ドキュメントURLのみを含め、マスクは含めないでください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URLマスクの検索と削除 </p> </td> 
      <td colname="col2"> <p>単純なURLマスク（フルパス、部分パス、ワイルドカードまたは正規表現を使用するURLマスク）を指定します。 </p> <p>指定したURLマスクが検索インデックス内のページと一致する場合、検索ロボットはページを削除してから、他のページを追加または更新します。 次に例を示します。 </p> <p> 
      <userinput>
        https://www.mydomain.com/products/1998/household/* 
      </userinput> </p> <p>次の例のように、正規表現を使用することもできます。 </p> <p> 
      <userinput>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </userinput> </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してください</a>。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## ライブWebサイトのインクリメンタルインデックススケジュールの設定 {#task_2A46BA189ECC4317A9D5C6E99A336F33}

増分インデックスの頻度と、増分インデックスのクロールと更新に使用する基準時間を選択できます。

選択した時刻は、[アカウントの設定]で設定したタイムゾーンに従ってローカルに表示されます。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

多くの場合、深夜には、メンテナンスのためにウェブサーバがダウンする予定です。 スケジュールされたインデックス時間中にサーバーがダウンした場合、インデックス作成処理は失敗します。 Webサーバーが利用可能な時間帯を選択していることを確認してください。

インデックススケジュールは、ライブインデックスにのみ適用されます。ステージングされたインデックスはスケジュールできません。

**ライブWebサイトのインクリメンタルインデックススケジュールを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Incremental Index]** ます **[!UICONTROL Live Schedule]**。
1. [ページ内]のドロ **[!UICONTROL Incremental Index Schedule]** ップダウンリスト **[!UICONTROL Incrementally Index]** で、インデックス作成の頻度を時間単位または分単位で選択します。
1. ドロップダ **[!UICONTROL Base Time]** ウンリストで、新しい増分インデックスを再生成する開始時間を選択します。
1. クリック **[!UICONTROL Save Changes]**.

## ライブWebサイトまたはステージWebサイトの増分インデックスの実行 {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

増分インデックスを使用して、頻繁に変更されるページの集まりなど、ライブWebサイトやステージングされたWebサイトの「断片」のインデックスを作成できます。

**ライブWebサイトまたはステージWebサイトの増分インデックスを実行するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. クリック **[!UICONTROL Incremental Index Now]**.
1. （オプション）インデックスエラーが発生した場合は、をクリックし **[!UICONTROL View Errors]** て関連付けられたログを表示します。

## ライブまたはステージングされたWebサイトの増分インデックスログの表示 {#task_E668E1F1240C476DAA1CA783DC728232}

ライブインクリメンタルインデックスまたはステージインクリメンタルインデックスが完了すると、関連するログを表示して、発生したエラーのトラブルシューティングを行うことができます。


ログをエクスポートしたり、保存したりすることはできません。 ログは、新しいインデックスが発生するまで表示可能なままです。

**ライブWebサイトまたはステージWebサイトの増分インデックスログを表示するには**

1. 製品メニューで、次のいずれかの操作を行います。

   * Click **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Click **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. ログページの上部または下部で、次のいずれかの操作を行います。

   * ナビゲーションオプシ **[!UICONTROL First]**&#x200B;ョン、、、、 **[!UICONTROL Prev]**&#x200B;また **[!UICONTROL Next]**&#x200B;はを使 **[!UICONTROL Last]**&#x200B;用して **[!UICONTROL Go to line]** ログ内を移動します。

   * 表示オプション、または **[!UICONTROL Errors only]**&#x200B;を使用 **[!UICONTROL Wrap line]**&#x200B;して、 **[!UICONTROL Show]** 表示内容を調整します。

