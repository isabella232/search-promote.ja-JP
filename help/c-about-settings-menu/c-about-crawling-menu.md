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
source-git-commit: 77a4e88c7bf47b637030e3935a39dfdf4f175e80

---


# クロールメニューについて{#about-the-crawling-menu}

クロールメニューの設定日、URLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URL入力ポイントを使用します。

## URL入力ポイントについて {#concept_5D857E3B5C124E85BC0B5AE77A509573}

ほとんどのWebサイトには、顧客が最初に訪問する主なエントリポイントまたはホームページが1つあります。 このメインエントリポイントは、検索ロボットがインデックスのクロールを開始するURLアドレスです。 ただし、Webサイトに複数のドメインまたはサブドメインがある場合、またはサイトの一部がプライマリエントリポイントからリンクされていない場合は、「URLエントリポイント」を使用してエントリポイントを追加できます。

指定した各URLエントリポイントより下のすべてのWebサイトページのインデックスが作成されます。 URLエントリポイントをマスクと組み合わせて、Webサイトのどの部分にインデックスを付けるかを正確に制御できます。 URL入力ポイントの設定の効果がユーザーに表示される前に、Webサイトのインデックスを再構築する必要があります。

通常、メインのエントリポイントは、インデックスを作成して検索するWebサイトのURLです。 この主なエントリポイントは、「アカウントの設定」で設定します。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

メインURLエントリポイントを指定した後、必要に応じて、クロールする追加のエントリポイントを順番に指定できます。 多くの場合、メインエントリポイントの下のページからリンクされていないWebページに対して、追加のエントリポイントを指定します。 次の例のように、Webサイトが複数のドメインにまたがる場合は、追加のエントリポイントを指定します。

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

各エントリポイントを、次の表に示す1つ以上のスペース区切りキーワードで修飾します。 これらのキーワードは、ページのインデックス化方法に影響を与えます。

**重要**:特定のキーワードをエントリポイントとスペースで区切ります。コンマは有効な区切り文字ではありません。

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
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成せず、ページのリンク先に移動する場合は、 
     <userinput>
       noindex 
     </userinput> をクリックします。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>このキーワードは、 
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
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成する際に、ページのリンクをたどらない場合は、 
     <userinput>
       nofollow 
     </userinput> をクリックします。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>このキーワードは、 
     <userinput>
       content="nofollow" 
     </userinput> between 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> タグを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>form </p> </td> 
   <td colname="col2"> <p> エントリポイントがログインページの場合、 
     <userinput>
       form 
     </userinput> は、通常、検索ロボットがログインフォームを送信し、適切なcookieを受け取ってからWebサイトをクロールできるようにするために使用されます。 「form」キーワードを使用すると、エントリポイントページのインデックスは作成されず、検索ロボットはエントリポイントページをクロール済みとしてマークしません。 使用 
     <userinput>
       nofollow 
     </userinput> 検索ロボットがページのリンクをたどらないようにする場合。 </p> </td> 
  </tr> 
 </tbody> 
</table>

コンテンツタイプに [ついても参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)い。

インデックスコネク [タについても参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)い。

## インデックスを作成する複数のURLエントリポイントの追加 {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Webサイトに複数のドメインまたはサブドメインがあり、それらをクロールする場合は、URL入力ポイントを使用してURLを追加できます。

WebサイトのメインURLエントリポイントを設定するには、「アカウントの設定」を使用します。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

**インデックスを作成する複数のURLエントリポイントを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Entrypoints]**。
1. ページの [!DNL URL Entrypoints] フィールドに、1 [!DNL Entrypoints] 行につき1つのURLアドレスを入力します。
1. （オプション）ドロッ **[!UICONTROL Add Index Connector Configurations]** プダウンリストで、インデックス作成のエントリポイントとして追加するインデックスコネクタを選択します。

   ドロップダウンリストは、1つ以上のインデックスコネクタ定義を以前に追加した場合にのみ使用できます。

   ![](assets/url_entrypoints_index_connector.png)

   詳しくは、 [インデックスコネクタ定義の追加を参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)い。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## URLマスクについて {#concept_8039DFC53FF3410AA494D602F71BA164}

URLマスクは、検索ロボットがインデックスを作成するか、インデックスを作成しないかを判断するパターンです。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

使用できるURLマスクは次の2種類です。

* URLマスクを含める
* URLマスクの除外

「URLマスクを含める」は、検索ロボットに対し、マスクのパターンに一致するドキュメントのインデックスを作成するよう指示します。

「URLマスクを除外」は、検索ロボットに対して、一致するドキュメントのインデックスを作成するよう指示します。

検索ロボットは、リンクからWebサイト内のリンクに移動する際に、URLを検出し、それらのURLに一致するマスクを探します。 最初の一致によって、そのURLをインデックスに含めるか除外するかが決まります。 検出されたURLに一致するマスクがない場合、そのURLはインデックスから破棄されます。

エントリポイントURLのURLマスクを含めると、自動的に生成されます。 この動作により、Webサイト上で遭遇したすべてのドキュメントのインデックスが作成されます。 また、Webサイトから「離脱」するリンクも便利に廃止されます。 例えば、インデックス付きのページがhttps://www.yahoo.comにリンクしている場合、検索ロボットはそのURLのインデックスを作成しません。これは、エントリポイントURLによって自動的に生成されるインクルードマスクと一致しないからです。

指定する各URLマスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* のように完全なパス `https://www.mydomain.com/products.html`。
* のように、部分パス `https://www.mydomain.com/products`。
* に示すように、ワイルドカードを使用するURLで `https://www.mydomain.com/*.html`す。
* 正規表現（上級ユーザー向け）。

   マスクを正規表現にするには、マスクの種類（または） `regexp` とURLマスクの間にキ `exclude` ーワー `include`ドを挿入します。

以下に、除外URLマスクの簡単な例を示します。

```
exclude https://www.mydomain.com/photos
```

この例は除外URLマスクなので、パターンに一致するドキュメントのインデックスは作成されません。 このパターンは、検出されたすべてのアイテム（ファイルとフォルダーの両方）に一致し、除外URL `https://www.mydomain.com/photos.html` に一致する `https://www.mydomain.com/photos/index.html`と、その両方のアイテムのインデックスが作成されないようにします。 フォルダー内のファイルのみを一致さ `/photos/` せるには、次の例のように、URLマスクの末尾にスラッシュを含める必要があります。

```
exclude https://www.mydomain.com/photos/
```

次の除外マスクの例では、ワイルドカードを使用しています。 検索ロボットに対し、拡張子「.pdf」のファイルを見過ごすよう指示します。 検索ロボットは、これらのファイルをインデックスに追加しません。

```
exclude *.pdf
```

単純なインクルードURLマスクは次のとおりです。

```
include https://www.mydomain.com/news/
```

URLエントリポイントから一連のリンクを介してリンクされたドキュメント、またはURLエントリポイント自体として使用されたドキュメントのみがインデックス化されます。 ドキュメントのURLを「URLを含む」マスクとしてリストするだけで、リンクされていないドキュメントのインデックスは作成されません。 リンクされていないドキュメントをインデックスに追加するには、URLエントリポイント機能を使用します。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

「マスクを含める」と「マスクを除外」は連携して機能します。 除外URLマスクを作成し、除外するページのうち1つ以上をURLマスクを含めることで、Webサイトの大部分をインデックス作成から除外できます。 例えば、エントリポイントURLが次のような場合、

```
https://www.mydomain.com/photos/
```

検索ロボットは、と、の下のすべてのページをクロールし、インデックスを作成します。 `/photos/summer/``/photos/spring/` (フォルダから各ディレクトリに少なくとも1つのページへのリンクがあると仮定し `/photos/fall/``photos` ます)。 この動作は、リンクパスを使用して、検索ロボットが、、、および、のフォルダ内のドキュメント、およびフォルダURLを検索でき、エントリポイントURLによって自動的に生成されるインクルードマスクと一致するからです。 `/summer/``/spring/``/fall/`

