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
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '11033'
ht-degree: 1%

---


# クロールメニューについて{#about-the-crawling-menu}

クロールメニューの設定日、URLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URL入力ポイントを使用します。

## URL入力ポイントについて{#concept_5D857E3B5C124E85BC0B5AE77A509573}

ほとんどのWebサイトには、顧客が最初に訪問する主なエントリーポイント(ホームページ)が1つあります。 このメインエントリポイントは、検索ロボットがインデックスのクロールを開始する際のURLアドレスです。 ただし、Webサイトに複数のドメインまたはサブドメインがある場合、またはサイトの一部がプライマリエントリポイントからリンクされていない場合は、「URL入力ポイント」を使用してエントリポイントを追加できます。

指定した各URLエントリポイントより下のWebサイトページには、すべてインデックスが作成されます。 URLエントリポイントとマスクを組み合わせて、Webサイトのどの部分にインデックスを付けるかを厳密に制御できます。 URL入力ポイント設定の効果がユーザーに表示されるようにするには、Webサイトのインデックスを再構築する必要があります。

メインエントリポイントは、通常、インデックスを作成して検索するWebサイトのURLです。 このメインエントリポイントは、「アカウントの設定」で設定します。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

メインURLエントリポイントを指定した後、必要に応じて、クロールする追加のエントリポイントを順番に指定できます。 多くの場合、メインエントリポイントの下のページからリンクされていないWebページに対して、追加のエントリポイントを指定します。 次の例のように、Webサイトが複数のドメインにまたがる場合は、追加のエントリポイントを指定します。

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

各エントリポイントを次の表に示す、1つ以上のスペースで区切られたキーワードで修飾します。 これらのキーワードは、ページのインデックス作成方法に影響を与えます。

**重要**:特定のキーワードをエントリポイントから、およびスペースで相互に区切るようにしてください。コンマは有効な区切り文字ではありません。

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
     <code>
       noindex 
     </code>を入力ポイントの後に挿入します。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>このキーワードは、 
     <code>
       content="noindex" 
     </code>)を 
     <code>
       &lt;head&gt; 
     </code>... 
     エントリポイントページの<code>
       &lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成する際に、そのページのリンクをたどる必要がない場合は、 
     <code>
       nofollow 
     </code>を入力ポイントの後に挿入します。 </p> <p>次の例のように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>このキーワードは、 
     <code>
       content="nofollow" 
     </code> 
     <code>
       &lt;head&gt; 
     </code>... 
     エントリポイントページの<code>
       &lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>form </p> </td> 
   <td colname="col2"> <p> エントリポイントがログインページの場合、 
     <code>
       form 
     </code>は、通常、検索ロボットがログインフォームを送信し、適切なcookieを受け取った後でWebサイトをクロールできるようにするために使用されます。 「form」キーワードを使用する場合、エントリポイントページのインデックスは作成されず、検索ロボットはエントリポイントページをクロール済みとしてマークしません。 使用する 
     <code>
       nofollow 
     </code>を返します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「[コンテンツタイプについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)」も参照してください。

[インデックスコネクタについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)も参照してください。

## インデックスを作成する複数のURLエントリポイントの追加{#task_2338A47387D74CFDAC4D4EF4A367ED45}

Webサイトに複数のドメインまたはサブドメインがあり、それらをクロールする場合は、URL入力ポイントを使用してURLを追加できます。

WebサイトのメインURLエントリポイントを設定するには、「アカウントの設定」を使用します。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

**インデックスを作成する複数のURLエントリポイントを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。
1. [!DNL URL Entrypoints]ページの[!DNL Entrypoints]フィールドに、1行に1つのURLアドレスを入力します。
1. （オプション）**[!UICONTROL Add Index Connector Configurations]**&#x200B;ドロップダウンリストで、インデックス作成のエントリポイントとして追加するインデックスコネクタを選択します。

   このドロップダウンリストは、1つ以上のインデックスコネクタ定義を以前に追加した場合にのみ使用できます。

   ![](assets/url_entrypoints_index_connector.png)

   「[インデックスコネクタ定義の追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)」を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## URLマスクについて{#concept_8039DFC53FF3410AA494D602F71BA164}

URLマスクは、検索ロボットがインデックスを付けたかインデックスを付けなかったかをWebサイトのドキュメントで判断するパターンです。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

使用できるURLマスクは次の2種類です。

* URLマスクを含める
* URLマスクの除外

URLマスクを含めると、検索ロボットはマスクのパターンに一致するドキュメントをインデックス付けするように指示されます。

URLマスクを除外すると、検索ロボットは一致するドキュメントのインデックスを作成するように指示します。

検索ロボットは、リンクからWebサイト内のリンクに移動する際、URLに遭遇し、それらのURLに一致するマスクを探します。 最初の一致によって、そのURLをインデックスに含めるか、除外するかが決まります。 検出されたURLに一致するマスクがない場合、そのURLはインデックスから破棄されます。

エントリポイントURLに対するURLマスクを含めるは、URLが自動的に生成されます。 この動作により、Webサイトで遭遇するすべてのドキュメントのインデックスが作成されます。 また、ウェブサイトから「離脱」するリンクが便利になくなります。 例えば、インデックス付きのページがhttps://www.yahoo.comにリンクしている場合、検索ロボットはそのURLのインデックスを作成しません。これは、エントリポイントURLによって自動的に生成されるインクルードマスクと一致しないためです。

指定する各URLマスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* `https://www.mydomain.com/products.html`のようなフルパス。
* `https://www.mydomain.com/products`のような部分的なパス。
* `https://www.mydomain.com/*.html`のようにワイルドカードを使用するURL。
* 正規式（上級ユーザー用）

   マスクを正規式にするには、マスクタイプ（`exclude`または`include`）とURLマスクの間にキーワード`regexp`を挿入します。

以下に、単純な除外URLマスクの例を示します。

```
exclude https://www.mydomain.com/photos
```

この例は除外URLマスクなので、パターンに一致するドキュメントのインデックスは作成されません。 このパターンは、検出されたアイテム（ファイルとフォルダーの両方）と一致するので、`https://www.mydomain.com/photos.html`と`https://www.mydomain.com/photos/index.html`（両方とも除外URLと一致）のインデックスは作成されません。 `/photos/`フォルダー内のファイルのみを一致させるには、次の例のように、URLマスクの末尾にスラッシュを含める必要があります。

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

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

マスクを含めると、マスクを除外すると機能します。 「URLを除外」マスクを作成し、「URLを含む」マスクを使用して除外されたページを1つ以上含めることで、Webサイトの大部分をインデックス作成から除外できます。 例えば、エントリポイントURLが次のような場合、

