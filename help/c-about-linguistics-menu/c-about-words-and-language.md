---
description: 「単語と言語」を使用して、検索用語とWebページのコンテンツとの一致方法を判断できます。
seo-description: 「単語と言語」を使用して、検索用語とWebページのコンテンツとの一致方法を判断できます。
seo-title: 単語と言語について
solution: Target
title: 単語と言語について
topic: Linguistics,Site search and merchandising
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 単語と言語について{#about-words-language}

を使用して、検 [!DNL Words & Language] 索用語とWebページのコンテンツとの一致方法を判断できます。

## 単語と言語の使用 {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

設定の効果をサイト訪 [!DNL Words & Language] 問者が利用できるようにする前に、その設定に加えた変更を含めて、サイトインデックスを再生成する必要があります。 インデックス作成とは異なり、再生成時にはWebページのクロールは行われず、数秒で済みます。

## 検索用語とWebコンテンツとの一致方法の設定 {#task_351A9144A51F4B41923BDBACDEF3B616}

単語と言語を使用して、サイト検索/マーチャンダイジングが検索用語とWebページのコンテンツとをどのように一致させるかを判断できます。

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**検索用語とWebコンテンツとの一致方法を設定するには**

1. 製品メニューで、/をクリッ **[!UICONTROL Linguistics]** クしま **[!UICONTROL Words & Language]**&#x200B;す。
1. ページ [!DNL Words & Languages] で、必要なオプションを設定します。

   <!-- 
   
   r_words_and_languages_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>大文字と小文字の区別 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>大文字と小文字を区別するかどうかを指定します。 例えば、選択した場合、「成功」と「成功」は区別され、検索結果はこの2つの間で異なる場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>分音区別 </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p> 読み分け符号を含む単語を含まない単語と区別するかどうかを指定します。 例えば、「pagina」を選択すると、「pagina」と区別されます。 英語以外の言語を使用するWebサイトがある場合は、このオプションの選択を解除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>数値 </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p>数字を含む単語のインデックスを作成するかどうかを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アポストロフィを無視 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>アポストロフィはクエリから削除されます。 例えば、「Tree's」を検索すると、「Trees」を検索した場合と同じ結果が返されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ハイフンを無視 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>ハイフンはクエリから削除されます。 例えば、「blue-bell」を検索すると、「bluebell」を検索した場合と同じ結果が返されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>英数字の部分一致 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>このオプションを選択すると、アルファベット順の数値の遷移でトークンを分割し、一部または製品のトークンでフリーテキストの一致を許可できます。 </p> <p>例えば、Webサイト上の1つ以上のページの本文コンテンツに <span class="codeph"> 910XT </span> の製品識別子があるとします。 このオプションを選択 <i>しない</i> 場合、 <span class="keyword"> Adobe Search&amp;Promoteは </span> 910XTを検索する際に、この製品IDに一致するものを検索しま <span class="codeph"></span>す。 また、「 <span class="uicontrol"> Search Concat-Div-Enable」をオンにす </span> ると、 <span class="keyword"> Adobe Search&amp;Promoteでも </span> 910 XTが見つかります <span class="codeph"></span>。 ただし、 <span class="codeph"> 910またはXTのインスタンスが排他的に見つか </span> るわけで <span class="codeph"> はあり </span> ません。 </p> <p>「英数字の部分一致」を <span class="uicontrol"> 選択すると、イ </span>ンデクサーはこれらの英数字の混合トークンを複数のトークンに分割します。 例えば、XYZ123などの製品識別子は、次の3つのト <span class="codeph"> ークンに </span> インデックス化されます。 <span class="codeph"> XYZ123、 </span>XYZ <span class="codeph"> 、 </span>および <span class="codeph"> 123 </span>。 この機能により、検索時のフリーテキストの一致がこれらのバリエーションのいずれかに対して可能になります。 </p> <p>別の例では、製品識別子AB910XTがあるとし <span class="codeph"> ます </span>。 半英数字半角英数字半角文字一致を選択し <span class="uicontrol"> 、 </span> Search <i>Concconccc</i> -Div-Div-Enableを有効にすると、adobe Search <span class="uicontrol"> &amp;Promoteではindexeを有効にし、AB </span><span class="keyword"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>Search Promoteとし、AB 9 次に、例えば、 <span class="codeph"> 910XTを検索すると、910XT、910 </span>XT、 <span class="codeph"> XTを展開する、 </span>XTのインスタンスも検索され <span class="codeph"> ま </span><span class="codeph"></span>す。 </p> <p> <p>注意： 「 <span class="uicontrol"> Concat-Div-Enableの検索」は、デフォ </span> ルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </p> <p> <p>注意： 英数字の部 <span class="uicontrol"> 分一致は、す </span> べてのインデックス付きフィールドにグローバルに適用されます。 ただし、これはフリーテキストの一致にのみ影響します。完全一致や範囲の一致には影響しません。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>音に似たマッチング </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p>同じように聞こえる単語は、「health」や「helth」などと一致します。 この機能を使用すると、ユーザーは単語のスペルミスにかかわらず簡単に検索できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>代替単語フォーム </p> </td> 
      <td colname="col2"> <p>初期設定は <b>Default Alternate Word Formsです</b>。 </p> <p>「代替単語フォーム」ドロップダウンリストで、次のオプションから選択できます。 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>None</b> <p>インデックス作成中に、語幹決定や代替の単語フォームは適用されません。 </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>デフォルトの代替単語フォーム</b> <p>インデックス付け中に、ステミングが自動的に行われます。 </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>ドメインディクショナリ</b> <p>ステミングディクショナリとして設定したドメインディクショナリは、代替単語フォームのソースとして使用されます。 </p> <p>辞書につ <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> いてを参照してくだ </a>さい。 </p> <p>詳しくは、 <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> 辞書をステミング辞書として設定するを参照してくだ </a>さい。 </p> </li> 
      </ul> </p> <p>Adobe Search&amp;Promoteでフレーズステミングが有効にな <span class="keyword"> っている場合は、フレ </span>ーズ内で代替単語フォームも発生することに注意してください。 </p> <p>「 <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Search&amp;Promote 8.15.0リリースノート（2014年6月20日）」を参照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>言語 </p> </td> 
      <td colname="col2"> <p>初期設定 <b>は英語（米国）です</b>。 </p> <p>選択した言語により、日付と数値が、選択した地域で使用されている規則に従って解析されます。 </p> <p>「代替ワ <span class="uicontrol"> ードフォーム」が「デフォルトの </span> 代替ワードフォーム」または「ドメイ <span class="uicontrol"> ン辞書」に設定されている場合、選択した言語の言語ルールに従って、単語フ </span><span class="uicontrol"></span>ォームと単語の終わりが変更されます。 </p> <p>デフォルトでは、Webサイトから読み取るページの言語は、「言語」設定では決まりません。 読み取りページの言語は、HTTPヘッダーまたはページ自体のメタタグから決定されます。 Webサイトには、様々な言語のページを含めることができます。 ここで選択した言語に関係なく、各ページの読み取りとインデックス作成が正しく行われます。 </p> <p>Webサイトの一部のページでUTF-8などのUnicode文字セットエンコーディングを使用する場合は、各ページの言語が正しく指定されていることを確認します。 適切なHTTPヘッダーまたはメタタグがUnicodeドキュメントに存在しない場合は、設定/メタデータ/インジェクションを使用して、 <span class="uicontrol"> 適切な言 </span> 語を指 <span class="uicontrol"> 定するこ </span><span class="uicontrol"></span> とができます。 </p> <p>「言語が指 <span class="uicontrol"> 定されていない文書に適用しますか？」を選択します。 </span> を使用して、Webサイトから読み取ったページで明示的な設定がないページの言語設定を使用します。 この設定は、一部のドキュメ <i>ント</i> に言語設定がない場合にのみ使用します。 言語設定を <span class="uicontrol"> 含むドキ </span> ュメントの場合は <span class="uicontrol"> 、 None </span><span class="uicontrol"></span><i></i> / Metadata &gt; Injectionsを使用します。影響を受けるドキュメントのセットは、よく知られていて管理が容易な小さなリストです。 </p> <p>注射につい <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> てを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>分解装置を使用しますか？ </p> </td> 
      <td colname="col2"> <p> <p>注意： この機能は、デンマーク語とドイツ語でのみ使用されます。 また、この機能はデフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 有効にした後、「解凍を使用し <b>ますか？」</b> オプションは、この表で前述した言語ドロップダウンリストから「デン <span class="uicontrol"> マーク語」または「ド </span> イツ語」を選択した場 <span class="uicontrol"></span><span class="uicontrol"></span> 合にのみ、ユーザーインターフェイスに表示されます。 </p> </p> <p>「解凍ツールを使用」を選 <span class="uicontrol"> 択した場合は、 </span>の場合、サービスはデンマーク語またはドイツ語の複合語を分類し、元の複合語と共にコンポーネント語のインデックスを作成できます。 </p> <p>この機能の動作を確認するには、テキストフィールドに単語を入力し、「テスト」をクリック <span class="uicontrol"> しま </span>す。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Settings]**.
1. 変更の結果をプレビューするには、をクリックして、ステージ **[!UICONTROL regenerate your staged site index]** ングされたWebサイトインデックスを再構築します。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

