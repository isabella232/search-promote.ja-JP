---
description: 'null'
seo-description: 'null'
seo-title: よくある質問
solution: Target
title: よくある質問
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# よくある質問{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Webサイト上のSWFファイルのインデックス作成と検索のサポートについて説明するよくある質問ページです。

SWFファイルに関してよく寄せられる質問を次に示します。

* [SWFファイルのクロールとインデックス作成のタイミング](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [SWFのインデックスを作成するには、何を行う必要がありますか。](#section_0A6A52CC70D4495BBE14D91906318F95)
* [SWFファイルはどのように認識されますか。](#section_B36C0536AB544F509601DC6A11A8E656)
* [SWFファイルのインデックスの作成方法](#section_36856058A4B54FA5ABF921344F50410C)
* [SWFファイルは1ページと見なされますか。](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [個々のSWFファイルのインデックスを作成しないようにする方法を教えてください。](#section_E38AD37989EF410B97AF5125057BFD22)
* [SWFファイルのインデックスが作成されないようにする方法を教えてください。](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## SWFファイルのクロールとインデックス作成のタイミング {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

次の例のように、HTMLページ上の埋め込みタグまたはオブジェクトタグにSWFファイルが含まれている場合、SWFファイルのクロールおよびインデックス作成が行われます。

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

また、ファイルURLをエントリポイントとしてリストした場合は、SWFファイルも認識されます。

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

## SWFファイルのインデックスを作成するには、何を行う必要がありますか。 {#section_0A6A52CC70D4495BBE14D91906318F95}

SWFファイルをクロールしてインデックスを作成するには、コンテンツタ **[!UICONTROL Adobe Flash Movies]** イプ(// **[!UICONTROL Settings]** ) **[!UICONTROL Crawling]** を選択しま **[!UICONTROL Content Types]**&#x200B;す。

FlashファイルがHTMLドキュメント内のタグまたはタ `<embed>` グから参照されて `<object>` いる限り、テキストのインデックスが作成され、ファイル内のすべてのURLがクロールされます。

ファイルがタグまたはタグのどちらからも参照さ `<embed>` れていな `<object>` い場合は、HTMLドキュメント内のタグまたはURLエントリポイ `<a href=...>` ントとしてSWFファイルをリストできます。

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

## SWFファイルはどのように認識されますか。 {#section_B36C0536AB544F509601DC6A11A8E656}

SWFファイルは、次のMIMEタイプで識別されます。

`application/x-shockwave-flash`

SWFファイルは、ファイル拡張子が.swf `application/octet-stream`である場 `text/plain` 合、「」またはMIMEタイプでも認識されます。

サーバーの設定が正しくない場合、SWFファイルに別のMIMEタイプが使用される可能性があります。 SWFファイルのクロールおよびインデックス作成に問題がある場合は、サーバー設定を確認してください。

## SWFファイルのインデックスの作成方法 {#section_36856058A4B54FA5ABF921344F50410C}

SWFファイルに含まれるテキストは、含まれるHTMLページ内のテキストのよ `<body>` うにインデックス付けされます。 検索結果が埋め込みSWFファイル内のテキストを見つけた場合、結果は実際にはSWFファイルではなく、含まれるHTMLページにリンクします。 これにより、SWFファイルは正しいコンテキストで表示されます。

SWFファイルに「ムービーの読み込み」アクションとしてURLが含まれている場合、参照先のSWFファイル内のテキストのインデックスは、含まれるHTMLページの一部として作成されます。

SWFファイルに「URLの取得」アクションとしてURLが含まれている場合、HTML参照がクロールされ、後でインデックスが作成されるのと同様に、URLは後でクロールされ、インデッ `<a href=...>` クスが作成されます。

SWFファイルがURLエントリポイントとしてリストされている場合、SWFファイルのテキストのインデックスは1つのページとして作成されます。 エントリポイントSWFからテキストを検索した場合、含まれるHTMLページではなく、ムービーに直接リンクされる検索結果です。

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

## SWFファイルは1ページと見なされますか。 {#section_0158D6DE70BC40D78E2374787B9F58AB}

いいえ。SWFファイルは、含まれるHTMLページの一部と見なされます。 SWFファイルに含まれるすべての「ムービーを読み込み」URLも、含まれるHTMLページの一部と見なされます。 したがって、HTMLページから参照されるSWFファイルは、アカウントのページ合計の「ページ」としてカウントされません。

SWFファイルがURLエントリポイントとしてリストされている場合、そのSWFファイルと、そのSWFファイルにリストされているすべての「ムービーを読み込む」URLが、アカウントのページ合計で1つの「ページ」としてカウントされます。

## 個々のSWFファイルのインデックスを作成しないようにする方法を教えてください。 {#section_E38AD37989EF410B97AF5125057BFD22}

SWFファイルのインデックスが作成されないようにするには、含まれるHTMLドキュメントにロボットのメタタグ( `<meta name="ROBOTS" content="NOINDEX">`)ま `<noindex>` たはタグのいずれかを追加します。 つまり、またはタグを含むドキュ `<embed>` メント `<object>` です。

また、robotsのmetaタグ( `<meta name="ROBOTS" content="NOFOLLOW">`)を使用して、SWFファイルに含まれる次のURLを防ぐこともできます。 含まれるHTMLドキュメントで次の操作が無効になっている場合、SWFファイルで「Get URL」アクションとしてリストされたURLは実行されません。

## SWFファイルがWebサイトでインデックス付けされないようにする方法を教えてください。 {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

SWFインデックスを無効にするには、コンテンツタイ **[!UICONTROL Adobe Flash Movies]** プ( > **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** )の選択を解除 **[!UICONTROL Content Types]**&#x200B;します。

を使用して、SWFファイルのインデック [!DNL URL Masks] ス作成を無効にすることもできます。

詳しくは、 [URLマスクをインデックスに追加する、またはインデックス部分に追加しないを参照してください。](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

SWFインデックスを無効にするには、次のURLマスクのいずれかを入力します。

* `exclude *.swf` （正規表現を使用していない場合）
* `exclude regexp ^.*\.swf$` （正規表現を使用している場合）

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

## Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。 {#section_EE1A3A705AE74148BD195A0CE513A5C4}

サイト検索/マーチャンダイジングは、Adobe Flashで作成されたSWFファイルからUTF-8を取得します。 UTF-8には、言語の表示は含まれていません。 コンテンツタイプ(// **[!UICONTROL Adobe Flash Movies]****[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**)を選択した場合は、メタデータイプのインジェクションを使用して、SWFファイルで使用する言語を指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

古いSWFファイルでも文字セットが指定されていません。 SWFコンテンツタイプ( > **[!UICONTROL Adobe Flash Movies]** > **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する文字セットを指定する必要があります。

## 一般検索 {#reference_E2C675162789452A9B99C6633B12CBEF}

サイト検索/マーチャンダイジングが、Webサイトを訪問する顧客がどのようにして探しているものを見つけるかを示すよくある質問ページです。

一般検索に関する一般的な質問を次に示します。

* [サイトを使用するには、ソフトウェアをインストールする必要がありますか。](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [サイトがページの制限を超えた場合はどうなりますか。](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [毎週の電子メールアドレスを変更する方法を教えてください。](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [サイト検索/マーチャンダイジングに関する顧客情報はどの程度安全ですか。](#section_5484CB954167412BB7F0480CB0C504B8)
* [顧客情報のプライバシーについて教えてください。](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [自分のバナー広告を検索に表示できますか。](#section_611EB8B32C16418386CB7DC7FB6954B8)

検索機能に関してよく寄せられる質問を次に示します。

* [サイトの検索結果をカスタマイズできますか。](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [顧客が検索している情報を確認できますか。](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [どのコンテンツタイプ（PDF、テキスト、Flash、MP3およびMicrosoft Office）のインデックスを作成して検索するかを制御する方法を教えてください。](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [ASP、JSP、PHP、CFM、またはPerlベースのコンテンツを使用して動的に生成されるWebページはサポートされていますか。](#section_E279F004F1C542A2B9773B832E7B013F)
* [同義語を使用して検索結果を改善する方法](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [検索結果の順序を管理できるか。](#section_C6361048502745779D9749A842C4C370)
* [検索結果ページの言語を変更できますか。](#section_6EE41DA8241247D48BBEB061A50599C5)
* [アドビに複数のサイトを持つことはできますか。](#section_AFA8825182094660A71EEC84B8329D6D)
* [複数のドメインを検索できますか。](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [サイトを個別のセクションに細分して…](#section_52153A9DE9F9493B967A70583848B2A4)
* [Webサイトの一部を除外する方法を教えてください。](#section_D452EDE153654EF398F4A87780C6D43B)
* [どの文字セットがサポートされていますか。](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [Webサイトを変更または更新した場合はどうなりますか。](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [自分のサイトのインデックスを自動的に作成できますか。](#section_9C7D41636238488691ECDFEE4D4E5103)
* [私は自分のウェブサイトでパスワードを使う。 引き続きサイト検索/マーチャンダイジングを使用できますか。](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [httpsのクロールとインデックス作成をサポートしているか、または…](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [サイト検索/マーチャンダイジングは、Webサイト上のrobots.txtファイルに従いますか。](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [ウェブサイトの特定の部分は頻繁に更新する必要があるので…](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [スクリプトまたはプログラムを使用して増分を開始できますか…](#section_0B6BB039557A42AA876D35D748E17DD0)

## サイト検索/マーチャンダイジングを使用するには、ソフトウェアをインストールする必要がありますか。 {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

いいえ。これは、サイト検索/マーチャンダイジングの主な利点です。 エンジンは、プロ仕様のアプリケーションで、当社の高パフォーマンスのサーバー上で完全にホストされ、維持されています。 これにより、他の検索ソリューションよりもソフトウェアの方が使いやすくなります。 必要なのは、Webサイトの顧客が検索を入力できるように、ページに少量のHTMLコードを追加することだけです。 サイト検索/マーチャンダイジングは、他のすべての処理を行います。

## サイトがページの制限を超えた場合はどうなりますか。 {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

訪問者が中断することなくWebサイトを検索できるように、検索を継続して提供します。 Webサイトがページの制限を超えているかどうかを確認するには、完全なインデックスのステータスまたはライブログを確認します。

About [Full Indexを参照してください](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3)。

ライブま [たはステージングされた完全なインデックスログの表示を参照してください。](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## 週別レポートの送信先の電子メールアドレスを変更する方法を教えてください。 {#section_AE27F63DD13F425B940C8E7D9ED5C614}

毎週のレポートは、アクティブな各アカウントの所有者に送信されます。 電子メールアドレスは、//をクリッ **[!UICONTROL Settings]** クして変 **[!UICONTROL My Profile]** 更できま **[!UICONTROL Personal Information]**&#x200B;す。 複数のアクティブな検索アカウントがある場合は、すべてのニュースレターが新しいアドレスに送信されます。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

## サイト検索/マーチャンダイジングに関する顧客情報はどの程度安全ですか。 {#section_5484CB954167412BB7F0480CB0C504B8}

サイト検索/マーチャンダイジングは、安全で、高速で、安定し、使いやすくなっています。 Cookieを（必要に応じて）使用することを強制されることはありません。また、パスワードなどの機密情報は、後でブラウザーから取得できるURLリンクには置かれません。

## 顧客情報のプライバシーについて教えてください。 {#section_8FB493F15E51454BA92A0C83E14C0CC7}

アドビは、お客様と訪問者のプライバシーを守ることに取り組んでいます。 See the Adobe [Privacy Center](https://www.adobe.com/privacy.html).

## 検索結果ページに自分のバナー広告を表示できますか。 {#section_611EB8B32C16418386CB7DC7FB6954B8}

はい。検索結果の外観と内容を制御します。 Webサイトの検索結果テンプレート内で、LinkExchangeやSmartClicksなど、独自のバナー交換ネットワークへのリンクを作成できます。 訪問者が行ったヒットは、バナー交換アカウントに適切にクレジットされます。

## サイトの検索結果をカスタマイズできますか。 {#section_A64B3A621B794DF78D35ED06D9C43D0B}

はい。これは、サイト検索/マーチャンダイジング専用の機能です。 アドビの高度なテンプレート技術とHTMLに関する知識があれば、検索結果の表示を正確に制御できます。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

お客様のサーバとサイト検索/マーチャンダイジングサーバとの間の移行は、お客様にとって完全にシームレスで目に見えないものです。 HTMLがわからない場合や、カスタムテンプレートを作成する時間がない場合は、アドビのプロフェッショナルWeb開発者の社内チームが作成する、魅力的で使いやすい様々なテンプレートから選択できます。

## サイトで検索している顧客を確認できますか。 {#section_73709E1B0E82478DA7B4D15B6C845F33}

はい。過去2か月間にWebサイトを訪問した訪問者による検索の検索統計を保持します。 これらの統計は、製品メニューの「レポート」でいつでも確認できます。 検索レポートは、Webサイトで訪問者が何を探しているかに関する重要な情報を提供します。 この情報を使用して、デザインを改善したり、サイト検索/マーチャンダイジングエンジンを調整して訪問者に対してより良いサービスを提供したりできます。

## どのコンテンツタイプ（PDF、テキスト、Flash、MP3およびMicrosoft Office）のインデックスを作成して検索するかを制御する方法を教えてください。 {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

PDFドキュメント、プレーンテキストドキュメント、Flashムービー、MP3ファイル、またはMicrosoft Officeドキュメント内のテキストのインデックス作成と検索を有効または無効にするアカウントを簡単に設定できます。

これらの設定はページ上で制御さ [!DNL Staged Content Types] れます。

コンテンツタ [イプについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)い。

## ASP、JSP、PHP、CFM、またはPerlベースのコンテンツを使用して動的に生成されるWebページはサポートされていますか。 {#section_E279F004F1C542A2B9773B832E7B013F}

静的または動的に生成されるHTML Webページのインデックスが作成されます。これには、データベースやその他のバックエンドプロセスから作成されたページが含まれます。 ブラウザーに表示されるHTMLコードはインデックス付けされるので、これらのバックエンドアーキテクチャがHTMLページに結び付く限り、Webサイトでサイト検索/マーチャンダイジングを使用できます。

検索ロボットは、で指定したWebサイトアドレスの最初のページからWebサイトをクロールし、ペ [!DNL Account Settings]ージ間のリンクに従って移動します。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

検索ロボットがWebサイトのすべてのページをクロールしてインデックスを作成すると、検索エンジンを使用してサイトを検索できます。 つまり、動的に生成されたドキュメントが他のページのリンクと共にWebサイトに組み込まれている場合でも、検索ロボットは動的なコンテンツをクロールし、インデックスを付けることができます。

Webサイトのコンテンツをクロールしてインデックス化すると、Webサイトの顧客はインデックス化されたコンテンツ内の情報を検索できます。

## 同義語を使用してサイトの検索結果を改善する方法を教えてください。 {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

同義語は、訪問者が検索クエリに関連するページを見つける場合に使用できます。

例えば、サイトで販売する製品の価格表を含むページがあるとします。 ただし、サイト検索/マーチャンダイジングで提供される検索レポートを調べると、顧客が検索で「コスト」、「費用」、「料金」、「手数料」という語を探していることがわかります。 これらの単語は、検索結果に価格表ページを表示しません。 の機能を使 [!DNL Add Synonyms] 用する [!DNL Dictionaries]と、これらの語句をすべて同義語として指定し、顧客が使用する検索語句に関係なく価格表を検索できるようになります。

辞書につ [いてを参照](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034)。

## 検索結果の順序を管理できますか。 {#section_C6361048502745779D9749A842C4C370}

はい。高度な関連性インターフェイスを使用すると、特定の検索クエリに対して返されるページを制御できます。 この機能は、顧客が特定の単語をクエリする際に特定のページを確実に表示するようにする場合に役立ちます。

詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。

## 検索結果ページの言語を変更できますか。 {#section_6EE41DA8241247D48BBEB061A50599C5}

はい。サイト検索/マーチャンダイジングテンプレートは、選択した言語を使用し、Webサイトの外観に合わせた結果ページを作成する際に柔軟に使用できます。

テンプレートは、テキスト、標準のHTMLタグ、および検索結果を表示するために定義された特別なタグの組み合わせで構成されます。 顧客が検索を行うと、検索ロボットはテンプレートを読み、標準のHTMLタグを使用してテキストを出力し、特殊なテンプレートタグに基づいて結果のリンクを挿入します。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

結果の言語を変更する場合は、テンプレートに表示される英語のテキストを編集できます。

詳しくは、プ [レゼンテーションまたは転送テンプレートの編集を参照してくださ](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)い。

## アドビのお客様ログインに複数のサイトを設定できますか。 {#section_AFA8825182094660A71EEC84B8329D6D}

はい。アドビのお客様ログイン1つで、様々なWebサイトに対して異なる検索エンジンを管理できます。 「アカウント」でアカウントを選択し、管理します。

使用する [別のアカウントの選択を参照してください](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26)。

## 複数のドメインを検索できますか。 {#section_BFBB0E9861D942F095B56CF0A8F16596}

はい。を使用して、複数のドメインへのアクセスを設定できま [!DNL URL Entrypoints]す。 所有する追加のドメインのURLエントリポイントを指定します。 所有していないドメインのインデックスを作成する権限が必要です。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

## サイトを個別のセクションに細分して、顧客がこれらの領域のいずれかを個別に検索できるようにするか、またはサイト全体を検索できるようにするか。 {#section_52153A9DE9F9493B967A70583848B2A4}

はい。「コレクション」機能が追加され、顧客がWebサイトの特定の領域を検索して、探しているものをすばやく見つけることができます。

コレクション [についてを参照してくださ](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127)い。

例えば、顧客は、製品の販売情報に関連するURLのコレクションや、サポートサービスに関連するURLのコレクションを検索できます。 コレクションを設定して、顧客に対してコレクションのコンボボックスまたはチェックボックスのグループが表示されるようにできます。

## Webサイトの一部を検索対象から除外する方法を教えてください。 {#section_D452EDE153654EF398F4A87780C6D43B}

はい。URLマスクを指定して、インデックスに含めるまたは除外するWebサイトページを決定します。 URLマスクは、Webサイトのページを検索結果に表示するかどうかを決定します。

URLマスクに [ついてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)い。

URLマスクス [クリプトについてを参照してくださ](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)い。

個々のWebページの一部が検索されないように、ページの一部をインデックス作成から除外できます。 テキストをタグとタグで囲 `<noindex>` み `</noindex>` ます。 この方法は、検索からナビゲーションテキストを除外する場合に役立ちます。

## どの文字セットがサポートされていますか。 {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

通常、Webページでは、次のようなメタタグを使用して文字セットを指定します。

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

サイト検索/マーチャンダイジングエンジンは、今日インターネットで使用されているすべての一般的な文字セットを使用して、Webページのインデックスを適切に作成します。 サポートされている文字セットの一部には、以下が含まれます。

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>アラビア語(ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>中国語(繁体；Big5) </p> </td> 
   <td colname="col3"> <p>日本語(Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アラビア語(Windows-1256) </p> </td> 
   <td colname="col2"> <p>中国語(繁体；EUC-TW) </p> </td> 
   <td colname="col3"> <p>ロシア語(KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バルト語(ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>キリル言語(ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>南ヨーロッパ言語(ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バルト語(Windows-1257) </p> </td> 
   <td colname="col2"> <p>キリル言語(Windows-1251) </p> </td> 
   <td colname="col3"> <p>トルコ語(ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中央ヨーロッパ言語(ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>ギリシャ語(ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>トルコ語(Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中央ヨーロッパ言語(Windows-1250) </p> </td> 
   <td colname="col2"> <p>ギリシャ語(Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode (UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>ヘブライ語(ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII(us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>ヘブライ語(Windows-1255) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ言語(ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体字、EUC-CN) </p> </td> 
   <td colname="col2"> <p>日本語(EUC-JP) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ言語(ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体字、GB2312) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ言語(Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体字、GBK) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ言語(x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体字、HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

上記に記載されていない文字セットについては、テクニカルサポートにお問い合わせください。

## Webサイトを変更または更新した場合はどうなりますか。 {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Webサイトのコンテンツを変更した後、フルインデックスまたはインクリメンタルインデックスを実行できます。 サイト検索/マーチャンダイジングは、変更されたWebサイトのコンテンツをダウンロードし、インデックスを作成します。 インデックスの作成が完了すると、新しいコンテンツを検索できます。 また、特定の時間と特定の日に、サイトの自動インデックス作成をスケジュールすることもできます。

ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

詳しくは、 [ライブWebサイトのインデックスの完全なスケジュールの設定を参照してくださ](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)い。

詳しくは、 [ライブWebサイトのインクリメンタルインデックススケジュールの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)い。

## 自分のサイトのインデックスを自動的に作成できますか。 {#section_9C7D41636238488691ECDFEE4D4E5103}

はい。サイトの自動インデックスを毎日スケジュールできます。

毎日の自動インデックス作成の他に、頻繁にサイトの一部を変更し、インデックスを増分的に作成するように選択できます。 自動インデックスがスケジュールされた日に、インデックスの実行時刻を制御できます。 また、必要に応じていつでも手動でサイトインデックスを開始できます。

詳しくは、 [ライブWebサイトのインデックスの完全なスケジュールの設定を参照してくださ](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)い。

詳しくは、 [ライブWebサイトのインクリメンタルインデックススケジュールの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)い。

## 私は自分のウェブサイトでパスワードを使う。 引き続きサイト検索/マーチャンダイジングを使用できますか。 {#section_4618EB5B66704640B5502D1B5CB4B32E}

HTTP基本認証を使用してWebサイトの特定の部分をパスワードで保護する場合、サイト検索/マーチャンダイジングでサイトのインデックスを作成する際に使用できる領域とパスワードを指定できます。

Webサイ [トの必要な領域にアクセスするためのパスワードの追加を参照してください。](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## httpsのクロールとインデックス作成、または安全なサーバーコンテンツのインデックス作成をサポートしていますか。 {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

はい。安全なサーバー(https)上のコンテンツをクロールし、インデックスを作成できます。

## サイト検索/マーチャンダイジングは、Webサイト上のrobots.txtファイルに従いますか。 {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

はい。ロボット排他プロトコルは準拠しています。 検索ロボットは、Webサイトにrobots.txtファイルが存在する場合、そのファイルを調べます。 robots.txtファイルでサイトのクロールの対象からすべてのロボットが除外される場合、サイト検索/マーチャンダイジングロボットも除外されます。 サイト検索/マーチャンダイジングロボットのみがサイトをクロールできるようにするには、robots.txtファイルの内容を次のように設定します。

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

WebロボットとRobots Exclusion Protocolの詳細については、以下を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## 顧客が最も正確な検索結果を得るために、Webサイトの特定の部分を頻繁に更新する必要があります。 増分インデックスはこの問題に役立ちますか？ {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

はい。このシナリオは、サイト検索/マーチャンダイジングを容易にするために増分インデックス機能が構築されたものです。 増分インデックスの主な利点は、企業がWebサイトの一部を動的に変化させるインデックスを頻繁に作成できることです。 この機能により、検索結果が「最大1分間」の精度で表示されます。

ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

詳しくは、 [ライブWebサイトのインクリメンタルインデックススケジュールの設定を参照してくださ](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)い。

## 動的に生成されるWebページは、製品カタログや在庫管理システムなどのバックエンドデータベースからサポートされていますか。 {#section_26896C556483457E879785E751583B16}

静的または動的に生成されるHTML Webページ（データベースから作成されたページやその他のバックエンドプロセスを含む）のインデックスが作成されます。 HTMLコードはブラウザで表示されるようにインデックス付けされているので、バックエンドのデータベース情報がHTMLページに結び付く限り、Webサイトでのサイト検索/マーチャンダイジングを使用できます。

検索ロボットは、で指定したWebサイトアドレスの最初のページからWebサイトをクロールし、ペ [!DNL Account Settings]ージ間のリンクに従って移動します。

詳しくは、 [アカウント設定の指定を参照してくださ](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)い。

検索ロボットがWebサイトのすべてのページをクロールしてインデックスを作成すると、検索エンジンを使用してサイトを検索できます。 つまり、動的に生成されたドキュメントが他のページのリンクと共にWebサイトに組み込まれている場合でも、検索ロボットは、動的なデータベースのコンテンツをクロールし、インデックスを作成できます。

Webサイトのコンテンツをクロールしてインデックス化すると、Webサイトの顧客はインデックス化されたコンテンツ内の情報を検索できます。

タイトル内の情報、メタ説明、メタキーワードドキュメントタグ、またはこれら3つすべてに限定された、フルコンテンツ検索や、より狭いトピックベースの検索を簡単に有効にできます。 また、メタデータ定義を使用して、実際の検索結果に商品の画像などのカスタム表示フィールドを作成することもできます。

詳しくは、 [新しいメタタグフィールドの追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)い。

## スクリプトまたはプログラムを使用してサイトのインデックスを増分的に開始できますか。 {#section_0B6BB039557A42AA876D35D748E17DD0}

はい。スクリプトやプログラムを使用してWebサイトのインデックスを増分的に開始したり、コンテンツが変更または更新されるたびにサイトのインデックスを作成するようにサーバーに対してpingを実行したりできます。

スクリプト化イ [ンデックスについてを参照してくださ](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)い。

## 機能の実装 {#reference_2D0C4A80B8D64051BA9694D562DCE663}

の各機能の実装について説明するよくある質問ページで [!DNL Search&Promote]す。

Webサイトでの機能の実装に関して、よく寄せられる質問を [!DNL Search&Promote] 次に示します。

* [ビジネスルールが実行されないのはなぜですか。](#section_7FEB60383D8A4B11A60DFF9067274699)
* [インデックス作成のスケジュール、インデックス作成の開始中にエラーが発生し、ステージングインデックスの開始中に問題が発生するのはなぜですか。](#section_E05758193DF5436784B0145839989F75)
* [インデックスサイズの制限が許可された境界を超えています。 この問題が発生する理由と修正方法](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## ビジネスルールが実行されないのはなぜですか。 {#section_7FEB60383D8A4B11A60DFF9067274699}

バナーを表示するとき、または結果を表示順序や順序を決める際に、ビジネスルールを設定します。 また、ファセット内の項目の位置や、特定の検索に使用するテンプレートを設定することもできます。
ビジネスルールの順序を変更して、プレゼンテーションテンプレートで実行する順序を変更します。 ビジネスルールは、定義された順に実行されます。つまり、ルールの順序番号が大きいほど、プロセスで後から実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、「ビジネスルール」ページの表の「順序」列に新しい番号を入力します。

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## インデックス作成のスケジュール、インデックス作成の開始中にエラーが発生し、ステージングインデックスの開始中に問題が発生するのはなぜですか。 {#section_E05758193DF5436784B0145839989F75}

インデックスを生成すると、インデックスがいっぱいか増分かに関係なく、インデックスクロールのステータス情報がリアルタイムで表示されます。 例えば、インデックス作成プロセス中に発生した開始時間、経過時間、およびエラーを表示できます。 最後のインデックスのステータスに関する情報も表示されます。 この情報を使用して、発生したインデックスエラーのトラブルシューティングを行います。

インデックスのスケジュールについては、「ライブWebサ [イトのインデックスのフルスケジュールの設定](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) 」および「ライブWebサ [イトのインクリメンタルインデックススケジュールの設定」を参照してください](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)。

ステージングされたインデックスの開始については、 [ライブまたはステージングされたWebサイトのフルインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) または [ライブまたはステージWebサイトの増分インデックスを実行中…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## インデックスサイズの制限が許可された境界を超えています。 この問題が発生する理由と修正方法 {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Webサイトは拡大しがちで、Search&amp;Promoteが追加されたドキュメントやWebページを「見つける」のが長期間にわたります。 最終的に、アカウントがインデックスサイズの制限を超える可能性があります。この場合、を使用することを検討できま **[!UICONTROL URL Mask]**&#x200B;す。 この機能を使用すると、不要なドキュメントやWebページのインデックス付けを行わないインデックスクロールは非表示になり、インデックスサイズが小さくなります。 別の方法として、お使いのアカウントでインデックスサイズの制限を大きく設定する場合は、テクニカルサポートにお問い合わせください。

URLマスクに [ついてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)い。

どのような対処をすべきか不明な場合は、テクニカルサポートにお問い合わせください。 インデックスサイズに影響を与える変数が他にも多数あり、調整するとアカウントの請求にも影響を与える可能性があります。

## 国際 {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

中国語（簡体字および繁体字）、日本語、韓国語などのマルチバイトアジア言語を含む、19を超える言語のインデックス作成と検索のサポートについて説明するよくある質問ページです。

言語と文字セットに関する一般的な質問を次に示します。

* [検索クエリの文字セットエンコーディングを制御するもの](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [検索されたページのエンコーディングが次のエンコーディングと一致する場合のみ。](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [検索結果ページで使用されるエンコーディング](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Unicode、UTF-8、エンコードされたページでサイト検索/マーチャンダイジングを使用できますか。](#section_130997CB08934A13A5261D85CF88040C)
* [Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。](#section_539AFF482F814D28B5929F683D2F2175)
* [Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。](#section_9C0849528AFF4C10AA97A2C912992638)
* [Webサイトで中国語、日本語、韓国語のMicrosoft Officeファイルを検索できないのはなぜですか。](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Webサイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [何か特別な事をして…](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Netscape 4.7以前のバージョンでは、検索結果に中国語、日本語、韓国語のフォントが表示されるのはなぜですか。](#section_DF42567063304F918D406AC76529DFB7)

## 検索クエリの文字セットエンコーディングを制御するものは何ですか。 {#section_DF2E8570AFC2480FA199FD26C941A22F}

検索アカウントの「Webフォーム」セクションには、検索機能をWebサイトに追加する際に使用する検索フォームのサンプルが含まれています。 この検索フォームコードを見ると、次のような行が見つかります。

`<input type=hidden name="sp_f" value="iso-8859-1">`

このコード行は、入力クエリが西ヨーロッパ言語の一般的なエンコードであるiso-8859-1でエンコードされていることを検索エンジンに通知します。 この設定は、製品メニューに移動し、//をクリッ **[!UICONTROL Settings]** クして変 **[!UICONTROL My Profile]** 更できま **[!UICONTROL Personal Information]**&#x200B;す。 ページの [!DNL Personal Information] ドロップリストで、 **[!UICONTROL Character Encoding]** 新しいエンコーディングを選択します。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

検索フォームの行を編集して、Webページのエンコーディング値を手動で変更す `sp_f` ることもできます。 検索フォームの `sp_f` 値は、表示されるページの文字セットエンコーディングと一致する必要があります。

## 検索クエリのエンコーディングと一致するエンコーディングを持つページのみが検索されますか。 {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

デフォルトでは、いいえ。 Webサイトのページが文字セットのエンコーディングを正しく識別できる限り、ページで複数のエンコーディングが使用されている場合でも、検索クエリのエンコーディングとページのエンコーディングとの間で必要な変換が行われます。

## 検索結果ページで使用されるエンコーディング {#section_DA68670F35D54EAABF7DBB010F4409BF}

結果テンプレートのデフォルトのエンコーディングは、アカウントの文字セットエンコーディングによって決まります。

詳しくは、 [個人ユーザ情報の設定を参照してくださ](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)い。

HTMLテンプレートで文字セットを指定する方法について詳しく説明します。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

## Unicode、UTF-8、エンコードされたページでサイト検索/マーチャンダイジングを使用できますか。 {#section_130997CB08934A13A5261D85CF88040C}

はい。ただし、UTF-8などのUnicode文字セットは、ページの書き込み言語を判断するのに十分な情報を提供しません。 これらのページを正しく検索するには、言語を指定する必要があります。 ドキュメントの言語を判断するには、次の順序で情報を処理します。

* サーバーからドキュメントに配信されるコンテンツ言語HTTPヘッダー。
* ドキュメントのセクション `META HTTP-EQUIV="Content-Language" Content="ja_JP"`内のMETA要 `<HEAD>` 素（例：）。

* タグのLANG `<HTML>` 属性(例： `<HTML LANG="ja_JP">`)。

サーバーがContent-Language HTTPヘッダーを配信するように設定されておらず、ドキュメントに言語のMETA要素もタグの言語属性も含まれていない場合は、メタデータインジェクションを使用して適切な言語を指定できます。 `<HTML>`

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。 {#section_539AFF482F814D28B5929F683D2F2175}

サイト検索/マーチャンダイジングは、言語を示さないAdobe PDFファイルからUTF-8を取得します。 ( > > **[!UICONTROL PDF Documents]****[!UICONTROL Settings]** )を選択した場合 **[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;は、メタデータインジェクションを使用して、PDFファイルで使用する言語を指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。 {#section_9C0849528AFF4C10AA97A2C912992638}

サイト検索/マーチャンダイジングは、言語を示さないAdobe Flashで作成されたAdobe FlashムービーファイルからUTF-8を取得します。 コンテンツタイプ(// **[!UICONTROL Adobe Flash Movies]****[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する言語を指定する必要があります。

Flashバージョン4以前のSWFファイルの場合、ファイル内の文字セットは指定されません。 コンテンツタイプ(// **[!UICONTROL Adobe Flash Movies]****[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する文字セットを指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Webサイトで中国語、日本語、韓国語のMicrosoft Officeファイルを検索できないのはなぜですか。 {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

サイト検索/マーチャンダイジングは、言語を示さないMicrosoft Officeファイル(Microsoft Word、Microsoft Excel、Microsoft PowerPoint)からUTF-8を取得します。 コンテンツタイプ(// **[!UICONTROL Microsoft Office Files]** )を選択した場合、メタ **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;データインジェクションを使用して、Microsoft Officeファイルで使用する言語を指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Webサイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。 {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

コンテンツタイプ( > **[!UICONTROL Text in MP3 Music Files]** > **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**)を選択した場合、メタデータインジェクションを使用して、MP3ファイルのエンコードに使用する文字セットを指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Webサイト上の.txtファイルを正しくインデックス付けするために、何か特別な操作を行う必要がありますか。 {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

コンテンツタイプ(// **[!UICONTROL Text Documents]** )を選択した場合、メタデ **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;ータインジェクションを使用して、.txtファイルのエンコードに使用する文字セットを指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## Netscape 4.7以前のバージョンでは、検索結果に中国語、日本語、韓国語のフォントが表示されるのはなぜですか。 {#section_DF42567063304F918D406AC76529DFB7}

アカウントでデフォルトのテンプレート、使用可能なテンプレートの1つ、またはこれらのテンプレートに基づくテンプレートを使用する場合は、フォントタグにArialまたはHelveticaをフォントフェースとして指定するフォントタグが含まれる場合があります。 例： `<font face="arial, helvetica" size="+1">`Netscape 4.7以前では、ArialまたはHelveticaのフォントが使用されている場合、中国語、日本語、韓国語の文字は表示されません。 属性を削 `face` 除するか、フォントを中国語、日本語、韓国語に適したフォントに置き換えます。

## 低ページ数 {#reference_4344E3E3CB2948939860F8C078BD7773}

インデックス作成ページ数が少ないことに関連する一般的な問題を説明する、よくある質問のページです。

インデックス作成ページ数の低さに関する一般的な質問を次に示します。

* [インデックスログを調べたか？](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [URLに入力ミスはありますか。](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [エントリポイントWebページに他のページへのリンクが含まれているか。](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [埋め込まれたWebサイト上の他のページへのリンクです。](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Webページ上のHTMLタグが](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [...の中で、HTMLコメントタグの形式が正しくない。](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Webページに別のページへのリンクが含まれているか…](#section_F8082759184049AAA8FA6342C1F84389)
* [URLに仮想ドメインサービスを使用しているか…](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Webページでメタ更新タグを使用しているか。](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Webページでメタロボットタグを使用しているか。](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Webサイトでロボットの除外ファイルを使用しているか。](#section_BF7B663347814F58AD736066C86B7D25)

## インデックスログを調べたか？ {#section_D6626536DC3D40DDA4A1224F1CB276BF}

インデックスログには、サイト検索/マーチャンダイジングロボットがWebサイトのインデックスを作成する際に収集する詳細な情報が含まれます。 ログには、クロールされたリンクと発生したエラーのリストが含まれます。 インデックスログを調べるのが、Webサイト上のすべてのページにインデックスが付けられていない理由を判断する最善の方法です。

ライブま [たはステージングされた完全なインデックスログの表示を参照してください。](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

ライブま [たはステージングされたインデックスの増分ログの表示を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## URLに入力ミスはありますか。 {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

長いURLをHTMLフォームに入力すると、1つ以上の誤字が発生する場合があります。 URLにはスペースを含めないでください。 また、一部のWebサーバーでは、大文字と小文字が区別される方法でURLを処理します。

製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Entrypoints]**。 ページで、 [!DNL Staged URL Entrypoints] 以下を確認します。

* URLに誤字は含まれていません。
* URL内の文字はすべて正しい大文字と小文字を使用しています。
* URLにスペース文字が含まれていません。

URL入力ポイントをテストするには、URLをコピーしてWebブラウザーに貼り付け、Webサイトが表示されるかどうかを確認します。 表示されない場合は、URLパスに誤りがないことを確認してください。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

## エントリポイントWebページには、Webサイト上の他のページへのリンクが含まれていますか。 {#section_1C2D6ED54E7249268B555D9DC33352B3}

サイト検索/マーチャンダイジングロボットは、顧客と同じようにWebサイトをクロールします。ページ間のリンクをたどる方法。 検索ロボットがサイト上の他のページを見つけてインデックスを付けるには、その前にリンクがエントリポイントWebページに存在している必要があります。

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

## Webサイト上の他のページへのリンクはJavaScriptに埋め込まれていますか。 {#section_EE34A67D60A844EBB0921C03544FF63E}

JavaScriptを使用して他のページにリンクするロールオーバーアクションやメニューなど、Webサイト上で高度なナビゲーションテクニックを使用できます。 ただし、サイト検索/マーチャンダイジングロボットは、JavaScriptに埋め込まれたリンクをたどることはできません。

この問題を解決する1つの方法は、JavaScriptを含むHTML内の他のページへの非表示のリンクを配置することです。 Webサイトの顧客にはこれらのリンクは表示されませんが、検索ロボットはリンクを見つけてクロールします。 ページの下部のタグの直前に、非表示のタグを配置でき `</body>` ます。 次のようになります。

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

もう1つの解決策は、Webサイト上の追加ページのURLを、クロールとインデックスのエントリポイントとしてリストすることです。 次に示すように、URL `https://` の先頭を指定します。

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

詳しくは、 [インデックスを作成する複数のURLエントリポイントの追加を参照してください](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)。

## Webページ上のHTMLタグのシーケンスが無効ですか。 {#section_F31A2F5D2C284AC084158A5BD763DC5D}

HTML仕様では、タグ、タグ、タグがHTMLドキ `<html>`ュメ `<head>`ント内の特 `<body>` 定のシーケンスに従っている必要があります。 すべてのWebページのタグは、次の順序で配置する必要があります。

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

HTMLタグの順序が正しくない場合、サイト検索/マーチャンダイジングロボットはWebページの解析とインデックス付けを適切に行えません。 次の例は、適切なシーケンスにないタグの例です。

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

この場合、、、およびタグ `<html>`をWeb `<head>`ページ `<body>` 上の適切なシーケンスに配置します。

## WebページでHTMLコメントタグの形式が正しくない。 {#section_D1C39D79341845CB9C38579AABDF3A24}

Webページで無効なHTMLコメントを注意深く確認し、修正してください。

HTMLの仕様では、HTMLコメントは文字で始まり、文字で終わ `<!--` る必要があります `-->`。 サイト検索/マーチャンダイジングロボットがWebページ上のタグを誤って解析する原因となる、誤った形式のコメントを見過ごすのは簡単です。 コメントが正しく形成されていない場合は、サイト検索/マーチャンダイジングロボットが、解析が必要な他の重要なタグを見逃す原因になる可能性があります。 Webページのタグの直前のコメントに `<body>` 注意してください。

次に、適切に形成されたコメントの例を示します。

`<!-- This HTML comment is OK. -->`

次の例は、コメントの形式が正しくない場合を示しています。

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Webページに、別のドメインのページへのリンクが含まれているか。 {#section_F8082759184049AAA8FA6342C1F84389}

多くの場合、Webサイトは、異なるドメインアドレスを持つWebサーバー上に実際に存在するページで構成されます。 例えば、メインWebサイトのアドレスが次のような場合、

`https://www.mydomain.com/`

また、Webサイトには、次のような別のドメインのページが含まれている場合もあります。

`https://www.otherdomain.com/`

デフォルトでは、サイト検索/マーチャンダイジングロボットは、メイン以外のドメインのリンクをたどりません。 ただし、検索アカウントに追加のエントリポイントを設定すると、複数のドメインのインデックスを簡単に作成できます。

製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Entrypoints]**。 サイトの「メインWebサイトエントリポイント」URLを追加します。 次に、サイトページを含む他のドメインにURLエントリポイントを追加します。 例えば、メインURLエントリポイントを次のように設定します。

`https://www.mydomain.com/`

次の追加のサイトURLエントリポイントを追加します。

`https://www.otherdomain.com/`

## URLに仮想ドメインサービスを使用しているか。 {#section_2861F09EA21A45E6B7E15F032739CDF3}

仮想ドメインサービス（「ドメインリダイレクトサービス」とも呼ばれる）を使用して、顧客がWebサイトにアクセスするためのより良いURLを提供している可能性があります。 例えば、Webサイトの実際のアドレスが次のような場合、

`https://www.myispdomain.com/~myname/mywebpages/`

ただし、仮想ドメインサービスを使用すると、顧客は次のアドレスでサイトにアクセスできます。

`https://myname.adomain.com/`

 または

`https://adomain.com/myname/`

デフォルトでは、サイト検索/マーチャンダイジングロボットは、メイン以外のドメインのリンクをたどりません。 ただし、検索アカウントに追加のエントリポイントを設定すると、複数のドメインのインデックスを簡単に作成できます。

製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Entrypoints]**。 サイトの仮想ドメイン名に「メインWebサイトのURLエントリポイント」を追加します。 次に、Webサイトが実際に存在するドメインに別のエントリポイントを追加します。

例えば、メインURLエントリポイントを次のように設定します。

`https://myname.adomain.com/`

次のWebサイトのURLエントリポイントを追加します。

`https://www.myispdomain.com/~myname/mywebpages/`

## Webページでメタ更新タグを使用しているか。 {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

多くのWebサイトには、次のようなタグの間にメタ更新タグを含むフロントペ `<head>...</head>` ージがあります。

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

特定の状況で、サイト検索/マーチャンダイジングロボットがメタ更新URLをたどってWebサイトのコンテンツのインデックスを作成できない場合があります。 この問題は、追加のエントリポイントを設定することで簡単に対処できます。

製品メニューで、/クロール/ **[!UICONTROL Settings]** をクリックしま **[!UICONTROL URL Entrypoints]**&#x200B;す。 メタ更新タグのURLに別のエントリポイントを追加します。

## Webページでメタロボットタグを使用しているか。 {#section_36275A33DDFE4620BABA948F8A63DBD2}

Webページでは、メタロボットタグを使用して、定期的にWebサイトをクロールしようとするWebロボットを制御する場合があります。 Webページのタグの間にメタロボ `<head>...</head>` ットのタグが表示され、次のタグのようになります。

`<meta name="robots" content="noindex, nofollow">`

サイト検索/マーチャンダイジングロボット自体がWebロボットなので、メタロボットタグの指示に従います。 この方法で他のロボットを除外すると、サイト検索/マーチャンダイジングロボットも除外されます。

WebロボットとRobots Exclusion Protocolの詳細については、以下を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Webサイトでインデックスを作成するWebページのメタロボットタグを削除または変更します。

## Webサイトでロボットの除外ファイルを使用しているか。 {#section_BF7B663347814F58AD736066C86B7D25}

Webサイトにrobots.txtというページがあり、すべてのロボットや特定のロボットがクロールから除外される場合があります。 Webサイトにrobots.txtファイルがあるかどうかを確認するには、次に示すように、最上位ドメインのすぐ下にあるファイルを探します。

`https://www.yourdomain.com/robots.txt`

robots.txtファイルの内容は次のようになります。

```
User-agent: * 
Disallow: /
```

サイト検索/マーチャンダイジングロボット自体がWebロボットなので、robots.txtファイルの指示に従い、サイト検索/マーチャンダイジングロボットを除外します。 この問題を回避するには、robots exclusion file(robots.txt)を編集して、サイト検索/マーチャンダイジングロボットが次のようにWebサイトをクロールし、インデックスを付けることを許可します。

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Webサイト上でのMicrosoft® Officeファイルのインデックス作成と検索のサポートについて説明するよくある質問ページです。

Microsoft Officeファイルに関してよく寄せられる質問を次に示します。

* [Microsoft Officeファイルでインデックスを作成する](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Microsoft Officeファイルでインデックスが作成されない内容…](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [HTMLページとは異なる方法でMicrosoft Officeファイルのインデックスを作成する方法…](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Microsoft Officeファイルのインデックスを作成しないようにする方法](#section_FEBA71274CD14CB99731ADF982087F4C)

## Microsoft Officeファイルでインデックスを作成する {#section_8681DADFCFE24B7787B1FC08D431EE28}

Microsoft Wordファイル、Microsoft Excelファイル、およびMicrosoft PowerPointファイルの完全な内容のインデックスが作成されます。

Microsoft Wordファイルの次の部分のインデックスが作成されます。

* タイトル
* キーワード
* 件名（説明）
* テキストベースのコンテンツ
* 他のドキュメントへのハイパーリンク

Microsoft Excelファイルの次の部分のインデックスが作成されます。

* タイトル
* キーワード
* 件名（説明）
* セル内のテキスト
* セル内の数式の値

Microsoft PowerPointファイルの次の部分のインデックスが作成されます。

* タイトル
* キーワード
* 件名（説明）
* 各スライドのテキスト

## Microsoft Officeファイルでインデックスが作成されない内容 {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Microsoft Officeファイルに含まれるグラフィック、または含まれるグラフィックの一部であるテキストはインデックス付けされません。 カスタムプロパティの定義は、メタデータとしてインデックス化されません。 PowerPointファイル内のヘッダーやフッターなど、特別なフィールドのテキストの一部もインデックス付けされません。

## HTMLページとは異なるインデックス付けを行うMicrosoft Officeファイルの作成方法 {#section_C104B44684F340549A6B9EB8F39EDDBB}

検索ロボットがMicrosoft OfficeファイルとHTMLファイルをインデックス付けする方法の違いは、各HTMLファイルが個別のページで、1つのMicrosoft Officeファイルが数百ページを表すことができることです。 このため、各ページは、Microsoft Officeファイル内で検索アカウントの下の個別のページとしてカウントされます。

## Microsoft OfficeファイルのインデックスがWebサイト上で作成されないようにする方法を教えてください。 {#section_FEBA71274CD14CB99731ADF982087F4C}

検索ロボットでMicrosoft Officeファイルのクロールとインデックスの作成を行わない場合は、コンテンツタイプ(// **[!UICONTROL Microsoft Office Files]** )の選択を解除 **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;します。

また、を使用して、Microsoft Officeフ [!DNL URL Masks] ァイルのインデックスを無効にすることもできます。

次のURLマスクを入力します。

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>正規表現を使用しない場合 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclude *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">exclude *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">exclude *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>正規表現を使用している場合 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">除外regexp ^*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">除外regexp ^*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">除外regexp ^*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

詳しくは、 [URLマスクをインデックスに追加する、またはインデックス部分に追加しないを参照してください。](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Webサイト上のMP3音楽ファイルのインデックス作成と検索のサポートについて説明するよくある質問ページです。

MP3ファイルに関する一般的な質問を次に示します。

* [MP3ファイルはいつクロールされ、インデックスが作成されますか？](#section_538EA1682C9C47E3A62640BB25D84C36)
* [クロールとインデックスの処理…](#section_3CD794446E3545379C14E9F222118665)
* [MP3ファイルはどのようにして認識されますか。](#section_230E7336965A424F96C5CCF1D3C2D103)
* [MP3ファイル内のインデックスは何ですか。](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [MP3ファイルは1ページと見なされますか。](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [個々のMP3ファイルのインデックスを作成しないようにする方法を教えてください。](#section_C989DC1D3D3841B38F683A462195DC05)
* [MP3ファイルのインデックスが作成されないようにする方法を教えてください。](#section_305D2B28D1124776B6DC0C62A17827C6)
* [サイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## MP3ファイルはいつクロールされ、インデックスが作成されますか？ {#section_538EA1682C9C47E3A62640BB25D84C36}

MP3ファイルは、2つの方法のいずれかでクロールおよびインデックス化されます。 最も一般的な方法は、HTMLファイル内のアンカーhrefタグを使用する方法です。

`<a href="MP3-file-URL"></a>`

2つ目の方法は、MP3ファイルのURLをURL入力ポイントとして入力する方法です。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

## サイト上のMP3ファイルをクロールしてインデックスを作成するには、何をする必要がありますか。 {#section_3CD794446E3545379C14E9F222118665}

アカウントのMP3のクロールとインデックス作成をアクティブにするには、製品メニューで//をク **[!UICONTROL Settings]** リック **[!UICONTROL Crawling]** しま **[!UICONTROL Content Types]**&#x200B;す。 ページで、 [!DNL Staged Content Types] を選択します **[!UICONTROL Text in MP3 Music Files]**。

コンテンツタ [イプについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)い。

## MP3ファイルはどのようにして認識されますか。 {#section_230E7336965A424F96C5CCF1D3C2D103}

MP3ファイルは、「audio/mpeg」のMIMEタイプで認識されます。

## MP3ファイル内のインデックスは何ですか。 {#section_E99D252B27CA4946AED3FCD3ABD8779D}

MP3ファイルには、必要に応じて少量のテキスト情報が格納されます。 この情報には、アルバム名、アーティスト名、曲のタイトル、曲のジャンル、リリース年度、コメントが含まれます。 この情報は、ファイルの最後にTAGと呼ばれる場所に保存されます。 TAG情報を含むMP3ファイルのインデックスは、次の方法で作成されます。

* 曲のタイトルは、HTMLページのタイトルと同じように扱われます。
* コメントは、HTMLページに対して定義された説明と同じように扱われます。
* ジャンルは、HTMLページに対して定義されたキーワードと同じように扱われます。
* アーティスト名、アルバム名およびリリース年は、HTMLドキュメントの本文と同じように扱われます。

## MP3ファイルは1ページと見なされますか。 {#section_9910BEB6617D4D2090558CDF6C65D16B}

はい。Webサイト上でクロールされ、インデックスが作成された各MP3ファイルは、1ページとしてカウントされます。

## 個々のMP3ファイルのインデックスを作成しないようにする方法を教えてください。 {#section_C989DC1D3D3841B38F683A462195DC05}

MP3ファイルにリンクするアンカータグを、タグとタグで囲 `<nofollow>``</nofollow>` みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

もう1つの方法は、MP3ファイルのURLを除外マスクとして追加することです。

URLマスクに [ついてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)い。

URLマスクス [クリプトについてを参照してくださ](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)い。

## MP3ファイルのインデックスが作成されないようにする方法を教えてください。 {#section_305D2B28D1124776B6DC0C62A17827C6}

アカウントのMP3インデックスを制御する最も簡単な方法は、ページの選択を解除す **[!UICONTROL Text in MP3 Music Files]** ることで [!DNL Staged Content Types] す。

詳しくは、ク [ロールおよびインデックスを作成するコンテンツタイプの選択を参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)い。

また、URLマスク機能を使用して、ファイル拡張子によるMP3インデックス作成を無効にすることもできます。 これを行うには、製品メニューで//をクリ **[!UICONTROL Settings]** ック **[!UICONTROL Crawling]** します **[!UICONTROL URL Masks]**。 次のいずれかのマスクを入力します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>もしアカウントが… </p> </th> 
   <th colname="col2" class="entry"> <p>次のURLマスクを入力します </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>正規表現を使用しない </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclude *.mp3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>正規表現を使用します。 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 除外regexp ^*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

## サイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。 {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

中国語、日本語または韓国語のMP3ファイルを検索するには、製品メニューで// **[!UICONTROL Settings]** をク **[!UICONTROL Crawling]** リック **[!UICONTROL Content Types]** します **[!UICONTROL Text in MP3 Music Files]**。 次に、//をク **[!UICONTROL Settings]** リック **[!UICONTROL Metadata]** し **[!UICONTROL Injections]**、MP3ファイルのエンコードに使用する文字セットを指定します。

詳しくは、ク [ロールおよびインデックスを作成するコンテンツタイプの選択を参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)い。

About [Injectionsを参照](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)。

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Webサイト上のPDFファイルのインデックス作成と検索のサポートについて、よくある質問(FAQ)ページです。

PDFファイルに関してよく寄せられる質問を次に示します。

* [PDFファイル内のインデックスの作成](#section_62BFCD7158B44F2BB3B1864224B50174)
* [PDFファイル内のインデックス付けされない要素](#section_A14B353AE503408896BACBBF3F748FA0)
* [インデックス付きPDFファイルはどのようにカウントされますか。](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [検索結果にPDFアイコンを表示できますか。](#section_829CE82CC3544502A13D27C4DB820189)
* [検索結果を特定のページにリンクできるか…](#section_A06E7F7017E6441E98209D288EE57BF6)
* [PDFファイルのインデックスが作成されないようにする方法を教えてください。](#section_96671419A822486AAC654D8DAD819940)
* [Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## PDFファイル内のインデックスの作成 {#section_62BFCD7158B44F2BB3B1864224B50174}

PDFファイルの完全なコンテンツのインデックスが作成されます。 PDFファイルの次の部分のインデックスが作成されます。

* タイトル
* キーワード
* 件名（説明）
* テキストベースのコンテンツ

## PDFファイル内のインデックス付けされない要素 {#section_A14B353AE503408896BACBBF3F748FA0}

PDFの目次、ファイル内のグラフィック、または含まれるグラフィックの一部であるテキストはインデックス化されません。

## インデックス付きPDFファイルはどのようにカウントされますか。 {#section_C35DE36A65D649BD8FF314E9EFD990A6}

複数のページを含むPDFを含む各PDFファイルは、1つのドキュメントとしてカウントされます。

## 検索結果にPDFアイコンを表示できますか。 {#section_829CE82CC3544502A13D27C4DB820189}

はい。テンプレート `<search-if-link-extension>` 内でタグを使用して、PDFアイコンや他のグラフィックやテキストを検索結果に含めます。

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

PDFアイコンは、検索結果が非常に大きいPDFファイルにリンクしていることを顧客が知るのに役立ちます。 モデム経由でWebサイトにアクセスしている顧客やモバイルデバイスからアクセスしている顧客にとって、ファイルサイズは重要です。

## 検索結果をPDFファイルの特定のページにリンクさせることはできますか。 {#section_A06E7F7017E6441E98209D288EE57BF6}

はい。顧客は、スマートリンクテンプレートタ `<search-smart-link>...</search-smart-link>`グ()を使用して、検索結果を含む最初のPDFページをクリックして開くことができます。

スマートリンクを使用するには、テンプレ `<search-link>...</search-link>` ートの検索結果セクションにあるタグをタグで置き換 `<search-smart-link>...</search-smart-link>` えます。 顧客がスマートリンクタグで生成されたリンクをクリックすると、検索クエリに関連する最初のPDFページに移動します。

>[!NOTE]
>
>この機能を使用するには、最新バージョンのAdobe AcrobatまたはAdobe Acrobat Readerを使用する必要があります。このバージョンには、ハイライトプラグインと外部ウィンドウハンドラー(EWH)プラグインが含まれている必要があります。 また、WebブラウザーでNetscape Navigator用のAdobe Acrobatプラグイン（このNetscape Navigatorプラグインを使用できる任意のブラウザー）またはInternet Explorer 4.0以降用のAcrobat ActiveXコントロールを使用する必要があります。

詳しくは、検 [索テンプレートタグを参照してくださ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)い。

## PDFファイルのインデックスがWebサイト上で作成されないようにするにはどうすればよいですか。 {#section_96671419A822486AAC654D8DAD819940}

検索ロボットでPDFファイルのクロールとインデックス作成を行わない場合は、コンテンツタイプ(// **[!UICONTROL PDF Documents]** )の選択を解除 **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;します。

を使用してPDFインデックスを無効にす [!DNL URL Masks] ることもできます。

詳しくは、 [URLマスクをインデックスに追加する、またはインデックス部分に追加しないを参照してください。](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

PDFインデックスを無効にするには、次のURLマスクのいずれかを入力します。

* `exclude *.pdf` （正規表現を使用していない場合）
* `exclude regexp ^.*\.pdf$` （正規表現を使用している場合）

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

## Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。 {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

サイト検索/マーチャンダイジングは、言語を示さないPDFファイルからUTF-8を取得します。 コンテンツタイプ(// **[!UICONTROL PDF Documents]** )を選択した場合は、メタデー **[!UICONTROL Settings]****[!UICONTROL Crawling]****[!UICONTROL Content Types]**&#x200B;タインジェクションを使用して、PDFファイルで使用する言語を指定する必要があります。

フィールド [挿入定義の追加を参照してくださ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)い。

## ページ数が多すぎます {#reference_48A748BC1ED14844ACAC2735C8388E8A}

インデクサーが実際より多くのページをカウントした理由と、各ケースでの解決策について説明する、よくある質問ページです。

貴社のWebサイトがページ数の上限を下回っていると確信しているが、インデクサーが上限に達したと伝えている場合は、考えられる解決策に関して、次のよくある質問と回答を確認する必要があります。

* [様々なインデックスログを調べましたか。](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [CGIプログラムのインデックスはWebサイト上で作成されていますか。](#section_86ED8A641B3841EC80153B4F107548FD)
* [サーバーでディレクトリの参照が有効になっているか。](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Webサイトにフォーラムやニュースグループはありますか。](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [WebサイトにPDFまたはMicrosoft Officeファイルがあるか…](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [複数のURLエントリポイントがあるか。](#section_8C54AFD7DF56472A9364D516482B534C)
* [内部バイト数または時間制限を超えた場合…](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## 様々なインデックスログを調べましたか。 {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

インデックスログには、Webサイトのインデックスを作成する際にサイト検索/マーチャンダイジングロボットによって収集された詳細な情報が含まれます。 ログには、クロールされたすべてのリンクと発生したエラーの一覧が含まれます。 インデックスを作成するページを判断する際は、インデックスログを調べるのが最適な場所です。

ライブま [たはステージングされた完全なインデックスログの表示を参照してください。](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

ライブま [たはステージングされたインデックスの増分ログの表示を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

詳しくは、 [ライブのスクリプト化された増分インデックスログの表示または…を参照してください。](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

ライブま [たはステージングされたインデックスログの再生成の表示を参照してください。](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

詳しくは、 [ライブまたはステージングされたWebサイトの再ランク付けインデックスログの表示を参照してくださ](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D)い。

## CGIプログラムのインデックスはWebサイト上で作成されていますか。 {#section_86ED8A641B3841EC80153B4F107548FD}

CGIプログラムはURLパラメータを使用し、インデクサが複数の「偽の」URLをクロールする場合があります。 サイト検索/マーチャンダイジングがCGIプログラムを読み取り、CGIパラメータを含むURLに従う場合、検索インデックスに役に立たないページの数倍がクロールされ、インデックスが作成されている可能性があります。 一般的なCGIパラメーターは、URLの中でまたは文字で `?` 表示さ `&` れます。

URLマスク機能を使用して、CGIプログラムのインデックスが作成されないようにマスクできます。 URLプレフィックスをマスクしたり、正規表現を使用してCGIスクリプトをマスクしたりできます。

URLマスクに [ついてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)い。

URLマスクス [クリプトについてを参照してくださ](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)い。

正規表 [現を参照](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)。

## サーバーでディレクトリの参照が有効になっているか。 {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Webサーバーでディレクトリの参照が有効になっていて、特定のディレクトリにindex.htmlファイルが存在しない場合、そのディレクトリへのアクセスによって、そのディレクトリ内のファイルの一覧が表示されます。 通常、ページの上部にはリンクがあり、クリック、クリックなどを使用してリストを様々な方法で並べ替 **[!UICONTROL Name]**&#x200B;え **[!UICONTROL Last modified]**&#x200B;るこ **[!UICONTROL Size]**&#x200B;とができます。 通常、これらは、末尾などの文字を含むURLとしてサイト検索/マーチャンダイジングのインデックスログ `?M=A` に表示されます。 サイト検索/マーチャンダイジングのインデクサーはリンクとしてこれらに従うので、複数の「偽の」URLのインデックスを作成する可能性があります。

通常、適切に設計されたWebサイトでは、すべてのディレクトリにインデックスファイルが存在するか、インデックスファイルのないディレクトリのディレクトリ参照が無効になっています。 幸い、サーバー側でページを変更したり、ディレクトリリストを無効にしたりできない場合は、これらの「偽の」URLを隠す簡単な方法があります。

このタスクを実行するには、//をク **[!UICONTROL Settings]** リック **[!UICONTROL Crawling]** しま **[!UICONTROL URL Masks]**&#x200B;す。 その文字を含むURLをマスクするマスクを追加しま `?`す。 このタスクは、次の正規表現マスクを入力することで実行できます。

`exclude regexp ^.*\?.*$`

マスクを作成した後は、必ずWebサイトのインデックスを再作成してください。

ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Webサイトにフォーラムやニュースグループはありますか。 {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Webサイト上でフォーラムまたはニュースグループをクロールする場合、異なる表示オプションや並べ替えオプションのURLをフォローしている可能性があります。 この動作は、同じページのインデックスが複数回作成されることを意味します。

通常、フォーラムやニュースグループには独自の検索エンジンが付属しています。 この場合、を使用して、サイト検索/マーチ [!DNL URL Masks] ャンダイジングのフォーラムをマスクできます。

製品メニューで//をクリ **[!UICONTROL Settings]** ックし **[!UICONTROL Crawling]** ます **[!UICONTROL URL Masks]**。 ページで、URL [!DNL Staged URL Masks] を「URLマスクを除外」として入力し、フォーラムをマスクします。

詳しくは、 [URLマスクをインデックスに追加する、またはインデックス部分に追加しないを参照してください。](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

マスクを作成したら、必ずWebサイトのインデックスを再作成してください。

ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

ライブま [たはステージングされたWebサイトの増分インデックスの実行を参照してください。](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## WebサイトにPDFファイルまたはMicrosoft Officeファイルがあるか。 {#section_455FC5438DF74E68AB9A31D359EAD4D9}

WebサイトにPDFファイルまたはフ [!DNL Microsoft Office] ァイルがある場合、少数のファイルのインデックスサイズでは多数のページがカウントされることがあります。 PDFまたはMicrosoft Officeファイルの各ページが別のページとしてカウントされるので、ドキュメントよりもページのインデックスが作成されるページの方が多いのです。

製品メニューで//をクリ **[!UICONTROL Index]** ックし **[!UICONTROL Full Index]** ます **[!UICONTROL Live Index]**。 ページ上 [!DNL Full Index] でを選択し、 **[!UICONTROL Count All Pages]**&#x200B;をクリックして、合 **[!UICONTROL Full Index Now]** 計ページ数を表示します。 PDFファイルやMicrosoft Officeファイルのインデックスを作成しない場合は、/からこのコンテンツタイプを無効にす **[!UICONTROL Settings]** ることが **[!UICONTROL Crawling]** できま **[!UICONTROL Content Types]**&#x200B;す。

ライブま [たはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

コンテンツタ [イプについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)い。

## 複数のURLエントリポイントがあるか。 {#section_8C54AFD7DF56472A9364D516482B534C}

サイト検索/マーチャンダイジングロボットは、指定されたURLエントリポイントからクロールを開始し、見つかったすべてのリンクをその特定のドメイン内のすべてのコンテンツにたどります。 URLエントリポイントを多く指定した場合、大量のページがクロールされる可能性があります。

次の手順で、追加のドメインのエン `nofollow` トリポイントドキュメントのヘッダーにRobots Exclusion Protocolのタグを使用します。

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

上記のコードは、サイト検索/マーチャンダイジングロボットに対し、ページのコンテンツのインデックスを作成するが、追加のページへのリンクをたどらないように指示しています。

WebロボットとRobots Exclusion Protocolの詳細については、以下を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

追加のドメインのページのソースにアクセスできない場合は、複数のURLエントリポイントを削除できます。 これにより、顧客が検索できるコンテンツを持つドメインに対してのみ、インデックス作成アクティビティを制限できます。

URL入力ポイ [ントについてを参照してくださ](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)い。

## サイト検索/マーチャンダイジングの内部バイト数または時間制限を超えたか。 {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

アカウントが[フルインデックスステータス]画面の上限に達したかどうかを確認します。 インデックスが許可されているサイズを超えている、または許可されている時間を超えているとステータスレポートに表示される場合、Webサイトのインデックスは完全には作成されません。 このエラーを修正して、Webサイトのページを適切にカバーし、数えることができます。

サイト検索/マーチャンダイジングサーバを保護するため、バイトと時間には内部的な制限があります。 クロールされたファイルのサイズが非常に大きい場合、またはサイト検索/マーチャンダイジングが到達しようとするサーバーの速度が遅い場合にのみ、これらの制限に達します。

制限時間に達した場合は、サーバーがオンラインであることを確認し、後でインデックスを再試行します。 バイト数の制限に達した場合は、インデックスログを参照して、クロールされたファイルを確認します。 異常に大きい？ 次のいずれかのメッセージが表示された場合は、テクニカルサポートにお問い合わせください。