```
https://www.mydomain.com/photos/
```

検索ロボットは、`/photos/summer/`、`/photos/spring/`、`/photos/fall/`の下のすべてのページをクロールしてインデックス化します（`photos`フォルダーから各ディレクトリに少なくとも1ページへのリンクがあると仮定）。 この動作は、リンクパスによって、検索ロボットが`/summer/`、`/spring/`、`/fall/`内のドキュメントを見つけ、フォルダーとフォルダーURLが、エントリポイントURLによって自動的に生成されるインクルードマスクと一致するために発生します。

次の例のように、`/fall/`フォルダー内の除外URLマスクを含むすべてのページを除外するように選択できます。

```
exclude https://www.mydomain.com/photos/fall/
```

または、次のURLマスクを使用して、インデックスの一部として選択的に`/photos/fall/redleaves4.html`のみを含めます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

上記の2つのマスクの例が意図したとおりに機能するため、次のように、「include mask」が最初に表示されます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

検索ロボットは指定された順番に従うので、最初に`/photos/fall/redleaves4.html`を含み、次に`/fall`フォルダー内の残りのファイルを除外します。

手順が次のとおり逆の方法で指定されている場合：

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

その場合、マスクが含めるように指定しても、`/photos/fall/redleaves4.html`は含められません。

最初に表示されるURLマスクは、マスク設定の後で表示されるURLマスクよりも常に優先されます。 また、検索ロボットが「URLを含む」マスクと「URLを除外」マスクに一致するページを検出した場合は、最初に表示されるマスクが常に優先されます。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

## URLマスクを使用したキーワードの使用について{#section_7609A7A6D79B482ABCA8900886541AAB}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致したページのインデックス作成に影響を与えます。

