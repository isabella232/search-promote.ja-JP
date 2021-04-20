---
description: Search&amp;Promoteに関するよくある質問を読みます。
solution: Target
title: よくある質問
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '8648'
ht-degree: 0%

---


# よくある質問{#frequently-asked-questions}

## AdobeFlash{#reference_4A25BBDE32214AF5A1A454F38FD51243}

Webサイト上のSWFファイルのインデックス作成と検索のサポートについて説明する、よくある質問ページです。

SWFファイルに関してよく寄せられる質問は、次のとおりです。

* [SWFファイルはいつクロールされ、インデックス化されますか？](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [SWFのインデックスを作成するには、何をする必要がありますか。](#section_0A6A52CC70D4495BBE14D91906318F95)
* [SWFファイルはどのように認識されますか。](#section_B36C0536AB544F509601DC6A11A8E656)
* [SWFファイルのインデックスの作成方法](#section_36856058A4B54FA5ABF921344F50410C)
* [SWFファイルは1ページと見なされますか。](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [個々のSWFファイルのインデックス付けを防ぐ方法](#section_E38AD37989EF410B97AF5125057BFD22)
* [SWFファイルのインデックスが作成されないようにする方法](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## SWFファイルはいつクロールされ、インデックス化されますか？{#section_01BB5259140D4D5FB04CCB7A1A63DE99}

次の例のように、HTMLページ上のembedまたはobjectタグに含まれるSWFファイルは、クロールされ、インデックス化されます。

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

ファイルURLをエントリポイントとしてリストした場合も、SWFファイルが認識されます。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## SWFファイルのインデックスを作成するには、何をする必要がありますか。{#section_0A6A52CC70D4495BBE14D91906318F95}

SWFファイルをクロールしてインデックスを作成するには、コンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択します。

FlashファイルがHTMLドキュメント内の`<embed>`タグまたは`<object>`タグから参照されている限り、テキストのインデックスが作成され、ファイルに一覧表示されているすべてのURLがクロールされます。

ファイルが`<embed>`タグまたは`<object>`タグから参照されていない場合は、SWFファイルをHTMLドキュメントの`<a href=...>`タグまたはURLエントリポイントとしてリストできます。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## SWFファイルはどのように認識されますか。{#section_B36C0536AB544F509601DC6A11A8E656}

SWFファイルは、次のMIMEタイプで識別されます。

`application/x-shockwave-flash`

また、ファイル拡張子が.swfである場合、SWFファイルは`application/octet-stream`&quot;または`text/plain` MIMEタイプでも認識されます。

サーバーの設定が正しくない場合、SWFファイルに異なるMIMEタイプが使用されている可能性があります。 SWFファイルのクロールおよびインデックス付けに問題がある場合は、サーバー設定を確認してください。

## SWFファイルのインデックスの作成方法{#section_36856058A4B54FA5ABF921344F50410C}

SWFファイル内のテキストは、含まれるHTMLページ内の`<body>`テキストと同じようにインデックス化されます。 埋め込みSWFファイル内のテキストが検索結果によって見つかった場合、結果は、SWFファイルではなく、含まれるHTMLページに実際にリンクされます。 これにより、SWFファイルは正しいコンテキストで表示されます。

SWFファイルに「ムービーの読み込み」アクションとしてURLが含まれている場合、参照先のSWFファイル内のテキストのインデックスは、含まれるHTMLページの一部として作成されます。

SWFファイルに「URLの取得」アクションとしてURLが含まれている場合、HTML `<a href=...>`参照がクロールされ、後でインデックス付けされるのと同じように、URLはクロールされ、後でインデックス付けされます。

SWFファイルがURLエントリポイントとしてリストされている場合、SWFファイルのテキストのインデックスは1つのページとして作成されます。 エントリポイントSWFからテキストを検索した結果は、含まれるHTMLページではなく、ムービーに直接リンクします。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## SWFファイルは1ページと見なされますか。{#section_0158D6DE70BC40D78E2374787B9F58AB}

いいえ。SWFファイルは、含まれるHTMLページの一部と見なされます。 SWFファイルに含まれるすべての「ムービーを読み込み」URLも、含まれるHTMLページの一部と見なされます。 したがって、HTMLページから参照されるSWFファイルは、アカウントのページ合計の「ページ」としてカウントされません。

SWFファイルがURLエントリポイントとしてリストされている場合、そのSWFファイルと、そのSWFファイルにリストされているすべての「ムービーを読み込む」URLが、アカウントのページ合計で1つの「ページ」としてカウントされます。

## 個々のSWFファイルのインデックス付けを防ぐ方法を教えてください。{#section_E38AD37989EF410B97AF5125057BFD22}

SWFファイルのインデックスが作成されないようにするには、含まれるHTMLドキュメントにrobotsのmetaタグ(`<meta name="ROBOTS" content="NOINDEX">`)または`<noindex>`タグを追加します。 つまり、`<embed>`タグまたは`<object>`タグを含むドキュメントです。

また、robots metaタグ(`<meta name="ROBOTS" content="NOFOLLOW">`)を使用して、SWFファイルに含まれる次のURLを防ぐこともできます。 含まれるHTMLドキュメントが次のように無効になっている場合、SWFファイルで「Get URL」アクションとしてリストされているURLは実行されません。

## SWFファイルのインデックスがWebサイトで作成されないようにする方法を教えてください。{#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

SWFインデックスを無効にするには、コンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)の選択を解除します。

[!DNL URL Masks]を使用してSWFファイルのインデックスを無効にすることもできます。

[インデックス部分へのURLマスクの追加を参照してください…](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

SWFインデックスを無効にするには、次のURLマスクのいずれかを入力します。

* `exclude *.swf` (正規式を使用しない場合)
* `exclude regexp ^.*\.swf$` (正規式を使用している場合)

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

## Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。{#section_EE1A3A705AE74148BD195A0CE513A5C4}

サイト検索/マーチャンダイジングは、AdobeFlashで作成されたSWFファイルからUTF-8を取得します。 UTF-8には、言語の表示は含まれません。 コンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する言語を指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

古いSWFファイルでも文字セットが指定されていません。 SWFコンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する文字セットを指定する必要があります。

## 一般検索{#reference_E2C675162789452A9B99C6633B12CBEF}

サイト検索/マーチャンダイジングが、Webサイトを訪問する顧客がどのようにして探しているものを見つけるかを支援するかを説明する、よくある質問ページです。

一般検索に関するよくある質問は次のとおりです。

* [サイトを使用するには、ソフトウェアをインストールする必要があるか…](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [サイトがページ数の上限を超えるとどうなりますか。](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [週単位の電子メールアドレスを変更する方法を教えてください。](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [サイト検索/マーチャンダイジングに関する顧客情報はどの程度安全ですか。](#section_5484CB954167412BB7F0480CB0C504B8)
* [顧客情報のプライバシーについて教えてください。](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [自分のバナー広告を検索に表示できますか。](#section_611EB8B32C16418386CB7DC7FB6954B8)

検索機能に関してよく寄せられる質問は次のとおりです。

* [サイトの検索結果をカスタマイズできますか。](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [お客様が検索している情報を確認できますか。](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [どのコンテンツタイプ(PDF、テキスト、Flash、MP3、Microsoft Office)のインデックスを作成し、検索するかを制御する方法を教えてください。](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [ASP、JSP、PHP、CFM、またはPerlベースのコンテンツを使用して動的に生成されるWebページはサポートされていますか。](#section_E279F004F1C542A2B9773B832E7B013F)
* [同義語を使用して検索結果を改善する方法](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [検索結果の順序を管理できるか](#section_C6361048502745779D9749A842C4C370)
* [検索結果ページの言語を変更できますか。](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Adobeに複数のサイトを設定できるか…](#section_AFA8825182094660A71EEC84B8329D6D)
* [複数のドメインを検索できますか。](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [サイトを個別のセクションに細分化して](#section_52153A9DE9F9493B967A70583848B2A4)
* [Webサイトの一部を除外する方法を教えてください。](#section_D452EDE153654EF398F4A87780C6D43B)
* [サポートされる文字セットは何ですか。](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [Webサイトを変更または更新した場合はどうなりますか。](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [サイトのインデックスを自動的に作成できますか。](#section_9C7D41636238488691ECDFEE4D4E5103)
* [私は自分のウェブサイトでパスワードを使う。引き続きサイト検索/マーチャンダイジングを使用できますか？](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [httpsのクロールおよびインデックス作成をサポートしているか、または…](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [サイト検索/マーチャンダイジングは、Webサイトのrobots.txtファイルに従いますか。](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Webサイトの一部は頻繁に更新する必要があるので、](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [スクリプトまたはプログラムを使用して増分を開始できますか…](#section_0B6BB039557A42AA876D35D748E17DD0)

## サイト検索/マーチャンダイジングを使用するには、ソフトウェアをインストールする必要がありますか。{#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

いいえ。これは、サイト検索/マーチャンダイジングの主な利点です。 エンジンは、プロ仕様のアプリケーションで、当社の高パフォーマンスサーバー上でのみホストされ、保守されます。 これにより、他の検索ソリューションよりも使いやすくなります。 必要なのは、Webサイトの顧客が検索に参加できるように、ページに少量のHTMLコードを追加することだけです。 サイト検索/マーチャンダイジングは残りすべてを処理します。

## サイトがページ数の上限を超えるとどうなりますか。{#section_ECA5FA01032D4322BABA4E2C7FE498C1}

お客様のサイトを訪問者が中断することなく検索できるように、お客様の検索サービスを提供し続けています。 Webサイトがページ数の上限を超えているかどうかを確認するには、完全なインデックスのステータスまたはライブログを確認します。

[完全なインデックスについて](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3)を参照してください。

[ライブまたはステージングされた完全なインデックスログの表示を参照してください…](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## 週別レポートの送信先の電子メールアドレスを変更する方法を教えてください。{#section_AE27F63DD13F425B940C8E7D9ED5C614}

毎週のレポートは、アクティブな各アカウントの所有者に送信されます。 電子メールアドレスは、**[!UICONTROL Settings]**/**[!UICONTROL My Profile]**/**[!UICONTROL Personal Information]**&#x200B;をクリックして変更できます。 複数のアクティブな検索アカウントがある場合は、すべてのニュースレターが新しいアドレスに送信されます。

[個人ユーザー情報の設定](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)を参照してください。

## サイト検索/マーチャンダイジングに関する顧客情報はどの程度安全ですか。{#section_5484CB954167412BB7F0480CB0C504B8}

サイト検索/マーチャンダイジングは、安全で、迅速、安定していて、使いやすいものです。 Cookieを（必要に応じて）使用してアドビの製品を使用するように強制されることはありません。また、パスワードなどの機密情報は、後でブラウザーから取得できるURLリンクに置かれません。

## 顧客情報のプライバシーについて教えてください。{#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobeは、お客様と訪問者のプライバシーを守ることに取り組んでいます。 Adobe[プライバシーセンター](https://www.adobe.com/privacy.html)を参照してください。

## 検索結果ページに独自のバナー広告を表示できますか。{#section_611EB8B32C16418386CB7DC7FB6954B8}

はい。検索結果の外観とコンテンツを制御します。 Webサイトの検索結果テンプレート内に、LinkExchangeやSmartClicksなど、独自のバナー交換ネットワークへのリンクを作成できます。 訪問者が行ったヒットは、バナー交換アカウントに正しく配分されます。

## サイトの検索結果をカスタマイズできますか。{#section_A64B3A621B794DF78D35ED06D9C43D0B}

はい。これは、サイト検索/マーチャンダイジング専用の機能です。 アドビの高度なテンプレート技術とHTMLに関する知識が少ないので、検索結果の表示方法を正確に制御できます。

[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

自社のサーバーとSite Search/Merchandisingサーバーのトランジションは、お客様にとって完全にシームレスで目に見えないものです。 HTMLがわからない場合や、カスタムテンプレートを作成する時間がない場合は、AdobeのプロフェッショナルなWeb開発者の社内チームが作成する、魅力的で使いやすい様々なテンプレートから選択できます。

## サイトで検索している顧客を確認できますか。{#section_73709E1B0E82478DA7B4D15B6C845F33}

はい。過去2か月間、Webサイト上の訪問者が検索した場合の検索統計を保持します。 これらの統計は、製品メニューの「レポート」でいつでも確認できます。 検索レポートは、Webサイトで訪問者が何を探しているかに関する重要な情報を提供します。 この情報を使用して、デザインを改善したり、サイト検索/マーチャンダイジングエンジンを調整して訪問者に適したサービスを提供したりできます。

## どのコンテンツタイプ(PDF、テキスト、Flash、MP3、Microsoft Office)のインデックスを作成し、検索するかを制御する方法を教えてください。{#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

PDFドキュメント、プレーンテキストドキュメント、Flashムービー、MP3ファイル、またはMicrosoft Officeドキュメント内のテキストのインデックス作成と検索を有効または無効にするように、アカウントを簡単に設定できます。

これらの設定は[!DNL Staged Content Types]ページで制御されます。

「[コンテンツタイプについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)」を参照してください。

## ASP、JSP、PHP、CFM、またはPerlベースのコンテンツを使用して動的に生成されるWebページはサポートされていますか。{#section_E279F004F1C542A2B9773B832E7B013F}

静的または動的に生成されるHTML Webページのインデックスは、データベースから作成されたページやその他のバックエンドプロセスを含めて作成されます。 ブラウザーに表示されるHTMLコードはインデックス付けされているので、これらのバックエンドアーキテクチャがHTMLページに結果をもたらす限り、WebサイトでSite Search/Merchandisingを使用できます。

検索ロボットは、[!DNL Account Settings]で指定されたWebサイトアドレスの最初のページから始めてWebサイトをクロールし、ページ間のリンクをたどります。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

検索ロボットがWebサイトのすべてのページをクロールしてインデックスを作成すると、検索エンジンを使用してサイトを検索できます。 つまり、動的に生成されたドキュメントが他のページのリンクと共にWebサイトに組み込まれている場合でも、検索ロボットは動的なコンテンツをクロールしてインデックスを付けることができます。

Webサイトコンテンツのクロールおよびインデックス作成が完了すると、Webサイトのユーザーは、インデックス作成されたコンテンツ内の情報を検索できます。

## 同義語を使用してサイトの検索結果を改善する方法を教えてください。{#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

訪問者が検索クエリに関連するページを見つける場合は、同義語を使用できます。

例えば、サイトで販売する商品の価格リストを含むページがあるとします。 ただし、サイト検索/マーチャンダイジングによって提供される検索レポートを調べると、顧客の検索内で「コスト」、「費用」、「料金」、「有料」という語が必要になることがわかります。 これらの単語は、検索結果に価格リストページを表示しません。 [!DNL Dictionaries]の[!DNL Add Synonyms]機能を使用すると、これらの語句をすべて同義語として指定でき、顧客は、どの検索語句を使用しているかに関係なく、価格のリストを見つけることができます。

[辞書](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034)についてを参照してください。

## 検索結果の順序を管理できますか。{#section_C6361048502745779D9749A842C4C370}

はい。高度な関連性インターフェースを使用すると、特定の検索クエリに対して返されるページを制御できます。 この機能は、顧客が特定の単語をクエリしたときに特定のページを確実に表示したい場合に役立ちます。

「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」を参照してください。

## 検索結果ページの言語を変更できますか。{#section_6EE41DA8241247D48BBEB061A50599C5}

はい。サイト検索/マーチャンダイジングテンプレートは、選択した言語を使用し、Webサイトの外観に合わせた結果ページを作成できるという点で柔軟性があります。

テンプレートは、テキスト、標準のHTMLタグ、および検索結果を表示するために定義された特別なタグの組み合わせで構成されます。 顧客が検索を行うと、検索ロボットはテンプレートを読み、標準のHTMLタグを使用してテキストを出力し、特殊なテンプレートタグに基づいて結果のリンクを挿入します。

[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

結果の言語を変更する場合は、テンプレートに表示される英語のテキストを編集できます。

「[プレゼンテーションまたはトランスポートテンプレートの編集](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)」を参照してください。

## Adobeのお客様ログインに複数のサイトを設定できますか。{#section_AFA8825182094660A71EEC84B8329D6D}

はい。1人のAdobeの顧客ログインを使用して、様々なWebサイトに対して異なる検索エンジンを管理できます。 「アカウント」の下のアカウントを選択して管理します。

「[使用する別のアカウントの選択](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26)」を参照してください。

## 複数のドメインを検索できますか。{#section_BFBB0E9861D942F095B56CF0A8F16596}

はい。[!DNL URL Entrypoints]を使用して、複数のドメインへのアクセスを設定できます。 自分が所有する追加のドメインのURL入力ポイントを指定します。 所有していないドメインのインデックスを作成する権限が必要です。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

## サイトを個別のセクションに細分して、顧客がこれらの領域のいずれかを個別に検索できるようにするか、またはサイト全体を検索できるようにするか。{#section_52153A9DE9F9493B967A70583848B2A4}

はい。「コレクション」機能が追加され、Webサイトの特定の領域を検索して、探しているものをすばやく見つけることができます。

[コレクションについて](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127)を参照してください。

例えば、製品の販売情報に関連するURLのコレクションや、サポートサービスに関連するURLのコレクションを検索できます。 コレクションを設定すると、ユーザーに対して、コレクションのドロップダウンリストまたはチェックボックスのグループが表示されます。

## Webサイトの一部を検索対象から除外する方法を教えてください。{#section_D452EDE153654EF398F4A87780C6D43B}

はい。URLマスクを指定して、インデックス作成に含める、または除外するWebサイトページを決定します。 URLマスクは、Webサイトのページを検索結果に表示するかどうかを決定します。

[URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

[URLマスクスクリプトについて](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)を参照してください。

個々のWebページの一部が検索されないようにするために、ページの一部をインデックス付けから除外できます。 テキストを`<noindex>`タグと`</noindex>`タグで囲みます。 このメソッドは、検索からナビゲーションテキストを除外する場合に役立ちます。

## サポートされる文字セットは何ですか。{#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

Webページでは、通常、次のようなメタタグを使用して文字セットを指定します。

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

サイト検索/マーチャンダイジングエンジンは、今日インターネットで使用されているすべての一般的な文字セットを使用して、Webページのインデックスを適切に作成します。 次の文字セットがサポートされています。

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>アラビア語(ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>中国語(繁体字；Big5) </p> </td> 
   <td colname="col3"> <p>日本語(Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アラビア語(Windows-1256) </p> </td> 
   <td colname="col2"> <p>中国語(繁体字；EUC-TW) </p> </td> 
   <td colname="col3"> <p>ロシア語(KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バルト語(ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>キリル言語(ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>南ヨーロッパ語(ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>バルト語(Windows-1257) </p> </td> 
   <td colname="col2"> <p>キリル語(Windows-1251) </p> </td> 
   <td colname="col3"> <p>トルコ語(ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中央ヨーロッパ語(ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>ギリシャ語(ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>トルコ語(Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中央ヨーロッパ語(Windows-1250) </p> </td> 
   <td colname="col2"> <p>ギリシャ語(Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode(UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>ヘブライ語(ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII(us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>ヘブライ語(Windows-1255) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ語(ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体；EUC-CN) </p> </td> 
   <td colname="col2"> <p>日本語(EUC-JP) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ語(ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体；GB2312) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ語(Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体；GBK) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>西ヨーロッパ語(x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>中国語(簡体；HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>日本語(ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

上記に記載されていない文字セットについては、テクニカルサポートにお問い合わせください。

## Webサイトを変更または更新した場合はどうなりますか。{#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Webサイトのコンテンツを変更した後、フルインデックスまたはインクリメンタルインデックスを実行できます。 Site search/merchandisingは、変更されたWebサイトのコンテンツをダウンロードし、インデックスを作成します。 インデックス作成が完了すると、ユーザーは新しいコンテンツを検索できます。 また、特定の時間と特定の日にサイトの自動インデックスをスケジュールすることもできます。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

「[ライブWebサイトのフルインデックススケジュールの設定](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)」を参照してください。

「[ライブWebサイトの増分インデックススケジュールの設定](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)」を参照してください。

## サイトのインデックスを自動的に作成できますか。{#section_9C7D41636238488691ECDFEE4D4E5103}

はい。サイトの自動インデックスを毎日スケジュールできます。

毎日の自動インデックス作成の他に、サイトの一部を頻繁に変更する場合に、インデックスを増分的に作成するように選択できます。 自動インデックスがスケジュールされている日には、インデックスの実行時刻を制御できます。 また、必要に応じていつでも手動でサイトインデックスを開始できます。

「[ライブWebサイトのフルインデックススケジュールの設定](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)」を参照してください。

「[ライブWebサイトの増分インデックススケジュールの設定](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)」を参照してください。

## 私は自分のウェブサイトでパスワードを使う。 引き続きサイト検索/マーチャンダイジングを使用できますか。{#section_4618EB5B66704640B5502D1B5CB4B32E}

HTTP基本認証を使用してWebサイトの特定の部分をパスワードで保護する場合、Site Search/Merchandisingでサイトのインデックスを作成する際に使用できる領域とパスワードを指定できます。

[Webサイトの必要な領域にアクセスするためのパスワードの追加を参照してください…](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## httpsまたはセキュアサーバーコンテンツのクロールおよびインデックス作成をサポートしていますか？{#section_D5BB8B8FBEA4405583E86B4AEC37151B}

はい。安全なサーバー(https)上のコンテンツをクロールしてインデックスを作成できます。

## サイト検索/マーチャンダイジングは、Webサイトのrobots.txtファイルに従いますか。{#section_73BBF6FE93C64C109F45CBC2FA394DB2}

はい。ロボット排他プロトコルは準拠しています。 検索ロボットは、robots.txtファイルがWebサイトに存在する場合、そのファイルを調べます。 robots.txtファイルで、サイトのクロールからすべてのロボットが除外される場合、サイト検索/マーチャンダイジングロボットも除外されます。 サイト検索/マーチャンダイジングロボットのみがサイトをクロールできるようにするには、robots.txtファイルの内容を次のように設定します。

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

WebロボットとRobots Exclusion Protocolについて詳しくは、次を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## 顧客が最も正確な検索結果を得られるように、Webサイトの特定の部分は頻繁に更新する必要があります。 増分インデックスはこの問題に役立ちますか？{#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

はい。このシナリオは、サイト検索とマーチャンダイジングを容易にするためにインクリメンタルインデックス機能が構築されたものです。 増分インデックスの主な利点は、会社がWebサイト内で動的に変化する部分に頻繁にインデックスを作成できる点です。 この機能により、「最大1分間」の精度で検索結果が表示されます。

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

「[ライブWebサイトの増分インデックススケジュールの設定](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)」を参照してください。

## 動的に生成されるWebページは、製品カタログや在庫管理システムなどのバックエンドデータベースでサポートされていますか。{#section_26896C556483457E879785E751583B16}

静的または動的に生成されるHTML Webページ。データベースから作成されたページや、その他のバックエンドプロセスのインデックスが作成されます。 ブラウザーが閲覧するHTMLコードのインデックスが作成されるので、バックエンドのデータベース情報がHTMLページに結果を出す限り、Webサイトでの検索とマーチャンダイジングを使用できます。

検索ロボットは、[!DNL Account Settings]で指定されたWebサイトアドレスの最初のページから始めてWebサイトをクロールし、ページ間のリンクをたどります。

「[アカウント設定の指定](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)」を参照してください。

検索ロボットがWebサイトのすべてのページをクロールしてインデックスを作成すると、検索エンジンを使用してサイトを検索できます。 つまり、動的に生成されたドキュメントが他のページのリンクと共にWebサイトに組み込まれている場合、検索ロボットは動的データベースコンテンツのクロールやインデックス付けを引き続き行うことができます。

Webサイトコンテンツのクロールおよびインデックス作成が完了すると、Webサイトのユーザーは、インデックス作成されたコンテンツ内の情報を検索できます。

タイトル、メタ説明、メタドキュメントタグ、メタキーワード情報タグのいずれかまたはすべてに限定された、フルコンテンツ検索や、より狭いトピックベースの検索を簡単に有効にできます。 メタデータ定義を使用して、実際の検索結果に製品の画像などのカスタム表示フィールドを作成することもできます。

「[新しいmetaタグフィールドの追加](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)」を参照してください。

## スクリプトまたはプログラムを使用してサイトのインクリメンタルインデックスを開始できますか。{#section_0B6BB039557A42AA876D35D748E17DD0}

はい。スクリプトやプログラムを使用してWebサイトの増分インデックスを開始したり、サーバーにpingを送信してコンテンツが変更または更新されるたびにサイトのインデックスを作成したりできます。

「[スクリプトインデックスについて](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)」を参照してください。

## 機能の実装{#reference_2D0C4A80B8D64051BA9694D562DCE663}

[!DNL Search&Promote]での様々な機能の実装について説明する、よくある質問ページです。

Webサイトでの[!DNL Search&Promote]での機能の実装に関して、次のよくある質問があります。

* [ビジネスルールが実行されないのはなぜですか。](#section_7FEB60383D8A4B11A60DFF9067274699)
* [インデックスのスケジュール設定、インデックスの開始中にエラーが発生し、ステージングされたインデックスの開始中に問題が発生するのはなぜですか。](#section_E05758193DF5436784B0145839989F75)
* [インデックスサイズの制限が許可された境界を超えています。この問題が起こるのはなぜですか？](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## ビジネスルールが実行されないのはなぜですか。{#section_7FEB60383D8A4B11A60DFF9067274699}

バナーを表示する場合はビジネスルールを設定し、表示する結果と表示順序を決定する場合はビジネスルールを設定します。 また、ファセット内の項目の位置、および特定の検索に使用するテンプレートを設定することもできます。
ビジネスルールの順序を変更して、プレゼンテーションテンプレートで実行する順序を変更します。 ビジネスルールは、定義された順に実行されます。つまり、ルールの注文番号が高いほど、後でプロセス内で実行され、以前のルールが切り捨てられます。 ルールの順序を変更するには、「ビジネスルール」ページの表の「順序」列に新しい番号を入力します。

[ビジネスルールについて](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)を参照してください。

## インデックスのスケジュール設定、インデックスの開始中にエラーが発生し、ステージングされたインデックスの開始中に問題が発生するのはなぜですか？{#section_E05758193DF5436784B0145839989F75}

インデックスを生成するとき、インデックスがいっぱいか増分かに関係なく、インデックスクロールの状態情報がリアルタイムで表示されます。 例えば、開始時間、経過時間、およびインデックス作成プロセス中に発生したエラーを表示できます。 最後のインデックスの状態に関する情報も表示されます。 この情報を使用して、インデックスエラーが発生した場合のトラブルシューティングを行います。

インデックスのスケジュールについては、「[ライブWebサイトの完全なインデックススケジュールの設定](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)」および「[ライブWebサイトの増分インデックススケジュールの設定](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)」を参照してください。

ステージングされたインデックスの開始については、[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください。](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D)または[ライブまたはステージ化されたWebサイトの増分インデックスを実行中…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB)。

## インデックスサイズの制限が許可された境界を超えています。 この問題が発生する理由と修正方法{#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Webサイトは増加傾向にあり、時間の経過とともに、追加されたドキュメントやWebページがより多くSearch&amp;Promoteで「発見」されます。 最終的には、アカウントがインデックスサイズの制限を超える可能性があります。このような場合は、**[!UICONTROL URL Mask]**&#x200B;を使用することを検討してください。 この機能を使用すると、不要またはインデックス付けする必要のないインデックスクロールからドキュメントおよびWebページを非表示にし、インデックスサイズを小さくできます。 別の方法として、テクニカルサポートに連絡して、インデックスサイズの上限をアカウント内で大きく設定することもできます。

[URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

何をすべきか不明な場合は、テクニカルサポートにお問い合わせください。 インデックスサイズに影響を与える変数は他にも多数あり、調整するとアカウントの請求にも影響する場合があります。

## 国際{#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

中国語（簡体字および繁体字）、日本語、韓国語などのマルチバイトアジア言語を含む、19以上の言語のインデックス作成と検索のサポートについて、よくある質問のページです。

言語と文字セットに関するよくある質問は次のとおりです。

* [検索クエリの文字セットエンコーディングを制御するもの](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [エンコードが次のエンコードと一致する検索ページのみです。](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [検索結果ページに使用されるエンコーディング](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Unicode、UTF-8、エンコードされたページでサイト検索/マーチャンダイジングを使用できますか。](#section_130997CB08934A13A5261D85CF88040C)
* [Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。](#section_539AFF482F814D28B5929F683D2F2175)
* [Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。](#section_9C0849528AFF4C10AA97A2C912992638)
* [Webサイトで中国語、日本語、韓国語のMicrosoft Officeファイルを検索できないのはなぜですか。](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Webサイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [何か特別な事をしなきゃ…](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Netscape 4.7以前のバージョンで検索結果に中国語、日本語、韓国語のフォントが表示されるのはなぜですか。](#section_DF42567063304F918D406AC76529DFB7)

## 検索クエリの文字セットエンコーディングを制御するコントロール{#section_DF2E8570AFC2480FA199FD26C941A22F}

検索アカウントの「Web フォーム」セクションには、検索機能をWebサイトに追加するために使用するサンプルの検索フォームが含まれています。 この検索フォームコードを見ると、次のような行が見つかります。

`<input type=hidden name="sp_f" value="iso-8859-1">`

このコード行は、西ヨーロッパ言語の一般的なエンコードであるiso-8859-1で入力クエリがエンコードされていることを検索エンジンに知らせます。 この設定は、製品メニューに移動して&#x200B;**[!UICONTROL Settings]**/**[!UICONTROL My Profile]**/**[!UICONTROL Personal Information]**&#x200B;をクリックすると変更できます。 [!DNL Personal Information]ページの&#x200B;**[!UICONTROL Character Encoding]**&#x200B;ドロップリストで、新しいエンコーディングを選択します。

[個人ユーザー情報の設定](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)を参照してください。

検索フォームの`sp_f`行を編集して、Webページのエンコーディング値を手動で変更することもできます。 検索フォームの`sp_f`値は、表示されるページの文字セットエンコーディングと一致する必要があることに注意してください。

## エンコードが検索クエリのエンコードと一致するページのみが検索されますか。{#section_9E544F3DB7DE41618DC1BC8224B32C5A}

デフォルトではnoです。 Webサイトページが文字セットエンコーディングを正しく識別できる限り、ページで複数のエンコーディングが使用されている場合でも、検索クエリのエンコーディングとページのエンコーディングの間で必要な変換が行われます。

## 検索結果ページに使用されるエンコーディング{#section_DA68670F35D54EAABF7DBB010F4409BF}

アカウントの文字セットエンコーディングによって、結果テンプレートのデフォルトのエンコーディングが決まります。

[個人ユーザー情報の設定](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)を参照してください。

HTMLテンプレートで文字セットを指定する方法についても詳しく説明しています。

[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

## Unicode、UTF-8、エンコードされたページでサイト検索/マーチャンダイジングを使用できますか。{#section_130997CB08934A13A5261D85CF88040C}

はい。ただし、UTF-8などのUnicode文字セットは、ページに書き込まれる言語を判断するのに十分な情報を提供しません。 これらのページを正しく検索するには、言語を指定する必要があります。 ドキュメントの言語を決定するには、次の順序で情報を処理します。

* サーバーからドキュメント用に配信されるコンテンツ言語HTTPヘッダー。
* ドキュメントの`<HEAD>`セクションのMETA要素（例：`META HTTP-EQUIV="Content-Language" Content="ja_JP"`）。

* `<HTML>`タグのLANG属性（例：`<HTML LANG="ja_JP">`）。

サーバーがContent-Language HTTPヘッダーを配信するように設定されておらず、ドキュメントに言語のMETA要素も`<HTML>`タグのlanguage属性も含まれていない場合は、メタデータインジェクションを使用して適切な言語を指定できます。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。{#section_539AFF482F814D28B5929F683D2F2175}

サイト検索/マーチャンダイジングは、言語の表示のないAdobe PDFファイルからUTF-8を取得します。 **[!UICONTROL PDF Documents]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、PDFファイルで使用する言語を指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Webサイトで中国語、日本語、韓国語のSWFファイルを検索できないのはなぜですか。{#section_9C0849528AFF4C10AA97A2C912992638}

サイト検索/マーチャンダイジングは、言語を示さないAdobeFlashで作成されたAdobeFlashムービーファイルからUTF-8を取得します。 コンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する言語を指定する必要があります。

Flashバージョン4以前のSWFファイルでは、ファイル内の文字の文字セットは指定されません。 コンテンツタイプ&#x200B;**[!UICONTROL Adobe Flash Movies]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、SWFファイルで使用する文字セットを指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Webサイトで中国語、日本語、韓国語のMicrosoft Officeファイルを検索できないのはなぜですか。{#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

サイト検索/マーチャンダイジングは、言語を示さないMicrosoft Officeファイル（Microsoft Word、Microsoft Excel、およびMicrosoft PowerPoint）からUTF-8を取得します。 コンテンツタイプ&#x200B;**[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** )を選択した場合は、メタデータインジェクションを使用して、Microsoft Officeファイルで使用する言語を指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Webサイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。{#section_DB6D60CF46F94125BF4E54AF3036DBFC}

コンテンツタイプ&#x200B;**[!UICONTROL Text in MP3 Music Files]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、MP3ファイルのエンコードに使用する文字セットを指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Webサイトの.txtファイルのインデックスを正しく作成するために、特別な作業を行う必要がありますか。{#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

コンテンツタイプ&#x200B;**[!UICONTROL Text Documents]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、.txtファイルのエンコードに使用する文字セットを指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## Netscape 4.7以前のバージョンで検索結果に中国語、日本語、韓国語のフォントが表示されるのはなぜですか。{#section_DF42567063304F918D406AC76529DFB7}

アカウントで、デフォルトのテンプレート、使いやすいテンプレートの1つ、またはこれらのテンプレートに基づくテンプレートを使用する場合、フォント面としてArialまたはHelveticaを指定するフォントタグが含まれている可能性があります。 例： `<font face="arial, helvetica" size="+1">`Netscape 4.7以前では、ArialまたはHelveticaのフォントを使用すると、中国語、日本語、韓国語は表示されません。 `face`属性を削除するか、フォントを中国語、日本語、韓国語に適したフォントに置き換えます。

## 低ページ数{#reference_4344E3E3CB2948939860F8C078BD7773}

インデックス付けページ数が少ないことに関連する一般的な問題を説明する、よくある質問ページです。

インデックス付けページ数の少なさに関するよくある質問は次のとおりです。

* [インデックス・ログを調べたか？](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [URLに入力ミスがあるか。](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [エントリポイントWebページに他のページへのリンクがあるか](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [Webサイトの他のページへのリンクが埋め込まれている…](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Webページ上のHTMLタグが](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [HTMLコメントタグの形式が不適切な場合は、](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Webページに別のページへのリンクが含まれているか](#section_F8082759184049AAA8FA6342C1F84389)
* [URLに仮想ドメインサービスを使用しているか…](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Webページでメタ更新タグを使用しているか。](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Webページでメタロボットタグを使用しているか。](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Webサイトでロボットの除外ファイルを使用しているか。](#section_BF7B663347814F58AD736066C86B7D25)

## インデックス・ログを調べたか？{#section_D6626536DC3D40DDA4A1224F1CB276BF}

インデックスログには、サイト検索/マーチャンダイジングロボットがWebサイトのインデックスの作成時に収集する詳細情報が含まれます。 ログには、クロールされたリンクのリストが含まれ、発生したエラーが含まれます。 インデックスログを調べるのが、Webサイトのすべてのページのインデックスが作成されない理由を判断する開始に最適な場所です。

[ライブまたはステージングされた完全なインデックスログの表示を参照してください…](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

[ライブまたはステージングされたインクリメンタルインデックスログの表示を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## URLに入力ミスがあるか。{#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

長いURLをHTMLフォームに入力すると、誤字が1つ以上発生する場合があります。 URLにスペースを含めないでください。 また、一部のWebサーバーでは、URLを大文字と小文字が区別される方法で処理することに注意してください。

製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 [!DNL Staged URL Entrypoints]ページで、以下を確認します。

* URLに誤字はありません。
* URL内の文字はすべて正しい大文字と小文字を使用しています。
* URLにスペース文字は含まれません。

URLの入力ポイントをテストするには、URLをコピーしてWebブラウザーに貼り付け、Webサイトが表示されるかどうかを確認します。 表示されない場合は、URLパスで誤りがないことを再度確認してください。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

## エントリポイントWebページには、Webサイト上の他のページへのリンクが含まれていますか。{#section_1C2D6ED54E7249268B555D9DC33352B3}

サイト検索/マーチャンダイジングロボットは、顧客と同じようにWebサイトをクロールします。ページ間のリンクをたどる方法。 検索ロボットがサイト上の他のページを見つけてインデックスを付けるには、エントリポイントWebページにリンクが存在する必要があります。

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## Webサイト上の他のページへのリンクはJavaScriptに埋め込まれていますか。{#section_EE34A67D60A844EBB0921C03544FF63E}

JavaScriptを使用して他のページにリンクするロールオーバーアクションやメニューなど、Webサイト上で高度なナビゲーションテクニックを使用できます。 ただし、サイト検索/マーチャンダイジングロボットは、JavaScriptに埋め込まれたリンクをたどることはできません。

この問題の解決に使用できる解決策の1つは、JavaScriptを含むHTML内の他のページへの非表示のリンクを配置することです。 Webサイトのユーザーにはこれらのリンクは表示されませんが、検索ロボットはリンクを見つけてクロールします。 ページの下部の`</body>`タグの直前に、非表示のタグを配置できます。 次のようになります。

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

もう1つの解決策は、Webサイト上の追加ページのURLをクロールとインデックスのエントリポイントとしてリストすることです。 次に示すように、URLの先頭は`https://`にします。

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

[インデックスを作成する複数のURLエントリポイントの追加](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)を参照してください。

## Webページ上のHTMLタグのシーケンスが無効ですか。{#section_F31A2F5D2C284AC084158A5BD763DC5D}

HTMLの仕様では、`<html>`、`<head>`および`<body>`タグがHTMLドキュメント内の特定のシーケンスに従っている必要があります。 すべてのWebページのタグは、次の順序で記述する必要があります。

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

HTMLタグの順序が正しくない場合、サイト検索/マーチャンダイジングロボットはWebページの解析とインデックス作成を適切に行えません。 次の例は、適切な順序にないタグの例です。

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

この場合、`<html>`、`<head>`および`<body>`タグをWebページ上の適切なシーケンスに配置します。

## Webページで、HTMLコメントタグの形式が正しくない。{#section_D1C39D79341845CB9C38579AABDF3A24}

Webページでは、無効なHTMLコメントを注意深く確認し、修正してください。

HTMLの仕様では、HTMLコメントは`<!--`で始まり`-->`で終わる必要があります。 形式が間違っているコメントを見過ごすと、サイト検索/マーチャンダイジングロボットがWebページ上のタグを誤って解析する原因になります。 コメントが不適切に形成されると、サイト検索/マーチャンダイジングロボットが、解析が必要な他の重要なタグを見逃す原因となる場合があります。 Webページの`<body>`タグの直前にあるコメントに気をつけてください。

次に、適切に形成されたコメントの例を示します。

`<!-- This HTML comment is OK. -->`

次の例は、コメントの形式が不適切な場合を示しています。

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Webページに、別のドメインのページへのリンクが含まれているか。{#section_F8082759184049AAA8FA6342C1F84389}

多くの場合、Webサイトは、Webサーバー上に実際に存在し、異なるドメインアドレスを持つページで構成されます。 例えば、メインWebサイトのアドレスが次のような場合、

`https://www.mydomain.com/`

また、Webサイトの別のドメインに次のようなページがある場合もあります。

`https://www.otherdomain.com/`

デフォルトでは、サイト検索/マーチャンダイジングロボットは、メインのドメイン以外のドメインのリンクをたどりません。 ただし、検索アカウントに追加のエントリポイントを設定すると、複数のドメインのインデックスを簡単に作成できます。

製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 サイト追加の「メインWebサイトエントリポイント」URL。 次に、サイトページを含む他のドメインにURL入力ポイントを追加します。 例えば、メインURL入力ポイントを次のように設定します。

`https://www.mydomain.com/`

次のサイトURL入力ポイントを追加します。

`https://www.otherdomain.com/`

## URLに仮想ドメインサービスを使用しているか。{#section_2861F09EA21A45E6B7E15F032739CDF3}

仮想ドメインサービス（「ドメインリダイレクトサービス」とも呼ばれます）を使用して、顧客がWebサイトにアクセスするためのより優れたURLを提供している可能性があります。 例えば、Webサイトの実際のアドレスが次のような場合、

`https://www.myispdomain.com/~myname/mywebpages/`

ただし、仮想ドメインサービスを使用すると、顧客が次のアドレスでサイトにアクセスできるようになります。

`https://myname.adomain.com/`

 または

`https://adomain.com/myname/`

デフォルトでは、サイト検索/マーチャンダイジングロボットは、メインのドメイン以外のドメインのリンクをたどりません。 ただし、検索アカウントに追加のエントリポイントを設定すると、複数のドメインのインデックスを簡単に作成できます。

製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 「追加main webサイトURL」エントリポイントは、サイトの仮想ドメイン名を示します。 次に、Webサイトが実際に存在するドメインにエントリポイントを追加します。

例えば、メインURLのエントリポイントを次のように設定します。

`https://myname.adomain.com/`

次のWebサイトのURL入力ポイントを追加します。

`https://www.myispdomain.com/~myname/mywebpages/`

## Webページでメタ更新タグを使用しているか。{#section_5A2F544C237C49B8B1A7FE0C45371C0D}

多くのWebサイトには、次のような`<head>...</head>`タグの間にメタ更新タグを含むフロントページがあります。

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

状況によっては、サイト検索/マーチャンダイジングロボットがメタ更新URLに従ってWebサイトのコンテンツのインデックスを作成できない場合があります。 この問題は、追加のエントリポイントを設定することで、簡単に対処できます。

製品メニューで、**[!UICONTROL Settings]**/クロール/**[!UICONTROL URL Entrypoints]**&#x200B;をクリックします。 meta refreshタグのURL追加への別のエントリポイント。

## Webページでメタロボットタグを使用しているか。{#section_36275A33DDFE4620BABA948F8A63DBD2}

Webページでは、メタロボットタグを使用して、Webサイトを定期的にクロールしようとするWebロボットを制御する場合があります。 Webページの`<head>...</head>`タグの間にメタロボットタグが表示されるのは、次のタグのようです。

`<meta name="robots" content="noindex, nofollow">`

サイト検索/マーチャンダイジングロボット自体がWebロボットなので、meta robotsタグの指示に従います。 このように他のロボットを除外すると、サイト検索/マーチャンダイジングロボットも除外されます。

WebロボットとRobots Exclusion Protocolについて詳しくは、次を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Webサイトでインデックスを作成するWebページのメタロボットタグを削除または変更します。

## Webサイトでロボットの除外ファイルを使用しているか。{#section_BF7B663347814F58AD736066C86B7D25}

Webサイトには、robots.txtという名前のページがあり、すべてのまたは特定のロボットがこのページをクロールできない場合があります。 Webサイトにrobots.txtファイルがあるかどうかを確認するには、次に示すように、最上位ドメインの直下にあるファイルを探します。

`https://www.yourdomain.com/robots.txt`

robots.txtファイルの内容は次のテキストのようになります。

```
User-agent: * 
Disallow: /
```

サイト検索/マーチャンダイジングロボットはWebロボットなので、robots.txtファイルの指示に従います。サイト検索/マーチャンダイジングロボットは除外されます。 この問題を回避するには、robots exclusionファイル(robots.txt)を編集し、サイト検索/マーチャンダイジングロボットが次のようにWebサイトをクロールし、インデックスを作成できるようにします。

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Webサイト上のMicrosoft® Officeファイルのインデックス作成と検索のサポートについて説明するよくある質問ページです。

Microsoft Officeファイルに関するよくある質問は次のとおりです。

* [Microsoft Officeファイルでインデックスを作成する](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Microsoft Officeファイルでインデックスを作成しないもの](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [HTMLページとは異なる方法でMicrosoft Officeファイルのインデックスを作成する方法](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Microsoft Officeファイルのインデックスが作成されないようにする方法](#section_FEBA71274CD14CB99731ADF982087F4C)

## Microsoft Officeファイルでインデックスを作成する{#section_8681DADFCFE24B7787B1FC08D431EE28}

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

## Microsoft Officeファイルでインデックスを作成しない{#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Microsoft Officeファイルに含まれるグラフィック、または含まれるグラフィックの一部であるテキストは、インデックス付けされません。 カスタムプロパティ定義は、メタデータとしてインデックス化されません。 PowerPointファイル内のヘッダーやフッターなど、特殊フィールド内のテキストにも、インデックスが作成されないものがあります。

## Microsoft Officeファイルのインデックスの作成方法を、HTMLページとは異なる方法で指定します。{#section_C104B44684F340549A6B9EB8F39EDDBB}

検索ロボットがMicrosoft OfficeファイルとHTMLファイルをインデックス付けする方法の違いは、各HTMLファイルが1ページずつで、1つのMicrosoft Officeファイルが数百ページを表すことがある点です。 このため、各ページはMicrosoft Officeファイル内で検索アカウントの下にある個別のページとしてカウントされます。

## Microsoft OfficeファイルのインデックスがWebサイト上で作成されないようにする方法{#section_FEBA71274CD14CB99731ADF982087F4C}

検索ロボットでMicrosoft Officeファイルのクロールとインデックス作成を行わない場合は、コンテンツタイプ&#x200B;**[!UICONTROL Microsoft Office Files]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)の選択を解除します。

[!DNL URL Masks]を使用して、Microsoft Officeファイルのインデックス作成を無効にすることもできます。

次のURLマスクを入力します。

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>正規式を使用しない場合 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclude *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">exclude *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">exclude *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>正規式を使用している場合 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">regexp ^を除外します。*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">regexp ^を除外します。*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">regexp ^を除外します。*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

[インデックス部分へのURLマスクの追加を参照してください…](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Webサイト上のMP3音楽ファイルのインデックス作成と検索のサポートについて説明する、よくある質問ページです。

MP3ファイルに関するよくある質問を次に示します。

* [MP3ファイルは、いつクロールされ、インデックス化されますか？](#section_538EA1682C9C47E3A62640BB25D84C36)
* [クロールしてインデックスを付けるには…](#section_3CD794446E3545379C14E9F222118665)
* [MP3ファイルはどのように認識されますか？](#section_230E7336965A424F96C5CCF1D3C2D103)
* [MP3ファイル内のインデックスとは何ですか。](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [MP3ファイルは1ページとしてカウントされますか。](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [個々のMP3ファイルのインデックス作成を防ぐ方法](#section_C989DC1D3D3841B38F683A462195DC05)
* [MP3ファイルのインデックスが作成されないようにする方法](#section_305D2B28D1124776B6DC0C62A17827C6)
* [サイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## MP3ファイルは、いつクロールされ、インデックス化されますか？{#section_538EA1682C9C47E3A62640BB25D84C36}

MP3ファイルは、2つの方法のいずれかでクロールおよびインデックス付けされます。 最も一般的な方法は、HTMLファイル内のアンカーhrefタグを使用する方法です。

`<a href="MP3-file-URL"></a>`

2つ目の方法は、MP3ファイルのURLをURL入力ポイントとして入力する方法です。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

## サイト上のMP3ファイルをクロールしてインデックスを作成するには、何をする必要がありますか。{#section_3CD794446E3545379C14E9F222118665}

アカウントのMP3クロールおよびインデックスをアクティブにするには、製品メニューで&#x200B;**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Content Types]**&#x200B;をクリックします。 [!DNL Staged Content Types]ページで&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;を選択します。

「[コンテンツタイプについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)」を参照してください。

## MP3ファイルはどのように認識されますか？{#section_230E7336965A424F96C5CCF1D3C2D103}

MP3ファイルは、「audio/mpeg」のMIMEタイプで認識されます。

## MP3ファイル内のインデックスとは何ですか。{#section_E99D252B27CA4946AED3FCD3ABD8779D}

MP3ファイルには、必要に応じて少量のテキスト情報が格納されます。 この情報には、アルバム名、アーティスト名、曲のタイトル、曲のジャンル、リリース年度、コメントが含まれます。 この情報は、ファイルの最後（TAGと呼ばれる場所）に保存されます。 TAG情報を含むMP3ファイルのインデックスは、次のように作成されます。

* 曲のタイトルは、HTMLページのタイトルのように扱われます。
* コメントは、HTMLページに対して定義された説明と同様に扱われます。
* このジャンルは、HTMLページに対して定義されたキーワードと同様に扱われます。
* アーティスト名、アルバム名およびリリース年は、HTMLドキュメントの本文と同様に扱われます。

## MP3ファイルは1ページとしてカウントされますか。{#section_9910BEB6617D4D2090558CDF6C65D16B}

はい。Webサイト上でクロールされ、インデックスが作成された各MP3ファイルは、1ページとしてカウントされます。

## 個々のMP3ファイルのインデックスを作成しない方法を教えてください。{#section_C989DC1D3D3841B38F683A462195DC05}

MP3ファイルにリンクするアンカータグを`<nofollow>`タグと`</nofollow>`タグで囲みます。 検索ロボットは、これらのタグ間のリンクをたどりません。

もう1つの方法は、MP3ファイルのURLを除外マスクとして追加することです。

[URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

[URLマスクスクリプトについて](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)を参照してください。

## MP3ファイルのインデックスが作成されないようにする方法{#section_305D2B28D1124776B6DC0C62A17827C6}

アカウントのMP3インデックスを制御する最も簡単な方法は、[!DNL Staged Content Types]ページで&#x200B;**[!UICONTROL Text in MP3 Music Files]**&#x200B;を選択解除することです。

[クロールおよびインデックスを作成するコンテンツタイプの選択](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)を参照してください。

また、URLマスク機能を使用して、ファイル拡張子によるMP3インデックス作成を無効にすることもできます。 これを行うには、製品メニューで&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;をクリックします。 次のいずれかのマスクを入力します。

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>アカウントが </p> </th> 
   <th colname="col2" class="entry"> <p>次のURLマスクを入力します </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>正規式を使用しない </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclude *.mp3  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>正規式を使用 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> regexp ^を除外します。*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

## サイトで中国語、日本語、韓国語のMP3ファイルを検索できないのはなぜですか。{#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

中国語、日本語、または韓国語のMP3ファイルを検索するには、製品メニューで&#x200B;**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL Content Types]**/**[!UICONTROL Text in MP3 Music Files]**&#x200B;をクリックします。 次に、**[!UICONTROL Settings]**/**[!UICONTROL Metadata]**/**[!UICONTROL Injections]**&#x200B;をクリックし、MP3ファイルのエンコードに使用する文字セットを指定します。

[クロールおよびインデックスを作成するコンテンツタイプの選択](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)を参照してください。

[インジェクションについて](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)を参照してください。

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Webサイト上のPDFファイルのインデックス作成と検索のサポートについて、よくある質問ページを紹介します。

PDFファイルに関してよく寄せられる質問は次のとおりです。

* [PDFファイル内のインデックス付けの対象](#section_62BFCD7158B44F2BB3B1864224B50174)
* [PDFファイルでインデックスが作成されないのは何ですか。](#section_A14B353AE503408896BACBBF3F748FA0)
* [インデックス付きPDFファイルはどのようにカウントされますか？](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [検索結果にPDFアイコンを表示できますか。](#section_829CE82CC3544502A13D27C4DB820189)
* [検索結果が次の特定のページにリンクするか…](#section_A06E7F7017E6441E98209D288EE57BF6)
* [PDFファイルのインデックスが作成されないようにする方法を教えてください。](#section_96671419A822486AAC654D8DAD819940)
* [Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## PDFファイル内のインデックス付けの対象{#section_62BFCD7158B44F2BB3B1864224B50174}

PDFファイルの完全なコンテンツのインデックスが作成されます。 PDFファイルの次の部分のインデックスが作成されます。

* タイトル
* キーワード
* 件名（説明）
* テキストベースのコンテンツ

## PDFファイルでインデックスが作成されないのは何ですか。{#section_A14B353AE503408896BACBBF3F748FA0}

PDF目次、ファイル内のグラフィック、または含まれるグラフィックの一部であるテキストのインデックスは作成されません。

## インデックス付きPDFファイルはどのようにカウントされますか？{#section_C35DE36A65D649BD8FF314E9EFD990A6}

複数のページを含むPDFを含む各PDFファイルは、1つのドキュメントとしてカウントされます。

## 検索結果にPDFアイコンを表示できますか。{#section_829CE82CC3544502A13D27C4DB820189}

はい。テンプレート内で`<search-if-link-extension>`タグを使用して、PDFアイコンや他のグラフィックやテキストを検索結果に含めます。

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

PDFアイコンは、検索結果が非常に大きい可能性のあるPDFファイルにリンクしていることを顧客が知るのに役立ちます。 モデム経由でWebサイトにアクセスしているユーザーやモバイルデバイスからアクセスしているユーザーは、ファイルサイズが問題になる場合があります。

## 検索結果はPDFファイル内の特定のページにリンクできますか。{#section_A06E7F7017E6441E98209D288EE57BF6}

はい。スマートリンクテンプレートタグ(`<search-smart-link>...</search-smart-link>`)を使用すると、検索結果を含む最初のPDFページをクリックして開くことができます。

スマートリンクを使用するには、テンプレートの検索結果セクションにある`<search-link>...</search-link>`タグを`<search-smart-link>...</search-smart-link>`タグに置き換えます。 顧客は、スマートリンクタグによって生成されるリンクをクリックすると、検索クエリに関連する最初のPDFページに移動します。

>[!NOTE]
>
>この機能を使用するには、お客様が最新バージョンのAdobe AcrobatまたはAdobe AcrobatReaderを使用する必要があります。このバージョンには、ハイライトプラグインと外部ウィンドウハンドラ(EWH)プラグインが含まれている必要があります。 また、WebブラウザーでNetscape Navigator用のAdobe Acrobatプラグイン（このNetscape Navigatorプラグインを受け入れる任意のブラウザーを使用できます）またはInternet Explorer 4.0以降用のAcrobatActiveXコントロールを使用する必要があります。

[検索テンプレートタグ](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)を参照してください。

## PDFファイルのインデックスがWebサイト上で作成されないようにするには、どうすればよいですか。{#section_96671419A822486AAC654D8DAD819940}

検索ロボットでPDFファイルのクロールとインデックス作成を行わない場合は、コンテンツタイプ&#x200B;**[!UICONTROL PDF Documents]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)の選択を解除します。

また、[!DNL URL Masks]を使用してPDFインデックスを無効にすることもできます。

[インデックス部分へのURLマスクの追加を参照してください…](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

PDFインデックスを無効にするには、次のURLマスクのいずれかを入力します。

* `exclude *.pdf` (正規式を使用しない場合)
* `exclude regexp ^.*\.pdf$` (正規式を使用している場合)

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

## Webサイトで中国語、日本語、韓国語のPDFファイルを検索できないのはなぜですか。{#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

サイト検索/マーチャンダイジングは、言語を示さないPDFファイルからUTF-8を取得します。 コンテンツタイプ&#x200B;**[!UICONTROL PDF Documents]**(**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)を選択した場合は、メタデータインジェクションを使用して、PDFファイルで使用する言語を指定する必要があります。

[フィールドインジェクション定義の追加](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)を参照してください。

## ページが多すぎます{#reference_48A748BC1ED14844ACAC2735C8388E8A}

インデクサーが実際のページ数よりも多くページをカウントした理由と、各ケースでの解決策の一部を説明する、よくある質問ページです。

Webサイトがページ数の制限を下回っていることが確実で、インデクサーが上限に達したと伝える場合は、考えられる解決策について、次のような一般的な質問と回答を確認する必要があります。

* [様々なインデックス・ログを調べましたか。](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [CGIプログラムのインデックスをWebサイト上で作成しているか。](#section_86ED8A641B3841EC80153B4F107548FD)
* [サーバーでディレクトリの参照が有効になっているか。](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Webサイトにフォーラムまたはニュースグループがありますか。](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [WebサイトにPDFまたはMicrosoft Officeファイルがあるかどうか…](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [複数のURL入力ポイントがあるか。](#section_8C54AFD7DF56472A9364D516482B534C)
* [の内部バイト数または時間制限を超えています…](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## 様々なインデックス・ログを調べましたか。{#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

インデックスログには、Webサイトのインデックスの作成時にサイト検索/マーチャンダイジングロボットによって収集された詳細情報が含まれます。 ログには、クロールされたすべてのリンクのリストと発生したエラーが含まれます。 インデックスを作成するページを判断する際には、インデックスログを調べるのが開始に最適な場所です。

[ライブまたはステージングされた完全なインデックスログの表示を参照してください…](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

[ライブまたはステージングされたインクリメンタルインデックスログの表示を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

[ライブまたは…のスクリプト増分インデックスログの表示を参照してください。](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

[ライブまたはステージングされたインデックスの再生成ログの表示を参照してください。](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

[ライブまたはステージングされたWebサイトの再ランク付けインデックスログの表示](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D)を参照してください。

## CGIプログラムのインデックスをWebサイト上で作成しているか。{#section_86ED8A641B3841EC80153B4F107548FD}

CGIプログラムはURLパラメーターを使用するので、インデクサーが複数の「偽」のURLをクロールする場合があります。 サイト検索/マーチャンダイジングがCGIプログラムを読み取り、その後にCGIパラメータを含むURLを読み取る場合、クロールおよびインデックス付けされているページの数倍が検索インデックスに役立ちません。 一般的なCGIパラメーターは、`?`または`&`文字のURLで表示されます。

URLマスク機能を使用して、CGIプログラムのインデックスが作成されないようにマスクできます。 URLプレフィックスをマスクしたり、正規式を使用してCGIスクリプトをマスクしたりできます。

[URLマスクについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)を参照してください。

[URLマスクスクリプトについて](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)を参照してください。

[正規式](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)を参照してください。

## サーバーでディレクトリの参照が有効になっているか。{#section_073C88EEE74F4CA0AD2C7145D4810B22}

Webサーバーでディレクトリの参照が有効になっていて、特定のディレクトリにindex.htmlファイルが存在しない場合、そのディレクトリへのアクセスによって、そのディレクトリ内のファイルの一覧が表示されます。 通常、ページの上部には、**[!UICONTROL Name]**、**[!UICONTROL Last modified]**、**[!UICONTROL Size]**&#x200B;などをクリックするだけで、リストを異なる方法で並べ替えるためのリンクがあります。 通常、これらはサイト検索/マーチャンダイジングインデックスログに`?M=A`などの文字を含むURLとして表示されます。 サイト検索/マーチャンダイジングインデクサーはリンクとしてこれらに従うので、複数の「疑似」URLにインデックスを付ける可能性があります。

通常、適切に設計されたWebサイトでは、すべてのディレクトリにインデックスファイルが存在するか、インデックスファイルのないディレクトリのディレクトリ参照が無効になっています。 幸いにも、ページを変更できない場合や、サーバ側のディレクトリリストを無効にできない場合は、これらの「偽」のURLを隠す簡単な方法があります。

このタスクを実行するには、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;をクリックします。 &lt;a0追加/>という文字を含むURLをマスクするマスク。 `?`このタスクは、次の正規式マスクを入力して行うことができます。

`exclude regexp ^.*\?.*$`

マスクを作成した後は、Webサイトのインデックスを再作成してください。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Webサイトにフォーラムまたはニュースグループがありますか。{#section_8DCB94F0850A41B9B2EA885F779E2F84}

Webサイト上でフォーラムまたはニュースグループをクロールする場合、様々な表示オプションや並べ替えオプションで、URLをフォローしている可能性があります。 つまり、同じページのインデックスが複数回作成されます。

通常、フォーラムやニュースグループには独自の検索エンジンが付属しています。 その場合は、[!DNL URL Masks]を使用して、サイト検索/マーチャンダイジングでフォーラムをマスクできます。

製品メニューで、**[!UICONTROL Settings]**/**[!UICONTROL Crawling]**/**[!UICONTROL URL Masks]**&#x200B;をクリックします。 [!DNL Staged URL Masks]ページで、URLマスクを除外としてURLを入力して、フォーラムをマスクします。

[インデックス部分へのURLマスクの追加を参照してください…](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

マスクを作成した後は、必ずWebサイトのインデックスを再作成してください。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

[ライブまたはステージングされたWebサイトの増分インデックスの実行を参照してください…](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## WebサイトにPDFファイルまたはMicrosoft Officeファイルがありますか。{#section_455FC5438DF74E68AB9A31D359EAD4D9}

WebサイトにPDFファイルまたは[!DNL Microsoft Office]ファイルがある場合、少数のファイルのインデックスサイズで多くのページがカウントされることに気づくかもしれません。 インデックスが作成されるページ数がドキュメント数よりも多いのは、PDFまたはMicrosoft Officeファイル内の各ページが個別のページとしてカウントされるためです。

製品メニューで、**[!UICONTROL Index]**/**[!UICONTROL Full Index]**/**[!UICONTROL Live Index]**&#x200B;をクリックします。 [!DNL Full Index]ページで、「**[!UICONTROL Count All Pages]**」を選択し、「**[!UICONTROL Full Index Now]**」をクリックして合計ページ数を表示します。 PDFファイルまたはMicrosoft Officeファイルのインデックスを作成しない場合は、**[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;でこのコンテンツタイプを無効にできます。

[ライブまたはステージングされたWebサイトの完全なインデックスの実行を参照してください…](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

「[コンテンツタイプについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)」を参照してください。

## 複数のURL入力ポイントがあるか。{#section_8C54AFD7DF56472A9364D516482B534C}

サイト検索/マーチャンダイジングロボットは、指定されたURLエントリポイントからクロールを開始し、見つかったすべてのリンクをそのドメイン内のすべてのコンテンツにたどります。 URL入力ポイントを多数指定した場合は、大量のページがクロールされる可能性があります。

追加ドメインのエントリポイントドキュメントのヘッダーで、Robots Exclusion Protocolの`nofollow`タグを使用します。

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

上記のコードは、サイト検索/マーチャンダイジングロボットに対して、ページのコンテンツのインデックスを作成するように指示していますが、追加のページへのリンクに従わないように指示しています。

WebロボットとRobots Exclusion Protocolについて詳しくは、次を参照してください。

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

追加のドメインのページのソースにアクセスできない場合は、複数のURL入力ポイントを削除できます。 これにより、ユーザーが検索できるコンテンツを望むドメインに対してのみインデックス作成のアクティビティを制限できます。

[URL入力ポイントについて](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)を参照してください。

## サイト検索/マーチャンダイジングの内部バイト数または時間制限を超えたか。{#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

[フルインデックスステータス]画面で、アカウントが上限に達したかどうかを確認します。 インデックスのサイズが許可されている値を超えている、または許容される値より長い時間がかかったとステータスレポートに表示された場合、Webサイトのインデックスは完全には作成されません。 このエラーを修正して、Webサイトのページを適切にカバーし、数えることができます。

サイト検索/マーチャンダイジングサーバーを保護するため、バイトと時間には内部的な制限があります。 クロールされたファイルが非常に大きい場合、またはサイト検索/マーチャンダイジングが到達しようとしているサーバーの速度が遅い場合にのみ、これらの制限に達します。

時間制限に達した場合は、サーバーがオンラインであることを確認し、後でインデックスを再試行します。 バイト数の制限に達した場合は、インデックスログを表示して、クロールされたファイルを確認します。 異常に大きい？ 次のいずれかのメッセージが表示された場合は、テクニカルサポートにお問い合わせください。
