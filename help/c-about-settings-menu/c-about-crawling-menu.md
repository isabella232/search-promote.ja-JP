---
description: クロールメニューの設定日、URLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URL入力ポイントを使用します。
seo-description: クロールメニューの設定日、URLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URL入力ポイントを使用します。
seo-title: クロールメニューについて
solution: Target
subtopic: Crawling
title: クロールメニューについて
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: e080a61e24a3809beff7c212ff3d088b2a8ad3b6
workflow-type: tm+mt
source-wordcount: '11115'
ht-degree: 1%

---


# クロールメニューについて{#about-the-crawling-menu}

クロールメニューの設定日、URLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URL入力ポイントを使用します。

## URL入力ポイントについて {#concept_5D857E3B5C124E85BC0B5AE77A509573}

ほとんどのWebサイトには、顧客が最初に訪問する主なエントリーポイント(ホームページ)が1つあります。 このメインエントリポイントは、検索ロボットがインデックスのクロールを開始する際のURLアドレスです。 ただし、Webサイトに複数のドメインまたはサブドメインがある場合、またはサイトの一部がプライマリエントリポイントからリンクされていない場合は、「URL入力ポイント」を使用してエントリポイントを追加できます。

指定した各URLエントリポイントより下のWebサイトページには、すべてインデックスが作成されます。 URLエントリポイントとマスクを組み合わせて、Webサイトのどの部分にインデックスを付けるかを厳密に制御できます。 URL入力ポイント設定の効果がユーザーに表示されるようにするには、Webサイトのインデックスを再構築する必要があります。

メインエントリポイントは、通常、インデックスを作成して検索するWebサイトのURLです。 このメインエントリポイントは、「アカウントの設定」で設定します。

「アカウント設定の [指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

メインURLエントリポイントを指定した後、必要に応じて、クロールする追加のエントリポイントを順番に指定できます。 多くの場合、メインエントリポイントの下のページからリンクされていないWebページに対して、追加のエントリポイントを指定します。 次の例のように、Webサイトが複数のドメインにまたがる場合は、追加のエントリポイントを指定します。

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

各エントリポイントを次の表に示す、1つ以上のスペースで区切られたキーワードで修飾します。 これらのキーワードは、ページのインデックス作成方法に影響を与えます。

**重要**: 特定のキーワードをエントリポイントから、およびスペースで相互に区切るようにしてください。 コンマは有効な区切り文字ではありません。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>キーワード </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成しないが、そのページのリンクをたどる必要がある場合は、 
     <userinput>
       noindex 
     </userinput> を入力します。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>このキーワードは、 
     <userinput>
       content="noindex" 
     </userinput>)を 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> エントリポイントページのタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成する際に、そのページのリンクをたどる必要がない場合は、 
     <userinput>
       nofollow 
     </userinput> を入力します。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>このキーワードは、 
     <userinput>
       content="nofollow" 
     </userinput> 間に 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> のタグを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>form </p> </td> 
   <td colname="col2"> <p> エントリポイントがログインページの場合、 
     <userinput>
       form 
     </userinput> は、通常、検索ロボットがログインフォームを送信し、適切なcookieを受け取った後にwebサイトをクロールできるようにするために使用されます。 「form」キーワードを使用する場合、エントリポイントページのインデックスは作成されず、検索ロボットはエントリポイントページをクロール済みとしてマークしません。 使用する 
     <userinput>
       nofollow 
     </userinput> を返します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

コンテンツタイプ [についても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)。

Index Connector [についても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)。

## インデックスを作成する複数のURLエントリポイントの追加 {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Webサイトに複数のドメインまたはサブドメインがあり、それらをクロールする場合は、URL入力ポイントを使用してURLを追加できます。

WebサイトのメインURLエントリポイントを設定するには、「アカウントの設定」を使用します。

「アカウント設定の [指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

**インデックスを作成する複数のURLエントリポイントを追加するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL URL Entrypoints]**。
1. ページの [!DNL URL Entrypoints] フィールドに、1行につき1つのURLアドレスを [!DNL Entrypoints] 入力します。
1. （オプション） **[!UICONTROL Add Index Connector Configurations]** ドロップダウンリストで、インデックス作成のエントリポイントとして追加するインデックスコネクタを選択します。

   ドロップダウンリストは、1つ以上のインデックスコネクタ定義を以前に追加した場合にのみ使用できます。

   ![](assets/url_entrypoints_index_connector.png)

   「インデックスコネクタ定義の [追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)」を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## URLマスクについて {#concept_8039DFC53FF3410AA494D602F71BA164}

URLマスクは、検索ロボットがインデックスを付けたかインデックスを付けなかったかをWebサイトのドキュメントで判断するパターンです。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

使用できるURLマスクは次の2種類です。

* URLマスクを含める
* URLマスクの除外

URLマスクを含めると、検索ロボットはマスクのパターンに一致するドキュメントをインデックス付けするように指示されます。

URLマスクを除外すると、検索ロボットは一致するドキュメントのインデックスを作成するように指示します。

検索ロボットは、リンクからWebサイト内のリンクに移動する際、URLに遭遇し、それらのURLに一致するマスクを探します。 最初の一致によって、そのURLをインデックスに含めるか、除外するかが決まります。 検出されたURLに一致するマスクがない場合、そのURLはインデックスから破棄されます。

エントリポイントURLに対するURLマスクを含めるは、URLが自動的に生成されます。 この動作により、Webサイトで遭遇するすべてのドキュメントのインデックスが作成されます。 また、ウェブサイトから「離脱」するリンクが便利になくなります。 例えば、インデックス付きのページがhttps://www.yahoo.comにリンクしている場合、検索ロボットはそのURLのインデックスを作成しません。これは、エントリポイントURLによって自動的に生成されるインクルードマスクと一致しないためです。

指定する各URLマスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* に示すように、フルパス `https://www.mydomain.com/products.html`。
* のように、部分的なパス `https://www.mydomain.com/products`。
* ワイルドカードを使用するURL `https://www.mydomain.com/*.html`。
* 正規式（上級ユーザー用）

   マスクを正規式にするには、マスクタイプ(ま `regexp` たは `exclude``include`)とURLマスクの間にキーワードを挿入します。

以下に、単純な除外URLマスクの例を示します。

```
exclude https://www.mydomain.com/photos
```

この例は除外URLマスクなので、パターンに一致するドキュメントのインデックスは作成されません。 このパターンは、検出されたアイテム（ファイルとフォルダーの両方）と一致するので、 `https://www.mydomain.com/photos.html``https://www.mydomain.com/photos/index.html`との両方が除外URLと一致している場合、そのURLのインデックスは作成されません。 フォルダー内のファイルのみを一致させるには、次の例のように、URLマスクの末尾にスラッシュを含める必要があり `/photos/` ます。

```
exclude https://www.mydomain.com/photos/
```

次の除外マスクの例では、ワイルドカードを使用しています。 これは、「.pdf」拡張子を持つファイルを見過ごすよう検索ロボットに指示します。 検索ロボットは、これらのファイルをインデックスに追加しません。

```
exclude *.pdf
```

単純なインクルードURLマスクは次のとおりです。

```
include https://www.mydomain.com/news/
```

URLエントリポイントから一連のリンクを介してリンクされたドキュメント、またはURLエントリポイント自体として使用されたエントリのみがインデックス化されます。 ドキュメントのURLを「URLを含む」マスクとしてリストするだけで、リンクされていないドキュメントのインデックスは作成されません。 インデックスにリンクされていないドキュメントを追加するには、URL入力ポイント機能を使用します。

「URL入力ポイント [について](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)」を参照してください。