マスクとキーワードの区切り文字としてコンマは無効です。スペースのみを使用できます。

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
     <code>
       noindex 
     </code>をインクルードURLマスクの後に挿入します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>上記の例では、検索ロボットが 
     <code>
       .swf 
     </code>拡張子を持ちますが、これらのファイルに含まれるすべてのテキストのインデックス作成を無効にします。 </p> <p>Folio Builder 
     <code>
       noindex 
     </code>キーワードは、 
     <code>
       content="noindex" 
     </code> ～ 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> URLマスクと一致するページのテキストにインデックスを付けるが、一致するページのリンクに従わない場合は、 
     <code>
       nofollow 
     </code>をインクルードURLマスクの後に挿入します。 次の例のように、キーワードとマスクは必ずスペースで区切ってください。 </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Folio Builder 
     <code>
       nofollow 
     </code>キーワードは、 
     <code>
       content="nofollow" 
     </code> ～ 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用します。 </p> <p>先頭に 
     <code>
       regexp 
     </code>は正規式として扱われます。 検索ロボットが除外正規式URLマスクに一致するドキュメントを検出した場合、それらのドキュメントのインデックスは作成されません。 検索ロボットが「含む正規式のURLマスク」に一致するドキュメントを検出すると、それらのドキュメントのインデックスが作成されます。 例えば、次のURLマスクがあるとします。 </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>検索ロボットは、 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>次の除外正規式URLマスクがある場合： </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>検索ロボットは、 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>正規式URLマスクを含む次の場合： </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>検索ロボットは、「.swf」拡張子を持つファイルからのすべてのリンクに従います。 Folio Builder 
     <code>
       noindex 
     </code>キーワードは、一致したファイルのテキストのインデックスが作成されないことを示します。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分へのURLマスクの追加（インデックス部分の追加）{#task_E1AFC17C746048B8843013D979E082C1}

[!DNL URL Masks]を使用して、Webサイトのどの部分をクロールしてインデックスを作成するか、または作成しないかを定義できます。

「URLマスクをテスト」フィールドを使用して、インデックス作成後にドキュメントが含まれているかどうかをテストします。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**Webサイトのインデックス部分にURLマスクを追加するか、インデックス部分に追加しないかを指定するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Masks]**&#x200B;をクリックします。
1. （オプション）[!DNL URL Masks]ページの&#x200B;**[!UICONTROL Test URL Masks]**&#x200B;フィールドに、WebサイトのテストURLマスクを入力し、**[!UICONTROL Test]**&#x200B;をクリックします。
1. [!DNL URL Masks]フィールドに`include`と入力するか（クロールしてインデックスを作成するWebサイトを追加する場合）、`exclude`と入力し（Webサイトのクロールおよびインデックスの作成をブロックする場合）、URLマスクアドレスを入力します。

   1行につき1つのURLマスクアドレスを入力します。 例：

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 日付マスクについて{#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

日付マスクを使用すると、ファイルの年齢に基づいて検索結果にファイルを含めたり、除外したりできます。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

使用できる日付マスクは次の2種類です。

* 日付マスクを含める（「include-days」と「include-date」）

   指定した日付以前の日付付けマスクインデックスファイルを含めます。
* 日付マスクを除外（「exclude-days」と「exclude-date」）

   指定した日付以前の日付の付いた日付マスクインデックスファイルを除外します。

デフォルトでは、ファイルの日付はメタタグ情報から決定されます。 Metaタグが見つからない場合は、検索ロボットがファイルをダウンロードした際にサーバから受け取ったHTTPヘッダからファイルの日付が決定されます。

指定する各日付マスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* `https://www.mydomain.com/products.html`のような完全なパス
* `https://www.mydomain.com/products`のような部分的なパス
* ワイルドカードを使用するURL `https://www.mydomain.com/*.html`
* 正規式。 マスクを正規式にするには、URLの前にキーワード`regexp`を挿入します。

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

これは除外日付マスクなので、パターンと一致するファイルはインデックス化されず、90日以上経過しています。 ドキュメントを除外すると、テキストのインデックスは作成されず、そのファイルからのリンクも追跡されません。 ファイルは事実上無視されます。 この例では、ファイルとフォルダーの両方が、指定したURLパターンと一致する場合があります。 `https://www.mydomain.com/docs/archive.html`と`https://www.mydomain.com/docs/archive/index.html`の両方がパターンと一致し、90日以上前の場合はインデックス化されません。 `/docs/archive/`フォルダー内のファイルのみを一致させるには、日付マスクの末尾に次のようなスラッシュを含める必要があります。

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

日付マスクはワイルドカードでも使用できます。 次の除外マスクは、2011-02-15以前の拡張子「.pdf」を持つファイルを検索ロボットに見過ごすよう指示します。 検索ロボットは、一致するファイルをインデックスに追加しません。

```
exclude-date 2011-02-15 *.pdf
```

「インクルード」の日付マスクの外観は似ていますが、一致したファイルのみがインデックスに追加されます。 次のインクルード日付マスクの例は、Webサイトの`/docs/archive/manual/`領域にある古いファイル（0日以上）のテキストのインデックスを作成するよう検索ロボットに指示します。

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

マスクを含めると、マスクを除外すると機能します。 例えば、除外日付マスクを作成し、除外するページのうち1つ以上をURLマスクを含むページに含めることで、Webサイトの大部分をインデックス作成から除外できます。 エントリポイントURLが次の場合：

```
https://www.mydomain.com/archive/
```

検索ロボットは、`/archive/summer/`、`/archive/spring/`、`/archive/fall/`の下のすべてのページをクロールしてインデックスを作成します（`archive`フォルダーから各フォルダーに少なくとも1ページへのリンクがあると仮定）。 この動作は、リンクパスによって、検索ロボットが`/summer/`、`/spring/`、`/fall/`の各フォルダー内のファイルを「見つけ」、フォルダーURLが入力ポイントURLによって自動的に生成されたインクルードマスクと一致するために発生します。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

`/fall/`フォルダー内の90日以上経過したページをすべて除外し、次のように日付マスクを除外します。

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

`/archive/fall/index.html`のみ（古いファイルとは関係なく、0日以上前のファイルはすべて一致）を、次の日付マスクを使用してインデックスの一部として選択的に含めることができます。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

上記の2つのマスクの例を意図したとおりに機能させるには、まず次のように「マスクを含める」をリストする必要があります。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

検索ロボットは指定された順序に従うので、検索ロボットはまず`/archive/fall/index.html`を含み、次に`/fall`フォルダー内の残りのファイルを除外します。

手順が次のとおり逆の方法で指定されている場合：

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

その場合、マスクが指定する必要があるとしても、`/archive/fall/index.html`は含まれません。 最初に表示される日付マスクは、マスク設定の後で表示される日付マスクよりも常に優先されます。 また、検索ロボットが「日付を含む」マスクと「日付を除外する」マスクの両方に一致するページを検出した場合は、最初に表示されるマスクが常に優先されます。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

## 日付マスクを使用したキーワードの使用について{#section_CCBB3E3FDBDE4725B2B571FD6594470C}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致したページのインデックス作成に影響を与えます。

マスクとキーワードの区切り文字としてコンマは無効です。スペースのみを使用できます。

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
     <code>
       noindex 
     </code>は、次のように日付マスクを含める： </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>上記の例では、10日以上前の「.swf」拡張子を持つファイルのリンクは、すべて検索ロボットに従うように指定しています。 ただし、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>古いファイルのテキストは、インデックスが作成されていないが、それらのファイルのすべてのリンクをたどるようにしてください。 このような場合は、除外日付マスクを使用する代わりに、「noindex」キーワードを含む日付マスクを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> インデックスマスクで指定された日付以前のページのテキストの日付をインデックス化する場合、一致したページのリンクに従わないようにするには、 
     <code>
       nofollow 
     </code>は、次のように日付マスクを含める： </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>Folio Builder 
     <code>
       nofollow 
     </code>キーワードは、 
     <code>
       content="nofollow" 
     </code> ～ 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>含めるマスクと除外するマスクの両方に使用します。 </p> <p>検索ロボットは通常、日付マスクをチェックする前にすべてのファイルをダウンロードして解析します。 この動作は、一部のファイルタイプではファイル自体に日付を指定できるためです。 例えば、HTMLドキュメントには、ファイルの日付を設定するメタタグを含めることができます。 </p> <p>日付に基づいて多数のファイルを除外し、不要な読み込みをサーバーに行いたくない場合は、 
     <code>
       server-date 
     </code>を日付マスクのURLの後に挿入します。 </p> <p>このキーワードは、各ファイルを解析する代わりに、サーバから返されたファイルの日付を信頼するように検索ロボットに指示します。 例えば、次の除外日付マスクでは、ドキュメントが90日以上前の場合、HTTPヘッダー内のサーバーから返された日付に従って、URLに一致するページが無視されます。 </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> サーバーから返される日付が90日以上前の場合、 
     <code>
       server-date 
     </code>は、除外されたドキュメントをサーバーからダウンロードしないことを指定します。 その結果、ドキュメントのインデックス作成に要する時間が短縮され、サーバへの負荷が軽減されます。 If 
     <code>
       server-date 
     </code>が指定されていない場合、検索ロボットはHTTPヘッダ内のサーバから返される日付を無視します。 代わりに、各ファイルがダウンロードされ、日付が指定されているかどうかを確認します。 ファイルに日付が指定されていない場合、検索ロボットはサーバから返された日付を使用します。 </p> <p>次を使用しないでください。 
     <code>
       server-date 
     </code>を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 含めるマスクと除外するマスクの両方に使用します。 </p> <p>前に 
     <code>
       regexp 
     </code>は正規式として扱われます。 </p> <p>検索ロボットは、除外正規式の日付マスクに一致するファイルを検出した場合、それらのファイルのインデックス付けを行いません。 </p> <p>検索ロボットは、「含む」正規式の日付マスクに一致するファイルを検出すると、それらのドキュメントのインデックスを作成します。 </p> <p>例えば、次の日付マスクがあるとします。 </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>マスクは、180日以上前の一致するファイルを検索ロボットに除外するように指示します。 つまり、URLに「archive」という語を含むファイルです。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規式</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分に日付マスクを追加する、またはWebサイトのインデックス部分に追加しない{#task_0010543C55F648D2B5DEFEFAD60FAF04}

日付マスクを使用すると、ファイルの保存期間に基づいて顧客の検索結果にファイルを含めたり、除外したりできます。

**[!UICONTROL Test Date]**&#x200B;フィールドと&#x200B;**[!UICONTROL Test URL]**&#x200B;フィールドを使用して、インデックス作成後にファイルが含まれているかどうかをテストします。

URLマスクの結果がユーザーに表示されるように、サイトインデックスを再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**Webサイトのインデックス部分に日付マスクを追加するには、またはインデックス部分に追加しないには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Date Masks]**&#x200B;をクリックします。
1. （オプション）[!DNL Date Masks]ページの&#x200B;**[!UICONTROL Test Date]**&#x200B;フィールドに、YYYY-MM-DD形式の日付を入力します（例：`2011-07-25`）。「**[!UICONTROL Test URL]**」フィールドに、webサイトのURLマスクを入力し、「**[!UICONTROL Test]**」をクリックします。
1. [!DNL Date Masks]フィールドに、1行に1つの日付マスクアドレスを入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## パスワードについて{#concept_3EDBD731725D46B891F834D4472774DC}

WebサイトのHTTP基本認証で保護されている部分にアクセスするには、1つ以上のパスワードを追加します。

パスワード設定の効果がユーザーに表示される前に、サイトインデックスを作成し直す必要があります。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

[!DNL Passwords]ページで、1行に各パスワードを入力します。 パスワードは、次の例のように、URLまたは領域、ユーザー名、パスワードで構成されます。

```
https://www.mydomain.com/ myname mypassword
```

上のようなURLパスを使用する代わりに、領域を指定することもできます。

使用する正しい領域を決定するには、パスワードで保護されたWebページをブラウザーで開き、「Enter Network Password」ダイアログ・ボックスを確認します。

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

上記のリストでは、サーバーの認証要求と一致する領域またはURLを含む最初のパスワードが使用されます。 `https://www.mysite.com/path1/path2/index.html`のファイルが`Realm3`にある場合でも、例えば`name2`や`password2`は、URLで定義されるパスワードが領域で定義されるパスワードの上に表示されるので使用されます。

## Webサイトの認証が必要な領域にアクセスするためのパスワードの追加{#task_DED19D476FF04B48BB6456D5ECB8628A}

「パスワード」を使用すると、クロールやインデックス作成の目的で、Webサイトのパスワードで保護された領域にアクセスできます。

パスワードの影響がユーザーに表示される前に、サイトインデックスを必ず作成し直してください

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**Webサイトの認証が必要な領域にアクセスするためのパスワードを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Passwords]**&#x200B;をクリックします。
1. [!DNL Passwords]ページの&#x200B;**[!UICONTROL Passwords]**&#x200B;フィールドに、領域またはURLと、それに関連するユーザー名、パスワードをスペースで区切って入力します。

   領域パスワードとURLパスワードを別々の行に示す例：

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   1行に1つのパスワードのみを追加します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## コンテンツタイプについて{#concept_6FEA1355C0374500B4C53090C34A8A07}