次の例のように、URLマスクを除外するフォル `/fall/` ダー内のすべてのページを除外するように選択できます。

```
exclude https://www.mydomain.com/photos/fall/
```

または、次のURLマスクを使用して、 `/photos/fall/redleaves4.html` インデックスの一部としてのみ選択的に含めることもできます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

上記の2つのマスクの例が意図したとおりに動作するように、次のように、インクルードマスクが最初に表示されます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

検索ロボットはリストに表示された順に指示に従うので、検索ロボットは最初にを含め、次にフォ `/photos/fall/redleaves4.html`ルダ内の残りのファイルを除外し `/fall` ます。

手順が次とは逆の方法で指定されている場合：

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

その場 `/photos/fall/redleaves4.html` 合、マスクが含めるように指定されていても、含められません。

最初に表示されるURLマスクは、マスク設定の後に表示されるURLマスクよりも常に優先されます。 また、検索ロボットが「URLを含む」マスクと「URLを除外」マスクに一致するページを検出した場合は、最初に表示されるマスクが常に優先されます。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

## URLマスクを使用したキーワードの使用について {#section_7609A7A6D79B482ABCA8900886541AAB}

各インクルードマスクを1つ以上のスペース区切りキーワードで修飾でき、一致したページのインデックスの作成方法に影響を与えます。