マスクを含めると、マスクを除外すると機能します。 「URLを除外」マスクを作成し、「URLを含む」マスクを使用して除外されたページを1つ以上含めることで、Webサイトの大部分をインデックス作成から除外できます。 例えば、エントリポイントURLが次のような場合、

```
https://www.mydomain.com/photos/
```

検索ロボットは、との下のすべてのページをクロールしてインデックス付けし `/photos/summer/`ます `/photos/spring/` (フォル `/photos/fall/``photos` ダから各ディレクトリに少なくとも1ページへのリンクがあると仮定)。 この動作は、リンクパスによって、検索ロボットがエントリポイントURLによって自動的に生成されるインクルードマスクに一致するドキュメントを、、、、 `/summer/`、および、の各フォルダ `/spring/``/fall/`ーと、の各URLで検索できるために発生します。

次の例のように、URLマスクを除外を含む `/fall/` フォルダー内のすべてのページを除外するように選択できます。

```
exclude https://www.mydomain.com/photos/fall/
```

または、次のURLマスクを使用して、インデックス `/photos/fall/redleaves4.html` の一部としてのみ選択的に含めます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

上記の2つのマスクの例が意図したとおりに機能するため、次のように、「include mask」が最初に表示されます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

検索ロボットはリストに表示された順序に従うので、検索ロボットは最初にを含め、次に `/photos/fall/redleaves4.html``/fall` フォルダー内の残りのファイルを除外します。

手順が次のとおり逆の方法で指定されている場合：

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

そ `/photos/fall/redleaves4.html` の場合、マスクが含めると指定しても含めない。

最初に表示されるURLマスクは、マスク設定の後で表示されるURLマスクよりも常に優先されます。 また、検索ロボットが「URLを含む」マスクと「URLを除外」マスクに一致するページを検出した場合は、最初に表示されるマスクが常に優先されます。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

## URLマスクを使用したキーワードの使用について {#section_7609A7A6D79B482ABCA8900886541AAB}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致したページのインデックス作成に影響を与えます。

マスクとキーワードの区切り文字としてコンマは無効です。 スペースのみを使用できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>キーワード </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> URLマスクと一致するページのテキストのインデックスを作成せず、一致したページのリンクに従う場合は、 
     <userinput>
       noindex 
     </userinput> を追加します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>上記の例では、検索ロボットが 
     <userinput>
       .swf 
     </userinput> 拡張子を指定します。ただし、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>Adobe コード内の   
     <userinput>
       noindex 
     </userinput> keywordは、 
     <userinput>
       content="noindex" 
     </userinput> 間に 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> 一致したページのタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> URLマスクと一致するページのテキストにインデックスを付けるが、一致するページのリンクに従わない場合は、 
     <userinput>
       nofollow 
     </userinput> を追加します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Adobe コード内の   
     <userinput>
       nofollow 
     </userinput> keywordは、 
     <userinput>
       content="nofollow" 
     </userinput> 間に 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> 一致したページのタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用します。 </p> <p>先頭に 
     <userinput>
       regexp 
     </userinput> は正規式として扱われます。 検索ロボットが除外正規式URLマスクに一致するドキュメントを検出した場合、それらのドキュメントのインデックスは作成されません。 検索ロボットが「含む正規式のURLマスク」に一致するドキュメントを検出すると、それらのドキュメントのインデックスが作成されます。 例えば、次のURLマスクがあるとします。 </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>検索ロボットは、 
     <userinput>
       https://www.mydomain.com/products/page1.html 
     </userinput> </p> <p>次の除外正規式URLマスクがある場合： </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>検索ロボットは、 
     <userinput>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </userinput>。 </p> <p>正規式URLマスクを含む次の場合： </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>検索ロボットは、「.swf」拡張子を持つファイルからのすべてのリンクに従います。 Adobe コード内の   
     <userinput>
       noindex 
     </userinput> keywordは、一致したファイルのテキストのインデックスが作成されないことを示します。 </p> <p>詳しくは、 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 正規式を参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分へのURLマスクの追加、またはインデックス部分へのURLマスクの追加 {#task_E1AFC17C746048B8843013D979E082C1}

を使用して、Webサイト [!DNL URL Masks] のどの部分をクロールしてインデックスを作成するか、または作成しないかを定義できます。

「URLマスクをテスト」フィールドを使用して、インデックス作成後にドキュメントが含まれているかどうかをテストします。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**Webサイトのインデックス部分にURLマスクを追加するか、インデックス部分に追加しないかを指定するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL URL Masks]**。
1. （オプション） [!DNL URL Masks] ページのフィールドに、WebサイトのテストURLマスクを入力し、をクリックし **[!UICONTROL Test URL Masks]****[!UICONTROL Test]**&#x200B;ます。
1. フィールドに、URLマスクアドレスの後にURLを入力し、URLマスクアドレスを入力します（クロールおよびインデックスを作成するWebサイトを追加する場合）。または [!DNL URL Masks]`include``exclude` 、URLマスクを入力します（Webサイトがクロールおよびインデックスを作成しない場合）。

   1行につき1つのURLマスクアドレスを入力します。 例：

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## 日付マスクについて {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

日付マスクを使用すると、ファイルの年齢に基づいて検索結果にファイルを含めたり、除外したりできます。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

使用できる日付マスクは次の2種類です。

* 日付マスクを含める（「include-days」と「include-date」）

   指定した日付以前の日付付けマスクインデックスファイルを含めます。
* 日付マスクを除外（「exclude-days」と「exclude-date」）

   指定した日付以前の日付の付いた日付マスクインデックスファイルを除外します。

デフォルトでは、ファイルの日付はメタタグ情報から決定されます。 Metaタグが見つからない場合は、検索ロボットがファイルをダウンロードした際にサーバから受け取ったHTTPヘッダからファイルの日付が決定されます。