[!DNL Content Types]を使用して、このアカウントのクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、AdobeFlashムービー、Word、Excel、PowerpointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

ユーザーに対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを作成し直す必要があります。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

## MP3音楽ファイルのインデックス付けについて{#section_AD2E28BEEE3E46629E2B05C34A963673}

[!DNL Content Types]ページで&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;オプションを選択した場合、MP3ファイルは、2つの方法のいずれかでクロールされ、インデックスが作成されます。 最初に、最も一般的な方法は、次のように、HTMLファイル内のアンカーhrefタグを使用する方法です。

```
<a href="MP3-file-URL"></a>
```

2つ目の方法は、MP3ファイルのURLをURL入力ポイントとして入力する方法です。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

MP3ファイルは、そのMIMEタイプ「audio/mpeg」で認識されます。

MP3ミュージックファイルは、通常、少量のテキストしか含まない場合でも、非常に大きなサイズになる可能性があることに注意してください。 例えば、MP3ファイルには、アルバム名、アーティスト名、曲のタイトル、曲のジャンル、リリース年度、コメントなどを任意で保存できます。 この情報は、ファイルの最後（TAGと呼ばれる場所）に保存されます。 TAG情報を含むMP3ファイルのインデックスは、次のように作成されます。

* 曲のタイトルは、HTMLページのタイトルのように扱われます。
* コメントは、HTMLページに対して定義された説明と同様に扱われます。
* ジャンルは、HTMLページに対して定義されたキーワードと同様に扱われます。
* アーティスト名、アルバム名およびリリース年は、HTMLページの本文と同様に扱われます。

Webサイト上でクロールおよびインデックスが作成された各MP3ファイルは、1ページとしてカウントされます。

Webサイトに大きなMP3ファイルが多数ある場合は、アカウントのインデックス付けバイト制限を超える可能性があります。 この場合は、[!DNL Content Types]ページの&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;の選択を解除して、Webサイト上のすべてのMP3ファイルがインデックス付けされないようにすることができます。

Webサイト上の特定のMP3ファイルのインデックス作成を禁止する必要がある場合は、次のいずれかを実行できます。

* MP3ファイルにリンクするアンカータグを`<nofollow>`タグと`</nofollow>`タグで囲みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

