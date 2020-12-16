---
description: 単語と言語を使用して、検索用語とWebページのコンテンツとの一致方法を判断できます。
seo-description: 単語と言語を使用して、検索用語とWebページのコンテンツとの一致方法を判断できます。
seo-title: 単語と言語について
solution: Target
title: 単語と言語について
topic: Linguistics,Site search and merchandising
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 1%

---


# 単語と言語について{#about-words-language}

[!DNL Words & Language]を使って、検索用語とWebページのコンテンツとの一致方法を判断できます。

## 単語と言語を使用{#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

[!DNL Words & Language]設定の効果をサイト訪問者が利用できるようにする前に、その設定に対する変更を含めて、サイトインデックスを再生成する必要があります。 インデックス作成とは異なり、再生成を行うと、Webページのクロールは行われず、数秒で済みます。

## 検索用語とWebコンテンツとの一致方法の設定{#task_351A9144A51F4B41923BDBACDEF3B616}

単語と言語を使用して、サイト検索とマーチャンダイジングが検索用語とWebページのコンテンツをどのように一致させるかを判断できます。

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**検索用語とWebコンテンツとの一致方法を設定するには**

1. 製品メニューで、**[!UICONTROL Linguistics]**/**[!UICONTROL Words & Language]**&#x200B;をクリックします。
1. [!DNL Words & Languages]ページで、必要なオプションを設定します。

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
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>大文字と小文字を区別するかどうかを指定します。 例えば、「成功」と「成功」は「成功」と区別され、検索結果はこの2つの間で異なる場合があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>読み分け感度 </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p> 読み分け符号を含む単語を含まない単語と区別するかどうかを指定します。 例えば、選択すると、「pagina」は「pagina」と区別されます。 英語以外の言語を使用するWebサイトがある場合は、このオプションの選択を解除します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>数値 </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p>桁数を含む単語をインデックス化するかどうかを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アポストロフィを無視 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>アポストロフィはクエリから削除されます。 例えば、「Tree's」という検索を行うと、「Trees」という検索と同じ結果が返されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ハイフンを無視 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>ハイフンはクエリから削除されます。 例えば、「blue-bell」という検索を行うと、「bluebell」という検索と同じ結果が返されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>英数字の部分一致 </p> </td> 
      <td colname="col2"> <p>デフォルトでは選択されていません。 </p> <p>このオプションを選択すると、アルファベット順の数値トランジションにトークンを分割して、部品や製品のトークンに対するフリーテキストの一致を許可できます。 </p> <p>例えば、Webサイト上の1つ以上のページの本文コンテンツに<span class="codeph"> 910XT </span>の製品識別子があるとします。 このオプションが<i>選択されて</i>いない&lt;a0/&gt;場合、<span class="keyword">AdobeSearch&amp;Promote</span>は、<span class="codeph"> 910XT </span>を検索する際に、この製品識別子に対する一致を検索します。 そして、<span class="uicontrol"> Search Concat-Div-Enable </span>をオンにすると、<span class="keyword">AdobeSearch&amp;Promote</span>も<span class="codeph"> 910 XT </span>を見つけ出します。 しかし、<span class="codeph"> 910 </span>や<span class="codeph"> XT </span>のインスタンスは排他的に見つかりません。 </p> <p>「<span class="uicontrol">英数字の部分一致</span>」を選択すると、インデクサーはこれらの英数字の混合トークンを複数のトークンに分割します。 例えば、<span class="codeph"> XYZ123 </span>などの製品識別子は、次の3つのトークンにインデックス化されます。<span class="codeph"> XYZ123 </span>、<span class="codeph"> XYZ </span>、および<span class="codeph"> 123 </span>。 この機能により、これらのバリアントのいずれかに対して検索時のフリーテキストの一致が可能になります。 </p> <p>別の例では、製品識別子<span class="codeph"> AB910XT </span>があるとします。 「<span class="uicontrol">部分的な英数字の一致</span> <i>と</i>に対して<span class="uicontrol">検索コンカット —Div-Enable </span>を有効にすると、<span class="keyword">AdobeSearch&amp;Promote</span>は<span class="codeph"> AB910XT </span>, &lt;a110/&gt; AB </span>、<span class="codeph"> 910 </span>、<span class="codeph"> XT </span>。 <span class="codeph">次に、ユーザが<span class="codeph"> 910XT </span>を検索すると、例えば、<span class="codeph"> 910XT </span>、<span class="codeph"> 910 </span>、または<span class="codeph"> XT </span>のインスタンスも検索できるように拡張する。 </span></p> <p> <p>注意： <span class="uicontrol">検索コンカット —Div-Enable </span>は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </p> <p> <p>注意： <span class="uicontrol">英数字の部分一致</span>は、インデックス付きのすべてのフィールドにグローバルに適用されます。 ただし、これはフリーテキストの一致にのみ影響します。完全一致や範囲の一致には影響しません。 </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>音に似たマッチング </p> </td> 
      <td colname="col2"> <p>デフォルトで選択済み. </p> <p>同じ音の単語は、「health」や「helth」のように一致します。 この機能を使用すると、ユーザーは単語のスペルが誤っていても簡単に検索できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>代替語Forms </p> </td> 
      <td colname="col2"> <p>初期設定は<b>デフォルトの代替単語Forms</b>です。 </p> <p>「代替ワードForms」ドロップダウンリストでは、次のオプションから選択できます。 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>None</b> <p>インデックスの作成中に、ステミングや代替の単語フォームは適用されません。 </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>既定の代替単語Forms</b> <p>ステミングはインデックス作成中に自動的に行われます。 </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>ドメインディクショナリ</b> <p>ステミングディクショナリとして設定したドメインディクショナリは、代替単語フォームのソースとして使用されます。 </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local">辞書</a>についてを参照してください。 </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local">ステミングディクショナリとしてのディクショナリの設定</a>を参照してください。 </p> </li> 
      </ul> </p> <p><span class="keyword">AdobeSearch&amp;Promote</span>でフレーズステミングが有効な場合は、代替単語フォームがフレーズ内でも発生することに注意してください。 </p> <p><a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local">Search&amp;Promote8.15.0リリースノート（2014年6月19日）</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>言語 </p> </td> 
      <td colname="col2"> <p>初期設定は<b>英語（米国）</b>です。 </p> <p>選択した言語により、日付と数値は、世界の選択した部分で使用される規則に従って解析されます。 </p> <p><span class="uicontrol">代替ワードForms</span>が<span class="uicontrol">デフォルトの代替ワードForms</span>または<span class="uicontrol">ドメインディクショナリ</span>に設定されている場合、選択した言語の言語規則に従って、単語の形式と単語の終わりが変わります。 </p> <p>デフォルトでは、Webサイトから読み取るページの言語は、「言語」設定では決定されません。 読み取りページの言語は、そのHTTPヘッダーから、またはページ自体のメタタグから判別されます。 Webサイトには、様々な言語のページを含めることができます。 ここで選択する言語に関係なく、各ページは正しく読み取りおよびインデックス付けされます。 </p> <p>Webサイトの一部のページでUTF-8などのUnicode文字セットエンコーディングを使用する場合は、各ページの言語が正しく指定されていることを確認してください。 適切なHTTPドキュメントまたはメタタグがUnicodeヘッダーに存在しない場合は、<span class="uicontrol">設定</span> &gt; <span class="uicontrol">メタデータ</span> &gt; <span class="uicontrol">インジェクション</span>を使用して、適切な言語を指定できます。 </p> <p>[<span class="uicontrol">ドキュメントに適用しますか？ </span> を使用して、Webサイトから読み取ったページで明示的な設定がないページに対して「言語」設定を使用する場合。ドキュメントの<i>一部の</i>のみに言語設定がない場合に、この設定を使用します。 <span class="uicontrol">設定</span> &gt; <span class="uicontrol">メタデータ</span> &gt; <span class="uicontrol">インジェクション</span>を使用します(ドキュメントの<i>none</i>のいずれかに言語設定がある場合、または影響を受けるドキュメントのセットがよく知られていて、管理性に優れています)。 </p> <p><a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local">インジェクションについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>分解装置を使用しますか？ </p> </td> 
      <td colname="col2"> <p> <p>注意： この機能は、デンマーク語とドイツ語でのみ使用されます。 また、この機能はデフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 有効にした後、<b>Decompounderを使用しますか？</b> 」オプションは、この表で前述した「 <span class="uicontrol"> 言語」 </span> ドロップダウンリストから「デンマーク語」 <span class="uicontrol"> または「 </span>  <span class="uicontrol">  </span> ドイツ語」を選択した場合にのみ、ユーザーインターフェイスに表示されます。 </p> </p> <p><span class="uicontrol"> 「解凍ツールを使用しますか？」 </span>を使用する場合、サービスはデンマーク語またはドイツ語の複合語を分類し、元の複合語と共にコンポーネント語をインデックス化できます。 </p> <p>この機能の動作を確認するには、テキストフィールドに単語を入力し、[<span class="uicontrol">テスト</span>]をクリックします。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Save Settings]**.
1. 変更の結果をプレビューするには、**[!UICONTROL regenerate your staged site index]**&#x200B;をクリックして、ステージングされたWebサイトのインデックスを再構築します。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