指定する各日付マスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* フルパス( `https://www.mydomain.com/products.html`
* 部分パス( `https://www.mydomain.com/products`
* ワイルドカードを使用するURL `https://www.mydomain.com/*.html`
* 正規式。 マスクを正規式にするには、URLの前にキーワード `regexp` を挿入します。

「日付を含む」と「除外する」の両方の日付マスクでは、次の2つの方法のいずれかで日付を指定できます。 マスクは、一致するファイルが指定した日付以前に作成された場合にのみ適用されます。

1. 日数。 例えば、日付マスクが次のような場合、

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   指定した日数がカウントバックされます。 ファイルの日付が指定日以前の場合は、マスクが適用されます。

1. YYYY-MM-DDの形式を使用した実際の日付。 例えば、日付マスクが次のような場合、

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   一致したドキュメントの日付が指定した日付以前の場合は、日付マスクが適用されます。

以下に、単純な除外日付マスクの例を示します。

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

これは除外日付マスクなので、パターンと一致するファイルはインデックス化されず、90日以上経過しています。 ドキュメントを除外すると、テキストのインデックスは作成されず、そのファイルからのリンクも追跡されません。 ファイルは事実上無視されます。 この例では、ファイルとフォルダーの両方が、指定したURLパターンと一致する場合があります。 との両方がパターン `https://www.mydomain.com/docs/archive.html``https://www.mydomain.com/docs/archive/index.html` に一致し、90日以上経過している場合はインデックスが作成されません。 フォルダー内のファイルのみを一致させるには、 `/docs/archive/` フォルダーの最後に次のようにスラッシュを付ける必要があります。

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

日付マスクはワイルドカードでも使用できます。 次の除外マスクは、2011-02-15以前の拡張子「.pdf」を持つファイルを検索ロボットに見過ごすよう指示します。 検索ロボットは、一致するファイルをインデックスに追加しません。

```
exclude-date 2011-02-15 *.pdf
```

「インクルード」の日付マスクの外観は似ていますが、一致したファイルのみがインデックスに追加されます。 次のインクルード日付マスクの例は、Webサイトの `/docs/archive/manual/` 領域内で、作成日数が0日以上古いファイルのテキストのインデックスを作成するよう検索ロボットに指示します。

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

マスクを含めると、マスクを除外すると機能します。 例えば、除外日付マスクを作成し、除外するページのうち1つ以上をURLマスクを含むページに含めることで、Webサイトの大部分をインデックス作成から除外できます。 エントリポイントURLが次の場合：

```
https://www.mydomain.com/archive/
```

検索ロボットは、、およびの下のすべてのページをクロールしてインデックス付けし `/archive/summer/`ます(フォルダから各フォルダに少なくとも1ページへのリンクがあると仮定し `/archive/spring/``/archive/fall/``archive` ます)。 この動作は、リンクパスによって、検索ロボットが、 `/summer/`、、 `/spring/``/fall/` およびフォルダ内のファイルを「検索」でき、フォルダURLが、エントリポイントURLによって自動的に生成されるインクルードマスクに一致するために発生します。

「URL入力ポイント [について](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)」を参照してください。

「アカウント設定の [指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

次のように、除外する日付マスクを含むフ `/fall/` ォルダー内の、90日を超えるページをすべて除外するように選択できます。

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

次の日付マスクを使用して、インデックスの一部として、 `/archive/fall/index.html` （古さにかかわらず、0日以上前のファイルがすべて一致する）のみを選択的に含めることができます。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

上記の2つのマスクの例を意図したとおりに機能させるには、まず次のように「マスクを含める」をリストする必要があります。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

検索ロボットは指定された順序に従うので、検索ロボットは最初にを含め、次に `/archive/fall/index.html``/fall` フォルダー内の残りのファイルを除外します。

手順が次のとおり逆の方法で指定されている場合：

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

そ `/archive/fall/index.html` の場合、マスクは含める必要があると指定していても含めません。 最初に表示される日付マスクは、マスク設定の後で表示される日付マスクよりも常に優先されます。 また、検索ロボットが「日付を含む」マスクと「日付を除外する」マスクの両方に一致するページを検出した場合は、最初に表示されるマスクが常に優先されます。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

## 日付マスクを使用したキーワードの使用について {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致したページのインデックス作成に影響を与えます。

マスクとキーワードの区切り文字としてコンマは無効です。 スペースのみを使用できます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>キーワード </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> 「マスクを含む」で指定した日付以前のページのテキストのインデックスを作成しない場合は、 
     <userinput>
       noindex 
     </userinput> を指定します。 </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>上記の例では、10日以上前の「.swf」拡張子を持つファイルのリンクは、すべて検索ロボットに従うように指定しています。 ただし、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>古いファイルのテキストは、インデックスが作成されていないが、それらのファイルのすべてのリンクをたどるようにしてください。 このような場合は、除外日付マスクを使用する代わりに、「noindex」キーワードを含む日付マスクを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> インデックスマスクで指定された日付以前のページのテキストの日付をインデックス化する場合、一致したページのリンクに従わないようにするには、 
     <userinput>
       nofollow 
     </userinput> を指定します。 </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>Adobe コード内の   
     <userinput>
       nofollow 
     </userinput> keywordは、 
     <userinput>
       content="nofollow" 
     </userinput> 間に 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> タグ内に配置する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用します。 </p> <p>検索ロボットは通常、日付マスクをチェックする前にすべてのファイルをダウンロードして解析します。 この動作は、一部のファイルタイプではファイル自体に日付を指定できるためです。 例えば、HTMLドキュメントには、ファイルの日付を設定するメタタグを含めることができます。 </p> <p>日付に基づいて多数のファイルを除外し、不要な読み込みをサーバーに行いたくない場合は、 
     <userinput>
       server-date 
     </userinput> を追加します。 </p> <p>このキーワードは、各ファイルを解析する代わりに、サーバから返されたファイルの日付を信頼するように検索ロボットに指示します。 例えば、次の除外日付マスクでは、ドキュメントが90日以上前の場合、HTTPヘッダー内のサーバーから返された日付に従って、URLに一致するページが無視されます。 </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> サーバーから返される日付が90日以上前の場合、 
     <userinput>
       server-date 
     </userinput> 除外されたドキュメントをサーバーからダウンロードしないことを指定します。 その結果、ドキュメントのインデックス作成に要する時間が短縮され、サーバへの負荷が軽減されます。 グループの中に「 
     <userinput>
       server-date 
     </userinput> を指定しない場合、検索ロボットはHTTPヘッダー内のサーバーから返される日付を無視します。 代わりに、各ファイルがダウンロードされ、日付が指定されているかどうかを確認します。 ファイルに日付が指定されていない場合、検索ロボットはサーバから返された日付を使用します。 </p> <p>次を使用しないでください。 
     <userinput>
       server-date 
     </userinput> ファイルに、サーバーの日付を上書きするコマンドが含まれている場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 含めるマスクと除外するマスクの両方に使用します。 </p> <p>前に 
     <userinput>
       regexp 
     </userinput> は正規式として扱われます。 </p> <p>検索ロボットは、除外正規式の日付マスクに一致するファイルを検出した場合、それらのファイルのインデックス付けを行いません。 </p> <p>検索ロボットは、「含む」正規式の日付マスクに一致するファイルを検出すると、それらのドキュメントのインデックスを作成します。 </p> <p>例えば、次の日付マスクがあるとします。 </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>マスクは、180日以上前の一致するファイルを検索ロボットに除外するように指示します。 つまり、URLに「archive」という語を含むファイルです。 </p> <p>詳しくは、 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 正規式を参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分に日付マスクを追加する、またはインデックス部分に追加しない {#task_0010543C55F648D2B5DEFEFAD60FAF04}

日付マスクを使用すると、ファイルの保存期間に基づいて顧客の検索結果にファイルを含めたり、除外したりできます。

インデックス作成後にファイルが含まれているかどうかをテストするには、 **[!UICONTROL Test Date]** および **[!UICONTROL Test URL]** フィールドを使用します。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**Webサイトのインデックス部分に日付マスクを追加するには、またはインデックス部分に追加しないには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Date Masks]**。
1. （オプション） [!DNL Date Masks] ページの **[!UICONTROL Test Date]** フィールドに、YYYY-MM-DD形式の日付を入力します(例： `2011-07-25`)。 「URLマスク」 **[!UICONTROL Test URL]** フィールドにwebサイトのURLマスクを入力し、をクリックし **[!UICONTROL Test]**&#x200B;ます。
1. フィールドに、1行につき1つの日付マスクアドレスを入力し [!DNL Date Masks] ます。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## パスワードについて {#concept_3EDBD731725D46B891F834D4472774DC}

WebサイトのHTTP基本認証で保護されている部分にアクセスするには、1つ以上のパスワードを追加します。

パスワード設定の効果がユーザーに表示される前に、サイトインデックスを作成し直す必要があります。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

ページ上で [!DNL Passwords] 、1行に1つのパスワードを入力します。 パスワードは、次の例のように、URLまたは領域、ユーザー名、パスワードで構成されます。

```
https://www.mydomain.com/ myname mypassword
```

上のようなURLパスを使用する代わりに、領域を指定することもできます。

使用する正しい領域を決定するには、パスワードで保護されたWebページをブラウザーで開き、ネットワークパスワードの入力ダイアログボックスを確認します。

![](assets/realms.gif)

領域名は、この場合は「My Site Realm」です。

上記の領域名を使用したパスワードは、次のようになります。

```
My Site Realm myusername mypassword
```

Webサイトに複数のレルムがある場合、次の例のように、各レルムのユーザー名とパスワードを別々の行に入力して、複数のパスワードを作成できます。

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

URLまたはレルムを含むパスワードを組み合わせて、パスワードリストを次のように指定できます。

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

上記のリストでは、サーバーの認証要求と一致する領域またはURLを含む最初のパスワードが使用されます。 例えば、のファイル `https://www.mysite.com/path1/path2/index.html` がにある場合でも、とが使用されます。これは、URLで定義されるパスワードが領域で定義されるパスワードの上に表示されるから `Realm3``name2``password2` です。

## 認証が必要なWebサイトの領域にアクセスするためのパスワードの追加 {#task_DED19D476FF04B48BB6456D5ECB8628A}

「パスワード」を使用すると、クロールやインデックス作成の目的で、Webサイトのパスワードで保護された領域にアクセスできます。

パスワードの影響がユーザーに表示される前に、サイトインデックスを必ず作成し直してください

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**Webサイトの認証が必要な領域にアクセスするためのパスワードを追加するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Passwords]**。
1. ページの [!DNL Passwords]**[!UICONTROL Passwords]** フィールドに、領域またはURLと、それに関連するユーザー名、パスワードをスペースで区切って入力します。

   領域パスワードとURLパスワードを別々の行に示す例：

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   1行に1つのパスワードのみを追加します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## コンテンツタイプについて {#concept_6FEA1355C0374500B4C53090C34A8A07}

を使用して、このアカウント [!DNL Content Types] のクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成用に選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、Adobe Flashムービー、Word、Excel、PowerpointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

ユーザーに対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを作成し直す必要があります。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

## MP3音楽ファイルのインデックスについて {#section_AD2E28BEEE3E46629E2B05C34A963673}

ページでこのオプション **[!UICONTROL Text in MP3 Music Files]**[!DNL Content Types] を選択すると、MP3ファイルは、2つの方法のいずれかでクロールされ、インデックス化されます。 最初に、最も一般的な方法は、次のように、HTMLファイル内のアンカーhrefタグを使用する方法です。

```
<a href="MP3-file-URL"></a>
```

2つ目の方法は、MP3ファイルのURLをURL入力ポイントとして入力する方法です。

「URL入力ポイント [について](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)」を参照してください。

MP3ファイルは、そのMIMEタイプ「audio/mpeg」で認識されます。

MP3ミュージックファイルは、通常、少量のテキストしか含まない場合でも、非常に大きなサイズになる可能性があることに注意してください。 例えば、MP3ファイルには、アルバム名、アーティスト名、曲のタイトル、曲のジャンル、リリース年度、コメントなどを任意で保存できます。 この情報は、ファイルの最後（TAGと呼ばれる場所）に保存されます。 TAG情報を含むMP3ファイルのインデックスは、次のように作成されます。

* 曲のタイトルは、HTMLページのタイトルのように扱われます。
* コメントは、HTMLページに対して定義された説明と同様に扱われます。
* ジャンルは、HTMLページに対して定義されたキーワードと同様に扱われます。
* アーティスト名、アルバム名およびリリース年は、HTMLページの本文と同様に扱われます。

Webサイト上でクロールおよびインデックスが作成された各MP3ファイルは、1ページとしてカウントされます。

Webサイトに大きなMP3ファイルが多数ある場合は、アカウントのインデックス付けバイト制限を超える可能性があります。 この場合は、 **[!UICONTROL Text in MP3 Music Files]** ページで選択を解除して、Webサイト [!DNL Content Types] 上のすべてのMP3ファイルがインデックス付けされないようにすることができます。

Webサイト上の特定のMP3ファイルのインデックス作成を禁止する必要がある場合は、次のいずれかを実行できます。

* MP3ファイルにリンクするアンカータグを、 `<nofollow>` およびの `</nofollow>` タグで囲みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

* 除外マ追加スクとしてのMP3ファイルのURLです。

   URLマスク [についてを参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)。

## クロールおよびインデックスを作成するコンテンツタイプの選択 {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

を使用して、このアカウント [!DNL Content Types] のクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成用に選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、Adobe Flashムービー、Word、Excel、PowerpointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

ユーザーに対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを作成し直す必要があります。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

中国語、日本語または韓国語のMP3ファイルをクロールしてインデックスを作成するには、次の手順を実行します。 次に、 > **[!UICONTROL Settings]** > **[!UICONTROL Metadata]****[!UICONTROL Injections]**>で、MP3ファイルのエンコードに使用する文字セットを指定します。

Injections [についてを参照してください](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)。

**クロールおよびインデックスを作成するコンテンツタイプを選択するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Content Types]**。
1. ページで、Webサイト上でクロールおよびインデックスを作成するファイルタイプを確認し [!DNL Content Types] ます。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## 接続について {#concept_E2F3B7E7521147479E5948A94BB3A40B}

「接続」を使用すると、検索ロボットがWebサイトのインデックス作成に使用するHTTP接続を10個まで追加できます。

接続数を増やすと、クロールとインデックスの完了に要する時間が大幅に短縮されます。 ただし、接続を追加するたびに、サーバーの負荷が増えることに注意してください。

## 接続を追加してインデックス作成速度を向上 {#task_3E9B83E43C1842A19066355A15C4A6FB}

「接続」を使用すると、Webサイトのインデックス作成に要する時間を短縮できます。クローラーで使用するHTTP接続の同時数を増やすことができます。 10個までの接続を追加できます。

接続が追加されるたびに、サーバーに負荷がかかることに注意してください。

**接続を追加してインデックス作成速度を上げるには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Connections]**。
1. ページの [!DNL Parallel Indexing Connections] フィールドに、追加する接続数(1 ～ 10)を **[!UICONTROL Number of Connections]** 入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## フォーム送信について {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