* 除外マ追加スクとしてのMP3ファイルのURLです。

   [URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

## クロールするコンテンツタイプとインデックス{#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}を選択

[!DNL Content Types]を使用して、このアカウントのクロールおよびインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、AdobeFlashムービー、Word、Excel、PowerpointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストは、Webサイト上の他のすべてのテキストと共に検索されます。

ユーザーに対してコンテンツタイプ設定の効果が表示される前に、サイトインデックスを作成し直す必要があります。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

中国語、日本語または韓国語のMP3ファイルをクロールしてインデックスを作成するには、次の手順を実行します。 次に、**[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;で、MP3ファイルのエンコードに使用する文字セットを指定します。

[インジェクションについて](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)を参照してください。

**クロールおよびインデックスを作成するコンテンツタイプを選択するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Content Types]**&#x200B;をクリックします。
1. [!DNL Content Types]ページで、Webサイト上のクロールおよびインデックスを作成するファイルタイプを確認します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 接続について{#concept_E2F3B7E7521147479E5948A94BB3A40B}

「接続」を使用すると、検索ロボットがWebサイトのインデックス作成に使用するHTTP接続を10個まで追加できます。

接続数を増やすと、クロールとインデックスの完了に要する時間が大幅に短縮されます。 ただし、接続を追加するたびに、サーバーの負荷が増えることに注意してください。

## インデックス作成速度を上げるための接続の追加{#task_3E9B83E43C1842A19066355A15C4A6FB}

「接続」を使用すると、Webサイトのインデックス作成に要する時間を短縮できます。クローラーで使用するHTTP接続の同時数を増やすことができます。 10個までの接続を追加できます。

接続が追加されるたびに、サーバーに負荷がかかることに注意してください。

**接続を追加してインデックス作成速度を上げるには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Connections]**&#x200B;をクリックします。
1. [!DNL Parallel Indexing Connections]ページの&#x200B;**[!UICONTROL Number of Connections]**&#x200B;フィールドに、追加する接続数(1 ～ 10)を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォーム送信について{#concept_CADD5D7CF373497DAA6F8564D7BC8502}

フォームの送信を使用すると、Webサイト上のフォームを認識して処理するのに役立ちます。

Webサイトのクロールおよびインデックス作成中に、検出された各フォームが、追加したフォーム定義と比較されます。 フォームがフォーム定義と一致する場合は、インデックス作成のためにフォームが送信されます。 フォームが複数の定義と一致する場合は、一致する定義ごとに1回フォームが送信されます。

## Webサイト上のフォームのインデックス作成用のフォーム定義の追加{#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

[!DNL Form Submission]を使用すると、Webサイトで認識されるフォームを処理してインデックスを作成できます。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**Webサイト上のフォームのインデックス作成用のフォーム定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、**[!UICONTROL Add New Form]**&#x200B;をクリックします。
1. [!DNL Add Form Definition]ページで、[!DNL Form Recognition]と[!DNL Form Submission]のオプションを設定します。

   [!DNL Form Definition]ページの[!DNL Form Recognition]セクションにある5つのオプションは、処理可能なWebページ内のフォームを識別するために使用されます。

   [!DNL Form Submission]セクションの3つのオプションは、フォームと共にWebサーバーに送信されるパラメーターと値を指定するために使用されます。

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
      <td colname="col2"> <p>フォームを含むWebページを識別します。 単一のページに表示されるフォームを識別するには、次の例のようにそのページのURLを入力します。 </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>複数のページに表示されるフォームを識別するには、ページの説明にワイルドカードを使用するURLマスクを指定します。 例えば、<code> https://www.mydomain.com/register/ </code>の下にあるASPページで発生したフォームを識別するには、次のように指定します。 </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>また、正規式を使用して複数のページを識別することもできます。 単に 
      次の例のように、URLマスクの前の<code>
        regexp 
      </code>キーワード： </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLマスク </p> </td> 
      <td colname="col2"> <p>Folio Builderの 
      <code>
        &lt;form&gt; 
      </code>タグ。 </p> <p>ページのURLマスクと同様に、アクションのURLマスクは、単一のURL、ワイルドカードを含むURLまたは正規式の形式にすることができます。 </p> <p>URLマスクは、次のいずれかになります。 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 次のようなフルパス。<code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 次のような部分的なパスです。<code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 以下のようなワイルドカードを使用するURL。<code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 次のような正規式。<code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URLマスクまたはアクションURLマスクで識別されるページのテキストのインデックスを作成しない場合、またはこれらのページにリンクを追跡したくない場合、 
      <code>
        noindex 
      </code>と 
      <code>
        nofollow 
      </code>キーワード。 URLマスクまたは入力ポイントを使用して、これらのキーワードをマスクに追加できます。 </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> URL入力ポイントについて</a>を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URLマスクについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名マスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      webページの<code>
        &lt;form&gt; 
      </code>タグにname属性が含まれています。 </p> <p>単純な名前( 
      <code>
        login_form 
      </code>)、ワイルドカード( 
      <code>
        form* 
      </code>)または正規式( 
      <code>
        regexp ^.*authorize.*$ 
      </code>)。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにしておくことができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォームIDマスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      webページの<code>
        &lt;form&gt; 
      </code>タグにid属性が含まれています。 </p> <p>単純な名前( 
      <code>
        login_form 
      </code>)、ワイルドカード( 
      <code>
        form* 
      </code>)または正規式( 
      <code>
        regexp ^.*authorize.*$ 
      </code>)。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにしておくことができます。 </p> </td> 
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
      <code>
        &lt;input&gt; 
      </code>タグ（非表示フィールドを含む）、デフォルト 
      <code>
        &lt;option&gt; 
      </code> 
      <code>
        &lt;select&gt; 
      </code>タグと、 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code>タグ)は、Webページから読み取られます。 ただし、<span class="wintitle">フォーム送信</span>セクションの<span class="uicontrol">パラメーター</span>フィールドに指定されているパラメーターは、すべてデフォルトのフォームに置き換えられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>フォーム送信パラメーターに 
      <code>
        not 
      </code>キーワード。 </p> <p>パラメーターのプレフィックスに 
      <code>
        not 
      </code>の場合、フォーム送信の一部として送信されません。 この動作は、送信する必要があるチェックボックスの選択を解除した場合に役立ちます。 </p> <p>例えば、次のパラメーターを送信するとします。 </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 値を含む電子メールパラメーター 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 値を持つパスワードパラメーター 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckboxパラメーターの選択が解除されている。 </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>その他 
      <code>
        &lt;form&gt; 
      </code>パラメーターをデフォルト値として </p> </li> 
      </ul> </p> <p>フォーム送信パラメーターは次のようになります。 </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>メソッドの属性 
      Webページの<code>
        &lt;form&gt; 
      </code>タグは、GET方式またはPOST方式を使用して、データをサーバーに送信するかどうかを決定するために使用されます。 </p> <p>Folio Builder 
      <code>
        &lt;form&gt; 
      </code>タグにmethod属性が含まれていない場合、フォームはGETメソッドを使用して送信されます。 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. クリック **[!UICONTROL Add]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォーム定義の編集{#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Webサイト上のフォームが変更された場合や、定義を変更する必要が生じた場合は、既存のフォーム定義を編集できます。

[!DNL Form Submission]ページには、フォーム定義に対して行った変更を元に戻す[!DNL History]機能がないことに注意してください。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**フォーム定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、更新するフォーム定義の右側の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Form Definition]ページで、[!DNL Form Recognition]と[!DNL Form Submission]のオプションを設定します。

   [Webサイト](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F)でのフォームのインデックス作成に使用するフォーム定義の追加のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォーム定義の削除{#task_C350FC0CDE344F2786215D544C048B5E}

Webサイトにフォームが存在しなくなった場合や、特定のフォームを処理してインデックスを作成したくない場合は、既存のフォーム定義を削除できます。

[!DNL Form Submission]ページには、フォーム定義に対して行った変更を元に戻す[!DNL History]機能がないことに注意してください。

変更の結果がユーザーに表示されるように、サイトインデックスを必ず再構築してください。

「[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)」を参照してください。

**フォーム定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、削除するフォーム定義の右側の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。

   削除するフォーム定義が正しいことを確認してください。 次の手順で&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックした場合、削除の確認ダイアログボックスは表示されません。
1. [!DNL Delete Form Definition]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタについて{#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

XMLページや任意のフィードのインデックス作成に使用する追加の入力ソースを定義するには、[!DNL Index Connector]を使用します。

データフィード入力ソースを使用すると、Webサイトで一般に見つかるものとは異なるフォームに保存されたコンテンツに、利用可能なクロール方法の1つを使用してアクセスできます。 クロールおよびインデックス付けされた各ドキュメントは、Webサイト上のコンテンツページに直接対応しています。 ただし、データフィードはXMLドキュメントから、またはカンマ区切りまたはタブ区切りのテキストファイルから取得され、インデックスを作成するコンテンツ情報が含まれます。

XMLデータソースは、個々のドキュメントに対応する情報を含むXMLスタンザス（レコード）で構成されます。 これらの個々のドキュメントはインデックスに追加されます。 テキストデータフィードには、個々のドキュメントに対応する個々の改行区切りレコードが含まれています。 これらの個々のドキュメントもインデックスに追加されます。 どちらの場合も、インデックスコネクタ設定は、フィードの解釈方法を説明します。 各設定では、ファイルの保存場所と、サーバーがファイルにアクセスする方法が説明されます。 この設定では、「マッピング」情報も説明します。 つまり、各レコードの項目を使用して、結果のインデックスにメタデータフィールドを埋め込む方法です。

[!DNL Staged Index Connector Definitions]ページにインデックスコネクタ定義を追加した後、「名前」または「種類」の値に&#x200B;*以外の*&#x200B;の設定を変更できます。

[!DNL Index Connector]ページには次の情報が表示されます。

* 設定および追加した、定義済みのインデックスコネクタの名前。
* 追加した各コネクタに対して、次のいずれかのデータソースの種類を指定します。

   * **テキスト** ：単純な「フラット」ファイル、カンマ区切り、タブ区切りなどの一貫した区切り形式。
   * **フィード** - XMLフィード
   * **XML**  - XMLドキュメントのコレクションです。

* 次回のクロールとインデックス作成に対してコネクタが有効かどうかを示します。
* データソースのアドレス。

[インデックスコネクタについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)も参照してください

## インデックスコネクタのテキスト設定とフィード設定でのインデックス作成プロセスの動作{#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p><span class="uicontrol">テキスト</span>の場合、改行で区切られた各テキスト行は、個々のドキュメントに対応し、カンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p><span class="uicontrol">フィード</span>では、各ドキュメントのデータは次の形式の正規式パターンを使用して抽出されます。 </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle">インデックスコネクタ</span>ページの<span class="uicontrol">マップ</span>を使用して、データのキャッシュコピーを作成し、クローラーのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが入力されます。 </p> <p>解析済みデータがローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラが必要とする単純なHTMLドキュメントが作成されます。 例： </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span>要素は、タイトルメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 同様に、<span class="codeph"> &lt;body&gt; </span>要素は、Bodyメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義済みのURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについては、元のドキュメントで見つかったデータを持つ各フィールドに対して、<span class="codeph"> &lt;meta&gt; </span>タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれるドキュメントごとに、次の例のようなリンクも生成されます。 </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングには、プライマリキーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取得される際に使用されるキーを形成します。 </p> <p>クローラはURL <span class="codeph">インデックスを認識します。</span>スキームプレフィックス。これにより、ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p><span class="codeph">インデックス：</span>リンクは、クローラの保留リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、ドキュメントのデータがキャッシュから取得されます。 その後、HTML画像を「アセンブル」し、処理してインデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## インデックスコネクタのXML設定でのインデックス作成プロセスの動作{#section_7F1551EA51854C5C99F284CE260526EB}

XML設定のインデックス作成プロセスは、テキスト設定とフィード設定のプロセスと似ていますが、以下の小さな変更と例外があります。

XMLクロールのドキュメントは既に個別のファイルに分けられているので、上記の表の手順1と2は直接適用されません。 [!DNL Index Connector Add]ページの&#x200B;**[!UICONTROL Host Address]**&#x200B;フィールドと&#x200B;**[!UICONTROL File Path]**&#x200B;フィールドにURLを指定すると、URLがダウンロードされ、通常のHTMLドキュメントとして処理されます。 ダウンロードドキュメントには`<a href="{url}"...`リンクのコレクションが含まれ、それぞれが処理されるXMLドキュメントを指すことを期待します。 そのようなリンクは次の形式に変換されます。

```
<a href="index:<ic_config_name>?url="{url}">
```

例えば、Adobeの設定から次のリンクが返されたとします。

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

上の表では、手順3は適用されず、クロールおよびインデックス作成時に手順4が完了します。

または、XMLドキュメントを、クロールプロセスによって自然に発見された他のドキュメントと混在させることもできます。 このような場合は、書き換えルール(**[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**)を使用して、XMLドキュメントのURLを変更し、インデックスコネクタに転送することができます。

[クロールリストの取得URLルールについて](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)を参照してください。

例えば、次の書き換えルールがあるとします。

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

このルールは、`.xml`で終わるURLをインデックスコネクタリンクに変換します。 クローラは`index:` URLスキームを認識して書き換えます。 ダウンロードプロセスは、プライマリ上のIndex Connector Apacheサーバーを通じてリダイレクトされます。 ダウンロードされた各ドキュメントは、フィードで使用されるのと同じ正規式パターンを使用して調べられます。 ただし、この場合、製造されたHTMLドキュメントはキャッシュに保存されません。 代わりに、インデックス処理用にクローラに直接渡されます。

## 複数のインデックスコネクタの設定方法{#section_C2B14C0F06354A57AEF6238FF3814E5D}

任意のアカウントに対して複数のインデックスコネクタ設定を定義できます。 次の図に示すように、設定は&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]**&#x200B;のドロップダウンリストに自動的に追加されます。

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

注意：各ドキュメントのURLはインデックスコネクタ設定名とドキュメントの主キーを使用して構築されるので、増分更新を実行する際は、必ず同じインデックスコネクタ設定名を使用してください。 これにより、[!DNL Adobe Search&Promote]は、以前にインデックス付けされたドキュメントを正しく更新できます。

[URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)も参照してください。

**インデックスコネクタを追加する際のセットアップマップの使用**

インデックスコネクタを追加する際に、オプションで&#x200B;**[!UICONTROL Setup Maps]**&#x200B;機能を使用して、データソースのサンプルをダウンロードできます。 データは、インデックスの適合性を調べられます。

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
   <td colname="col2"> <p>最初にタブを試し、次に縦棒(<span class="codeph">)を試して区切り値を決定します。 | </span>)を挿入し、最後にカンマ( <span class="codeph"> , </span>)を挿入します。 「<span class="uicontrol">マップの設定</span>」をクリックする前に、既に区切り値を指定している場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なタグとフィールドの値に推測値が入力されます。 さらに、解析済みデータのサンプリングも表示されます。 ファイルにヘッダー行が含まれていることがわかっている場合は、必ず「<span class="uicontrol">先頭行</span>のヘッダー」を選択してください。 この情報は、設定関数で結果のマップエントリを識別しやすくするために使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子はMapテーブルのタグ行に表示され、同様の値はFieldsにも表示されます。 これらの行は使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータの説明とItemtagの値の識別を行うので、この方法は役に立ちます。 </p> <p> <p>注意： セットアップマップ機能は、XMLソース全体をダウンロードして分析を実行します。 ファイルのサイズが大きい場合は、この操作がタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は可能なすべてのXPath項目を識別しますが、その多くは使用が望ましくない項目です。 結果のMap定義を確認し、不要または不要なMap定義を削除してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>プライマリリンクリストではなく、個々のドキュメントを代表するユーザーのURLをダウンロードします。 この単一のドキュメントは、フィードで使用されるのと同じメカニズムを使用して解析され、結果が表示されます。 </p> <p><span class="uicontrol"> 追加 </span>をクリックして設定を保存する前に、URLをプライマリリンクリストドキュメントに戻してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**重要**:サイズの大きいXMLデータセットでは、ファイルパーサーがファイル全体をメモリに読み込もうとするので、セットアップマップ機能が動作しない場合があります。その結果、メモリ不足状態が発生する可能性があります。 ただし、インデックス作成時に同じドキュメントが処理された場合、メモリへの読み込みは行われません。 その代わりに、大きなドキュメントは「外出中」に処理され、最初にメモリに完全に読み込まれるわけではありません。

**インデックスコネクタを追加する際のプレビューの使用**

インデックスコネクタを追加する際、オプションで&#x200B;**[!UICONTROL Preview]**&#x200B;機能を使用して、データを保存しているかのようにデータを検証できます。 設定をアカウントに保存せずに、設定に対するテストを実行します。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラが使用するメインキャッシュフォルダと競合しません。

プレビューは、 Acct:IndexConnector-プレビュー-Max-ドキュメントで制御される5つのドキュメントのデフォルトのみを処理します。 プレビューしたドキュメントは、インデックス作成クローラに表示されるとおり、ソース形式で表示されます。 表示は、Webブラウザーの「表示ソース」機能に似ています。 標準のナビゲーションリンクを使用して、プレビューセット内のドキュメントを移動できます。

プレビューはXML設定をサポートしません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## インデックスコネクタ定義の追加{#task_96779B651A654E1F871F55D6DBBC8886}

各インデックスコネクタの設定は、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

新しい有効な定義の効果がユーザーに表示される前に、サイトインデックスを作成し直します。

**インデックスコネクタ定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Stage Index Connector Definitions]ページで、**[!UICONTROL Add New Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector Add]ページで、必要なコネクタオプションを設定します。 使用できるオプションは、選択した&#x200B;**[!UICONTROL Type]**&#x200B;によって異なります。

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
      <td colname="col2"> <p>データのソース。 選択したデータソースタイプは、<span class="wintitle">インデックスコネクタ追加</span>ページで使用できる結果のオプションに影響します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行で区切られた各行のテキストは、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）を、1から始まる列番号で参照されるメタデータフィールドにマップできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むプライマリXMLドキュメントをダウンロードします。 </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>リンク( 
      <code>
        &lt;a&gt; 
      </code>)を個々のXMLドキュメントに送信します。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
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
      <td colname="col2"> <p>垂直更新時に使用する単純なフラットテキストファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、FullまたはIncremental File Pathファイル(<span class="uicontrol">プライマリキー</span>として指定された列)にある値に対応している必要があります。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスすることができます。 </p> </li> 
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
      <td colname="col2"> <p>指定したデータソースファイルの各フィールドの説明文字として使用する文字を指定します。 </p> <p>カンマ文字(<span class="codeph">、</span>)は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るのに役立つフィールド区切り文字として機能します。 </p> <p><span class="uicontrol">タブを選択しますか？ </span> をクリックします。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>先頭行のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>インデックス作成用の最小ドキュメント数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス処理でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1にして、列番号を指定します。 各列に新しいマップ行を追加するには、「<span class="wintitle">アクション</span>」の下の「<span class="uicontrol"> + </span>」をクリックします。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップすることもできます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>が、現在のアカウントに対して定義済みのメタデータフィールドを選択できるドロップダウンリストになります。 </p> <p>必要に応じて、<span class="uicontrol">フィールド</span>の値は、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、<span class="wintitle">フィルタースクリプト</span>で使用されるコンテンツの作成に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプトについて</a>を参照してください。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つだけ含まれていないが、2つ以上のフィールドを組み合わせて<i>一意の識別子を形成できる場合は、複数の<span class="uicontrol">列</span>の値を縦区切り("|")で定義できますの値。</span></i><span class="uicontrol"> </span></p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：フィード</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
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
      <td colname="col2"> <p>垂直更新時に使用する複数の疎な「行」ドキュメントを含むXML情報へのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、「垂直方向の更新」の操作中にダウンロードされ、処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子の値を含む、単純なフラットテキストファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、Incremental Index操作中にダウンロードされ、処理されます。 このファイル内の値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、FullまたはIncremental File Pathファイル(<span class="uicontrol">プライマリキー</span>として指定された列)にある値に対応している必要があります。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスすることができます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> ファイル </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、AdobeXMLドキュメントの次のフィードフラグメントでは、Itemtagの値は<span class="codeph">レコード</span>です。 </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードされるファイルに必要なレコードの最小数を指定します。 受け取るレコードが少ない場合、インデックス処理は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス処理でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータとのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析済みXMLデータのXPath表現を指定します。 上記のAdobeXMLドキュメントの例を使用して、Itemtagオプションの下で、次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>に対応付けられます。 </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内に含まれる）。<span class="codeph">タイトル</span>は、メタデータフィールド<span class="codeph">タイトル&lt;a11に対応します/&gt;。</span> </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内）（name属性は<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph"> desc1に対応します/&gt;。</span> </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">レコード</span>要素内の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本体&lt;a11にマッピングされます。/&gt;。<span class="codeph"></span></span> </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a>を参照 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各<span class="codeph"> &lt;meta&gt; </span>タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>が、現在のアカウントに対して定義済みのメタデータフィールドを選択できるドロップダウンリストになります。 </p> <p>必要に応じて、<span class="uicontrol">フィールド</span>の値は、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、<span class="wintitle">フィルタースクリプト</span>で使用されるコンテンツの作成に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプトについて</a>を参照してください。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つだけ含まれていない場合でも、<i>2つ以上のフィールドを組み合わせて</i>一意の識別子を形成できる場合は、複数の<span class="uicontrol">タグ</span>を縦区切り文字("|")の値。</span><span class="uicontrol"> </span></p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 削除に使用しますか？  </span> <p>Incremental Index操作でのみ使用されます。 このXPathパターンに一致するレコードは、削除対象の項目を識別します。 これらの各レコードの<span class="uicontrol">プライマリキー</span>値は、Delete File Pathと同様に、「削除」リクエストの作成に使用されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能をアクティブにするには、テクニカルサポートにお問い合わせください。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行うには、設定を「オン」にします。 または、構成を「オフ」にして、クロールやインデックス作成を防ぐことができます。 </p> <p> <b>注意</b>:無効なインデックスコネクタの設定は、エントリポイントリストに見つかった場合は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>File Path </p> </td> 
      <td colname="col2"> <p>リンク( 
      <code>
        &lt;a&gt; 
      </code>)を個々のXMLドキュメントに送信します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスすることができます。 </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>必要に応じて、HTTPSサーバーにアクセスするための正しい認証資格情報を入力できます。 </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> ファイル </li> 
      </ul> </p> <p> <b>注意</b>:プロトコル設定は、「ホストアドレス」または「ファイルパス」フィールドに情報が指定されている場合にのみ使用されます。個々のXMLドキュメントは、URLの仕様に従って、HTTPまたはHTTPSを使用してダウンロードされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの「行」を定義するXML要素を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> タグ </span> <p>解析済みXMLデータのXPath表現を指定します。 上記のAdobeXMLドキュメントの例で、Itemtagオプションの下の次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、次のように変換されます。 </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>に対応付けられます。 </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内に含まれる）。<span class="codeph">タイトル</span>は、メタデータフィールド<span class="codeph">タイトル&lt;a11に対応します/&gt;。</span> </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性（<span class="codeph">レコード</span>要素内）（name属性は<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph"> desc1に対応します/&gt;。</span> </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">レコード</span>要素内の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本体&lt;a11にマッピングされます。/&gt;。<span class="codeph"></span></span> </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a>を参照 </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグで使用するname属性値を定義します。 </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>が、現在のアカウントに対して定義済みのメタデータフィールドを選択できるドロップダウンリストになります。 </p> <p>必要に応じて、<span class="uicontrol">フィールド</span>の値は、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、<span class="wintitle">フィルタースクリプト</span>で使用されるコンテンツの作成に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプトについて</a>を参照してください。 </p> <p>Index Connectorが、任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が連結されて、結果のキャッシュドキュメントで単一の値になります。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字値（最初に定義された区切り文字）が連結に使用されます。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリ・キーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのインデックス内のURLで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つだけ含まれていない場合でも、<i>2つ以上のフィールドを組み合わせて</i>一意の識別子を形成できる場合は、複数の<span class="uicontrol">タグ</span>を縦区切り文字("|")の値。</span><span class="uicontrol"> </span></p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションを選択すると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> アクション </span> <p>行をマップに追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）**[!UICONTROL Setup Maps]**&#x200B;をクリックして、データソースのサンプルをダウンロードします。 データは、インデックスの適合性を調べられます。 この機能は、テキストおよびフィードのタイプでのみ使用できます。
