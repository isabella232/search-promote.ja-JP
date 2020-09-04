---
description: オートコンプリートの様々な領域を設定して、オートコンプリートが有効な検索フォームの生成を制御したり、オートコンプリートが有効な検索フォームの一部として含まれるautocomplete_data.jsファイルを制御したりできます。
seo-description: オートコンプリートの様々な領域を設定して、オートコンプリートが有効な検索フォームの生成を制御したり、オートコンプリートが有効な検索フォームの一部として含まれるautocomplete_data.jsファイルを制御したりできます。
seo-title: オートコンプリートについて
solution: Target
subtopic: Auto-Complete
title: オートコンプリートについて
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 1%

---


# オートコンプリートについて{#about-auto-complete}

オートコンプリートの様々な領域を設定して、オートコンプリートが有効な検索フォームの生成を制御したり、オートコンプリートが有効な検索フォームの一部として含まれるautocomplete_data.jsファイルを制御したりできます。

## オートコンプリートについて {#concept_093A9CD754864BA79B456FE4BEB64578}

ファイル [!DNL autocomplete_data.js] は再生成され、オートコンプリートセットアップページで保存された変更があるたびに検索コンテンツネットワークに公開されます。

## オートコンプリートの設定 {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

オートコンプリート対応の検索フォームおよびファイルの生成を制御するオプションを設定および設定できます。

<!-- 

t_configuring_auto-complete.xml

 -->

オートコンプリートを設定した後、結果として得られるHTMLソースをレビュー用に表示できます。 HTMLソースは、Webサイトのページにコピー&amp;ペーストするものです。