フォームの送信を使用すると、Webサイト上のフォームを認識して処理するのに役立ちます。

Webサイトのクロールおよびインデックス作成中に、検出された各フォームが、追加したフォーム定義と比較されます。 フォームがフォーム定義と一致する場合は、インデックス作成のためにフォームが送信されます。 フォームが複数の定義と一致する場合は、一致する定義ごとに1回フォームが送信されます。

## Webサイト上のフォームのインデックス作成用のフォーム定義の追加 {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

を使用すると、Webサイト [!DNL Form Submission] で認識されるフォームをインデックス作成の目的で処理できます。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**Webサイト上のフォームのインデックス作成用のフォーム定義を追加するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Form Submission]**。
1. ページで、 [!DNL Form Submission] をクリックし **[!UICONTROL Add New Form]**&#x200B;ます。
1. ページで、 [!DNL Add Form Definition] とのオプション [!DNL Form Recognition] を設定し [!DNL Form Submission] ます。

   ページの [!DNL Form Recognition][!DNL Form Definition] セクションにある5つのオプションは、処理可能なWebページ内のフォームを識別するために使用されます。

   この [!DNL Form Submission] セクションの3つのオプションを使用して、フォームと共にWebサーバーに送信されるパラメーターと値を指定します。

   1行につき1つの認識または送信パラメータを入力します。 各パラメーターには、名前と値を含める必要があります。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>フォーム認識</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ページURLマスク </p> </td> 
      <td colname="col2"> <p>フォームを含むWebページを識別します。 単一のページに表示されるフォームを識別するには、次の例のようにそのページのURLを入力します。 </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>複数のページに表示されるフォームを識別するには、ページの説明にワイルドカードを使用するURLマスクを指定します。 例えば、ASPページ上で発生したフォームを識別する <code> https://www.mydomain.com/register/ </code>には、次のように指定します。 </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>また、正規式を使用して複数のページを識別することもできます。 単に 
      <userinput>
        regexp 
      </userinput> キーワードを使用してURLマスクを設定する方法を示します。 </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLマスク </p> </td> 
      <td colname="col2"> <p>Folio Builderの 
      <userinput>
        &lt;form&gt; 
      </userinput> 。 </p> <p>ページのURLマスクと同様に、アクションのURLマスクは、単一のURL、ワイルドカードを含むURLまたは正規式の形式にすることができます。 </p> <p>URLマスクは、次のいずれかになります。 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 次のようなフルパス。 <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 次のような部分的なパスです。 <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 以下のようなワイルドカードを使用するURL。 <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 次のような正規式。 <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URLマスクまたはアクションURLマスクで識別されるページのテキストのインデックスを作成しない場合、またはこれらのページにリンクを追跡したくない場合、 
      <userinput>
        noindex 
      </userinput> および 
      <userinput>
        nofollow 
      </userinput> キーワード。 URLマスクまたは入力ポイントを使用して、これらのキーワードをマスクに追加できます。 </p> <p>URL入力ポイント <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> <p>URLマスク <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名マスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      <userinput>
        &lt;form&gt; 
      </userinput> webページのタグにはname属性が含まれます。 </p> <p>単純な名前( 
      <userinput>
        login_form 
      </userinput>)の場合、名前にワイルドカード( 
      <userinput>
        form* 
      </userinput>)または正規式( 
      <userinput>
        regexp ^.*許可します。*$ 
      </userinput>と呼ばれていました）のリリース情報も含まれています。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにしておくことができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォームIDマスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      <userinput>
        &lt;form&gt; 
      </userinput> webページのタグにはid属性が含まれます。 </p> <p>単純な名前( 
      <userinput>
        login_form 
      </userinput>)の場合、名前にワイルドカード( 
      <userinput>
        form* 
      </userinput>)または正規式( 
      <userinput>
        regexp ^.*許可します。*$ 
      </userinput>と呼ばれていました）のリリース情報も含まれています。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにしておくことができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>名前付きパラメーターまたは名前付きパラメーターを含むフォーム、または含まないフォームを特定の値で識別します。 </p> <p>例えば、rick_brough@mydomain.comにプリセットされ、パスワードパラメーターは含まれ、名称パラメーターは含まれない電子メールパラメーターを含むフォームを識別するには、次のパラメーター設定を1行に1つずつ指定します。 </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>フォーム送信</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLを上書き </p> </td> 
      <td colname="col2"> <p>フォーム送信のターゲットが、フォームのアクション属性で指定されたものと異なる場合に指定します。 </p> <p>例えば、フォーム内のURL値とは異なるURL値を構成するJavaScript関数を使用してフォームが送信される場合に、このオプションを使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Overrideメソッド </p> </td> 
      <td colname="col2"> <p>フォーム送信のターゲットがフォームのaction属性で使用されているものと異なる場合、およびJavaScriptの送信によってメソッドが変更された場合に指定します。 </p> <p>すべてのフォームパラメーターのデフォルト値( 
      <userinput>
        &lt;入力&gt; 
      </userinput> タグ（非表示フィールドを含む）、デフォルト 
      <userinput>
        &lt;オプション&gt; 
      </userinput> から 
      <userinput>
        &lt;選択&gt; 
      </userinput> タグと、 
      <userinput>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </userinput> タグ)は、Webページから読み取られます。 ただし、「 <span class="wintitle"> フォーム送信」 </span> セクションの「パラメータ」フィールドにリストされているすべてのパラメーターは、フォームのデフォルト値 <span class="uicontrol"></span> に置き換えられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>フォーム送信パラメーターに 
      <userinput>
        は 
      </userinput> keyword. </p> <p>パラメーターのプレフィックスに 
      <userinput>
        は 
      </userinput>の場合、フォームの送信の一部として送信されません。 この動作は、送信する必要があるチェックボックスの選択を解除した場合に役立ちます。 </p> <p>例えば、次のパラメーターを送信するとします。 </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 値を含む電子メールパラメーター 
      <userinput>
        nobody@mydomain.com 
      </userinput> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 値を持つパスワードパラメーター 
      <userinput>
        trime 
      </userinput> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckboxパラメーターの選択が解除されている。 </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>その他すべて 
      <userinput>
        &lt;form&gt; 
      </userinput> パラメーターのデフォルト値 </p> </li> 
      </ul> </p> <p>フォーム送信パラメーターは次のようになります。 </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>メソッドの属性 
      <userinput>
        &lt;form&gt; 
      </userinput> タグを使用して、GETメソッドまたはPOSTメソッドを使用して、データをサーバーに送信するかどうかを決定します。 </p> <p>    
      <userinput>
        &lt;form&gt; 
      </userinput> タグにmethod属性が含まれていない場合、フォームはGETメソッドを使用して送信されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## フォーム定義の編集 {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Webサイト上のフォームが変更された場合や、定義を変更する必要が生じた場合は、既存のフォーム定義を編集できます。

フォーム定義に対して行った変更を元に戻す [!DNL History] 機能は [!DNL Form Submission] ページにないことに注意してください。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**フォーム定義を編集するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Form Submission]**。
1. ページ上で、更新す [!DNL Form Submission]**[!UICONTROL Edit]** るフォーム定義の右側をクリックします。
1. ページで、 [!DNL Edit Form Definition] とのオプション [!DNL Form Recognition] を設定し [!DNL Form Submission] ます。

   Webサイト上のフォームのインデックス作成に関するフォーム定義の [追加のオプションの表を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## フォーム定義の削除 {#task_C350FC0CDE344F2786215D544C048B5E}

Webサイトにフォームが存在しなくなった場合や、特定のフォームを処理してインデックスを作成したくない場合は、既存のフォーム定義を削除できます。

フォーム定義に対して行った変更を元に戻す [!DNL History] 機能は [!DNL Form Submission] ページにないことに注意してください。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ステージングされたWebサイトの増分インデックスの [設定を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)。

**フォーム定義を削除するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Form Submission]**。
1. ページ上で [!DNL Form Submission] 、削除するフォーム定義 **[!UICONTROL Delete]** の右側をクリックします。

   削除するフォーム定義が正しいことを確認してください。 次の手順でをクリックしたときに、削除の確認ダイアログボックス **[!UICONTROL Delete]** は表示されません。
1. ページで、 [!DNL Delete Form Definition] をクリックし **[!UICONTROL Delete]**&#x200B;ます。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## インデックスコネクタについて {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

XMLページ [!DNL Index Connector] や任意のフィードのインデックス作成に使用する追加の入力ソースを定義する場合に使用します。

データフィード入力ソースを使用すると、Webサイトで一般に見つかるものとは異なるフォームに保存されたコンテンツに、利用可能なクロール方法の1つを使用してアクセスできます。 クロールおよびインデックス付けされた各ドキュメントは、Webサイト上のコンテンツページに直接対応しています。 ただし、データフィードはXMLドキュメントから、またはカンマ区切りまたはタブ区切りのテキストファイルから取得され、インデックスを作成するコンテンツ情報が含まれます。

XMLデータソースは、個々のドキュメントに対応する情報を含むXMLスタンザス（レコード）で構成されます。 これらの個々のドキュメントはインデックスに追加されます。 テキストデータフィードには、個々のドキュメントに対応する個々の改行区切りレコードが含まれています。 これらの個々のドキュメントもインデックスに追加されます。 どちらの場合も、インデックスコネクタ設定は、フィードの解釈方法を説明します。 各設定では、ファイルの保存場所と、サーバーがファイルにアクセスする方法が説明されます。 この設定では、「マッピング」情報も説明します。 つまり、各レコードの項目を使用して、結果のインデックスにメタデータフィールドを埋め込む方法です。

インデックスコネクタ定義を [!DNL Staged Index Connector Definitions] ページに追加した後で、「名前」または「種類」の値を ** 除く、任意の設定を変更できます。

この [!DNL Index Connector] ページには、以下の情報が表示されます。

* 設定および追加した、定義済みのインデックスコネクタの名前。
* 追加した各コネクタに対して、次のいずれかのデータソースの種類を指定します。

   * **テキスト** — 単純な「フラット」ファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。
   * **フィード** - XMLフィード
   * **XML** - XMLドキュメントのコレクション。

* 次回のクロールとインデックス作成に対してコネクタが有効かどうかを示します。
* データソースのアドレス。

Index Connectorにつ [いても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## インデックスコネクタのテキスト設定とフィード設定でのインデックス作成プロセスの動作 {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手順 </p> </th> 
   <th colname="col2" class="entry"> <p>手順 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードします。 </p> </td> 
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、ファイルのダウンロードは簡単です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p>テ <span class="uicontrol"> キスト </span>の場合、改行で区切られた各テキスト行は、個々のドキュメントに対応し、カンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p>フィ <span class="uicontrol"></span>ードの場合、各ドキュメントのデータは、次の形式の正規式パターンを使用して抽出されます。 </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>「 <span class="uicontrol"> Index Connector」 </span> ページの <span class="wintitle"></span> マップを使用して、データのキャッシュ済みコピーを作成し、クローラのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが入力されます。 </p> <p>解析済みデータがローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラが必要とする単純なHTMLドキュメントが作成されます。 例： </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span> 要素は、タイトルメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 同様に、 <span class="codeph"> &lt;body&gt; </span> 要素は、Bodyメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>: 事前定義済みのURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングに対して、 <span class="codeph"> &lt;meta&gt; </span> タグは、元のドキュメントで見つかったデータを持つ各フィールドに対して生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれるドキュメントごとに、次の例のようなリンクも生成されます。 </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングには、プライマリキーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取得される際に使用されるキーを形成します。 </p> <p>クローラはURL <span class="codeph"> インデックスを認識します。 </span> スキームのプレフィックスが追加され、ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p>インデックス <span class="codeph"> : </span> リンクは、クローラの保留リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、ドキュメントのデータがキャッシュから取得されます。 その後、HTML画像を「アセンブル」し、処理してインデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## インデックスコネクタのXML設定でのインデックス作成プロセスの動作 {#section_7F1551EA51854C5C99F284CE260526EB}

XML設定のインデックス作成プロセスは、テキスト設定とフィード設定のプロセスと似ていますが、以下の小さな変更と例外があります。

XMLクロールのドキュメントは既に個別のファイルに分けられているので、上記の表の手順1と2は直接適用されません。 ページの「」 **[!UICONTROL Host Address]** と「」 **[!UICONTROL File Path]** フィールドにURLを指定すると、 [!DNL Index Connector Add] ページは通常のHTMLドキュメントとしてダウンロードされ、処理されます。 ダウンロードドキュメントには、処理されるXMLドキュメントを指すリンクのコレクションが含まれていることを期待します。 `<a href="{url}"...` 各リンクは、 そのようなリンクは次の形式に変換されます。

```
<a href="index:<ic_config_name>?url="{url}">
```

例えば、アドビの設定から次のリンクが返された場合：

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

上の表では、手順3は適用されず、クロールおよびインデックス作成時に手順4が完了します。

または、XMLドキュメントを、クロールプロセスによって自然に発見された他のドキュメントと混在させることもできます。 そのような場合は、書き換えルール( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**)を使用してXMLドキュメントのURLを変更し、それらをIndex Connectorに送信できます。

「クロールリスト取得URLルール [について](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)」を参照してください。

例えば、次の書き換えルールがあるとします。

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

このルールは、で終わるすべてのURLをインデックスコネクタリンク `.xml` に変換します。 クローラは、 `index:` URLスキームを認識して書き換えます。 ダウンロードプロセスは、プライマリ上のIndex Connector Apacheサーバーを通じてリダイレクトされます。 ダウンロードされた各ドキュメントは、フィードで使用されるのと同じ正規式パターンを使用して調べられます。 ただし、この場合、製造されたHTMLドキュメントはキャッシュに保存されません。 代わりに、インデックス処理用にクローラに直接渡されます。

## 複数のインデックスコネクタを設定する方法 {#section_C2B14C0F06354A57AEF6238FF3814E5D}

任意のアカウントに対して複数のインデックスコネクタ設定を定義できます。 次の図に示すように、設定は、 **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** >のドロップダウンリスト **[!UICONTROL URL Entrypoints]** に自動的に追加されます。

![](assets/url_entrypoints_index_connector.png)

ドロップダウンリストから設定を選択すると、URLエントリポイントのリストの最後に値が追加されます。

>[!NOTE]
>
>無効なインデックスコネクタの設定はドロップダウンリストに追加されますが、選択することはできません。 同じインデックスコネクタの設定を2回目に選択した場合は、設定がリストの最後に追加され、前のインスタンスが削除されます。

増分クロールのインデックスコネクタエントリポイントを指定するには、次の形式を使用してエントリを追加します。

```
index:<indexconnector_configuration_name>
```

[インデックスコネクタ]ページで追加された各エントリが見つかり、有効になっている場合、クローラは追加された各エントリを処理します。

注意： 各ドキュメントのURLはインデックスコネクタ設定名とドキュメントの主キーを使用して構築されるので、増分更新を実行する際は、必ず同じインデックスコネクタ設定名を使用してください。 これにより、以前にインデックス付けさ [!DNL Adobe Search&Promote] れたドキュメントを正しく更新できます。

「URL入力ポイント [について](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)」も参照してください。

**インデックスコネクタを追加する際のセットアップマップの使用**

インデックスコネクタを追加する際、必要に応じてこの機能を使用して、データソースのサンプル **[!UICONTROL Setup Maps]** をダウンロードできます。 データは、インデックスの適合性を調べられます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>インデックスコネクタの種類を選択した場合 </p> </th> 
   <th colname="col2" class="entry"> <p>設定マップ機能 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>テキスト </p> </td> 
   <td colname="col2"> <p>最初にタブを試し、次に縦棒( <span class="codeph"> | </span>)を挿入し、最後にコンマ( <span class="codeph"> , </span>)を挿入します。 「マップの <span class="uicontrol"> 設定」をクリックする前に、既に区切り値を指定している場合は、代わりにその値が使用され </span>ます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なタグとフィールドの値に推測値が入力されます。 さらに、解析済みデータのサンプリングも表示されます。 ファイルにヘッダー行が含まれている場合は、必ず「 <span class="uicontrol"> 先頭行のヘッダー」を選択し </span> てください。 この情報は、設定関数で結果のマップエントリを識別しやすくするために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子はMapテーブルのタグ行に表示され、同様の値はFieldsにも表示されます。 これらの行は使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータの説明とItemtagの値の識別を行うので、この方法は役に立ちます。 </p> <p> <p>注意：  セットアップマップ機能は、XMLソース全体をダウンロードして分析を実行します。 ファイルのサイズが大きい場合は、この操作がタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は可能なすべてのXPath項目を識別しますが、その多くは使用が望ましくない項目です。 結果のMap定義を確認し、不要または不要なMap定義を削除してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>プライマリリンクリストではなく、個々のドキュメントを代表するユーザーのURLをダウンロードします。 この単一のドキュメントは、フィードで使用されるのと同じメカニズムを使用して解析され、結果が表示されます。 </p> <p>設定を保存するには、「追加」をクリックする前に、URLをプライマリリンクリストドキュメントに戻す必要があります。 <span class="uicontrol"></span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**重要**: サイズの大きいXMLデータセットでは、ファイルパーサーがファイル全体をメモリに読み込もうとするので、セットアップマップ機能が動作しない場合があります。 その結果、メモリ不足状態が発生する可能性があります。 ただし、インデックス作成時に同じドキュメントが処理された場合、メモリへの読み込みは行われません。 その代わりに、大きなドキュメントは「外出中」に処理され、最初にメモリに完全に読み込まれるわけではありません。

**インデックスコネクタを追加する際のプレビューの使用**

インデックスコネクタを追加する際、オプションでこの機能を使用して、データを保存しているかのよう **[!UICONTROL Preview]** に、データを検証できます。 設定をアカウントに保存せずに、設定に対するテストを実行します。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。 インデックス作成クローラが使用するメインキャッシュフォルダと競合しません。

プレビューは、 Acct:IndexConnector-プレビュー-Max-ドキュメントで制御される5つのドキュメントのデフォルトのみを処理します。 プレビューしたドキュメントは、インデックス作成クローラに表示されるとおり、ソース形式で表示されます。 表示は、Webブラウザーの「表示ソース」機能に似ています。 標準のナビゲーションリンクを使用して、プレビューセット内のドキュメントを移動できます。

プレビューはXML設定をサポートしません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## インデックスコネクタ定義の追加 {#task_96779B651A654E1F871F55D6DBBC8886}

各インデックスコネクタの設定は、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

新しい有効な定義の効果がユーザーに表示される前に、サイトインデックスを作成し直します。

**インデックスコネクタ定義を追加するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページで、 [!DNL Stage Index Connector Definitions] をクリックし **[!UICONTROL Add New Index Connector]**&#x200B;ます。
1. ページで、目的のコネクタオプションを設定 [!DNL Index Connector Add] します。 使用できるオプションは、選択したオプションによ **[!UICONTROL Type]** って異なります。

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>オプション </p> </th> 
      <th colname="col2" class="entry"> <p>説明 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>名前 </p> </td> 
      <td colname="col2"> <p>インデックスコネクタ設定の一意の名前です。 英数字を使用できます。 「_」と「 — 」も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択したデータソースの種類は、 <span class="wintitle"> インデックスコネクタ追加 </span> ページで使用できる結果のオプションに影響します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行で区切られた各行のテキストは、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）を、1から始まる列番号で参照されるメタデータフィールドにマップできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むプライマリXMLドキュメントをダウンロードします。 </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>リンク( 
      <userinput>
        &lt;a&gt; 
      </userinput>)を個々のXMLドキュメントに追加します。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類： テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>: 無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p> または </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドに対する適切なエントリに分類されます。 </p> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incremental File Path </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 ファイルを指定しない場合は、代わりにFile Pathの下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直ファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新時に使用する単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、 <span class="uicontrol"> プライマリキーとして指定された列の、FullまたはIncremental File Pathファイル内の値に対応する必要があり </span>ます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTP、またはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で設定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、またはHTTPS接続の最大再試行数を指定します。 この値は0 ～ 10の範囲で設定する必要があります。 </p> <p>値が0の場合は、再試行を禁止します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの各フィールドの説明文字として使用する文字を指定します。 </p> <p>カンマ文字( <span class="codeph"> , </span>)は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るのに役立つフィールド区切り文字として機能します。 </p> <p>タブを選択し <span class="uicontrol"> ますか？ </span> をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭行のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>インデックス作成用の最小ドキュメント数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>: この機能は、完全なインデックス処理でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1にして、列番号を指定します。 各列に新しいマップ行を追加するには、「 <span class="wintitle"> アクション」で、「 </span>+」をクリックし <span class="uicontrol"></span>ます。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップすることもできます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p>「 <span class="uicontrol"> フィールド」 </span> がドロップダウンリストになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応じて、「 <span class="uicontrol"></span> フィールド」の値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、 <span class="wintitle"> フィルタリングスクリプトで使用するコンテンツの作成に役立つ場合があり </span>ます。 </p> <p>フィルタリングスクリプト <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field </span> 値が、定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには <span class="wintitle"> 許可リスト </span> 属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p>プライマリ <span class="uicontrol"> キーの </span> 値は、インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が発生した場合は無視されます。 ソースドキュメントに <span class="uicontrol"> プライマリキーとして使用する一意の値が1つだけない </span>場合に、2つ以上のフィールドを一緒に使用して一意の識別子を形成できる場合は <i>、複数の列の値を縦棒(")で区切って、</i><span class="uicontrol"></span><span class="uicontrol"></span> プライマリキーを定義できます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類： フィード</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>: 無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>複数の「行」情報を含むプライマリXMLドキュメントへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incremental File Path </p> </td> 
      <td colname="col2"> <p>複数の「行」情報を含む増分XMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 ファイルを指定しない場合は、代わりにFile Pathの下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直ファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新時に使用する複数の疎な「行」ドキュメントを含むXML情報へのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、 <span class="uicontrol"> プライマリキーとして指定された列の、FullまたはIncremental File Pathファイル内の値に対応する必要があり </span>ます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、Adobe XMLドキュメントの次のフィードフラグメントでは、Itemtagの値は <span class="codeph"> recordで </span>す。 </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>インデックス作成用の最小ドキュメント数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>: この機能は、完全なインデックス処理でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータとのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析済みXMLデータのXPath表現を指定します。 上記のAdobe XMLドキュメントの例を使用して、Itemtagオプションの下で、次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>レコード <span class="codeph"> 要素の </span> displayurl <span class="codeph"> 属性は、メタデータフィールド </span> のpage-urlにマップされ <span class="codeph"></span>ます。 </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>メタ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタ要素内に含まれるメタ要素、メタデータ要素内に含まれる <span class="codeph"> 要素、メタデータ要素内に含まれる要素名をメタデータフィールド要素とメタデータフィールド要素 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>とを対応付ける要素 </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>メタ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタ要素内に含まれるメタ要素、メタデータ要素内に含まれる <span class="codeph"> 要素、メタデータ要素内に含まれる要素名の説明、メタデータフィールドの属性 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>とメタデータフィールドの説明とを対応付ける要素。 </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>メタデータ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタデータ要素内に含まれるメタ <span class="codeph"> 要素、メタデータ要素内に含まれる </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素、メタデータ要素内に含まれる名前を記述し、メタデータフィールド本体に対する属性をマップする要素。 </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p>https://www.w3schools.com/xpath/を参照して <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> ください。 </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各 <span class="codeph"> &lt;meta&gt; </span> タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p>「 <span class="uicontrol"> フィールド」 </span> がドロップダウンリストになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応じて、「 <span class="uicontrol"></span> フィールド」の値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、 <span class="wintitle"> フィルタリングスクリプトで使用するコンテンツの作成に役立つ場合があり </span>ます。 </p> <p>フィルタリングスクリプト <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field </span> 値が、定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには <span class="wintitle"> 許可リスト </span> 属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p>プライマリ <span class="uicontrol"> キーの </span> 値は、インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が発生した場合は無視されます。 ソースドキュメントに <span class="uicontrol"> プライマリキーとして使用する一意の値が1つだけなく、2つ以上のフィールドを一緒に使用して一意のを作成 </span>できる場合は <i>、複数の</i><span class="uicontrol"></span><span class="uicontrol"></span> プライマリタグを縦棒(")で結合して、キーを定義します。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 削除に使用しますか？ </span> <p>Incremental Index操作でのみ使用されます。 このXPathパターンに一致するレコードは、削除対象の項目を識別します。 これらの各レコードの <span class="uicontrol"> プライマリキー </span> 値は、Delete File Pathと同様に、「削除」リクエストの作成に使用されます。 </p> <p> <b>注意</b>: この機能は、デフォルトでは有効になっていません。 お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類： XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>: 無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>リンク( 
      <userinput>
        &lt;a&gt; 
      </userinput>)を個々のXMLドキュメントに追加します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> File </li> 
      </ul> </p> <p> <b>注意</b>: プロトコル設定は、「ホストアドレス」または「ファイルパス」フィールドに情報が指定されている場合にのみ使用されます。 個々のXMLドキュメントは、URLの仕様に従って、HTTPまたはHTTPSを使用してダウンロードされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの「行」を定義するXML要素を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> タグ </span> <p>解析済みXMLデータのXPath表現を指定します。 上記のAdobe XMLドキュメントの例で、Itemtagオプションの下の次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>レコード <span class="codeph"> 要素の </span> displayurl <span class="codeph"> 属性は、メタデータフィールド </span> のpage-urlにマップされ <span class="codeph"></span>ます。 </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>メタ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタ要素内に含まれるメタ要素、メタデータ要素内に含まれる <span class="codeph"> 要素、メタデータ要素内に含まれる要素名をメタデータフィールド要素とメタデータフィールド要素 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>とを対応付ける要素 </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>メタ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタ要素内に含まれるメタ要素、メタデータ要素内に含まれる <span class="codeph"> 要素、メタデータ要素内に含まれる要素名の説明、メタデータフィールドの属性 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>とメタデータフィールドの説明とを対応付ける要素。 </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>メタデータ要素内に含まれる <span class="codeph"> メタ要素の </span> 内容属性、メタデータ要素内に含まれるメタ <span class="codeph"> 要素、メタデータ要素内に含まれる </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素、メタデータ要素内に含まれる名前を記述し、メタデータフィールド本体に対する属性をマップする要素。 </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p>https://www.w3schools.com/xpath/を参照して <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> ください。 </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> メタデータ? </span> <p>「 <span class="uicontrol"> フィールド」 </span> がドロップダウンリストになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応じて、「 <span class="uicontrol"></span> フィールド」の値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、 <span class="wintitle"> フィルタリングスクリプトで使用するコンテンツの作成に役立つ場合があり </span>ます。 </p> <p>フィルタリングスクリプト <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> についてを参照してくだ </a>さい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field </span> 値が、定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには <span class="wintitle"> 許可リスト </span> 属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p>プライマリ <span class="uicontrol"> キーの </span> 値は、インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が発生した場合は無視されます。 ソースドキュメントに <span class="uicontrol"> プライマリキーとして使用する一意の値が1つだけなく、2つ以上のフィールドを一緒に使用して一意のを作成 </span>できる場合は <i>、複数の</i><span class="uicontrol"></span><span class="uicontrol"></span> プライマリタグを縦棒(")で結合して、キーを定義します。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）をクリック **[!UICONTROL Setup Maps]** して、データソースのサンプルをダウンロードします。 データは、インデックスの適合性を調べられます。 この機能は、テキストおよびフィードのタイプでのみ使用できます。
1. （オプション）をクリック **[!UICONTROL Preview]** して、設定の実際の動作をテストします。 この機能は、テキストおよびフィードのタイプでのみ使用できます。
1. をクリック **[!UICONTROL Add]** して、設定をページおよび [!DNL Index Connector Definitions] ページ上の [!DNL Index Connector Configurations] ドロップダウンリストに追加し [!DNL URL Entrypoints] ます。

   「URL入力ポイント [について](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)」を参照してください。
1. ページで、 [!DNL Index Connector Definitions] をクリックし **[!UICONTROL rebuild your staged site index]**&#x200B;ます。
1. （オプション） [!DNL Index Connector Definitions] ページで、次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## インデックスコネクタ定義の編集 {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

定義した既存のインデックスコネクタを編集できます。

>[!NOTE]
>
>ドロップダウンリストから「インデックスコネクタ名」や「種類」など、変更できるオプションは [!DNL Type] ありません。

**インデックスコネクタ定義を編集するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページの列見出しの下で、設定を変更す [!DNL Index Connector][!DNL Actions]**[!UICONTROL Edit]** るインデックスコネクタ定義名をクリックします。
1. ページで、目的のオプション [!DNL Index Connector Edit] を設定します。

   「インデックスコネクタ定義の [追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション） [!DNL Index Connector Definitions] ページで、をクリックし **[!UICONTROL rebuild your staged site index]**&#x200B;ます。
1. （オプション） [!DNL Index Connector Definitions] ページで、次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## インデックスコネクタ定義の設定の表示 {#task_D0B71A7426E54247BDB3468EC576D871}

既存のインデックスコネクタ定義の設定を確認できます。

インデックスコネクタ定義を [!DNL Index Connector Definitions] ページに追加した後は、その種類の設定を変更できません。 代わりに、定義を削除してから、新しい定義を追加する必要があります。

**インデックスコネクタ定義の設定を表示するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページの列見出しの下で、設定を確認または編集す [!DNL Index Connector][!DNL Actions]**[!UICONTROL Edit]** るインデックスコネクタ定義名をクリックします。

## インデックスコネクタ定義のコピー {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

既存のインデックスコネクタ定義をコピーして、作成する新しいインデックスコネクタの基本として使用できます。

インデックスコネクタ定義をコピーする場合、コピーされた定義はデフォルトで無効になります。 定義を有効または「有効にする」には、 [!DNL Index Connector Edit] ページで定義を編集し、を選択する必要があり **[!UICONTROL Enable]**&#x200B;ます。

「インデックスコネクタ定義の [編集](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)」を参照してください。

**インデックスコネクタ定義をコピーするには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページの列見出しの下で、設定を重複する [!DNL Index Connector] インデックスコネクタ定義名 [!DNL Actions]**[!UICONTROL Copy]** をクリックします。
1. ページで、定義の新しい名前を [!DNL Index Connector Copy] 入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション） [!DNL Index Connector Definitions] ページで、次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## インデックスコネクタ定義の名前の変更 {#task_5132118FC21B47D99881E0ED425225D7}

既存のインデックスコネクタ定義の名前を変更できます。

定義の名前を変更したら、 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** >を選択し **[!UICONTROL URL Entrypoints]**&#x200B;ます。 新しい定義名が [!DNL URL Entrypoints] ページのドロップダウンリストに反映されるようにする必要がある。

詳しくは、インデックスを作成する複数のURLエントリポイントの [追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

**インデックスコネクタ定義の名前を変更するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページの列見出しの下で、変更するインデックスコネクタ定義名 [!DNL Index Connector][!DNL Actions]**[!UICONTROL Rename]** をクリックします。
1. ページで、 [!DNL Index Connector Rename] フィールドに定義の新しい名前を入力し [!DNL Name] ます。
1. クリック **[!UICONTROL Rename]**.
1. Click **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. リストに以前のインデックスコネクタの名前が存在する場合は、その名前を削除し、新しく名前を変更したエントリを追加します。

   詳しくは、インデックスを作成する複数のURLエントリポイントの [追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。 1.（オプション） [!DNL Index Connector Definitions] ページで、次のいずれかの操作を行います。

   * をクリック **[!UICONTROL History]** すると、行った変更がすべて元に戻ります。

      「Historyオプションの [使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)」を参照してください。

   * クリック **[!UICONTROL Live]**.

      ライブ設定の [表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、 [ステージ設定をライブにプッシュするを参照してください](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)。

## インデックスコネクタ定義の削除 {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

不要になった、または使用しなくなった既存のインデックスコネクタ定義は削除できます。

**インデックスコネクタ定義を削除するには**

1. 製品メニューで、//をクリックし **[!UICONTROL Settings]** ま **[!UICONTROL Crawling]** す **[!UICONTROL Index Connector]**。
1. ページの列見出しの下で、削除するインデックスコネクタ定義名 [!DNL Index Connector Definitions][!DNL Actions]**[!UICONTROL Delete]** をクリックします。
1. ページで、 [!DNL Index Connector Delete] をクリックし **[!UICONTROL Delete]**&#x200B;ます。
