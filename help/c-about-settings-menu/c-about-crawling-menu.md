---
description: クロールメニューの設定日およびURLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URLエントリポイントを使用します。
solution: Target
subtopic: Crawling
title: クロールメニューについて
topic-legacy: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
exl-id: 22dbbc30-bf1c-4d51-8fb0-708115ba844b
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '11015'
ht-degree: 1%

---

# クロールメニューについて{#about-the-crawling-menu}

クロールメニューの設定日およびURLマスク、パスワード、コンテンツタイプ、接続、フォーム定義、URLエントリポイントを使用します。

## URLエントリポイントについて {#concept_5D857E3B5C124E85BC0B5AE77A509573}

ほとんどのWebサイトには、顧客が最初に訪問する主なエントリポイントまたはホームページが1つあります。 この主なエントリポイントは、検索ロボットがインデックスクロールを開始するURLアドレスです。 ただし、Webサイトに複数のドメインまたはサブドメインがある場合や、サイトの一部がプライマリエントリポイントからリンクされていない場合は、「 URLエントリポイント」を使用して、さらにエントリポイントを追加できます。

指定された各URLエントリポイントの下にあるすべてのWebサイトページにインデックスが付けられます。 URLのエントリポイントとマスクを組み合わせて、Webサイトのどの部分にインデックスを付けるかを正確に制御できます。 URLエントリポイント設定の効果がユーザーに表示されるようにするには、Webサイトのインデックスを再構築する必要があります。

メインエントリポイントは通常、インデックスを作成して検索するWebサイトのURLです。 この主なエントリポイントは、「アカウントの設定」で設定します。

[アカウント設定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)の指定を参照してください。

メインURLエントリポイントを指定した後、必要に応じて、順番にクロールする追加のエントリポイントを指定できます。 ほとんどの場合、メインエントリポイントの下のページからリンクされていないWebページに対して、追加のエントリポイントを指定します。 次の例に示すように、Webサイトが複数のドメインにまたがる場合は、追加のエントリポイントを指定します。

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

各エントリポイントは、次の表に示す1つ以上のスペース区切りキーワードで修飾します。 これらのキーワードは、ページのインデックス作成方法に影響を与えます。

**重要**:特定のキーワードをエントリポイントから、および互いにスペースで区切るようにします。コンマは有効な区切り文字ではありません。

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
   <td colname="col2"> <p> エントリポイントページのテキストのインデックスを作成せず、ページのリンクをたどる場合は、 
     <code>
       noindex 
     </code>を入力します。 </p> <p>次の例に示すように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>このキーワードは、 
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
   <td colname="col2"> <p> エントリポイントページのテキストにインデックスを付けるが、ページのリンクをたどる必要がない場合は、 
     <code>
       nofollow 
     </code>を入力します。 </p> <p>次の例に示すように、キーワードをエントリポイントからスペースで区切ります。 </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>このキーワードは、 
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
     </code>は、通常、検索ロボットがログインフォームを送信し、Webサイトをクロールする前に適切なCookieを受け取れるようにするために使用されます。 「form」キーワードを使用すると、入口ページはインデックス化されず、検索ロボットは、入口ページをクロール済みとしてマークしません。 用途 
     <code>
       nofollow 
     </code>を指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[コンテンツタイプ](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)についても参照してください。

[インデックスコネクタについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)も参照してください。

## インデックスを作成する複数のURLエントリポイントの追加 {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Webサイトに複数のドメインまたはサブドメインがあり、それらをクロールする場合、「 URL入力ポイント」を使用してURLを追加できます。

WebサイトのメインURLエントリポイントを設定するには、「アカウントの設定」を使用します。

[アカウント設定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)の指定を参照してください。