詳しくは、検索フォームが表示されるとおりに [プレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

「オートコンプリートWordリストの [設定](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)」を参照してください。

詳しくは、オートコンプリートCSSの [設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

**オートコンプリートを設定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Auto-Complete]** す **[!UICONTROL Auto-Complete Setup]**。
1. ページで、目的のオプションを設定 [!DNL Auto-Complete Setup] します。

   検索フォームがユーザーの [目的に合わせて表示されるようにプレビューするものも参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col2"> <p>オートコンプリート提案リストに表示する項目の最大数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最小入力文字数 </p> </td> 
      <td colname="col2"> <p>顧客がオートコンプリート検索フォームに入力しなければ、サーチクエリが表示されない文字数を指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大キャッシュエントリ数 </p> </td> 
      <td colname="col2"> <p>顧客のブラウザーにキャッシュするために以前に要求したオートコンプリートの提案の最大数を指定します。 通常、この設定はデフォルトの1000のままにしてください。 </p> <p>このオプションを0に設定すると、ブラウザーのキャッシュを完全に無効にできますが、これはお勧めしません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名 </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応検索フォームの「form」タグの「name」属性を指定します。 例： </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com"ターゲット="_blank"&gt; </span> </p> <p>ここで、 <span class="filepath"> SiteSearch </span> はフォームタグのname属性です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>DivタグID </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応検索フォームの"div"タグのID属性を指定します。 例： </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>ここで、 <span class="filepath"></span> オートコンプリートはdivタグの属性です。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Input tag ID </p> </td> 
      <td colname="col2"> <p>オートコンプリート対応検索フォームの「input」タグのID属性を指定します。 例： </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>ここで <span class="filepath"> q </span> は、inputタグのid属性です。 </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>シャドウを表示 </p> </td>
      <td colname="col2"> <p>オートコンプリート候補リストに化粧用のドロップシャドウを追加します。 </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>フレーズの先頭にのみ一致 </p> </td>
      <td colname="col2"> <p>入力テキストの先頭に一致する結果のみを提示します。 </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>UTF-8文字セットのサポート </p> </td>
      <td colname="col2"> <p>用語の非ASCII文字を正しく処理する。 </p> </td>
      </tr>
    </tbody> 
   </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## オートコンプリートWordリストの設定 {#task_1F8E0F346263443383F8CFD2C7AB35D4}

オートコンプリートで顧客に対して表示する語句のリストを提案として設定します。

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

「オートコンプリートの [設定](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)」を参照してください。

詳しくは、オートコンプリートCSSの [設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

**オートコンプリートワードリストを設定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Auto-Complete]** す **[!UICONTROL Auto-Complete Word List]**。
1. ページで、目的のオプションを設定 [!DNL Auto-Complete Word List] します。

   詳しくは、検索フォームが表示されるとおりに [プレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col2"> <p> 顧客の最近の検索で使用された語句を含める期間を制御します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 最大検索数 </p> </td> 
      <td colname="col2"> <p>オートコンプリートの単語リストに含める検索語句の最大数を制御します。 最も人気の高いトップワードやフレーズが含まれます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フィールド名 </p> </td> 
      <td colname="col2"> <p>各フィールド名は、インデックス値を含める1つのフィールドの名前を定義します。 フィールド名を追加または削除するには、+と — を使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>最大値 </p> </td> 
      <td colname="col2"> <p>選択したフィールド名に対して許可するフィールド値の最大数を定義します。 最も多く参照されるトップ値も含まれます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>こ追加れらの語句 </p> </td> 
      <td colname="col2"> <p> オートコンプリートの単語リストには、この領域に一覧表示されている単語とフレーズが入力されます。 </p> <p> 「 <span class="uicontrol"> 編集」をクリック </span> してリストを表示したり、リストに単語やフレーズを追加したりします。 完了したら、「変更の <span class="uicontrol"> 保存」をクリックし </span>ます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>これらの語句を削除する </p> </td> 
      <td colname="col2"> <p> この領域のエントリは、オートコンプリートの単語リストには表示されません。 </p> <p> 「 <span class="uicontrol"> 編集」をクリック </span> してリストを表示したり、リストに単語やフレーズを追加したりします。 完了したら、「変更の <span class="uicontrol"> 保存」をクリックし </span>ます。 </p> <p> このリストでは正規式を使用できます。 このリストで正規式を指定するには、行の後に1つのスペースを続け、その後に正規式を続けて開始します。 <code>regexp</code> 正規式に一致する単語リスト内の行はすべて削除されます。 </p> <p> <b>重要</b>:正規式は、他のアプリケーションで以前に使用したことがある場合にのみ使用してください。 </p> <p>詳しくは、 <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 正規式を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>大文字と小文字を区別しない </p> </td> 
      <td colname="col2"> <p>オートコンプリートワードリストの重複エントリで、英字の大文字と小文字のみが異なるエントリは削除されます。単語リストのエントリはすべて強制的に小文字に変換されます。 </p> <p>オートコンプリートの提案を「最初の文字が大文字」または「すべて大文字」で表示する場合は、「/* styles for result item */」の下のオートコンプリートCSSコンテンツに、 <code>
          text-transform : capitalize; 
        </code> または <code>
          text-transform : uppercase; 
        </code> CSSテキストプロパティを追加します。 </p> <p>詳しくは、オートコンプリートCSSの <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> 設定を参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再インデックス時に更新 </p> </td> 
      <td colname="col2"> <p>アカウントの再インデックスが成功するたびに、単語のオートコンプリートリストが自動的に再生成されます。 </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。
   * 行っ **[!UICONTROL Preview Word List]** た変更を保存するには、をクリックします。その後、オートコンプリート候補リストを確認できる [!DNL Auto-Complete Word List Preview] ページを開きます。 ページ上部近くにあるナビゲーションオプションを使用して、表示されるリストを確認し、調整します。 完了したら、をクリック **[!UICONTROL Close]** して [!DNL Auto-Complete Word List] ページに戻ります。

      「Historyオプションの [使用](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## オートコンプリートCSSの設定 {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

オートコンプリートCSSを使用して、使用するオートコンプリートカスケードスタイルシートを設定します。

<!-- 

t_configuring_auto-complete_css.xml

 -->

オートコンプリートCSSは、のコンテンツを制御し [!DNL autocomplete_styles.css]ます。このコンテンツはオートコンプリート対応の検索フォームの一部として含まれます。 ここで指定するCSSによって、オートコンプリートの提案リストが視覚的に表示されます。 可能な視覚的なプレゼンテーションのアイデアの例については、次を参照してください。

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[オートコンプリートWordリストの設定](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)。

[オートコンプリートの設定](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)。

オートコンプリートCSSの設定が完了したら、検索フォームをプレビューして、指定したCSSが外観とレイアウトで許容可能かどうかを確認できます。

詳しくは、検索フォームが表示されるとおりに [プレビューするを参照してください。](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**重要**:カスタムのオートコンプリートCSSを適用するには、HTMLコードに表示される2行目からコメントタグを削除する必要があります。 次に、検索フォームを含むページのheadセクション内に同じ行を移動します。

「検索フォームのHTMLコードを…に [コピーする」を参照してください。](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**オートコンプリートCSSを設定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Auto-Complete]** す **[!UICONTROL Auto-Complete CSS]**。
1. テキストフィールドに、オートコンプリート提案リストに関連付けるカスケードスタイルシートの情報を貼り付けるか、入力します。 [!DNL Auto-Complete CSS]
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## 検索フォームがWebサイトに表示されるとおりにプレビューする {#task_437B35EFA5424603A08AF8E79E6B4714}

オートコンプリートCSSとオートコンプリートCSSの設定に基づいて、WebサイトにHTMLコードを追加する場合の検索フォームの表示をプレビューできます。

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

「オートコンプリートの [設定](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)」を参照してください。

詳しくは、オートコンプリートCSSの [設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

「検索フォームのHTMLコードを…に [コピーする」を参照してください。](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

「検索フォームでのコレクションの [使用](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)」を参照してください。

フォーム [でのフレームの使用を参照してください](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)。

詳しくは、「アドバンス検索フォーム [の例](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)」を参照してください。

詳しくは、HTMLコードからの [詳細検索を参照してください](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)。

「 [アドバンス検索フォームテンプレートコード](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)」を参照してください。

**Webサイトに表示される検索フォームをプレビューするには**

1. 製品メニューで、//をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Auto-Complete]** す **[!UICONTROL Search Form]**。
1. （オプション）をクリック **[!UICONTROL HTML code]** して、Webサイトのページにコピー&amp;ペーストするHTMLを表示します。

## 検索フォームのHTMLコードのWebサイトのページへのコピー {#task_A3A01EA800F24C0AA33902387E0362C7}

オートコンプリートCSSとオートコンプリートCSSの設定に基づいて、WebサイトにHTMLコードを追加する場合の検索フォームの表示をプレビューできます。

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

「オートコンプリートの [設定](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)」を参照してください。

詳しくは、オートコンプリートCSSの [設定を参照してください](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)。

「検索フォームのHTMLコードを…に [コピーする」を参照してください。](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

「検索フォームでのコレクションの [使用](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)」を参照してください。

フォーム [でのフレームの使用を参照してください](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)。

詳しくは、「アドバンス検索フォーム [の例](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)」を参照してください。

詳しくは、HTMLコードからの [詳細検索を参照してください](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)。

「 [アドバンス検索フォームテンプレートコード](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)」を参照してください。

**検索フォームのHTMLコードをWebサイトのページにコピーするには**

1. 製品メニューで、//をクリックし **[!UICONTROL Design]** ま **[!UICONTROL Auto-Complete]** す **[!UICONTROL Form Source]**。

   >[!NOTE]
   >
   >フォームソースの `form name=` 値は変更しないでください。

1. （オプション）次のいずれかの操作を行います。

   * オートコンプリートCSSを設定し、検索フォームにスタイルを適用する場合は、HTMLコードに表示される2行目からコメントタグを削除します。 次に、検索フォームを含むページのheadセクション内に同じ行を移動します。
   * パフォーマンスを最大にするには、HTMLコードの下部に表示されているタグを移動し、検索フォームを含む各ページのbodyセクションの下部に配置します。

1. コードをコピーして、検索フォームを表示するWebサイトのWebページに貼り付けます。