コンマは、マスクとキーワードの区切り文字としては無効です。スペースのみを使用できます。

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
   <td colname="col2"> <p> URLマスクに一致するページ上のテキストのインデックスを作成せず、一致したページのリンク先を探す場合は、 
     <userinput>
       noindex 
     </userinput> を追加します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>上の例では、検索ロボットが 
     <userinput>
       .swf 
     </userinput> 拡張子を使用しますが、これらのファイルに含まれるすべてのテキストのインデックス作成を無効にします。 </p> <p>Adobe コード内の   
     <userinput>
       noindex 
     </userinput> キーワードは、 
     <userinput>
       content="noindex" 
     </userinput> between 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> 一致したページのタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> URLマスクと一致するページ上のテキストのインデックスを作成し、一致するページのリンクをたどりたくない場合は、 
     <userinput>
       nofollow 
     </userinput> を追加します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Adobe コード内の   
     <userinput>
       nofollow 
     </userinput> キーワードは、 
     <userinput>
       content="nofollow" 
     </userinput> between 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> 一致したページのタグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用されます。 </p> <p>先頭に 
     <userinput>
       regexp 
     </userinput> は正規表現として扱われます。 検索ロボットが「以下を除外」正規表現URLマスクに一致するドキュメントを検出した場合、それらのドキュメントのインデックスは作成されません。 検索ロボットが正規表現URLマスクを含むドキュメントを検出した場合、それらのドキュメントのインデックスが作成されます。 例えば、次のURLマスクがあるとします。 </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>検索ロボットは、 
     <userinput>
       https://www.mydomain.com/products/page1.html 
     </userinput> </p> <p>次のようなexclude正規表現のURLマスクがある場合： </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>検索ロボットは、 
     <userinput>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </userinput>。 </p> <p>次のような正規表現のURLマスクを含める場合： </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>検索ロボットは、拡張子が「.swf」のファイルのすべてのリンクに従います。 Adobe コード内の   
     <userinput>
       noindex 
     </userinput> keywordは、一致したファイルのテキストのインデックスが作成されないことを指定します。 </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分に対するURLマスクの追加 {#task_E1AFC17C746048B8843013D979E082C1}

を使用して、Webサ [!DNL URL Masks] イトのどの部分をクロールしてインデックスを作成するか、またはインデックスを作成しないかを定義できます。

「URLマスクをテスト」フィールドを使用して、インデックスの作成後にドキュメントが含まれているかどうかをテストします。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**Webサイトのインデックス部分にURLマスクを追加するか、インデックス部分にURLマスクを追加しないかを指定するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Masks]**。
1. （オプション）ページの [!DNL URL Masks] フィールドに、Webサ **[!UICONTROL Test URL Masks]** イトのテストURLマスクを入力し、をクリックします **[!UICONTROL Test]**。
1. フィールド [!DNL URL Masks] に、 `include` （クロールおよびインデックスを作成するWebサイトを追加するには）または `exclude` （Webサイトのクロールおよびインデックス作成をブロックするには）と入力し、URLマスクのアドレスを入力します。

   1行に1つのURLマスクアドレスを入力します。 例：

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 日付マスクについて {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

日付マスクを使用すると、ファイルの年齢に基づいて検索結果にファイルを含めたり、除外したりできます。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

使用できる日付マスクは次の2種類です。

* 日付マスクを含める（「include-days」および「include-date」）

   指定した日付以前の日付のインデックスファイルを日付マスクに含めます。
* 日付マスクの除外（「exclude-days」および「exclude-date」）

   指定した日付以前の日付のインデックスファイルを除外します。

デフォルトでは、ファイルの日付はメタタグ情報から決定されます。 Metaタグが見つからない場合、検索ロボットがファイルをダウンロードしたときにサーバから受信したHTTPヘッダからファイルの日付が決定されます。

指定する各日付マスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* フルパス( `https://www.mydomain.com/products.html`
* 部分パス( `https://www.mydomain.com/products`
* ワイルドカードを使用するURL `https://www.mydomain.com/*.html`
* 正規表現。 マスクを正規表現にするには、URLの前にキーワード `regexp` を挿入します。

「含む」と「除外する」の両方の日付マスクは、次の2つの方法のいずれかで日付を指定できます。 マスクは、一致したファイルが指定した日付以前に作成された場合にのみ適用されます。

1. 日数。 例えば、日付マスクが次のような場合、

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   指定した日数がカウントバックされます。 ファイルの日付が日付に達した日付以前の場合、マスクが適用されます。

1. YYYY-MM-DDの形式を使用した実際の日付。 例えば、日付マスクが次のような場合、

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   一致したドキュメントの日付が指定した日付以前の場合は、日付マスクが適用されます。

以下に、単純な除外日付マスクの例を示します。

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

これは除外日付マスクなので、パターンに一致するファイルはインデックス化されず、90日以上経過しています。 ドキュメントを除外すると、テキストのインデックスは作成されず、そのファイルのリンクも表示されません。 ファイルは事実上無視されます。 この例では、ファイルとフォルダーの両方が、指定したURLパターンと一致する場合があります。 との両方がパターン `https://www.mydomain.com/docs/archive.html` に一致し `https://www.mydomain.com/docs/archive/index.html` 、90日以上経過した場合はインデックスが作成されないことに注意してください。 フォルダー内のファイルのみを一致さ `/docs/archive/` せるには、次のように、日付マスクの末尾にスラッシュを含める必要があります。

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

日付マスクはワイルドカードでも使用できます。 次の除外マスクは、2011-02-15以前のファイル拡張子「.pdf」を持つファイルを検索ロボットに見過ごすように指示します。 検索ロボットは、一致したファイルをインデックスに追加しません。

```
exclude-date 2011-02-15 *.pdf
```

「日付マスクを含める」は似ているように見え、一致したファイルのみがインデックスに追加されます。 次のインクルード日付マスクの例は、Webサイトの領域内で、生後0日前またはそれより古いファイルのテキストのインデックスを作成するよう検索ロボ `/docs/archive/manual/` ットに指示しています。

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

「マスクを含める」と「マスクを除外」は連携して機能します。 例えば、除外する日付マスクを作成し、除外するページのうち1つ以上にURLを含めるマスクを含めることで、Webサイトの大部分をインデックス作成から除外できます。 エントリポイントURLが次の場合：

```
https://www.mydomain.com/archive/
```

検索ロボットは、、、およびの下のすべてのページをクロールし、インデックスを作成します `/archive/summer/`(フォ `/archive/spring/`ルダから各フォルダに少なくとも1つのページへのリンクがあると仮定し `/archive/fall/``archive` ます)。 この動作は、リンクパスを使用して、検索ロボットが、、、およびフォルダ内のファイル、およびフォルダURLを「検索」でき、エントリポイントURLによって自動的に生成されたインクルードマスクと一致する `/summer/``/spring/``/fall/` からです。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

次のように、除外する日付マスクを含むフォルダー内の、90日 `/fall/` を超えるページをすべて除外するよう選択できます。

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

次の日付マスクを使用し `/archive/fall/index.html` て、インデックスの一部として、ファイルの古さ（0日以上前のファイルが一致した場合）のみを選択的に含めることができます。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

上記の2つのマスクの例が意図したとおりに機能するには、次のように、最初に「マスクを含める」をリストする必要があります。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

検索ロボットは指定された順序で指示に従うので、検索ロボットは最初にを含め、 `/archive/fall/index.html`次にフォルダー内の残りのファイルを除外し `/fall` ます。

手順が次とは逆の方法で指定されている場合：

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

その場 `/archive/fall/index.html` 合、マスクが含める必要があると指定していても、含められません。 最初に表示される日付マスクは、後でマスク設定に表示される日付マスクよりも常に優先されます。 また、検索ロボットが「含む日付マスク」と「除外する日付マスク」の両方に一致するページを検出した場合、最初に表示されるマスクが常に優先されます。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

## 日付マスクでのキーワードの使用について {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

各インクルードマスクを1つ以上のスペース区切りキーワードで修飾でき、一致したページのインデックスの作成方法に影響を与えます。

コンマは、マスクとキーワードの区切り文字としては無効です。スペースのみを使用できます。

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
   <td colname="col2"> <p> インクルードマスクで指定された日付以前の日付のページ上のテキストのインデックスを作成しない場合は、 
     <userinput>
       noindex 
     </userinput> を次のように日付マスクを含める： </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>上の例では、検索ロボットが10日前以前の拡張子「.swf」を持つファイルのすべてのリンクをたどるように指定しています。 ただし、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>古いファイルのテキストはインデックス付けされず、それらのファイルのリンクの後に残るようにします。 このような場合は、除外する日付マスクを使用する代わりに、「noindex」キーワードを含む日付マスクを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> インクルードマスクで指定された日付以前のページのテキストのインデックスを作成し、一致するページのリンクをたどらない場合は、 
     <userinput>
       nofollow 
     </userinput> を次のように日付マスクを含める： </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>Adobe コード内の   
     <userinput>
       nofollow 
     </userinput> キーワードは、 
     <userinput>
       content="nofollow" 
     </userinput> between 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> タグに含まれるページの名前を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用されます。 </p> <p>検索ロボットは、通常、日付マスクをチェックする前にすべてのファイルをダウンロードし、解析します。 この動作は、一部のファイルタイプではファイル自体の日付を指定できるので発生します。 例えば、HTMLドキュメントには、ファイルの日付を設定するメタタグを含めることができます。 </p> <p>日付に基づいて多数のファイルを除外し、サーバーに不要な読み込みを行わない場合は、 
     <userinput>
       server-date 
     </userinput> の後に置きます。 </p> <p>このキーワードは、各ファイルを解析する代わりに、サーバから返されたファイルの日付を信頼するように検索ロボットに指示します。 例えば、次の「日付を除外」マスクを使用すると、HTTPヘッダーでサーバーから返された日付に従って、ドキュメントが90日以上古い場合にURLに一致するページが無視されます。 </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> サーバーから返された日付が90日以上経過している場合、 
     <userinput>
       server-date 
     </userinput> 除外されたドキュメントをサーバーからダウンロードしないことを指定します。 その結果、ドキュメントのインデックス作成に要する時間が短縮され、サーバーへの負荷が軽減されます。 グループの中に「 
     <userinput>
       server-date 
     </userinput> を指定しない場合、検索ロボットはHTTPヘッダー内のサーバーから返された日付を無視します。 代わりに、各ファイルがダウンロードされ、日付が指定されているかどうかが確認されます。 ファイルに日付が指定されていない場合、検索ロボットはサーバから返された日付を使用します。 </p> <p>使用しないでください。 
     <userinput>
       server-date 
     </userinput> ファイルに、サーバーの日付を上書きするコマンドが含まれている場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 含めるマスクと除外するマスクの両方に使用します。 </p> <p>前に 
     <userinput>
       regexp 
     </userinput> は正規表現として扱われます。 </p> <p>検索ロボットは、除外正規表現の日付マスクに一致するファイルを検出した場合、それらのファイルのインデックスは作成しません。 </p> <p>検索ロボットは、「正規表現を含む」日付マスクに一致するファイルを検出した場合、それらのドキュメントのインデックスを作成します。 </p> <p>例えば、次の日付マスクがあるとします。 </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>マスクは、検索ロボットに対して、180日以上前の一致するファイルを除外するように指示します。 つまり、URLに「archive」という単語を含むファイルです。 </p> <p>正規表現を参 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分に日付マスクを追加する（インデックス部分に含めない） {#task_0010543C55F648D2B5DEFEFAD60FAF04}

日付マスクを使用すると、ファイルの年齢に基づいて顧客の検索結果にファイルを含めたり、除外したりできます。

インデックス **[!UICONTROL Test Date]** 作成後にフ **[!UICONTROL Test URL]** ァイルが含まれているかどうかをテストするには、およびの各フィールドを使用します。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**Webサイトのインデックス部分に日付マスクを追加するには、またはインデックス部分に追加しないには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Date Masks]**。
1. （オプション）ペ [!DNL Date Masks] ージのフ **[!UICONTROL Test Date]** ィールドに、YYYY-MM-DD形式の日付(例： `2011-07-25`);このフィ **[!UICONTROL Test URL]** ールドに、WebサイトのURLマスクを入力し、をクリックしま **[!UICONTROL Test]**&#x200B;す。
1. フィールド [!DNL Date Masks] に、1行に1つの日付マスクアドレスを入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## パスワードについて {#concept_3EDBD731725D46B891F834D4472774DC}

HTTP基本認証で保護されているWebサイトの一部にアクセスするには、1つ以上のパスワードを追加します。

パスワード設定の効果をユーザーに表示する前に、サイトインデックスを再構築する必要があります。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

ページで [!DNL Passwords] は、各パスワードを1行に入力します。 パスワードは、次の例のように、URLまたは領域、ユーザー名、パスワードで構成されます。

```
https://www.mydomain.com/ myname mypassword
```

上記のようにURLパスを使用する代わりに、領域を指定することもできます。

使用する領域を決定するには、パスワードで保護されたWebページをブラウザで開き、[ネットワークパスワードの入力]ダイアログボックスを表示します。

![](assets/realms.gif)

領域名は、この場合は「My Site Realm」です。

上記の領域名を使用して、パスワードは次のようになります。

```
My Site Realm myusername mypassword
```

Webサイトに複数の領域がある場合は、次の例のように、各領域のユーザー名とパスワードを別々の行に入力して、複数のパスワードを作成できます。

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

URLまたはレルムを含むパスワードを混在させて、パスワードリストを次のように表示できます。

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

上のリストでは、サーバーの認証要求に一致する領域またはURLを含む最初のパスワードが使用されます。 例えば、のファイルがにあ `https://www.mysite.com/path1/path2/index.html` る場合 `Realm3`でも、 `name2``password2` URLで定義されたパスワードが領域で定義されたパスワードの上に表示されるので、およびが使用されます。

## 認証が必要なWebサイトの領域にアクセスするためのパスワードの追加 {#task_DED19D476FF04B48BB6456D5ECB8628A}

「パスワード」を使用すると、クロールやインデックス作成の目的で、Webサイトのパスワードで保護された領域にアクセスできます。

パスワードの影響が顧客に表示される前に、サイトインデックスを必ず再構築してください

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**認証が必要なWebサイトの領域にアクセスするためのパスワードを追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Passwords]**。
1. ページの [!DNL Passwords] フィールド **[!UICONTROL Passwords]** に、領域またはURLと、それに関連するユーザー名、パスワードをスペースで区切って入力します。

   領域パスワードとURLパスワードを別々の行に記述した例：

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   1行に1つのパスワードのみを追加します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## コンテンツタイプについて {#concept_6FEA1355C0374500B4C53090C34A8A07}

を使用して、こ [!DNL Content Types] のアカウントのクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成用に選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、Adobe Flashムービー、Word、Excel、PowerPointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

顧客に対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを再構築する必要があります。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

## MP3音楽ファイルのインデックス作成について {#section_AD2E28BEEE3E46629E2B05C34A963673}

ページでこのオプションを選択 **[!UICONTROL Text in MP3 Music Files]** すると、MP3 [!DNL Content Types] ファイルがクロールされ、2つの方法のいずれかでインデックスが作成されます。 最初に、最も一般的な方法は、次のように、HTMLファイル内のアンカーhrefタグを使用する方法です。

```
<a href="MP3-file-URL"></a>
```

2つ目の方法は、MP3ファイルのURLをURL入力ポイントとして入力する方法です。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

MP3ファイルは、そのMIMEタイプ「audio/mpeg」で認識されます。

MP3ミュージックファイルのサイズは、通常は少量のテキストしか含まれていない場合でも、非常に大きくなる可能性があります。 例えば、MP3ファイルには、アルバム名、アーティスト名、曲のタイトル、曲のジャンル、リリース年、コメントなどの情報を任意で保存できます。 この情報は、ファイルの最後にTAGと呼ばれる場所に保存されます。 TAG情報を含むMP3ファイルのインデックスは、次のように作成されます。

* 曲のタイトルは、HTMLページのタイトルと同じように扱われます。
* コメントは、HTMLページに対して定義された説明と同じように扱われます。
* ジャンルは、HTMLページに対して定義されたキーワードと同じように扱われます。
* アーティスト名、アルバム名、リリース年は、HTMLページの本文と同じように扱われます。

Webサイト上でクロールおよびインデックス付けされた各MP3ファイルは、1ページとしてカウントされます。

Webサイトに大きなMP3ファイルが多数ある場合は、アカウントのインデックス作成のバイト制限を超える可能性があります。 この場合は、ページ上で選択を解 **[!UICONTROL Text in MP3 Music Files]** 除して、Webサ [!DNL Content Types] イト上のすべてのMP3ファイルのインデックスが作成されないようにすることができます。

Webサイト上の特定のMP3ファイルのインデックス作成を防ぐだけの場合は、次のいずれかの操作を行います。

* MP3ファイルにリンクするアンカータグを、タグとタグで囲 `<nofollow>``</nofollow>` みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

* MP3ファイルのURLを除外マスクとして追加します。

   URLマスクに [ついてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)い。

## クロールおよびインデックスを作成するコンテンツタイプの選択 {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

を使用して、こ [!DNL Content Types] のアカウントのクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成用に選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、Adobe Flashムービー、Word、Excel、PowerPointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

顧客に対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを再構築する必要があります。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

中国語、日本語、韓国語のMP3ファイルをクロールしてインデックスを作成するには、次の手順を実行します。 次に、// **[!UICONTROL Settings]** で、MP3 **[!UICONTROL Metadata]** ファ **[!UICONTROL Injections]**&#x200B;イルのエンコードに使用する文字セットを指定します。

About [Injectionsを参照](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)。

**クロールおよびインデックスを作成するコンテンツタイプを選択するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Content Types]**。
1. ページで、 [!DNL Content Types] Webサイト上でクロールおよびインデックスを作成するファイルの種類を確認します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## 接続について {#concept_E2F3B7E7521147479E5948A94BB3A40B}

「接続」を使用して、検索ロボットがWebサイトのインデックスを作成する際に使用するHTTP接続を10個まで追加できます。

接続数を増やすと、クロールとインデックスの完了に要する時間が大幅に短縮されます。 ただし、接続を追加するたびに、サーバーの負荷が増えることに注意してください。

## インデックス作成速度を向上させるための接続の追加 {#task_3E9B83E43C1842A19066355A15C4A6FB}

「接続」を使用すると、Webサイトのインデックス作成に要する時間を短縮できます。この場合、クローラーが使用するHTTP接続の同時数を増やすことができます。 10個までの接続を追加できます。

接続を追加するたびに、サーバーに配置される負荷が増えることに注意してください。

**インデックス作成の速度を上げるために接続を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Connections]**。
1. ページ [!DNL Parallel Indexing Connections] のフィールド **[!UICONTROL Number of Connections]** に、追加する接続数(1 ～ 10)を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## フォームの送信について {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