**インデックスを作成する複数のURLエントリポイントを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。
1. [!DNL URL Entrypoints]ページの[!DNL Entrypoints]フィールドに、1行に1つのURLアドレスを入力します。
1. （オプション） **[!UICONTROL Add Index Connector Configurations]**&#x200B;ドロップダウンリストで、インデックス作成のエントリポイントとして追加するインデックスコネクタを選択します。

   ドロップダウンリストは、1つ以上のインデックスコネクタ定義を既に追加している場合にのみ使用できます。

   ![](assets/url_entrypoints_index_connector.png)

   [インデックスコネクタ定義の追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## URLマスクについて {#concept_8039DFC53FF3410AA494D602F71BA164}

URLマスクは、検索ロボットのインデックスをドキュメント化するWebサイトとインデックス化しないWebサイトを決定するパターンです。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

次の2種類のURLマスクを使用できます。

* URLマスクを含める
* URLマスクの除外

URLマスクを含めると、検索ロボットはマスクのパターンに一致するドキュメントのインデックスを作成します。

URLマスクを除外は、検索ロボットに対し、一致するドキュメントのインデックスを作成するよう指示します。

検索ロボットは、リンクからWebサイト内のリンクに移動する際にURLを検出し、それらのURLに一致するマスクを探します。 最初の一致によって、そのURLをインデックスに含めるか除外するかが決まります。 検出されたURLと一致するマスクがない場合、そのURLはインデックスから破棄されます。

エントリポイントURL用のURLマスクを含めるが、自動的に生成されます。 この動作により、Webサイト上で検出されるすべてのドキュメントのインデックスが作成されます。 また、Webサイトを「離れる」リンクも便利に廃止されます。 例えば、インデックス付きのページがhttps://www.yahoo.comにリンクする場合、検索ロボットはそのURLにインデックスを付けません。これは、エントリポイントURLによって自動的に生成されたインクルードマスクと一致しないからです。

指定する各URLマスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* `https://www.mydomain.com/products.html`のような完全パス。
* `https://www.mydomain.com/products`のような部分パス。
* `https://www.mydomain.com/*.html`のようにワイルドカードを使用するURL。
* 正規表現（上級ユーザー向け）。

   マスクを正規表現にするには、キーワード`regexp`をマスクタイプ（`exclude`または`include`）とURLマスクの間に挿入します。

以下に、単純な除外URLマスクの例を示します。

```
exclude https://www.mydomain.com/photos
```

この例は除外URLマスクなので、パターンに一致するドキュメントのインデックスは作成されません。 パターンは、検出された項目（ファイルとフォルダーの両方）を照合し、`https://www.mydomain.com/photos.html`と`https://www.mydomain.com/photos/index.html`（両方とも除外URLと一致）のインデックスが作成されないようにします。 `/photos/`フォルダー内のファイルのみを一致させるには、次の例のように、URLマスクの末尾にスラッシュを含める必要があります。

```
exclude https://www.mydomain.com/photos/
```

次の除外マスクの例では、ワイルドカードを使用しています。 「.pdf」拡張子を持つファイルを検索ロボットが見過ごすよう指示します。 検索ロボットは、これらのファイルをインデックスに追加しません。

```
exclude *.pdf
```

単純なインクルードURLマスクは次のとおりです。

```
include https://www.mydomain.com/news/
```

URLエントリポイントからの一連のリンクを介してリンクされたドキュメント、またはURLエントリポイント自体として使用されるドキュメントのみがインデックス付けされます。 ドキュメントのURLを含むURLマスクとしてリストするだけで、リンクが解除されたドキュメントのインデックスは作成されません。 リンクされていないドキュメントをインデックスに追加するには、「URLエントリポイント」機能を使用します。

[URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

マスクを含めると除外マスクは一緒に使用できます。 除外URLマスクを作成し、除外URLマスクを使用して除外されたページを1つ以上含めることで、Webサイトの大部分をインデックス作成から除外できます。 例えば、エントリポイントURLが次のような場合、

```
https://www.mydomain.com/photos/
```

検索ロボットは、`/photos/summer/`、`/photos/spring/`および`/photos/fall/`（`photos`フォルダーから各ディレクトリに少なくとも1つのページへのリンクがあると仮定）の下にあるすべてのページをクロールし、インデックス化します。 この動作は、リンクパスによって、検索ロボットが`/summer/`、`/spring/`、`/fall/`内のドキュメントを検索でき、フォルダーとフォルダーURLが、エントリポイントURLによって自動的に生成されるインクルードマスクに一致するために発生します。

次の例に示すように、除外URLマスクを含む`/fall/`フォルダー内のすべてのページを除外するように選択できます。

```
exclude https://www.mydomain.com/photos/fall/
```

または、次のURLマスクを使用して、インデックスの一部に`/photos/fall/redleaves4.html`のみを選択的に含めます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

上記の2つのマスクの例が意図したとおりに動作するように、次のようにインクルードマスクが最初にリストされます。

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

検索ロボットは、リストに表示されている順序で指示に従うので、検索ロボットは最初に`/photos/fall/redleaves4.html`を含み、次に`/fall`フォルダー内の残りのファイルを除外します。

手順が次のように逆の方法で指定されている場合：

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

その場合、`/photos/fall/redleaves4.html`は含まれません。

最初に表示されるURLマスクは、マスク設定の後半に表示されるURLマスクよりも常に優先されます。 また、検索ロボットがURLを含むマスクとURLを除外マスクに一致するページを検出した場合は、常に、最初にリストされたマスクが優先されます。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

## URLマスクでのキーワードの使用について {#section_7609A7A6D79B482ABCA8900886541AAB}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致するページのインデックス作成方法に影響します。

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
   <td colname="col2"> <p> URLマスクに一致するページのテキストのインデックスを作成しないが、一致するページのリンクをたどる場合は、 
     <code>
       noindex 
     </code>を含むURLマスクの後に追加します。 次の例のように、キーワードとマスクを必ずスペースで区切ります。 </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>上記の例では、検索ロボットが、 
     <code>
       .swf 
     </code>拡張子を使用しますが、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>10. 
     <code>
       noindex 
     </code>キーワードは、 
     <code>
       content="noindex" 
     </code>を 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> URLマスクに一致するが、一致するページのリンクをたどる必要がないページのテキストのインデックスを作成する場合は、 
     <code>
       nofollow 
     </code>を含むURLマスクの後に追加します。 次の例のように、キーワードとマスクを必ずスペースで区切ります。 </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>10. 
     <code>
       nofollow 
     </code>キーワードは、 
     <code>
       content="nofollow" 
     </code>を 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>インクルードマスクと除外マスクの両方に使用します。 </p> <p>前に 
     <code>
       regexp 
     </code>は正規表現として扱われます。 検索ロボットが除外正規表現URLマスクに一致するドキュメントを検出した場合、それらのドキュメントのインデックスは作成されません。 検索ロボットがInclude正規表現URLマスクに一致するドキュメントを検出した場合、それらのドキュメントのインデックスが作成されます。 例えば、次のURLマスクがあるとします。 </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>検索ロボットは、 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>次の正規表現URLマスクを除外する場合： </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>検索ロボットは、 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>次のURLマスクを含める場合： </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>検索ロボットは、拡張子が「.swf」のファイルからのすべてのリンクに従います。 10. 
     <code>
       noindex 
     </code>キーワードは、一致するファイルのテキストのインデックスが作成されないことを指定します。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規表現</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分にURLマスクを追加する、またはインデックス部分にURLマスクを追加しない {#task_E1AFC17C746048B8843013D979E082C1}

[!DNL URL Masks]を使用して、Webサイトのどの部分にクロールおよびインデックスを作成するかを定義できます。

インデックス作成の後にドキュメントが含まれているかどうかをテストするには、「 URLマスクのテスト」フィールドを使用します。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**Webサイトのインデックス部分にURLマスクを追加する、またはインデックス部分にURLマスクを追加しない場合**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;をクリックします。
1. （オプション） [!DNL URL Masks]ページの「**[!UICONTROL Test URL Masks]**」フィールドに、WebサイトのテストURLマスクを入力し、「**[!UICONTROL Test]**」をクリックします。
1. 「 [!DNL URL Masks] 」フィールドに、 `include` （クロールしてインデックスを作成するWebサイトを追加する場合）と入力するか、 `exclude` （Webサイトがクロールしてインデックスを作成するのを防ぐ場合）と入力し、URLマスクアドレスを入力します。

   1行につき1つのURLマスクアドレスを入力します。 例：

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 日付マスクについて {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

日付マスクを使用して、ファイルの有効期間に基づいて検索結果に含めるファイルや除外するファイルを指定できます。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

次の2種類の日付マスクを使用できます。

* 日付マスク（「include-days」と「include-date」）を含める

   指定した日付以前の日付マスクインデックスファイルを含めます。
* 日付マスクを除外（「exclude-days」と「exclude-date」）

   指定した日付以前の日付のインデックスファイルを除外します。

デフォルトでは、ファイルの日付はメタタグ情報から決まります。 Metaタグが見つからない場合、検索ロボットがファイルをダウンロードした際にサーバから受信したHTTPヘッダからファイルの日付を決定する。

指定する各日付マスクは、別々の行に記述する必要があります。

マスクは、次のいずれかを指定できます。

* `https://www.mydomain.com/products.html`のような完全パス
* `https://www.mydomain.com/products`のような部分パス
* ワイルドカード`https://www.mydomain.com/*.html`を使用するURL
* 正規表現。 マスクを正規表現にするには、URLの前にキーワード`regexp`を挿入します。

「日付を含む」と「日付を除外」の両方で、次の2つの方法のいずれかで日付を指定できます。 マスクは、一致するファイルが指定した日付以前に作成された場合にのみ適用されます。

1. 日数。 例えば、日付マスクが次のような場合、

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   指定した日数がカウントされます。 ファイルの日付が日付に達する前またはそれ以前の場合、マスクが適用されます。

1. YYYY-MM-DD形式の実際の日付。 例えば、日付マスクが次のような場合、

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   一致したドキュメントの日付が指定した日付以前の場合は、日付マスクが適用されます。

以下に、単純な除外日付マスクの例を示します。

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

これは除外日付マスクなので、パターンに一致するファイルはインデックス化されず、90日以前になります。 ドキュメントを除外すると、テキストはインデックス化されず、そのファイルからはリンクが追跡されません。 ファイルは事実上無視されます。 この例では、ファイルとフォルダーの両方が指定したURLパターンに一致する場合があります。 `https://www.mydomain.com/docs/archive.html`と`https://www.mydomain.com/docs/archive/index.html`の両方がパターンに一致し、90日以上前の場合はインデックスが作成されません。 `/docs/archive/`フォルダー内のファイルのみを一致させるには、次のように日付マスクの末尾にスラッシュを含める必要があります。

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

日付マスクはワイルドカードでも使用できます。 次のexcludeマスクは、2011-02-15以前の日付の「.pdf」拡張子を持つファイルを検索ロボットに見渡すように指示します。 検索ロボットは、一致するファイルをインデックスに追加しません。

```
exclude-date 2011-02-15 *.pdf
```

「日付マスクを含める」は似ていますが、一致したファイルのみがインデックスに追加されます。 次のインクルード日付マスクの例は、Webサイトの`/docs/archive/manual/`領域内の古いファイルのテキストのインデックスを検索ロボットに対して作成するように指示します。

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

マスクを含めると除外マスクは一緒に使用できます。 例えば、除外日付マスクを作成し、URLマスクを含む除外ページを1つ以上含めることで、Webサイトの大部分をインデックス作成から除外できます。 エントリポイントURLが次の場合：

```
https://www.mydomain.com/archive/
```

検索ロボットは、`/archive/summer/`、`/archive/spring/`および`/archive/fall/`（`archive`フォルダーから各フォルダーに少なくとも1つのページへのリンクがあると仮定）の下にあるすべてのページをクロールし、インデックス化します。 この動作は、リンクパスによって、検索ロボットが`/summer/`、`/spring/`、`/fall/`の各フォルダー内のファイルを「検索」でき、フォルダーURLがエントリポイントURLによって自動的に生成されたインクルードマスクに一致するために発生します。

[URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

[アカウント設定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)の指定を参照してください。

`/fall/`フォルダー内の90日を超えるページをすべて除外する場合は、次のように日付マスクを除外します。

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

次の日付マスクを使用して、インデックスの一部に`/archive/fall/index.html`のみを（古いファイルの数に関係なく、0日以上のファイルが一致する）選択的に含めることができます。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

上記の2つのマスクの例が意図したとおりに機能するには、次のように、インクルードマスクを最初にリストする必要があります。

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

検索ロボットは指定された順序で方向に従うので、検索ロボットはまず`/archive/fall/index.html`を含み、次に`/fall`フォルダー内の残りのファイルを除外します。

手順が次のように逆の方法で指定されている場合：

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

その場合、マスクで指定されていても`/archive/fall/index.html`は含まれません。 最初に表示される日付マスクは、後でマスク設定に表示される日付マスクよりも常に優先されます。 また、検索ロボットで「含む日付マスク」と「除外する日付マスク」の両方に一致するページが検出された場合は、最初にリストされたマスクが常に優先されます。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

## 日付マスクでのキーワードの使用について {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

各インクルードマスクを1つ以上のスペースで区切られたキーワードで修飾でき、一致するページのインデックス作成方法に影響します。

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
     <code>
       noindex 
     </code>を含む日付マスクの後に次のように表示します。 </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>上記の例では、検索ロボットが、拡張子が「.swf」で、10日以前のファイルからのすべてのリンクに従うように指定しています。 ただし、これらのファイルに含まれるすべてのテキストのインデックス作成は無効になります。 </p> <p>古いファイルのテキストがインデックス付けされていないが、それらのファイルのすべてのリンクに従っていることを確認する必要がある場合があります。 そのような場合は、除外日付マスクを使用する代わりに、「noindex」キーワードを含む日付マスクを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> インクルードマスクで指定された日付以前の日付のページでテキストのインデックスを作成するが、一致するページのリンクをたどる必要がない場合は、 
     <code>
       nofollow 
     </code>を含む日付マスクの後に次のように表示します。 </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>キーワードとマスクは必ずスペースで区切ってください。 </p> <p>10. 
     <code>
       nofollow 
     </code>キーワードは、 
     <code>
       content="nofollow" 
     </code>を 
     一致したページの<code>
       &lt;head&gt;...&lt;/head&gt; 
     </code>タグ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>インクルードマスクと除外マスクの両方に使用します。 </p> <p>検索ロボットは、通常、日付マスクを確認する前に、すべてのファイルをダウンロードして解析します。 この動作は、一部のファイルタイプで、ファイル自体に日付を指定できるために発生します。 例えば、HTMLドキュメントには、ファイルの日付を設定するメタタグを含めることができます。 </p> <p>日付に基づいて多数のファイルを除外し、サーバーに不要な負荷をかけたくない場合は、 
     <code>
       server-date 
     </code>を日付マスク内のURLの後に追加します。 </p> <p>このキーワードは、各ファイルを解析する代わりに、サーバから返されるファイルの日付を検索ロボットに信頼するように指示します。 例えば、次のexclude日付マスクでは、ドキュメントが90日以前の場合、HTTPヘッダーでサーバーから返された日付に従って、URLに一致するページが無視されます。 </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> サーバーから返される日付が90日以上過ぎている場合、 
     <code>
       server-date 
     </code>は、除外されたドキュメントをサーバーからダウンロードしないことを指定します。 その結果、ドキュメントのインデックス作成時間が短縮され、サーバーへの負荷が軽減されます。 If 
     <code>
       server-date 
     </code>が指定されていない場合、検索ロボットはHTTPヘッダーでサーバから返された日付を無視します。 代わりに、各ファイルがダウンロードされ、日付が指定されているかどうかを確認します。 ファイルに日付が指定されていない場合、検索ロボットはサーバから返された日付を使用します。 </p> <p>を使用しないでください。 
     <code>
       server-date 
     </code>を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 包含マスクと除外マスクの両方に使用します。 </p> <p>前に 
     <code>
       regexp 
     </code>は正規表現として扱われます。 </p> <p>検索ロボットは、除外正規表現の日付マスクに一致するファイルを検出した場合、それらのファイルのインデックスを作成しません。 </p> <p>検索ロボットは、「含む」正規表現の日付マスクに一致するファイルを検出した場合、それらのドキュメントのインデックスを作成します。 </p> <p>例えば、次の日付マスクがあるとします。 </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>マスクは、180日以上古い一致するファイルを検索ロボットに除外するよう指示します。 つまり、URLに「archive」という単語を含むファイルです。 </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local">正規表現</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Webサイトのインデックス部分に日付マスクを追加する、またはインデックス部分に日付マスクを追加しない {#task_0010543C55F648D2B5DEFEFAD60FAF04}

日付マスクを使用して、ファイルの有効期間に基づいて顧客検索結果にファイルを含めたり、顧客検索結果からファイルを除外したりできます。

**[!UICONTROL Test Date]**&#x200B;フィールドと&#x200B;**[!UICONTROL Test URL]**&#x200B;フィールドを使用して、インデックス作成後にファイルが含まれているかどうかをテストします。

URLマスクの結果が顧客に表示されるように、サイトのインデックスを再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**Webサイトのインデックス部分に日付マスクを追加する、またはインデックス部分に日付マスクを追加しない場合**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**&#x200B;をクリックします。
1. （オプション） [!DNL Date Masks]ページの&#x200B;**[!UICONTROL Test Date]**&#x200B;フィールドに、YYYY-MM-DD形式の日付（例：`2011-07-25`）を入力します。「**[!UICONTROL Test URL]**」フィールドにwebサイトのURLマスクを入力し、「**[!UICONTROL Test]**」をクリックします。
1. [!DNL Date Masks]フィールドに、1行につき1つの日付マスクアドレスを入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## パスワードについて {#concept_3EDBD731725D46B891F834D4472774DC}

HTTP基本認証で保護されているWebサイトの一部にアクセスするには、1つ以上のパスワードを追加できます。

パスワード設定の効果がユーザーに表示される前に、サイトのインデックスを再構築する必要があります。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

[!DNL Passwords]ページで、各パスワードを1行に入力します。 パスワードは、次の例に示すように、URLまたは領域、ユーザー名、パスワードで構成されます。

```
https://www.mydomain.com/ myname mypassword
```

上記のようにURLパスを使用する代わりに、領域を指定することもできます。

使用する正しい領域を決定するには、パスワードで保護されたWebページをブラウザで開き、「ネットワークパスワードの入力」ダイアログボックスを表示します。

![](assets/realms.gif)

この場合、領域名は「My Site Realm」です。

上記の領域名を使用すると、パスワードは次のようになります。

```
My Site Realm myusername mypassword
```

Webサイトに複数のレルムがある場合は、次の例に示すように、各レルムのユーザー名とパスワードを別々の行に入力して、複数のパスワードを作成できます。

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

URLまたはレルムを含むパスワードを混在させて、パスワード・リストを次のように表示できます。

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

上のリストでは、サーバの認証要求に一致するレルムまたはURLを含む最初のパスワードが使用されます。 `https://www.mysite.com/path1/path2/index.html`のファイルが`Realm3`にある場合でも、例えば`name2`と`password2`は、URLで定義されたパスワードが領域で定義されたパスワードの上に表示されるために使用されます。

## 認証が必要なWebサイトの領域にアクセスするためのパスワードの追加 {#task_DED19D476FF04B48BB6456D5ECB8628A}

パスワードを使用して、クロールやインデックス作成の目的で、Webサイトのパスワードで保護された領域にアクセスできます。

パスワードの効果が顧客に表示される前に、必ずサイトインデックスを再構築してください

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**認証が必要なWebサイトの領域にアクセスするためのパスワードを追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**&#x200B;をクリックします。
1. [!DNL Passwords]ページの「**[!UICONTROL Passwords]**」フィールドに、領域またはURLと、それに関連するユーザー名およびパスワードをスペースで区切って入力します。

   領域パスワードとURLパスワードを別々の行に記述する例：

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   1行に1つのパスワードのみを追加します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## コンテンツタイプについて {#concept_6FEA1355C0374500B4C53090C34A8A07}

[!DNL Content Types]を使用して、クロールしてこのアカウントのインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成の対象として選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、AdobeFlashムービー、Word、Excel、PowerPointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストが、Webサイト上の他のすべてのテキストと共に検索されます。

コンテンツタイプ設定の効果がユーザーに表示される前に、サイトインデックスを再構築する必要があります。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

## MP3音楽ファイルのインデックス作成について {#section_AD2E28BEEE3E46629E2B05C34A963673}

[!DNL Content Types]ページでオプション&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;を選択した場合、MP3ファイルがクロールされ、2つの方法のいずれかでインデックスが作成されます。 最も一般的な方法は、次に示すように、HTMLファイル内のアンカーhrefタグから取得する方法です。

```
<a href="MP3-file-URL"></a>
```

2つ目の方法は、MP3ファイルのURLをURLエントリポイントとして入力する方法です。

[URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

MP3ファイルは、そのMIMEタイプ「audio/mpeg」で認識されます。

MP3音楽ファイルのサイズは、通常は少量のテキストしか含まれていない場合でも、非常に大きい場合があることに注意してください。 例えば、MP3ファイルには、アルバム名、アーティスト名、曲タイトル、曲のジャンル、リリース年、コメントなどを任意で格納できます。 この情報は、ファイルの最後にある、いわゆるTAGに保存されます。 TAG情報を含むMP3ファイルのインデックスは、次のように作成されます。

* 曲のタイトルは、HTMLページのタイトルのように扱われます。
* コメントは、HTMLページに対して定義された説明と同じように扱われます。
* ジャンルは、HTMLページ用に定義されたキーワードのように扱われます。
* アーティスト名、アルバム名、リリース年はHTMLページの本文と同じように扱われます。

Webサイト上でクロールおよびインデックス付けされた各MP3ファイルは、1ページとしてカウントされます。

Webサイトに大きなMP3ファイルが多数含まれている場合、アカウントのインデックス作成バイト制限を超える可能性があります。 この場合は、[!DNL Content Types]ページで&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;の選択を解除して、Webサイト上のすべてのMP3ファイルのインデックス作成を防ぐことができます。

Webサイト上の特定のMP3ファイルのインデックス作成だけを防ぐ場合は、次のいずれかの操作を行います。

* MP3ファイルにリンクするアンカータグを`<nofollow>`タグと`</nofollow>`タグで囲みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

* MP3ファイルのURLを除外マスクとして追加します。

   [URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

## クロールおよびインデックスを作成するコンテンツタイプの選択 {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

[!DNL Content Types]を使用して、クロールしてこのアカウントのインデックスを作成するファイルの種類を選択できます。

クロールおよびインデックス作成の対象として選択できるコンテンツタイプには、PDFドキュメント、テキストドキュメント、AdobeFlashムービー、Word、Excel、PowerPointなどのMicrosoft Officeアプリケーションのファイル、MP3ファイルのテキストが含まれます。 選択したコンテンツタイプ内のテキストが、Webサイト上の他のすべてのテキストと共に検索されます。

コンテンツタイプ設定の効果がユーザーに表示される前に、サイトインデックスを再構築する必要があります。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

中国語、日本語、または韓国語のMP3ファイルをクロールしてインデックスを作成するには、以下の手順を実行します。 次に、 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;で、MP3ファイルのエンコードに使用する文字セットを指定します。

[インジェクションについて](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)を参照してください。

**クロールおよびインデックスを作成するコンテンツタイプを選択するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;をクリックします。
1. [!DNL Content Types]ページで、Webサイト上でクロールおよびインデックスを作成するファイルタイプを確認します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## 接続について {#concept_E2F3B7E7521147479E5948A94BB3A40B}

「接続」を使用すると、検索ロボットがWebサイトのインデックスを作成する際に使用するHTTP接続を最大10個まで追加できます。

接続数を増やすと、クロールとインデックスの完了に要する時間が大幅に短縮されます。 ただし、接続を追加するたびにサーバーの負荷が高くなることに注意してください。

## 接続を追加してインデックス作成を高速化 {#task_3E9B83E43C1842A19066355A15C4A6FB}

「接続」を使用して、クローラーが使用する同時HTTP接続の数を増やすことで、Webサイトのインデックス作成に要する時間を短縮できます。 最大10個の接続を追加できます。

接続を追加するたびに、サーバーに配置される負荷が増加することに注意してください。

**接続を追加してインデックス作成速度を上げるには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**&#x200B;をクリックします。
1. [!DNL Parallel Indexing Connections]ページの「**[!UICONTROL Number of Connections]**」フィールドに、追加する接続数(1～10)を入力します。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォームの送信について {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

フォームの送信を使用すると、Webサイト上のフォームを認識し、処理するのに役立ちます。

Webサイトのクロールおよびインデックス作成中に、検出された各フォームが、追加したフォーム定義と比較されます。 フォームがフォーム定義と一致する場合、そのフォームはインデックス作成用に送信されます。 フォームが複数の定義に一致する場合、一致する定義ごとに1回送信されます。

## Webサイト上のフォームのインデックス作成用のフォーム定義の追加 {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

[!DNL Form Submission]を使用すると、Webサイト上でインデックス作成の目的で認識されるフォームの処理に役立ちます。

変更の結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**Webサイト上のフォームのインデックス作成用のフォーム定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、「**[!UICONTROL Add New Form]**」をクリックします。
1. [!DNL Add Form Definition]ページで、[!DNL Form Recognition]と[!DNL Form Submission]のオプションを設定します。

   [!DNL Form Definition]ページの[!DNL Form Recognition]セクションの5つのオプションは、処理可能なWebページ内のフォームを識別するために使用されます。

   [!DNL Form Submission]セクションの3つのオプションを使用して、フォームと共にWebサーバーに送信されるパラメーターと値を指定します。

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
      <td colname="col2"> <p>フォームを含むWebページを特定します。 単一のページに表示されるフォームを識別するには、次の例のように、そのページのURLを入力します。 </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>複数のページに表示されるフォームを識別するには、ページを記述する際にワイルドカードを使用するURLマスクを指定します。 例えば、<code> https://www.mydomain.com/register/ </code>の下のASPページで発生したフォームを識別するには、次のように指定します。 </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>また、正規表現を使用して複数のページを識別することもできます。 単に 
      URLマスクの前の<code>
        regexp 
      </code>キーワードを、次の例のように指定します。 </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLマスク </p> </td> 
      <td colname="col2"> <p>のアクション属性を識別します。 
      <code>
        &lt;form&gt; 
      </code>タグを使用します。 </p> <p>ページURLマスクと同様に、アクションURLマスクも、単一のURL、ワイルドカードを含むURL、または正規表現の形式を取ることができます。 </p> <p>URLマスクには、次のいずれかを使用できます。 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 次のような完全パス。<code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 次のような部分パス。<code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 以下のようにワイルドカードを使用するURL。<code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 次に示す正規表現。<code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URLマスクまたはアクションURLマスクで識別されるページのテキストのインデックスを作成しない場合、またはそれらのページのリンクをたどりたくない場合は、 
      <code>
        noindex 
      </code>と 
      <code>
        nofollow 
      </code>キーワード。 URLマスクまたはエントリポイントを使用して、これらのキーワードをマスクに追加できます。 </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> URLエントリポイントについて</a>を参照してください。 </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URLマスクについて</a>を参照してください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォーム名マスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      webページの<code>
        &lt;form&gt; 
      </code>タグには、name属性が含まれます。 </p> <p>単純な名前( 
      <code>
        login_form 
      </code>)の名前にワイルドカード( 
      <code>
        form* 
      </code>)または正規表現( 
      <code>
        regexp ^.*authorize.*$ 
      </code>)です。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにすることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>フォームIDマスク </p> </td> 
      <td colname="col2"> <p>フォームが 
      webページの<code>
        &lt;form&gt; 
      </code>タグには、id属性が含まれます。 </p> <p>単純な名前( 
      <code>
        login_form 
      </code>)の名前にワイルドカード( 
      <code>
        form* 
      </code>)または正規表現( 
      <code>
        regexp ^.*authorize.*$ 
      </code>)です。 </p> <p>通常、フォームにはname属性がないので、このフィールドは空のままにすることができます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>指定したパラメーターまたは指定した値を含む指定したパラメーターを含む、または含まないフォームを特定します。 </p> <p>例えば、rick_brough@mydomain.comにプリセットされている電子メールパラメーター（パスワードパラメーター）が含まれ、名パラメーターではないフォームを識別するには、次のパラメーター設定を1行に1つずつ指定します。 </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>フォーム送信</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>アクションURLの上書き </p> </td> 
      <td colname="col2"> <p>フォーム送信の対象がフォームのアクション属性で指定されたものと異なる場合に指定します。 </p> <p>例えば、フォーム内のURLとは異なるURL値を作成するJavaScript関数を使用してフォームが送信される場合に、このオプションを使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Overrideメソッド </p> </td> 
      <td colname="col2"> <p>フォーム送信の対象がフォームのアクション属性で使用されるものと異なる場合と、送信時にJavaScriptによってメソッドが変更された場合を指定します。 </p> <p>すべてのフォームパラメーター( 
      <code>
        &lt;input&gt; 
      </code>タグ（非表示のフィールドを含む）、デフォルト 
      <code>
        &lt;option&gt; 
      </code> 
      <code>
        &lt;select&gt; 
      </code>タグと、 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code>タグ)はWebページから読み取られます。 ただし、「<span class="wintitle">フォーム送信</span>」セクションの「<span class="uicontrol">パラメーター</span>」フィールドに一覧表示されているパラメーターはすべて、フォームのデフォルト値に置き換えられます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>パラメーター </p> </td> 
      <td colname="col2"> <p>フォーム送信パラメーターの先頭に 
      <code>
        not 
      </code>キーワード。 </p> <p>パラメーターに 
      <code>
        not 
      </code>の場合、フォームの送信の一部として送信されません。 この動作は、選択を解除する必要があるチェックボックスに役立ちます。 </p> <p>例えば、次のパラメーターを送信するとします。 </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 値を持つ電子メールパラメーター 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 値を持つパスワードパラメーター 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckboxパラメーターの選択を解除。 </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>その他 
      <code>
        &lt;form&gt; 
      </code>パラメーターをデフォルト値として </p> </li> 
      </ul> </p> <p>フォーム送信パラメーターは次のようになります。 </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>のmethod属性 
      webページの<code>
        &lt;form&gt; 
      </code>タグを使用して、GETメソッドまたはPOSTメソッドを使用して、データをサーバーに送信するかどうかを決定します。 </p> <p>( 
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

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォーム定義の編集 {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Webサイト上のフォームが変更された場合や、定義を変更する必要がある場合は、既存のフォーム定義を編集できます。

[!DNL Form Submission]ページには、フォーム定義に対して行った変更を元に戻す[!DNL History]機能がないことに注意してください。

変更の結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**フォーム定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、更新するフォーム定義の右側にある&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Edit Form Definition]ページで、[!DNL Form Recognition]と[!DNL Form Submission]のオプションを設定します。

   [Webサイト上のフォームのインデックス作成に関するフォーム定義の追加](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F)のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## フォーム定義の削除 {#task_C350FC0CDE344F2786215D544C048B5E}

フォームがWebサイト上に存在しなくなった場合や、特定のフォームを処理してインデックスを作成する必要がなくなった場合は、既存のフォーム定義を削除できます。

[!DNL Form Submission]ページには、フォーム定義に対して行った変更を元に戻す[!DNL History]機能がないことに注意してください。

変更の結果が顧客に表示されるように、サイトのインデックスを必ず再構築してください。

[ステージングされたWebサイトの増分インデックスの設定](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)を参照してください。

**フォーム定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;をクリックします。
1. [!DNL Form Submission]ページで、削除するフォーム定義の右側にある&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。

   削除するフォーム定義が正しいことを確認してください。 次の手順で&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックしても、削除の確認ダイアログボックスは表示されません。
1. [!DNL Delete Form Definition]ページで、「**[!UICONTROL Delete]**」をクリックします。
1. （オプション）次のいずれかの操作を行います。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタについて {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

[!DNL Index Connector]を使用して、XMLページや任意の種類のフィードのインデックス作成用に追加の入力ソースを定義します。

データフィード入力ソースを使用すると、利用可能なクロール方法の1つを使用して、Webサイトで通常検出されるものとは異なるフォームに保存されたコンテンツにアクセスできます。 クロールおよびインデックス付けされた各ドキュメントは、Webサイト上のコンテンツページに直接対応します。 ただし、データフィードは、XMLドキュメント、またはコンマ区切りまたはタブ区切りのテキストファイルから取得され、インデックスを作成するコンテンツ情報が含まれます。

XMLデータソースは、個々のドキュメントに対応する情報を含むXMLスタンサ（レコード）で構成されます。 これらの個々のドキュメントは、インデックスに追加されます。 テキストデータフィードには、個々のドキュメントに対応する個々の改行区切りレコードが含まれます。 これらの個々のドキュメントもインデックスに追加されます。 どちらの場合も、インデックスコネクタ設定では、フィードの解釈方法を説明します。 各設定では、ファイルの保存場所と、サーバーがファイルにアクセスする方法を説明します。 この設定は、「マッピング」情報も記述します。 つまり、各レコードの項目を使用して、結果のインデックスにメタデータフィールドを設定する方法です。

[!DNL Staged Index Connector Definitions]ページにインデックスコネクタ定義を追加した後、「名前」または「タイプ」の値に&#x200B;*以外の設定を変更できます。*

[!DNL Index Connector]ページには、次の情報が表示されます。

* 設定して追加した定義済みのインデックスコネクタの名前。
* 追加した各コネクタに対して、次のいずれかのデータソースタイプを指定します。

   * **テキスト**  — 単純な「フラット」ファイル、コンマ区切り形式、タブ区切り形式、またはその他の一貫した区切り形式。
   * **フィード**  - XMLフィード。
   * **XML**  - XMLドキュメントのコレクション。

* 次回のクロールとインデックス作成に対してコネクタが有効かどうか。
* データソースのアドレス。

[インデックスコネクタについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)も参照してください。

## インデックスコネクタのテキスト設定およびフィード設定に対するインデックス作成プロセスの仕組み {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>テキスト設定とフィード設定の場合、単純なファイルダウンロードです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>ダウンロードしたデータソースを個々の擬似ドキュメントに分類します。 </p> </td> 
   <td colname="col3"> <p><span class="uicontrol">テキスト</span>の場合、改行で区切られた各テキスト行は、個々のドキュメントに対応し、コンマやタブなど、指定した区切り文字を使用して解析されます。 </p> <p><span class="uicontrol">フィード</span>の場合、各ドキュメントのデータは次の形式の正規表現パターンを使用して抽出されます。 </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle">インデックスコネクタの<span class="uicontrol">マップ</span>を使用して</span>を追加し、データのキャッシュコピーを作成して、クローラーのリンクのリストを作成します。 データはローカルキャッシュに保存され、設定済みのフィールドが設定されます。 </p> <p>解析されたデータはローカルキャッシュに書き込まれます。 </p> <p>このキャッシュは後で読み取られ、クローラーで必要な単純なHTMLドキュメントを作成します。 例： </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span>要素は、「タイトル」メタデータフィールドへのマッピングが存在する場合にのみ生成されます。 同様に、 <span class="codeph"> &lt;body&gt; </span>要素は、Bodyメタデータフィールドへのマッピングが存在する場合にのみ生成されます。 </p> <p> <b>重要</b>:事前定義済みのURLメタタグへの値の割り当てはサポートされていません。 </p> <p>その他すべてのマッピングについては、元のドキュメント内のデータを持つ各フィールドに対して<span class="codeph"> &lt;meta&gt; </span>タグが生成されます。 </p> <p>各ドキュメントのフィールドがキャッシュに追加されます。 キャッシュに書き込まれるドキュメントごとに、次の例のようにリンクも生成されます。 </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>設定のマッピングでは、プライマリキーとして識別される1つのフィールドが必要です。 このマッピングは、データがキャッシュから取得される際に使用されるキーを形成します。 </p> <p>クローラーは、URL <span class="codeph">インデックスを認識します。</span>スキームプレフィックス。ローカルにキャッシュされたデータにアクセスできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>キャッシュされたドキュメントセットをクロールします。 </p> </td> 
   <td colname="col3"> <p><span class="codeph">インデックス：</span>リンクは、クローラーの保留中リストに追加され、通常のクロールシーケンスで処理されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>各ドキュメントを処理します。 </p> </td> 
   <td colname="col3"> <p>各リンクのキー値はキャッシュ内のエントリに対応するので、各リンクをクロールすると、そのドキュメントのデータがキャッシュから取得されます。 次に、HTML画像を「アセンブル」し、処理してインデックスに追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## インデックスコネクタのXML設定に対するインデックス作成プロセスの仕組み {#section_7F1551EA51854C5C99F284CE260526EB}

XML設定のインデックス作成プロセスは、次のマイナーな変更と例外を含むテキストおよびフィード設定のプロセスと似ています。

XMLクロールのドキュメントは既に個々のファイルに分割されているので、上記の表の手順1と2は直接適用されません。 [!DNL Index Connector Add]ページの&#x200B;**[!UICONTROL Host Address]**&#x200B;フィールドと&#x200B;**[!UICONTROL File Path]**&#x200B;フィールドにURLを指定すると、そのURLがダウンロードされ、通常のHTMLドキュメントとして処理されます。 ダウンロードドキュメントには`<a href="{url}"...`リンクのコレクションが含まれ、各リンクが処理されるXMLドキュメントを指すことが期待されます。 このようなリンクは次の形式に変換されます。

```
<a href="index:<ic_config_name>?url="{url}">
```

例えば、Adobeの設定から次のリンクが返された場合、

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

上の表では、手順3は適用されず、クロールおよびインデックス作成時に手順4が完了します。

または、XMLドキュメントを、クロールプロセスで自然に検出された他のドキュメントと混在させることもできます。 そのような場合は、書き換えルール( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]** )を使用して、XMLドキュメントのURLを変更し、Index Connectorに転送することができます。

[クロールリスト取得URLルール](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)についてを参照してください。

例えば、次の書き換えルールがあるとします。

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

このルールは、`.xml`で終わるすべてのURLをインデックスコネクタリンクに変換します。 クローラは、`index:` URLスキームを認識して書き換えます。 ダウンロードプロセスは、プライマリ上のIndex Connector Apacheサーバーからリダイレクトされます。 ダウンロードした各ドキュメントは、フィードで使用されるのと同じ正規表現パターンを使用して調べられます。 ただし、この場合、製造されたHTMLドキュメントはキャッシュに保存されません。 代わりに、インデックス処理用にクローラーに直接渡されます。

## 複数のインデックスコネクタの設定方法 {#section_C2B14C0F06354A57AEF6238FF3814E5D}

任意のアカウントに対して複数のインデックスコネクタ設定を定義できます。 次の図に示すように、設定は&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]**&#x200B;のドロップダウンリストに自動的に追加されます。

![](assets/url_entrypoints_index_connector.png)

ドロップダウンリストから設定を選択すると、URLエントリポイントのリストの末尾に値が追加されます。

>[!NOTE]
>
>無効なインデックスコネクタ設定はドロップダウンリストに追加されますが、選択することはできません。 同じインデックスコネクタ設定を2回選択すると、リストの最後に追加され、前のインスタンスが削除されます。

増分クロールのインデックスコネクタエントリポイントを指定するには、次の形式を使用してエントリを追加します。

```
index:<indexconnector_configuration_name>
```

インデックスコネクタページで、追加された各エントリが見つかり、有効になっている場合、クローラーはそのエントリを処理します。

注意：各ドキュメントのURLは、インデックスコネクタ設定名とドキュメントのプライマリキーを使用して構築されるので、増分更新を実行する際は、同じインデックスコネクタ設定名を使用するようにしてください。 これにより、[!DNL Adobe Search&Promote]は、以前にインデックス付けされたドキュメントを正しく更新できます。

[URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)も参照してください。

**インデックスコネクタを追加する際のセットアップマップの使用**

インデックスコネクタを追加する際に、オプションで機能&#x200B;**[!UICONTROL Setup Maps]**&#x200B;を使用して、データソースのサンプルをダウンロードできます。 データはインデックスの適合性を調べられます。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>「インデックスコネクタ」タイプを選択した場合 </p> </th> 
   <th colname="col2" class="entry"> <p>マップを設定機能 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>テキスト </p> </td> 
   <td colname="col2"> <p>最初にタブを試し、次に縦棒( <span class="codeph"> )を試して区切り文字の値を決定します。 | </span>)を挿入し、最後にコンマ( <span class="codeph"> 、 </span>)を挿入します。 「<span class="uicontrol">マップを設定</span>」をクリックする前に区切り文字値を既に指定している場合は、代わりにその値が使用されます。 </p> <p>最適なスキームを使用すると、Mapフィールドに適切なTag値とField値の推測値が入力されます。 さらに、解析済みデータのサンプリングが表示されます。 ファイルにヘッダー行が含まれていることがわかっている場合は、「最初の行の<span class="uicontrol">ヘッダー</span>」を必ず選択してください。 設定関数は、この情報を使用して、結果のマップエントリをより適切に識別します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>フィード </p> </td> 
   <td colname="col2"> <p>データソースをダウンロードし、単純なXML解析を実行します。 </p> <p>結果のXPath識別子は、Mapテーブルのタグ行に表示され、同様の値がFieldsに表示されます。 これらの行は、使用可能なデータのみを識別し、より複雑なXPath定義は生成されません。 ただし、XMLデータとItemtagの値を識別するので、これでも役に立ちます。 </p> <p> <p>注意： 「マップを設定」機能は、分析を実行するXMLソース全体をダウンロードします。 ファイルのサイズが大きい場合、この操作はタイムアウトする可能性があります。 </p> </p> <p>成功した場合、この関数は可能なすべてのXPath項目を識別します。この項目の多くは、使用するのが望ましくありません。 必ず、結果のマップ定義を確認し、不要なマップ定義や不要なマップ定義を削除してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>プライマリリンクリストではなく、代表的な個々のドキュメントのURLをダウンロードします。 この単一のドキュメントは、フィードで使用されるのと同じメカニズムを使用して解析され、結果が表示されます。 </p> <p>「<span class="uicontrol"></span>を追加」をクリックして設定を保存する前に、URLを元のプライマリリンクリストドキュメントに戻してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**重要**:サイズの大きいXMLデータセットに対しては、ファイルパーサがファイル全体をメモリに読み込もうとするので、マップ設定機能が動作しない場合があります。その結果、メモリ不足が発生する場合があります。 ただし、インデックス作成時に同じドキュメントを処理する場合、メモリに読み込まれません。 その代わりに、大きなドキュメントは「外出先で」処理され、最初にメモリに完全に読み込まれるわけではありません。

**インデックスコネクタを追加する際のプレビューの使用**

インデックスコネクタを追加する際に、オプションで&#x200B;**[!UICONTROL Preview]**&#x200B;機能を使用して、データを保存しているかのようにデータを検証できます。 設定に対してテストを実行しますが、設定をアカウントに保存する必要はありません。 テストは、設定済みのデータソースにアクセスします。 ただし、ダウンロードキャッシュは一時的な場所に書き込まれます。インデックス作成クローラーが使用するメインキャッシュフォルダーとは競合しません。

Previewは、 Acct:IndexConnector-Preview-Max-Documentsで制御されたデフォルトの5つのドキュメントのみを処理します。 プレビューされたドキュメントは、インデックス作成クローラーに表示されるとおりに、ソース形式で表示されます。 この表示は、Webブラウザの「ソースを表示」機能に似ています。 標準のナビゲーションリンクを使用して、プレビューセット内のドキュメントを移動できます。

プレビューでは、XML設定はサポートされていません。このようなドキュメントは直接処理され、キャッシュにダウンロードされないからです。

## インデックスコネクタ定義の追加 {#task_96779B651A654E1F871F55D6DBBC8886}

各インデックスコネクタ設定は、データソースと、そのソースに定義されたデータ項目をインデックス内のメタデータフィールドに関連付けるマッピングを定義します。

新しい有効な定義の効果がユーザーに表示される前に、サイトのインデックスを再構築します。

**インデックスコネクタ定義を追加するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Stage Index Connector Definitions]ページで、「**[!UICONTROL Add New Index Connector]**」をクリックします。
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
      <td colname="col2"> <p>インデックスコネクタ設定の一意の名前。 英数字を使用できます。 「_」と「 — 」の文字も使用できます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイプ </p> </td> 
      <td colname="col2"> <p>データのソース。 選択したデータソースタイプは、 <span class="wintitle">インデックスコネクタの追加</span>ページで使用できる結果のオプションに影響します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> テキスト </span> <p>単純なフラットテキストファイル、コンマ区切り、タブ区切り、またはその他の一貫した区切り形式。 改行区切りの各テキスト行は、個々のドキュメントに対応し、指定した区切り文字を使用して解析されます。 </p> <p>各値（列）は、列番号で参照されるメタデータフィールドに1からマッピングできます。 </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>複数の「行」の情報を含むプライマリXMLドキュメントをダウンロードします。 </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>リンク( 
      <code>
        &lt;a&gt; 
      </code>)を個々のXMLドキュメントに追加します。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：テキスト</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、設定を「オフ」にして、クロールやインデックス作成を防ぐこともできます。 </p> <p> <b>注意</b>:無効なインデックスコネクタ設定がエントリポイントリストに見つかった場合、その設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データが存在するサーバーホストのアドレスを指定します。 </p> <p>必要に応じて、次の例のように、データソースドキュメントへの完全なURI(Uniform Resource Identifier)パスを指定できます。 </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p> または </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URIは、「Host Address」、「File Path」、「Protocol」、およびオプションで「Username」、「Password」フィールドの適切なエントリに分類されます。 </p> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、コンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>増分ファイルパス </p> </td> 
      <td colname="col2"> <p>単純なフラットテキストファイル、コンマ区切り、タブ区切り、またはその他の一貫した区切り形式ファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、インクリメンタルインデックスの操作中にダウンロードされて処理されます。 ファイルを指定しない場合は、代わりに[ファイルパス]の下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直ファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新時に使用する単純なフラット・テキスト・ファイル、カンマ区切り、タブ区切り、またはその他の一貫した区切り形式のファイルへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、垂直更新の操作中にダウンロードされて処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子値を含む、単純なフラットテキストファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、インクリメンタルインデックスの操作中にダウンロードされて処理されます。 このファイルに含まれる値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、<span class="uicontrol">プライマリキー</span>として指定された列の、FullまたはIncremental File Pathファイルの値に対応している必要があります。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocol </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>必要に応じて、適切な認証資格情報を入力してHTTPSサーバーにアクセスできます。 </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> File </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>タイムアウト </p> </td> 
      <td colname="col2"> <p>FTP、SFTP、HTTPまたはHTTPS接続のタイムアウトを秒単位で指定します。 この値は30 ～ 300の範囲で指定する必要があります。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>再試行 </p> </td> 
      <td colname="col2"> <p>失敗したFTP、SFTP、HTTP、HTTPSの接続の再試行の最大回数を指定します。 この値は、0 ～ 10の範囲で指定する必要があります。 </p> <p>値が0の場合、再試行は行われません。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>エンコード </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルで使用する文字エンコーディングシステムを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>区切り </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイルの各フィールドの区切りに使用する文字を指定します。 </p> <p>コンマ文字( <span class="codeph"> 、 </span> )は区切り文字の例です。 コンマは、指定したデータソースファイル内のデータフィールドを区切るのに役立つフィールド区切り文字として機能します。 </p> <p><span class="uicontrol"> Tab? </span> を使用して、水平タブ文字を区切り文字として使用します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1行目のヘッダー </p> </td> 
      <td colname="col2"> <p>データソースファイルの最初の行にヘッダー情報のみが含まれ、データは含まれないことを示します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>インデックス作成用のドキュメントの最小数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードするファイルに必要な最小レコード数を指定します。 受け取ったレコードが少ない場合、インデックス操作は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス操作でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定します。 </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 列 </span> <p> 最初の列を1にして列番号を指定します。 各列に新しいマップ行を追加するには、「<span class="wintitle">アクション</span>」で、「<span class="uicontrol"> + </span>」をクリックします。 </p> <p>データソースの各列を参照する必要はありません。 代わりに、値をスキップするように選択できます。 </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>をドロップダウンリストにし、現在のアカウントに対して定義済みのメタデータフィールドを選択できるようにします。 </p> <p><span class="uicontrol">フィールド</span>の値は、必要に応じて、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、 <span class="wintitle">フィルタースクリプト</span>で使用するコンテンツを作成する場合に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプト</a>についてを参照してください。 </p> <p>Index Connectorが任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が、結果としてキャッシュされたドキュメントで単一の値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>の値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字の値（定義された最初の区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つも含まれていない場合でも、<i>で2つ以上のフィールドを組み合わせて一意の識別子を形成できる場合は、<span class="uicontrol">プライマリキー</span>を複数の<span class="uicontrol">列</span>を縦棒（|""の値に基づいて）。</i> </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグがすべて削除されます。 </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> アクション </span> <p>マップに行を追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、設定を「オフ」にして、クロールやインデックス作成を防ぐこともできます。 </p> <p> <b>注意</b>:無効なインデックスコネクタ設定がエントリポイントリストに見つかった場合、その設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのIPアドレスまたはURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含むプライマリXMLドキュメントへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>増分ファイルパス </p> </td> 
      <td colname="col2"> <p>複数の「行」の情報を含む増分XMLドキュメントのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、インクリメンタルインデックスの操作中にダウンロードされて処理されます。 ファイルを指定しない場合は、代わりに[ファイルパス]の下に表示されるファイルが使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>垂直ファイルパス </p> </td> 
      <td colname="col2"> <p>垂直更新中に使用する、複数の疎な「行」の情報を含むXMLドキュメントへのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、垂直更新の操作中にダウンロードされて処理されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパスを削除 </p> </td> 
      <td colname="col2"> <p>1行に1つのドキュメント識別子値を含む、単純なフラットテキストファイルのパスを指定します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> <p>このファイルを指定した場合は、インクリメンタルインデックスの操作中にダウンロードされて処理されます。 このファイルに含まれる値は、以前にインデックス付けされたドキュメントを削除する「削除」リクエストの作成に使用されます。 このファイルの値は、<span class="uicontrol">プライマリキー</span>として指定された列の、FullまたはIncremental File Pathファイルの値に対応している必要があります。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>必要に応じて、適切な認証資格情報を入力してHTTPSサーバーにアクセスできます。 </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> ファイル </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の個々のXML行を識別するために使用できるXML要素を識別します。 </p> <p>例えば、次のAdobeXMLドキュメントのFeedフラグメントでは、Itemtag値は<span class="codeph">レコード</span>です。 </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col1"> <p>インデックス作成用のドキュメントの最小数 </p> </td> 
      <td colname="col2"> <p>正の値に設定した場合は、ダウンロードするファイルに必要な最小レコード数を指定します。 受け取ったレコードが少ない場合、インデックス操作は中止されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> <p> <b>注意</b>:この機能は、完全なインデックス操作でのみ使用されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>XPath式を使用して、XML要素とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobeXMLドキュメントを使用すると、オプションItemtagの下で、次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、を次のように変換します。 </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>要素の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>にマップされます。 </span></p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">コンテンツ</span>属性（<span class="codeph">タイトル</span>という名前属性を持つ<span class="codeph">レコード</span>要素内に含まれる）は、メタデータフィールド<span class="codeph">タイトル&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">レコードの</span>要素（name属性が<span class="codeph">説明</span>）に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性は、メタデータフィールド<span class="codeph"> &lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">レコードの</span>要素内に含まれる<span class="codeph">メタデータ</span>要素の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本文&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a>を参照してください。 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> フィールド </span> <p>生成された各<span class="codeph"> &lt;meta&gt; </span>タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>をドロップダウンリストにし、現在のアカウントに対して定義済みのメタデータフィールドを選択できるようにします。 </p> <p><span class="uicontrol">フィールド</span>の値は、必要に応じて、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、 <span class="wintitle">フィルタースクリプト</span>で使用するコンテンツを作成する場合に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプト</a>についてを参照してください。 </p> <p>Index Connectorが任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が、結果としてキャッシュされたドキュメントで単一の値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>の値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字の値（定義された最初の区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つも含まれていない場合でも、<i>で2つ以上のフィールドを組み合わせて一意のプライマリキー</span>を定義できます。の値に基づいて)。</i><span class="uicontrol"><span class="uicontrol"></span> </span></p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 削除にを使用しますか？  </span> <p>増分インデックス操作でのみ使用されます。 このXPathパターンに一致するレコードは、削除する項目を識別します。 これらの各レコードの<span class="uicontrol">プライマリキー</span>値は、ファイルパスの削除と同様に、「削除」リクエストの作成に使用されます。 </p> <p> <b>注意</b>:この機能は、デフォルトでは有効になっていません。お使いの機能を有効化するには、テクニカルサポートにお問い合わせください。 </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> アクション </span> <p>マップに行を追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>データソースの種類：XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>有効 </p> </td> 
      <td colname="col2"> <p>クロールとインデックスを行う設定を「オン」にします。 または、設定を「オフ」にして、クロールやインデックス作成を防ぐこともできます。 </p> <p> <b>注意</b>:無効なインデックスコネクタ設定がエントリポイントリストに見つかった場合、その設定は無視されます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ホストアドレス </p> </td> 
      <td colname="col2"> <p>データソースファイルが見つかったホストシステムのURLアドレスを指定します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ファイルパス </p> </td> 
      <td colname="col2"> <p>リンク( 
      <code>
        &lt;a&gt; 
      </code>)を個々のXMLドキュメントに追加します。 </p> <p>パスは、ホストアドレスのルートに対する相対パスです。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>プロトコル </p> </td> 
      <td colname="col2"> <p>ファイルへのアクセスに使用するプロトコルを指定します。 次の中から選択できます。 </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>必要に応じて、適切な認証資格情報を入力してHTTPサーバーにアクセスできます。 </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>必要に応じて、適切な認証資格情報を入力してHTTPSサーバーにアクセスできます。 </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTPサーバーにアクセスするには、適切な認証資格情報を入力する必要があります。 </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> ファイル </li> 
      </ul> </p> <p> <b>注意</b>:[プロトコル]設定は、[ホストアドレス]フィールドや[ファイルパス]フィールドに情報が指定されている場合にのみ使用されます。個々のXMLドキュメントは、URL仕様に従って、HTTPまたはHTTPSを使用してダウンロードされます。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>指定したデータソースファイル内の「行」を定義するXML要素を識別します。 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>マップ </p> </td> 
      <td colname="col2"> <p>列番号を使用して、列とメタデータのマッピングを指定できます。 </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> タグ </span> <p>解析されたXMLデータのXPath表現を指定します。 上記の例のAdobeXMLドキュメントを使用すると、オプションItemtagの下で、次の構文を使用してマッピングできます。 </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>上記の構文は、を次のように変換します。 </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph">レコード</span>要素の<span class="codeph"> displayurl </span>属性は、メタデータフィールド<span class="codeph"> page-url </span>にマップされます。 </span></p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p><span class="codeph">メタデータ</span>要素内に含まれる<span class="codeph">コンテンツ</span>属性（<span class="codeph">タイトル</span>という名前属性を持つ<span class="codeph">レコード</span>要素内に含まれる）は、メタデータフィールド<span class="codeph">タイトル&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph">レコードの</span>要素（name属性が<span class="codeph">説明</span>）に含まれる<span class="codeph">メタ</span>要素の<span class="codeph">コンテンツ</span>属性は、メタデータフィールド<span class="codeph"> &lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph">レコードの</span>要素内に含まれる<span class="codeph">メタデータ</span>要素の<span class="codeph">コンテンツ</span>属性（name属性が<span class="codeph">説明</span>）は、メタデータフィールド<span class="codeph">本文&lt;a11にマッピングされます。/&gt;.<span class="codeph"></span></span> </p> </li> 
      </ul> </p> <p>XPathは比較的複雑な表記法です。 詳しくは、次の場所を参照してください。 </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a>を参照してください。 </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> フィールド </span> <p>生成された各&lt;meta&gt;タグに使用するname属性値を定義します。 </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> メタデータ? </span> <p><span class="uicontrol">フィールド</span>をドロップダウンリストにし、現在のアカウントに対して定義済みのメタデータフィールドを選択できるようにします。 </p> <p><span class="uicontrol">フィールド</span>の値は、必要に応じて、未定義のメタデータフィールドにすることができます。 未定義のメタデータフィールドは、 <span class="wintitle">フィルタースクリプト</span>で使用するコンテンツを作成する場合に役立ちます。 </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local">フィルタリングスクリプト</a>についてを参照してください。 </p> <p>Index Connectorが任意のマップフィールドで複数のヒットを持つXMLドキュメントを処理する場合、複数の値が、結果としてキャッシュされたドキュメントで単一の値に連結されます。 デフォルトでは、これらの値はコンマ区切り文字を使用して組み合わされます。 ただし、対応する<span class="wintitle">フィールド</span>の値が定義済みのメタデータフィールドであるとします。 さらに、そのフィールドには<span class="wintitle">許可リスト</span>属性が設定されています。 この場合、フィールドのリスト区切り文字の値（定義された最初の区切り文字）が連結で使用されます。 </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> プライマリキー? </span> <p>プライマリキーとして識別されるマップ定義は1つだけです。 このフィールドは、このドキュメントをインデックスに追加したときに表示される一意の参照になります。 この値は、ドキュメントのURLのインデックスで使用されます。 </p> <p><span class="uicontrol">プライマリキー</span>の値は、インデックスコネクタ設定で表されるすべてのドキュメントで一意である必要があります。発生した重複は無視されます。 ソースドキュメントに<span class="uicontrol">プライマリキー</span>として使用する一意の値が1つも含まれていない場合でも、<i>で2つ以上のフィールドを組み合わせて一意のプライマリキー</span>を定義できます。の値に基づいて)。</i><span class="uicontrol"><span class="uicontrol"></span> </span></p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTMLを削除しますか？  </span> <p>このオプションをオンにすると、このフィールドのデータに含まれるHTMLタグはすべて削除されます。 </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> アクション </span> <p>マップに行を追加したり、マップから行を削除したりできます。 行の順序は重要ではありません。 </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. （オプション）**[!UICONTROL Setup Maps]**&#x200B;をクリックして、データソースのサンプルをダウンロードします。 データはインデックスの適合性を調べられます。 この機能は、テキストおよびフィードのタイプに対してのみ使用できます。
1. （オプション）**[!UICONTROL Preview]**&#x200B;をクリックして、設定の実際の動作をテストします。 この機能は、テキストおよびフィードのタイプに対してのみ使用できます。
1. **[!UICONTROL Add]**&#x200B;をクリックして、設定を[!DNL Index Connector Definitions]ページと[!DNL URL Entrypoints]ページの[!DNL Index Connector Configurations]ドロップダウンリストに追加します。

   [URLエントリポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。
1. [!DNL Index Connector Definitions]ページで、「**[!UICONTROL rebuild your staged site index]**」をクリックします。
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の編集 {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

定義済みの既存のインデックスコネクタを編集できます。

>[!NOTE]
>
>[!DNL Type]ドロップダウンリストの「インデックスコネクタ名」や「タイプ」など、一部のオプションは変更できません。

**インデックスコネクタ定義を編集するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を変更するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。
1. [!DNL Index Connector Edit]ページで、必要なオプションを設定します。

   [インデックスコネクタ定義の追加](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)のオプションの表を参照してください。
1. クリック **[!UICONTROL Save Changes]**.
1. （オプション）[!DNL Index Connector Definitions]ページで、「**[!UICONTROL rebuild your staged site index]**」をクリックします。
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の設定の表示 {#task_D0B71A7426E54247BDB3468EC576D871}

既存のインデックスコネクタ定義の設定を確認できます。

[!DNL Index Connector Definitions]ページにインデックスコネクタ定義を追加した後は、そのタイプ設定を変更できません。 代わりに、定義を削除してから、新しい定義を追加する必要があります。

**インデックスコネクタ定義の設定を表示するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を確認または編集するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

## インデックスコネクタ定義のコピー {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

既存のインデックスコネクタ定義をコピーして、作成する新しいインデックスコネクタの基礎として使用できます。

インデックスコネクタ定義をコピーする場合、コピーされた定義はデフォルトで無効になります。 定義を有効または「オン」にするには、[!DNL Index Connector Edit]ページから定義を編集し、**[!UICONTROL Enable]**&#x200B;を選択する必要があります。

[インデックスコネクタ定義の編集](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)を参照してください。

**インデックスコネクタ定義をコピーするには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、設定を複製するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Copy]**&#x200B;をクリックします。
1. [!DNL Index Connector Copy]ページで、定義の新しい名前を入力します。
1. クリック **[!UICONTROL Copy]**.
1. （オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の名前の変更 {#task_5132118FC21B47D99881E0ED425225D7}

既存のインデックスコネクタ定義の名前を変更できます。

定義の名前を変更したら、 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;をチェックします。 新しい定義名が[!DNL URL Entrypoints]ページのドロップダウンリストに反映されるようにする必要があります。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

**インデックスコネクタ定義の名前を変更するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector]ページの[!DNL Actions]列見出しの下で、変更するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Rename]**&#x200B;をクリックします。
1. [!DNL Index Connector Rename]ページで、[!DNL Name]フィールドに定義の新しい名前を入力します。
1. クリック **[!UICONTROL Rename]**.
1. **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 以前のインデックスコネクタの名前がリストに存在する場合は、その名前を削除し、新しく名前を変更したエントリを追加します。

   [インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。 1.（オプション）[!DNL Index Connector Definitions]ページで、次のいずれかの操作を行います。

   * **[!UICONTROL History]**&#x200B;をクリックして、加えた変更を元に戻します。

      [「履歴」オプション](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)の使用を参照してください。

   * クリック **[!UICONTROL Live]**.

      [ライブ設定の表示](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)を参照してください。

   * クリック **[!UICONTROL Push Live]**.

      [ライブのステージ設定をプッシュする](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)を参照してください。

## インデックスコネクタ定義の削除 {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

不要になった既存のインデックスコネクタ定義や使用しない既存のインデックスコネクタ定義を削除できます。

**インデックスコネクタ定義を削除するには**

1. 製品メニューで、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;をクリックします。
1. [!DNL Index Connector Definitions]ページの[!DNL Actions]列見出しの下で、削除するインデックスコネクタ定義名の&#x200B;**[!UICONTROL Delete]**&#x200B;をクリックします。
1. [!DNL Index Connector Delete]ページで、「**[!UICONTROL Delete]**」をクリックします。
