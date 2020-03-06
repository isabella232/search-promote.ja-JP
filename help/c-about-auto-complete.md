---
description: オートコンプリートの様々な領域を設定して、オートコンプリート対応の検索フォームの生成を制御し、オートコンプリート対応の検索フォームの一部として含まれるautocomplete_data.jsファイルを制御できます。
seo-description: オートコンプリートの様々な領域を設定して、オートコンプリート対応の検索フォームの生成を制御し、オートコンプリート対応の検索フォームの一部として含まれるautocomplete_data.jsファイルを制御できます。
seo-title: オートコンプリートについて
solution: Target
subtopic: Auto-Complete
title: オートコンプリートについて
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 439100ab96f4b597c55b1c1ae38a5778c208e896

---


# オートコンプリートについて{#about-auto-complete}

オートコンプリートの様々な領域を設定して、オートコンプリート対応の検索フォームの生成を制御し、オートコンプリート対応の検索フォームの一部として含まれるautocomplete_data.jsファイルを制御できます。

## オートコンプリートについて {#concept_093A9CD754864BA79B456FE4BEB64578}

ファイルは再 [!DNL autocomplete_data.js] 生され、オートコンプリートの設定ページで保存された変更があるたびに、検索コンテンツネットワークに公開されます。

## オートコンプリートの設定 {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

オートコンプリート対応の検索フォームの生成を制御するオプションと、ファイルを設定できます。

<!-- 

t_configuring_auto-complete.xml

 -->

オートコンプリートを設定した後、結果のHTMLソースをレビュー用に表示できます。 HTMLソースは、Webサイトのページにコピー&amp;ペーストするものです。