1. （オプション）**[!UICONTROL Preview]**&#x200B;をクリックして、設定の実際の動作をテストします。 この機能は、テキストおよびフィードのタイプでのみ使用できます。
1. **[!UICONTROL Add]**&#x200B;をクリックして、設定を[!DNL Index Connector Definitions]ページと[!DNL URL Entrypoints]ページの[!DNL Index Connector Configurations]ドロップダウンリストに追加します。

   [URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。
1. [!DNL Index Connector Definitions]ページで、**[!UICONTROL rebuild your staged site index]**&#x200B;をクリックします。
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の編集{#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

定義した既存のインデックスコネクタを編集できます。

>[!NOTE]
>
>[!DNL Type]ドロップダウンリストの「インデックスコネクタ名」や「種類」など、変更できないオプションがあります。

**インデックスコネクタ定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を変更するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Index Connector Edit]ページで、必要なオプションを設定します。

   「[インデックスコネクタ定義の追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)」のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Index Connector Definitions]ページで、**[!UICONTROL rebuild your staged site index]**&#x200B;をクリックします。
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の設定の表示{#task_D0B71A7426E54247BDB3468EC576D871}

既存のインデックスコネクタ定義の設定を確認できます。

[!DNL Index Connector Definitions]ページにインデックスコネクタ定義を追加した後は、その種類の設定を変更できません。 代わりに、定義を削除してから、新しい定義を追加する必要があります。

**インデックスコネクタ定義の設定を表示するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を確認または編集するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

## インデックスコネクタ定義のコピー{#task_3AD55DF07FC44A748D0EFDAB7B35699B}

既存のインデックスコネクタ定義をコピーして、作成する新しいインデックスコネクタの基本として使用できます。

インデックスコネクタ定義をコピーする場合、コピーされた定義はデフォルトで無効になります。 定義を有効または「有効にする」には、[!DNL Index Connector Edit]ページで定義を編集し、**[!UICONTROL Enable]**&#x200B;を選択する必要があります。

「[インデックスコネクタ定義の編集](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)」を参照してください。

**インデックスコネクタ定義をコピーするには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を重複するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Index Connector Copy]ページで、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の名前変更{#task_5132118FC21B47D99881E0ED425225D7}

既存のインデックスコネクタ定義の名前を変更できます。

定義の名前を変更した後、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;をチェックします。 新しい定義名が[!DNL URL Entrypoints]ページのドロップダウンリストに反映されることを確認する必要があります。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

**インデックスコネクタ定義の名前を変更するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、変更するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Index Connector Rename]ページの[!DNL Name]フィールドに、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Rename]**.
1. **[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 リストに以前のインデックスコネクタの名前が存在する場合は、その名前を削除し、新しく名前を変更したエントリを追加します。

   [インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。 1.（オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、行った変更を元に戻します。

      [「履歴」オプションの使用](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [プッシュステージ設定をライブにする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の削除{#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

不要になった、または使用しなくなった既存のインデックスコネクタ定義は削除できます。

**インデックスコネクタ定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector Definitions]ページの[!DNL Actions]列見出しの下で、削除するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Index Connector Delete]ページで、**[!UICONTROL Delete]**&#x200B;をクリックします。