フォームの送信を使用すると、Webサイト上のフォームを認識し、処理できます。

Webサイトのクロール中およびインデックス作成中に、検出された各フォームが、追加したフォーム定義と比較されます。 フォームがフォーム定義と一致する場合は、インデックス作成用にフォームが送信されます。 フォームが複数の定義と一致する場合、一致する定義ごとに1回フォームが送信されます。

## Webサイト上のフォームのインデックス作成用のフォーム定義の追加 {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

を使用すると、Webサ [!DNL Form Submission] イトで認識されるフォームをインデックス作成の目的で処理できます。

変更の結果が顧客に表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**Webサイト上のフォームのインデックス作成用のフォーム定義を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Form Submission]**。
1. ページ上で、 [!DNL Form Submission] をクリックしま **[!UICONTROL Add New Form]**&#x200B;す。
1. ページで、 [!DNL Add Form Definition] とのオプションを [!DNL Form Recognition] 設定し [!DNL Form Submission] ます。

   ページのセクションの5つ [!DNL Form Recognition] のオプション [!DNL Form Definition] は、処理可能なWebページ内のフォームを識別するために使用されます。

   このセクションの3つのオ [!DNL Form Submission] プションを使用して、フォームと共にWebサーバーに送信されるパラメーターと値を指定します。

   1行に1つの認識または送信パラメータを入力します。 各パラメーターには名前と値を含める必要があります。

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
      <td colname="col2"> <p>フォームを含むWebページを識別します。 単一のページに表示されるフォームを識別するには、次の例のようにそのページのURLを入力します。 </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>複数のページに表示されるフォームを識別するには、ページの説明にワイルドカードを使用するURLマスクを指定します。 例えば、ASPページの下で検出されたフォームを <code> https://www.mydomain.com/register/ </code>識別するには、次のように指定します。 </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>正規表現を使用して複数のページを識別することもできます。 単に 
      <userinput>
        regexp 
      </userinput> キーワードをURLマスクの前に置き換えます。 </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLマスク </p> </td> 
      <td colname="col2"> <p>アクション属性を識別します。 
      <userinput>
        &lt;form&gt; 
      </userinput> 。 </p> <p>ページのURLマスクと同様に、アクションのURLマスクは、単一のURL、ワイルドカードを含むURL、または正規表現の形式をとることができます。 </p> <p>URLマスクは、次のいずれかです。 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 次のようなフルパス。 <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 次のような部分パス。 <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 以下のようにワイルドカードを使用するURL。 <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 次のような正規表現。 <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URLマスクやアクションURLマスクで識別されるページ上のテキストのインデックスを作成しない場合、またはこれらのページでリンクをたどる必要がない場合は、 
      <userinput>
        noindex 
      </userinput> および 
      <userinput>
        nofollow 
      </userinput> キーワード。 URLマスクまたはエントリポイントを使用して、これらのキーワードをマスクに追加できます。 </p> <p>URL入力ポイ <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> ントについてを参照してくだ </a>さい。 </p> <p>URLマスクにつ <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> いてを参照してくださ </a>い。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名マスク </p> </td> 
      <td colname="col2"> <p>フォームを識別します。 
      <userinput>
        &lt;form&gt; 
      </userinput> Webページ内のタグには、name属性が含まれます。 </p> <p>単純な名前( 
      <userinput>
        login_form 
      </userinput>)の場合、名前にワイルドカード( 
      <userinput>
        form* 
      </userinput>)または正規表現( 
      <userinput>
        regexp ^.*許可*$ 
      </userinput>と呼ばれていました）のリリース情報も含まれています。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにすることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォームIDマスク </p> </td> 
      <td colname="col2"> <p>フォームを識別します。 
      <userinput>
        &lt;form&gt; 
      </userinput> Webページ内のタグにはid属性が含まれます。 </p> <p>単純な名前( 
      <userinput>
        login_form 
      </userinput>)の場合、名前にワイルドカード( 
      <userinput>
        form* 
      </userinput>)または正規表現( 
      <userinput>
        regexp ^.*許可*$ 
      </userinput>と呼ばれていました）のリリース情報も含まれています。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにすることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>指定した値を含む、または含まないフォーム、または指定した値を持つ名前付きパラメーターを識別します。 </p> <p>例えば、rick_brough@mydomain.comに事前設定されているが、first-nameパラメーターではないパスワードパラメーターを含む電子メールパラメーターを含むフォームを識別するには、次のパラメーター設定を1行に1つずつ指定します。 </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>フォーム送信</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLを上書き </p> </td> 
      <td colname="col2"> <p>フォーム送信のターゲットが、フォームのアクション属性で指定されたターゲットと異なる場合に指定します。 </p> <p>例えば、フォーム内のURL値とは異なるURL値を構成するJavaScript関数を使用してフォームが送信される場合に、このオプションを使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Overrideメソッド </p> </td> 
      <td colname="col2"> <p>フォーム送信のターゲットがフォームのアクション属性で使用されているものと異なる場合、およびJavaScriptの送信でメソッドが変更された場合に指定します。 </p> <p>すべてのフォームパラメーターのデフォルト値( 
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
      </userinput> タグ)は、Webページから読み取られます。 ただし、「フォーム送信」セクションの「パラメ <span class="wintitle"> ータ」フィー </span> ルドに表示されるすべてのパ <span class="uicontrol"> ラメ </span> ータは、フォームのデフォルトに置き換えられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>フォーム送信パラメーターの先頭に 
      <userinput>
        は 
      </userinput> keyword. </p> <p>パラメーターのプレフィックスを 
      <userinput>
        は 
      </userinput>の場合、フォームの送信の一部として送信されません。 この動作は、送信する必要のあるチェックボックスの選択を解除する場合に役立ちます。 </p> <p>例えば、次のパラメーターを送信するとします。 </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 値を含む電子メールパラメータ 
      <userinput>
        nobody@mydomain.com 
      </userinput> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 値を持つパスワードパラメーター 
      <userinput>
        タイム 
      </userinput> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckboxパラメーターの選択を解除した状態。 </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>その他すべて 
      <userinput>
        &lt;form&gt; 
      </userinput> パラメータのデフォルト値 </p> </li> 
      </ul> </p> <p>フォーム送信パラメータは次のようになります。 </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>メソッド属性( 
      <userinput>
        &lt;form&gt; 
      </userinput> タグを使用して、GETメソッドまたはPOSTメソッドを使用してデータをサーバーに送信するかどうかを決定します。 </p> <p>    
      <userinput>
        &lt;form&gt; 
      </userinput> タグにmethod属性が含まれていない場合、フォームはGETメソッドを使用して送信されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## フォーム定義の編集 {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Webサイト上のフォームが変更された場合や、定義を変更する必要がある場合は、既存のフォーム定義を編集できます。

ページには、フォーム定義 [!DNL History] に対して行っ [!DNL Form Submission] た変更を元に戻す機能はありません。

変更の結果が顧客に表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**フォーム定義を編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Form Submission]**。
1. ページ [!DNL Form Submission] 上で、更新 **[!UICONTROL Edit]** するフォーム定義の右側のをクリックします。
1. ページで、 [!DNL Edit Form Definition] とのオプションを [!DNL Form Recognition] 設定し [!DNL Form Submission] ます。

   Webサイト上のフォームのインデックス作成に [使用するフォーム定義の追加のオプションの表を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## フォーム定義の削除 {#task_C350FC0CDE344F2786215D544C048B5E}

Webサイトにフォームが存在しなくなった場合、または特定のフォームを処理してインデックスを作成する必要がなくなった場合は、既存のフォーム定義を削除できます。

ページには、フォーム定義 [!DNL History] に対して行っ [!DNL Form Submission] た変更を元に戻す機能はありません。

変更の結果が顧客に表示されるように、サイトインデックスを必ず再構築してください。

詳しくは、ス [テージングされたWebサイトの増分インデックスの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)い。

**フォーム定義を削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Form Submission]**。
1. ページ [!DNL Form Submission] 上で、削 **[!UICONTROL Delete]** 除するフォーム定義の右側をクリックします。

   削除するフォーム定義が正しいことを確認してください。 次の手順でをクリックしても、削除の確認ダイアログボ **[!UICONTROL Delete]** ックスは表示されません。
1. ページ上で、 [!DNL Delete Form Definition] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## インデックスコネクタについて {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

XMLペー [!DNL Index Connector] ジやフィードのインデックス作成用の追加の入力ソースを定義する場合に使用します。

データフィード入力ソースを使用すると、使用可能なクロール方法の1つを使用して、Webサイトで一般に見つかるものとは異なるフォームに保存されたコンテンツにアクセスできます。 クロールおよびインデックス付けされた各ドキュメントは、Webサイト上のコンテンツページに直接対応します。 ただし、データフィードはXMLドキュメントか、コンマまたはタブ区切りのテキストファイルから取得され、インデックスを作成するコンテンツ情報が含まれています。

XMLデータソースは、個々のドキュメントに対応する情報を含むXMLスタンザ（レコード）で構成されます。 これらの個々のドキュメントがインデックスに追加されます。 テキストデータフィードには、個々のドキュメントに対応する個々の新しい行区切りのレコードが含まれています。 これらの個々のドキュメントもインデックスに追加されます。 どちらの場合も、インデックスコネクタの設定は、フィードの解釈方法を示します。 各設定は、ファイルの保存場所と、サーバーがファイルにアクセスする方法を示します。 この設定では、「マッピング」情報も説明します。 つまり、各レコードの項目を使用して、結果のインデックスにメタデータフィールドを入力する方法です。

ページにインデックスコネクタ定義を追加し [!DNL Staged Index Connector Definitions] た後、「名前」または「種類」の値を除く *設定を* 、任意に変更できます。

このペ [!DNL Index Connector] ージには、次の情報が表示されます。

* 設定および追加した定義済みのインデックスコネクタの名前。
* 追加した各コネクタに対して、次のいずれかのデータソースタイプを指定します。

   * **テキスト** — 単純な「フラット」ファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。
   * **フィード** - XMLフィード
   * **XML** - XMLドキュメントのコレクション。

* 次回のクロールとインデックス作成のためにコネクタが有効になっているかどうか。
* データソースのアドレス。

Index Connectorについ [ても参照してください](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## インデックスコネクタのテキスト設定とフィード設定でのインデックス作成プロセスの仕組み {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、単純なファイルのダウンロードです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p>テキ <span class="uicontrol"> スト </span>の場合、改行で区切られた各行のテキストは個々のドキュメントに対応し、コンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p>フィー <span class="uicontrol"> ド </span>の場合、各ドキュメントのデータは次の形式の正規表現パターンを使用して抽出されます。 </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>[インデッ <span class="uicontrol"> クスコネク </span> タの追加]ページの <span class="wintitle"></span> [マップ]を使用して、データのキャッシュされたコピーを作成し、クローラのリンクの一覧を作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが入力されます。 </p> <p>解析されたデータがローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラーが必要とする単純なHTMLドキュメントを作成します。 例： </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>&lt;title&gt; <span class="codeph"> 要素は、タ </span> イトルメタデータフィールドにマッピングが存在する場合にのみ生成されます。 同様に、 <span class="codeph"> &lt;body&gt;要素は、Body </span> メタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義されたURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについて <span class="codeph"> は、元のドキ </span> ュメント内のデータを含む各フィールドに対して&lt;meta&gt;タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれる各ドキュメントに対して、次の例のようにリンクも生成されます。 </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングには、主キーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取り込まれる際に使用されるキーを形成します。 </p> <p>クローラはURLインデックスを認 <span class="codeph"> 識します。スキーム </span> のプレフィックス。ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p>インデッ <span class="codeph"> クス：リン </span> クは、クローラーの保留リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、そのドキュメントのデータがキャッシュから取得されます。 次に、HTML画像を「アセンブル」して処理し、インデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## インデックスコネクタのXML設定でのインデックス作成プロセスの仕組み {#section_7F1551EA51854C5C99F284CE260526EB}

XML設定のインデックス作成プロセスは、テキストおよびフィード設定のプロセスに似ていますが、以下の小さな変更と例外があります。

XMLクロールのドキュメントは既に個別のファイルに分けられているので、上記の表の手順1と2は直接適用されません。 ページのとフィールドにURLを指 **[!UICONTROL Host Address]** 定する **[!UICONTROL File Path]** と、通常のHTMLドキ [!DNL Index Connector Add] ュメントとしてダウンロードされ、処理されます。 ダウンロードドキュメントには、処理されるXMLドキュメントを指すリ `<a href="{url}"...` ンクのコレクションが含まれていることが期待されます。 このようなリンクは次の形式に変換されます。

```
<a href="index:<ic_config_name>?url="{url}">
```

例えば、アドビの設定から次のリンクが返されたとします。

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

上の表では、手順3は適用されず、クロールおよびインデックス作成時に手順4が完了しています。

または、XMLドキュメントを、クロールプロセスで自然に見つかった他のドキュメントと混在させることができます。 このような場合は、書き換えルール( > **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]****[!UICONTROL Crawl List Retrieve URL Rules]**)を使用して、XMLドキュメントのURLを変更し、Index Connectorに送信することができます。

「クロール [リストのURL取得の規則」を参照してくださ](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)い。

例えば、次の書き換えルールがあるとします。

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

このルールは、で終わるすべてのURLをインデッ `.xml` クスコネクタリンクに変換します。 クローラは `index:` URLスキームを認識し、書き換えます。 ダウンロードプロセスは、マスター上のIndex Connector Apacheサーバーを通じてリダイレクトされます。 ダウンロードされた各ドキュメントは、フィードで使用されるのと同じ正規表現パターンを使用して調べられます。 ただし、この場合、製造されたHTMLドキュメントはキャッシュに保存されません。 代わりに、インデックス処理のためにクローラーに直接渡されます。

## 複数のインデックスコネクタを設定する方法 {#section_C2B14C0F06354A57AEF6238FF3814E5D}

任意のアカウントに対して複数のインデックスコネクタの設定を定義できます。 次の図に示すように、設定は、 > >のドロップダ **[!UICONTROL Settings]** ウンリ **[!UICONTROL Crawl]** ストに **[!UICONTROL URL Entrypoints]** 自動的に追加されます。

![](assets/url_entrypoints_index_connector.png)

ドロップダウンリストから設定を選択すると、URLエントリポイントのリストの最後に値が追加されます。

>[!NOTE]
>
>無効なインデックスコネクタの設定はドロップダウンリストに追加されますが、選択することはできません。 同じインデックスコネクタの設定を2回目に選択した場合、その設定はリストの最後に追加され、前のインスタンスが削除されます。

増分クロールのインデックスコネクタエントリポイントを指定するには、次の形式を使用してエントリを追加します。

```
index:<indexconnector_configuration_name>
```

[インデックスコネクタ]ページで追加された各エントリが見つかり、有効になっている場合は、クローラがそのエントリを処理します。

注意：各ドキュメントのURLはインデックスコネクタの設定名とドキュメントの主キーを使用して構築されるので、増分更新を実行する際は、必ず同じインデックスコネクタの設定名を使用してください。 これにより、以前にインデックス [!DNL Adobe Search&Promote] 付けされたドキュメントを正しく更新できます。

URL入力ポイントにつ [いても参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

**インデックスコネクタの追加時のセットアップマップの使用**

インデックスコネクタを追加する際に、オプションでこの機能を使用して、デー **[!UICONTROL Setup Maps]** タソースのサンプルをダウンロードできます。 データはインデックスの適合性を調べられます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>インデックスコネクタの種類を選択した場合 </p> </th> 
   <th colname="col2" class="entry"> <p>マップを設定機能 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>テキスト </p> </td> 
   <td colname="col2"> <p>最初にタブを試し、次に縦棒( <span class="codeph"> | </span>)と最後のコンマ( <span class="codeph"> , </span>)。 「マップの設定」をクリックする前に区切り値を既に指 <span class="uicontrol"> 定してい </span>る場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なタグとフィールドの値に推測が入力されます。 さらに、解析されたデータのサンプリングが表示されます。 ファイルにヘッダー行が含ま <span class="uicontrol"> れていることがわか </span> っている場合は、必ず「最初の行のヘッダー」を選択してください。 この情報を使用して、結果のマップエントリをより適切に識別します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子は、Mapテーブルのタグ行に表示され、同様の値がFieldsに表示されます。 これらの行は使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータを説明し、Itemtagの値を識別するので、この機能は役に立ちます。 </p> <p> <p>注意： マップの設定機能は、分析を実行するためにXMLソース全体をダウンロードします。 ファイルのサイズが大きい場合は、この操作がタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は、使用が望ましくないXPath項目をすべて識別します。 必ず、結果のMap定義を確認し、不要または不要なMap定義を削除してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>マスターリンクリストではなく、個々の代表的なドキュメントのURLをダウンロードします。 この1つのドキュメントは、フィードで使用されるのと同じメカニズムを使用して解析され、結果が表示されます。 </p> <p>「追加」をク <span class="uicontrol"> リック </span> して設定を保存する前に、URLをマスターリンクリストドキュメントに戻す必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**重要**:ファイルパーサーがファイル全体をメモリに読み込もうとするので、マップの設定機能は大きなXMLデータセットに対しては動作しない場合があります。 その結果、メモリ不足状態が発生する可能性があります。 ただし、インデックス作成時に同じドキュメントが処理された場合、そのドキュメントはメモリに読み込まれません。 その代わり、大きなドキュメントは「外出先で」処理され、最初にメモリに読み込まれることはありません。

**インデックスコネクタの追加時のプレビューの使用**

インデックスコネクタを追加する際に、保存したかのように、オプションでこ **[!UICONTROL Preview]** の機能を使用してデータを検証することができます。 設定に対するテストを実行しますが、設定をアカウントに保存しません。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラが使用するメインキャッシュフォルダと競合しません。

「プレビュー」は、Acct:IndexConnector-Preview-Max-Documentsで制御される5つのドキュメントのデフォルトのみを処理します。 プレビューされたドキュメントは、インデックス作成クローラに表示されるとおり、ソース形式で表示されます。 この表示は、Webブラウザの「ソースの表示」機能に似ています。 プレビューセット内のドキュメントは、標準のナビゲーションリンクを使用して移動できます。

プレビューはXML設定をサポートしません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## インデックスコネクタ定義の追加 {#task_96779B651A654E1F871F55D6DBBC8886}

各Index Connector設定は、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

新しい有効な定義の効果が顧客に表示される前に、サイトインデックスを再構築します。

**インデックスコネクタ定義を追加するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページ上で、 [!DNL Stage Index Connector Definitions] をクリックしま **[!UICONTROL Add New Index Connector]**&#x200B;す。
1. ページで、 [!DNL Index Connector Add] 必要なコネクタオプションを設定します。 使用できるオプションは、選択したオプションに **[!UICONTROL Type]** よって異なります。

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
      <td colname="col2"> <p>インデックスコネクタ設定の一意の名前。 英数字を使用できます。 「_」と「 — 」も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択したデータソースタイプは、インデックスコネクタの追加ページで使用できる結果のオプ <span class="wintitle"> ションに影響を与 </span> えます。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行で区切られた各テキスト行は、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）を、1から始まる列番号で参照されるメタデータフィールドにマップできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むマスターXMLドキュメントをダウンロードします。 </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>リンク( 
      <userinput>
        &lt;a&gt; 
      </userinput>)を個々のXMLドキュメントに置き換えます。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定がエントリポイントリストに見つかった場合、それらは無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p> または </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>このURIは、「Host Address」、「File Path」、「Protocol」、および「Username」、「Password」の各フィールドの適切なエントリに分類されます。 </p> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incremental File Path </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>このファイルを指定した場合、Incremental Index操作中にダウンロードされ、処理されます。 ファイルが指定されていない場合は、代わりに「ファイルパス」の下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>縦のファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新時に使用する単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式のファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>指定した場合、このファイルは、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスの削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>このファイルを指定した場合、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、プライマリ・キーとして指定された列のFullまたはIncremental File Pathファイルの値に対応している必要が <span class="uicontrol"> ありま </span>す。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、HTTPサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTP、またはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で指定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、またはHTTPS接続の再試行の最大回数を指定します。 この値は0 ～ 10の範囲で指定する必要があります。 </p> <p>値が0の場合、再試行は行われません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の各フィールドの区切り文字を指定します。 </p> <p>コンマ文字( <span class="codeph"> , </span>)は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るフィールド区切り文字として機能します。 </p> <p>タブを選 <span class="uicontrol"> 択しますか？ </span> をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭行のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>インデックス作成用の最小ドキュメント数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス操作でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1(1)にして、列番号を指定します。 各列に新しいマップ行を追加するには、「アクション」の「 <span class="wintitle"> +」 </span>をクリック <span class="uicontrol"> しま </span>す。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップするように選択できます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p>フィールド <span class="uicontrol"> が </span> コンボボックスになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応 <span class="uicontrol"> じて、 </span> Field値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、フィルタリングスクリプトで使用するコンテンツの作成に役立 <span class="wintitle"> つ場合があり </span>ます。 </p> <p>スクリプトのフ <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> ィルタリングについてを参照してく </a>ださい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、結果のキャッシュされたドキュメントで、複数の値が1つの値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field値が定義済み </span> のメタデータフィールドであるとします。 また、このフィールドには「リストを許可」属 <span class="wintitle"> 性が設定さ </span> れています。 この場合、フィールドのList Delimiters値（最初に定義された区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、この文書を索引に追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p>主キ <span class="uicontrol"> ー値は、 </span> インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が見つかった場合は無視されます。 元のドキュメントに主キーとして使用する一意の値が1つだけ含まれていないが、複数のフィールドを組み合わせて一意の識別子を作成できる場合 <span class="uicontrol"> 、複数の列の値を縦棒 </span><i></i><span class="uicontrol"></span><span class="uicontrol"></span> (|)で区切って、主キーを定義できます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグが削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：フィード</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定がエントリポイントリストに見つかった場合、それらは無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含むマスターXMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incremental File Path </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含む増分XMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>このファイルを指定した場合、Incremental Index操作中にダウンロードされ、処理されます。 ファイルが指定されていない場合は、代わりに「ファイルパス」の下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>縦のファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新時に使用する複数の疎な「行」の情報を含むXMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>指定した場合、このファイルは、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスの削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> <p>このファイルを指定した場合、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、プライマリ・キーとして指定された列のFullまたはIncremental File Pathファイルの値に対応している必要が <span class="uicontrol"> ありま </span>す。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、HTTPサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、次のAdobe XMLドキュメントのフィードフラグメントでは、Itemタグの値はレコード <span class="codeph"> です </span>。 </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>正の値に設定した場合、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス操作でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobe XMLドキュメントを使用して、オプションItemtagの下で、次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>レコード <span class="codeph"> 要素のdisplayurl属 </span> 性は、メタデ <span class="codeph"> ータ </span> フィールドのpage-url <span class="codeph"> にマップされま </span>す。 </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素のコンテンツ、 </span><span class="codeph"> メタ要素内に含まれるレコード要素、名前メタデータ要素内に含まれるメタ要素、メタデータ要素内に含まれるメタデータ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素、メタデータ要素内にマップされるレコード要素。 </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素の内容、レコード要素内に含まれるレコード要素、名前メタデータ </span> 属性内に含まれるレコード要素、メタデータフィールド <span class="codeph"> 内にマップされるメタ要素 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>の内容。 </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素 </span> の内容、レコード要素内に含まれる <span class="codeph"></span> メタ要素内の内容、メタデータ要素内のメタデータ要素内のメタデータ <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素内のメタデータ要素とメタデータ要素本体との対応付けを行う。 </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p>https://www.w3schools.com/xpath/を参照して <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> ください </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性 <span class="codeph"> 値を定義し </span> ます。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p>フィールド <span class="uicontrol"> が </span> コンボボックスになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応 <span class="uicontrol"> じて、 </span> Field値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、フィルタリングスクリプトで使用するコンテンツの作成に役立 <span class="wintitle"> つ場合があり </span>ます。 </p> <p>スクリプトのフ <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> ィルタリングについてを参照してく </a>ださい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、結果のキャッシュされたドキュメントで、複数の値が1つの値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field値が定義済み </span> のメタデータフィールドであるとします。 また、このフィールドには「リストを許可」属 <span class="wintitle"> 性が設定さ </span> れています。 この場合、フィールドのList Delimiters値（最初に定義された区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、この文書を索引に追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p>主キ <span class="uicontrol"> ー値は、 </span> インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が見つかった場合は無視されます。 元の文書に主キーとして使用する一意の値が1つも含まれていない場合でも、複数のフィールドを組み合わせて一意の識別子を作成できる場合は <span class="uicontrol"> 、複数の </span>Tagを縦棒 <i></i><span class="uicontrol"></span><span class="uicontrol"></span> (|)で区切って、主キーを定義できます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグが削除されます。 </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 削除に使用しますか？ </span> <p>Incremental Index操作中のみ使用されます。 このXPathパターンに一致するレコードは、削除する項目を識別します。 このよ <span class="uicontrol"> うな各レ </span> コードのプライマリキー値は、Delete File Pathと同様に、「削除」リクエストの作成に使用されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。 お使いの機能を有効にするには、テクニカルサポートにお問い合わせください。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定がエントリポイントリストに見つかった場合、それらは無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>リンク( 
      <userinput>
        &lt;a&gt; 
      </userinput>)を個々のXMLドキュメントに置き換えます。 </p> <p>パスは、ホストアドレスのルートを基準とした相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次のいずれかを選択できます。 </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>必要に応じて、HTTPサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための適切な認証資格情報を入力できます。 </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> File </li> 
      </ul> </p> <p> <b>注意</b>:「プロトコル」設定は、「ホストアドレス」または「ファイルパス」フィールドに情報が指定されている場合にのみ使用されます。 個々のXMLドキュメントは、URLの指定に従って、HTTPまたはHTTPSを使用してダウンロードされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の「行」を定義するXML要素を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobe XMLドキュメントのItemtagオプションの下で、次の構文を使用してドキュメントをマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>レコード <span class="codeph"> 要素のdisplayurl属 </span> 性は、メタデ <span class="codeph"> ータ </span> フィールドのpage-url <span class="codeph"> にマップされま </span>す。 </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素のコンテンツ、 </span><span class="codeph"> メタ要素内に含まれるレコード要素、名前メタデータ要素内に含まれるメタ要素、メタデータ要素内に含まれるメタデータ </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素、メタデータ要素内にマップされるレコード要素。 </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素の内容、レコード要素内に含まれるレコード要素、名前メタデータ </span> 属性内に含まれるレコード要素、メタデータフィールド <span class="codeph"> 内にマップされるメタ要素 </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>の内容。 </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>メタ <span class="codeph"> 要素内に含まれるメタ要素 </span> の内容、レコード要素内に含まれる <span class="codeph"></span> メタ要素内の内容、メタデータ要素内のメタデータ要素内のメタデータ <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>要素内のメタデータ要素とメタデータ要素本体との対応付けを行う。 </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p>https://www.w3schools.com/xpath/を参照して <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> ください </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> メタデータ? </span> <p>フィールド <span class="uicontrol"> が </span> コンボボックスになり、現在のアカウントに対して定義済みのメタデータフィールドを選択できます。 </p> <p>必要に応 <span class="uicontrol"> じて、 </span> Field値に未定義のメタデータフィールドを設定できます。 未定義のメタデータフィールドは、フィルタリングスクリプトで使用するコンテンツの作成に役立 <span class="wintitle"> つ場合があり </span>ます。 </p> <p>スクリプトのフ <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> ィルタリングについてを参照してく </a>ださい。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、結果のキャッシュされたドキュメントで、複数の値が1つの値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する <span class="wintitle"> Field値が定義済み </span> のメタデータフィールドであるとします。 また、このフィールドには「リストを許可」属 <span class="wintitle"> 性が設定さ </span> れています。 この場合、フィールドのList Delimiters値（最初に定義された区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、この文書を索引に追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p>主キ <span class="uicontrol"> ー値は、 </span> インデックスコネクタの設定で表されるすべてのドキュメントで一意である必要があります。重複が見つかった場合は無視されます。 元の文書に主キーとして使用する一意の値が1つも含まれていない場合でも、複数のフィールドを組み合わせて一意の識別子を作成できる場合は <span class="uicontrol"> 、複数の </span>Tagを縦棒 <i></i><span class="uicontrol"></span><span class="uicontrol"></span> (|)で区切って、主キーを定義できます。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTMLを削除しますか？ </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグが削除されます。 </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）をクリック **[!UICONTROL Setup Maps]** して、データソースのサンプルをダウンロードします。 データはインデックスの適合性を調べられます。 この機能は、テキストとフィードのタイプでのみ使用できます。
1. （オプション）をクリ **[!UICONTROL Preview]** ックして、設定の実際の動作をテストします。 この機能は、テキストとフィードのタイプでのみ使用できます。
1. をクリ **[!UICONTROL Add]** ックして、設定をペ [!DNL Index Connector Definitions] ージおよびページ上のド [!DNL Index Connector Configurations] ロップダウンリストに追加し [!DNL URL Entrypoints] ます。

   URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。
1. ページ上で、 [!DNL Index Connector Definitions] をクリックしま **[!UICONTROL rebuild your staged site index]**&#x200B;す。
1. （オプション）ページで、 [!DNL Index Connector Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## インデックスコネクタ定義の編集 {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

定義した既存のインデックスコネクタを編集できます。

>[!NOTE]
>
>コンボボックスの「インデックスコネクタ名」や「タイプ」など、変更できないオプションが [!DNL Type] あるとは限りません。

**インデックスコネクタの定義を編集するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページの [!DNL Index Connector] 列見出しの下 [!DNL Actions] で、設定を変更 **[!UICONTROL Edit]** するインデックスコネクタ定義名をクリックします。
1. ページで、 [!DNL Index Connector Edit] 必要なオプションを設定します。

   インデックスコネクタ定義の追加のオ [プションの表を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）ページで、 [!DNL Index Connector Definitions] をクリックしま **[!UICONTROL rebuild your staged site index]**&#x200B;す。
1. （オプション）ページで、 [!DNL Index Connector Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## インデックスコネクタ定義の設定の表示 {#task_D0B71A7426E54247BDB3468EC576D871}

既存のインデックスコネクタ定義の設定を確認できます。

ページにインデックスコネクタ定義を追加した後 [!DNL Index Connector Definitions] は、その種類の設定を変更することはできません。 代わりに、定義を削除し、新しい定義を追加する必要があります。

**インデックスコネクタ定義の設定を表示するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページの [!DNL Index Connector] 列見出しの下 [!DNL Actions] で、設定を確認ま **[!UICONTROL Edit]** たは編集するインデックスコネクタ定義名をクリックします。

## インデックスコネクタ定義のコピー {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

既存のインデックスコネクタ定義をコピーして、作成する新しいインデックスコネクタの基本として使用できます。

インデックスコネクタ定義をコピーする場合、コピーされた定義はデフォルトで無効になっています。 定義を有効または「有効にする」には、ページから編集し、を選択 [!DNL Index Connector Edit] する必要がありま **[!UICONTROL Enable]**&#x200B;す。

詳しくは、イ [ンデックスコネクタ定義の編集を参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)い。

**インデックスコネクタの定義をコピーするには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページの [!DNL Index Connector] 列見出しの下 [!DNL Actions] で、設定を複製す **[!UICONTROL Copy]** るインデックスコネクタ定義名をクリックします。
1. ページ [!DNL Index Connector Copy] で、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）ページで、 [!DNL Index Connector Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## インデックスコネクタ定義の名前の変更 {#task_5132118FC21B47D99881E0ED425225D7}

既存のインデックスコネクタ定義の名前を変更できます。

定義の名前を変更したら、//を **[!UICONTROL Settings]** チェック **[!UICONTROL Crawling]** しま **[!UICONTROL URL Entrypoints]**&#x200B;す。 新しい定義名がページのドロップダウンリストに反映されることを確認し [!DNL URL Entrypoints] ます。

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

**インデックスコネクタ定義の名前を変更するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページの [!DNL Index Connector] 列見出しの下 [!DNL Actions] で、変更するインデ **[!UICONTROL Rename]** ックスコネクタ定義名をクリックします。
1. ページ [!DNL Index Connector Rename] で、フィールドに定義の新しい名前を入力し [!DNL Name] ます。
1. クリック **[!UICONTROL Rename]**.
1. Click **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. 以前のインデックスコネクタの名前がリストに存在する場合は、その名前を削除し、新しく名前を変更したエントリを追加します。

   詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。 1.（オプション）ページで、 [!DNL Index Connector Definitions] 次のいずれかの操作を行います。

   * 変更を **[!UICONTROL History]** 元に戻すには、をクリックします。

      詳しくは、「 [履歴」オプションの使用を参照してくださ](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)い。

   * クリック **[!UICONTROL Live]**.

      ライブ設 [定の表示を参照してください](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)。

   * クリック **[!UICONTROL Push Live]**.

      詳しくは、ス [テージ設定をライブにプッシュするを参照してくださ](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)い。

## インデックスコネクタ定義の削除 {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

不要になった既存のインデックスコネクタ定義を削除したり、使用したりできます。

**インデックスコネクタ定義を削除するには**

1. 製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL Index Connector]**。
1. ページの [!DNL Index Connector Definitions] 列見出しの下 [!DNL Actions] で、削除するインデ **[!UICONTROL Delete]** ックスコネクタ定義名をクリックします。
1. ページ上で、 [!DNL Index Connector Delete] をクリックしま **[!UICONTROL Delete]**&#x200B;す。