詳しく [は、検索フォームが表示される状態をプレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

詳しくは、 [オートコンプリートワードリストの設定を参照してくださ](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)い。

詳しくは、 [オートコンプリートCSSの設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

**オートコンプリートを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Auto-Complete]** ます **[!UICONTROL Auto-Complete Setup]**。
1. ページ [!DNL Auto-Complete Setup] で、必要なオプションを設定します。

   検索フォーム [が表示される状態をプレビューするものも参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>提案の最大数 </p> </td> 
      <td colname="col2"> <p>オートコンプリート候補リストに表示する項目の最大数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小入力文字数 </p> </td> 
      <td colname="col2"> <p>顧客が提案を表示する前にオートコンプリート検索フォームに入力する必要がある文字数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大キャッシュエントリ数 </p> </td> 
      <td colname="col2"> <p>顧客のブラウザーにキャッシュする、以前に要求したオートコンプリートの提案の最大数を指定します。 通常、この設定はデフォルトの1000のままにしておく必要があります。 </p> <p>このオプションを0に設定すると、ブラウザーのキャッシュを完全に無効にできますが、お勧めしません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名 </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応の検索フォームの「フォーム」タグの「名前」属性を指定します。 例： </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>ここ <span class="filepath"> で、 </span> SiteSearchはフォームタグのname属性です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>DivタグID </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応の検索フォームの"div"タグのID属性を指定します。 例： </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>ここで <span class="filepath"> 、オ </span> ートコンプリートはdivタグの属性です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Input tag ID </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応の検索フォームの「input」タグのID属性を指定します。 例： </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>qは <span class="filepath"> 入 </span> 力タグのid属性です。 </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>シャドウを表示 </p> </td>
      <td colname="col2"> <p>オートコンプリート候補リストにコスメティックドロップシャドウを追加します。 </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>フレーズの先頭にのみ一致 </p> </td>
      <td colname="col2"> <p>入力テキストの先頭に一致する結果のみを提案します。 </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>UTF-8文字セットのサポート </p> </td>
      <td colname="col2"> <p>用語の非ASCII文字を正しく処理する。 </p> </td>
      </tr>
    </tbody> 
   </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## オートコンプリート単語リストの設定 {#task_1F8E0F346263443383F8CFD2C7AB35D4}

オートコンプリートで顧客に提案として表示する単語やフレーズのリストを設定します。

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

「オートコ [ンプリートの設定」を参照してくださ](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)い。

詳しくは、 [オートコンプリートCSSの設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

**オートコンプリート単語リストを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Auto-Complete]** ます **[!UICONTROL Auto-Complete Word List]**。
1. ページ [!DNL Auto-Complete Word List] で、必要なオプションを設定します。

   詳しく [は、検索フォームが表示される状態をプレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>人気のある検索期間 </p> </td> 
      <td colname="col2"> <p> 顧客の最近の検索で使用した語句を含める期間を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 最大検索数 </p> </td> 
      <td colname="col2"> <p>オートコンプリートの単語リストに含める、検索する単語やフレーズの最大数を制御します。 最も人気の高い上位の単語やフレーズが含まれます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p>各フィールド名は、インデックス付きの値を含める1つのフィールドの名前を定義します。 フィールド名を追加または削除するには、+と — を使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大値数 </p> </td> 
      <td colname="col2"> <p>選択したフィールド名に対して許可されるフィールド値の最大数を定義します。 最も多く参照される上位の値も含まれます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>次の語句を追加 </p> </td> 
      <td colname="col2"> <p> オートコンプリートの単語リストには、この領域に表示される単語とフレーズが入力されます。 </p> <p> 「編集」 <span class="uicontrol"> をク </span> リックして、リストを表示するか、リストに単語やフレーズを追加します。 完了したら、「変更の保存」をク <span class="uicontrol"> リックしま </span>す。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>これらの語句を削除する </p> </td> 
      <td colname="col2"> <p> この領域のエントリは、オートコンプリートの単語リストには表示されません。 </p> <p> 「編集」 <span class="uicontrol"> をク </span> リックして、リストを表示するか、リストに単語やフレーズを追加します。 完了したら、「変更の保存」をク <span class="uicontrol"> リックしま </span>す。 </p> <p> このリストでは正規表現を使用できます。 このリストで正規表現を指定するには、 
        <userinput>
          regexp 
        </userinput> 後にスペースが1つ、その後に正規表現が続きます。 正規表現に一致する単語リスト内の行は削除されます。 </p> <p> <b>重要</b>:正規表現は、他のアプリケーションで以前に使用したことがある場合にのみ使用してください。 </p> <p>正規表現を参 <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>大文字と小文字を区別しない </p> </td> 
      <td colname="col2"> <p>オートコンプリートの単語リストで、アルファベットの大文字と小文字のみが異なる重複したエントリは削除されます。すべての単語リストのエントリは強制的に小文字に変換されます。 </p> <p>オートコンプリートの提案を「先頭文字を大文字にする」または「すべて大文字にする」にする場合は、 
        <userinput>
          text-transform :大文字にする 
        </userinput>  または 
        <userinput>
          text-transform :大文字； 
        </userinput> 「/* styles for result item */」の下にある、オートコンプリートCSSコンテンツに対するCSSテキストプロパティ。 </p> <p>詳しくは、オ <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> ートコンプリートCSSの設定を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再インデックス時に更新 </p> </td> 
      <td colname="col2"> <p>アカウントの再インデックスが成功するたびに、オートコンプリートのワードリストが自動的に再生成されます。 </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。
   * 変更を **[!UICONTROL Preview Word List]** 保存するには、をクリックし、オートコンプリートの提案リ [!DNL Auto-Complete Word List Preview] ストを確認できるページを開きます。 ページ上部のナビゲーションオプションを使用して、表示されるリストを確認し、絞り込みます。 完了したら、をクリックし **[!UICONTROL Close]** てページに戻り [!DNL Auto-Complete Word List] ます。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## オートコンプリートCSSの設定 {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

オートコンプリートCSSを使用して、使用するオートコンプリートカスケードスタイルシートを設定します。

<!-- 

t_configuring_auto-complete_css.xml

 -->

オートコンプリートCSSは、のコンテンツを制御し [!DNL autocomplete_styles.css]ます。このコンテンツは、オートコンプリートが有効な検索フォームの一部として含まれます。 ここで指定するCSSは、オートコンプリート提案リストの視覚的な表示を制御します。 可能な視覚的なプレゼンテーションのアイデアの例については、次を参照してください。

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[オートコンプリート単語リストの設定を参照してください](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)。

[オートコンプリートの設定を参照してください](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)。

オートコンプリートCSSの設定が完了したら、検索フォームをプレビューして、指定したCSSが外観とレイアウトで許容可能かどうかを確認できます。

詳しく [は、検索フォームが表示される状態をプレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**重要**:カスタムのオートコンプリートCSSを適用するには、HTMLコードに表示される2行目からコメントタグを削除する必要があります。 次に、検索フォームを含むページのheadセクション内に同じ行を移動します。

「検 [索フォームのHTMLコードを](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**オートコンプリートCSSを設定するには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Auto-Complete]** ます **[!UICONTROL Auto-Complete CSS]**。
1. テキストフ [!DNL Auto-Complete CSS] ィールドに、オートコンプリート候補リストに関連付けるカスケードスタイルシートの情報を貼り付けるか、入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## Webサイトに表示される検索フォームのプレビュー {#task_437B35EFA5424603A08AF8E79E6B4714}

オートコンプリートCSSとオートコンプリートCSSの設定に基づいて、WebサイトにHTMLコードを追加する場合に検索フォームがどのように表示されるかをプレビューできます。

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

「オートコ [ンプリートの設定」を参照してくださ](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)い。

詳しくは、 [オートコンプリートCSSの設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

「検 [索フォームのHTMLコードを](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

「検索フォ [ームでのコレクションの使用」を参照してくださ](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)い。

詳しくは、フ [ォームでのフレームの使用を参照してくださ](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)い。

詳しくは、 [アドバンス検索フォームの例を参照してくださ](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)い。

詳しくは、HTML [コードからのアドバンス検索を参照してくださ](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)い。

詳しくは、「 [アドバンス検索フォームテンプレートコード](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)」を参照。

**Webサイトに表示される検索フォームをプレビューするには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Auto-Complete]** ます **[!UICONTROL Search Form]**。
1. （オプション）をク **[!UICONTROL HTML code]** リックして、Webサイトのページにコピー&amp;ペーストするHTMLを表示します。

## 検索フォームのHTMLコードのWebサイトのページへのコピー {#task_A3A01EA800F24C0AA33902387E0362C7}

オートコンプリートCSSとオートコンプリートCSSの設定に基づいて、WebサイトにHTMLコードを追加する場合に検索フォームがどのように表示されるかをプレビューできます。

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

「オートコ [ンプリートの設定」を参照してくださ](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)い。

詳しくは、 [オートコンプリートCSSの設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

「検 [索フォームのHTMLコードを](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

「検索フォ [ームでのコレクションの使用」を参照してくださ](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)い。

詳しくは、フ [ォームでのフレームの使用を参照してくださ](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)い。

詳しくは、 [アドバンス検索フォームの例を参照してくださ](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)い。

詳しくは、HTML [コードからのアドバンス検索を参照してくださ](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)い。

詳しくは、「 [アドバンス検索フォームテンプレートコード](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)」を参照。

**検索フォームのHTMLコードをWebサイトのページにコピーするには**

1. 製品メニューで//をクリ **[!UICONTROL Design]** ックし **[!UICONTROL Auto-Complete]** ます **[!UICONTROL Form Source]**。

   >[!NOTE]
   >
   >フォームソースの値 `form name=` は変更しないでください。

1. （オプション）次のいずれかの操作を行います。

   * オートコンプリートCSSを設定し、検索フォームにスタイルを適用する場合は、HTMLコードの2行目からコメントタグを削除します。 次に、検索フォームを含むページのheadセクション内に同じ行を移動します。
   * パフォーマンスを最大にするには、HTMLコードの下部に表示されているタグを移動し、検索フォームを含む各ページのbodyセクションの下部に配置します。

1. コードをコピーし、検索フォームを表示するWebサイトのWebページに貼り付けます。
